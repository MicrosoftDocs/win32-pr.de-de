---
description: Gibt die maximale Anzahl zusätzlicher PCM-Beispiele an, die nach dem Decodieren einer Datei am Ende von zurückgegeben werden können.
ms.assetid: 82b3676c-7653-421c-aac7-7f20a642779f
title: MFPKEY_Decoder_MaxNumPCMSamplesWithPaddedSilence-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b1f97b55c2eedd8cc7d6d524379569073fa35d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343834"
---
# <a name="mfpkey_decoder_maxnumpcmsampleswithpaddedsilence-property"></a>Mfpkey- \_ Decoder \_ MaxNumPCMSamplesWithPaddedSilence Eigenschaft

Gibt die maximale Anzahl zusätzlicher PCM-Beispiele an, die nach dem Decodieren einer Datei am Ende von zurückgegeben werden können.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.

## <a name="data-type"></a>Datentyp

VT \_ I4

## <a name="default-value"></a>Standardwert

2048

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft kann verwendet werden, um künstliche Stille zu schätzen, die zwischen den Liedern eingefügt wird, wenn Sie dem Decoder nacheinander zugeführt werden.

Für die Windows Media Audio 10 Professional-und Windows Media Audio 9-Decoders ohne Verlust ist diese Eigenschaft stets gleich 0 (null).

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

 

 
