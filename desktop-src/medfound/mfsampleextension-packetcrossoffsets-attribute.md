---
description: Gibt die Offsets zu den Nutz Last Grenzen in einem Frame für geschützte Beispiele an.
ms.assetid: 8aa25afd-efa8-4fe0-92d4-8432f9d633c9
title: MFSampleExtension_PacketCrossOffsets-Attribut (wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d416f41fef9caab3d73c2bdd015d345452ccbd69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347861"
---
# <a name="mfsampleextension_packetcrossoffsets-attribute"></a>MF Sample Extension \_ packetcrossoffsets-Attribut

Gibt die Offsets zu den Nutz Last Grenzen in einem Frame für geschützte Beispiele an.

## <a name="data-type"></a>Datentyp

Bytearray

## <a name="getset"></a>Abrufen/Festlegen

Zum Abrufen dieses Attributs müssen Sie [**imfattributes:: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)aufrufen.

Um dieses Attribut festzulegen, müssen Sie [**imfattributes:: setBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)aufrufen.

## <a name="applies-to"></a>Gilt für:

[**IMF Sample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>Bemerkungen

Dieses Attribut gilt für Medien Beispiele, die von Windows Media Digital Rights Management (DRM) geschützt werden. Der Wert des-Attributs ist ein Array von **DWORD** s. Jeder Eintrag im Array ist der Offset einer Nutz Last Grenze relativ zum Anfang des Frames. Diese Werte können von einer Anwendung beim Entschlüsseln und erneuten Erstellen der Frames verwendet werden.

Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista \[ -Desktop-Apps \| UWP-apps\]<br/>                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]<br/>                              |
| Header<br/>                   | <dl> <dt>Wmcontainer. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[ASF-Splitter](asf-splitter.md)
</dt> <dt>

[Beispiel Attribute](sample-attributes.md)
</dt> <dt>

[Medien Beispiele](media-samples.md)
</dt> </dl>

 

 




