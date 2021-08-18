---
description: Version 2 des Hyper-V-WMI-Anbieters ist neu für Windows 8 Windows Server 2012.
ms.assetid: A91ACF7A-AFE6-45B6-960C-C4AAA0083735
title: Neues beim Hyper-V-WMI-Anbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbaab65c08031c291eb11e8f865b77e256e5600deba060e0f8176ec8d13c3714
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119754930"
---
# <a name="whats-new-in-hyper-v-wmi-provider"></a>Neues beim Hyper-V-WMI-Anbieter

Version 2 des Hyper-V-WMI-Anbieters ist neu für Windows 8 Windows Server 2012.

## <a name="windows-10-version-1709"></a>Windows 10, Version 1709

Neue Klassen:

-   [**Msvm \_ Battery**](msvm-battery.md)
-   [**Msvm \_ BatterySettingData**](msvm-batterysettingdata.md)
-   [**Msvm \_ PersistentMemoryController**](msvm-persistentmemorycontroller.md)

Neue Eigenschaften:

-   [**Msvm \_ CollectionReferencePointExportJob:**](msvm-collectionreferencepointexportjob.md) **ExportedGuestStateFilePaths**
-   [**Msvm \_ EthernetSwitchHardwareOffloadData:**](msvm-ethernetswitchhardwareoffloaddata.md) **DefaultQueueVrssIndependentHostSpreading,** **DefaultQueueVrssExcludePrimaryProcessor,** **DefaultQueueVrssQueueSchedulingMode** und **DefaultQueueVrssMinQueuePairs**
-   [**Msvm \_ EthernetSwitchHardwareOffloadSettingData:**](msvm-ethernetswitchhardwareoffloadsettingdata.md) **DefaultQueueVrssIndependentHostSpreading**, **DefaultQueueVrssExcludePrimaryProcessor**, **DefaultQueueVrssQueueSchedulingMode**, **DefaultQueueVrssMinQueuePairs**,
-   [**Msvm \_ EthernetSwitchPortOffloadData:**](msvm-ethernetswitchportoffloaddata.md) **VrssVmbusChannelAffinityPolicy,** **VrssIndependentHostSpreading,** **VrssExcludePrimaryProcessor,** **VrssQueueSchedulingModes** und **VrssMinQueuePairs**
-   [**Msvm \_ VirtualHardDiskSettingData:**](msvm-virtualharddisksettingdata.md) **DataAlignment,** **PmemAddressAbstractionType** und **IsPmemCompatible**
-   [**Msvm \_ VirtualSystemExportSettingData:**](msvm-virtualsystemexportsettingdata.md) **DisableDifferentialOfIgnoredStorage** und **ExcludedVirtualHardDisks**
-   [**Msvm \_ VirtualSystemManagementServiceSettingData:**](msvm-virtualsystemmanagementservicesettingdata.md) **HypervisorRootSchedulerEnabled**
-   [**Msvm \_ VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md): **CPUCappingMagnitude** und **CancelIfBlackoutThresholdExceeded**
-   [**Msvm \_ VirtualSystemReferencePointExportJob:**](msvm-virtualsystemreferencepointexportjob.md) **ExportedGuestStateFilePath**
-   [**Msvm \_ VirtualSystemSettingData:**](msvm-virtualsystemsettingdata.md) **Architektur,** **AutomaticSnapshotsEnabled,** **IsAutomaticSnapshot,** **GuestStateFile** und **GuestStateDataRoot**

## <a name="windows-10-version-1703"></a>Windows 10, Version 1703

Neue Klassen:

