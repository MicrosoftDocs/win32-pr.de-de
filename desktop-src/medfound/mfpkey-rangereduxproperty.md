---
description: Gibt den Grad an, in dem der Codec den effektiven Farbbereich des Videos reduzieren soll.
ms.assetid: 7227957b-59c9-4dd9-ad2b-a383e888cd46
title: MFPKEY_RANGEREDUX-Eigenschaft (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b3a186522cdc328ab7b6f8e11154ae605673d2cca9d988e0e07c0d159e71589
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113310"
---
# <a name="mfpkey_rangeredux-property"></a>MFPKEY \_ RANGEREDUX-Eigenschaft

Gibt den Grad an, in dem der Codec den effektiven Farbbereich des Videos reduzieren soll.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

g \_ wszWMVCRangeRedux

## <a name="data-type"></a>Datentyp

VT \_ I4

## <a name="default-value"></a>Standardwert

0

## <a name="remarks"></a>Hinweise

Bereichsverringerung gibt den Grad an, in dem der Codec luma und den Bereich des Videos reduzieren soll. Durch das Reduzieren des Bereichs wird die Größe codierter Videoframes reduziert, aber auch die Farbdetails des Videos.

Die Bereichsverringerung besteht aus einer Reduzierung während der Codierung und Erweiterung während der Decodierung. Es ist möglich, die Erweiterungsfaktoren von den Reduzierungsfaktoren zu unterscheiden. Dies wird jedoch in den meisten Szenarien, in denen die Bereichsumkehnung nützlich ist, nicht empfohlen.

Die Bereichsverringerung und -erweiterung erfolgt separat für Luma- und Channel-Kanäle. Das Reduzieren des Bereichs kann eine effiziente Möglichkeit sein, die Komplexität von Videos mit niedriger Bitrate zu reduzieren, ohne die Bilddetails zu einbußen. Wenn Sie alle vier Werte auf 8 festlegen, wird die Menge an Luma- und Stichinformationen um die Hälfte reduziert, und es müssen mehr Bits an die Beibehaltung von Bilddetails geleitet werden.

Der Codec kann die Bereichsverringerung beim Codieren von Videos mit sehr niedrigen Bitraten automatisch verwenden. Wenn Sie alle vier Werte auf 0 festlegen, wird die Bereichsverringerung auch in Szenarien mit niedriger Bitrate vollständig deaktiviert.

Das Reduzieren des Farbbereichs reduziert die codierte Größe von Videoframes, kann jedoch zu Unscharfheit in den decodierten Frames führen.

Wenn diese Eigenschaft nicht festgelegt ist, bestimmt der Codec, ob die Bereichsverringerung zur Codierungszeit verwendet werden soll. In der Regel wird diese Option vom Codec nur mit niedrigen Bitraten ausgewählt.

Der Wert dieser Eigenschaft ist eine Kombination aus vier Komponenten, getrennt durch Nullen, formatiert als 0x0M0m0N0n, wobei:

-   M ist der Codierungsbereichsverringerungsfaktor für die Y-Komponente.
-   m ist der Decodierungsbereichserweiterungsfaktor für die Y-Komponente (in der Regel identisch mit M).
-   N ist der Codierungsbereichsreduzierungsfaktor für die UV-Komponente.
-   n ist der Decodierungsbereichserweiterungsfaktor für die UV-Komponente (in der Regel identisch mit N).

Jeder Faktor ist eine Ziffer von 0 bis 8, wobei 0 keine Reduzierung oder Erweiterung und 8 die maximale Reduzierung oder Erweiterung ist.

Wenn Sie den Wert auf 0x00000000, ist die Bereichsverringerung vollständig deaktiviert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Media Foundation Eigenschaften](media-foundation-properties.md)
</dt> </dl>

 

 




