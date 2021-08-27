---
description: Windows Server 2008.
ms.assetid: 2f7b62f8-ba1e-42d2-8872-38d4475e4a2a
title: Neuerungen in VSS in Windows Server 2008 und Windows Vista SP1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83ee109eec31c084dc43fb9e0cc6341f443a16e6aa06ac989a7f328d9bb3011f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120006120"
---
# <a name="whats-new-in-vss-in-windows-server-2008-and-windows-vista-sp1"></a>Neuerungen in VSS in Windows Server 2008 und Windows Vista SP1

Windows Server 2008 und Windows Vista mit Service Pack 1 (SP1) führen die folgenden Änderungen an der Volumeschattenkopie-Dienst ein.

> [!Note]  
> Alle Änderungen für Windows Vista gelten für Windows Server 2008 und Windows Vista mit SP1. Ausführliche Informationen zu diesen Änderungen finden Sie unter [Neuerungen in VSS in Windows Vista.](what-s-new-in-vss-in-windows-vista.md)

 

-   [Neue VSS-Schnittstellen](#new-vss-interfaces)
-   [Neue VSS-Enumerationen](#new-vss-enumerations)
-   [Neue VSS-Strukturen](#new-vss-structures)
-   [Vorhandene VSS-Enumerationsänderungen](#existing-vss-enumeration-modifications)
-   [Änderungen an vorhandenen VSS-Schnittstellen](#existing-vss-interface-modifications)
-   [Neue VSS Writer](#new-vss-writers)

## <a name="new-vss-interfaces"></a>Neue VSS-Schnittstellen

<dl>

[**IVssDifferentialSoftwareSnapshotMgmt3**](/windows/desktop/api/VsMgmt/nn-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt3)  
[**IVssHardwareSnapshotProviderEx**](/windows/desktop/api/VsProv/nn-vsprov-ivsshardwaresnapshotproviderex)  
</dl>

## <a name="new-vss-enumerations"></a>Neue VSS-Enumerationen

<dl>

[**\_\_VSS-HARDWAREOPTIONEN \_**](/windows/desktop/api/Vss/ne-vss-vss_hardware_options)  
[**\_VSS-SCHUTZFEHLER \_**](/windows/desktop/api/VsMgmt/ne-vsmgmt-vss_protection_fault)  
[**\_VSS-SCHUTZEBENE \_**](/windows/desktop/api/VsMgmt/ne-vsmgmt-vss_protection_level)  
</dl>

## <a name="new-vss-structures"></a>Neue VSS-Strukturen

<dl>

[**VSS \_ VOLUME \_ PROTECTION \_ INFO**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_volume_protection_info)  
</dl>

## <a name="existing-vss-enumeration-modifications"></a>Vorhandene VSS-Enumerationsänderungen

<dl> <dt>

<span id="VSS_BACKUP_SCHEMA_enumeration"></span><span id="vss_backup_schema_enumeration"></span><span id="VSS_BACKUP_SCHEMA_ENUMERATION"></span>[**VSS \_ BACKUP \_ SCHEMA-Enumeration**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema)
</dt> <dd>

<dl> <dt>

<span id="Added_value_"></span><span id="added_value_"></span><span id="ADDED_VALUE_"></span>Mehrwert:
</dt> <dd>

VSS \_ BS \_ WRITER UNTERSTÜTZT \_ \_ \_ PARALLELE WIEDERHERSTELLUNGEN.

</dd> </dl> </dd> </dl>

<dl> <dt>

<span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_enumeration"></span><span id="_vss_volume_snapshot_attributes_enumeration"></span><span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_ENUMERATION"></span>[**\_ VSS \_ VOLUME \_ SNAPSHOT \_ ATTRIBUTES-Enumeration**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes)
</dt> <dd>

<dl> <dt>

<span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Hinzugefügte Werte:
</dt> <dd>

VSS \_ VOLSNAP \_ ATTR \_ DELAYED \_ POSTSNAPSHOT

VSS \_ VOLSNAP \_ ATTR \_ TXF \_ RECOVERY

</dd> </dl> </dd> </dl>

## <a name="existing-vss-interface-modifications"></a>Änderungen an vorhandenen VSS-Schnittstellen

<dl> <dt>

<span id="IVssBackupComponentsEx2_interface"></span><span id="ivssbackupcomponentsex2_interface"></span><span id="IVSSBACKUPCOMPONENTSEX2_INTERFACE"></span>[**IVssBackupComponentsEx2-Schnittstelle**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponentsex2)
</dt> <dd>

<dl> <dt>

<span id="Added_method_"></span><span id="added_method_"></span><span id="ADDED_METHOD_"></span>Methode hinzugefügt:
</dt> <dd>

[**BreakSnapshotSetEx**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-breaksnapshotsetex)

</dd> </dl> </dd> </dl>

## <a name="new-vss-writers"></a>Neue VSS Writer

Windows Server 2008 und Windows Vista mit SP1 führen die folgenden VSS Writer ein:

-   IIS-Konfigurationswriter
-   IIS Metabase Writer
-   NPS VSS Writer
-   Remotedesktopdienste Gateway VSS Writer (Terminaldienste)
-   Remotedesktopdienste (Terminaldienste) – Lizenzierung von VSS Writer

Diese Writer sind in [In-Box VSS Writers](in-box-vss-writers.md)dokumentiert.

 

 