-   [**Msvm \_ AssignableDeviceDismountSettingData**](msvm-assignabledevicedismountsettingdata.md)
-   [**Msvm \_ AssignableDeviceService**](msvm-assignabledeviceservice.md)
-   [**Msvm \_ CollectionReferencePointExportJob**](msvm-collectionreferencepointexportjob.md)
-   [**Msvm \_ EthernetSwitchHardwareOffloadSettingData**](msvm-ethernetswitchhardwareoffloadsettingdata.md)
-   [**Msvm \_ EthernetSwitchPortMigrationQosSettingData**](msvm-ethernetswitchportmigrationqossettingdata.md)
-   [**Msvm \_ EthernetSwitchPortRdmaSettingData**](msvm-ethernetswitchportrdmasettingdata.md)
-   [**Msvm \_ EthernetSwitchPortTeamMappingSettingData**](msvm-ethernetswitchportteammappingsettingdata.md)
-   [**Msvm \_ GpuPartition**](msvm-gpupartition.md)
-   [**Msvm \_ GpuPartitionSettingData**](msvm-gpupartitionsettingdata.md)
-   [**Msvm \_ NetworkConnectionDiagnosticInformation**](msvm-networkconnectiondiagnosticinformation.md)
-   [**Msvm \_ NetworkConnectionDiagnosticSettingData**](msvm-networkconnectiondiagnosticsettingdata.md)
-   [**Msvm \_ PartitionableGpu**](msvm-partitionablegpu.md)
-   [**Msvm \_ PciExpress**](msvm-pciexpress.md)
-   [**Msvm \_ PciExpressSettingData**](msvm-pciexpresssettingdata.md)
-   [**Msvm \_ SecurityElement**](msvm-securityelement.md)
-   [**Msvm \_ SecurityService**](msvm-securityservice.md)
-   [**Msvm \_ SecuritySettingData**](msvm-securitysettingdata.md)
-   [**Msvm \_ StorageSettingData**](msvm-storagesettingdata.md)
-   [**Msvm \_ SummaryInformationBase**](msvm-summaryinformationbase.md)
-   [**Msvm \_ SystemComponentSettingData**](msvm-systemcomponentsettingdata.md)
-   [**Msvm \_ VirtualSystemReferencePointExportJob**](msvm-virtualsystemreferencepointexportjob.md)
-   [**Msvm \_ VirtualSystemReferencePointSettingData**](msvm-virtualsystemreferencepointsettingdata.md)

Entfernte Klassen:

-   [**Msvm \_ TPMSettingData**](msvm-tpmsettingdata.md)

Neue Methoden:

-   [**Msvm \_ CollectionSnapshotService-Klasse:**](msvm-collectionsnapshotservice.md) [ **ApplySnapshot**](msvm-collectionsnapshotservice-applysnapshot.md)
-   [**Msvm \_ VirtualSystemManagementService-Klasse:**](msvm-virtualsystemmanagementservice.md) [**AddSystemComponentSetting**](msvm-virtualsystemmanagementservice-addsystemcomponentsettings.md), [**DiagnoseNetworkConnection**](msvm-virtualsystemmanagementservice-diagnosenetworkconnection.md), [**ModifySystemComponentSettings**](msvm-virtualsystemmanagementservice-modifysystemcomponentsettings.md)und [**RemoveSystemComponentSettings**](msvm-virtualsystemmanagementservice-removesystemcomponentsettings.md)
-   [**Msvm \_ VirtualSystemReferencePointService-Klasse:**](msvm-virtualsystemreferencepointservice.md) [ **ImportReferencePointMetadata**](msvm-virtualsystemreferencepointservice-importreferencepointmetadata.md)

Neue Eigenschaften:

