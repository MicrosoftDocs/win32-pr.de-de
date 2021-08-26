---
description: Gibt die durchschnittlichen Bytes pro Sekunde in einem qualitätsbasierten VBR-Audiostream (Variable Bit Rate) an.
ms.assetid: dcee969a-617e-4045-a468-8158afb06356
title: MFPKEY_WMAENC_AVGBYTESPERSEC-Eigenschaft (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfadc41e9f2c9f4410bc84c6d8bf23f30c559b96c83abba80beb719e8ccb8eba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119953300"
---
# <a name="mfpkey_wmaenc_avgbytespersec-property"></a>MFPKEY \_ WMAENC \_ AVGBYTESPERSEC-Eigenschaft

Gibt die durchschnittlichen Bytes pro Sekunde in einem qualitätsbasierten VBR-Audiostream (Variable Bit Rate) an.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

g \_ wszWMACAvgBytesPerSecond

## <a name="data-type"></a>Datentyp

VT \_ I4

## <a name="remarks"></a>Hinweise

Sie können diesen Wert aus dem Decoder erhalten, nachdem der Stream codiert wurde.

Dieser Wert ist für den Audiodecoder erforderlich, um den Inhalt ordnungsgemäß zu dekomprimieren.

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

 

 




