---
description: Gibt an, wann eine Transformation geleert wird.
ms.assetid: 1e87f58f-546f-4dd4-b218-1458ff17db53
title: MF_TOPONODE_FLUSH -Attribut (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67e02c297efa68c6e6c585837675a46b729ec2382be072828059fd795d1c67a9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663880"
---
# <a name="mf_toponode_flush-attribute"></a>MF \_ TOPONODE \_ FLUSH-Attribut

Gibt an, wann eine Transformation geleert wird.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Hinweise

Dieses Attribut gilt für Transformationsknoten (**MF \_ TOPOLOGY \_ TRANSFORM \_ NODE**).

Der Wert des -Attributs ist ein Member der [**MF \_ TOPONODE \_ FLUSH \_ MODE-Enumeration.**](/windows/desktop/api/mfidl/ne-mfidl-mf_toponode_flush_mode) Wenn dieses Attribut nicht festgelegt ist, ist der Standardwert **MF \_ TOPONODE \_ FLUSH \_ ALWAYS**.

Das Leeren erfolgt durch Aufrufen [**von DURCHSICHTTransform::P rocessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) für die Transformation mit der [**MFT \_ MESSAGE COMMAND \_ \_ FLUSH-Nachricht.**](mft-message-command-flush.md) Weitere Informationen finden Sie unter [**MFT \_ MESSAGE \_ TYPE-Enumeration.**](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**ATTRIBUTEs::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**ATTRIBUTEs::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**TOPOLOGIENode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[Topologieknotenattribute](topology-node-attributes.md)
</dt> </dl>

 

 




