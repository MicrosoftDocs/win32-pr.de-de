---
description: 'Weitere Informationen zu: <span id=vhd.vhd_functions></span> Virtual Disk Functions'
MS-HAID: vhd.vhd\_functions
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Funktionen für virtuelle Datenträger
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32133e3afa8402de8483a68eb4957b261b46e556
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477216"
---
# <a name="span-idvhdvhd_functionsspanvirtual-disk-functions"></a><span id="vhd.vhd_functions"></span>Funktionen für virtuelle Datenträger

Die folgenden Funktionen werden in virtuellen Datenträgern verwendet:

## <a name="span-idin_this_sectionspanin-this-section"></a><span id="in_this_section"></span>In diesem Abschnitt


| Thema | BESCHREIBUNG | 
|-------|-------------|
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-applysnapshotvhdset"><strong>ApplySnapshotVhdSet</strong></a></p> | <p>Wendet eine Momentaufnahme des aktuellen virtuellen Datenträgers für VHD-Set-Dateien an.</p> | 
| <p><a href="/windows/desktop/api/virtdisk/nf-virtdisk-addvirtualdiskparent"><strong>AddVirtualDiskParent</strong></a></p> | <p>Fügt ein übergeordnetes Element an einen virtuellen Datenträger an, der mit dem <strong>flag OPEN_VIRTUAL_DISK_FLAG_CUSTOM_DIFF_CHAIN</strong> geöffnet wurde.</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-attachvirtualdisk"><strong>AttachVirtualDisk</strong></a></p> | <p>Fügt eine virtuelle Festplatte (Virtual Hard Disk, VHD) oder EINE CD- oder DVD-Imagedatei (ISO) an, indem ein geeigneter VHD-Anbieter für die Anlage vorhanden ist.</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-breakmirrorvirtualdisk"><strong>BreakMirrorVirtualDisk</strong></a></p> | <p>Unterbricht einen zuvor initiierten Spiegelungsvorgang und legt die Spiegelung auf den aktiven virtuellen Datenträger fest.</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-compactvirtualdisk"><strong>CompactVirtualDisk</strong></a></p> | <p>Reduziert die Größe einer Sicherungsdatei für virtuelle Festplatten (VHD).</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-createvirtualdisk"><strong>CreateVirtualDisk</strong></a></p> | <p>Erstellt eine VHD-Imagedatei (Virtuelle Festplatte), entweder mithilfe von Standardparametern oder mithilfe eines vorhandenen virtuellen Datenträgers oder physischen Datenträgers.</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-deletesnapshotvhdset"><strong>DeleteSnapshotVhdSet</strong></a></p> | <p>Löscht eine Momentaufnahme aus einer VHD-Satzdatei.</p> | 
| <p><a href="/windows/desktop/api/virtdisk/nf-virtdisk-deletevirtualdiskmetadata"><strong>DeleteVirtualDiskMetadata</strong></a></p> | <p>Löscht Metadaten von einem virtuellen Datenträger.</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-detachvirtualdisk"><strong>DetachVirtualDisk</strong></a></p> | <p>Trennt eine virtuelle Festplatte (Virtual Hard Disk, VHD) oder eine CD- oder DVD-Imagedatei (ISO), indem ein geeigneter Anbieter virtueller Datenträger für den Vorgang suchen.</p> | 
| <p><a href="/windows/desktop/api/virtdisk/nf-virtdisk-enumeratevirtualdiskmetadata"><strong>EnumerateVirtualDiskMetadata</strong></a></p> | <p>Listet die einem virtuellen Datenträger zugeordneten Metadaten auf.</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-expandvirtualdisk"><strong>ExpandVirtualDisk</strong></a></p> | <p>Erhöht die Größe einer festen oder dynamisch erweiterbaren virtuellen Festplatte (VHD).</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-getstoragedependencyinformation"><strong>GetStorageDependencyInformation</strong></a></p> | <p>Gibt die Beziehungen zwischen virtuellen Festplatten (VHDs) oder CD- oder DVD-Imagedateien (ISO) oder den in diesen Datenträgern enthaltenen Volumes und deren übergeordnetem Datenträger oder Volume zurück.</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-getvirtualdiskinformation"><strong>GetVirtualDiskInformation</strong></a></p> | <p>Ruft Informationen zu einer VHD ab.</p> | 
| <p><a href="/windows/desktop/api/virtdisk/nf-virtdisk-getvirtualdiskmetadata"><strong>GetVirtualDiskMetadata</strong></a></p> | <p>Ruft die angegebenen Metadaten vom virtuellen Datenträger ab.</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-getvirtualdiskoperationprogress"><strong>GetVirtualDiskOperationProgress</strong></a></p> | <p>Überprüft den Fortschritt eines asynchronen Vorgangs einer virtuellen Festplatte (VHD).</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-getvirtualdiskphysicalpath"><strong>GetVirtualDiskPhysicalPath</strong></a></p> | <p>Ruft den Pfad zum physischen Geräteobjekt ab, das eine virtuelle Festplatte (VHD) oder EINE CD- oder DVD-Imagedatei (ISO) enthält.</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-mergevirtualdisk"><strong>MergeVirtualDisk</strong></a></p> | <p>Führt eine untergeordnete virtuelle Festplatte (VHD) in einer differenzierenden Kette mit mindestens einem übergeordneten virtuellen Datenträger in der Kette zusammen.</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-mirrorvirtualdisk"><strong>MirrorVirtualDisk</strong></a></p> | <p>Initiiert einen Spiegelungsvorgang für einen virtuellen Datenträger.</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-modifyvhdset"><strong>ModifyVhdSet</strong></a></p> | <p>Ändert den internen Inhalt einer virtuellen Datenträgerdatei. Kann verwendet werden, um das aktive Blatt festzulegen oder Momentaufnahmeeinträge zu korrigieren.</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-openvirtualdisk"><strong>OpenVirtualDisk</strong></a></p> | <p>Öffnet eine virtuelle Festplatte (VHD) oder CD- oder DVD-Imagedatei (ISO) zur Verwendung.</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-querychangesvirtualdisk"><strong>QueryChangesVirtualDisk</strong></a></p> | <p>Ruft Informationen zu Änderungen an den angegebenen Bereichen einer virtuellen Festplatte (VHD) ab, die durch resiliente Änderungsnachverfolgung (Resilient Change Tracking, RCT) nachverfolgt werden.</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-rawscsivirtualdisk"><strong>RawSCSIVirtualDisk</strong></a></p> | <p>Gibt eine eingebettete SCSI-Anforderung direkt an eine virtuelle Festplatte aus.</p> | 
| <p><a href="/windows/desktop/api/virtdisk/nf-virtdisk-resizevirtualdisk"><strong>ResizeVirtualDisk</strong></a></p> | <p>Ändern der Größe eines virtuellen Datenträgers.</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-setvirtualdiskinformation"><strong>SetVirtualDiskInformation</strong></a></p> | <p>Legt Informationen zu einer virtuellen Festplatte (VHD) fest.</p> | 
| <p><a href="/windows/desktop/api/virtdisk/nf-virtdisk-setvirtualdiskmetadata"><strong>SetVirtualDiskMetadata</strong></a></p> | <p>Legt ein Metadatenelement für einen virtuellen Datenträger fest.</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-takesnapshotvhdset"><strong>TakeSnapshotVhdSet</strong></a></p> | <p>Erstellt eine Momentaufnahme des aktuellen virtuellen Datenträgers für VHD-Set-Dateien.</p> | 


 

 

 
