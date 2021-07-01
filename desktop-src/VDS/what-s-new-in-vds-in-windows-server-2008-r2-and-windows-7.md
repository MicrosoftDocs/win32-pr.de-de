---
description: Erfahren Sie mehr über neue Änderungen für den Virtual Disk Service (VDS) in Windows Server 2008 R2 und Windows 7.
ms.assetid: 4ab37529-8d56-47a3-ad3d-0197cabd4f87
title: Neues in VDS in Windows Server 2008 R2 und Windows 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9050b157e9ce3c78550fdcffbd688988b7eacf90
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119655"
---
# <a name="whats-new-in-vds-in-windows-server-2008-r2-and-windows-7"></a><span data-ttu-id="66252-103">Neues in VDS in Windows Server 2008 R2 und Windows 7</span><span class="sxs-lookup"><span data-stu-id="66252-103">What's New in VDS in Windows Server 2008 R2 and Windows 7</span></span>

<span data-ttu-id="66252-104">\[Ab Windows 8 Windows Server 2012 wird die COM-Schnittstelle des [Virtual Disk Service](virtual-disk-service-portal.md) durch die Windows Storage-Schnittstelle [Verwaltungs-API.](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)\]</span><span class="sxs-lookup"><span data-stu-id="66252-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="66252-105">Windows Server 2008 R2 und Windows 7 führen die folgenden Änderungen am Dienst für virtuelle Datenträger (Virtual Disk Service, VDS) ein:</span><span class="sxs-lookup"><span data-stu-id="66252-105">Windows Server 2008 R2 and Windows 7 introduce the following changes to the Virtual Disk Service (VDS):</span></span>

