---
description: Gibt die Endpunkt-ID für ein audioerfassungs-Gerät an.
ms.assetid: a0d8b54b-7a05-4307-a756-a34bb22f1afd
title: MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_AUDCAP_ENDPOINT_ID-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a1448dc753a8e3b8221fa040309d3f5b60c4879
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372283"
---
# <a name="mf_devsource_attribute_source_type_audcap_endpoint_id-attribute"></a>MF \_ devsource \_ - \_ Attribut \_ Quelltyp " \_ audcap \_ EndPoint \_ ID"-Attribut

Gibt die Endpunkt-ID für ein audioerfassungs-Gerät an.

## <a name="data-type"></a>Datentyp

**WCHAR\***

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).

Um dieses Attribut festzulegen, müssen Sie [**imfattributes:: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)aufrufen.

## <a name="remarks"></a>Bemerkungen

Der Wert des-Attributs ist eine Endpunkt-ID. Dieses Attribut wird mit den folgenden Funktionen verwendet:

-   Sie kann als Eingabe für die Funktionen [**mfkreatedevicesource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) und [**mfkreatedevicesourceaktivierungs**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) verwendet werden. In diesem Kontext gibt das-Attribut das audioerfassungs Gerät für die-Funktion an. Sie können die Endpunkt-ID für ein bestimmtes Gerät abrufen, indem Sie die [**immdevice:: GetId**](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getid) -Methode aufrufen. Weitere Informationen finden Sie in der Dokumentation zur kernton-API.
-   Wenn die [**mfenumtovicesources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) -Funktion Audiogeräte auflistet, enthalten die zurückgegebenen Aktivierungs Objekte dieses Attribut. Das-Attribut wird vom Aktivierungs Objekt intern verwendet, wenn es die Medienquelle erstellt.

Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Mspdl. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Audio-/Videoaufzeichnung](audio-video-capture.md)
</dt> <dt>

[Geräte Attribute erfassen](capture-device-attributes.md)
</dt> </dl>

 

 
