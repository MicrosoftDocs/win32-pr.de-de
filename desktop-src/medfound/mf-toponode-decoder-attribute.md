---
description: Gibt an, ob ein zugrunde liegendes Topologieknotenobjekt ein Decoder ist.
ms.assetid: b6d576dc-b12f-49bf-b938-db2c629df400
title: MF_TOPONODE_DECODER-Attribut (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f8946e9de4131ce62a7ab76119b4a409cea03b1d05000a5c28c3cbab4bdcf3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117875184"
---
# <a name="mf_toponode_decoder-attribute"></a>MF \_ TOPONODE \_ DECODER-Attribut

Gibt an, ob das zugrunde liegende Objekt eines Topologieknotens ein Decoder ist.

## <a name="data-type"></a>Datentyp

**UINT32**

Als boolescher Wert behandeln.

## <a name="remarks"></a>Hinweise

Dieses Attribut gilt für alle Knotentypen.

Wenn der Wert dieses Attributs ungleich 0 (null) ist, ist das zugrunde liegende Objekt des Knotens ein Decoder.

Das Topologieladeprogramm legt dieses Attribut beim Erstellen eines Decoderknotens fest. Eine Anwendung sollte dieses Attribut festlegen, wenn die Anwendung der Topologie manuell einen Decoder hinzufügt.

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**ATTRIBUTEAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**DENKattribute::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**TOPOLOGYNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[Topologieknotenattribute](topology-node-attributes.md)
</dt> </dl>

 

 




