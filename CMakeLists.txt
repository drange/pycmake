#  Copyright (C)  2016 Statoil ASA, Norway.
#                      Pål Grønås Drange <PGDR@statoil.com>
#
#  This file is part of ERT - Ensemble based Reservoir Tool.
#
#  ERT is free software: you can redistribute it and/or modify it under the
#  terms of the GNU General Public License as published by the Free Software
#  Foundation, either version 3 of the License, or (at your option) any later
#  version.
#
#  ERT is distributed in the hope that it will be useful, but WITHOUT ANY
#  WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR
#  A PARTICULAR PURPOSE.
#
#  See the GNU General Public License at <http://www.gnu.org/licenses/gpl.html>
#  for more details

cmake_minimum_required (VERSION 2.8.1)
project (PYTHON_MODULE_VERSIONS)
find_package( PythonInterp 2.6 REQUIRED )

include(pycmake.cmake)

#
# Using the above features
#

python_module( matplotlib REQUIRED 1.2.0  MINIMUM                    )
python_module( numpy      REQUIRED 1.8.2  EXACT                      )
python_module( pandas     REQUIRED 0.15.1                            )
python_module( PyQt4      REQUIRED 4.8.0                             )
python_module( PyQt4.Qt   REQUIRED 4.8.0  MINIMUM "PYQT_VERSION_STR" )
python_module( PyQt4.Qt   REQUIRED 4.8.0  MINIMUM   "QT_VERSION_STR" )
python_module( re         REQUIRED 2.2.1  MINIMUM                    )
python_module( requests   REQUIRED 2.2.1  EXACT   "__version__"      )
python_module( inspect    REQUIRED                                   )
#python_module(no_such    OPTIONAL 0.0.1  MINIMUM                    )
