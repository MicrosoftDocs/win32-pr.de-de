---
description: Gibt an, ob die Aufzeichnungs-Engine Audiodaten erfasst, aber kein Video.
ms.assetid: 0A905D55-CEE5-44FC-97A5-9474872D5724
title: MF_CAPTURE_ENGINE_USE_AUDIO_DEVICE_ONLY-Attribut (MF. Engine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f02e0b8f1002bcfff12f8a2bea93612456b6072
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959050"
---
# <a name="mf_capture_engine_use_audio_device_only-attribute"></a>Die \_ MF \_ -Erfassungs \_ -Engine verwendet \_ \_ nur Audiogeräte \_ Attribute

Gibt an, ob die Aufzeichnungs-Engine Audiodaten erfasst, aber kein Video.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Bemerkungen

Wenn dieses Attribut **true** ist, wird von der Aufzeichnungs-Engine kein Video Erfassungsgerät ausgewählt oder verwendet. Legen Sie dieses Attribut auf " **true** " fest, wenn Sie Audiodaten ohne Video erfassen möchten. Der Standardwert ist **FALSE**.

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

 

 




