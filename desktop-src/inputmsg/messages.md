---
title: Meldungen
description: Die Themen in diesem Abschnitt enthalten die Referenz Spezifikationen für bestimmte Zeiger Eingabe Meldungen und-Benachrichtigungen.
ms.assetid: 65F4DCD0-DAE1-4AC2-AB36-23D114803138
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 3e143990c65daad306ef6f743d25ef4e0cca8001
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390298"
---
# <a name="messages"></a>Meldungen

Die Themen in diesem Abschnitt enthalten die Referenz Spezifikationen für bestimmte [Zeiger Eingabe Meldungen und-Benachrichtigungen](messages-and-notifications-portal.md).

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
<td>[<strong>DM_POINTERHITTEST</strong>] (DM-pointerhittest.MD)<br/></td>
<td>Wird an ein Fenster gesendet, wenn eine Zeiger Eingabe zuerst erkannt wird, um das wahrscheinlichste Eingabe Ziel für die [direkte Bearbeitung](/previous-versions/windows/desktop/directmanipulation/direct-manipulation-portal)zu ermitteln. <br/></td>
</tr>
<tr class="even">
<td>[<strong>WM_NCPOINTERDOWN</strong>] (WM-ncpointerdown.MD)<br/></td>
<td>Wird gepostet, wenn ein Zeiger einen Kontakt über den nicht-Client Bereich eines Fensters herstellt. Die Meldung zielt auf das Fenster ab, über das der Zeiger Kontakt herstellt. Der Zeiger wird implizit im Fenster erfasst, sodass das Fenster weiterhin Eingaben für den Zeiger empfängt, bis der Kontakt unterbrochen wird. <br/> Wenn ein Fenster diesen Zeiger aufgezeichnet hat, wird diese Meldung nicht gepostet. Stattdessen wird ein [<strong>WM_POINTERDOWN</strong>] (WM-pointerdown.MD) an das Fenster gesendet, das diesen Zeiger aufgezeichnet hat. <br/>
<blockquote>
[!Important]<br />
Desktop-Apps sollten dpi-fähig sein. Wenn Ihre APP nicht dpi-fähig ist, können Bildschirm Koordinaten, die in Zeiger Nachrichten und zugehörigen Strukturen enthalten sind, aufgrund der dpi-Virtualisierung ungenau erscheinen. Die dpi-Virtualisierung bietet Unterstützung für die automatische Skalierung für Anwendungen, die nicht mit dpi-Werten kompatibel sind und standardmäßig aktiv sind (Benutzer können Sie deaktivieren). Weitere Informationen finden Sie unter [Schreiben von High-dpi-Win32-Anwendungen](/previous-versions//dd464660(v=vs.85)).
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>[<strong>WM_NCPOINTERUP</strong>] (WM-ncpointerup.MD)<br/></td>
<td>Wird gepostet, wenn ein Zeiger, der den Kontakt über den nicht-Client Bereich eines Fensters hergestellt hat, den Kontakt unterbricht. Die Nachricht bezieht sich auf das Fenster, über das der Zeiger Kontakt herstellt, und der Zeiger ist an diesem Punkt implizit im Fenster erfasst, sodass das Fenster weiterhin Eingaben für den Zeiger empfängt, bis der Kontakt unterbrochen wird, einschließlich der [<strong>WM_NCPOINTERUP</strong>] (WM-ncpointerup.MD)-Benachrichtigung. <br/> Wenn ein Fenster diesen Zeiger aufgezeichnet hat, wird diese Meldung nicht gepostet. Stattdessen wird ein [<strong>WM_POINTERUP</strong>] (WM-pointerup.MD) an das Fenster gesendet, das diesen Zeiger aufgezeichnet hat. <br/>
<blockquote>
[!Important]<br />
Desktop-Apps sollten dpi-fähig sein. Wenn Ihre APP nicht dpi-fähig ist, können Bildschirm Koordinaten, die in Zeiger Nachrichten und zugehörigen Strukturen enthalten sind, aufgrund der dpi-Virtualisierung ungenau erscheinen. Die dpi-Virtualisierung bietet Unterstützung für die automatische Skalierung für Anwendungen, die nicht mit dpi-Werten kompatibel sind und standardmäßig aktiv sind (Benutzer können Sie deaktivieren). Weitere Informationen finden Sie unter [Schreiben von High-dpi-Win32-Anwendungen](/previous-versions//dd464660(v=vs.85)).
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>[<strong>WM_NCPOINTERUPDATE</strong>] (WM-ncpointerupdate.MD)<br/></td>
<td>Wird bereitgestellt, um ein Update für einen Zeiger bereitzustellen, der den Kontakt über den nicht-Client Bereich eines Fensters hergestellt hat, oder wenn ein nicht erfasster Kontakt, der sich im nicht-Client Bereich eines Fensters bewegt, verschoben wird Während der Mauszeiger bewegt wird, wird die Nachricht auf das Fenster ausgerichtet, über das sich der Zeiger befindet. Während sich der Mauszeiger auf der-Oberfläche befindet, wird der Zeiger implizit in dem Fenster erfasst, über das der Zeiger den Kontakt hergestellt hat, und dieses Fenster empfängt weiterhin Eingaben für den Zeiger, bis der Kontakt unterbrochen wird. <br/> Wenn ein Fenster diesen Zeiger aufgezeichnet hat, wird diese Meldung nicht gepostet. Stattdessen wird ein [<strong>WM_POINTERUPDATE</strong>] (WM-pointerupdate.MD) an das Fenster gesendet, das diesen Zeiger aufgezeichnet hat.<br/>
<blockquote>
[!Important]<br />
Desktop-Apps sollten dpi-fähig sein. Wenn Ihre APP nicht dpi-fähig ist, können Bildschirm Koordinaten, die in Zeiger Nachrichten und zugehörigen Strukturen enthalten sind, aufgrund der dpi-Virtualisierung ungenau erscheinen. Die dpi-Virtualisierung bietet Unterstützung für die automatische Skalierung für Anwendungen, die nicht mit dpi-Werten kompatibel sind und standardmäßig aktiv sind (Benutzer können Sie deaktivieren). Weitere Informationen finden Sie unter [Schreiben von High-dpi-Win32-Anwendungen](/previous-versions//dd464660(v=vs.85)).
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>[<strong>WM_PARENTNOTIFY</strong>] (WM-parentnotify.MD)<br/></td>
<td>Wird an ein Fenster gesendet, wenn eine bedeutende Aktion in einem Nachfolger Fenster auftritt. Diese Nachricht ist nun so erweitert, dass Sie das [<strong>WM_POINTERDOWN</strong>] (WM-pointerdown.MD)-Ereignis einschließt. Wenn das untergeordnete Fenster erstellt wird, sendet das System [<strong>WM_PARENTNOTIFY</strong>] (/Previous-Versions/Windows/Desktop/inputmsg/WM-parentnotify) direkt vor der Funktion [up<strong>Window</strong>] (/Windows/Win32/API/winuser/NF-winuser-createwindowa) oder [up-<strong>windowex</strong>] (/Windows/Win32/API/winuser/NF-winuser-createwindowexa), die das Fenster erstellt, zurückgibt. Wenn das untergeordnete Fenster zerstört wird, sendet das System die Nachricht, bevor eine Verarbeitung zum Zerstören des Fensters erfolgt.<br/> Ein Fenster empfängt diese Meldung über seine [<strong>WindowProc</strong>] (/Previous-Versions/Windows/Desktop/Legacy/ms633573 (v = vs. 85))-Funktion. <br/>
<blockquote>
[!Important]<br />
Desktop-Apps sollten dpi-fähig sein. Wenn Ihre APP nicht dpi-fähig ist, können Bildschirm Koordinaten, die in Zeiger Nachrichten und zugehörigen Strukturen enthalten sind, aufgrund der dpi-Virtualisierung ungenau erscheinen. Die dpi-Virtualisierung bietet Unterstützung für die automatische Skalierung für Anwendungen, die nicht mit dpi-Werten kompatibel sind und standardmäßig aktiv sind (Benutzer können Sie deaktivieren). Weitere Informationen finden Sie unter [Schreiben von High-dpi-Win32-Anwendungen](/previous-versions//dd464660(v=vs.85)).
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>[<strong>WM_POINTERACTIVATE</strong>] (WM-pointeractivate.MD)<br/></td>
<td>Wird an ein inaktives Fenster gesendet, wenn ein primärer Zeiger eine [<strong>WM_POINTERDOWN</strong>] (WM-pointerdown.MD) über das Fenster generiert. Solange die Nachricht nicht behandelt wird, wird die übergeordnete Fenster Kette nach oben verschoben, bis Sie das Fenster der obersten Ebene erreicht. Anwendungen können auf diese Meldung reagieren, um anzugeben, ob Sie aktiviert werden sollen.<br/> Ein Fenster empfängt diese Meldung über seine [<strong>WindowProc</strong>] (/Previous-Versions/Windows/Desktop/Legacy/ms633573 (v = vs. 85))-Funktion. <br/></td>
</tr>
<tr class="odd">
<td>[<strong>WM_POINTERCAPTURECHANGED</strong>] (WM-pointercapturechanged.MD)<br/></td>
<td>Wird an ein Fenster gesendet, das die Erfassung eines Eingabe Zeigers verliert.<br/> Ein Fenster empfängt diese Meldung über seine [<strong>WindowProc</strong>] (/Previous-Versions/Windows/Desktop/Legacy/ms633573 (v = vs. 85))-Funktion.<br/></td>
</tr>
<tr class="even">
<td>[<strong>WM_POINTERDEVICECHANGE</strong>] (WM-pointerdevicechange.MD)<br/></td>
<td>Wird an ein Fenster gesendet, wenn eine Änderung in den Einstellungen eines Monitors vorliegt, dem ein Digitalisierer angefügt ist. Diese Meldung enthält Informationen zur Skalierung des Anzeigemodus. <br/></td>
</tr>
<tr class="odd">
<td>[<strong>WM_POINTERDEVICEINRANGE</strong>] (WM-pointerdeviceinrange.MD)<br/></td>
<td>Wird an ein Fenster gesendet, wenn ein Zeiger Gerät innerhalb des Bereichs eines eingabedigitalisierers erkannt wird. Diese Meldung enthält Informationen zum Gerät und seiner Nähe. <br/></td>
</tr>
<tr class="even">
<td>[<strong>WM_POINTERDEVICEOUTOFRANGE</strong>] (WM-pointerdeviceoutofrange.MD)<br/></td>
<td>Wird an ein Fenster gesendet, wenn ein Zeiger Gerät den Bereich eines eingabedigitalisierers verlassen hat. Diese Meldung enthält Informationen zum Gerät und seiner Nähe. <br/></td>
</tr>
<tr class="odd">
<td>[<strong>WM_POINTERDOWN</strong>] (WM-pointerdown.MD)<br/></td>
<td>Wird gepostet, wenn ein Zeiger über den Client Bereich eines Fensters kontaktiert wird. Diese Eingabe Nachricht bezieht sich auf das Fenster, über das der Zeiger Kontakt herstellt, und der Zeiger wird implizit im Fenster erfasst, sodass das Fenster weiterhin Eingaben für den Zeiger empfängt, bis der Kontakt unterbrochen wird. <br/> Ein Fenster empfängt diese Meldung über seine [<strong>WindowProc</strong>] (/Previous-Versions/Windows/Desktop/Legacy/ms633573 (v = vs. 85))-Funktion.<br/>
<blockquote>
[!Important]<br />
Desktop-Apps sollten dpi-fähig sein. Wenn Ihre APP nicht dpi-fähig ist, können Bildschirm Koordinaten, die in Zeiger Nachrichten und zugehörigen Strukturen enthalten sind, aufgrund der dpi-Virtualisierung ungenau erscheinen. Die dpi-Virtualisierung bietet Unterstützung für die automatische Skalierung für Anwendungen, die nicht mit dpi-Werten kompatibel sind und standardmäßig aktiv sind (Benutzer können Sie deaktivieren). Weitere Informationen finden Sie unter [Schreiben von High-dpi-Win32-Anwendungen](/previous-versions//dd464660(v=vs.85)).
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>[<strong>WM_POINTERENTER</strong>] (WM-pointerenter.MD)<br/></td>
<td>Wird an ein Fenster gesendet, wenn ein neuer Zeiger über das Fenster (Hover) in den Erkennungsbereich wechselt oder wenn ein vorhandener Zeiger innerhalb der Fenstergrenzen bewegt wird. <br/></td>
</tr>
<tr class="odd">
<td>[<strong>WM_POINTERLEAVE</strong>] (WM-pointerleave.MD)<br/></td>
<td>Wird an ein Fenster gesendet, wenn ein Zeiger den Erkennungsbereich über dem Fenster verlässt (Hover) oder wenn ein Zeiger außerhalb der Fenstergrenzen bewegt wird. <br/></td>
</tr>
<tr class="even">
<td>[<strong>WM_POINTERROUTEDAWAY</strong>] (WM-pointerroutedaway.MD)<br/></td>
<td>Tritt für den Prozess auf, der Eingaben empfängt, wenn die Zeiger Eingabe an einen anderen Prozess weitergeleitet wird.<br/></td>
</tr>
<tr class="odd">
<td>[<strong>WM_POINTERROUTEDRELEASED</strong>] (WM-pointerroutedreleased.MD)<br/></td>
<td>Wird an alle Prozesse gesendet (für die prozessübergreifende Verkettung durch [<strong>addcontentwithcrossprocesschaining</strong>] (/Windows/Win32/API/directmanipulation/NF-directmanipulation-idirectmanipulationcompositor2-addcontentwithcrossprocesschaining) und derzeit nicht für die Verarbeitung von Zeiger Eingaben), wenn eine [<strong>WM_POINTERUP</strong>] (WM-pointerup.MD)-Meldung für den aktuellen Prozess empfangen wird. <br/></td>
</tr>
<tr class="even">
<td>[<strong>WM_POINTERROUTEDTO</strong>] (WM-pointerroutedto.MD)<br/></td>
<td>Wird gesendet, wenn eine vorhandene Zeiger Eingabe für eine vorhandene Zeiger-ID von einem Prozess in einen anderen über den für prozessübergreifende Verkettung konfigurierten Inhalt übergeht ([<strong>addcontentwithcrossprocesschaining</strong>] (/Windows/Win32/API/directmanipulation/NF-directmanipulation-idirectmanipulationcompositor2-addcontentwithcrossprocesschaining)).<br/></td>
</tr>
<tr class="odd">
<td>[<strong>WM_POINTERUP</strong>] (WM-pointerup.MD)<br/></td>
<td>Wird gepostet, wenn ein Zeiger, der den Kontakt über den Client Bereich eines Fensters hergestellt hat, den Kontakt unterbricht. Diese Eingabe Nachricht bezieht sich auf das Fenster, über das der Zeiger Kontakt herstellt, und der Zeiger ist an diesem Punkt implizit im Fenster erfasst, sodass das Fenster weiterhin Eingabe Nachrichten empfängt, einschließlich der [<strong>WM_POINTERUP</strong>] (WM-pointerup.MD)-Benachrichtigung für den Zeiger, bis die Verbindung unterbrochen wird. <br/> Ein Fenster empfängt diese Meldung über seine [<strong>WindowProc</strong>] (/Previous-Versions/Windows/Desktop/Legacy/ms633573 (v = vs. 85))-Funktion. <br/>
<blockquote>
[!Important]<br />
Desktop-Apps sollten dpi-fähig sein. Wenn Ihre APP nicht dpi-fähig ist, können Bildschirm Koordinaten, die in Zeiger Nachrichten und zugehörigen Strukturen enthalten sind, aufgrund der dpi-Virtualisierung ungenau erscheinen. Die dpi-Virtualisierung bietet Unterstützung für die automatische Skalierung für Anwendungen, die nicht mit dpi-Werten kompatibel sind und standardmäßig aktiv sind (Benutzer können Sie deaktivieren). Weitere Informationen finden Sie unter [Schreiben von High-dpi-Win32-Anwendungen](/previous-versions//dd464660(v=vs.85)).
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>[<strong>WM_POINTERUPDATE</strong>] (WM-pointerupdate.MD)<br/></td>
<td>Wird bereitgestellt, um ein Update für einen Zeiger bereitzustellen, der den Kontakt über den Client Bereich eines Fensters hergestellt hat, oder auf einem nicht aufgezeichneten Zeiger, der auf den Client Bereich eines Fensters zeigt. Während der Mauszeiger bewegt wird, wird die Nachricht auf das Fenster ausgerichtet, über das sich der Zeiger befindet. Während sich der Mauszeiger auf der-Oberfläche befindet, wird der Zeiger implizit in dem Fenster erfasst, über das der Zeiger den Kontakt hergestellt hat, und dieses Fenster empfängt weiterhin Eingaben für den Zeiger, bis der Kontakt unterbrochen wird. <br/>
<blockquote>
[!Important]<br />
Desktop-Apps sollten dpi-fähig sein. Wenn Ihre APP nicht dpi-fähig ist, können Bildschirm Koordinaten, die in Zeiger Nachrichten und zugehörigen Strukturen enthalten sind, aufgrund der dpi-Virtualisierung ungenau erscheinen. Die dpi-Virtualisierung bietet Unterstützung für die automatische Skalierung für Anwendungen, die nicht mit dpi-Werten kompatibel sind und standardmäßig aktiv sind (Benutzer können Sie deaktivieren). Weitere Informationen finden Sie unter [Schreiben von High-dpi-Win32-Anwendungen](/previous-versions//dd464660(v=vs.85)).
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>[<strong>WM_POINTERWHEEL</strong>] (WM-pointerwheel.MD)<br/></td>
<td>Wird im Fenster mit dem Vordergrund Tastaturfokus gesendet, wenn ein Mausrad gedreht wird. <br/> Ein Fenster empfängt diese Meldung über seine [<strong>WindowProc</strong>] (/Previous-Versions/Windows/Desktop/Legacy/ms633573 (v = vs. 85))-Funktion.<br/>
<blockquote>
[!Important]<br />
Desktop-Apps sollten dpi-fähig sein. Wenn Ihre APP nicht dpi-fähig ist, können Bildschirm Koordinaten, die in Zeiger Nachrichten und zugehörigen Strukturen enthalten sind, aufgrund der dpi-Virtualisierung ungenau erscheinen. Die dpi-Virtualisierung bietet Unterstützung für die automatische Skalierung für Anwendungen, die nicht mit dpi-Werten kompatibel sind und standardmäßig aktiv sind (Benutzer können Sie deaktivieren). Weitere Informationen finden Sie unter [Schreiben von High-dpi-Win32-Anwendungen](/previous-versions//dd464660(v=vs.85)).
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>[<strong>WM_POINTERHWHEEL</strong>] (WM-pointerhwheel.MD)<br/></td>
<td>Wird im Fenster mit dem Vordergrund Tastaturfokus gesendet, wenn ein horizontales Mausrad gedreht wird. <br/> Ein Fenster empfängt diese Meldung über seine [<strong>WindowProc</strong>] (/Previous-Versions/Windows/Desktop/Legacy/ms633573 (v = vs. 85))-Funktion.<br/>
<blockquote>
[!Important]<br />
Desktop-Apps sollten dpi-fähig sein. Wenn Ihre APP nicht dpi-fähig ist, können Bildschirm Koordinaten, die in Zeiger Nachrichten und zugehörigen Strukturen enthalten sind, aufgrund der dpi-Virtualisierung ungenau erscheinen. Die dpi-Virtualisierung bietet Unterstützung für die automatische Skalierung für Anwendungen, die nicht mit dpi-Werten kompatibel sind und standardmäßig aktiv sind (Benutzer können Sie deaktivieren). Weitere Informationen finden Sie unter [Schreiben von High-dpi-Win32-Anwendungen](/previous-versions//dd464660(v=vs.85)).
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>[<strong>WM_TOUCHHITTESTING</strong>] (WM-touchhittesting.MD)<br/></td>
<td>Wird an ein Fenster in einem Touchscreen gesendet, um das wahrscheinlichste Berührungs Ziel zu ermitteln. <br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verweis auf Zeiger-Eingabe Nachricht](wmpointer-reference.md)
</dt> </dl>

 

