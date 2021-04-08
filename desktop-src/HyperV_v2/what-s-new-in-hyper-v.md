---
description: Version 2 des Hyper-V-WMI-Anbieters ist für Windows 8 und Windows Server 2012 neu.
ms.assetid: A91ACF7A-AFE6-45B6-960C-C4AAA0083735
title: Neuerungen beim Hyper-V-WMI-Anbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce222fd18955e88b9e33e1b706cf81ef5a806917
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866380"
---
# <a name="whats-new-in-hyper-v-wmi-provider"></a>Neues in Hyper-V-WMI-Anbieter

Version 2 des Hyper-V-WMI-Anbieters ist für Windows 8 und Windows Server 2012 neu.

## <a name="windows-10-version-1709"></a>Windows 10, Version 1709

Neue Klassen:

-   [**MSVM- \_ Akku**](msvm-battery.md)
-   [**MSVM- \_ batterysettingdata**](msvm-batterysettingdata.md)
-   [**MSVM \_ persistentmemorycontroller**](msvm-persistentmemorycontroller.md)

Neue Eigenschaften:

-   [**MSVM \_ Collectionreferencepointexportjob**](msvm-collectionreferencepointexportjob.md): **exportedgueststatefilepath**
-   [**MSVM \_ Ethernetwitchhardwareoffloaddata**](msvm-ethernetswitchhardwareoffloaddata.md): **defaultqueuevrssindependenthostdisposition**, **defaultqueuevrssexclugelimaryprocessor**, **defaultqueuevrssqueueschedulingmode** und **defaultqueuevrssminqueuepairs**
-   [**MSVM \_ Ethernetwitchhardwareoffloadsettingdata**](msvm-ethernetswitchhardwareoffloadsettingdata.md): **defaultqueuevrssindependenthostdisposition**, **defaultqueuevrssexclugelimaryprocessor**, **defaultqueuevrssqueueschedulingmode**, **defaultqueuevrssminqueuepairs**,
-   [**MSVM \_ Ethernezwitchportoffloaddata**](msvm-ethernetswitchportoffloaddata.md): **vrssvmbuschannelaffinitypolicy**, **vrssindependenthostdisposition**, **vrssexclugelimaryprocessor**, **vrssqueueschedulingmodes** und **vrssminqueuepairs**
-   [**MSVM \_ Virtualharddisksettingdata**](msvm-virtualharddisksettingdata.md): **dataalignment**, **pmemaddressabstractiontype** und **ispmemcompatible**
-   [**MSVM \_ Virtualsystemexportsettingdata**](msvm-virtualsystemexportsettingdata.md): **disabledifferenalofignoredstorage** und **excludedvirtualharddisks**
-   [**MSVM \_ Virtualsystemmanagementservicesettingdata**](msvm-virtualsystemmanagementservicesettingdata.md): **hypervisorrootscheduleraktivierte**
-   [**MSVM \_ Virtualsystemmigrationsettingdata**](msvm-virtualsystemmigrationsettingdata.md): **cpucappingmagnitude** und **cancelifblackoutcedoldexceging**
-   [**MSVM \_ Virtualsystemreferencepointexportjob**](msvm-virtualsystemreferencepointexportjob.md): **exportedgueststatefilepath**
-   [**MSVM \_ Virtualsystemsettingdata**](msvm-virtualsystemsettingdata.md): **Architecture**, **automaticsnapshotsenabled**, **isautomaticsnapshot**, **gueststatefile** und **gueststatedataroot**

## <a name="windows-10-version-1703"></a>Windows 10, Version 1703

Neue Klassen:

