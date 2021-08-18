---
title: Meldungen
description: Die Themen in diesem Abschnitt enthalten die Referenzspezifikationen für bestimmte Zeigereingabenachrichten und Benachrichtigungen.
ms.assetid: 65F4DCD0-DAE1-4AC2-AB36-23D114803138
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 076ba9d8b33bf2848d6088c4bac42b60ce9e19646abe5163358f25b063250b9e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118756952"
---
# <a name="messages"></a>Meldungen

Die Themen in diesem Abschnitt enthalten die Referenzspezifikationen für bestimmte [Zeigereingabenachrichten und Benachrichtigungen.](messages-and-notifications-portal.md)

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
<td>[<strong>DM_POINTERHITTEST</strong>] (dm-pointerhittest.md)<br/></td>
<td>Wird an ein Fenster gesendet, wenn die Zeigereingabe zum ersten Mal erkannt wird, um das wahrscheinlichste Eingabeziel für die direkte [Bearbeitung zu bestimmen.](/previous-versions/windows/desktop/directmanipulation/direct-manipulation-portal) <br/></td>
</tr>
<tr class="even">
<td>[<strong>WM_NCPOINTERDOWN</strong>] (wm-ncpointerdown.md)<br/></td>
<td>Wird gepostet, wenn ein Zeiger den Kontakt über den nicht clientseitigen Bereich eines Fensters vor stellt. Die Nachricht ist auf das Fenster festgelegt, über das der Zeiger kontakt mit ihr kontaktt. Der Zeiger wird implizit auf das Fenster erfasst, sodass das Fenster weiterhin Eingaben für den Zeiger erhält, bis er den Kontakt unterbricht. <br/> Wenn ein Fenster diesen Zeiger erfasst hat, wird diese Meldung nicht gesendet. Stattdessen wird ein [<strong>WM_POINTERDOWN</strong>](wm-pointerdown.md) an das Fenster gesendet, das diesen Zeiger erfasst hat. <br/>
<blockquote>
[!Important]<br />
Desktop-Apps sollten DPI-bewusst sein. Wenn Ihre App keine DPI-Unterstützung hat, können Bildschirmkoordinaten, die in Zeigermeldungen und verwandten Strukturen enthalten sind, aufgrund der DPI-Virtualisierung ungenau erscheinen. Die DPI-Virtualisierung bietet Unterstützung für die automatische Skalierung für Anwendungen, die nicht DPI-bewusst sind und standardmäßig aktiv sind (Benutzer können sie deaktivieren). Weitere Informationen finden Sie unter [Writing High-DPI Win32 Applications ( Schreiben von Win32-Anwendungen mit hohem DPI-Code).](/previous-versions//dd464660(v=vs.85))
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>[<strong>WM_NCPOINTERUP</strong>] (wm-ncpointerup.md)<br/></td>
<td>Wird veröffentlicht, wenn ein Zeiger, der den Kontakt über den Nicht-Clientbereich eines Fensters hergestellt hat, den Kontakt unterbricht. Die Nachricht zielt auf das Fenster ab, über das der Zeiger kontaktiert, und der Zeiger wird an diesem Punkt implizit im Fenster erfasst, sodass das Fenster weiterhin Eingaben für den Zeiger erhält, bis er den Kontakt unterbricht, einschließlich der Benachrichtigung [<strong>WM_NCPOINTERUP</strong>](wm-ncpointerup.md). <br/> Wenn ein Fenster diesen Zeiger erfasst hat, wird diese Meldung nicht gesendet. Stattdessen wird ein [<strong>WM_POINTERUP</strong>](wm-pointerup.md) an das Fenster gesendet, das diesen Zeiger erfasst hat. <br/>
<blockquote>
[!Important]<br />
Desktop-Apps sollten DPI-bewusst sein. Wenn Ihre App keine DPI-Unterstützung hat, können Bildschirmkoordinaten, die in Zeigermeldungen und verwandten Strukturen enthalten sind, aufgrund der DPI-Virtualisierung ungenau erscheinen. Die DPI-Virtualisierung bietet Unterstützung für die automatische Skalierung für Anwendungen, die nicht DPI-bewusst sind und standardmäßig aktiv sind (Benutzer können sie deaktivieren). Weitere Informationen finden Sie unter [Writing High-DPI Win32 Applications ( Schreiben von Win32-Anwendungen mit hohem DPI-Code).](/previous-versions//dd464660(v=vs.85))
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>[<strong>WM_NCPOINTERUPDATE</strong>] (wm-ncpointerupdate.md)<br/></td>
<td>Veröffentlicht, um ein Update für einen Zeiger zur Verfügung zu stellen, der den Kontakt über den Nicht-Clientbereich eines Fensters hergestellt hat, oder wenn ein nicht gekapselter Kontakt mit dem Zeigen auf den Nicht-Clientbereich eines Fensters bewegt wird. Während der Zeiger darauf zeigt, richtet sich die Nachricht an das Fenster, über dem sich der Zeiger befindet. Während der Zeiger mit der Oberfläche in Kontakt ist, wird der Zeiger implizit auf das Fenster erfasst, über das der Zeiger kontaktiert wurde, und dieses Fenster erhält weiterhin Eingaben für den Zeiger, bis er den Kontakt unterbricht. <br/> Wenn ein Fenster diesen Zeiger erfasst hat, wird diese Meldung nicht gesendet. Stattdessen wird ein [<strong>WM_POINTERUPDATE</strong>](wm-pointerupdate.md) an das Fenster gesendet, das diesen Zeiger erfasst hat.<br/>
<blockquote>
[!Important]<br />
Desktop-Apps sollten DPI-bewusst sein. Wenn Ihre App keine DPI-Unterstützung hat, können Bildschirmkoordinaten, die in Zeigermeldungen und verwandten Strukturen enthalten sind, aufgrund der DPI-Virtualisierung ungenau erscheinen. Die DPI-Virtualisierung bietet Unterstützung für die automatische Skalierung für Anwendungen, die nicht DPI-bewusst sind und standardmäßig aktiv sind (Benutzer können sie deaktivieren). Weitere Informationen finden Sie unter [Writing High-DPI Win32 Applications ( Schreiben von Win32-Anwendungen mit hohem DPI-Code).](/previous-versions//dd464660(v=vs.85))
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>[<strong>WM_PARENTNOTIFY</strong>] (wm-parentnotify.md)<br/></td>
<td>Wird an ein Fenster gesendet, wenn eine wichtige Aktion in einem Nachfolgerfenster auftritt. Diese Meldung wurde nun erweitert, um das Ereignis [<strong>WM_POINTERDOWN</strong>](wm-pointerdown.md) ein. Wenn das untergeordnete Fenster erstellt wird, Das System sendet [<strong>WM_PARENTNOTIFY</strong>](/previous-versions/windows/desktop/inputmsg/wm-parentnotify) direkt vor der<strong>[CreateWindow</strong>](/windows/win32/api/winuser/nf-winuser-createwindowa) oder [<strong>CreateWindowEx</strong>](/windows/win32/api/winuser/nf-winuser-createwindowexa), die die Fensterrückgaben erstellt. Wenn das untergeordnete Fenster zerstört wird, sendet das System die Nachricht, bevor eine Verarbeitung zum Zerstören des Fensters stattfindet.<br/> Ein Fenster empfängt diese Meldung über die<strong>[WindowProc</strong>](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)))-Funktion. <br/>
<blockquote>
[!Important]<br />
Desktop-Apps sollten DPI-bewusst sein. Wenn Ihre App keine DPI-Unterstützung hat, können Bildschirmkoordinaten, die in Zeigermeldungen und verwandten Strukturen enthalten sind, aufgrund der DPI-Virtualisierung ungenau erscheinen. Die DPI-Virtualisierung bietet Unterstützung für die automatische Skalierung für Anwendungen, die nicht DPI-bewusst sind und standardmäßig aktiv sind (Benutzer können sie deaktivieren). Weitere Informationen finden Sie unter [Writing High-DPI Win32 Applications ( Schreiben von Win32-Anwendungen mit hohem DPI-Code).](/previous-versions//dd464660(v=vs.85))
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>[<strong>WM_POINTERACTIVATE</strong>] (wm-pointeractivate.md)<br/></td>
<td>Wird an ein inaktives Fenster gesendet, wenn ein primärer Zeiger eine<strong>[WM_POINTERDOWN</strong>](wm-pointerdown.md) über das Fenster generiert. Solange die Nachricht nicht behandelt wird, wird die übergeordnete Fensterkette nach oben geworfen, bis sie das Fenster der obersten Ebene erreicht. Anwendungen können auf diese Meldung antworten, um anzugeben, ob sie aktiviert werden möchten.<br/> Ein Fenster empfängt diese Meldung über die<strong>[WindowProc</strong>](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)))-Funktion. <br/></td>
</tr>
<tr class="odd">
<td>[<strong>WM_POINTERCAPTURECHANGED</strong>] (wm-pointercapturechanged.md)<br/></td>
<td>Wird an ein Fenster gesendet, das die Erfassung eines Eingabezeigers verliert.<br/> Ein Fenster empfängt diese Meldung über die<strong>[WindowProc</strong>](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)))-Funktion.<br/></td>
</tr>
<tr class="even">
<td>[<strong>WM_POINTERDEVICECHANGE</strong>] (wm-pointerdevicechange.md)<br/></td>
<td>Wird an ein Fenster gesendet, wenn sich die Einstellungen eines Monitors ändern, an den ein Digitizer angefügt ist. Diese Meldung enthält Informationen zur Skalierung des Anzeigemodus. <br/></td>
</tr>
<tr class="odd">
<td>[<strong>WM_POINTERDEVICEINRANGE</strong>] (wm-pointerdeviceinrange.md)<br/></td>
<td>Wird an ein Fenster gesendet, wenn ein Zeigergerät innerhalb des Bereichs eines Eingabededisierers erkannt wird. Diese Meldung enthält Informationen zum Gerät und seiner Nähe. <br/></td>
</tr>
<tr class="even">
<td>[<strong>WM_POINTERDEVICEOUTOFRANGE</strong>] (wm-pointerdeviceoutofrange.md)<br/></td>
<td>Wird an ein Fenster gesendet, wenn ein Zeigergerät den Bereich eines Eingabededisierers entfernt hat. Diese Meldung enthält Informationen zum Gerät und seiner Nähe. <br/></td>
</tr>
<tr class="odd">
<td>[<strong>WM_POINTERDOWN</strong>] (wm-pointerdown.md)<br/></td>
<td>Wird gepostet, wenn ein Zeiger über den Clientbereich eines Fensters kontaktiert. Diese Eingabenachricht zielt auf das Fenster ab, über das der Zeiger kontaktiert, und der Zeiger wird implizit auf das Fenster erfasst, sodass das Fenster weiterhin Eingaben für den Zeiger erhält, bis er den Kontakt unterbricht. <br/> Ein Fenster empfängt diese Meldung über die<strong>[WindowProc</strong>](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)))-Funktion.<br/>
<blockquote>
[!Important]<br />
Desktop-Apps sollten DPI-bewusst sein. Wenn Ihre App keine DPI-Unterstützung hat, können Bildschirmkoordinaten, die in Zeigermeldungen und verwandten Strukturen enthalten sind, aufgrund der DPI-Virtualisierung ungenau erscheinen. Die DPI-Virtualisierung bietet Unterstützung für die automatische Skalierung für Anwendungen, die nicht DPI-bewusst sind und standardmäßig aktiv sind (Benutzer können sie deaktivieren). Weitere Informationen finden Sie unter [Writing High-DPI Win32 Applications ( Schreiben von Win32-Anwendungen mit hohem DPI-Code).](/previous-versions//dd464660(v=vs.85))
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>[<strong>WM_POINTERENTER</strong>] (wm-pointerenter.md)<br/></td>
<td>Wird an ein Fenster gesendet, wenn ein neuer Zeiger in den Erkennungsbereich über dem Fenster wechselt (mit dem Zeigen darauf), oder wenn ein vorhandener Zeiger innerhalb der Fenstergrenzen bewegt wird. <br/></td>
</tr>
<tr class="odd">
<td>[<strong>WM_POINTERLEAVE</strong>] (wm-pointerleave.md)<br/></td>
<td>Wird an ein Fenster gesendet, wenn ein Zeiger den Erkennungsbereich über dem Fenster verlässt (mit dem Zeigen darauf), oder wenn ein Zeiger außerhalb der Fenstergrenzen bewegt wird. <br/></td>
</tr>
<tr class="even">
<td>[<strong>WM_POINTERROUTEDAWAY</strong>] (wm-pointerroutedaway.md)<br/></td>
<td>Tritt auf dem Prozess ein, der Eingaben empfängt, wenn die Zeigereingabe an einen anderen Prozess geroutet wird.<br/></td>
</tr>
<tr class="odd">
<td>[<strong>WM_POINTERROUTEDRELEASED</strong>] (wm-pointerroutedreleased.md)<br/></td>
<td>Wird an alle Prozesse gesendet (konfiguriert für prozessübergreifende Verkettung über [<strong>AddContentWithCrossProcessChaining</strong>](/windows/win32/api/directmanipulation/nf-directmanipulation-idirectmanipulationcompositor2-addcontentwithcrossprocesschaining) und verarbeitet derzeit keine Zeigereingaben), die jemals einer bestimmten Zeiger-ID zugeordnet sind, wenn eine [<strong>WM_POINTERUP</strong>](wm-pointerup.md)-Nachricht für den aktuellen Prozess empfangen wird. <br/></td>
</tr>
<tr class="even">
<td>[<strong>WM_POINTERROUTEDTO</strong>] (wm-pointerroutedto.md)<br/></td>
<td>Wird bei laufender Zeigereingabe für eine vorhandene Zeiger-ID zwischen den für prozessübergreifende Verkettung konfigurierten Inhalten ([<strong>AddContentWithCrossProcessChaining</strong>](/windows/win32/api/directmanipulation/nf-directmanipulation-idirectmanipulationcompositor2-addcontentwithcrossprocesschaining)) gesendet.<br/></td>
</tr>
<tr class="odd">
<td>[<strong>WM_POINTERUP</strong>] (wm-pointerup.md)<br/></td>
<td>Wird veröffentlicht, wenn ein Zeiger, der den Kontakt über den Clientbereich eines Fensters hergestellt hat, den Kontakt unterbricht. Diese Eingabenachricht zielt auf das Fenster ab, über das der Zeiger kontaktiert, und der Zeiger wird an diesem Punkt implizit im Fenster erfasst, sodass das Fenster weiterhin Eingabemeldungen einschließlich der Benachrichtigung [<strong>WM_POINTERUP</strong>](wm-pointerup.md) für den Zeiger erhält, bis er den Kontakt unterbricht. <br/> Ein Fenster empfängt diese Meldung über die<strong>[WindowProc</strong>](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)))-Funktion. <br/>
<blockquote>
[!Important]<br />
Desktop-Apps sollten DPI-bewusst sein. Wenn Ihre App keine DPI-Unterstützung hat, können Bildschirmkoordinaten, die in Zeigermeldungen und verwandten Strukturen enthalten sind, aufgrund der DPI-Virtualisierung ungenau erscheinen. Die DPI-Virtualisierung bietet Unterstützung für die automatische Skalierung für Anwendungen, die nicht DPI-bewusst sind und standardmäßig aktiv sind (Benutzer können sie deaktivieren). Weitere Informationen finden Sie unter [Writing High-DPI Win32 Applications ( Schreiben von Win32-Anwendungen mit hohem DPI-Code).](/previous-versions//dd464660(v=vs.85))
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>[<strong>WM_POINTERUPDATE</strong>] (wm-pointerupdate.md)<br/></td>
<td>Veröffentlicht, um ein Update für einen Zeiger zur Verfügung zu stellen, der den Kontakt über den Clientbereich eines Fensters hergestellt hat, oder auf einen nicht gekapselten Zeiger, der auf den Clientbereich eines Fensters zeigt. Während der Zeiger darauf zeigt, richtet sich die Nachricht an das Fenster, über dem sich der Zeiger befindet. Während der Zeiger mit der Oberfläche in Kontakt ist, wird der Zeiger implizit auf das Fenster erfasst, über das der Zeiger kontaktiert wurde, und dieses Fenster erhält weiterhin Eingaben für den Zeiger, bis er den Kontakt unterbricht. <br/>
<blockquote>
[!Important]<br />
Desktop-Apps sollten DPI-bewusst sein. Wenn Ihre App keine DPI-Unterstützung hat, können Bildschirmkoordinaten, die in Zeigermeldungen und verwandten Strukturen enthalten sind, aufgrund der DPI-Virtualisierung ungenau erscheinen. Die DPI-Virtualisierung bietet Unterstützung für die automatische Skalierung für Anwendungen, die nicht DPI-bewusst sind und standardmäßig aktiv sind (Benutzer können sie deaktivieren). Weitere Informationen finden Sie unter [Writing High-DPI Win32 Applications ( Schreiben von Win32-Anwendungen mit hohem DPI-Code).](/previous-versions//dd464660(v=vs.85))
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>[<strong>WM_POINTERWHEEL</strong>] (wm-pointerwheel.md)<br/></td>
<td>Wird an das Fenster mit Vordergrundtastenfokus gesendet, wenn ein Scrollrad gedreht wird. <br/> Ein Fenster empfängt diese Meldung über die Funktion<strong>[WindowProc</strong>](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)).<br/>
<blockquote>
[!Important]<br />
Desktop-Apps sollten DPI-fähige Apps sein. Wenn Ihre App nicht DPI-bewusst ist, können Bildschirmkoordinaten, die in Zeigermeldungen und zugehörigen Strukturen enthalten sind, aufgrund der DPI-Virtualisierung ungenau erscheinen. Die DPI-Virtualisierung bietet Unterstützung für die automatische Skalierung für Anwendungen, die nicht DPI-bewusst sind und standardmäßig aktiv sind (Benutzer können sie deaktivieren). Weitere Informationen finden Sie unter [Schreiben von Win32-Anwendungen mit hohem DPI-Anteil.](/previous-versions//dd464660(v=vs.85))
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>[<strong>WM_POINTERHWHEEL</strong>] (wm-pointerhwheel.md)<br/></td>
<td>Wird an das Fenster mit Vordergrundtastenfokus gesendet, wenn ein horizontales Scrollrad gedreht wird. <br/> Ein Fenster empfängt diese Meldung über die Funktion<strong>[WindowProc</strong>](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)).<br/>
<blockquote>
[!Important]<br />
Desktop-Apps sollten DPI-fähige Apps sein. Wenn Ihre App nicht DPI-bewusst ist, können Bildschirmkoordinaten, die in Zeigermeldungen und zugehörigen Strukturen enthalten sind, aufgrund der DPI-Virtualisierung ungenau erscheinen. Die DPI-Virtualisierung bietet Unterstützung für die automatische Skalierung für Anwendungen, die nicht DPI-bewusst sind und standardmäßig aktiv sind (Benutzer können sie deaktivieren). Weitere Informationen finden Sie unter [Schreiben von Win32-Anwendungen mit hohem DPI-Anteil.](/previous-versions//dd464660(v=vs.85))
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>[<strong>WM_TOUCHHITTESTING</strong>] (wm-touchhittesting.md)<br/></td>
<td>Wird in einem Touch-Down an ein Fenster gesendet, um das wahrscheinlichste Touchziel zu ermitteln. <br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zeigereingabe-Meldungsverweis](wmpointer-reference.md)
</dt> </dl>

 

