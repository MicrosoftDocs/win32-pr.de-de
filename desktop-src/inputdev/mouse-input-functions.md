---
title: 'Mauseingabefunktionen '
description: 'Mauseingabefunktionen '
ms.assetid: a666b25b-a75c-4500-8077-fabe07589a1d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c9b6abb4283ce4101b2e22c36653500db8109a0b8efbc01f9f3affe20c367a7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119717380"
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
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/win32/api/commctrl/nf-commctrl-_trackmouseevent"><strong>_TrackMouseEvent</strong></a><br/></td>
<td>Sendet Nachrichten, wenn der Mauszeiger ein Fenster verlässt oder für einen bestimmten Zeitraum auf ein Fenster zeigt. Diese Funktion ruft <a href="/windows/desktop/api/winuser/nf-winuser-trackmouseevent"><strong>TrackMouseEvent</strong></a> auf, sofern vorhanden, andernfalls emuliert sie es.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/winuser/nf-winuser-dragdetect"><strong>DragDetect</strong></a><br/></td>
<td>Erfasst die Maus und zeichnet ihre Bewegung auf, bis der Benutzer die linke Maustaste loslässt, die ESC-Taste drückt oder die Maus so bewegt, dass sie sich außerhalb des Ziehrechtecks um den angegebenen Punkt herum befindet. Die Breite und Höhe des Ziehrechtecks wird durch die <strong>SM_CXDRAG</strong> und <strong>SM_CYDRAG</strong> Werte angegeben, die von der <a href="/windows/desktop/api/winuser/nf-winuser-getsystemmetrics"><strong>GetSystemMetrics-Funktion</strong></a> zurückgegeben werden.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/winuser/nf-winuser-getcapture"><strong>GetCapture</strong></a><br/></td>
<td>Ruft ein Handle für das Fenster ab (sofern vorhanden), das die Maus erfasst hat. Nur jeweils ein Fenster kann die Maus erfassen. Dieses Fenster empfängt Mauseingaben, unabhängig davon, ob sich der Cursor innerhalb seiner Rahmen befindet oder nicht. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/winuser/nf-winuser-getdoubleclicktime"><strong>GetDoubleClickTime</strong></a><br/></td>
<td>Ruft die aktuelle Doppelklickzeit für die Maus ab. Ein Doppelklick ist eine Reihe von zwei Mausklicks, der zweite, der innerhalb eines angegebenen Zeitraums nach dem ersten auftritt. Die Doppelklickzeit ist die maximale Anzahl von Millisekunden, die zwischen dem ersten und zweiten Klick eines Doppelklicks auftreten können. Die maximale Doppelklickzeit beträgt 5.000 Millisekunden.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/winuser/nf-winuser-getmousemovepointsex"><strong>GetMouseMovePointsEx</strong></a><br/></td>
<td>Ruft einen Verlauf von bis zu 64 vorherigen Koordinaten der Maus oder des Stifts ab.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/winuser/nf-winuser-mouse_event"><strong>mouse_event</strong></a><br/></td>
<td>Die <a href="/windows/desktop/api/winuser/nf-winuser-mouse_event"><strong>mouse_event-Funktion</strong></a> synthetisiert Mausbewegungen und Schaltflächenklicks.<br/>
<blockquote>
[!Note]<br />
Diese Funktion wurde abgelöst. Verwenden Sie stattdessen <a href="/windows/desktop/api/winuser/nf-winuser-sendinput"><strong>SendInput.</strong></a>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/winuser/nf-winuser-releasecapture"><strong>ReleaseCapture</strong></a><br/></td>
<td>Gibt die Mauserfassung aus einem Fenster im aktuellen Thread frei und stellt die normale Verarbeitung der Mauseingabe wieder her. Ein Fenster, das die Maus erfasst hat, empfängt alle Mauseingaben, unabhängig von der Position des Cursors, außer wenn auf eine Maustaste geklickt wird, während sich der Cursor-Hot Spot im Fenster eines anderen Threads befindet. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/winuser/nf-winuser-setcapture"><strong>SetCapture</strong></a><br/></td>
<td>Legt die Mauserfassung auf das angegebene Fenster fest, das zum aktuellen Thread gehört.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/winuser/nf-winuser-setdoubleclicktime"><strong>SetDoubleClickTime</strong></a><br/></td>
<td>Legt die Doppelklickzeit für die Maus fest. Bei einem Doppelklick handelt es sich um eine Reihe von zwei Mausklicks, der zweite klickt innerhalb eines angegebenen Zeitraums nach dem ersten Klick. Die Doppelklickzeit ist die maximale Anzahl von Millisekunden, die zwischen dem ersten und zweiten Klick eines Doppelklicks auftreten können. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/winuser/nf-winuser-swapmousebutton"><strong>SwapMouseButton</strong></a><br/></td>
<td>Kehrt die Bedeutung der linken und rechten Maustaste um oder stellt sie wieder her. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/winuser/nf-winuser-trackmouseevent"><strong>TrackMouseEvent</strong></a><br/></td>
<td>Sendet Nachrichten, wenn der Mauszeiger ein Fenster verlässt oder für einen bestimmten Zeitraum auf ein Fenster zeigt.<br/>
<blockquote>
[!Note]<br />
Die <a href="/windows/win32/api/commctrl/nf-commctrl-_trackmouseevent"><strong>_TrackMouseEvent-Funktion</strong></a> ruft <a href="/windows/desktop/api/winuser/nf-winuser-trackmouseevent"><strong>TrackMouseEvent</strong></a> auf, sofern vorhanden, andernfalls <strong>emuliert _TrackMouseEvent</strong> <strong>TrackMouseEvent.</strong>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

 

