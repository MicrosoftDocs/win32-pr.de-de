---
title: DWM-Nachrichten
description: Dieser Abschnitt enthält Informationen zu den Desktopfenster-Manager -Nachrichten (DWM).
ms.assetid: FF251CDA-7D68-4dd0-A54B-50B07E11C7C1
keywords:
- Desktopfenster-Manager (DWM), Referenz
- DWM (Desktopfenster-Manager),Referenz
- Desktopfenster-Manager (DWM),messages
- DWM (Desktopfenster-Manager),Messages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3715494dc514dea471e50321acf1f64c5745ffe52dacae69752c8f10fecf0e84
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119726020"
---
# <a name="dwm-messages"></a>DWM-Nachrichten

Dieser Abschnitt enthält Informationen zu den Desktopfenster-Manager -Nachrichten (DWM).

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
<td><a href="wm-dwmcolorizationcolorchanged.md"><strong>WM_DWMCOLORIZATIONCOLORCHANGED</strong></a><br/></td>
<td>Informiert alle Fenster der obersten Ebene darüber, dass sich die Farbgebungsfarbe geändert hat.<br/></td>
</tr>
<tr class="even">
<td><a href="wm-dwmcompositionchanged.md"><strong>WM_DWMCOMPOSITIONCHANGED</strong></a><br/></td>
<td>Informiert alle Fenster der obersten Ebene darüber, dass die DWM-Komposition aktiviert oder deaktiviert wurde. <br/>
<blockquote>
[!Note]<br />
Ab Windows 8 ist die DWM-Komposition immer aktiviert, sodass diese Nachricht unabhängig von Änderungen des Videomodus nicht gesendet wird.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="wm-dwmncrenderingchanged.md"><strong>WM_DWMNCRENDERINGCHANGED</strong></a><br/></td>
<td>Wird gesendet, wenn sich die Richtlinie zum Rendern von Nicht-Clientbereich geändert hat.<br/></td>
</tr>
<tr class="even">
<td><a href="wm-dwmsendiconiclivepreviewbitmap.md"><strong>WM_DWMSENDICONICLIVEPREVIEWBITMAP</strong></a><br/></td>
<td>Weist ein Fenster an, eine statische Bitmap zur Verwendung als <em></em>Livevorschau <em>(auch</em> als Vorschau anzeigen) dieses Fensters zu verwenden.<br/></td>
</tr>
<tr class="odd">
<td><a href="wm-dwmsendiconicthumbnail.md"><strong>WM_DWMSENDICONICTHUMBNAIL</strong></a><br/></td>
<td>Weist ein Fenster an, eine statische Bitmap zur Verwendung als Miniaturansicht dieses Fensters zur Verfügung zu stellen.<br/></td>
</tr>
<tr class="even">
<td><a href="wm-dwmwindowmaximizedchange.md"><strong>WM_DWMWINDOWMAXIMIZEDCHANGE</strong></a><br/></td>
<td>Wird gesendet, wenn ein dwm-zusammengestelltes Fenster maximiert ist.<br/></td>
</tr>
</tbody>
</table>



 

 

 





