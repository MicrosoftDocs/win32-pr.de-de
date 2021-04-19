---
description: Gibt die optimalen Einstellungen für die visuelle Qualität an, die für den erweiterten Windows Media Video 9-Profil Encoder verwendet werden sollen.
ms.assetid: 9449b5fa-4f13-4c33-bfdf-611720e8dd77
title: MFPKEY_COMPRESSIONOPTIMIZATIONTYPE-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3000caa10aa7db7d201cd11fd9a189fd6ac33591
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348320"
---
# <a name="mfpkey_compressionoptimizationtype-property"></a>Mfpkey \_ compressionoptimizationtype (Eigenschaft)

Gibt die optimalen Einstellungen für die visuelle Qualität an, die für den erweiterten Windows Media Video 9-Profil Encoder verwendet werden sollen.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

g \_ wszwmvccompressionoptimizationtype

## <a name="data-type"></a>Datentyp

VT \_ I4

## <a name="default-value"></a>Standardwert

0

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft bietet eine schnelle Möglichkeit, eine Reihe von Optionen für die Videocodierung zu konfigurieren. Sie kann auf einen der folgenden Werte festgelegt werden.



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
<td>Der Codec erzwingt keine Optimierung und verwendet alle Funktionen, die von anderen Eigenschaften angegeben werden. In vielen Fällen verwendet der Codec interne Logik, um Einstellungen zu ermitteln, wenn Sie nicht angegeben werden. Dies ist der Standardwert.</td>
</tr>
<tr class="even">
<td>1</td>
<td>Aktiviert die Funktionen, mit denen die beste visuelle Qualität erzeugt wird. Wenn Sie diesen Wert verwenden, wird der Codec so konfiguriert, als hätten Sie die folgenden Eigenschaften festgelegt:<br/>
<ul>
<li><a href="mfpkey-bdeltaqpproperty.md">MFPKEY_BDELTAQP</a> = 1</li>
<li><a href="mfpkey-complexityexproperty.md">MFPKEY_COMPLEXITYEX</a> = 3</li>
<li><a href="mfpkey-loopfilterproperty.md">MFPKEY_LOOPFILTER</a> = 1</li>
<li><a href="mfpkey-motionmatchmethodproperty.md">MFPKEY_MOTIONMATCHMETHOD</a> =-1</li>
<li><a href="mfpkey-motionsearchlevelproperty.md">MFPKEY_MOTIONSEARCHLEVEL</a> = 1</li>
<li><a href="mfpkey-motionsearchrangeproperty.md">MFPKEY_MOTIONSEARCHRANGE</a> =-1</li>
<li><a href="mfpkey-numbframesproperty.md">MFPKEY_NUMBFRAMES</a> = 1</li>
</ul>
Wenn Sie eine der Eigenschaften in der vorherigen Liste festlegen, überschreibt der von Ihnen festgelegte Wert die Werte, die dieser Einstellung zugeordnet sind, mit Ausnahme der <a href="mfpkey-complexityexproperty.md">MFPKEY_COMPLEXITYEX</a>.<br/></td>
</tr>
</tbody>
</table>



 

Wenn Sie den Wert der \_ Eigenschaft "compressionoptimizationtype" der Eigenschaft "mfpkey" auf "1" festlegen, wirkt sich dies auch auf "2" und die Registrierungs Einstellung der Bewegungsvektor-kostenmethode auf "1" aus. Weitere Informationen finden Sie im Webartikel [using the Advanced Settings of the Windows Media Video 9 Advanced Profile Codec](https://www.microsoft.com/windows/windowsmedia/howto/articles/codecadvancedsettings.aspx).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften von Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




