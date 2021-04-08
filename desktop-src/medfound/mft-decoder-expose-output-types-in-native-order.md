---
description: Gibt an, ob ein Decoder vor anderen Formaten IYUV/I420-Ausgabetypen (für die Transcodierung geeignet) verfügbar macht.
ms.assetid: 8505CFA1-210A-4DA8-B92A-FCE62F0310E5
title: MFT_DECODER_EXPOSE_OUTPUT_TYPES_IN_NATIVE_ORDER-Attribut (MF Transform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01ecf074fa0767552a48e3238374dbd02f077404
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755280"
---
# <a name="mft_decoder_expose_output_types_in_native_order-attribute"></a>MFT- \_ Decoder macht \_ \_ Ausgabe \_ Typen im systemeigenen \_ \_ \_ Order-Attribut verfügbar.

Gibt an, ob ein Decoder vor anderen Formaten IYUV/I420-Ausgabetypen (für die Transcodierung geeignet) verfügbar macht.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Bemerkungen

Dieses Attribut ist ein Hinweis für den Decoder, seine Liste der Ausgabetypen in einer bestimmten Reihenfolge anzuordnen, abhängig von der vorgesehenen Verwendung, entweder Wiedergabe oder transcode.

Bei den meisten Codierungs Formaten (H. 264, MPEG-2, WMV) unterstützen die Video-Decoder in Microsoft Media Foundation mehrere allgemeine YUV-Ausgaben, einschließlich NV12, YV12, im YUY2, IYUV und I420. Der Decoder bietet mithilfe der [**imftransform:: getoutputavailabletype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) -Methode eine geordnete Liste von Ausgabetypen.

Für die Wiedergabe ist NV12 das effizienteste und unterschiedlichste Format. Daher bieten Decoder standardmäßig NV12 als ersten Ausgabetyp in der Liste an. Dadurch wird die zum Auflösen des Medientyps erforderliche Zeit minimiert, wenn eine Wiedergabe Topologie aufgebaut wird. Bei der Transcodierung sind IYUV oder I420 jedoch für die CPU effizienter und werden in der Regel von Encodern bevorzugt.

Wenn ein Decoder dieses Attribut unterstützt, weist das Attribut folgendes Verhalten auf:

-   Wenn das Attribut einen Wert ungleich 0 (null) aufweist, werden IYUV und I420 zuerst in der Liste der Ausgabemedien Typen angezeigt. Diese Einstellung ist für die Transcodierung am effizientesten.
-   Wenn das-Attribut 0 (null) ist, wird NV12 zuerst in der Liste der Ausgabemedien Typen angezeigt. Diese Einstellung ist für die Wiedergabe am effizientesten und ist die Standardeinstellung.

So legen Sie dieses Attribut fest:

1.  Aufrufen von [**imftransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) für den Decoder zum Abrufen eines [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) -Zeigers.
2.  Zum Hinzufügen des Attributs wird [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) aufgerufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8 \[ -Desktop-Apps \| UWP-apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                |
| Header<br/>                   | <dl> <dt>"MF Transform. h"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




