---
description: Gibt an, ob der Quell Leser eine DirectX-Videobeschleunigung (DXVA) im Video Decoder ermöglicht.
ms.assetid: ec539038-3fd3-41b7-a0e6-e75e3f2828a7
title: MF_SOURCE_READER_DISABLE_DXVA-Attribut (mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9362f067d1d6ceae426e9ee6530e08b95837595f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348738"
---
# <a name="mf_source_reader_disable_dxva-attribute"></a>MF- \_ Quell \_ Leser \_ deaktivierte \_ DXVA-Attribute

Gibt an, ob der [Quell Leser](source-reader.md) eine DirectX-Videobeschleunigung (DXVA) im Video Decoder ermöglicht.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Bemerkungen

Dieses Attribut gilt, wenn die folgenden Bedingungen zutreffen:

-   Der Quell Leser decodiert einen Videostream.
-   Der Video Decoder unterstützt die DXVA-Decodierung.
-   Die Anwendung verwendet das [ \_ \_ \_ D3D \_ Manager](mf-source-reader-d3d-manager.md) -Attribut des MF-Quell Readers, um die [Direct3D-Device Manager](direct3d-device-manager.md) für den Quell Leser festzulegen.

Dieses Attribut ermöglicht es der Anwendung, DXVA zu deaktivieren, während die Decodierung an Direct3D-Oberflächen noch nicht

Standardmäßig verwendet der Quell Reader den [Direct3D-Device Manager](direct3d-device-manager.md) aus zwei Gründen:

-   , Um die DXVA-Decodierung im Video Decoder zu aktivieren.
-   , Um Direct3D-Oberflächen für die Videobeispiele zuzuordnen.

Wenn der Wert des MF- \_ Quell \_ Readers \_ \_ DXVA-Attributs deaktiviert ist, deaktiviert der Quell Leser die DXVA-Decodierung, obwohl er weiterhin den Direct3D- [Device Manager](direct3d-device-manager.md) verwendet, um Direct3D-Oberflächen zuzuordnen.

Wenn das [ \_ \_ \_ D3D \_ Manager](mf-source-reader-d3d-manager.md) -Attribut des MF-Quell Readers nicht festgelegt ist, \_ wird das \_ \_ DXVA-Attribut des MF-Quell Readers deaktiviert \_ .

Der Standardwert dieses Attributs ist **false**. Dies bedeutet, dass die DXVA-Decodierung aktiviert ist, wenn verfügbar.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ -Desktop-Apps \| UWP-apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2 \[ -Desktop-Apps \| UWP-apps\]<br/>                           |
| Header<br/>                   | <dl> <dt>"Mfreadwrite. h"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Quell Leser](source-reader.md)
</dt> <dt>

[Attribute des Quell Readers](source-reader-attributes.md)
</dt> </dl>

 

 




