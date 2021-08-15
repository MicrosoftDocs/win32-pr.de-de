---
description: Gibt die optimalen Visuellen Qualitätseinstellungen an, die für den encoder für Windows Media Video 9 Advanced Profile verwendet werden sollen.
ms.assetid: 9449b5fa-4f13-4c33-bfdf-611720e8dd77
title: MFPKEY_COMPRESSIONOPTIMIZATIONTYPE-Eigenschaft (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c7171990280fe004b12c306a09af3b617ba2de0a7cfa274edb3d9191b16a886
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118242879"
---
# <a name="mfpkey_compressionoptimizationtype-property"></a>MFPKEY \_ COMPRESSIONOPTIMIZATIONTYPE-Eigenschaft

Gibt die optimalen Visuellen Qualitätseinstellungen an, die für den encoder für Windows Media Video 9 Advanced Profile verwendet werden sollen.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

g \_ wszWMVCCompressionOptimizationType

## <a name="data-type"></a>Datentyp

VT \_ I4

## <a name="default-value"></a>Standardwert

0

## <a name="remarks"></a>Hinweise

Diese Eigenschaft bietet eine schnelle Möglichkeit, eine Reihe von Videocodierungsoptionen zu konfigurieren. Sie kann auf einen der folgenden Werte festgelegt werden.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Wert</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>0</td>
<td>Der Codec zwingt die Optimierung nicht und verwendet alle Funktionen, die von anderen Eigenschaften angegeben werden. In vielen Fällen verwendet der Codec interne Logik, um Einstellungen zu bestimmen, wenn sie nicht angegeben sind. Dies ist der Standardwert.</td>
</tr>
<tr class="even">
<td>1</td>
<td>Aktiviert die Features, die die beste visuelle Qualität erzeugen. Wenn Sie diesen Wert verwenden, wird der Codec so konfiguriert, als hätten Sie die folgenden Eigenschaften festgelegt:<br/>
<ul>
<li><a href="mfpkey-bdeltaqpproperty.md">MFPKEY_BDELTAQP</a> = 1</li>
<li><a href="mfpkey-complexityexproperty.md">MFPKEY_COMPLEXITYEX</a> = 3</li>
<li><a href="mfpkey-loopfilterproperty.md">MFPKEY_LOOPFILTER</a> = 1</li>
<li><a href="mfpkey-motionmatchmethodproperty.md">MFPKEY_MOTIONMATCHMETHOD</a> = -1</li>
<li><a href="mfpkey-motionsearchlevelproperty.md">MFPKEY_MOTIONSEARCHLEVEL</a> = 1</li>
<li><a href="mfpkey-motionsearchrangeproperty.md">MFPKEY_MOTIONSEARCHRANGE</a> = -1</li>
<li><a href="mfpkey-numbframesproperty.md">MFPKEY_NUMBFRAMES</a> = 1</li>
</ul>
Wenn Sie eine der Eigenschaften in der vorherigen Liste festlegen, überschreibt der festgelegte Wert die Werte, die dieser Einstellung zugeordnet sind, mit Ausnahme <a href="mfpkey-complexityexproperty.md">von MFPKEY_COMPLEXITYEX</a>.<br/></td>
</tr>
</tbody>
</table>



 

Das Festlegen des Werts der MFPKEY \_ COMPRESSIONOPTIMIZATIONTYPE-Eigenschaft auf 1 wirkt sich auch darauf aus, dass die Registrierungseinstellung Dquant Option auf 2 und die Registrierungseinstellung Motion Vector Cost Method auf 1 festgelegt wird. Weitere Informationen finden Sie im Webartikel [Verwenden der erweiterten Einstellungen des Windows Media Video 9 Advanced Profile Codec](https://www.microsoft.com/windows/windowsmedia/howto/articles/codecadvancedsettings.aspx).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Media Foundation-Eigenschaften](media-foundation-properties.md)
</dt> </dl>

 

 




