---
description: Ruft die effektive URL eines Bytestreams ab.
ms.assetid: 0A83CFC0-7EAA-464B-BA39-50DF220AF683
title: MF_BYTESTREAM_EFFECTIVE_URL -Attribut (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98f26ece6ef4b0c4b25629f6669296cec56e23a4bf28b7e284b343e16c0df512
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941080"
---
# <a name="mf_bytestream_effective_url-attribute"></a>MF \_ BYTESTREAM \_ EFFECTIVE \_ URL-Attribut

Ruft die effektive URL eines Bytestreams ab.

## <a name="data-type"></a>Datentyp

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut zu erhalten, rufen [**Sie DEN ATTRIBUTEAttributes::GetString auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)

Rufen Sie ZUM Festlegen dieses [**Attributs DEN WERTATTRIBUTEs::SetString auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)

## <a name="applies-to"></a>Gilt für:

[**VERERBByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)

## <a name="remarks"></a>Hinweise

Die effektive URL kann sich von der ursprünglichen URL unterscheiden, wenn die ursprüngliche URL zusätzliche Informationen enthält, z. B. Suchzeichenfolgen oder Anker, oder wenn die Anforderung umgeleitet wurde.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Desktop-Apps \| UWP-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Desktop-Apps \| UWP-Apps\]<br/>                            |
| Header<br/>                   | <dl> <dt>Mfobjects.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Bytestreamattribute](byte-stream-attributes.md)
</dt> <dt>

[**VERERBByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)
</dt> </dl>

 

 