-   [**Msvm \_ EthernetSwitchHardwareOffloadData:**](msvm-ethernetswitchhardwareoffloaddata.md) **DefaultQueueVmmqQueuePairs,** **DefaultQueueVmmqEnabled** und **DefaultQueueVrssEnabled**
-   [**Msvm \_ EthernetSwitchPortOffloadData:**](msvm-ethernetswitchportoffloaddata.md) **VmmqQueuePairs,** **VmmqEnabled** und **VrssEnabled**
-   [**Msvm \_ EthernetSwitchPortOffloadSettingData:**](msvm-ethernetswitchportoffloadsettingdata.md) **VmmqQueuePairs,** **VmmqEnabled** und **VrssEnabled**
-   [**Msvm \_ GuestClusterInformation:**](msvm-guestclusterinformation.md) **LastResourceMoveTime**
-   [**Msvm \_ KvpExchangeComponentSettingData:**](msvm-kvpexchangecomponentsettingdata.md) **DisableHostKVPItems**
-   [**Msvm \_ MemorySettingData:**](msvm-memorysettingdata.md) **SgxSize** und **SgxEnabled**
-   [**Msvm \_ Physical3dGraphicsProcessor:**](msvm-physical3dgraphicsprocessor.md) **CompatibleForVirtualization** und **DriverModelVersion**
-   [**Msvm \_ ProcessorSettingData:**](msvm-processorsettingdata.md) **HwThreadsPerCoreCpuGroupId,** **HideHypervisorPresent** und **ExposeVirtualizationExtensions**
-   [**Msvm \_ SettingsDefineCapabilities**](msvm-settingsdefinecapabilities.md): **SupportStatement**
-   [**Msvm \_ StorageAllocationSettingData:**](msvm-storageallocationsettingdata.md) **WriteHardeningMethod**
-   [**Msvm \_ SummaryInformation:**](msvm-summaryinformation.md) **Abgeschirmt**
-   [**Msvm \_ SyntheticEthernetPortSettingData:**](msvm-syntheticethernetportsettingdata.md) **AllowPacketDirect**
-   [**Msvm \_ VirtualSystemCollection:**](msvm-virtualsystemcollection.md) **LastApplyConsistencyLevel,** **LastApplyVirtualMachineIds,** **LastApplyTime,** **FailedOverReplicationType,** **ReplicationMode** und **ReplicationState**
-   [**Msvm \_ VirtualSystemExportSettingData:**](msvm-virtualsystemexportsettingdata.md) **ExportForLiveMigration**
-   [**Msvm \_ VirtualSystemMigrationSettingData:**](msvm-virtualsystemmigrationsettingdata.md) **AvoidRemovingVHDs** und **AllowOverwriteExistingFile**
-   [**Msvm \_ VirtualSystemSettingData:**](msvm-virtualsystemsettingdata.md) **HighMmioGapSize**
-   [**Msvm \_ VirtualSystemSnapshotSettingData:**](msvm-virtualsystemsnapshotsettingdata.md) **GuestBackupType**

Entfernte Eigenschaften:

-   [**Msvm \_ VirtualSystemSettingData:**](msvm-virtualsystemsettingdata.md) **ParentPackage**

## <a name="windows-10"></a>Windows 10

Neue Klassen:

