---
description: GUID des Haupt Typs für einen Medientyp.
ms.assetid: b88b5fcf-8025-4638-930d-9fc5cf0ec8a3
title: MF_MT_MAJOR_TYPE-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98c4cc02df4f89e261605c91b71ac1c80ba38b9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348199"
---
# <a name="mf_mt_major_type-attribute"></a>\_ \_ Haupt \_ Attribut von MF MT

GUID des Haupt Typs für einen Medientyp.

## <a name="data-type"></a>Datentyp

**GUID**

## <a name="remarks"></a>Bemerkungen

Der Haupttyp definiert die Gesamtkategorie der Mediendaten. Zu den Haupttypen gehören Videos, Audiodateien, Skripts usw. Eine Liste möglicher Werte finden Sie unter [Hauptmedien Typen](media-type-guids.md).

Eine alternative Möglichkeit zum Abrufen dieses Attributs ist das Aufrufen von [**imfmediatype:: getmajortype**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getmajortype).

Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista \[ -Desktop-Apps \| UWP-apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**Imfattributes:: GetGuid**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[**Imfattributes:: SetGuid**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[**IMF MediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Medientyp Attribute](media-type-attributes.md)
</dt> </dl>

 

 




