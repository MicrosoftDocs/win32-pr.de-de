---
description: Identifiziert die Komponente, die ein Aufzeichnungs Ereignis generiert hat.
ms.assetid: DCCF3054-AF14-44C7-84C0-B03E35B5D90A
title: MF_CAPTURE_ENGINE_EVENT_GENERATOR_GUID-Attribut (MF. Engine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb9a5068db357523a626404910fb7d752ea0b621
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349039"
---
# <a name="mf_capture_engine_event_generator_guid-attribute"></a>\_ \_ \_ \_ \_ GUID-Attribut des MF-Erfassungs Moduls

Identifiziert die Komponente, die ein Aufzeichnungs Ereignis generiert hat.

## <a name="data-type"></a>Datentyp

**GUID**

## <a name="remarks"></a>Bemerkungen

Dieses Attribut wird für einige Ereignisse der Aufzeichnungs-Engine angezeigt. Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetGuid**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid) für das Ereignis Objekt. Das Ereignis Objekt wird über die [**imfcaptureengineoneventcallback:: OnEvent**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengineoneventcallback-onevent) -Methode an die Anwendung übermittelt.

Der Wert ist ein Schnittstellen Bezeichner für die Komponente, die das Ereignis generiert hat. Beispielsweise gibt der Wert **IID \_ IMF capturepreviewsink** die Vorschau Senke ([**IMF capturepreviewsink**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturepreviewsink)) an. Nicht jedes Aufzeichnungs Ereignis enthält dieses Attribut.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                   |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                         |
| Header<br/>                   | <dl> <dt>"MF"-Engine. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attribute der Aufzeichnungs-Engine](capture-engine-attributes.md)
</dt> <dt>

[**IMF captureengine:: Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