-   [**CIM \_ CollectedMSEs**](cim-collectedmses.md)
-   [**\_CIM-Sammlung**](cim-collection.md)
-   [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md)
-   [**CIM \_ ElementView**](cim-elementview.md)
-   [**CIM \_ MemberOfCollection**](cim-memberofcollection.md)
-   [**CIM \_ TPM**](cim-tpm.md)
-   [**\_CIM-Ansicht**](cim-view.md)
-   [**Msvm \_ CollectedCollections**](msvm-collectedcollections.md)
-   [**Msvm \_ CollectedReferencePoints**](msvm-collectedreferencepoints.md)
-   [**Msvm \_ CollectedSnapshots**](msvm-collectedsnapshots.md)
-   [**Msvm \_ CollectedVirtualSystems**](msvm-collectedvirtualsystems.md)
-   [**Msvm \_ CollectionManagementService**](msvm-collectionmanagementservice.md)
-   [**Msvm \_ CollectionReferencePointExportSettingData**](msvm-collectionreferencepointexportsettingdata.md)
-   [**Msvm \_ CollectionReferencePointService**](msvm-collectionreferencepointservice.md)
-   [**Msvm \_ CollectionReferencePointSettingData**](msvm-collectionreferencepointsettingdata.md)
-   [**Msvm \_ CollectionSettingData**](msvm-collectionsettingdata.md)
-   [**Msvm \_ CollectionSnapshotExportSettingData**](msvm-collectionsnapshotexportsettingdata.md)
-   [**Msvm \_ CollectionSnapshotService**](msvm-collectionsnapshotservice.md)
-   [**Msvm \_ ComputerSystemSummaryInformation**](msvm-computersystemsummaryinformation.md)
-   [**Msvm \_ EthernetSwitchPortVfpSettingData**](msvm-ethernetswitchportvfpsettingdata.md)
-   [**Msvm \_ GuestClusterInformation**](msvm-guestclusterinformation.md)
-   [**Msvm \_ GuestCommunicationService**](msvm-guestcommunicationservice.md)
-   [**Msvm \_ GuestCommunicationServiceSettingData**](msvm-guestcommunicationservicesettingdata.md)
-   [**Msvm \_ GuestServiceInterfaceSettingDataComponent**](msvm-guestserviceinterfacesettingdatacomponent.md)
-   [**Msvm \_ ManagementCollection**](msvm-managementcollection.md)
-   [**Msvm \_ MoveUnmanagedVhd**](msvm-moveunmanagedvhd.md)
-   [**Msvm \_ ReferencePointCollection**](msvm-referencepointcollection.md)
-   [**Msvm \_ ReferencePointOfVirtualSystem**](msvm-referencepointofvirtualsystem.md)
-   [**Msvm \_ ReferencePointOfVirtualSystemCollection**](msvm-referencepointofvirtualsystemcollection.md)
-   [**Msvm \_ ResourceDependentOnResource**](msvm-resourcedependentonresource.md)
-   [**Msvm \_ SerialPortSettingData**](msvm-serialportsettingdata.md)
-   [**Msvm \_ ServiceOfVssComponent**](msvm-serviceofvsscomponent.md)
-   [**Msvm \_ SnapshotCollection**](msvm-snapshotcollection.md)
-   [**Msvm \_ SnapshotOfVirtualSystemCollection**](msvm-snapshotofvirtualsystemcollection.md)
-   [**Msvm \_ StandaloneV2ElementConformsToProfile**](msvm-standalonev2elementconformstoprofile.md)
-   [**Msvm \_ SyntheticDisplayControllerSettingData**](msvm-syntheticdisplaycontrollersettingdata.md)
-   [**Msvm \_ SyntheticKeyboard**](msvm-synthetickeyboard.md)
-   [**Msvm \_ TPM**](msvm-tpm.md)
-   [**Msvm \_ TPMSettingData**](msvm-tpmsettingdata.md)
-   [**Msvm \_ VHDSetInformation**](msvm-vhdsetinformation.md)
-   [**Msvm \_ VHDSnapshotInformation**](msvm-vhdsnapshotinformation.md)
-   [**Msvm \_ VirtualEthernetSwitchNicTeamingMember**](msvm-virtualethernetswitchnicteamingmember.md)
-   [**Msvm \_ VirtualEthernetSwitchNicTeamingSettingData**](msvm-virtualethernetswitchnicteamingsettingdata.md)
-   [**Msvm \_ VirtualMachineToDisks**](msvm-virtualmachinetodisks.md)
-   [**Msvm \_ VirtualSystemCollection**](msvm-virtualsystemcollection.md)
-   [**Msvm \_ VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md)
-   [**Msvm \_ VirtualSystemReferencePointExportSettingData**](msvm-virtualsystemreferencepointexportsettingdata.md)
-   [**Msvm \_ VirtualSystemReferencePointService**](msvm-virtualsystemreferencepointservice.md)
-   [**Msvm \_ VirtualSystemReferencePointSettingData**](msvm-virtualsystemreferencepointsettingdata.md)
-   [**Msvm \_ VirtualSystemSnapshotSettingData**](msvm-virtualsystemsnapshotsettingdata.md)
-   [**Msvm \_ VssService**](msvm-vssservice.md)

Klasse entfernt:

-   [**Msvm \_ ResourcePoolComponent**](msvm-resourcepoolcomponent.md)
-   [**Msvm \_ ResourcePoolRegistration**](msvm-resourcepoolregistration.md)
-   [**Msvm \_ ResourcePoolSettingData**](msvm-resourcepoolsettingdata.md)
-   [**Msvm \_ VirtualizationComponent**](msvm-virtualizationcomponent.md)
-   [**Msvm \_ VirtualizationComponentRegistration**](msvm-virtualizationcomponentregistration.md)

Neue Eigenschaften:

