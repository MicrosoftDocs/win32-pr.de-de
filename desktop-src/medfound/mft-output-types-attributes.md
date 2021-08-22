---
description: Enthält die registrierten Ausgabetypen für eine Media Foundation Transformation (MFT).
ms.assetid: 925267a2-4421-4874-a8a2-437876c729f1
title: MFT_OUTPUT_TYPES_Attributes-Attribut (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2699d244bc5184652d0ba1d89ebf4e1beaddb472bb1d6fa09c05d1edf99030fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119462780"
---
# <a name="mft_output_types_attributes-attribute"></a>Attribut \_ "MFT OUTPUT \_ TYPES \_ Attributes"

Enthält die registrierten Ausgabetypen für eine Media Foundation Transformation (MFT).

## <a name="data-type"></a>Datentyp

**MFT \_ REGISTER \_ TYPE \_ \[ \] INFO** stored as **BYTE \[ \]**

## <a name="remarks"></a>Hinweise

Dieses Attribut wird für die VON der [**MFTEnumEx-Funktion zurückgegebenen**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) [**POINTERActivate-Zeiger**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) festgelegt.

Dieses Attribut enthält ein Array von [**MFT \_ REGISTER TYPE \_ \_ INFO-Strukturen,**](/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info) die mindestens ein ausgabeformat beschreiben, das vom MFT unterstützt wird. Diese Werte stammen aus der Registrierung und dienen als Hinweis für die Anwendung. Der MFT unterstützt möglicherweise zusätzliche Formate. Zum Festlegen des tatsächlichen Ausgabeformats müssen Sie den MFT erstellen und [**DANN DIETRANSFORM::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype)aufrufen.

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps \| UWP-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2 \[ Desktop-Apps \| UWP-Apps\]<br/>                           |
| Header<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Transformieren von Attributen](transform-attributes.md)
</dt> </dl>

 

 