- [<span data-ttu-id="66252-106">Neue VDS-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="66252-106">New VDS Interfaces</span></span>](#new-vds-interfaces)
- [<span data-ttu-id="66252-107">Neue VDS-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="66252-107">New VDS Enumerations</span></span>](#new-vds-enumerations)
- [<span data-ttu-id="66252-108">Neue VDS-Strukturen</span><span class="sxs-lookup"><span data-stu-id="66252-108">New VDS Structures</span></span>](#new-vds-structures)
- [<span data-ttu-id="66252-109">Änderungen an vorhandenen VDS-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="66252-109">Modifications to Existing VDS Enumerations</span></span>](#modifications-to-existing-vds-enumerations)
- [<span data-ttu-id="66252-110">Änderungen an vorhandenen VDS-Strukturen</span><span class="sxs-lookup"><span data-stu-id="66252-110">Modifications to Existing VDS Structures</span></span>](#modifications-to-existing-vds-structures)

## <a name="new-vds-interfaces"></a><span data-ttu-id="66252-111">Neue VDS-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="66252-111">New VDS Interfaces</span></span>

<dl>

[<span data-ttu-id="66252-112">**IVdsDisk3**</span><span class="sxs-lookup"><span data-stu-id="66252-112">**IVdsDisk3**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdsdisk3)  
[<span data-ttu-id="66252-113">**IVdsDiskPartitionMF2**</span><span class="sxs-lookup"><span data-stu-id="66252-113">**IVdsDiskPartitionMF2**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdsdiskpartitionmf2)  
[<span data-ttu-id="66252-114">**IVdsDrive2**</span><span class="sxs-lookup"><span data-stu-id="66252-114">**IVdsDrive2**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdsdrive2)  
[<span data-ttu-id="66252-115">**IVdsHwProviderStoragePools**</span><span class="sxs-lookup"><span data-stu-id="66252-115">**IVdsHwProviderStoragePools**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdshwproviderstoragepools)  
[<span data-ttu-id="66252-116">**IVdsLun2**</span><span class="sxs-lookup"><span data-stu-id="66252-116">**IVdsLun2**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdslun2)  
[<span data-ttu-id="66252-117">**IVdsLunNumber**</span><span class="sxs-lookup"><span data-stu-id="66252-117">**IVdsLunNumber**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdslunnumber)  
[<span data-ttu-id="66252-118">**IVdsOpenVDisk**</span><span class="sxs-lookup"><span data-stu-id="66252-118">**IVdsOpenVDisk**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdsopenvdisk)  
[<span data-ttu-id="66252-119">**IVdsStoragePool**</span><span class="sxs-lookup"><span data-stu-id="66252-119">**IVdsStoragePool**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdsstoragepool)  
[<span data-ttu-id="66252-120">**IVdsSubSystem2**</span><span class="sxs-lookup"><span data-stu-id="66252-120">**IVdsSubSystem2**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdssubsystem2)  
[<span data-ttu-id="66252-121">**IVdsSubSystemInterconnect**</span><span class="sxs-lookup"><span data-stu-id="66252-121">**IVdsSubSystemInterconnect**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdssubsysteminterconnect)  
[<span data-ttu-id="66252-122">**IVdsVDisk**</span><span class="sxs-lookup"><span data-stu-id="66252-122">**IVdsVDisk**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdsvdisk)  
[<span data-ttu-id="66252-123">**IVdsVdProvider**</span><span class="sxs-lookup"><span data-stu-id="66252-123">**IVdsVdProvider**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdsvdprovider)  
[<span data-ttu-id="66252-124">**IVdsVolume2**</span><span class="sxs-lookup"><span data-stu-id="66252-124">**IVdsVolume2**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdsvolume2)  
[<span data-ttu-id="66252-125">**IVdsVolumeMF3**</span><span class="sxs-lookup"><span data-stu-id="66252-125">**IVdsVolumeMF3**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdsvolumemf3)  


## <a name="new-vds-enumerations"></a><span data-ttu-id="66252-126">Neue VDS-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="66252-126">New VDS Enumerations</span></span>

<dl>

[<span data-ttu-id="66252-127">**VDS_DISK_OFFLINE_REASON**</span><span class="sxs-lookup"><span data-stu-id="66252-127">**VDS_DISK_OFFLINE_REASON**</span></span>](/windows/desktop/api/Vds/ne-vds-vds_disk_offline_reason)  
[<span data-ttu-id="66252-128">**VDS_FORMAT_OPTION_FLAGS**</span><span class="sxs-lookup"><span data-stu-id="66252-128">**VDS_FORMAT_OPTION_FLAGS**</span></span>](/windows/desktop/api/Vds/ne-vds-vds_format_option_flags)  
[<span data-ttu-id="66252-129">**VDS_INTERCONNECT_FLAG**</span><span class="sxs-lookup"><span data-stu-id="66252-129">**VDS_INTERCONNECT_FLAG**</span></span>](/windows/desktop/api/Vds/ne-vds-vds_interconnect_flag)  
[<span data-ttu-id="66252-130">**VDS_RAID_TYPE**</span><span class="sxs-lookup"><span data-stu-id="66252-130">**VDS_RAID_TYPE**</span></span>](/windows/desktop/api/Vds/ne-vds-vds_raid_type)  
[<span data-ttu-id="66252-131">**VDS_STORAGE_POOL_STATUS**</span><span class="sxs-lookup"><span data-stu-id="66252-131">**VDS_STORAGE_POOL_STATUS**</span></span>](/windows/desktop/api/Vds/ne-vds-vds_storage_pool_status)  
[<span data-ttu-id="66252-132">**VDS_STORAGE_POOL_TYPE**</span><span class="sxs-lookup"><span data-stu-id="66252-132">**VDS_STORAGE_POOL_TYPE**</span></span>](/windows/desktop/api/Vds/ne-vds-vds_storage_pool_type)  
[<span data-ttu-id="66252-133">**VDS_SUB_SYSTEM_SUPPORTED_RAID_TYPE_FLAG**</span><span class="sxs-lookup"><span data-stu-id="66252-133">**VDS_SUB_SYSTEM_SUPPORTED_RAID_TYPE_FLAG**</span></span>](/windows/desktop/api/Vds/ne-vds-vds_sub_system_supported_raid_type_flag)  
[<span data-ttu-id="66252-134">**VDS_VDISK_STATE**</span><span class="sxs-lookup"><span data-stu-id="66252-134">**VDS_VDISK_STATE**</span></span>](/windows/desktop/api/Vds/ne-vds-vds_vdisk_state)  


## <a name="new-vds-structures"></a><span data-ttu-id="66252-135">Neue VDS-Strukturen</span><span class="sxs-lookup"><span data-stu-id="66252-135">New VDS Structures</span></span>

<dl>

[<span data-ttu-id="66252-136">**VDS_CREATE_VDISK_PARAMETERS**</span><span class="sxs-lookup"><span data-stu-id="66252-136">**VDS_CREATE_VDISK_PARAMETERS**</span></span>](/windows/desktop/api/Vds/ns-vds-vds_create_vdisk_parameters)  
[<span data-ttu-id="66252-137">**VDS_DISK_FREE_EXTENT**</span><span class="sxs-lookup"><span data-stu-id="66252-137">**VDS_DISK_FREE_EXTENT**</span></span>](/windows/desktop/api/Vds/ns-vds-vds_disk_free_extent)  
[<span data-ttu-id="66252-138">**VDS_DISK_PROP2**</span><span class="sxs-lookup"><span data-stu-id="66252-138">**VDS_DISK_PROP2**</span></span>](/windows/desktop/api/Vds/ns-vds-vds_disk_prop2)  
[<span data-ttu-id="66252-139">**VDS_DRIVE_PROP2**</span><span class="sxs-lookup"><span data-stu-id="66252-139">**VDS_DRIVE_PROP2**</span></span>](/windows/desktop/api/Vds/ns-vds-vds_drive_prop2)  
[<span data-ttu-id="66252-140">**VDS_HINTS2**</span><span class="sxs-lookup"><span data-stu-id="66252-140">**VDS_HINTS2**</span></span>](/windows/desktop/api/Vds/ns-vds-vds_hints2)  
[<span data-ttu-id="66252-141">**VDS_POOL_ATTRIBUTES**</span><span class="sxs-lookup"><span data-stu-id="66252-141">**VDS_POOL_ATTRIBUTES**</span></span>](/windows/desktop/api/Vds/ns-vds-vds_pool_attributes)  
[<span data-ttu-id="66252-142">**VDS_POOL_CUSTOM_ATTRIBUTES**</span><span class="sxs-lookup"><span data-stu-id="66252-142">**VDS_POOL_CUSTOM_ATTRIBUTES**</span></span>](/windows/desktop/api/Vds/ns-vds-vds_pool_custom_attributes)  
[<span data-ttu-id="66252-143">**VDS_STORAGE_POOL_DRIVE_EXTENT**</span><span class="sxs-lookup"><span data-stu-id="66252-143">**VDS_STORAGE_POOL_DRIVE_EXTENT**</span></span>](/windows/desktop/api/Vds/ns-vds-vds_storage_pool_drive_extent)  
[<span data-ttu-id="66252-144">**VDS_STORAGE_POOL_PROP**</span><span class="sxs-lookup"><span data-stu-id="66252-144">**VDS_STORAGE_POOL_PROP**</span></span>](/windows/desktop/api/Vds/ns-vds-vds_storage_pool_prop)  
[<span data-ttu-id="66252-145">**VDS_SUB_SYSTEM_PROP2**</span><span class="sxs-lookup"><span data-stu-id="66252-145">**VDS_SUB_SYSTEM_PROP2**</span></span>](/windows/desktop/api/Vds/ns-vds-vds_sub_system_prop2)  
[<span data-ttu-id="66252-146">**VDS_VDISK_PROPERTIES**</span><span class="sxs-lookup"><span data-stu-id="66252-146">**VDS_VDISK_PROPERTIES**</span></span>](/windows/desktop/api/Vds/ns-vds-vds_vdisk_properties)  
[<span data-ttu-id="66252-147">**VDS_VOLUME_PROP2**</span><span class="sxs-lookup"><span data-stu-id="66252-147">**VDS_VOLUME_PROP2**</span></span>](/windows/desktop/api/Vds/ns-vds-vds_volume_prop)  


## <a name="modifications-to-existing-vds-enumerations"></a><span data-ttu-id="66252-148">Änderungen an vorhandenen VDS-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="66252-148">Modifications to Existing VDS Enumerations</span></span>

<span data-ttu-id="66252-149">[**VDS_ASYNC_OUTPUT_TYPE**](/windows/desktop/api/Vds/ne-vds-vds_async_output_type) enumeration added values (Enumerationserumeration hinzugefügte Werte):</span><span class="sxs-lookup"><span data-stu-id="66252-149">[**VDS_ASYNC_OUTPUT_TYPE**](/windows/desktop/api/Vds/ne-vds-vds_async_output_type) enumeration added values:</span></span>

 <span data-ttu-id="66252-150">**VDS_ASYNCOUT_CREATE_VDISK**</span><span class="sxs-lookup"><span data-stu-id="66252-150">**VDS_ASYNCOUT_CREATE_VDISK**</span></span>  
<span data-ttu-id="66252-151">**VDS_ASYNCOUT_ATTACH_VDISK**</span><span class="sxs-lookup"><span data-stu-id="66252-151">**VDS_ASYNCOUT_ATTACH_VDISK**</span></span>  
<span data-ttu-id="66252-152">**VDS_ASYNCOUT_COMPACT_VDISK**</span><span class="sxs-lookup"><span data-stu-id="66252-152">**VDS_ASYNCOUT_COMPACT_VDISK**</span></span>  
<span data-ttu-id="66252-153">**VDS_ASYNCOUT_MERGE_VDISK**</span><span class="sxs-lookup"><span data-stu-id="66252-153">**VDS_ASYNCOUT_MERGE_VDISK**</span></span>  
<span data-ttu-id="66252-154">**VDS_ASYNCOUT_EXPAND_VDISK**</span><span class="sxs-lookup"><span data-stu-id="66252-154">**VDS_ASYNCOUT_EXPAND_VDISK**</span></span>  


<span data-ttu-id="66252-155">[](/windows/desktop/api/Vds/ne-vds-vds_controller_status) VDS_CONTROLLER_STATUS-Enumerations-Mehrwert:</span><span class="sxs-lookup"><span data-stu-id="66252-155">[**VDS_CONTROLLER_STATUS**](/windows/desktop/api/Vds/ne-vds-vds_controller_status) enumeration added value:</span></span>

<span data-ttu-id="66252-156">**VDS_CS_REMOVED**</span><span class="sxs-lookup"><span data-stu-id="66252-156">**VDS_CS_REMOVED**</span></span>  


<span data-ttu-id="66252-157">[](/windows/desktop/api/Vds/ne-vds-vds_disk_flag) VDS_DISK_FLAG-Enumerations-Mehrwert:</span><span class="sxs-lookup"><span data-stu-id="66252-157">[**VDS_DISK_FLAG**](/windows/desktop/api/Vds/ne-vds-vds_disk_flag) enumeration added value:</span></span>

<span data-ttu-id="66252-158">**VDS_DF_BOOT_FROM_DISK**</span><span class="sxs-lookup"><span data-stu-id="66252-158">**VDS_DF_BOOT_FROM_DISK**</span></span>  
<span data-ttu-id="66252-159">**VDS_DF_CURRENT_READ_ONLY**</span><span class="sxs-lookup"><span data-stu-id="66252-159">**VDS_DF_CURRENT_READ_ONLY**</span></span>  


<span data-ttu-id="66252-160">[**VDS_DRIVE_FLAG**](/windows/desktop/api/Vds/ne-vds-vds_drive_flag) enumeration added values (Enumerationserumeration hinzugefügte Werte):</span><span class="sxs-lookup"><span data-stu-id="66252-160">[**VDS_DRIVE_FLAG**](/windows/desktop/api/Vds/ne-vds-vds_drive_flag) enumeration added values:</span></span>

<span data-ttu-id="66252-161">**VDS_DRF_ASSIGNED**</span><span class="sxs-lookup"><span data-stu-id="66252-161">**VDS_DRF_ASSIGNED**</span></span>  
<span data-ttu-id="66252-162">**VDS_DRF_UNASSIGNED**</span><span class="sxs-lookup"><span data-stu-id="66252-162">**VDS_DRF_UNASSIGNED**</span></span>  
<span data-ttu-id="66252-163">**VDS_DRF_HOTSPARE_IN_USE**</span><span class="sxs-lookup"><span data-stu-id="66252-163">**VDS_DRF_HOTSPARE_IN_USE**</span></span>  
<span data-ttu-id="66252-164">**VDS_DRF_HOTSPARE_STANDBY**</span><span class="sxs-lookup"><span data-stu-id="66252-164">**VDS_DRF_HOTSPARE_STANDBY**</span></span>  


<span data-ttu-id="66252-165">[](/windows/desktop/api/Vds/ne-vds-vds_drive_status) VDS_DRIVE_STATUS-Enumerations-Mehrwert:</span><span class="sxs-lookup"><span data-stu-id="66252-165">[**VDS_DRIVE_STATUS**](/windows/desktop/api/Vds/ne-vds-vds_drive_status) enumeration added value:</span></span>

<span data-ttu-id="66252-166">**VDS_DRS_REMOVED**</span><span class="sxs-lookup"><span data-stu-id="66252-166">**VDS_DRS_REMOVED**</span></span>  


<span data-ttu-id="66252-167">[](/windows/desktop/api/Vds/ne-vds-vds_file_system_type) VDS_FILE_SYSTEM_TYPE-Enumerations-Mehrwert:</span><span class="sxs-lookup"><span data-stu-id="66252-167">[**VDS_FILE_SYSTEM_TYPE**](/windows/desktop/api/Vds/ne-vds-vds_file_system_type) enumeration added value:</span></span>

<span data-ttu-id="66252-168">**VDS_FST_EXFAT**</span><span class="sxs-lookup"><span data-stu-id="66252-168">**VDS_FST_EXFAT**</span></span>  


<span data-ttu-id="66252-169">[**VDS_HEALTH**](/windows/desktop/api/Vds/ne-vds-vds_health) enumeration added values (Enumerationserumeration hinzugefügte Werte):</span><span class="sxs-lookup"><span data-stu-id="66252-169">[**VDS_HEALTH**](/windows/desktop/api/Vds/ne-vds-vds_health) enumeration added values:</span></span>

<span data-ttu-id="66252-170">**VDS_H_REPLACED**</span><span class="sxs-lookup"><span data-stu-id="66252-170">**VDS_H_REPLACED**</span></span>  
<span data-ttu-id="66252-171">**VDS_H_PENDING_FAILURE**</span><span class="sxs-lookup"><span data-stu-id="66252-171">**VDS_H_PENDING_FAILURE**</span></span>  
<span data-ttu-id="66252-172">**VDS_H_DEGRADED**</span><span class="sxs-lookup"><span data-stu-id="66252-172">**VDS_H_DEGRADED**</span></span>  


<span data-ttu-id="66252-173">[**VDS_HWPROVIDER_TYPE**](/windows/desktop/api/Vds/ne-vds-vds_hwprovider_type) enumeration added values (Enumerationserumeration hinzugefügte Werte):</span><span class="sxs-lookup"><span data-stu-id="66252-173">[**VDS_HWPROVIDER_TYPE**](/windows/desktop/api/Vds/ne-vds-vds_hwprovider_type) enumeration added values:</span></span>

<span data-ttu-id="66252-174">**VDS_HWT_SAS**</span><span class="sxs-lookup"><span data-stu-id="66252-174">**VDS_HWT_SAS**</span></span>  
<span data-ttu-id="66252-175">**VDS_HWT_HYBRID**</span><span class="sxs-lookup"><span data-stu-id="66252-175">**VDS_HWT_HYBRID**</span></span>  


<span data-ttu-id="66252-176">[**VDS_LUN_FLAG**](/windows/desktop/api/Vds/ne-vds-vds_lun_flag) Enumerationserumeration hinzugefügte Werte:</span><span class="sxs-lookup"><span data-stu-id="66252-176">[**VDS_LUN_FLAG**](/windows/desktop/api/Vds/ne-vds-vds_lun_flag) enumeration added values:</span></span>

<span data-ttu-id="66252-177">**VDS_LF_READ_CACHE_ENABLED**</span><span class="sxs-lookup"><span data-stu-id="66252-177">**VDS_LF_READ_CACHE_ENABLED**</span></span>  
<span data-ttu-id="66252-178">**VDS_LF_WRITE_CACHE_ENABLED**</span><span class="sxs-lookup"><span data-stu-id="66252-178">**VDS_LF_WRITE_CACHE_ENABLED**</span></span>  
<span data-ttu-id="66252-179">**VDS_LF_MEDIA_SCAN_ENABLED**</span><span class="sxs-lookup"><span data-stu-id="66252-179">**VDS_LF_MEDIA_SCAN_ENABLED**</span></span>  
<span data-ttu-id="66252-180">**VDS_LF_CONSISTENCY_CHECK_ENABLED**</span><span class="sxs-lookup"><span data-stu-id="66252-180">**VDS_LF_CONSISTENCY_CHECK_ENABLED**</span></span>  
<span data-ttu-id="66252-181">**VDS_LF_SNAPSHOT**</span><span class="sxs-lookup"><span data-stu-id="66252-181">**VDS_LF_SNAPSHOT**</span></span>  


<span data-ttu-id="66252-182">[**VDS_LUN_PLEX_TYPE**](/windows/desktop/api/Vds/ne-vds-vds_lun_plex_type) enumeration added values (Enumerationserumeration hinzugefügte Werte):</span><span class="sxs-lookup"><span data-stu-id="66252-182">[**VDS_LUN_PLEX_TYPE**](/windows/desktop/api/Vds/ne-vds-vds_lun_plex_type) enumeration added values:</span></span>

<span data-ttu-id="66252-183">**VDS_LPT_RAID2**</span><span class="sxs-lookup"><span data-stu-id="66252-183">**VDS_LPT_RAID2**</span></span>  
<span data-ttu-id="66252-184">**VDS_LPT_RAID3**</span><span class="sxs-lookup"><span data-stu-id="66252-184">**VDS_LPT_RAID3**</span></span>  
<span data-ttu-id="66252-185">**VDS_LPT_RAID4**</span><span class="sxs-lookup"><span data-stu-id="66252-185">**VDS_LPT_RAID4**</span></span>  
<span data-ttu-id="66252-186">**VDS_LPT_RAID5**</span><span class="sxs-lookup"><span data-stu-id="66252-186">**VDS_LPT_RAID5**</span></span>  
<span data-ttu-id="66252-187">**VDS_LPT_RAID6**</span><span class="sxs-lookup"><span data-stu-id="66252-187">**VDS_LPT_RAID6**</span></span>  
<span data-ttu-id="66252-188">**VDS_LPT_RAID03**</span><span class="sxs-lookup"><span data-stu-id="66252-188">**VDS_LPT_RAID03**</span></span>  
<span data-ttu-id="66252-189">**VDS_LPT_RAID05**</span><span class="sxs-lookup"><span data-stu-id="66252-189">**VDS_LPT_RAID05**</span></span>  
<span data-ttu-id="66252-190">**VDS_LPT_RAID10**</span><span class="sxs-lookup"><span data-stu-id="66252-190">**VDS_LPT_RAID10**</span></span>  
<span data-ttu-id="66252-191">**VDS_LPT_RAID15**</span><span class="sxs-lookup"><span data-stu-id="66252-191">**VDS_LPT_RAID15**</span></span>  
<span data-ttu-id="66252-192">**VDS_LPT_RAID30**</span><span class="sxs-lookup"><span data-stu-id="66252-192">**VDS_LPT_RAID30**</span></span>  
<span data-ttu-id="66252-193">**VDS_LPT_RAID50**</span><span class="sxs-lookup"><span data-stu-id="66252-193">**VDS_LPT_RAID50**</span></span>  
<span data-ttu-id="66252-194">**VDS_LPT_RAID53**</span><span class="sxs-lookup"><span data-stu-id="66252-194">**VDS_LPT_RAID53**</span></span>  
<span data-ttu-id="66252-195">**VDS_LPT_RAID60**</span><span class="sxs-lookup"><span data-stu-id="66252-195">**VDS_LPT_RAID60**</span></span>  


<span data-ttu-id="66252-196">[**VDS_LUN_TYPE**](/windows/desktop/api/Vds/ne-vds-vds_lun_type) enumeration added values (Enumerationserumeration hinzugefügte Werte):</span><span class="sxs-lookup"><span data-stu-id="66252-196">[**VDS_LUN_TYPE**](/windows/desktop/api/Vds/ne-vds-vds_lun_type) enumeration added values:</span></span>

<span data-ttu-id="66252-197">**VDS_LT_RAID2**</span><span class="sxs-lookup"><span data-stu-id="66252-197">**VDS_LT_RAID2**</span></span>  
<span data-ttu-id="66252-198">**VDS_LT_RAID3**</span><span class="sxs-lookup"><span data-stu-id="66252-198">**VDS_LT_RAID3**</span></span>  
<span data-ttu-id="66252-199">**VDS_LT_RAID4**</span><span class="sxs-lookup"><span data-stu-id="66252-199">**VDS_LT_RAID4**</span></span>  
<span data-ttu-id="66252-200">**VDS_LT_RAID5**</span><span class="sxs-lookup"><span data-stu-id="66252-200">**VDS_LT_RAID5**</span></span>  
<span data-ttu-id="66252-201">**VDS_LT_RAID6**</span><span class="sxs-lookup"><span data-stu-id="66252-201">**VDS_LT_RAID6**</span></span>  
<span data-ttu-id="66252-202">**VDS_LT_RAID01**</span><span class="sxs-lookup"><span data-stu-id="66252-202">**VDS_LT_RAID01**</span></span>  
<span data-ttu-id="66252-203">**VDS_LT_RAID03**</span><span class="sxs-lookup"><span data-stu-id="66252-203">**VDS_LT_RAID03**</span></span>  
<span data-ttu-id="66252-204">**VDS_LT_RAID05**</span><span class="sxs-lookup"><span data-stu-id="66252-204">**VDS_LT_RAID05**</span></span>  
<span data-ttu-id="66252-205">**VDS_LT_RAID10**</span><span class="sxs-lookup"><span data-stu-id="66252-205">**VDS_LT_RAID10**</span></span>  
<span data-ttu-id="66252-206">**VDS_LT_RAID15**</span><span class="sxs-lookup"><span data-stu-id="66252-206">**VDS_LT_RAID15**</span></span>  
<span data-ttu-id="66252-207">**VDS_LT_RAID30**</span><span class="sxs-lookup"><span data-stu-id="66252-207">**VDS_LT_RAID30**</span></span>  
<span data-ttu-id="66252-208">**VDS_LT_RAID50**</span><span class="sxs-lookup"><span data-stu-id="66252-208">**VDS_LT_RAID50**</span></span>  
<span data-ttu-id="66252-209">**VDS_LT_RAID51**</span><span class="sxs-lookup"><span data-stu-id="66252-209">**VDS_LT_RAID51**</span></span>  
<span data-ttu-id="66252-210">**VDS_LT_RAID53**</span><span class="sxs-lookup"><span data-stu-id="66252-210">**VDS_LT_RAID53**</span></span>  
<span data-ttu-id="66252-211">**VDS_LT_RAID60**</span><span class="sxs-lookup"><span data-stu-id="66252-211">**VDS_LT_RAID60**</span></span>  
<span data-ttu-id="66252-212">**VDS_LT_RAID61**</span><span class="sxs-lookup"><span data-stu-id="66252-212">**VDS_LT_RAID61**</span></span>  


<span data-ttu-id="66252-213">[**VDS_OBJECT_TYPE**](/windows/desktop/api/Vds/ne-vds-vds_object_type) Hinzugefügte Enumerationswerte:</span><span class="sxs-lookup"><span data-stu-id="66252-213">[**VDS_OBJECT_TYPE**](/windows/desktop/api/Vds/ne-vds-vds_object_type) enumeration added values:</span></span>

<span data-ttu-id="66252-214">**VDS_OT_STORAGE_POOL**</span><span class="sxs-lookup"><span data-stu-id="66252-214">**VDS_OT_STORAGE_POOL**</span></span>  
<span data-ttu-id="66252-215">**VDS_OT_VDISK**</span><span class="sxs-lookup"><span data-stu-id="66252-215">**VDS_OT_VDISK**</span></span>  
<span data-ttu-id="66252-216">**VDS_OT_OPEN_VDISK**</span><span class="sxs-lookup"><span data-stu-id="66252-216">**VDS_OT_OPEN_VDISK**</span></span>  


<span data-ttu-id="66252-217">[](/windows/desktop/api/Vds/ne-vds-vds_port_status) VDS_PORT_STATUS-Enumerations-Mehrwert:</span><span class="sxs-lookup"><span data-stu-id="66252-217">[**VDS_PORT_STATUS**](/windows/desktop/api/Vds/ne-vds-vds_port_status) enumeration added value:</span></span>

<span data-ttu-id="66252-218">**VDS_DRS_REMOVED**</span><span class="sxs-lookup"><span data-stu-id="66252-218">**VDS_DRS_REMOVED**</span></span>  


<span data-ttu-id="66252-219">[**VDS_PROVIDER_FLAG**](/windows/desktop/api/Vds/ne-vds-vds_provider_flag) Hinzugefügte Enumerationswerte:</span><span class="sxs-lookup"><span data-stu-id="66252-219">[**VDS_PROVIDER_FLAG**](/windows/desktop/api/Vds/ne-vds-vds_provider_flag) enumeration added values:</span></span>

<span data-ttu-id="66252-220">**VDS_PF_SUPPORT_MIRROR**</span><span class="sxs-lookup"><span data-stu-id="66252-220">**VDS_PF_SUPPORT_MIRROR**</span></span>  
<span data-ttu-id="66252-221">**VDS_PF_SUPPORT_RAID5**</span><span class="sxs-lookup"><span data-stu-id="66252-221">**VDS_PF_SUPPORT_RAID5**</span></span>  


<span data-ttu-id="66252-222">[**VDS_PROVIDER_TYPE**](/windows/desktop/api/Vds/ne-vds-vds_provider_type) Hinzugefügte Enumerationswerte:</span><span class="sxs-lookup"><span data-stu-id="66252-222">[**VDS_PROVIDER_TYPE**](/windows/desktop/api/Vds/ne-vds-vds_provider_type) enumeration added values:</span></span>

<span data-ttu-id="66252-223">**VDS_PT_VIRTUALDISK**</span><span class="sxs-lookup"><span data-stu-id="66252-223">**VDS_PT_VIRTUALDISK**</span></span>  
<span data-ttu-id="66252-224">**VDS_PT_MAX**</span><span class="sxs-lookup"><span data-stu-id="66252-224">**VDS_PT_MAX**</span></span>  


<span data-ttu-id="66252-225">[**VDS_SERVICE_FLAG**](/windows/desktop/api/Vds/ne-vds-vds_service_flag) Hinzugefügte Enumerationswerte:</span><span class="sxs-lookup"><span data-stu-id="66252-225">[**VDS_SERVICE_FLAG**](/windows/desktop/api/Vds/ne-vds-vds_service_flag) enumeration added values:</span></span>

<span data-ttu-id="66252-226">**VDS_SVF_SUPPORT_MIRROR**</span><span class="sxs-lookup"><span data-stu-id="66252-226">**VDS_SVF_SUPPORT_MIRROR**</span></span>  
<span data-ttu-id="66252-227">**VDS_SVF_SUPPORT_RAID5**</span><span class="sxs-lookup"><span data-stu-id="66252-227">**VDS_SVF_SUPPORT_RAID5**</span></span>  


<span data-ttu-id="66252-228">[**VDS_SUB_SYSTEM_FLAG**](/windows/desktop/api/Vds/ne-vds-vds_sub_system_flag) Hinzugefügte Enumerationswerte:</span><span class="sxs-lookup"><span data-stu-id="66252-228">[**VDS_SUB_SYSTEM_FLAG**](/windows/desktop/api/Vds/ne-vds-vds_sub_system_flag) enumeration added values:</span></span>

<span data-ttu-id="66252-229">**VDS_SF_SUPPORTS_LUN_NUMBER**</span><span class="sxs-lookup"><span data-stu-id="66252-229">**VDS_SF_SUPPORTS_LUN_NUMBER**</span></span>  
<span data-ttu-id="66252-230">**VDS_SF_SUPPORTS_MIRRORED_CACHE**</span><span class="sxs-lookup"><span data-stu-id="66252-230">**VDS_SF_SUPPORTS_MIRRORED_CACHE**</span></span>  
<span data-ttu-id="66252-231">**VDS_SF_READ_CACHING_CAPABLE**</span><span class="sxs-lookup"><span data-stu-id="66252-231">**VDS_SF_READ_CACHING_CAPABLE**</span></span>  
<span data-ttu-id="66252-232">**VDS_SF_WRITE_CACHING_CAPABLE**</span><span class="sxs-lookup"><span data-stu-id="66252-232">**VDS_SF_WRITE_CACHING_CAPABLE**</span></span>  
<span data-ttu-id="66252-233">**VDS_SF_MEDIA_SCAN_CAPABLE**</span><span class="sxs-lookup"><span data-stu-id="66252-233">**VDS_SF_MEDIA_SCAN_CAPABLE**</span></span>  
<span data-ttu-id="66252-234">**VDS_SF_CONSISTENCY_CHECK_CAPABLE**</span><span class="sxs-lookup"><span data-stu-id="66252-234">**VDS_SF_CONSISTENCY_CHECK_CAPABLE**</span></span>  


<span data-ttu-id="66252-235">[](/windows/desktop/api/Vds/ne-vds-vds_transition_state) VDS_TRANSITION_STATE-Enumerations-Mehrwert:</span><span class="sxs-lookup"><span data-stu-id="66252-235">[**VDS_TRANSITION_STATE**](/windows/desktop/api/Vds/ne-vds-vds_transition_state) enumeration added value:</span></span>

<span data-ttu-id="66252-236">**VDS_TS_RESTRIPING**</span><span class="sxs-lookup"><span data-stu-id="66252-236">**VDS_TS_RESTRIPING**</span></span>  


<span data-ttu-id="66252-237">[**VDS_VERSION_SUPPORT_FLAG**](/windows/desktop/api/Vds/ne-vds-vds_version_support_flag) Hinzugefügte Enumerationswerte:</span><span class="sxs-lookup"><span data-stu-id="66252-237">[**VDS_VERSION_SUPPORT_FLAG**](/windows/desktop/api/Vds/ne-vds-vds_version_support_flag) enumeration added values:</span></span>

<span data-ttu-id="66252-238">**VDS_VSF_2_0**</span><span class="sxs-lookup"><span data-stu-id="66252-238">**VDS_VSF_2_0**</span></span>  
<span data-ttu-id="66252-239">**VDS_VSF_2_1**</span><span class="sxs-lookup"><span data-stu-id="66252-239">**VDS_VSF_2_1**</span></span>  
<span data-ttu-id="66252-240">**VDS_VSF_3_0**</span><span class="sxs-lookup"><span data-stu-id="66252-240">**VDS_VSF_3_0**</span></span>  


<span data-ttu-id="66252-241">[](/windows/desktop/api/Vds/ne-vds-vds_volume_status) VDS_VOLUME_STATUS-Enumerations-Mehrwert:</span><span class="sxs-lookup"><span data-stu-id="66252-241">[**VDS_VOLUME_STATUS**](/windows/desktop/api/Vds/ne-vds-vds_volume_status) enumeration added value:</span></span>

<span data-ttu-id="66252-242">**VDS_VS_OFFLINE**</span><span class="sxs-lookup"><span data-stu-id="66252-242">**VDS_VS_OFFLINE**</span></span>  


## <a name="modifications-to-existing-vds-structures"></a><span data-ttu-id="66252-243">Änderungen an vorhandenen VDS-Strukturen</span><span class="sxs-lookup"><span data-stu-id="66252-243">Modifications to Existing VDS Structures</span></span>

<span data-ttu-id="66252-244">[**VDS_CONTROLLER_NOTIFICATION-Struktur**](/windows/desktop/api/Vds/ns-vds-vds_controller_notification) wurden **ulEvent-Werte** hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="66252-244">[**VDS_CONTROLLER_NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_controller_notification) structure added **ulEvent** values:</span></span>

<span data-ttu-id="66252-245">VDS_NF_CONTROLLER_MODIFY</span><span class="sxs-lookup"><span data-stu-id="66252-245">VDS_NF_CONTROLLER_MODIFY</span></span>  
<span data-ttu-id="66252-246">VDS_NF_CONTROLLER_REMOVED</span><span class="sxs-lookup"><span data-stu-id="66252-246">VDS_NF_CONTROLLER_REMOVED</span></span>  


<span data-ttu-id="66252-247">[**VDS_DRIVE_NOTIFICATION-Struktur**](/windows/desktop/api/Vds/ns-vds-vds_drive_notification) wurde **ein ulEvent-Wert** hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="66252-247">[**VDS_DRIVE_NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_drive_notification) structure added **ulEvent** value:</span></span>

<span data-ttu-id="66252-248">VDS_NF_DRIVE_REMOVED</span><span class="sxs-lookup"><span data-stu-id="66252-248">VDS_NF_DRIVE_REMOVED</span></span>  


<span data-ttu-id="66252-249">[**VDS_PORT_NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_port_notification) Struktur wurden **ulEvent-Werte** hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="66252-249">[**VDS_PORT_NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_port_notification) structure added **ulEvent** values:</span></span>

<span data-ttu-id="66252-250">VDS_NF_PORT_MODIFY</span><span class="sxs-lookup"><span data-stu-id="66252-250">VDS_NF_PORT_MODIFY</span></span>  
<span data-ttu-id="66252-251">VDS_NF_PORT_REMOVED</span><span class="sxs-lookup"><span data-stu-id="66252-251">VDS_NF_PORT_REMOVED</span></span>  


 

 