-   [**Msvm \_ BootSourceSettingData:**](msvm-bootsourcesettingdata.md) **OptionalData**
-   [**Msvm \_ EthernetPortAllocationSettingData:**](msvm-ethernetportallocationsettingdata.md) **LastKnownSwitchName** und **CompartmentGuid**
-   [**Msvm \_ EthernetSwitchHardwareOffloadData:**](msvm-ethernetswitchhardwareoffloaddata.md) **PacketDirectInUse**
-   [**Msvm \_ EthernetSwitchPortOffloadSettingData:**](msvm-ethernetswitchportoffloadsettingdata.md) **PacketDirectModerationInterval**, **PacketDirectModerationCount**, **PacketDirectNumProcs**,
-   [**Msvm \_ EthernetSwitchPortSecuritySettingData:**](msvm-ethernetswitchportsecuritysettingdata.md) **EnableFixSpeed10G** und **Reserved**
-   [**Msvm \_ GuestServiceInterfaceComponentSettingData:**](msvm-guestserviceinterfacecomponentsettingdata.md) **DefaultEnabledStatePolicy**
-   [**Msvm \_ ProcessorSettingData:**](msvm-processorsettingdata.md) **EnableHostResourceProtection**
-   [**Msvm \_ StorageAllocationSettingData:**](msvm-storageallocationsettingdata.md) **StorageQoSPolicyID,** **CachingMode** und **SnapshotId**
-   [**Msvm \_ SummaryInformation:**](msvm-summaryinformation.md) **InstanceID**, **Version**, **ThumbnailImageHeight**, **ThumbnailImageWidth** und **HostComputerSystemName**
-   [**Msvm \_ Synthetic3DDisplayControllerSettingData:**](msvm-synthetic3ddisplaycontrollersettingdata.md) **VRAMSizeBytes**
-   [**Msvm \_ VirtualEthernetSwitchSettingData:**](msvm-virtualethernetswitchsettingdata.md) **TeamingEnabled** und **PacketDirectEnabled**
-   [**Msvm \_ VirtualHardDiskSettingData:**](msvm-virtualharddisksettingdata.md) **ParentTimestamp** und **ParentIdentifier**
-   [**Msvm \_ VirtualHardDiskState:**](msvm-virtualharddiskstate.md) **Zeitstempel**
-   [**Msvm \_ VirtualSystemExportSettingData:**](msvm-virtualsystemexportsettingdata.md) **BackupIntent** und **DifferentialBackupBase**
-   [**Msvm \_ VirtualSystemManagementServiceSettingData:**](msvm-virtualsystemmanagementservicesettingdata.md) **DefaultVirtualHardDiskCachingMode**
-   [**Msvm \_ VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md): **RemoveSourceUnmanagedVhds** und **UnmanagedVhds**
-   [**Msvm \_ VirtualSystemSettingData:**](msvm-virtualsystemsettingdata.md) **UserSnapshotType,** **GuestControlledCacheTypes,** **LockOnDisconnect,** **ParentPackage,** **AutomaticCriticalErrorActionTimeout,** **AutomaticCriticalErrorAction,** **ConsoleMode** und **SecureBootTemplateId**

Neue Methoden:

-   [**Msvm \_ ImageManagementService-Klasse:**](msvm-imagemanagementservice.md) [**ConvertVirtualHardDiskToVHDSet**](msvm-imagemanagementservice-convertvirtualharddisktovhdset.md), [**DeleteVHDSnapshot**](msvm-imagemanagementservice-deletevhdsnapshot.md), [**FindMountedStorageImageInstance**](msvm-imagemanagementservice-findmountedstorageimageinstance.md), [**GetVHDSetInformation**](msvm-imagemanagementservice-getvhdsetinformation.md), [**GetVHDSnapshotInformation**](msvm-imagemanagementservice-getvhdsnapshotinformation.md), [**GetVirtualDiskChanges**](msvm-imagemanagementservice-getvirtualdiskchanges.md), [**OptimizeVHDSet**](msvm-imagemanagementservice-optimizevhdset.md)und [**SetVHDSnapshotInformation**](msvm-imagemanagementservice-setvhdsnapshotinformation.md)
-   [**Msvm \_ ShutdownComponent-Klasse:**](msvm-shutdowncomponent.md) [ **InitiateReboot**](msvm-shutdowncomponent-initiatereboot.md)
-   [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md): [**AddBootSourceSettings**](msvm-virtualsystemmanagementservice-addbootsourcesettings.md), [**AddGuestServiceSettings**](msvm-virtualsystemmanagementservice-addguestservicesettings.md), [**DefinePlannedSystem**](msvm-virtualsystemmanagementservice-defineplannedsystem.md), [**ModifyGuestServiceSettings**](msvm-virtualsystemmanagementservice-modifyguestservicesettings.md), [**RemoveBootSourceSettings**](msvm-virtualsystemmanagementservice-removebootsourcesettings.md), [**RemoveGuesServiceSettings**](msvm-virtualsystemmanagementservice-removeguestservicesettings.md), [**SetInitialMachineConfigurationData**](msvm-virtualsystemmanagementservice-setinitialmachineconfigurationdata.md)und [**UpgradeSystemVersion**](msvm-virtualsystemmanagementservice-upgradesystemversion.md)
-   [**Msvm \_ VirtualSystemSnapshotService-Klasse:**](msvm-virtualsystemsnapshotservice.md) [ **ConvertToReferencePoint**](msvm-virtualsystemsnapshotservice-converttoreferencepoint.md)

