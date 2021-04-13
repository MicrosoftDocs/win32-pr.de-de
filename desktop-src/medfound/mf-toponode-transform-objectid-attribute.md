---
description: Der Klassen Bezeichner (CLSID) der dem topologieknoten zugeordneten Media Foundation Transformation (MFT).
ms.assetid: 6aa6e649-d23d-4d8d-be80-2b8814b07a57
title: MF_TOPONODE_TRANSFORM_OBJECTID-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ea96e09a75374bfe048b531492fc913f764d364
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527419"
---
# <a name="mf_toponode_transform_objectid-attribute"></a>MF \_ toponode \_ Transform \_ objectID-Attribut

Der Klassen Bezeichner (CLSID) der dem topologieknoten zugeordneten Media Foundation Transformation (MFT).

## <a name="data-type"></a>Datentyp

**GUID**

## <a name="remarks"></a>Bemerkungen

Dieses Attribut gilt für Transformations Knoten (**MF- \_ topologietransformations- \_ \_ Knoten**).

Anwendungen können dieses Attribut verwenden, um einen transfrom-Knoten zu initialisieren. Wenn Sie dieses Attribut festlegen, müssen Sie [**imftopologynode:: SetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) nicht mit einem Zeiger auf ein MFT-oder Aktivierungs Objekt aufrufen. Wenn Sie hingegen **SetObject** aufrufen, muss dieses Attribut nicht festgelegt werden. Weitere Informationen finden Sie unter [Erstellen von Topologien](creating-topologies.md).

Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mspdl. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**Imfattributes:: GetGuid**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[**Imfattributes:: SetGuid**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[**Imftopologynode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[Media Foundation Attribute](media-foundation-attributes.md)
</dt> <dt>

[Erstellen von Topologien](creating-topologies.md)
</dt> <dt>

[Topologieknotenattribute](topology-node-attributes.md)
</dt> </dl>

 

 




