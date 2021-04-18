---
title: Animations Steuerelement Stile (kommctrl. h)
description: In diesem Abschnitt werden die mit Animations Steuerelementen verwendeten Fenster Stile aufgelistet.
ms.assetid: ad4fc4fd-166d-4871-9f60-5133a48681aa
topic_type:
- apiref
api_name:
- ACS_AUTOPLAY
- ACS_CENTER
- ACS_TIMER
- ACS_TRANSPARENT
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d779b92c51420bc6bd9ad238bcff538dbc85841f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364940"
---
# <a name="animation-control-styles"></a>Animations Steuerelement Stile

In diesem Abschnitt werden die mit Animations Steuerelementen verwendeten Fenster Stile aufgelistet.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Konstante</th>
<th style="text-align: left;">BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="ACS_AUTOPLAY"></span><span id="acs_autoplay"></span><dl> <dt><strong>ACS_AUTOPLAY</strong></dt> </dl></td>
<td style="text-align: left;">Startet die Wiedergabe der Animation, sobald der AVI-Clip geöffnet ist. <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ACS_CENTER"></span><span id="acs_center"></span><dl> <dt><strong>ACS_CENTER</strong></dt> </dl></td>
<td style="text-align: left;">Zentriert die Animation im Fenster des Animations Steuer Elements. <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ACS_TIMER"></span><span id="acs_timer"></span><dl> <dt><strong>ACS_TIMER</strong></dt> </dl></td>
<td style="text-align: left;">Standardmäßig erstellt das Steuerelement einen Thread zur Wiedergabe des AVI-Clips. Wenn Sie dieses Flag festlegen, gibt das Steuerelement den Clip wieder, ohne einen Thread zu erstellen. intern verwendet das Steuerelement einen Win32-Timer zum Synchronisieren der Wiedergabe. <br/> <strong>Comctl32.dll Version 6 und höher:</strong> Dieser Stil wird nicht unterstützt. Standardmäßig gibt das-Steuerelement den AVI-Clip wieder, ohne einen Thread zu erstellen.<br/>
<blockquote>
[!Note]<br />
Comctl32.dll Version 6 ist nicht Verteil Bar. Wenn Sie Comctl32.dll Version 6 verwenden möchten, geben Sie ihn in einem Manifest an. Weitere Informationen zu Manifesten finden Sie unter <a href="cookbook-overview.md">Aktivieren von visuellen Stilen</a>.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ACS_TRANSPARENT"></span><span id="acs_transparent"></span><dl> <dt><strong>ACS_TRANSPARENT</strong></dt> </dl></td>
<td style="text-align: left;">Ermöglicht es Ihnen, die Hintergrundfarbe einer Animation mit der des zugrunde liegenden Fensters zu vergleichen und so einen &quot; transparenten Hintergrund zu erstellen &quot; . Das übergeordnete Element des Animations Steuer Elements darf nicht den WS_CLIPCHILDREN Stil aufweisen (siehe <a href="/windows/desktop/winmsg/window-styles">Fenster Stile</a>). Das-Steuerelement sendet eine <a href="wm-ctlcolorstatic.md"><strong>WM_CTLCOLORSTATIC</strong></a> Meldung an das übergeordnete Element. Legen Sie mit <a href="/windows/desktop/api/wingdi/nf-wingdi-setbkcolor"><strong>SetBkColor</strong></a> die Hintergrundfarbe für den Gerätekontext auf einen geeigneten Wert fest. Das-Steuerelement interpretiert das linke obere Pixel des ersten Frames als Standard Hintergrundfarbe der Animation. Alle Pixel mit dieser Farbe werden dem Wert neu zugeordnet, den Sie als Reaktion auf WM_CTLCOLORSTATIC angegeben haben. <br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Kommstrg. h</dt> </dl> |



