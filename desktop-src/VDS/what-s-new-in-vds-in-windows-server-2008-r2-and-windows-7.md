---
description: Erfahren Sie mehr über neue Änderungen für den Virtual Disk Service (VDS) in Windows Server 2008 R2 und Windows 7.
ms.assetid: 4ab37529-8d56-47a3-ad3d-0197cabd4f87
title: Neues in VDS in Windows Server 2008 R2 und Windows 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7461a4389a8b276bba33ceacb812f0990344e32a47d848f5d5bce461c3f89f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118347521"
---
# <a name="whats-new-in-vds-in-windows-server-2008-r2-and-windows-7"></a>Neues in VDS in Windows Server 2008 R2 und Windows 7

\[Ab Windows 8 und Windows Server 2012 wird die COM-Schnittstelle des [Virtual Disk Service](virtual-disk-service-portal.md) durch die [Windows Storage Verwaltungs-API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)ersetzt.\]

Windows Server 2008 R2 und Windows 7 führen die folgenden Änderungen am Virtual Disk Service (VDS) ein:

- [Neue VDS-Schnittstellen](#new-vds-interfaces)
- [Neue VDS-Enumerationen](#new-vds-enumerations)
- [Neue VDS-Strukturen](#new-vds-structures)
- [Änderungen an vorhandenen VDS-Enumerationen](#modifications-to-existing-vds-enumerations)
- [Änderungen an vorhandenen VDS-Strukturen](#modifications-to-existing-vds-structures)

## <a name="new-vds-interfaces"></a>Neue VDS-Schnittstellen

<dl>

[**IVdsDisk3**](/windows/desktop/api/Vds/nn-vds-ivdsdisk3)  
[**IVdsDiskPartitionMF2**](/windows/desktop/api/Vds/nn-vds-ivdsdiskpartitionmf2)  
[**IVdsDrive2**](/windows/desktop/api/Vds/nn-vds-ivdsdrive2)  
[**IVdsHwProviderStoragePools**](/windows/desktop/api/Vds/nn-vds-ivdshwproviderstoragepools)  
[**IVdsLun2**](/windows/desktop/api/Vds/nn-vds-ivdslun2)  
[**IVdsLunNumber**](/windows/desktop/api/Vds/nn-vds-ivdslunnumber)  
[**IVdsOpenVDisk**](/windows/desktop/api/Vds/nn-vds-ivdsopenvdisk)  
[**IVdsStoragePool**](/windows/desktop/api/Vds/nn-vds-ivdsstoragepool)  
[**IVdsSubSystem2**](/windows/desktop/api/Vds/nn-vds-ivdssubsystem2)  
[**IVdsSubSystemInterconnect**](/windows/desktop/api/Vds/nn-vds-ivdssubsysteminterconnect)  
[**IVdsVDisk**](/windows/desktop/api/Vds/nn-vds-ivdsvdisk)  
[**IVdsVdProvider**](/windows/desktop/api/Vds/nn-vds-ivdsvdprovider)  
[**IVdsVolume2**](/windows/desktop/api/Vds/nn-vds-ivdsvolume2)  
[**IVdsVolumeMF3**](/windows/desktop/api/Vds/nn-vds-ivdsvolumemf3)  


## <a name="new-vds-enumerations"></a>Neue VDS-Enumerationen

<dl>

[**VDS_DISK_OFFLINE_REASON**](/windows/desktop/api/Vds/ne-vds-vds_disk_offline_reason)  
[**VDS_FORMAT_OPTION_FLAGS**](/windows/desktop/api/Vds/ne-vds-vds_format_option_flags)  
[**VDS_INTERCONNECT_FLAG**](/windows/desktop/api/Vds/ne-vds-vds_interconnect_flag)  
[**VDS_RAID_TYPE**](/windows/desktop/api/Vds/ne-vds-vds_raid_type)  
[**VDS_STORAGE_POOL_STATUS**](/windows/desktop/api/Vds/ne-vds-vds_storage_pool_status)  
[**VDS_STORAGE_POOL_TYPE**](/windows/desktop/api/Vds/ne-vds-vds_storage_pool_type)  
[**VDS_SUB_SYSTEM_SUPPORTED_RAID_TYPE_FLAG**](/windows/desktop/api/Vds/ne-vds-vds_sub_system_supported_raid_type_flag)  
[**VDS_VDISK_STATE**](/windows/desktop/api/Vds/ne-vds-vds_vdisk_state)  


## <a name="new-vds-structures"></a>Neue VDS-Strukturen

<dl>

[**VDS_CREATE_VDISK_PARAMETERS**](/windows/desktop/api/Vds/ns-vds-vds_create_vdisk_parameters)  
[**VDS_DISK_FREE_EXTENT**](/windows/desktop/api/Vds/ns-vds-vds_disk_free_extent)  
[**VDS_DISK_PROP2**](/windows/desktop/api/Vds/ns-vds-vds_disk_prop2)  
[**VDS_DRIVE_PROP2**](/windows/desktop/api/Vds/ns-vds-vds_drive_prop2)  
[**VDS_HINTS2**](/windows/desktop/api/Vds/ns-vds-vds_hints2)  
[**VDS_POOL_ATTRIBUTES**](/windows/desktop/api/Vds/ns-vds-vds_pool_attributes)  
[**VDS_POOL_CUSTOM_ATTRIBUTES**](/windows/desktop/api/Vds/ns-vds-vds_pool_custom_attributes)  
[**VDS_STORAGE_POOL_DRIVE_EXTENT**](/windows/desktop/api/Vds/ns-vds-vds_storage_pool_drive_extent)  
[**VDS_STORAGE_POOL_PROP**](/windows/desktop/api/Vds/ns-vds-vds_storage_pool_prop)  
[**VDS_SUB_SYSTEM_PROP2**](/windows/desktop/api/Vds/ns-vds-vds_sub_system_prop2)  
[**VDS_VDISK_PROPERTIES**](/windows/desktop/api/Vds/ns-vds-vds_vdisk_properties)  
[**VDS_VOLUME_PROP2**](/windows/desktop/api/Vds/ns-vds-vds_volume_prop)  


## <a name="modifications-to-existing-vds-enumerations"></a>Änderungen an vorhandenen VDS-Enumerationen

[**VDS_ASYNC_OUTPUT_TYPE**](/windows/desktop/api/Vds/ne-vds-vds_async_output_type) Hinzugefügte Enumerationswerte:

 **VDS_ASYNCOUT_CREATE_VDISK**  
**VDS_ASYNCOUT_ATTACH_VDISK**  
**VDS_ASYNCOUT_COMPACT_VDISK**  
**VDS_ASYNCOUT_MERGE_VDISK**  
**VDS_ASYNCOUT_EXPAND_VDISK**  


[](/windows/desktop/api/Vds/ne-vds-vds_controller_status) VDS_CONTROLLER_STATUS-Enumerations-Mehrwert:

**VDS_CS_REMOVED**  


[](/windows/desktop/api/Vds/ne-vds-vds_disk_flag) VDS_DISK_FLAG-Enumerations-Mehrwert:

**VDS_DF_BOOT_FROM_DISK**  
**VDS_DF_CURRENT_READ_ONLY**  


[**VDS_DRIVE_FLAG**](/windows/desktop/api/Vds/ne-vds-vds_drive_flag) Hinzugefügte Enumerationswerte:

**VDS_DRF_ASSIGNED**  
**VDS_DRF_UNASSIGNED**  
**VDS_DRF_HOTSPARE_IN_USE**  
**VDS_DRF_HOTSPARE_STANDBY**  


[](/windows/desktop/api/Vds/ne-vds-vds_drive_status) VDS_DRIVE_STATUS-Enumerations-Mehrwert:

**VDS_DRS_REMOVED**  


[](/windows/desktop/api/Vds/ne-vds-vds_file_system_type) VDS_FILE_SYSTEM_TYPE-Enumerations-Mehrwert:

**VDS_FST_EXFAT**  


[**VDS_HEALTH**](/windows/desktop/api/Vds/ne-vds-vds_health) Hinzugefügte Enumerationswerte:

**VDS_H_REPLACED**  
**VDS_H_PENDING_FAILURE**  
**VDS_H_DEGRADED**  


[**VDS_HWPROVIDER_TYPE**](/windows/desktop/api/Vds/ne-vds-vds_hwprovider_type) Hinzugefügte Enumerationswerte:

**VDS_HWT_SAS**  
**VDS_HWT_HYBRID**  


[**VDS_LUN_FLAG**](/windows/desktop/api/Vds/ne-vds-vds_lun_flag) Hinzugefügte Enumerationswerte:

**VDS_LF_READ_CACHE_ENABLED**  
**VDS_LF_WRITE_CACHE_ENABLED**  
**VDS_LF_MEDIA_SCAN_ENABLED**  
**VDS_LF_CONSISTENCY_CHECK_ENABLED**  
**VDS_LF_SNAPSHOT**  


[**VDS_LUN_PLEX_TYPE**](/windows/desktop/api/Vds/ne-vds-vds_lun_plex_type) Hinzugefügte Enumerationswerte:

**VDS_LPT_RAID2**  
**VDS_LPT_RAID3**  
**VDS_LPT_RAID4**  
**VDS_LPT_RAID5**  
**VDS_LPT_RAID6**  
**VDS_LPT_RAID03**  
**VDS_LPT_RAID05**  
**VDS_LPT_RAID10**  
**VDS_LPT_RAID15**  
**VDS_LPT_RAID30**  
**VDS_LPT_RAID50**  
**VDS_LPT_RAID53**  
**VDS_LPT_RAID60**  


[**VDS_LUN_TYPE**](/windows/desktop/api/Vds/ne-vds-vds_lun_type) Hinzugefügte Enumerationswerte:

**VDS_LT_RAID2**  
**VDS_LT_RAID3**  
**VDS_LT_RAID4**  
**VDS_LT_RAID5**  
**VDS_LT_RAID6**  
**VDS_LT_RAID01**  
**VDS_LT_RAID03**  
**VDS_LT_RAID05**  
**VDS_LT_RAID10**  
**VDS_LT_RAID15**  
**VDS_LT_RAID30**  
**VDS_LT_RAID50**  
**VDS_LT_RAID51**  
**VDS_LT_RAID53**  
**VDS_LT_RAID60**  
**VDS_LT_RAID61**  


[**VDS_OBJECT_TYPE**](/windows/desktop/api/Vds/ne-vds-vds_object_type) Enumerations-Mehrwerte:

**VDS_OT_STORAGE_POOL**  
**VDS_OT_VDISK**  
**VDS_OT_OPEN_VDISK**  


[](/windows/desktop/api/Vds/ne-vds-vds_port_status) VDS_PORT_STATUS-Enumerations-Mehrwert:

**VDS_DRS_REMOVED**  


[**VDS_PROVIDER_FLAG**](/windows/desktop/api/Vds/ne-vds-vds_provider_flag) enumeration added values (Enumerationserumeration hinzugefügte Werte):

**VDS_PF_SUPPORT_MIRROR**  
**VDS_PF_SUPPORT_RAID5**  


[**VDS_PROVIDER_TYPE**](/windows/desktop/api/Vds/ne-vds-vds_provider_type) Enumerations-Mehrwerte:

**VDS_PT_VIRTUALDISK**  
**VDS_PT_MAX**  


[**VDS_SERVICE_FLAG**](/windows/desktop/api/Vds/ne-vds-vds_service_flag) Enumerations-Mehrwerte:

**VDS_SVF_SUPPORT_MIRROR**  
**VDS_SVF_SUPPORT_RAID5**  


[**VDS_SUB_SYSTEM_FLAG**](/windows/desktop/api/Vds/ne-vds-vds_sub_system_flag) Enumerations-Mehrwerte:

**VDS_SF_SUPPORTS_LUN_NUMBER**  
**VDS_SF_SUPPORTS_MIRRORED_CACHE**  
**VDS_SF_READ_CACHING_CAPABLE**  
**VDS_SF_WRITE_CACHING_CAPABLE**  
**VDS_SF_MEDIA_SCAN_CAPABLE**  
**VDS_SF_CONSISTENCY_CHECK_CAPABLE**  


[](/windows/desktop/api/Vds/ne-vds-vds_transition_state) VDS_TRANSITION_STATE-Enumerations-Mehrwert:

**VDS_TS_RESTRIPING**  


[**VDS_VERSION_SUPPORT_FLAG**](/windows/desktop/api/Vds/ne-vds-vds_version_support_flag) Enumerations-Mehrwerte:

**VDS_VSF_2_0**  
**VDS_VSF_2_1**  
**VDS_VSF_3_0**  


[](/windows/desktop/api/Vds/ne-vds-vds_volume_status) VDS_VOLUME_STATUS-Enumerations-Mehrwert:

**VDS_VS_OFFLINE**  


## <a name="modifications-to-existing-vds-structures"></a>Änderungen an vorhandenen VDS-Strukturen

[**VDS_CONTROLLER_NOTIFICATION-Struktur**](/windows/desktop/api/Vds/ns-vds-vds_controller_notification) wurden **ulEvent-Werte** hinzugefügt:

VDS_NF_CONTROLLER_MODIFY  
VDS_NF_CONTROLLER_REMOVED  


[**VDS_DRIVE_NOTIFICATION-Struktur**](/windows/desktop/api/Vds/ns-vds-vds_drive_notification) wurde **ulEvent-Wert** hinzugefügt:

VDS_NF_DRIVE_REMOVED  


[**VDS_PORT_NOTIFICATION-Struktur**](/windows/desktop/api/Vds/ns-vds-vds_port_notification) wurden **ulEvent-Werte** hinzugefügt:

VDS_NF_PORT_MODIFY  
VDS_NF_PORT_REMOVED  


 

 
