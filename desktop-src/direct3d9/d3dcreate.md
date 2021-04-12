---
description: Eine Kombination aus einem oder mehreren Flags, die das Erstellungs Verhalten des Geräts steuern.
ms.assetid: 91387a2d-3927-4285-a09b-9ce247e6bfdd
title: D3DCREATE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14de345d6cb6d164ee5cd3067e1f38ff66d9795d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958487"
---
# <a name="d3dcreate"></a>D3DCREATE

Eine Kombination aus einem oder mehreren Flags, die das Erstellungs Verhalten des Geräts steuern.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>#definieren</td>
<td>BESCHREIBUNG</td>
</tr>
<tr class="even">
<td>D3DCREATE_ADAPTERGROUP_DEVICE</td>
<td>Die Anwendung fordert das Gerät auf, alle Köpfe zu steuern, die dieser Master Adapter besitzt. Das Flag ist für nicht-Master Adapter unzulässig. Wenn dieses Flag festgelegt ist, sollten die an " <a href="/windows/desktop/api"><strong>kreatedevice</strong></a> " übergeben Präsentations Parameter auf ein Array von <a href="d3dpresent-parameters.md"><strong>D3DPRESENT_PARAMETERS</strong></a>zeigen. Die Anzahl der Elemente in <strong>D3DPRESENT_PARAMETERS</strong> sollte gleich der Anzahl von Adaptern sein, die durch den "zahlofadaptersingroup"-Member der <a href="/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9"><strong>D3DCAPS9</strong></a> -Struktur definiert werden. Die DirectX-Laufzeit weist jedes Element jedem Kopf in der numerischen Reihenfolge zu, die durch den adapterordinalingroup-Member von <strong>D3DCAPS9</strong>angegeben wird.</td>
</tr>
<tr class="odd">
<td>D3DCREATE_DISABLE_DRIVER_MANAGEMENT</td>
<td>Direct3D verwaltet Ressourcen anstelle des Treibers. Direct3D-Aufrufe schlagen für Ressourcen Fehler wie nicht ausreichenden Video Arbeitsspeicher fehl.</td>
</tr>
<tr class="even">
<td>D3DCREATE_DISABLE_DRIVER_MANAGEMENT_EX</td>
<td>Wie D3DCREATE_DISABLE_DRIVER_MANAGEMENT verwaltet Direct3D Ressourcen anstelle des Treibers. Im Gegensatz zu D3DCREATE_DISABLE_DRIVER_MANAGEMENT gibt D3DCREATE_DISABLE_DRIVER_MANAGEMENT_EX Fehler für Bedingungen zurück, wie z. b. unzureichenden Videospeicher.</td>
</tr>
<tr class="odd">
<td>D3DCREATE_DISABLE_PRINTSCREEN</td>
<td>Bewirkt, dass die Laufzeit keine Hotkeys für PrintScreen, Ctrl-Printscreen und Alt-Printscreen registriert, um den Inhalt des Desktops oder Fensters zu erfassen. 
<table>
<tbody>
<tr class="odd">
<td>Unterschiede zwischen Direct3D 9 und Direct3D 9Ex:<br/> Dieses Flag ist nur in Direct3D 9Ex verfügbar.<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>D3DCREATE_DISABLE_PSGP_THREADING</td>
<td>Beschränken Sie die Berechnung auf den Hauptanwendungs Thread. Wenn das Flag nicht festgelegt ist, kann die Laufzeit die Verarbeitung von Software Scheitel Punkten und andere Berechnungen im Arbeits Thread durchführen, um die Leistung von Multiprozessorsystemen zu verbessern. 
<table>
<tbody>
<tr class="odd">
<td>Unterschiede zwischen Windows XP und Windows Vista:<br/> Dieses Flag ist unter Windows Vista, Windows Server 2008 und Windows 7 verfügbar.<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>D3DCREATE_ENABLE_PRESENTSTATS</td>
<td>Ermöglicht das Sammeln der aktuellen Statistiken auf dem Gerät. Aufrufe von <a href="/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)"><strong>getpresentstatistics</strong></a> geben gültige Daten zurück. 
<table>
<tbody>
<tr class="odd">
<td>Unterschiede zwischen Direct3D 9 und Direct3D 9Ex:<br/> Dieses Flag ist nur in Direct3D 9Ex verfügbar.<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>D3DCREATE_FPU_PRESERVE</td>
<td>Legen Sie die Genauigkeit für Gleit Komma Berechnungen Direct3D auf die vom aufrufenden Thread verwendete Genauigkeit fest. Wenn Sie dieses Flag nicht angeben, ist Direct3D standardmäßig auf den Modus mit einfacher Genauigkeit und aus zwei Gründen festgelegt:
<ul>
<li>Der Modus mit doppelter Genauigkeit führt zu einer Verringerung der Direct3D-Leistung.</li>
<li>Teile von Direct3D gehen davon aus, dass Ausnahmen von Gleit Komma Einheiten maskiert werden. die Maskierung dieser Ausnahmen kann zu undefiniertem Verhalten führen.</li>
</ul></td>
</tr>
<tr class="odd">
<td>D3DCREATE_HARDWARE_VERTEXPROCESSING</td>
<td>Gibt die Vertex-Hardware Verarbeitung an.</td>
</tr>
<tr class="even">
<td>D3DCREATE_MIXED_VERTEXPROCESSING</td>
<td>Gibt die Vertexverarbeitung von gemischten (sowohl Software-als auch Hardware) an. Für Windows 10, Version 1607 und höher, wird die Verwendung dieser Einstellung nicht empfohlen. Siehe D3DCREATE_SOFTWARE_VERTEXPROCESSING.</td>
</tr>
<tr class="odd">
<td>D3DCREATE_SOFTWARE_VERTEXPROCESSING</td>
<td>Gibt die Verarbeitung von Software Scheitel Punkten an. Für Windows 10, Version 1607 und höher, wird die Verwendung dieser Einstellung nicht empfohlen. Verwenden Sie D3DCREATE_HARDWARE_VERTEXPROCESSING.
<div class="alert">
<blockquote>
[!Note]<br />
Wenn die Verarbeitung von Hardware Scheitel Punkten nicht verfügbar ist, wird die Verwendung der Verarbeitung von Software Scheitel Punkten in Windows 10, Version 1607 (und höheren Versionen), nicht empfohlen, da die Effizienz der Verarbeitung von Software Scheitel Punkten erheblich reduziert wurde und gleichzeitig die Sicherheit der Implementierung verbessert wurde.
</blockquote>
</div>
<div>
 
