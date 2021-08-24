---
description: Legt den Microsoft DirectX Graphic Infrastructure (DXGI) Geräte-Manager der Medien-Engine fest.
ms.assetid: CB952492-0ACF-4501-BD8B-133E26FCE8F7
title: MF_MEDIA_ENGINE_DXGI_MANAGER -Attribut (Mfmediaengine.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c454041f83a58cdb5b3c1e340d63908386546090eb52811e0c876e5d8bed0bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119723053"
---
# <a name="mf_media_engine_dxgi_manager-attribute"></a>DXGI \_ MANAGER-Attribut der MF-MEDIEN-ENGINE \_ \_ \_

Legt den Microsoft DirectX Graphic Infrastructure (DXGI) Geräte-Manager der Medien-Engine fest.

## <a name="data-type"></a>Datentyp

**DURCHDXGIDeviceManager \* *_ gespeichert als _* IUnknown\***

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut zu erhalten, rufen [**Sie DANNATTRIBUTEs::GetUnknown auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)

Rufen Sie ZUM Festlegen dieses [**Attributs DEN WERTATTRIBUTEs::SetUnknown auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)

## <a name="remarks"></a>Hinweise

Der Wert dieses Attributs ist ein Zeiger auf die [**BENUTZERDEFINIERTEGIDeviceManager-Schnittstelle.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager)

Im Frameservermodus ermöglicht dieses Attribut der Medien-Engine die Verwendung der Hardwarebeschleunigung für die Videodecodierung und Videoverarbeitung. Wenn das Attribut nicht festgelegt ist, verwendet die Medien-Engine Softwaredecodierung und -verarbeitung.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Desktop-Apps \| UWP-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Desktop-Apps \| UWP-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Mfmediaengine.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**ÄNDERMediaEngineClassFactory::CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance)
</dt> </dl>

 

 




