---
description: Gibt an, ob die Erfassungs-Engine Videos, aber keine Audiodaten erfasst.
ms.assetid: B0B7A7F2-02F9-46A6-954F-D6E9C3B73A29
title: MF_CAPTURE_ENGINE_USE_VIDEO_DEVICE_ONLY -Attribut (Mfcaptureengine.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd8dd903c4c56b52bf82a97b28edd5148e3c091788376f1ef460047b7f609b51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973969"
---
# <a name="mf_capture_engine_use_video_device_only-attribute"></a>MF \_ CAPTURE ENGINE USE VIDEO DEVICE \_ \_ \_ \_ \_ ONLY-Attribut

Gibt an, ob die Erfassungs-Engine Videos, aber keine Audiodaten erfasst.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Hinweise

Wenn dieses Attribut **TRUE ist,** wählt die Erfassungs-Engine kein Audioaufnahmegerät aus oder verwendet es nicht. Legen Sie dieses Attribut auf **TRUE** fest, wenn Sie Videos ohne Audio erfassen möchten. Der Standardwert ist **FALSE**.

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

 

 




