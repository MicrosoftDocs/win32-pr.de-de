---
title: 'Mauseingabefunktionen '
description: .
ms.assetid: a666b25b-a75c-4500-8077-fabe07589a1d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47437458cc8ad2bf85ecfa0d8676af8d26c67b89
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "103734976"
---
# <a name="mouse-input-functions"></a>Mauseingabefunktionen 


## <a name="in-this-section"></a>In diesem Abschnitt



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
<td><a href="/windows/win32/api/commctrl/nf-commctrl-_trackmouseevent"><strong>_TrackMouseEvent</strong></a><br/></td>
<td>Sendet Nachrichten, wenn der Mauszeiger ein Fenster verlässt oder für einen bestimmten Zeitraum auf ein Fenster zeigt. Diese Funktion ruft <a href="/windows/desktop/api/winuser/nf-winuser-trackmouseevent"><strong>trackmougevent</strong></a> auf, wenn Sie vorhanden ist, andernfalls emuliert sie.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/winuser/nf-winuser-dragdetect"><strong>Dragdetect</strong></a><br/></td>
<td>Erfasst die Maus und zeichnet ihre Bewegung auf, bis der Benutzer die linke Maustaste loslässt, die ESC-Taste drückt oder die Maus so bewegt, dass sie sich außerhalb des Ziehrechtecks um den angegebenen Punkt herum befindet. Die Breite und Höhe des Zieh Rechtecks werden durch die <strong>SM_CXDRAG</strong> -und <strong>SM_CYDRAG</strong> Werte angegeben, die von der <a href="/windows/desktop/api/winuser/nf-winuser-getsystemmetrics"><strong>GetSystemMetrics</strong></a> -Funktion zurückgegeben werden.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/winuser/nf-winuser-getcapture"><strong>GetCapture</strong></a><br/></td>
<td>Ruft ein Handle für das Fenster (sofern vorhanden) ab, das die Maus erfasst hat. Die Maus kann nur von einem Fenster erfasst werden. Dieses Fenster empfängt Maus Eingaben, unabhängig davon, ob sich der Cursor innerhalb seines Rahmens befindet. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/winuser/nf-winuser-getdoubleclicktime"><strong>Getdoubleclicktime</strong></a><br/></td>
<td>Ruft die aktuelle Doppelklick Zeit für die Maus ab. Ein Doppelklick ist eine Reihe von zwei Klicks der Maustaste, die zweite innerhalb eines angegebenen Zeitraums nach dem ersten. Bei der Doppelklick Zeit handelt es sich um die maximale Anzahl von Millisekunden, die zwischen dem ersten und zweiten Klick auf einen Doppelklick auftreten können. Die maximale Doppelklick Zeit beträgt 5000 Millisekunden.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/winuser/nf-winuser-getmousemovepointsex"><strong>Getmoucmuvepointsex</strong></a><br/></td>
<td>Ruft einen Verlauf von bis zu 64 vorherigen Koordinaten der Maus oder des Stifts ab.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/winuser/nf-winuser-mouse_event"><strong>mouse_event</strong></a><br/></td>
<td>Die <a href="/windows/desktop/api/winuser/nf-winuser-mouse_event"><strong>mouse_event</strong></a> -Funktion synthetisiert die Mausbewegung und Schaltflächen Klicks.<br/>
<blockquote>
[!Note]<br />
Diese Funktion wurde abgelöst. Verwenden Sie stattdessen <a href="/windows/desktop/api/winuser/nf-winuser-sendinput"><strong>SendInput</strong></a> .
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/winuser/nf-winuser-releasecapture"><strong>Releasecapture</strong></a><br/></td>
<td>Gibt die Maus Aufzeichnung von einem Fenster im aktuellen Thread frei und stellt die normale Verarbeitung der Maus Eingaben wieder her. Ein Fenster, das die Maus erfasst hat, erhält unabhängig von der Position des Cursors alle Maus Eingaben, außer wenn auf eine Maustaste geklickt wird, während sich der Cursor-Hotspot im Fenster eines anderen Threads befindet. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/winuser/nf-winuser-setcapture"><strong>SetCapture</strong></a><br/></td>
<td>Legt die Maus Aufzeichnung auf das angegebene Fenster fest, das zum aktuellen Thread gehört.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/winuser/nf-winuser-setdoubleclicktime"><strong>Setdoubleclicktime</strong></a><br/></td>
<td>Legt die Doppelklick Zeit für die Maus fest. Ein Doppelklick ist eine Reihe von zwei Mausklicks, die jeweils innerhalb eines angegebenen Zeitraums nach dem ersten auftreten. Der Doppelklick Zeitraum ist die maximale Anzahl von Millisekunden, die zwischen dem ersten und dem zweiten Mausklick eines Doppelklicks auftreten können. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/winuser/nf-winuser-swapmousebutton"><strong>Austausch Schaltfläche</strong></a><br/></td>
<td>Kehrt die Bedeutung der linken und rechten Maustaste um und stellt diese wieder her. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/winuser/nf-winuser-trackmouseevent"><strong>TrackMouseEvent</strong></a><br/></td>
<td>Sendet Nachrichten, wenn der Mauszeiger ein Fenster verlässt oder für einen bestimmten Zeitraum auf ein Fenster zeigt.<br/>
<blockquote>
[!Note]<br />
Die <a href="/windows/win32/api/commctrl/nf-commctrl-_trackmouseevent"><strong>_TrackMouseEvent</strong></a> -Funktion ruft <a href="/windows/desktop/api/winuser/nf-winuser-trackmouseevent"><strong>trackmouserevent</strong></a> auf, wenn Sie vorhanden ist, andernfalls emuliert <strong>_TrackMouseEvent</strong> <strong>trackmousevent</strong>.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

 

