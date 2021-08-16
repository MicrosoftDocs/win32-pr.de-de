---
title: DWM-Funktionen
description: Dieser Abschnitt enthält Informationen zu den DWM-Funktionen (Desktopfenster-Manager).
ms.assetid: 525807fe-c5d7-4997-87b9-a14d02c33cc3
keywords:
- Desktopfenster-Manager (DWM),Referenz
- DWM (Desktopfenster-Manager),Referenz
- Desktopfenster-Manager (DWM), Funktionen
- DWM (Desktopfenster-Manager),Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe8c1db28571fde16cf0fe0f9068f5bd650d31f637776c7bcc00717ab3043997
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118503305"
---
# <a name="dwm-functions"></a>DWM-Funktionen

Dieser Abschnitt enthält Informationen zu den DWM-Funktionen (Desktopfenster-Manager).

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
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmattachmilcontent"><strong>DwmAttachMilContent</strong></a><br/></td>
<td>Diese Funktion ist nicht implementiert.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc"><strong>DwmDefWindowProc</strong></a><br/></td>
<td>Standardfensterprozedur für DWM-Treffertests im Nicht-Clientbereich.<br/> Sie müssen auch sicherstellen, dass <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc"><strong>DwmDefWindowProc</strong></a> für die <a href="/windows/desktop/inputdev/wm-ncmouseleave"><strong>WM_NCMOUSELEAVE</strong></a> Meldung aufgerufen wird. Wenn <strong>DwmDefWindowProc</strong> nicht für die <strong>WM_NCMOUSELEAVE</strong> Meldung aufgerufen wird, entfernt DWM die Hervorhebung nicht aus den Schaltflächen <strong>Maximieren,</strong> <strong>Minimieren</strong>und <strong>Schließen,</strong> wenn der Cursor das Fenster verlässt.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdetachmilcontent"><strong>DwmDetachMilContent</strong></a><br/></td>
<td>Diese Funktion ist nicht implementiert.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenableblurbehindwindow"><strong>DwmEnableBlurBehindWindow</strong></a><br/></td>
<td>Aktiviert den Weichzeichnereffekt für ein angegebenes Fenster.<br/></td>
<b>Hinweis</b> Ab Windows 8 führt das Aufrufen dieser Funktion nicht zu einem Weichzeichnereffekt, da die Art und Weise geändert wird, wie Fenster gerendert werden.
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablecomposition"><strong>DwmEnableComposition</strong></a><br/></td>
<td>Aktiviert oder deaktiviert die DWM-Komposition. <br/>
<blockquote>
[!Note]<br />
Diese Funktion ist ab Windows 8 veraltet. DWM kann nicht mehr programmgesteuert deaktiviert werden.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablemmcss"><strong>DwmEnableMMCSS</strong></a><br/></td>
<td>Benachrichtigt den DWM, die MMCSS-Zeitplanung (Multimedia Class Schedule Service) zu verwenden oder zu deaktivieren, während der aufrufende Prozess aktiv ist.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea"><strong>DwmExtendFrameIntoClientArea</strong></a><br/></td>
<td>Erweitert den Fensterrahmen in den Clientbereich.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmflush"><strong>DwmFlush</strong></a><br/></td>
<td>Gibt einen Leerungsaufruf aus, der den Aufrufer bis zum nächsten Zeitpunkt blockiert, wenn alle derzeit ausstehenden Microsoft DirectX-Oberflächenupdates vorgenommen wurden. Dies kompensiert sehr komplexe Szenen oder Aufrufen von Prozessen mit sehr niedriger Priorität.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcolorizationcolor"><strong>DwmGetColorizationColor</strong></a><br/></td>
<td>Ruft die aktuelle Farbe ab, die für die DWM-Brillenkomposition verwendet wird. Dieser Wert basiert auf dem aktuellen Farbschema und kann vom Benutzer geändert werden. Anwendungen können auf Farbänderungen <a href="wm-dwmcolorizationcolorchanged.md"><strong></strong></a> lauschen, indem sie die WM_DWMCOLORIZATIONCOLORCHANGED-Benachrichtigung behandeln.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcompositiontiminginfo"><strong>DwmGetCompositionTimingInfo</strong></a><br/></td>
<td>Ruft die aktuellen Kompositions-Zeitsteuerungsinformationen für ein angegebenes Fenster ab.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetgraphicsstreamclient"><strong>DwmGetGraphicsStreamClient</strong></a><br/></td>
<td>Diese Funktion ist nicht implementiert.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetgraphicsstreamtransformhint"><strong>DwmGetGraphicsStreamTransformHint</strong></a><br/></td>
<td>Diese Funktion ist nicht implementiert.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgettransportattributes"><strong>DwmGetTransportAttributes</strong></a><br/></td>
<td>Ruft Transportattribute ab.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetunmettabrequirements"><strong>DwmGetUnmetTabRequirements</strong></a><br/></td>
<td><blockquote>
<strong>Hinweis</strong>  Diese Funktion ist öffentlich verfügbar, aber nicht funktionsfrei für Windows 10 Version 1803.
</blockquote>
Überprüft die Anforderungen, die zum Abrufen von Registerkarten in der Titelleiste der Anwendung für das angegebene Fenster erforderlich sind.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetwindowattribute"><strong>DwmGetWindowAttribute</strong></a><br/></td>
<td>Ruft den aktuellen Wert eines angegebenen Attributs ab, das auf ein Fenster angewendet wird.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwminvalidateiconicbitmaps"><strong>DwmInvalidateIconicBitmaps</strong></a><br/></td>
<td>Wird von einer Anwendung aufgerufen, um anzugeben, dass alle zuvor bereitgestellten miniaturen Bitmaps aus einem Fenster , sowohl Miniaturansichten als auch Peekdarstellungen, aktualisiert werden sollen.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmiscompositionenabled"><strong>DwmIsCompositionEnabled</strong></a><br/></td>
<td>Ruft einen Wert ab, der angibt, ob die DWM-Komposition aktiviert ist. Anwendungen auf Computern, auf denen Windows 7 oder früher ausgeführt wird, können auf Änderungen des Kompositionszustands lauschen, indem <a href="wm-dwmcompositionchanged.md"><strong>sie</strong></a> die WM_DWMCOMPOSITIONCHANGED-Benachrichtigung verarbeiten.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmmodifypreviousdxframeduration"><strong>DwmModifyPreviousDxFrameDuration</strong></a><br/></td>
<td>Ändert die Anzahl der Monitoraktualisierungen, über die der vorherige Frame angezeigt wird. <br/> <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmmodifypreviousdxframeduration"><strong>DwmModifyPreviousDxFrameDuration</strong></a> wird nicht mehr unterstützt. Ab Windows 8.1 geben Aufrufe von <strong>DwmModifyPreviousDxFrameDuration</strong> immer E_NOTIMPL zurück.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmquerythumbnailsourcesize"><strong>DwmQueryThumbnailSourceSize</strong></a><br/></td>
<td>Ruft die Quellgröße der DWM-Miniaturansicht ab.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmregisterthumbnail"><strong>DwmRegisterThumbnail</strong></a><br/></td>
<td>Erstellt eine DWM-Miniaturansichtsbeziehung zwischen dem Ziel- und dem Quellfenster.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmrendergesture"><strong>DwmRenderGesture</strong></a><br/></td>
<td>Benachrichtigt DWM, dass ein Berührungskontakt als Geste erkannt wurde und dwm Feedback für diese Geste ziehen sollte.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetdxframeduration"><strong>DwmSetDxFrameDuration</strong></a><br/></td>
<td>Legt die Anzahl der Monitoraktualisierungen fest, über die der dargestellte Frame angezeigt werden soll. <br/> <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetdxframeduration"><strong>DwmSetDxFrameDuration</strong></a> wird nicht mehr unterstützt. Ab Windows 8.1 geben Aufrufe von <strong>DwmSetDxFrameDuration</strong> immer E_NOTIMPL zurück.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap"><strong>DwmSetIconicLivePreviewBitmap</strong></a><br/></td>
<td>Legt eine statische, unerkannte Bitmap fest, um eine <em>Livevorschau</em> (auch als <em>Vorschauvorschau</em>bezeichnet) eines Fensters oder einer Registerkarte anzuzeigen. Die Taskleiste kann diese Bitmap verwenden, um eine Vorschau eines Fensters oder einer Registerkarte in voller Größe anzuzeigen.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticonicthumbnail"><strong>DwmSetIconicThumbnail</strong></a><br/></td>
<td>Legt eine statische, unerbittliche Bitmap für ein Fenster oder eine Registerkarte fest, die als Miniaturansichtsdarstellung verwendet werden soll. Die Taskleiste kann diese Bitmap als Miniaturansichtsoptionsziel für das Fenster oder die Registerkarte verwenden.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters"><strong>DwmSetPresentParameters</strong></a><br/></td>
<td>Legt die aktuellen Parameter für die Framekomposition fest. <br/> <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters"><strong>DwmSetPresentParameters</strong></a> wird nicht mehr unterstützt. Ab Windows 8.1 geben Aufrufe von <strong>DwmSetPresentParameters</strong> immer E_NOTIMPL zurück.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute"><strong>DwmSetWindowAttribute</strong></a><br/></td>
<td>Legt den Wert von Nicht-Clientrenderingattributen für ein Fenster fest.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/dwmapi/nf-dwmapi-dwmshowcontact"><strong>DwmShowContact</strong></a><br/></td>
<td>Wird von einer App oder einem Framework aufgerufen, um den visuellen Feedbacktyp anzugeben, der als Reaktion auf einen bestimmten Berührungs- oder Stiftkontakt gezeichnet werden soll.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmtethercontact"><strong>DwmTetherContact</strong></a><br/></td>
<td>Ermöglicht das grafische Feedback von Touch- und Drag-Interaktionen an den Benutzer.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/dwmapi/nf-dwmapi-dwmtransitionownedwindow"><strong>DwmTransitionOwnedWindow</strong></a><br/></td>
<td>Koordiniert die Animationen von Toolfenstern mit dem DWM.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmunregisterthumbnail"><strong>DwmUnregisterThumbnail</strong></a><br/></td>
<td>Entfernt eine DWM-Miniaturansichtsbeziehung, die von der <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmregisterthumbnail"><strong>DwmRegisterThumbnail-Funktion</strong></a> erstellt wurde.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmupdatethumbnailproperties"><strong>DwmUpdateThumbnailProperties</strong></a><br/></td>
<td>Aktualisiert die Eigenschaften für eine DWM-Miniaturansicht.<br/></td>
</tr>
</tbody>
</table>



 

 

