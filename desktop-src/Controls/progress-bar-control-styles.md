---
title: Statusleisten-Steuerelementstile (CommCtrl.h)
description: Die folgenden Steuerelementstile werden von Progress Bar-Steuerelementen unterstützt.
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
ms.openlocfilehash: 1216171b116bffb962b3ebfe1a76497473cf2db2
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465276"
---
# <a name="progress-bar-control-styles"></a>Statusleisten-Steuerelementstile

Die folgenden Steuerelementstile werden von [Progress Bar-Steuerelementen](progress-bar-control.md) unterstützt:




| Konstante | BESCHREIBUNG | 
|----------|-------------|
| <span id="PBS_MARQUEE"></span><span id="pbs_marquee"></span><dl><dt><strong>PBS_MARQUEE</strong></dt></dl> | <a href="common-control-versions.md">Version 6.0</a> oder höher. Der Statusindikator vergrößert sich nicht, sondern bewegt sich wiederholt entlang der Länge des Balkens. Dies gibt die Aktivität an, ohne anzugeben, welcher Anteil des Fortschritts abgeschlossen ist. <br /><blockquote>[!Note]<br />Comctl32.dll Version 6 ist nicht verteilbar, aber in Windows oder höher enthalten. Um Comctl32.dll Version 6 zu verwenden, geben Sie sie in einem Manifest an. Weitere Informationen zu Manifesten finden Sie unter <a href="cookbook-overview.md">Aktivieren von visuellen Stilen.</a></blockquote><br /> | 
| <span id="PBS_SMOOTH"></span><span id="pbs_smooth"></span><dl><dt><strong>PBS_SMOOTH</strong></dt></dl> | <a href="common-control-versions.md">Version 4.70</a> oder höher. Die Statusanzeige zeigt den Status in einer gleichmäßigen Bildlaufleiste anstelle der standardmäßigen segmentierten Leiste an. <br /><blockquote>[!Note]<br />Dieser Stil wird nur im Windows klassischen Design unterstützt. Alle anderen Designs überschreiben diesen Stil.</blockquote><br /> | 
| <span id="PBS_SMOOTHREVERSE"></span><span id="pbs_smoothreverse"></span><dl><dt><strong>PBS_SMOOTHREVERSE</strong></dt></dl> | <a href="common-control-versions.md">Version 6.0</a> oder höher und <strong>Windows Vista.</strong> Bestimmt das Animationsverhalten, das die Statusanzeige beim Rückwärtsbewegung (von einem höheren Wert zu einem niedrigeren Wert) verwenden soll. Wenn diese Einstellung festgelegt ist, erfolgt ein "reibungsloser" Übergang, andernfalls springt das Steuerelement zum niedrigeren Wert.<br /> | 
| <span id="PBS_VERTICAL"></span><span id="pbs_vertical"></span><dl><dt><strong>PBS_VERTICAL</strong></dt></dl> | <a href="common-control-versions.md">Version 4.70</a> oder höher. Die Statusanzeige zeigt den Status vertikal von unten nach oben an.<br /> | 




## <a name="remarks"></a>Hinweise

Mit [**CreateWindowEx,**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga)oder [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)können Sie Statusanzeigestile auf die gleiche Weise wie andere gängige Steuerelemente festlegen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>CommCtrl.h</dt> </dl> |



 