</div></td>
</tr>
<tr class="even">
<td>D3DCREATE_MULTITHREADED</td>
<td>Gibt an, dass die Anwendung Direct3D als multithreadsicher anfordert. Dadurch wird ein Direct3D-Thread häufiger in den Besitz seines globalen <a href="/windows/desktop/Sync/critical-section-objects">kritischen Abschnitts</a> übertragen, wodurch die Leistung beeinträchtigt werden kann. Wenn eine Anwendung Fenster Nachrichten in einem Thread verarbeitet, während Direct3D-API-Aufrufe in einer anderen vorgenommen werden, muss die Anwendung dieses Flag beim Erstellen des Geräts verwenden. Dieses Fenster muss vor dem Entladen d3d9.dll ebenfalls zerstört werden.</td>
</tr>
<tr class="odd">
<td>D3DCREATE_NOWINDOWCHANGES</td>
<td>Gibt an, dass Direct3D das Fokus Fenster in keiner Weise ändern darf.
<div class="alert">
<blockquote>
[!Note]<br />
Wenn dieses Flag festgelegt ist, muss die Anwendung alle Fokus Verwaltungs Ereignisse vollständig unterstützen, z. b. Alt + Tab-und Mausklicks-Ereignisse.
</blockquote>
</div>
<div>
 
</div></td>
</tr>
<tr class="even">
<td>D3DCREATE_PUREDEVICE</td>
<td>Gibt an, dass Direct3D Get *-Aufrufe für Elemente, die in Zustands Blöcken gespeichert werden können, nicht unterstützt. Es weist auch Direct3D an, keine Emulations Dienste für die Vertexverarbeitung bereitzustellen. Dies bedeutet Folgendes: Wenn das Gerät die Scheitelpunkt Verarbeitung nicht unterstützt, kann die Anwendung nur nachträglich transformierte Vertices verwenden.</td>
</tr>
<tr class="odd">
<td>D3DCREATE_SCREENSAVER</td>
<td>Ermöglicht Screensaver während einer Vollbild-Anwendung. Ohne dieses Flag deaktiviert Direct3D Screensaver so lange, wie es sich bei der aufrufenden Anwendung um Fullscreen handelt. Wenn die aufrufenden Anwendung bereits ein Bildschirmschoner ist, hat dieses Flag keine Auswirkungen. 
<table>
<tbody>
<tr class="odd">
<td>Unterschiede zwischen Direct3D 9 und Direct3D 9Ex:<br/> Dieses Flag ist nur in Direct3D 9Ex verfügbar.<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

D3DCREATE \_ Hardware \_ vertexprocessing, D3DCREATE \_ mixed \_ vertexprocessing und D3DCREATE \_ Software \_ vertexprocessing sind sich gegenseitig ausschließende Flags. Beim Aufrufen von [**createdevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice)muss mindestens eine dieser Scheitelpunkt-vertexflags angegeben werden.

## <a name="constant-information"></a>Konstante Informationen



|                          |            |
|--------------------------|------------|
| Header                   | D3d9. h     |
| Mindestens Betriebssystem | Windows 98 |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Konstanten](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
