---
description: Gibt die maximale Anzahl von Frames an, die die Videoaufnahmequelle puffert.
ms.assetid: af30606b-f1a0-4fbf-a831-05ed891f5d53
title: MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_MAX_BUFFERS -Attribut (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba50ad5489d08ba0fc986d56bef8d57c547fa0146a3bbb58290bca43009cc5af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973819"
---
# <a name="mf_devsource_attribute_source_type_vidcap_max_buffers-attribute"></a>MF \_ \_ DEVSOURCE-ATTRIBUT \_ \_ QUELLTYP \_ VIDCAP \_ MAX \_ BUFFERS-Attribut

Gibt die maximale Anzahl von Frames an, die die Videoaufnahmequelle puffert.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut zu erhalten, rufen [**Sie DIE ATTRIBUTEs::GetUINT32 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)

Rufen Sie ZUM Festlegen dieses [**Attributs DIE ATTRIBUTEs::SetUINT32 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)

## <a name="remarks"></a>Hinweise

Standardmäßig puffert die Videoaufnahmequelle maximal einen Frame gleichzeitig. Sie können das Pufferlimit erhöhen, indem Sie dieses Attribut festlegen.

Die richtige Methode zum Festlegen dieses Attributs hängt von der Funktion ab, die zum Erstellen der Medienquelle verwendet wird:

-   [**MFCreateDeviceSource:**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource)Legen Sie das Attribut über den *pAttributes-Parameter* der Funktion fest.
-   [**MFCreateDeviceSourceActivate: Legen**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate)Sie das Attribut über den *pAttributes-Parameter* der Funktion fest.
-   [**MFEnumDeviceSources:**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)Legen Sie das -Attribut für den VON der Funktion zurückgegebenen [**ATTRIBUTActivate-Zeiger**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) fest. Legen Sie das -Attribut fest, bevor [**SIE DENKActivate::ActivateObject aufrufen.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject)

Das -Attribut gilt nur für Videoaufnahmegeräte.

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                            |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Audio-/Videoaufzeichnung](audio-video-capture.md)
</dt> <dt>

[Erfassen von Geräteattributen](capture-device-attributes.md)
</dt> </dl>

 

 




