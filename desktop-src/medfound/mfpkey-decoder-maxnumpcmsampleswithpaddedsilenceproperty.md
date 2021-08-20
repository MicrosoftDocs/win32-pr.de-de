---
description: Gibt die maximale Anzahl zusätzlicher PCM-Beispiele an, die nach dem Decodieren einer Datei am Ende zurückgegeben werden können.
ms.assetid: 82b3676c-7653-421c-aac7-7f20a642779f
title: MFPKEY_Decoder_MaxNumPCMSamplesWithPaddedSilence-Eigenschaft (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1722c4c8457035f082b069f46f1758d7caf4a4f3b8f500ebd4462e334778e79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117690358"
---
# <a name="mfpkey_decoder_maxnumpcmsampleswithpaddedsilence-property"></a>\_MFPKEY-Decoder: \_ MaxNumPCMSamplesWithPaddedSilence-Eigenschaft

Gibt die maximale Anzahl zusätzlicher PCM-Beispiele an, die nach dem Decodieren einer Datei am Ende zurückgegeben werden können.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.

## <a name="data-type"></a>Datentyp

VT \_ I4

## <a name="default-value"></a>Standardwert

2048

## <a name="remarks"></a>Hinweise

Diese Eigenschaft kann verwendet werden, um künstliche Stille zu schätzen, die zwischen Titeln eingefügt wird, während sie nacheinander an den Decoder gespeist werden.

Für die Windows Media Audio 10-Professional und Windows Media Audio 9 Lossless-Decoder ist diese Eigenschaft immer gleich 0.

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

 

 
