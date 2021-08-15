---
description: Identifiziert die Komponente, die ein Erfassungsereignis generiert hat.
ms.assetid: DCCF3054-AF14-44C7-84C0-B03E35B5D90A
title: MF_CAPTURE_ENGINE_EVENT_GENERATOR_GUID -Attribut (Mfcaptureengine.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88efff7cea540c1fae2c14d44dd7676c4f523b562a66a4c4f4bc4dffea59d5e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118474468"
---
# <a name="mf_capture_engine_event_generator_guid-attribute"></a>GUID-Attribut des MF \_ CAPTURE \_ \_ \_ \_ ENGINE-EREIGNISGENERATORs

Identifiziert die Komponente, die ein Erfassungsereignis generiert hat.

## <a name="data-type"></a>Datentyp

**GUID**

## <a name="remarks"></a>Hinweise

Dieses Attribut wird für einige Ereignisse der Erfassungs-Engine angezeigt. Um dieses Attribut zu erhalten, rufen [**Sie DIE ATTRIBUTEs::GetGUID für das**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid) Ereignisobjekt auf. Das Ereignisobjekt wird über die [**METHODE DURCHCAPtureEngineOnEventCallback::OnEvent**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengineoneventcallback-onevent) an die Anwendung übergeben.

Der Wert ist ein Schnittstellenbezeichner für die Komponente, die das Ereignis generiert hat. Beispielsweise gibt der Wert **\_ IID-KapselungPreviewSink** die Vorschausenke an ([**VERFCapturePreviewSink**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturepreviewsink)). Nicht jedes Erfassungsereignis enthält dieses Attribut.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                   |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                         |
| Header<br/>                   | <dl> <dt>Mfcaptureengine.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Alphabetische Liste Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attribute der Erfassungs-Engine](capture-engine-attributes.md)
</dt> <dt>

[**INITIALIZECaptureEngine::Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




