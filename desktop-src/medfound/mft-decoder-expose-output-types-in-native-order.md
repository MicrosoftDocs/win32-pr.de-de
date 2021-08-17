---
description: Gibt an, ob ein Decoder IYUV/I420-Ausgabetypen (für die Transcodierung geeignet) vor anderen Formaten verfügbar macht.
ms.assetid: 8505CFA1-210A-4DA8-B92A-FCE62F0310E5
title: MFT_DECODER_EXPOSE_OUTPUT_TYPES_IN_NATIVE_ORDER-Attribut (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46b91492054215aee5a63dbcf0adf300d74933a0859a2d71256e7e4352deba9e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117872339"
---
# <a name="mft_decoder_expose_output_types_in_native_order-attribute"></a>\_MFT-DECODER \_ MACHT \_ \_ AUSGABETYPEN \_ IM \_ \_ NATIVEN ORDER-Attribut VERFÜGBAR

Gibt an, ob ein Decoder IYUV/I420-Ausgabetypen (für die Transcodierung geeignet) vor anderen Formaten verfügbar macht.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Hinweise

Dieses Attribut ist ein Hinweis für den Decoder, seine Liste der Ausgabetypen in einer bestimmten Reihenfolge anzuordnen, je nach beabsichtigter Verwendung, entweder Wiedergabe oder Transcodierung.

Für die meisten Codierungsformate (H.264, MPEG-2, WMV) unterstützen die Videodecoder in Microsoft Media Foundation mehrere gängige YUV-Ausgaben, einschließlich NV12, YV12, YUY2, IYUV und I420. Der Decoder bietet eine geordnete Liste von Ausgabetypen über die [**ZUGEHÖRIGETRANSFORM::GetOutputAvailableType-Methode.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype)

Für die Wiedergabe ist NV12 das effizienteste und am häufigsten unterstützte Format. Daher bieten Decoder in der Regel NV12 als ersten Ausgabetyp in der Liste an. Dadurch wird die Zeit minimiert, die zum Auflösen des Medientyps beim Erstellen einer Wiedergabetopologie benötigt wird. Für die Transcodierung sind IYUV oder I420 jedoch effizienter für die CPU und werden in der Regel von Encodern bevorzugt.

Wenn ein Decoder dieses Attribut unterstützt, weist das Attribut das folgende Verhalten auf:

-   Wenn das Attribut über einen Wert ungleich 0 (null) verfügt, werden IYUV und I420 zuerst in der Liste der Ausgabemedientypen angezeigt. Diese Einstellung ist für die Transcodierung am effizientesten.
-   Wenn das Attribut 0 (null) ist, wird NV12 zuerst in der Liste der Ausgabemedientypen angezeigt. Diese Einstellung ist für die Wiedergabe am effizientesten und die Standardeinstellung.

So legen Sie dieses Attribut fest:

1.  Rufen Sie [**ÜBERTRANSFORM::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) für den Decoder auf, um einen [**POINTERAttributes-Zeiger**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) abzurufen.
2.  Rufen Sie [**DIE ATTRIBUTEAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) auf, um das Attribut hinzuzufügen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 \|Desktop-Apps UWP-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                |
| Header<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