-   [**MSVM zugewiesen \_ abledevicedismountsettingdata**](msvm-assignabledevicedismountsettingdata.md)
-   [**MSVM zugewiesen \_ abledebug Service**](msvm-assignabledeviceservice.md)
-   [**MSVM \_ collectionreferencepointexportjob**](msvm-collectionreferencepointexportjob.md)
-   [**MSVM \_ ethernezwitchhardwareoffloadsettingdata**](msvm-ethernetswitchhardwareoffloadsettingdata.md)
-   [**MSVM \_ ethernetzwitchportmigrationqossettingdata**](msvm-ethernetswitchportmigrationqossettingdata.md)
-   [**MSVM \_ ethernetzwitchportrdmasettingdata**](msvm-ethernetswitchportrdmasettingdata.md)
-   [**MSVM \_ ethernetzwitchportteammappingsettingdata**](msvm-ethernetswitchportteammappingsettingdata.md)
-   [**MSVM- \_ gpupartition**](msvm-gpupartition.md)
-   [**MSVM \_ gpupartitionsettingdata**](msvm-gpupartitionsettingdata.md)
-   [**MSVM \_ networkconnectiondiagnosticinformation**](msvm-networkconnectiondiagnosticinformation.md)
-   [**MSVM \_ networkconnectiondiagnosticsettingdata**](msvm-networkconnectiondiagnosticsettingdata.md)
-   [**MSVM \_ partitionablegpu**](msvm-partitionablegpu.md)
-   [**MSVM \_ PCIExpress**](msvm-pciexpress.md)
-   [**MSVM \_ PCIExpress SettingData**](msvm-pciexpresssettingdata.md)
-   [**MSVM \_ SecurityElement**](msvm-securityelement.md)
-   [**MSVM- \_ SecurityService**](msvm-securityservice.md)
-   [**MSVM \_ securitysettingdata**](msvm-securitysettingdata.md)
-   [**MSVM \_ storagesettingdata**](msvm-storagesettingdata.md)
-   [**MSVM \_ summaryinformationbase**](msvm-summaryinformationbase.md)
-   [**MSVM \_ systemcomponentsettingdata**](msvm-systemcomponentsettingdata.md)
-   [**MSVM \_ virtualsystemreferencepointexportjob**](msvm-virtualsystemreferencepointexportjob.md)
-   [**MSVM \_ virtualsystemreferencepointsettingdata**](msvm-virtualsystemreferencepointsettingdata.md)

Entfernte Klassen:

-   [**MSVM \_ tpmsettingdata**](msvm-tpmsettingdata.md)

Neue Methoden:

-   [**MSVM \_ Collectionsnapshotservice**](msvm-collectionsnapshotservice.md) -Klasse: [ **applysnapshot**](msvm-collectionsnapshotservice-applysnapshot.md)
-   [**MSVM \_ Virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md) -Klasse: [**addsystemcomponentsetting**](msvm-virtualsystemmanagementservice-addsystemcomponentsettings.md), [**diagnosenetworkconnection**](msvm-virtualsystemmanagementservice-diagnosenetworkconnection.md), [**modifysystemcomponentsettings**](msvm-virtualsystemmanagementservice-modifysystemcomponentsettings.md)und [**removesystemcomponentsettings**](msvm-virtualsystemmanagementservice-removesystemcomponentsettings.md)
-   [**MSVM \_ Virtualsystemreferencepointservice**](msvm-virtualsystemreferencepointservice.md) -Klasse: [ **importreferencepointmetadata**](msvm-virtualsystemreferencepointservice-importreferencepointmetadata.md)

Neue Eigenschaften:

