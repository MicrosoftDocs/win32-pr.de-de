---
description: Enthält den symbolischen Link für einen Video Erfassungs Treiber.
ms.assetid: 3d256dec-ec8c-4c62-883b-e2c292fd90eb
title: MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_SYMBOLIC_LINK-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48e1c854ee070713462676482cc04690c2bdde2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130721"
---
# <a name="mf_devsource_attribute_source_type_vidcap_symbolic_link-attribute"></a>MF \_ devsource \_ - \_ Attribut \_ Quelltyp \_ VidCap \_ symbolischen \_ Link Attribut

Enthält den symbolischen Link für einen Video Erfassungs Treiber.

## <a name="data-type"></a>Datentyp

**WCHAR \** _

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut abzurufen, nennen Sie [_ *imfattributes:: GetString* *](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).

Um dieses Attribut festzulegen, müssen Sie [**imfattributes:: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)aufrufen.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie dieses Attribut als Eingabe für die [**mfkreatedevicesourceaktivierungs**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) -Funktion.

Außerdem wird dieses Attribut für die Aktivierungs Objekte festgelegt, die von den folgenden Funktionen zurückgegeben werden:

-   [**MF | atedevicesourceaktivierungs**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate)
-   [**Mfenumschlag**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)

Die symbolische Verknüpfung sollte als nicht transparente Zeichenfolge betrachtet werden. Der lesbare Anzeige Name für ein Gerät ist in dem Attribut "Anzeige Name" des [MF- \_ devsource- \_ Attributs \_ \_ ](mf-devsource-attribute-friendly-name.md) enthalten.

Das Attribut "MF \_ devsource \_ Attribute \_ Source \_ Type \_ VidCap \_ symbolischen \_ Link" kann als Wert des DevicePath-Arguments der [**setupdiopendeviceinterface**](/windows/win32/api/setupapi/nf-setupapi-setupdiopendeviceinterfacea) -Funktion übergeben werden.

Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                            |
| Header<br/>                   | <dl> <dt>Mspdl. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Audio-/Videoaufzeichnung](audio-video-capture.md)
</dt> <dt>

[Geräte Attribute erfassen](capture-device-attributes.md)
</dt> </dl>

 

 
