---
description: Gibt an, dass der MFT-Encoder beim Streaming das Empfangen von meencodingparameter-Ereignissen unterstützt.
ms.assetid: 8DE04537-641C-4154-9C7F-A7D025CA4C39
title: MFT_ENCODER_SUPPORTS_CONFIG_EVENT-Attribut (MF Transform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c49c688abc4d372a463115c369e4616babe3bcaa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356640"
---
# <a name="mft_encoder_supports_config_event-attribute"></a>Der MFT- \_ Encoder \_ unterstützt das \_ config- \_ Ereignis Attribut

Gibt an, dass der MFT-Encoder beim Streaming das Empfangen von [meencodingparameter](meencodingparameters.md) -Ereignissen unterstützt.

## <a name="data-type"></a>Datentyp

**Bool** gespeichert als **UInt32**

## <a name="remarks"></a>Bemerkungen

Gesendet vom MFT-Encoder durch [**imftransform::P rocesabvent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8.1 \[ Desktop-Apps \| UWP-apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 R2 \[ -Desktop-Apps \| UWP-apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>"MF Transform. h"</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>"MF Transform. idl"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMF Transform::P rocesabvent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent)
</dt> </dl>

 

 




