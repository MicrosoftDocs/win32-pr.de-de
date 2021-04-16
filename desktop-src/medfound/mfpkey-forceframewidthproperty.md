---
description: Gibt eine zwischen Rahmenbreite für codiertes Video an.
ms.assetid: 805bd587-31af-49b8-b5ab-2dcf2a3f81c5
title: MFPKEY_FORCEFRAMEWIDTH-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea4c8c7ac025de1c089c592a591136df966797d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528670"
---
# <a name="mfpkey_forceframewidth-property"></a>Mfpkey \_ forceframewidth (Eigenschaft)

Gibt eine zwischen Rahmenbreite für codiertes Video an.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

g \_ wszwmvcforceframewidth

## <a name="data-type"></a>Datentyp

VT \_ I4

## <a name="remarks"></a>Bemerkungen

Sie können diesen Wert und die Eigenschaft [mfpkey \_ forceframeheight](mfpkey-forceframeheightproperty.md) festlegen, um zu erzwingen, dass der Encoder den Videostream mit einer Frame Größe codiert, die kleiner als die Eingabe-oder Ausgabe Frame Größen ist. Beim decodierten wird die Größe des Videos an die ursprüngliche Eingabe Auflösung angepasst.

Gültige Frame Dimensionen auf beiden Achsen sind 2 bis 8192 Pixel. Frame Dimensionen müssen durch 2 teilbar sein.

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

 

 




