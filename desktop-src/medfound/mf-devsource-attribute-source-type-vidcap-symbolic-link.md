---
description: Enthält die symbolische Verknüpfung für einen Videoaufnahmetreiber.
ms.assetid: 3d256dec-ec8c-4c62-883b-e2c292fd90eb
title: MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_SYMBOLIC_LINK -Attribut (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1dd3b69899eb9df1973cb13611a822139ffda0e744c84137ff9d6094ed4a962d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104946"
---
# <a name="mf_devsource_attribute_source_type_vidcap_symbolic_link-attribute"></a>MF \_ \_ DEVSOURCE-ATTRIBUT \_ \_ QUELLTYP \_ VIDCAP SYMBOLIC \_ \_ LINK-Attribut

Enthält die symbolische Verknüpfung für einen Videoaufnahmetreiber.

## <a name="data-type"></a>Datentyp

**Wchar\***

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut zu erhalten, rufen [**Sie DEN ATTRIBUTEAttributes::GetString auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)

Rufen Sie ZUM Festlegen dieses [**Attributs DEN WERTATTRIBUTEs::SetString auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)

## <a name="remarks"></a>Hinweise

Verwenden Sie dieses Attribut als Eingabe für die [**MFCreateDeviceSourceActivate-Funktion.**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate)

Darüber hinaus wird dieses Attribut für die Aktivierungsobjekte festgelegt, die von den folgenden Funktionen zurückgegeben werden:

-   [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate)
-   [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)

Die symbolische Verknüpfung sollte als nicht transparente Zeichenfolge betrachtet werden. Der für Menschen lesbare Anzeigename für ein Gerät ist im [MF \_ DEVSOURCE \_ ATTRIBUTE FRIENDLY \_ \_ NAME-Attribut](mf-devsource-attribute-friendly-name.md) enthalten.

Das MF DEVSOURCE ATTRIBUTE SOURCE TYPE VIDCAP SYMBOLIC LINK-Attribut kann als Wert des DevicePath-Arguments der \_ \_ \_ \_ \_ \_ \_ [**SetupDiOpenDeviceInterface-Funktion übergeben**](/windows/win32/api/setupapi/nf-setupapi-setupdiopendeviceinterfacea) werden.

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                            |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Alphabetische Liste Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Audio-/Videoaufzeichnung](audio-video-capture.md)
</dt> <dt>

[Erfassen von Geräteattributen](capture-device-attributes.md)
</dt> </dl>

 

 
