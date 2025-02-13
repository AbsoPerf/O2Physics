# Copyright 2019-2020 CERN and copyright holders of ALICE O2.
# See https://alice-o2.web.cern.ch/copyright for details of the copyright holders.
# All rights not expressly granted are reserved.
#
# This software is distributed under the terms of the GNU General Public
# License v3 (GPL Version 3), copied verbatim in the file "COPYING".
#
# In applying this license CERN does not waive the privileges and immunities
# granted to it by virtue of its status as an Intergovernmental Organization
# or submit itself to any jurisdiction.


if(FastJet_FOUND)

o2physics_add_dpl_workflow(jet-deriveddata-producer
                    SOURCES jetderiveddataproducer.cxx
                    PUBLIC_LINK_LIBRARIES O2::Framework O2Physics::PWGJECore O2Physics::AnalysisCore
                    COMPONENT_NAME Analysis)

o2physics_add_dpl_workflow(jet-deriveddata-trigger-producer
                    SOURCES jetderiveddatatriggerproducer.cxx
                    PUBLIC_LINK_LIBRARIES O2::Framework O2Physics::PWGJECore O2Physics::AnalysisCore
                    COMPONENT_NAME Analysis)

                    o2physics_add_dpl_workflow(jet-deriveddata-producer-dummy
                    SOURCES jetderiveddataproducerdummy.cxx
                    PUBLIC_LINK_LIBRARIES O2::Framework O2Physics::PWGJECore O2Physics::AnalysisCore
                    COMPONENT_NAME Analysis)

o2physics_add_dpl_workflow(jet-deriveddata-writer
                    SOURCES jetderiveddatawriter.cxx
                    PUBLIC_LINK_LIBRARIES O2::Framework O2Physics::PWGJECore O2Physics::AnalysisCore
                    COMPONENT_NAME Analysis)

o2physics_add_dpl_workflow(jet-finder
                    SOURCES jetfinder.cxx
                    PUBLIC_LINK_LIBRARIES O2::Framework O2Physics::PWGJECore O2Physics::AnalysisCore
                    COMPONENT_NAME Analysis)

o2physics_add_dpl_workflow(jet-finder-d0-data-charged
                    SOURCES jetfinderD0DataCharged.cxx
                    PUBLIC_LINK_LIBRARIES O2::Framework O2Physics::PWGJECore O2Physics::AnalysisCore O2::FrameworkPhysicsSupport
                    COMPONENT_NAME Analysis)

o2physics_add_dpl_workflow(jet-finder-d0-mcd-charged
                    SOURCES jetfinderD0MCDCharged.cxx
                    PUBLIC_LINK_LIBRARIES O2::Framework O2Physics::PWGJECore O2Physics::AnalysisCore O2::FrameworkPhysicsSupport
                    COMPONENT_NAME Analysis)

o2physics_add_dpl_workflow(jet-finder-d0-mcp-charged
                    SOURCES jetfinderD0MCPCharged.cxx
                    PUBLIC_LINK_LIBRARIES O2::Framework O2Physics::PWGJECore O2Physics::AnalysisCore O2::FrameworkPhysicsSupport
                    COMPONENT_NAME Analysis)

o2physics_add_dpl_workflow(jet-matching-mc
                    SOURCES jetmatchingmc.cxx
                    PUBLIC_LINK_LIBRARIES O2::Framework O2Physics::PWGJECore O2Physics::AnalysisCore
                    COMPONENT_NAME Analysis)

o2physics_add_dpl_workflow(jet-matching-sub
                    SOURCES jetmatchingsub.cxx
                    PUBLIC_LINK_LIBRARIES O2::Framework O2Physics::PWGJECore O2Physics::AnalysisCore
                    COMPONENT_NAME Analysis)

o2physics_add_dpl_workflow(jet-matching-mc-sub
                    SOURCES jetmatchingmcsub.cxx
                    PUBLIC_LINK_LIBRARIES O2::Framework O2Physics::PWGJECore O2Physics::AnalysisCore
                    COMPONENT_NAME Analysis)

o2physics_add_dpl_workflow(jet-eventweight-mcd
                    SOURCES jeteventweightmcd.cxx
                    PUBLIC_LINK_LIBRARIES O2::Framework O2Physics::PWGJECore O2Physics::AnalysisCore
                    COMPONENT_NAME Analysis)

o2physics_add_dpl_workflow(jet-eventweight-mcp
                    SOURCES jeteventweightmcp.cxx
                    PUBLIC_LINK_LIBRARIES O2::Framework O2Physics::PWGJECore O2Physics::AnalysisCore
                    COMPONENT_NAME Analysis)

o2physics_add_dpl_workflow(jet-track-derived
                    SOURCES jettrackderived.cxx
                    PUBLIC_LINK_LIBRARIES O2::Framework O2Physics::PWGJECore O2Physics::AnalysisCore
                    COMPONENT_NAME Analysis)

o2physics_add_dpl_workflow(jet-taggerhf
                    SOURCES jettaggerhf.cxx
                    PUBLIC_LINK_LIBRARIES O2::Framework O2Physics::PWGJECore O2Physics::AnalysisCore
                    COMPONENT_NAME Analysis)

o2physics_add_dpl_workflow(estimator-rho
                    SOURCES rhoEstimator.cxx
                    PUBLIC_LINK_LIBRARIES O2::Framework O2Physics::PWGJECore O2Physics::AnalysisCore
                    COMPONENT_NAME Analysis)

o2physics_add_dpl_workflow(subtractor-eventwiseconstituent
                    SOURCES eventwiseConstituentSubtractor.cxx
                    PUBLIC_LINK_LIBRARIES O2::Framework O2Physics::PWGJECore O2Physics::AnalysisCore
                    COMPONENT_NAME Analysis)
endif()


o2physics_add_dpl_workflow(emcal-correction-task
                    SOURCES emcalCorrectionTask.cxx
                    PUBLIC_LINK_LIBRARIES O2::Framework O2Physics::AnalysisCore O2::DetectorsBase O2::EMCALBase O2::EMCALReconstruction
                    COMPONENT_NAME Analysis)

o2physics_add_dpl_workflow(emcal-matchedtracks-writer
                    SOURCES emcalMatchedTracksTask.cxx
                    PUBLIC_LINK_LIBRARIES O2::Framework O2Physics::AnalysisCore O2::DetectorsBase O2::EMCALBase O2::EMCALReconstruction
                    COMPONENT_NAME Analysis)
