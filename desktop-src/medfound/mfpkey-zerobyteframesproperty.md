---
description: Gibt die Anzahl der Videorahmen an, die übersprungen werden, da Sie Duplikate vorheriger Frames waren.
ms.assetid: ef4aa5a0-3788-493e-b541-c3a24509d939
title: MFPKEY_ZEROBYTEFRAMES-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffcf29d099b3a3fb27a307e970af7af1a5c3d58b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863432"
---
# <a name="mfpkey_zerobyteframes-property"></a>Mfpkey \_ zerobyteframes (Eigenschaft)

Gibt die Anzahl der Videorahmen an, die übersprungen werden, da Sie Duplikate vorheriger Frames waren.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

g \_ wszwmvczerobyteframes

## <a name="data-type"></a>Datentyp

VT \_ I4

## <a name="remarks"></a>Bemerkungen

Der Wert wird nicht von der Gesamtzahl der übergebenen Frames ([mfpkey \_ totalFrames](mfpkey-totalframesproperty.md)) abgezogen, wenn die Anzahl der codierten Frames ([mfpkey \_ codedframes](mfpkey-codedframesproperty.md)) berechnet wird.

Sie können den Codec daran hindern, doppelte Frames zu überspringen, indem Sie [mfpkey \_ producedummyframes](mfpkey-producedummyframesproperty.md) auf Variant \_ true festlegen.

Sie können diesen Wert erhalten, nachdem Sie die Übergabe von Beispielen abgeschlossen haben.

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

 

 




