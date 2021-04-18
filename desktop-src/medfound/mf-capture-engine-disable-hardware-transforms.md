---
description: Deaktiviert die Verwendung von hardwarebasierten Media Foundation Transformationen (MFTs) in der Erfassungs-Engine.
ms.assetid: 1C687FEC-276D-4759-A3B8-9A2A31CB0DE1
title: MF_CAPTURE_ENGINE_DISABLE_HARDWARE_TRANSFORMS-Attribut (MF. Engine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9631804c61fab953793c3f89d1eac3dc2e8f4dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343403"
---
# <a name="mf_capture_engine_disable_hardware_transforms-attribute"></a>MF \_ Capture- \_ Engine-Attribut " \_ \_ Hardware \_ Transformationen deaktivieren"

Deaktiviert die Verwendung von hardwarebasierten Media Foundation Transformationen (MFTs) in der Erfassungs-Engine.

## <a name="data-type"></a>Datentyp

**Bool** gespeichert als **UInt32**

## <a name="remarks"></a>Bemerkungen

Standardmäßig verwendet die Aufzeichnungs-Engine Hardware Decoder oder Encoder. Um die Verwendung von Hardware-MFTs zu deaktivieren, legen Sie dieses Attribut auf " **true** " fest, wenn Sie die Aufzeichnungs-Engine erstellen.

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

 

 