-   [**MSVM \_ Ethernezwitchhardwareoffloaddata**](msvm-ethernetswitchhardwareoffloaddata.md): **defaultqueuevmmqqueuepairs**, **defaultqueuevmmqaktivierte** und **defaultqueuevrssssaktivierte**
-   [**MSVM \_ Ethernezwitchportoffloaddata**](msvm-ethernetswitchportoffloaddata.md): **vmmqqueuepairs**, **vmmqaktivierte** und **vrssaktivierte**
-   [**MSVM \_ Ethernezwitchportoffloadsettingdata**](msvm-ethernetswitchportoffloadsettingdata.md): **vmmqqueuepairs**, **vmmqaktivierte** und **vrssaktivierte**
-   [**MSVM \_ Guestclusterinformation**](msvm-guestclusterinformation.md): **lastresourcemuvetime**
-   [**MSVM \_ Kvpexchangecomponentsettingdata**](msvm-kvpexchangecomponentsettingdata.md): **disablehostkvpitems**
-   [**MSVM \_ Memorysettingdata**](msvm-memorysettingdata.md): **sgxsize** und **sgxaktivierte**
-   [**MSVM \_ Physical3dGraphicsProcessor**](msvm-physical3dgraphicsprocessor.md): **compatibleforvirtualization** und **drivermodelversion**
-   [**MSVM \_ Processorsettingdata**](msvm-processorsettingdata.md): **hwthreadspercorecpugroupid**, **hidehypervisorpresent** und **exposevirtualizationextensions**
-   [**MSVM \_ Settingsdefinecapabili:**](msvm-settingsdefinecapabilities.md) **supportstatement**
-   [**MSVM \_ Storagezugecationsettingdata**](msvm-storageallocationsettingdata.md): **Beschreib tehardeningmethod**
-   [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md): **abgeschirmt**
-   [**MSVM \_ Syntheticethernetportsettingdata**](msvm-syntheticethernetportsettingdata.md): **allowpacketdirect**
-   [**MSVM \_ Virtualsystemcollection**](msvm-virtualsystemcollection.md): **LastApplyConsistencyLevel**, **lastapplyvirtualmachineids**, **lastapplytime**, **failedoverreplicationtype**, **replicationmode** und **replicationstate**
-   [**MSVM \_ Virtualsystemexportsettingdata**](msvm-virtualsystemexportsettingdata.md): **exportforlivemigration**
-   [**MSVM \_ Virtualsystemmigrationsettingdata**](msvm-virtualsystemmigrationsettingdata.md): " **vermeidremuvingvhds**" und " **Zuweisung** von" "" ".
-   [**MSVM \_ Virtualsystemsettingdata**](msvm-virtualsystemsettingdata.md): **highmmiogapsize**
-   [**MSVM \_ Virtualsystemsnapshotsettingdata**](msvm-virtualsystemsnapshotsettingdata.md): **guestbackuptype**

Entfernte Eigenschaften:

-   [**MSVM \_ Virtualsystemsettingdata**](msvm-virtualsystemsettingdata.md): Parameter **Package**

## <a name="windows-10"></a>Windows 10

Neue Klassen:

