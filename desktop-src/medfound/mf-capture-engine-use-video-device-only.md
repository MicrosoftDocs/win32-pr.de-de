---
description: Gibt an, ob die Aufzeichnungs-Engine Videos, aber keine Audiodaten erfasst.
ms.assetid: B0B7A7F2-02F9-46A6-954F-D6E9C3B73A29
title: MF_CAPTURE_ENGINE_USE_VIDEO_DEVICE_ONLY-Attribut (MF. Engine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0b687bfa7ec2f30f296dd83997f3e64ac4198fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959296"
---
# <a name="mf_capture_engine_use_video_device_only-attribute"></a>Die MF- \_ Erfassungs- \_ Engine \_ verwendet \_ \_ nur Video Geräte \_ Attribute

Gibt an, ob die Aufzeichnungs-Engine Videos, aber keine Audiodaten erfasst.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Bemerkungen

Wenn dieses Attribut **true** ist, wird von der Aufzeichnungs-Engine kein audioerfassungs-Gerät ausgewählt oder verwendet. Legen Sie dieses Attribut auf " **true** " fest, wenn Sie Video ohne Audiodaten erfassen möchten. Der Standardwert ist **FALSE**.

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

 

 




