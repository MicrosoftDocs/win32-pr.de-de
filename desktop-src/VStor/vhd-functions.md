---
description: 'Weitere Informationen finden Sie hier: <span id=vhd.vhd_functions></span> Virtual Disk Functions'
MS-HAID: vhd.vhd\_functions
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Virtual Disk-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4f31af2b24a55baa3c64bfe5bd9e09e0b9e2f59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345728"
---
# <a name="span-idvhdvhd_functionsspanvirtual-disk-functions"></a><span id="vhd.vhd_functions"></span>Virtual Disk-Funktionen

Die folgenden Funktionen werden in virtuellen Datenträgern verwendet:

## <a name="span-idin_this_sectionspanin-this-section"></a><span id="in_this_section"></span>In diesem Abschnitt

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Thema</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="/windows/win32/api/virtdisk/nf-virtdisk-applysnapshotvhdset"><strong>Applysnapshotvhdset</strong></a></p></td>
<td><p>Wendet eine Momentaufnahme des aktuellen virtuellen Datenträgers für VHD-Set-Dateien an.</p></td>
</tr>
<tr class="even">
<td><p><a href="/windows/desktop/api/virtdisk/nf-virtdisk-addvirtualdiskparent"><strong>Addvirtualdiskparent</strong></a></p></td>
<td><p>Fügt einem virtuellen Datenträger, der mit dem <strong>OPEN_VIRTUAL_DISK_FLAG_CUSTOM_DIFF_CHAIN</strong> -Flag geöffnet wurde, ein übergeordnetes Element</p></td>
</tr>
<tr class="odd">
<td><p><a href="/windows/win32/api/virtdisk/nf-virtdisk-attachvirtualdisk"><strong>Attachvirtualdisk</strong></a></p></td>
<td><p>Fügt eine virtuelle Festplatte (VHD) oder eine CD-oder DVD-Abbild Datei (ISO) an, indem ein geeigneter VHD-Anbieter zum Erreichen der Anlage gefunden wird.</p></td>
</tr>
<tr class="even">
<td><p><a href="/windows/win32/api/virtdisk/nf-virtdisk-breakmirrorvirtualdisk"><strong>Breakmirrorvirtualdisk</strong></a></p></td>
<td><p>Unterbricht einen zuvor initiierten Spiegel Vorgang und legt den Spiegel als aktiven virtuellen Datenträger fest.</p></td>
</tr>
<tr class="odd">
<td><p><a href="/windows/win32/api/virtdisk/nf-virtdisk-compactvirtualdisk"><strong>Compactvirtualdisk</strong></a></p></td>
<td><p>Verringert die Größe einer Sicherungs Speicherdatei für eine virtuelle Festplatte (VHD).</p></td>
</tr>
<tr class="even">
<td><p><a href="/windows/win32/api/virtdisk/nf-virtdisk-createvirtualdisk"><strong>"Kreatevirtualdisk"</strong></a></p></td>
<td><p>Erstellt eine virtuelle Festplatten Abbild Datei (VHD), entweder mithilfe von Standardparametern oder mithilfe eines vorhandenen virtuellen Datenträgers oder physischen Datenträgers.</p></td>
</tr>
<tr class="odd">
<td><p><a href="/windows/win32/api/virtdisk/nf-virtdisk-deletesnapshotvhdset"><strong>Delta-esnapshotvhdset</strong></a></p></td>
<td><p>Löscht eine Momentaufnahme aus einer VHD-Satz Datei.</p></td>
</tr>
<tr class="even">
<td><p><a href="/windows/desktop/api/virtdisk/nf-virtdisk-deletevirtualdiskmetadata"><strong>Deletevirtualdiskmetadata</strong></a></p></td>
<td><p>Löscht Metadaten von einem virtuellen Datenträger.</p></td>
</tr>
<tr class="odd">
<td><p><a href="/windows/win32/api/virtdisk/nf-virtdisk-detachvirtualdisk"><strong>Detachvirtualdisk</strong></a></p></td>
<td><p>Trennt eine virtuelle Festplatte (VHD) oder eine CD-oder DVD-Abbild Datei (ISO), indem Sie einen entsprechenden virtuellen Datenträger Anbieter zum Ausführen des Vorgangs sucht.</p></td>
</tr>
<tr class="even">
<td><p><a href="/windows/desktop/api/virtdisk/nf-virtdisk-enumeratevirtualdiskmetadata"><strong>Enumeratevirtualdiskmetadata</strong></a></p></td>
<td><p>Listet die Metadaten auf, die einem virtuellen Datenträger zugeordnet sind.</p></td>
</tr>
<tr class="odd">
<td><p><a href="/windows/win32/api/virtdisk/nf-virtdisk-expandvirtualdisk"><strong>Expandvirtualdisk</strong></a></p></td>
<td><p>Vergrößert die Größe einer festen oder dynamisch erweiterbaren virtuellen Festplatte (VHD).</p></td>
</tr>
<tr class="even">
<td><p><a href="/windows/win32/api/virtdisk/nf-virtdisk-getstoragedependencyinformation"><strong>Getstoragedependencyinformation</strong></a></p></td>
<td><p>Gibt die Beziehungen zwischen virtuellen Festplatten (VHDs), CD-oder DVD-Abbild Datei (ISO) oder den Volumes auf diesen Datenträgern und dem übergeordneten Datenträger oder Volume zurück.</p></td>
</tr>
<tr class="odd">
<td><p><a href="/windows/win32/api/virtdisk/nf-virtdisk-getvirtualdiskinformation"><strong>Getvirtualdiskinformation</strong></a></p></td>
<td><p>Ruft Informationen zu einer virtuellen Festplatte ab.</p></td>
</tr>
<tr class="even">
<td><p><a href="/windows/desktop/api/virtdisk/nf-virtdisk-getvirtualdiskmetadata"><strong>Getvirtualdiskmetadata</strong></a></p></td>
<td><p>Ruft die angegebenen Metadaten von der virtuellen Festplatte ab.</p></td>
</tr>
<tr class="odd">
<td><p><a href="/windows/win32/api/virtdisk/nf-virtdisk-getvirtualdiskoperationprogress"><strong>Getvirtualdiskoperationprogress</strong></a></p></td>
<td><p>Überprüft den Fortschritt eines asynchronen virtuellen Festplatten Vorgangs (VHD).</p></td>
</tr>
<tr class="even">
<td><p><a href="/windows/win32/api/virtdisk/nf-virtdisk-getvirtualdiskphysicalpath"><strong>Getvirtualdiskphysicalpath</strong></a></p></td>
<td><p>Ruft den Pfad zum physischen Geräte Objekt ab, das eine virtuelle Festplatte (VHD) oder eine CD-oder DVD-Abbild Datei (ISO) enthält.</p></td>
</tr>
<tr class="odd">
<td><p><a href="/windows/win32/api/virtdisk/nf-virtdisk-mergevirtualdisk"><strong>Mergevirtualdisk</strong></a></p></td>
<td><p>Führt eine untergeordnete virtuelle Festplatte (VHD) in einer differenzierenden Kette mit mindestens einem übergeordneten virtuellen Datenträger in der Kette zusammen.</p></td>
</tr>
<tr class="even">
<td><p><a href="/windows/win32/api/virtdisk/nf-virtdisk-mirrorvirtualdisk"><strong>Mirrorvirtualdisk</strong></a></p></td>
<td><p>Initiiert eine Spiegel Operation für einen virtuellen Datenträger.</p></td>
</tr>
<tr class="odd">
<td><p><a href="/windows/win32/api/virtdisk/nf-virtdisk-modifyvhdset"><strong>Modifyvhdset</strong></a></p></td>
<td><p>Ändert den internen Inhalt einer virtuellen Datenträger Datei. Kann zum Festlegen des aktiven Blatts oder zum Beheben von Momentaufnahme Einträgen verwendet werden.</p></td>
</tr>
<tr class="even">
<td><p><a href="/windows/win32/api/virtdisk/nf-virtdisk-openvirtualdisk"><strong>Openvirtualdisk</strong></a></p></td>
<td><p>Öffnet eine virtuelle Festplatte (VHD) oder eine CD-oder DVD-Abbild Datei (ISO) zur Verwendung.</p></td>
</tr>
<tr class="odd">
<td><p><a href="/windows/win32/api/virtdisk/nf-virtdisk-querychangesvirtualdisk"><strong>Querychangesvirtualdisk</strong></a></p></td>
<td><p>Ruft Informationen zu Änderungen an den angegebenen Bereichen einer virtuellen Festplatte (VHD) ab, die von der robusten Änderungs Nachverfolgung (RCT) nachverfolgt werden.</p></td>
</tr>
<tr class="even">
<td><p><a href="/windows/win32/api/virtdisk/nf-virtdisk-rawscsivirtualdisk"><strong>Rawscsivirtualdisk</strong></a></p></td>
<td><p>Gibt eine eingebettete SCSI-Anforderung direkt an eine virtuelle Festplatte aus.</p></td>
</tr>
<tr class="odd">
<td><p><a href="/windows/desktop/api/virtdisk/nf-virtdisk-resizevirtualdisk"><strong>Resizevirtualdisk</strong></a></p></td>
<td><p>Ändert die Größe eines virtuellen Datenträgers.</p></td>
</tr>
<tr class="even">
<td><p><a href="/windows/win32/api/virtdisk/nf-virtdisk-setvirtualdiskinformation"><strong>Setvirtualdiskinformation</strong></a></p></td>
<td><p>Legt Informationen zu einer virtuellen Festplatte (VHD) fest.</p></td>
</tr>
<tr class="odd">
<td><p><a href="/windows/desktop/api/virtdisk/nf-virtdisk-setvirtualdiskmetadata"><strong>Setvirtualdiskmetadata</strong></a></p></td>
<td><p>Legt ein Metadatenelement für einen virtuellen Datenträger fest.</p></td>
</tr>
<tr class="even">
<td><p><a href="/windows/win32/api/virtdisk/nf-virtdisk-takesnapshotvhdset"><strong>Takesnapshotvhdset</strong></a></p></td>
<td><p>Erstellt eine Momentaufnahme des aktuellen virtuellen Datenträgers für VHD-Satz Dateien.</p></td>
</tr>
</tbody>
</table>

 

 

 