## <a name="windows-81-and-windows-server-2012-r2"></a>Windows 8.1 und Windows Server 2012 R2

Windows 8.1 und Windows Server 2012 R2 enthalten neue Funktionen für Version 2 des Hyper-V-WMI-Anbieters.

-   Die **Eigenschaften IOPSAllocationUnits,** **IOPSLimit,** **IOPSReservation** und **PersistentReservationsSupported** wurden der [**Msvm \_ StorageAllocationSettingData-Klasse**](msvm-storageallocationsettingdata.md) hinzugefügt.
-   Die **VirtualDiskId-Eigenschaft** wurde der [**Msvm \_ VirtualHardDiskSettingData-Klasse**](msvm-virtualharddisksettingdata.md) hinzugefügt.
-   Informationen zur Speicher-QoS wurden der **OperationalStatus-Eigenschaft** der [**Klassen Msvm \_ LogicalDisk**](msvm-logicaldisk.md) und [**Msvm \_ ResourcePool**](msvm-resourcepool.md) hinzugefügt.
-   [**Msvm \_ StorageAlert-Klasse**](msvm-storagealert.md)
-   Die **ClusterMonitored-Eigenschaft** wurde den [**Klassen Msvm \_ EmulatedEthernetPortSettingData**](msvm-emulatedethernetportsettingdata.md) und [**Msvm \_ SyntheticEthernetPortSettingData**](msvm-syntheticethernetportsettingdata.md) hinzugefügt.
-   Die **Eigenschaften EnableCompression** und **EnableSmbTransport** wurden der [**Msvm \_ VirtualSystemMigrationServiceSettingData-Klasse**](msvm-virtualsystemmigrationservicesettingdata.md) hinzugefügt.
-   Die **EnableCompression-Eigenschaft** wurde der [**Msvm \_ VirtualSystemMigrationSettingData-Klasse**](msvm-virtualsystemmigrationsettingdata.md) hinzugefügt. Die **TransportType-Eigenschaft** enthält Informationen zur Livemigration.
-   [**Msvm \_ CopyFileToGuestJob-Klasse**](msvm-copyfiletoguestjob.md)
-   [**Msvm \_ CopyFileToGuestSettingData-Klasse**](msvm-copyfiletoguestsettingdata.md)
-   [**Msvm \_ GuestFileService-Klasse**](msvm-guestfileservice.md)
-   [**Msvm \_ GuestService-Klasse**](msvm-guestservice.md)
-   [**Msvm \_ GuestServiceInterfaceComponent-Klasse**](msvm-guestserviceinterfacecomponent.md)
-   [**Msvm \_ GuestServiceInterfaceComponentSettingData-Klasse**](msvm-guestserviceinterfacecomponentsettingdata.md)
-   [**Msvm \_ RegisteredGuestService-Klasse**](msvm-registeredguestservice.md)
-   Die **EnhancedSessionModeEnabled-Eigenschaft** wurde der [**Msvm \_ VirtualSystemManagementServiceSettingData-Klasse**](msvm-virtualsystemmanagementservicesettingdata.md) hinzugefügt.
-   Die **EnhancedModeState-Eigenschaft** und die [**InjectNonMaskableInterrupt-Methode**](injectnonmaskableinterrupt-msvm-computersystem.md) wurden der [**Msvm \_ ComputerSystem-Klasse**](msvm-computersystem.md) hinzugefügt.
-   Die **Eigenschaften BootSourceOrder,** **LowMmioGapSize,** **NetworkBootPreferredProtocol,** **PauseAfterBootFailure,** **SecureBootEnabled** und **VirtualSystemSubType** wurden der [**Msvm \_ VirtualSystemSettingData-Klasse**](msvm-virtualsystemsettingdata.md) hinzugefügt.
-   [**Msvm \_ BootSourceSettingData-Klasse**](msvm-bootsourcesettingdata.md)
-   [**Msvm \_ BootSourceComponent-Klasse**](msvm-bootsourcecomponent.md)
-   [**Msvm \_ LogicalIdentity-Klasse**](msvm-logicalidentity.md)
-   [**Msvm \_ CompatibilityVector-Klasse**](msvm-compatibilityvector.md)
-   Die [**GetSystemCompatibilityVectors-Methode**](getsystemcompatibilityvectors-msvm-virtualsystemmigrationservice.md) wurde der [**Msvm \_ VirtualSystemMigrationService-Klasse**](msvm-virtualsystemmigrationservice.md) hinzugefügt.
-   Die **Eigenschaften ReplicationStateEx,** **ReplicationHealthEx,** **EnhancedSessionModeState,** **VirtualSwitchNames** und **VirtualSystemSubType** wurden der [**Msvm \_ SummaryInformation-Klasse**](msvm-summaryinformation.md) hinzugefügt. Die **Eigenschaften ReplicationState** und **ReplicationHealth** sind veraltet und werden durch die **Eigenschaften ReplicationStateEx** und **ReplicationHealthEx** ersetzt.
-   Die **PnpDevicePath-Eigenschaft** wurde der [**Msvm \_ MountedStorageImage-Klasse**](msvm-mountedstorageimage.md) hinzugefügt.
-   Die **Eigenschaften AllowedHashAlgorithms** und **TrustedIssuerCertificateHashes** wurden der [**Msvm \_ TerminalServiceSettingData-Klasse**](msvm-terminalservicesettingdata.md) hinzugefügt.

