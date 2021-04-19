---
title: DWM-Meldungen
description: Dieser Abschnitt enthält Informationen zu den Desktopfenster-Manager (DWM)-Nachrichten.
ms.assetid: FF251CDA-7D68-4dd0-A54B-50B07E11C7C1
keywords:
- Desktopfenster-Manager (DWM), Referenz
- Dwm (Desktopfenster-Manager), Referenz
- Desktopfenster-Manager (DWM), Nachrichten
- Dwm (Desktopfenster-Manager), Nachrichten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 399db1399cfc7cb60d29f0fa554a2233dc75a279
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/11/2020
ms.locfileid: "106339865"
---
# <a name="dwm-messages"></a>DWM-Meldungen

Dieser Abschnitt enthält Informationen zu den Desktopfenster-Manager (DWM)-Nachrichten.

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
<td><a href="wm-dwmcolorizationcolorchanged.md"><strong>WM_DWMCOLORIZATIONCOLORCHANGED</strong></a><br/></td>
<td>Informiert alle Fenster der obersten Ebene darüber, dass sich die Farbe der Farbgebung geändert hat.<br/></td>
</tr>
<tr class="even">
<td><a href="wm-dwmcompositionchanged.md"><strong>WM_DWMCOMPOSITIONCHANGED</strong></a><br/></td>
<td>Informiert alle Fenster der obersten Ebene, dass die DWM-Komposition aktiviert oder deaktiviert wurde. <br/>
<blockquote>
[!Note]<br />
Ab Windows 8 ist die DWM-Komposition immer aktiviert, sodass diese Nachricht unabhängig von den videomodusänderungen nicht gesendet wird.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="wm-dwmncrenderingchanged.md"><strong>WM_DWMNCRENDERINGCHANGED</strong></a><br/></td>
<td>Wird gesendet, wenn sich die Renderingleistung des nicht-Client Bereichs geändert hat<br/></td>
</tr>
<tr class="even">
<td><a href="wm-dwmsendiconiclivepreviewbitmap.md"><strong>WM_DWMSENDICONICLIVEPREVIEWBITMAP</strong></a><br/></td>
<td>Weist ein Fenster an, eine statische Bitmap bereitzustellen, die als <em>Live Vorschau</em> (auch als <em>Vorschau Vorschau</em>bezeichnet) dieses Fensters verwendet werden soll.<br/></td>
</tr>
<tr class="odd">
<td><a href="wm-dwmsendiconicthumbnail.md"><strong>WM_DWMSENDICONICTHUMBNAIL</strong></a><br/></td>
<td>Weist ein Fenster an, ein statisches Bitmap bereitzustellen, das als Miniaturansicht dieses Fensters verwendet werden soll.<br/></td>
</tr>
<tr class="even">
<td><a href="wm-dwmwindowmaximizedchange.md"><strong>WM_DWMWINDOWMAXIMIZEDCHANGE</strong></a><br/></td>
<td>Wird gesendet, wenn ein von der DWM-Fenster erstellt wird.<br/></td>
</tr>
</tbody>
</table>



 

 

 





