---
description: Gibt die Anzahl der durch den Codec codierten Video Frames an, die tatsächlich Daten enthalten.
ms.assetid: f96fd0b2-8c81-4318-b44c-4b794b3945a3
title: MFPKEY_CODEDNONZEROFRAMES-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b1ca5fb26288e2ea9ff801ba13aa7bef570ca95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347561"
---
# <a name="mfpkey_codednonzeroframes-property"></a>Mfpkey \_ codednonzeroframes (Eigenschaft)

Gibt die Anzahl der durch den Codec codierten Video Frames an, die tatsächlich Daten enthalten.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.

## <a name="data-type"></a>Datentyp

VT \_ I4

## <a name="remarks"></a>Bemerkungen

Dieser Wert ist gleich " [mfpkey \_ totalFrames](mfpkey-totalframesproperty.md) " abzüglich aller Frames, die aufgrund von Bitraten Einschränkungen (abzüglich aller NULL-Byte-Frames) gelöscht wurden. Sie können diesen Wert erhalten, nachdem Sie die Übergabe von Beispielen abgeschlossen haben. Für doppelte Frames können NULL-Byte-Frames erstellt werden.

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

 

 
