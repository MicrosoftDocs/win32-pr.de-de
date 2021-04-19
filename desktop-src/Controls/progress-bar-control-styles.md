---
title: Statusanzeige-Steuerelement Stile (kommctrl. h)
description: Die folgenden Steuerelement Stile werden von Statusanzeige-Steuerelementen unterstützt.
ms.assetid: bd89aa74-c15e-4745-8b2b-7cbd8b28c1c8
topic_type:
- apiref
api_name:
- PBS_MARQUEE
- PBS_SMOOTH
- PBS_SMOOTHREVERSE
- PBS_VERTICAL
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d55ec928fb1ee2715576f3131dde0f661a91fcf8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370081"
---
# <a name="progress-bar-control-styles"></a>Stile der Statusanzeige-Steuerelemente

Die folgenden Steuerelement Stile werden von den [Status](progress-bar-control.md) Anzeige-Steuerelementen unterstützt:



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
<td style="text-align: left;"><span id="PBS_MARQUEE"></span><span id="pbs_marquee"></span><dl> <dt><strong>PBS_MARQUEE</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Version 6,0</a> oder höher. Der Status Indikator vergrößert sich nicht in der Größe, sondern verschiebt sich wiederholt entlang der Länge des Balkens, was die Aktivität angibt, ohne anzugeben, welcher Anteil des Fortschritts abgeschlossen ist. <br/>
<blockquote>
[!Note]<br />
Comctl32.dll Version 6 ist nicht Verteil Bar, aber in Windows oder höher enthalten. Wenn Sie Comctl32.dll Version 6 verwenden möchten, geben Sie ihn in einem Manifest an. Weitere Informationen zu Manifesten finden Sie unter <a href="cookbook-overview.md">Aktivieren von visuellen Stilen</a>.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="PBS_SMOOTH"></span><span id="pbs_smooth"></span><dl> <dt><strong>PBS_SMOOTH</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Version 4,70</a> oder höher. In der Statusleiste wird der Status Status in einer Smooth Scrollleiste anstelle der standardmäßigen segmentierten Leiste angezeigt. <br/>
<blockquote>
[!Note]<br />
Dieser Stil wird nur im klassischen Windows-Design unterstützt. Alle anderen Designs überschreiben diesen Stil.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="PBS_SMOOTHREVERSE"></span><span id="pbs_smoothreverse"></span><dl> <dt><strong>PBS_SMOOTHREVERSE</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Version 6,0</a> oder höher und <strong>Windows Vista.</strong> Bestimmt das Animations Verhalten, das von der Statusanzeige bei Rückwärtsbewegung (von einem höheren zu einem niedrigeren Wert) verwendet werden soll. Wenn dies festgelegt ist, &quot; wird ein reibungsloser &quot; Übergang ausgeführt, andernfalls springt das Steuerelement &quot; &quot; zum niedrigeren Wert.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="PBS_VERTICAL"></span><span id="pbs_vertical"></span><dl> <dt><strong>PBS_VERTICAL</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Version 4,70</a> oder höher. In der Statusleiste wird der Status vertikal von unten nach oben angezeigt.<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Bemerkungen

Sie können die Stile der Statusanzeige auf die gleiche Weise wie andere gängige Steuerelemente mit "", " [**", "**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)", " [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga)" oder " [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)" festlegen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Kommstrg. h</dt> </dl> |



 

