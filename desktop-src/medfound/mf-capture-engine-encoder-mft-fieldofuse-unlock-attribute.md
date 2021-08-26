---
description: Ermöglicht der Erfassungs-Engine die Verwendung eines Encoders, der Einschränkungen für die Verwendungsfelder aufnimmt.
ms.assetid: 28421875-9629-4F14-8159-2D86012F517F
title: MF_CAPTURE_ENGINE_ENCODER_MFT_FIELDOFUSE_UNLOCK_Attribute Attribut (Mfcaptureengine.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32f2fb9d85c68adbc726fa4b36f2ea960a33e68c4dff836fac0370c8e9e4e3a1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060820"
---
# <a name="mf_capture_engine_encoder_mft_fieldofuse_unlock_attribute-attribute"></a>MF \_ CAPTURE ENGINE ENCODER \_ \_ \_ MFT \_ FIELDOFUSE \_ \_ UNLOCK-Attribut

Ermöglicht der Erfassungs-Engine die Verwendung eines Encoders, der Einschränkungen für die Verwendungsfelder aufnimmt.

## <a name="data-type"></a>Datentyp

**IUnknown\***

## <a name="remarks"></a>Hinweise

Der Wert dieses Attributs ist ein Zeiger auf die VOM Aufrufer [**implementierte POINTERFieldOfUseMFTUnlock-Schnittstelle.**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) Es wird erwartet, dass die Implementierung dieser Schnittstelle durch den Aufrufer einen Handshake mit dem Encoder ausführt, wie unter [Verwendungseinschränkungen](field-of-use-restrictions.md)beschrieben. Microsoft Media Foundation definiert den Handshake nicht– in der Regel umfasst er eine Art kryptografischen Austausch.

Intern legt die Erfassungs-Engine den [**POINTERFieldOfUseMFTUnlock-Zeiger**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) auf dem Encoder fest, indem das [MFT \_ FIELDOFUSE \_ \_ UNLOCK-Attribut](mft-fieldofuse-unlock-attribute.md) des Encoders festgelegt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                   |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                         |
| Header<br/>                   | <dl> <dt>Mfcaptureengine.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attribute der Erfassungs-Engine](capture-engine-attributes.md)
</dt> <dt>

[**ADRPaturEngine::Initialisieren**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




