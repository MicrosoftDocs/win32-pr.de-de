---
description: Gibt die Offsets zu den Nutzlastgrenzen in einem Frame für geschützte Beispiele an.
ms.assetid: 8aa25afd-efa8-4fe0-92d4-8432f9d633c9
title: MFSampleExtension_PacketCrossOffsets -Attribut (Wmcontainer.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b39abdcaf0dfb5888c1705a0a76a19c3a55be522b82405f5a77345efe0d8f13e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119102306"
---
# <a name="mfsampleextension_packetcrossoffsets-attribute"></a>MFSampleExtension \_ PacketCrossOffsets-Attribut

Gibt die Offsets zu den Nutzlastgrenzen in einem Frame für geschützte Beispiele an.

## <a name="data-type"></a>Datentyp

Bytearray

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut zu erhalten, rufen [**Sie DEN ATTRIBUTEAttributes::GetBlob auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)

Rufen Sie ZUM Festlegen dieses [**Attributs DIE ATTRIBUTEs::SetBlob auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)

## <a name="applies-to"></a>Gilt für:

[**DURCHSCHN.Sample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>Hinweise

Dieses Attribut gilt für Medienbeispiele, die durch Windows Media Digital Rights Management (DRM) geschützt werden. Der Wert des Attributs ist ein Array von **DWORD-s.** Jeder Eintrag im Array ist der Offset einer Nutzlastgrenze relativ zum Anfang des Frames. Eine Anwendung kann diese Werte beim Entschlüsseln und Rekonstruieren der Frames verwenden.

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Vista-Desktop-Apps \| UWP-Apps\]<br/>                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows UWP-Apps für Server \[ 2008-Desktop-Apps \|\]<br/>                              |
| Header<br/>                   | <dl> <dt>Wmcontainer.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Alphabetische Liste Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[ASF-Splitter](asf-splitter.md)
</dt> <dt>

[Beispielattribute](sample-attributes.md)
</dt> <dt>

[Medienbeispiele](media-samples.md)
</dt> </dl>

 

 