Windows 8.1 und Windows Server 2012 R2 enthalten neue Funktionen für die Replikation virtueller Computer und die Failoverwiederherstellung.

-   [**Msvm \_ ReplicationProvider-Klasse**](msvm-replicationprovider.md)
-   [**Msvm \_ ReplicationRelationship-Klasse**](msvm-replicationrelationship.md)
-   Die [**Methoden ChangeReplicationModeToPrimary,**](changereplicationmodetoprimary-msvm-replicationservice.md) [**GetReplicationStatisticsEx,**](getreplicationstatisticsex-msvm-replicationservice.md) [**InitiateFailback,**](initiatefailback-msvm-replicationservice.md) [**RemoveReplicationRelationshipEx**](removereplicationrelationshipex-msvm-replicationservice.md)und [**ResetReplicationStatisticsEx**](resetreplicationstatisticsex-msvm-replicationservice.md) wurden der [**Msvm \_ ReplicationService-Klasse**](msvm-replicationservice.md) hinzugefügt. Die **Methoden GetReplicationStatisticsEx,** **RemoveReplicationRelationshipEx** und **ResetReplicationStatisticsEx** ersetzen die [**Methoden GetReplicationStatistics,**](getreplicationstatistics-msvm-replicationservice.md) [**RemoveReplicationRelationship**](removereplicationrelationship-msvm-replicationservice.md)und [**ResetReplicationStatistics.**](resetreplicationstatistics-msvm-replicationservice.md)
-   Die [**\_ Msvm-Klasse SystemReplicationRelationship zeigt**](msvm-systemreplicationrelationship.md) eine Zuordnung zwischen einem virtuellen Computer und vielen Replikationsbeziehungen.
-   Die **Eigenschaften AdditionalSettings** **und ReplicationProvider** wurden der [**Msvm \_ ReplicationSettingData-Klasse**](msvm-replicationsettingdata.md) hinzugefügt.
-   Informationen zum Host-zu-Host-Anbieter wurden den [**Methoden CreateReplicationRelationship**](createreplicationrelationship-msvm-replicationservice.md) und [**ModifyReplicationSettings**](modifyreplicationsettings-msvm-replicationservice.md) der [**Msvm \_ ReplicationService-Klasse**](msvm-replicationservice.md) hinzugefügt.
-   Die [**RequestReplicationStateChangeEx-Methode**](msvm-requestreplicationstatechangeex-computersystem.md) wurde der [**Msvm \_ ComputerSystem-Klasse**](msvm-computersystem.md) hinzugefügt und ersetzt die [**RequestReplicationStateChange-Methode.**](msvm-computersystem-requestreplicationstatechange.md) Die **InstanceID-Eigenschaft** kann jetzt die erweiterte Replikation angeben. Weitere Informationen zur erweiterten Replikation finden Sie unter [**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md).
-   [**Msvm \_ ReplicationSettingData-**](msvm-replicationsettingdata.md) und [**Msvm \_ ReplicationRelationship-Instanzen**](msvm-replicationrelationship.md) verfügen über eine 1:1-Beziehung, die Sie mit einer [**Msvm \_ SettingsDefineState-Zuordnung darstellen**](msvm-settingsdefinestate.md) können.

    | [**Msvm \_ SettingsDefineState-Eigenschaftenname**](msvm-settingsdefinestate.md) | Wert                                                                                                |
    |-----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
    | **ManagedElement**                                                          | Stellt das [**Msvm \_ ReplicationRelationship-Objekt**](msvm-replicationrelationship.md) dar.          |
    | **Settingdata**                                                             | Stellt das zugeordnete [**Msvm \_ ReplicationSettingData-Objekt**](msvm-replicationsettingdata.md) dar. |

    

     