-   [**CIM \_ collectedmses**](cim-collectedmses.md)
-   [**CIM \_ -Auflistung**](cim-collection.md)
-   [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md)
-   [**CIM- \_ Element Ansicht**](cim-elementview.md)
-   [**CIM- \_ mitgliedfassungs Sammlung**](cim-memberofcollection.md)
-   [**CIM- \_ TPM**](cim-tpm.md)
-   [**CIM- \_ Ansicht**](cim-view.md)
-   [**MSVM \_ collectedcollections**](msvm-collectedcollections.md)
-   [**MSVM \_ collectedreferencepoints**](msvm-collectedreferencepoints.md)
-   [**MSVM \_ collectedmoment Aufnahmen**](msvm-collectedsnapshots.md)
-   [**MSVM \_ collectedvirtualsystems**](msvm-collectedvirtualsystems.md)
-   [**MSVM \_ collectionmanagementservice**](msvm-collectionmanagementservice.md)
-   [**MSVM \_ collectionreferencepointexportsettingdata**](msvm-collectionreferencepointexportsettingdata.md)
-   [**MSVM \_ collectionreferencepointservice**](msvm-collectionreferencepointservice.md)
-   [**MSVM \_ collectionreferencepointsettingdata**](msvm-collectionreferencepointsettingdata.md)
-   [**MSVM \_ collectionsettingdata**](msvm-collectionsettingdata.md)
-   [**MSVM \_ collectionsnapshotexportsettingdata**](msvm-collectionsnapshotexportsettingdata.md)
-   [**MSVM \_ collectionsnapshotservice**](msvm-collectionsnapshotservice.md)
-   [**MSVM \_ computersystemsummaryinformation**](msvm-computersystemsummaryinformation.md)
-   [**MSVM \_ ethernetzwitchportvfpsettingdata**](msvm-ethernetswitchportvfpsettingdata.md)
-   [**MSVM \_ guestclusterinformation**](msvm-guestclusterinformation.md)
-   [**MSVM \_ guestcommunicationservice**](msvm-guestcommunicationservice.md)
-   [**MSVM \_ guestcommunicationservicesettingdata**](msvm-guestcommunicationservicesettingdata.md)
-   [**MSVM \_ guestserviceinterfaktenettingdatacomponent**](msvm-guestserviceinterfacesettingdatacomponent.md)
-   [**MSVM \_ managementcollection**](msvm-managementcollection.md)
-   [**MSVM " \_ muveunmanagedvhd"**](msvm-moveunmanagedvhd.md)
-   [**MSVM \_ referencepointcollection**](msvm-referencepointcollection.md)
-   [**MSVM \_ referencepoinpofvirtualsystem**](msvm-referencepointofvirtualsystem.md)
-   [**MSVM \_ referencepoinpofvirtualsystemcollection**](msvm-referencepointofvirtualsystemcollection.md)
-   [**MSVM \_ resourcedependentonresource**](msvm-resourcedependentonresource.md)
-   [**MSVM \_ serialportsettingdata**](msvm-serialportsettingdata.md)
-   [**MSVM \_ serviceofvsscomponent**](msvm-serviceofvsscomponent.md)
-   [**MSVM \_ snapshotcollection**](msvm-snapshotcollection.md)
-   [**MSVM \_ snapshostart System Collection**](msvm-snapshotofvirtualsystemcollection.md)
-   [**MSVM \_ StandaloneV2ElementConformsToProfile**](msvm-standalonev2elementconformstoprofile.md)
-   [**MSVM \_ syntheticdisplaycontrollersettingdata**](msvm-syntheticdisplaycontrollersettingdata.md)
-   [**MSVM \_ synthetickeyboard**](msvm-synthetickeyboard.md)
-   [**MSVM \_ TPM**](msvm-tpm.md)
-   [**MSVM \_ tpmsettingdata**](msvm-tpmsettingdata.md)
-   [**MSVM \_ vhdsetinformation**](msvm-vhdsetinformation.md)
-   [**MSVM \_ vhdsnapshotinformation**](msvm-vhdsnapshotinformation.md)
-   [**MSVM \_ virtualethernetzwitchnicteamingmember**](msvm-virtualethernetswitchnicteamingmember.md)
-   [**MSVM \_ virtualethernetzwitchnicteamingsettingdata**](msvm-virtualethernetswitchnicteamingsettingdata.md)
-   [**MSVM \_ virtualmachinetodisks**](msvm-virtualmachinetodisks.md)
-   [**MSVM \_ virtualsystemcollection**](msvm-virtualsystemcollection.md)
-   [**MSVM \_ virtualsystemreferencepoint**](msvm-virtualsystemreferencepoint.md)
-   [**MSVM \_ virtualsystemreferencepointexportsettingdata**](msvm-virtualsystemreferencepointexportsettingdata.md)
-   [**MSVM \_ virtualsystemreferencepointservice**](msvm-virtualsystemreferencepointservice.md)
-   [**MSVM \_ virtualsystemreferencepointsettingdata**](msvm-virtualsystemreferencepointsettingdata.md)
-   [**MSVM \_ virtualsystemsnapshotsettingdata**](msvm-virtualsystemsnapshotsettingdata.md)
-   [**MSVM- \_ VssService**](msvm-vssservice.md)

Entfernte Klasse:

-   [**MSVM \_ resourcepoolcomponent**](msvm-resourcepoolcomponent.md)
-   [**MSVM \_ resourcepoolregistration**](msvm-resourcepoolregistration.md)
-   [**MSVM \_ resourcepoolsettingdata**](msvm-resourcepoolsettingdata.md)
-   [**MSVM \_ virtualizationcomponent**](msvm-virtualizationcomponent.md)
-   [**MSVM \_ virtualizationcomponentregistration**](msvm-virtualizationcomponentregistration.md)

Neue Eigenschaften:

