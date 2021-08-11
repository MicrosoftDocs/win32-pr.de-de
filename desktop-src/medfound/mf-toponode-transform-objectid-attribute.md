---
description: Der Klassenbezeichner (CLSID) der Media Foundation Transformation (MFT), die diesem Topologieknoten zugeordnet ist.
ms.assetid: 6aa6e649-d23d-4d8d-be80-2b8814b07a57
title: MF_TOPONODE_TRANSFORM_OBJECTID -Attribut (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9b5013bc43f07e08e1a2c26530e9325595e62666986516029ef9d76e2c72ffe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118244314"
---
# <a name="mf_toponode_transform_objectid-attribute"></a>MF \_ TOPONODE \_ TRANSFORM \_ OBJECTID-Attribut

Der Klassenbezeichner (CLSID) der Media Foundation Transformation (MFT), die diesem Topologieknoten zugeordnet ist.

## <a name="data-type"></a>Datentyp

**GUID**

## <a name="remarks"></a>Hinweise

Dieses Attribut gilt für Transformationsknoten (**MF \_ TOPOLOGY \_ TRANSFORM \_ NODE**).

Anwendungen können dieses Attribut verwenden, um einen Transfrom-Knoten zu initialisieren. Wenn Sie dieses Attribut festlegen, müssen Sie NICHT MIT einem Zeiger auf ein MFT- oder Aktivierungsobjekt [**DIE TOPOLOGIENode::SetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) aufrufen. Wenn Sie dagegen **SetObject** aufrufen, müssen Sie dieses Attribut nicht festlegen. Weitere Informationen finden Sie unter [Erstellen von Topologien.](creating-topologies.md)

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

[**ATTRIBUTEs::GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[**ATTRIBUTEs::SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[**TOPOLOGIENode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[Media Foundation Attribute](media-foundation-attributes.md)
</dt> <dt>

[Erstellen von Topologien](creating-topologies.md)
</dt> <dt>

[Topologieknotenattribute](topology-node-attributes.md)
</dt> </dl>

 

 




