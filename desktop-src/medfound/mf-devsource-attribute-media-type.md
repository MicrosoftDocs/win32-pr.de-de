---
description: Gibt das Ausgabeformat eines Geräts an.
ms.assetid: 33a1b546-ece2-44ef-a1c0-5579c32be0bc
title: MF_DEVSOURCE_ATTRIBUTE_MEDIA_TYPE-Attribut (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb4685f419658ecf77782a4cef770fd205119bb6cfd95523edb7fbbe001fd700
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105036"
---
# <a name="mf_devsource_attribute_media_type-attribute"></a>MF \_ DEVSOURCE \_ ATTRIBUTE MEDIA \_ \_ TYPE-Attribut

Gibt das Ausgabeformat eines Geräts an.

## <a name="data-type"></a>Datentyp

**[**MFT \_ REGISTER \_ TYPE \_ INFO**](/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info)** stored as **\[ \] BYTE**

## <a name="getset"></a>Abrufen/Festlegen

Rufen Sie ZUM Abrufen dieses [**Attributs DIE ATTRIBUTEAttributes::GetBlob auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)

Rufen Sie ZUM Festlegen dieses [**Attributs DIE ATTRIBUTEAttributes::SetBlob auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)

## <a name="remarks"></a>Hinweise

Dieses Attribut enthält ein Paar von GUIDs: einen Haupttyp und einen Untertyp. Diese GUIDs beschreiben das Standardausgabeformat des Geräts. Das Gerät unterstützt möglicherweise zusätzliche Ausgabeformate.

Wenn beispielsweise ein Videoaufnahmegerät RGB-32-Videos ausgibt, ist der Wert dieses Attributs `{ MFMediaType_Video, MFVideoFormat_RGB32 }` .

Dieses Attribut ist ein Hinweis auf die Anwendung. Um das genaue Ausgabeformat zu erhalten, erstellen Sie die Medienquelle für das Gerät und abrufen den Präsentationsdeskriptor der Medienquelle.

Dieses Attribut wird für die Aktivierungsobjekte festgelegt, die von den folgenden Funktionen zurückgegeben werden:

-   [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate)
-   [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                            |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Audio-/Videoaufzeichnung](audio-video-capture.md)
</dt> <dt>

[Erfassen von Geräteattributen](capture-device-attributes.md)
</dt> </dl>

 

 