-   [**MSVM \_ Bootsourcesettingdata**](msvm-bootsourcesettingdata.md): **OptionalData**
-   [**MSVM \_ Ethernetportumcationsettingdata**](msvm-ethernetportallocationsettingdata.md): **lastknownswitchname** und **Abteilungs-GUID**
-   [**MSVM \_ Ethernezwitchhardwareoffloaddata**](msvm-ethernetswitchhardwareoffloaddata.md): **packetdirectinuse**
-   [**MSVM \_ Ethernezwitchportoffloadsettingdata**](msvm-ethernetswitchportoffloadsettingdata.md): **packetdirectmoderationinterval**, **packetdirectmoderationcount**, **packetdirectnumprocs**,
-   [**MSVM \_ Ethernetzwitchportsecuritysettingdata**](msvm-ethernetswitchportsecuritysettingdata.md): **EnableFixSpeed10G** und **reserved**
-   [**MSVM \_ Guestserviceinterfacecomponentsettingdata**](msvm-guestserviceinterfacecomponentsettingdata.md): **defaultenabledstatepolicy**
-   [**MSVM \_ Processorsettingdata**](msvm-processorsettingdata.md): **enablehustresourceprotection**
-   [**MSVM \_ Storagezugecationsettingdata**](msvm-storageallocationsettingdata.md): **storageqospolicyid**, **CachingMode** und **snapshotid**
-   [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md): **InstanceId**, **Version**, **thumbnailimageheight**, **ThumbnailImageWidth** und **hostcomputersystemname**
-   [**MSVM \_ Synthetic3DDisplayControllerSettingData**](msvm-synthetic3ddisplaycontrollersettingdata.md): **vramsizebytes**
-   [**MSVM \_ Virtualethernetzwitchsettingdata**](msvm-virtualethernetswitchsettingdata.md): **teamingenabled** und **packetdirectenabled**
-   [**MSVM \_ Virtualharddisksettingdata**](msvm-virtualharddisksettingdata.md): "Parameter **timestamp**" und "Parameter **Name** "
-   [**MSVM \_ Virtualharddiskstate**](msvm-virtualharddiskstate.md): **Zeitstempel**
-   [**MSVM \_ Virtualsystemexportsettingdata**](msvm-virtualsystemexportsettingdata.md): **backupintent** und **differentialbackupbase**
-   [**MSVM \_ Virtualsystemmanagementservicesettingdata**](msvm-virtualsystemmanagementservicesettingdata.md): **defaultvirtualharddiskcachingmode**
-   [**MSVM \_ Virtualsystemmigrationsettingdata**](msvm-virtualsystemmigrationsettingdata.md): **removesourceunmanagedvhds** und **unmanagedvhds**
-   [**MSVM \_ Virtualsystemsettingdata**](msvm-virtualsystemsettingdata.md): **usersnapshottype**, **guestcontrolledcachetypes**, **lockondisconnect, Parameter** **Package**, **automaticcriticalerroraction Timeout**, **automaticcriticalerroraction**, **consolemode** und **secureboottemplateid**

Neue Methoden:

-   [**MSVM \_ Imagemanagementservice**](msvm-imagemanagementservice.md) -Klasse: [**convertvirtualharddisktovhdset**](msvm-imagemanagementservice-convertvirtualharddisktovhdset.md), [**deletevhdsnapshot**](msvm-imagemanagementservice-deletevhdsnapshot.md), [**findmountedstorageimageinstance**](msvm-imagemanagementservice-findmountedstorageimageinstance.md), [**getvhdsetinformation**](msvm-imagemanagementservice-getvhdsetinformation.md), [**getvhdsnapshotinformation**](msvm-imagemanagementservice-getvhdsnapshotinformation.md), [**getvirtualdiskchanges**](msvm-imagemanagementservice-getvirtualdiskchanges.md), [**optimizevhdset**](msvm-imagemanagementservice-optimizevhdset.md)und [**setvhdsnapshotinformation**](msvm-imagemanagementservice-setvhdsnapshotinformation.md)
-   [**MSVM \_ Shutdowncomponent**](msvm-shutdowncomponent.md) -Klasse: [ **initiatereboot**](msvm-shutdowncomponent-initiatereboot.md)
-   [**MSVM \_ Virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md): [**addbootsourcesettings**](msvm-virtualsystemmanagementservice-addbootsourcesettings.md), [**addguestservicesettings**](msvm-virtualsystemmanagementservice-addguestservicesettings.md), [**defineplannedsystem**](msvm-virtualsystemmanagementservice-defineplannedsystem.md), [**modifyguestservicesettings**](msvm-virtualsystemmanagementservice-modifyguestservicesettings.md), [**removebootsourcesettings**](msvm-virtualsystemmanagementservice-removebootsourcesettings.md), [**removeguesservicesettings**](msvm-virtualsystemmanagementservice-removeguestservicesettings.md), [**setinitialmachineconfigurationdata**](msvm-virtualsystemmanagementservice-setinitialmachineconfigurationdata.md)und [**upgradesystemversion**](msvm-virtualsystemmanagementservice-upgradesystemversion.md)
-   [**MSVM \_ Virtualsystemsnapshotservice**](msvm-virtualsystemsnapshotservice.md) -Klasse: [ **converttoreferencepoint**](msvm-virtualsystemsnapshotservice-converttoreferencepoint.md)

