---
description: Gibt an, dass der MFT-Encoder das Empfangen von MEEncodingParameter-Ereignissen während des Streamings unterstützt.
ms.assetid: 8DE04537-641C-4154-9C7F-A7D025CA4C39
title: MFT_ENCODER_SUPPORTS_CONFIG_EVENT-Attribut (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25a528da44d59077c8445616f8fe344cba5497ced8b33be75e33be71bf9b5d76
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113040"
---
# <a name="mft_encoder_supports_config_event-attribute"></a>MFT \_ ENCODER UNTERSTÜTZT DAS \_ \_ CONFIG \_ EVENT-Attribut.

Gibt an, dass der MFT-Encoder den Empfang von [MEEncodingParameter-Ereignissen](meencodingparameters.md) während des Streamings unterstützt.

## <a name="data-type"></a>Datentyp

**Bool** als **UINT32** gespeichert

## <a name="remarks"></a>Hinweise

Wird vom MFT-Encoder über [**ÜBER DIETRANSFORM::P rocessEvent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent)gesendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8.1 \|Desktop-Apps UWP-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 \[R2-Desktop-Apps \| UWP-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>Mftransform.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Mftransform.idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**ÜBERTRANSFORM::P rocessEvent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent)
</dt> </dl>

 

 




