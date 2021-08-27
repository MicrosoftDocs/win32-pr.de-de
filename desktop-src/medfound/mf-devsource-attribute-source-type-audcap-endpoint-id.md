---
description: Gibt die Endpunkt-ID für ein Audioaufnahmegerät an.
ms.assetid: a0d8b54b-7a05-4307-a756-a34bb22f1afd
title: MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_AUDCAP_ENDPOINT_ID -Attribut (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6baafd2aa1bdfc3f4959b877963faff5df9aabe57c672555edb98f4cded8b1ae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113950"
---
# <a name="mf_devsource_attribute_source_type_audcap_endpoint_id-attribute"></a>MF \_ \_ DEVSOURCE-ATTRIBUT \_ \_ QUELLTYP \_ AUDCAP \_ ENDPOINT \_ ID-Attribut

Gibt die Endpunkt-ID für ein Audioaufnahmegerät an.

## <a name="data-type"></a>Datentyp

**Wchar\***

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut zu erhalten, rufen [**Sie DEN ATTRIBUTEAttributes::GetString auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)

Rufen Sie ZUM Festlegen dieses [**Attributs DEN WERTATTRIBUTEs::SetString auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)

## <a name="remarks"></a>Hinweise

Der Wert des Attributs ist eine Endpunkt-ID. Dieses Attribut wird mit den folgenden Funktionen verwendet:

-   Sie kann als Eingabe für die [**Funktionen MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) und [**MFCreateDeviceSourceActivate verwendet**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) werden. In diesem Kontext gibt das -Attribut das Audioaufnahmegerät für die Funktion an. Sie können die Endpunkt-ID für ein bestimmtes Gerät durch Aufrufen der [**IMMDevice::GetId-Methode**](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getid) erhalten. Weitere Informationen finden Sie in der Core Audio API-Dokumentation.
-   Wenn die [**MFEnumDeviceSources-Funktion**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) Audiogeräte aufzählt, enthalten die zurückgegebenen Aktivierungsobjekte dieses Attribut. Das -Attribut wird intern vom Aktivierungsobjekt verwendet, wenn es die Medienquelle erstellt.

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Audio-/Videoaufzeichnung](audio-video-capture.md)
</dt> <dt>

[Erfassen von Geräteattributen](capture-device-attributes.md)
</dt> </dl>

 

 