-   [**Msvm \_ ReplicationSettingData kann**](msvm-replicationsettingdata.md) zwischen dem Festlegen von Instanzen für die Replikationsbeziehung basierend auf der **InstanceId-** oder **ReplicationRelationship-Eigenschaft** unterscheiden. Daher haben diese Methoden, die eine einzelne Beziehung behandeln, ihre Signatur nicht geändert:

    -   [**Msvm \_ ReplicationService::CreateReplicationRelationship**](createreplicationrelationship-msvm-replicationservice.md)
    -   [**Msvm \_ ReplicationService::ModifyReplicationSettings**](modifyreplicationsettings-msvm-replicationservice.md)
    -   [**Msvm \_ ReplicationService::Resync**](resynchronize-msvm-replicationservice.md)
    -   [**Msvm \_ ReplicationService::StartReplication**](startreplication-msvm-replicationservice.md)

-   Obwohl Sie [**GetReplicationStatistics,**](getreplicationstatistics-msvm-replicationservice.md) [**RemoveReplicationRelationship**](removereplicationrelationship-msvm-replicationservice.md)und [**RequestReplicationStateChange**](msvm-computersystem-requestreplicationstatechange.md) immer für die primäre Beziehung verwenden können, wird empfohlen, stattdessen [**GetReplicationStatisticsEx,**](getreplicationstatisticsex-msvm-replicationservice.md) [**RemoveReplicationRelationshipEx**](removereplicationrelationshipex-msvm-replicationservice.md)und [**RequestReplicationStateChangeEx**](msvm-requestreplicationstatechangeex-computersystem.md) zu verwenden, da sie primäre und erweiterte Replikationsbeziehungen verarbeiten können. Weitere Informationen zur erweiterten Replikation finden Sie unter [**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md).
-   Obwohl diese Eigenschaften der [**Msvm \_ ComputerSystem-Klasse**](msvm-computersystem.md) weiterhin den Status für die primäre Replikationsbeziehung angeben, verwenden Sie stattdessen diese Eigenschaften eines [**Msvm \_ ReplicationRelationship-Objekts,**](msvm-replicationrelationship.md) um den aktuellen Status für die primäre und erweiterte Replikationsbeziehung zu bestimmen.

    | Eigenschaftenname                                | type        |
    |----------------------------------------------|-------------|
    | **ReplicationState**                         | Uint16 (RO) |
    | **Replicationhealth**                        | Uint16 (RO) |
    | **LastReplicationTime**                      | Datetime    |
    | **FailedOverReplicationType**                | Uint16      |
    | **LastApplicationConsistentReplicationTime** | Datetime    |
    | **LastReplicationType**                      | Uint16      |

    

     

 

 



