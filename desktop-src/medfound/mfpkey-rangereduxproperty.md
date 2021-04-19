---
description: Gibt den Grad an, zu dem der Codec den effektiven Farbbereich des Videos verringern soll.
ms.assetid: 7227957b-59c9-4dd9-ad2b-a383e888cd46
title: MFPKEY_RANGEREDUX-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49ec326e5d21a72792aab38f08d8c8c9207ab867
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349151"
---
# <a name="mfpkey_rangeredux-property"></a>Mfpkey \_ rangeredux (Eigenschaft)

Gibt den Grad an, zu dem der Codec den effektiven Farbbereich des Videos verringern soll.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

g \_ wszwmvcrangeredux

## <a name="data-type"></a>Datentyp

VT \_ I4

## <a name="default-value"></a>Standardwert

0

## <a name="remarks"></a>Bemerkungen

Bereichs Reduzierung gibt den Grad an, in dem der Codec den Bereich von Luma und Chroma des Videos verringern soll. Durch Verringern des Bereichs wird die Größe codierter Video Frames reduziert, aber auch die Farbdetails des Videos reduziert.

Die Bereichs Reduzierung besteht aus der Verringerung der Codierung und der Erweiterung während der Decodierung. Die Erweiterungs Faktoren können sich von den Reduzierungs Faktoren unterscheiden, aber dies wird in den meisten Szenarien nicht empfohlen, in denen das Neuzuordnen von Bereichen nützlich ist.

Die Bereichs Reduzierung und-Erweiterung erfolgt separat in den Kanälen von Luma und Chroma. Das Verringern des Bereichs kann eine effiziente Möglichkeit zum Reduzieren der Komplexität von Videos mit niedriger Bitrate sein, ohne dass die Bilddetails beeinträchtigt werden. Wenn Sie alle vier Werte auf 8 festlegen, wird die Menge der Informationen zu "Luma" und "Chroma" um die Hälfte reduziert, sodass mehr Bits zum Beibehalten der Bilddetails umgeleitet werden.

Beim Codieren von Videos mit sehr niedrigen Bitraten kann der Codec die Bereichs Reduzierung automatisch verwenden. Wenn Sie alle vier Werte auf 0 festlegen, wird die Bereichs Reduzierung auch in Szenarios mit geringem Bitrate vollständig deaktiviert.

Wenn Sie den Farbbereich verringern, wird die codierte Größe von Video Frames reduziert, aber es kann zu einer Unhöflichkeit in den decodierten Frames führen.

Wenn diese Eigenschaft nicht festgelegt ist, bestimmt der Codec, ob die Bereichs Reduzierung zur Codierungs Zeit verwendet werden soll. Diese Option wird normalerweise nur bei niedrigen Bitraten durch den Codec ausgewählt.

Der Wert dieser Eigenschaft ist eine Kombination aus vier Komponenten, die durch Nullen getrennt sind und als 0x0m0m0n0n formatiert sind, wobei Folgendes gilt:

-   M ist der Codierungs Bereich-Reduzierungs Faktor für die Y-Komponente.
-   m ist der Erweiterungs Faktor für den Decodierungs Bereich für die Y-Komponente (normalerweise identisch mit m).
-   N ist der Codierungs Bereich-Reduzierungs Faktor für die UV-Komponente.
-   n ist der Erweiterungs Faktor für den Decodierungs Bereich für die UV-Komponente (normalerweise identisch mit n).

Jeder Faktor ist eine Ziffer zwischen 0 und 8, wobei 0 keine Verringerung oder Erweiterung und 8 die maximale Reduzierung oder Erweiterung ist.

Wenn Sie den Wert auf 0x00000000 festlegen, wird die Bereichs Verkleinerung vollständig deaktiviert.

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

 

 




