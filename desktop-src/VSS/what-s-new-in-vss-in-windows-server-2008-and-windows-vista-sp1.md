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
# <a name="whats-new-in-vss-in-windows-server-2008-and-windows-vista-sp1"></a>Neues in VSS in Windows Server 2008 und Windows Vista SP1

Mit Windows Server 2008 und Windows Vista mit Service Pack 1 (SP1) werden die folgenden Änderungen am Volumeschattenkopie-Dienst eingeführt.

> [!Note]  
> Alle Änderungen für Windows Vista gelten für Windows Server 2008 und Windows Vista mit SP1. Ausführliche Informationen zu diesen Änderungen finden Sie unter [What es New in VSS in Windows Vista](what-s-new-in-vss-in-windows-vista.md).

 

-   [Neue VSS-Schnittstellen](#new-vss-interfaces)
-   [Neue VSS-Enumerationen](#new-vss-enumerations)
-   [Neue VSS-Strukturen](#new-vss-structures)
-   [Vorhandene Änderungen der VSS-Enumeration](#existing-vss-enumeration-modifications)
-   [Vorhandene Änderungen der VSS-Schnittstelle](#existing-vss-interface-modifications)
-   [Neue VSS-Writer](#new-vss-writers)

## <a name="new-vss-interfaces"></a>Neue VSS-Schnittstellen

<dl>

[**IVssDifferentialSoftwareSnapshotMgmt3**](/windows/desktop/api/VsMgmt/nn-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt3)  
[**Ivsshardwaresnapshotproviderex**](/windows/desktop/api/VsProv/nn-vsprov-ivsshardwaresnapshotproviderex)  
</dl>

## <a name="new-vss-enumerations"></a>Neue VSS-Enumerationen

<dl>

[**\_VSS- \_ Hardware \_ Optionen**](/windows/desktop/api/Vss/ne-vss-vss_hardware_options)  
[**VSS- \_ Schutz \_ Fehler**](/windows/desktop/api/VsMgmt/ne-vsmgmt-vss_protection_fault)  
[**VSS- \_ Schutz \_ Ebene**](/windows/desktop/api/VsMgmt/ne-vsmgmt-vss_protection_level)  
</dl>

## <a name="new-vss-structures"></a>Neue VSS-Strukturen

<dl>

[**VSS \_ - \_ \_ volumeschutzinformationen**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_volume_protection_info)  
</dl>

## <a name="existing-vss-enumeration-modifications"></a>Vorhandene Änderungen der VSS-Enumeration

<dl> <dt>

<span id="VSS_BACKUP_SCHEMA_enumeration"></span><span id="vss_backup_schema_enumeration"></span><span id="VSS_BACKUP_SCHEMA_ENUMERATION"></span>[**VSS \_ Sicherungs \_ Schema**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema) -Enumeration
</dt> <dd>

<dl> <dt>

<span id="Added_value_"></span><span id="added_value_"></span><span id="ADDED_VALUE_"></span>Hinzugefügter Wert:
</dt> <dd>

VSS \_ - \_ Writer-Writer \_ unterstützt \_ parallele \_ Wiederherstellungen

</dd> </dl> </dd> </dl>

<dl> <dt>

<span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_enumeration"></span><span id="_vss_volume_snapshot_attributes_enumeration"></span><span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_ENUMERATION"></span>Enumeration der [**\_ VSS- \_ volumemomentaufnahme- \_ \_ Attribute**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes)
</dt> <dd>

<dl> <dt>

<span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Hinzugefügte Werte:
</dt> <dd>

\_ \_ \_ verzögerte \_ PostSnapshot für VSS Volsnap attr

VSS \_ Volsnap \_ attr \_ TxF- \_ Wiederherstellung

</dd> </dl> </dd> </dl>

## <a name="existing-vss-interface-modifications"></a>Vorhandene Änderungen der VSS-Schnittstelle

<dl> <dt>

<span id="IVssBackupComponentsEx2_interface"></span><span id="ivssbackupcomponentsex2_interface"></span><span id="IVSSBACKUPCOMPONENTSEX2_INTERFACE"></span>[**IVssBackupComponentsEx2**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponentsex2) -Schnittstelle
</dt> <dd>

<dl> <dt>

<span id="Added_method_"></span><span id="added_method_"></span><span id="ADDED_METHOD_"></span>Hinzugefügte Methode:
</dt> <dd>

[**Breaksnapshotsekunden**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-breaksnapshotsetex)

</dd> </dl> </dd> </dl>

## <a name="new-vss-writers"></a>Neue VSS-Writer

In Windows Server 2008 und Windows Vista mit SP1 sind die folgenden VSS-Writer eingeführt:

-   IIS-konfigurationswriter
-   IIS-metabasiswriter
-   NPS-VSS-Writer
-   Remotedesktopdienste (Terminal Dienste) Gateway VSS Writer
-   Remotedesktopdienste (Terminal Dienste) Lizenzierungs-VSS Writer

Diese Writer sind in den [in-Box-VSS-Writern](in-box-vss-writers.md)dokumentiert.

 

 



