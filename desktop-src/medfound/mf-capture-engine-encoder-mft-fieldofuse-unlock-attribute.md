---
description: Ermöglicht der Erfassungs-Engine die Verwendung eines Encoders mit Einschränkungen für das Feld.
ms.assetid: 28421875-9629-4F14-8159-2D86012F517F
title: MF_CAPTURE_ENGINE_ENCODER_MFT_FIELDOFUSE_UNLOCK_Attribute-Attribut (MF. Engine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b29a9466162ff5551ee155343800d938276823ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215156"
---
# <a name="mf_capture_engine_encoder_mft_fieldofuse_unlock_attribute-attribute"></a>MF- \_ Erfassungs- \_ Engine- \_ Encoder \_ MFT \_ fieldofuse \_ Unlock Attribute- \_ Attribut

Ermöglicht der Erfassungs-Engine die Verwendung eines Encoders mit Einschränkungen für das Feld.

## <a name="data-type"></a>Datentyp

**IUnknown \** _

## <a name="remarks"></a>Bemerkungen

Der Wert dieses Attributs ist ein Zeiger auf die [_ *imffieldofusemftunlock* *](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) -Schnittstelle, die vom Aufrufer implementiert wird. Es wird erwartet, dass die Implementierung dieser Schnittstelle des Aufrufers einen Hand Shake mit dem Encoder durchführt, wie im [Feld Use Restrictions](field-of-use-restrictions.md)beschrieben. Microsoft Media Foundation definiert nicht den Handshake – in der Regel würde es sich um eine Art kryptografieaustausch handeln.

Intern legt die Aufzeichnungs-Engine den [**imffieldofusemftunlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) -Zeiger auf den Encoder fest, indem er das [MFT \_ fieldofuse \_ Unlock \_ Attribute](mft-fieldofuse-unlock-attribute.md) -Attribut des Encoders festlegt.

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

 

 




