---
title: DWM-Funktionen
description: Dieser Abschnitt enthält Informationen zu den Desktopfenster-Manager (DWM)-Funktionen.
ms.assetid: 525807fe-c5d7-4997-87b9-a14d02c33cc3
keywords:
- Desktopfenster-Manager (DWM), Referenz
- Dwm (Desktopfenster-Manager), Referenz
- Desktopfenster-Manager (DWM), Funktionen
- Dwm (Desktopfenster-Manager), Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 067f836e7fa8b5b84be02a402a3e0b3d0f78d1c1
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/08/2020
ms.locfileid: "104316604"
---
# <a name="dwm-functions"></a>DWM-Funktionen

Dieser Abschnitt enthält Informationen zu den Desktopfenster-Manager (DWM)-Funktionen.

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
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmattachmilcontent"><strong>Dwmattachmilcontent</strong></a><br/></td>
<td>Diese Funktion ist nicht implementiert.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc"><strong>DwmDefWindowProc</strong></a><br/></td>
<td>Standardfenster Prozedur für den DWM-Treffer Test innerhalb des nicht-Client Bereichs.<br/> Außerdem müssen Sie sicherstellen, dass <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc"><strong>DwmDefWindowProc</strong></a> für die <a href="/windows/desktop/inputdev/wm-ncmouseleave"><strong>WM_NCMOUSELEAVE</strong></a> Nachricht aufgerufen wird. Wenn <strong>DwmDefWindowProc</strong> nicht für die <strong>WM_NCMOUSELEAVE</strong> Nachricht aufgerufen wird, entfernt DWM die Hervorhebung nicht aus den Schaltflächen <strong>maximieren</strong>, <strong>minimieren</strong>und <strong>Schließen</strong> , wenn der Cursor das Fenster verlässt.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdetachmilcontent"><strong>Dwmdetachmilcontent</strong></a><br/></td>
<td>Diese Funktion ist nicht implementiert.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenableblurbehindwindow"><strong>Dwmenableblurabledwindow</strong></a><br/></td>
<td>Aktiviert den Weichzeichnereffekt in einem angegebenen Fenster.<br/></td>
<b>Hinweis</b> Beginnend mit Windows 8 führt das Aufrufen dieser Funktion nicht zu einem Weichzeichnereffekt aufgrund einer Stiländerung in der Art und Weise, in der Fenster gerendert werden.
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablecomposition"><strong>DwmEnableComposition</strong></a><br/></td>
<td>Aktiviert oder deaktiviert die DWM-Komposition. <br/>
<blockquote>
[!Note]<br />
Diese Funktion ist ab Windows 8 veraltet. DWM kann nicht mehr Programm gesteuert deaktiviert werden.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablemmcss"><strong>Dwmenablemmcss</strong></a><br/></td>
<td>Benachrichtigt den DWM, dass die MMCSS-Zeitplanung (Multimedia Class Schedule Service) deaktiviert wird, während der Aufrufprozess aktiv ist.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea"><strong>DwmExtendFrameIntoClientArea</strong></a><br/></td>
<td>Erweitert den Fensterrahmen in den Client Bereich.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmflush"><strong>Dwmflush</strong></a><br/></td>
<td>Gibt einen Flush-Aufruf aus, der den Aufrufer bis zum nächsten vorhanden ist, wenn alle aktuell ausstehenden Microsoft DirectX Surface-Aktualisierungen vorgenommen wurden. Dies kompensiert sehr komplexe Szenen oder Aufruf Prozesse mit sehr niedriger Priorität.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcolorizationcolor"><strong>DwmGetColorizationColor</strong></a><br/></td>
<td>Ruft die für die DWM-Glaskomposition verwendete aktuelle Farbe ab. Dieser Wert basiert auf dem aktuellen Farbschema und kann vom Benutzer geändert werden. Anwendungen können Farbänderungen überwachen, indem Sie die <a href="wm-dwmcolorizationcolorchanged.md"><strong>WM_DWMCOLORIZATIONCOLORCHANGED</strong></a> Benachrichtigung verarbeiten.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcompositiontiminginfo"><strong>Dwmgetcompositiontiminginfo</strong></a><br/></td>
<td>Ruft die aktuellen Informationen zur Kompositions Zeit für ein angegebenes Fenster ab.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetgraphicsstreamclient"><strong>Dwmgetgraphicsstreamclient</strong></a><br/></td>
<td>Diese Funktion ist nicht implementiert.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetgraphicsstreamtransformhint"><strong>Dwmgetgraphicsstreamtransformhint</strong></a><br/></td>
<td>Diese Funktion ist nicht implementiert.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgettransportattributes"><strong>Dwmgettransportattributes</strong></a><br/></td>
<td>Ruft Transport Attribute ab.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetunmettabrequirements"><strong>Dwmgetunmettabrequirements</strong></a><br/></td>
<td><blockquote>
<strong>Hinweis</strong>  Diese Funktion ist öffentlich verfügbar, aber nicht funktionsfähig für Windows 10, Version 1803.
</blockquote>
Überprüft die erforderlichen Anforderungen zum erhalten von Registerkarten in der Titelleiste der Anwendung für das angegebene Fenster.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetwindowattribute"><strong>DwmGetWindowAttribute</strong></a><br/></td>
<td>Ruft den aktuellen Wert eines angegebenen Attributs ab, das auf ein Fenster angewendet wird.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwminvalidateiconicbitmaps"><strong>Dwminvalidateiconfiguration</strong></a><br/></td>
<td>Wird von einer Anwendung aufgerufen, um anzugeben, dass alle zuvor bereitgestellten ikonischen Bitmaps aus einem Fenster, sowohl Miniaturansichten als auch Peek-Darstellungen, aktualisiert werden sollen.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmiscompositionenabled"><strong>DwmIsCompositionEnabled</strong></a><br/></td>
<td>Ruft einen Wert ab, der angibt, ob die DWM-Komposition aktiviert ist. Anwendungen auf Computern, auf denen Windows 7 oder früher ausgeführt wird, können Änderungen am Kompositions Status überwachen, indem Sie die <a href="wm-dwmcompositionchanged.md"><strong>WM_DWMCOMPOSITIONCHANGED</strong></a> Benachrichtigung verarbeiten.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmmodifypreviousdxframeduration"><strong>Dwmmodifypreviousdxframeduration</strong></a><br/></td>
<td>Ändert die Anzahl von Monitor Aktualisierungen, über die der vorherige Frame angezeigt wird. <br/> <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmmodifypreviousdxframeduration"><strong>Dwmmodifypreviousdxframeduration</strong></a> wird nicht mehr unterstützt. Beginnend mit Windows 8.1 geben Aufrufe von <strong>dwmmodifypreviousdxframeduration</strong> immer E_NOTIMPL zurück.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmquerythumbnailsourcesize"><strong>DwmQueryThumbnailSourceSize</strong></a><br/></td>
<td>Ruft die Quellgröße der DWM-Miniaturansicht ab.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmregisterthumbnail"><strong>Dwmregisterminiatur</strong></a><br/></td>
<td>Erstellt eine DWM-Miniatur Ansichts Beziehung zwischen den Ziel-und Quell Fenstern.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmrendergesture"><strong>Dwmrendergeste</strong></a><br/></td>
<td>Benachrichtigt dwm, dass ein touchkontakt als Geste erkannt wurde und dass DWM Feedback für diese Geste zeichnen sollte.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetdxframeduration"><strong>Dwmsetdxframeduration</strong></a><br/></td>
<td>Legt die Anzahl von Monitor Aktualisierungen fest, mit denen der dargestellte Frame angezeigt werden soll. <br/> " <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetdxframeduration"><strong>Dwmsetdxframeduration</strong></a> " wird nicht mehr unterstützt. Beginnend mit Windows 8.1 geben Aufrufe von <strong>dwmsetdxframeduration</strong> immer E_NOTIMPL zurück.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap"><strong>Dwmabticoniclivepreviewbitmap</strong></a><br/></td>
<td>Legt eine statische, legendäre Bitmap fest, um eine <em>Live Vorschau</em> (auch als <em>Peek Preview</em>bezeichnet) eines Fensters oder einer Registerkarte anzuzeigen. In der Taskleiste kann diese Bitmap verwendet werden, um eine Vorschau eines Fensters oder einer Registerkarte in voller Höhe anzuzeigen.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticonicthumbnail"><strong>Dwmcticonfiguration</strong></a><br/></td>
<td>Legt eine statische, ikonische Bitmap auf einem Fenster oder einer Registerkarte fest, die als Miniaturansicht verwendet werden soll. Die Taskleiste kann diese Bitmap als Miniatur Ansichts Ziel für das Fenster oder die Registerkarte verwenden.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters"><strong>Dwmsetpresentparameters</strong></a><br/></td>
<td>Legt die aktuellen Parameter für die Frame Komposition fest. <br/> " <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters"><strong>Dwmsetpresentparameters</strong></a> " wird nicht mehr unterstützt. Beginnend mit Windows 8.1 geben Aufrufe von <strong>dwmsetpresentparameters</strong> immer E_NOTIMPL zurück.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute"><strong>DwmSetWindowAttribute</strong></a><br/></td>
<td>Legt den Wert von nicht-Client-renderingattributen für ein Fenster fest.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/dwmapi/nf-dwmapi-dwmshowcontact"><strong>Dwmshowcontact</strong></a><br/></td>
<td>Wird von einer APP oder einem Framework aufgerufen, um den Typ des visuellen Feedbacks anzugeben, der als Reaktion auf einen bestimmten touchabdruck oder Stift Kontakt gezeichnet werden soll.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmtethercontact"><strong>Dwmtethercontact</strong></a><br/></td>
<td>Ermöglicht das grafische Feedback von toucheingaben und Zieh Interaktionen an den Benutzer.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/dwmapi/nf-dwmapi-dwmtransitionownedwindow"><strong>Dwmtransitionownedwindow</strong></a><br/></td>
<td>Koordiniert die Animationen von Tool Fenstern mit dem dwm.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmunregisterthumbnail"><strong>Dwmunregisterminiatur</strong></a><br/></td>
<td>Entfernt eine DWM-Miniaturansicht, die von der <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmregisterthumbnail"><strong>dwmregisterminiatur</strong></a> -Funktion erstellt wurde.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmupdatethumbnailproperties"><strong>DwmUpdateThumbnailProperties</strong></a><br/></td>
<td>Aktualisiert die Eigenschaften für eine DWM-Miniaturansicht.<br/></td>
</tr>
</tbody>
</table>



 

 