## <a name="windows-81-and-windows-server-2012-r2"></a>Windows 8.1 und Windows Server 2012 R2

Windows 8.1 und Windows Server 2012 R2 enthalten neue Funktionen für Version 2 des Hyper-V-WMI-Anbieters.

-   Die Eigenschaften " **iopsallocationunits**", " **iopslimit**", " **iopsreservierung**" und " **persistentreservationssupported** " wurden der [**MSVM-Klasse " \_ storagezucationsettingdata**](msvm-storageallocationsettingdata.md) " hinzugefügt.
-   Die **virtualdiskid** -Eigenschaft wurde der [**MSVM-Klasse " \_ virtualharddisksettingdata**](msvm-virtualharddisksettingdata.md) " hinzugefügt.
-   Informationen zu Speicher-QoS wurden der Eigenschaft **OperationalStatus** der [**MSVM \_ LogicalDisk**](msvm-logicaldisk.md) -und [**MSVM \_ resourcepool**](msvm-resourcepool.md) -Klassen hinzugefügt.
-   [**MSVM \_ Storagealert**](msvm-storagealert.md) -Klasse
-   Die **clusterüberwachter** -Eigenschaft wurde den Klassen [**MSVM \_ emuatedethernetportsettingdata**](msvm-emulatedethernetportsettingdata.md) und [**MSVM \_ syntheticethernetportsettingdata**](msvm-syntheticethernetportsettingdata.md) hinzugefügt.
-   Die Eigenschaften **EnableCompression** und **enablesmbtransport** wurden der [**MSVM \_ virtualsystemmigrationservicesettingdata**](msvm-virtualsystemmigrationservicesettingdata.md) -Klasse hinzugefügt.
-   Die **EnableCompression** -Eigenschaft wurde der [**MSVM-Klasse " \_ virtualsystemmigrationsettingdata**](msvm-virtualsystemmigrationsettingdata.md) " hinzugefügt. Die **TransportType** -Eigenschaft enthält Informationen zur Live Migration.
-   [**MSVM \_ Copyfiledeguestjob**](msvm-copyfiletoguestjob.md) -Klasse
-   [**MSVM \_ Copyfilestarguestsettingdata**](msvm-copyfiletoguestsettingdata.md) -Klasse
-   [**MSVM \_ Guestfileservice**](msvm-guestfileservice.md) -Klasse
-   [**MSVM \_ Guestservice**](msvm-guestservice.md) -Klasse
-   [**MSVM \_ Guestserviceingeterfacecomponent**](msvm-guestserviceinterfacecomponent.md) -Klasse
-   [**MSVM \_ Guestserviceinterfacecomponentsettingdata**](msvm-guestserviceinterfacecomponentsettingdata.md) -Klasse
-   [**MSVM \_ Registeredguestservice**](msvm-registeredguestservice.md) -Klasse
-   Die **enhancedsessionmodeaktivierte** Eigenschaft wurde der [**MSVM \_ virtualsystemmanagementservicesettingdata**](msvm-virtualsystemmanagementservicesettingdata.md) -Klasse hinzugefügt.
-   Die **enhancedmodestate** -Eigenschaft und die [**injetnonmaskableinterrupt**](injectnonmaskableinterrupt-msvm-computersystem.md) -Methode wurden der [**MSVM \_ Computersystem**](msvm-computersystem.md) -Klasse hinzugefügt.
-   Die Eigenschaften " **bootsourceorder**", " **lowmmiogapsize**", " **networkbootpreferredprotocol**", " **pauseafterbootfailure** ", " **securebootenabled**" und " **virtualsystemsubtype** " wurden der [**MSVM-Klasse " \_ virtualsystemsettingdata**](msvm-virtualsystemsettingdata.md) " hinzugefügt.
-   [**MSVM \_ Bootsourcesettingdata**](msvm-bootsourcesettingdata.md) -Klasse
-   [**MSVM \_ Bootsourcecomponent**](msvm-bootsourcecomponent.md) -Klasse
-   [**MSVM \_ Logicalidentity**](msvm-logicalidentity.md) -Klasse
-   [**MSVM \_ Compatibilityvector**](msvm-compatibilityvector.md) -Klasse
-   Die [**getsystemcompatibilityvectors**](getsystemcompatibilityvectors-msvm-virtualsystemmigrationservice.md) -Methode wurde der [**MSVM \_ virtualsystemmigrationservice**](msvm-virtualsystemmigrationservice.md) -Klasse hinzugefügt.
-   Die Eigenschaften " **replicationstateex**", " **replicationhealthex**", " **enhancedsessionmodestate**", " **virtualswitchnames** " und " **virtualsystemsubtype** " wurden der [**MSVM-Klasse " \_ SummaryInformation**](msvm-summaryinformation.md) " hinzugefügt. Die Eigenschaften " **replicationstate** " und " **ReplicationHealth** " sind veraltet und werden durch die Eigenschaften " **replicationstateex** " und " **replicationhealthex** " ersetzt.
-   Die **pnpdevicepath** -Eigenschaft wurde der [**MSVM \_ mountedstorageimage**](msvm-mountedstorageimage.md) -Klasse hinzugefügt.
-   Die Eigenschaften " **zugswedhashalgorithms** " und " **Treuhänder Name** " wurden der Klasse " [**MSVM \_ terminalservicesettingdata**](msvm-terminalservicesettingdata.md) " hinzugefügt.

Windows 8.1 und Windows Server 2012 R2 enthalten neue Funktionen für die Replikation virtueller Computer und die failoverwiederherstellung.

-   [**MSVM \_ Replicationprovider**](msvm-replicationprovider.md) -Klasse
-   [**MSVM \_ Replicationrelationship**](msvm-replicationrelationship.md) -Klasse
-   Die Methoden [**changereplicationmodetoprimary**](changereplicationmodetoprimary-msvm-replicationservice.md), [**getreplicationstatisticsex**](getreplicationstatisticsex-msvm-replicationservice.md), [**initiatefailback**](initiatefailback-msvm-replicationservice.md), [**removereplicationrelationshipex**](removereplicationrelationshipex-msvm-replicationservice.md)und [**remintreplicationstatisticsex**](resetreplicationstatisticsex-msvm-replicationservice.md) wurden der Klasse [**MSVM \_ replicationservice**](msvm-replicationservice.md) hinzugefügt. Die Methoden **getreplicationstatisticsex**, **removereplicationrelationshipex** und **rec treplicationstatisticsex** ersetzen die Methoden [**getreplicationstatistics**](getreplicationstatistics-msvm-replicationservice.md), [**removereplicationrelationship**](removereplicationrelationship-msvm-replicationservice.md)und [**recationstatistics**](resetreplicationstatistics-msvm-replicationservice.md) .
-   Die [**MSVM \_ systemreplicationrelationship**](msvm-systemreplicationrelationship.md) -Klasse zeigt eine Zuordnung zwischen einem virtuellen Computer und einer vielen Replikations Beziehung.
-   Die Eigenschaften **additionalsettings** und **replicationprovider** wurden der [**MSVM \_ replicationsettingdata**](msvm-replicationsettingdata.md) -Klasse hinzugefügt.
-   Die Informationen zum Host-zu-Host-Anbieter wurden den Methoden "up [**" und "**](createreplicationrelationship-msvm-replicationservice.md) [**modifyreplicationsettings**](modifyreplicationsettings-msvm-replicationservice.md) " der [**MSVM- \_ replicationservice**](msvm-replicationservice.md) -Klasse hinzugefügt.
-   Die [**requestreplicationstatechangeex**](msvm-requestreplicationstatechangeex-computersystem.md) -Methode wurde der [**MSVM \_ Computersystem**](msvm-computersystem.md) -Klasse hinzugefügt und ersetzt die [**requestreplicationstatechange**](msvm-computersystem-requestreplicationstatechange.md) -Methode. Die **InstanceId-** Eigenschaft kann jetzt die erweiterte Replikation angeben. Weitere Informationen zur erweiterten Replikation finden Sie unter [**MSVM \_ replicationrelationship**](msvm-replicationrelationship.md).
-   [**MSVM \_ Replicationsettingdata**](msvm-replicationsettingdata.md) -und [**MSVM \_ replicationrelationship**](msvm-replicationrelationship.md) -Instanzen verfügen über eine 1:1-Beziehung, die Sie mit einer [**MSVM \_ settingsdefinestate**](msvm-settingsdefinestate.md) -Zuordnung darstellen können.

    | [**MSVM \_ Name der settingsdefinestate**](msvm-settingsdefinestate.md) -Eigenschaft | Wert                                                                                                |
    |-----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
    | **"Managedelement"**                                                          | Stellt das [**MSVM- \_ replicationrelationship**](msvm-replicationrelationship.md) -Objekt dar.          |
    | **SettingData**                                                             | Stellt das zugeordnete [**MSVM \_ replicationsettingdata**](msvm-replicationsettingdata.md) -Objekt dar. |

    

     

-   [**MSVM \_ Replicationsettingdata**](msvm-replicationsettingdata.md) kann zwischen dem Festlegen von Instanzen für die Replikations Beziehung basierend auf der **InstanceId** oder der **replicationrelationship** -Eigenschaft unterscheiden. Daher haben diese Methoden, die sich mit einer einzelnen Beziehung beschäftigen, Ihre Signatur nicht geändert:

    -   [**MSVM \_ replicationservice:: kreatereplicationrelationship**](createreplicationrelationship-msvm-replicationservice.md)
    -   [**MSVM \_ replicationservice:: modifyreplicationsettings**](modifyreplicationsettings-msvm-replicationservice.md)
    -   [**MSVM \_ replicationservice:: Resync**](resynchronize-msvm-replicationservice.md)
    -   [**MSVM \_ replicationservice:: startreplizierung**](startreplication-msvm-replicationservice.md)

-   Obwohl Sie [**getreplicationstatistics**](getreplicationstatistics-msvm-replicationservice.md), [**removereplicationrelationship**](removereplicationrelationship-msvm-replicationservice.md)und [**requestreplicationstatechange**](msvm-computersystem-requestreplicationstatechange.md) immer für die primäre Beziehung verwenden können, empfiehlt es sich, stattdessen [**getreplicationstatisticsex**](getreplicationstatisticsex-msvm-replicationservice.md), [**removereplicationrelationshipex**](removereplicationrelationshipex-msvm-replicationservice.md)und [**requestreplicationstatechangeex**](msvm-requestreplicationstatechangeex-computersystem.md) zu verwenden, da Sie die primäre und erweiterte Replikations Beziehung verarbeiten können. Weitere Informationen zur erweiterten Replikation finden Sie unter [**MSVM \_ replicationrelationship**](msvm-replicationrelationship.md).
-   Obwohl diese Eigenschaften der [**MSVM \_ Computersystem**](msvm-computersystem.md) -Klasse weiterhin den Status der primären Replikations Beziehung anzeigen, verwenden Sie stattdessen die Eigenschaften eines [**MSVM- \_ replicationrelationship**](msvm-replicationrelationship.md) -Objekts, um den aktuellen Status für die primäre und erweiterte Replikations Beziehung zu ermitteln.

    | Eigenschaftenname                                | type        |
    |----------------------------------------------|-------------|
    | **ReplicationState**                         | UInt16 (RO) |
    | **ReplicationHealth**                        | UInt16 (RO) |
    | **Lastreplicationtime**                      | Datetime    |
    | **Failedoverreplicationtype**                | UInt16      |
    | **Lastapplicationkonsistentreplicationtime** | Datetime    |
    | **Lastreplicationtype**                      | UInt16      |

    

     

 

 



