---
description: Windows Server 2008.
ms.assetid: 2f7b62f8-ba1e-42d2-8872-38d4475e4a2a
title: Neues in VSS in Windows Server 2008 und Windows Vista SP1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f053e327a7a54a9597bc06836b37c00effc62f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129277"
---
# <a name="whats-new-in-vss-in-windows-server-2008-and-windows-vista-sp1"></a><span data-ttu-id="ddb40-103">Neues in VSS in Windows Server 2008 und Windows Vista SP1</span><span class="sxs-lookup"><span data-stu-id="ddb40-103">What's New in VSS in Windows Server 2008 and Windows Vista SP1</span></span>

<span data-ttu-id="ddb40-104">Mit Windows Server 2008 und Windows Vista mit Service Pack 1 (SP1) werden die folgenden Änderungen am Volumeschattenkopie-Dienst eingeführt.</span><span class="sxs-lookup"><span data-stu-id="ddb40-104">Windows Server 2008 and Windows Vista with Service Pack 1 (SP1) introduce the following changes to the Volume Shadow Copy Service.</span></span>

> [!Note]  
> <span data-ttu-id="ddb40-105">Alle Änderungen für Windows Vista gelten für Windows Server 2008 und Windows Vista mit SP1.</span><span class="sxs-lookup"><span data-stu-id="ddb40-105">All changes for Windows Vista apply to Windows Server 2008 and Windows Vista with SP1.</span></span> <span data-ttu-id="ddb40-106">Ausführliche Informationen zu diesen Änderungen finden Sie unter [What es New in VSS in Windows Vista](what-s-new-in-vss-in-windows-vista.md).</span><span class="sxs-lookup"><span data-stu-id="ddb40-106">For details on those changes, see [What's New in VSS in Windows Vista](what-s-new-in-vss-in-windows-vista.md).</span></span>

 

-   [<span data-ttu-id="ddb40-107">Neue VSS-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="ddb40-107">New VSS Interfaces</span></span>](#new-vss-interfaces)
-   [<span data-ttu-id="ddb40-108">Neue VSS-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="ddb40-108">New VSS Enumerations</span></span>](#new-vss-enumerations)
-   [<span data-ttu-id="ddb40-109">Neue VSS-Strukturen</span><span class="sxs-lookup"><span data-stu-id="ddb40-109">New VSS Structures</span></span>](#new-vss-structures)
-   [<span data-ttu-id="ddb40-110">Vorhandene Änderungen der VSS-Enumeration</span><span class="sxs-lookup"><span data-stu-id="ddb40-110">Existing VSS Enumeration Modifications</span></span>](#existing-vss-enumeration-modifications)
-   [<span data-ttu-id="ddb40-111">Vorhandene Änderungen der VSS-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="ddb40-111">Existing VSS Interface Modifications</span></span>](#existing-vss-interface-modifications)
-   [<span data-ttu-id="ddb40-112">Neue VSS-Writer</span><span class="sxs-lookup"><span data-stu-id="ddb40-112">New VSS Writers</span></span>](#new-vss-writers)

## <a name="new-vss-interfaces"></a><span data-ttu-id="ddb40-113">Neue VSS-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="ddb40-113">New VSS Interfaces</span></span>

<dl>

[<span data-ttu-id="ddb40-114">**IVssDifferentialSoftwareSnapshotMgmt3**</span><span class="sxs-lookup"><span data-stu-id="ddb40-114">**IVssDifferentialSoftwareSnapshotMgmt3**</span></span>](/windows/desktop/api/VsMgmt/nn-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt3)  
[<span data-ttu-id="ddb40-115">**Ivsshardwaresnapshotproviderex**</span><span class="sxs-lookup"><span data-stu-id="ddb40-115">**IVssHardwareSnapshotProviderEx**</span></span>](/windows/desktop/api/VsProv/nn-vsprov-ivsshardwaresnapshotproviderex)  
</dl>

## <a name="new-vss-enumerations"></a><span data-ttu-id="ddb40-116">Neue VSS-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="ddb40-116">New VSS Enumerations</span></span>

<dl>

[<span data-ttu-id="ddb40-117">**\_VSS- \_ Hardware \_ Optionen**</span><span class="sxs-lookup"><span data-stu-id="ddb40-117">**\_VSS\_HARDWARE\_OPTIONS**</span></span>](/windows/desktop/api/Vss/ne-vss-vss_hardware_options)  
[<span data-ttu-id="ddb40-118">**VSS- \_ Schutz \_ Fehler**</span><span class="sxs-lookup"><span data-stu-id="ddb40-118">**VSS\_PROTECTION\_FAULT**</span></span>](/windows/desktop/api/VsMgmt/ne-vsmgmt-vss_protection_fault)  
[<span data-ttu-id="ddb40-119">**VSS- \_ Schutz \_ Ebene**</span><span class="sxs-lookup"><span data-stu-id="ddb40-119">**VSS\_PROTECTION\_LEVEL**</span></span>](/windows/desktop/api/VsMgmt/ne-vsmgmt-vss_protection_level)  
</dl>

## <a name="new-vss-structures"></a><span data-ttu-id="ddb40-120">Neue VSS-Strukturen</span><span class="sxs-lookup"><span data-stu-id="ddb40-120">New VSS Structures</span></span>

<dl>

[<span data-ttu-id="ddb40-121">**VSS \_ - \_ \_ volumeschutzinformationen**</span><span class="sxs-lookup"><span data-stu-id="ddb40-121">**VSS\_VOLUME\_PROTECTION\_INFO**</span></span>](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_volume_protection_info)  
</dl>

## <a name="existing-vss-enumeration-modifications"></a><span data-ttu-id="ddb40-122">Vorhandene Änderungen der VSS-Enumeration</span><span class="sxs-lookup"><span data-stu-id="ddb40-122">Existing VSS Enumeration Modifications</span></span>

<dl> <dt>

<span data-ttu-id="ddb40-123"><span id="VSS_BACKUP_SCHEMA_enumeration"></span><span id="vss_backup_schema_enumeration"></span><span id="VSS_BACKUP_SCHEMA_ENUMERATION"></span>[**VSS \_ Sicherungs \_ Schema**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema) -Enumeration</span><span class="sxs-lookup"><span data-stu-id="ddb40-123"><span id="VSS_BACKUP_SCHEMA_enumeration"></span><span id="vss_backup_schema_enumeration"></span><span id="VSS_BACKUP_SCHEMA_ENUMERATION"></span>[**VSS\_BACKUP\_SCHEMA**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema) enumeration</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="ddb40-124"><span id="Added_value_"></span><span id="added_value_"></span><span id="ADDED_VALUE_"></span>Hinzugefügter Wert:</span><span class="sxs-lookup"><span data-stu-id="ddb40-124"><span id="Added_value_"></span><span id="added_value_"></span><span id="ADDED_VALUE_"></span>Added value:</span></span>
</dt> <dd>

<span data-ttu-id="ddb40-125">VSS \_ - \_ Writer-Writer \_ unterstützt \_ parallele \_ Wiederherstellungen</span><span class="sxs-lookup"><span data-stu-id="ddb40-125">VSS\_BS\_WRITER\_SUPPORTS\_PARALLEL\_RESTORES</span></span>

</dd> </dl> </dd> </dl>

<dl> <dt>

<span data-ttu-id="ddb40-126"><span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_enumeration"></span><span id="_vss_volume_snapshot_attributes_enumeration"></span><span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_ENUMERATION"></span>Enumeration der [**\_ VSS- \_ volumemomentaufnahme- \_ \_ Attribute**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes)</span><span class="sxs-lookup"><span data-stu-id="ddb40-126"><span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_enumeration"></span><span id="_vss_volume_snapshot_attributes_enumeration"></span><span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_ENUMERATION"></span>[**\_VSS\_VOLUME\_SNAPSHOT\_ATTRIBUTES**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes) enumeration</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="ddb40-127"><span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Hinzugefügte Werte:</span><span class="sxs-lookup"><span data-stu-id="ddb40-127"><span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Added values:</span></span>
</dt> <dd>

<span data-ttu-id="ddb40-128">\_ \_ \_ verzögerte \_ PostSnapshot für VSS Volsnap attr</span><span class="sxs-lookup"><span data-stu-id="ddb40-128">VSS\_VOLSNAP\_ATTR\_DELAYED\_POSTSNAPSHOT</span></span>

<span data-ttu-id="ddb40-129">VSS \_ Volsnap \_ attr \_ TxF- \_ Wiederherstellung</span><span class="sxs-lookup"><span data-stu-id="ddb40-129">VSS\_VOLSNAP\_ATTR\_TXF\_RECOVERY</span></span>

</dd> </dl> </dd> </dl>

## <a name="existing-vss-interface-modifications"></a><span data-ttu-id="ddb40-130">Vorhandene Änderungen der VSS-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="ddb40-130">Existing VSS Interface Modifications</span></span>

<dl> <dt>

<span data-ttu-id="ddb40-131"><span id="IVssBackupComponentsEx2_interface"></span><span id="ivssbackupcomponentsex2_interface"></span><span id="IVSSBACKUPCOMPONENTSEX2_INTERFACE"></span>[**IVssBackupComponentsEx2**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponentsex2) -Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="ddb40-131"><span id="IVssBackupComponentsEx2_interface"></span><span id="ivssbackupcomponentsex2_interface"></span><span id="IVSSBACKUPCOMPONENTSEX2_INTERFACE"></span>[**IVssBackupComponentsEx2**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponentsex2) interface</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="ddb40-132"><span id="Added_method_"></span><span id="added_method_"></span><span id="ADDED_METHOD_"></span>Hinzugefügte Methode:</span><span class="sxs-lookup"><span data-stu-id="ddb40-132"><span id="Added_method_"></span><span id="added_method_"></span><span id="ADDED_METHOD_"></span>Added method:</span></span>
</dt> <dd>

[<span data-ttu-id="ddb40-133">**Breaksnapshotsekunden**</span><span class="sxs-lookup"><span data-stu-id="ddb40-133">**BreakSnapshotSetEx**</span></span>](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-breaksnapshotsetex)

</dd> </dl> </dd> </dl>

## <a name="new-vss-writers"></a><span data-ttu-id="ddb40-134">Neue VSS-Writer</span><span class="sxs-lookup"><span data-stu-id="ddb40-134">New VSS Writers</span></span>

<span data-ttu-id="ddb40-135">In Windows Server 2008 und Windows Vista mit SP1 sind die folgenden VSS-Writer eingeführt:</span><span class="sxs-lookup"><span data-stu-id="ddb40-135">Windows Server 2008 and Windows Vista with SP1 introduce the following VSS writers:</span></span>

-   <span data-ttu-id="ddb40-136">IIS-konfigurationswriter</span><span class="sxs-lookup"><span data-stu-id="ddb40-136">IIS Configuration Writer</span></span>
-   <span data-ttu-id="ddb40-137">IIS-metabasiswriter</span><span class="sxs-lookup"><span data-stu-id="ddb40-137">IIS Metabase Writer</span></span>
-   <span data-ttu-id="ddb40-138">NPS-VSS-Writer</span><span class="sxs-lookup"><span data-stu-id="ddb40-138">NPS VSS Writer</span></span>
-   <span data-ttu-id="ddb40-139">Remotedesktopdienste (Terminal Dienste) Gateway VSS Writer</span><span class="sxs-lookup"><span data-stu-id="ddb40-139">Remote Desktop Services (Terminal Services) Gateway VSS Writer</span></span>
-   <span data-ttu-id="ddb40-140">Remotedesktopdienste (Terminal Dienste) Lizenzierungs-VSS Writer</span><span class="sxs-lookup"><span data-stu-id="ddb40-140">Remote Desktop Services (Terminal Services) Licensing VSS Writer</span></span>

<span data-ttu-id="ddb40-141">Diese Writer sind in den [in-Box-VSS-Writern](in-box-vss-writers.md)dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="ddb40-141">These writers are documented in [In-Box VSS Writers](in-box-vss-writers.md).</span></span>

 

 



