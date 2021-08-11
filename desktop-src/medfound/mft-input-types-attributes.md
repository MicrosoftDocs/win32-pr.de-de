---
description: Enthält die registrierten Eingabetypen für eine Media Foundation Transform (MFT).
ms.assetid: 0fb1d9f2-2b57-41bc-8365-0b88bd5a2f3d
title: MFT_INPUT_TYPES_Attributes -Attribut (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a750094361cdaa877bff82e20a74c1beae4e1a1f76ea0a9ad5be83f308c1f2d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118240235"
---
# <a name="mft_input_types_attributes-attribute"></a>Attribut "MFT \_ \_ INPUT TYPES \_ Attributes"

Enthält die registrierten Eingabetypen für eine Media Foundation Transform (MFT).

## <a name="data-type"></a>Datentyp

**MFT \_ REGISTER \_ TYPE \_ INFO \[ \] als** **BYTE gespeichert \[ \]**

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut zu erhalten, rufen [**Sie DIE ATTRIBUTEs::GetBlob auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)

Rufen Sie ZUM Festlegen dieses [**Attributs DIE ATTRIBUTEs::SetBlob auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)

## <a name="remarks"></a>Hinweise

Dieses Attribut wird für die VON der [**MFTEnumEx-Funktion**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) zurückgegebenen [**ATTRIBUTEActivate-Zeiger**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) festgelegt.

Dieses Attribut enthält ein Array von [**MFT \_ REGISTER TYPE \_ \_ INFO-Strukturen,**](/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info) die ein oder mehrere eingabeformate beschreiben, die von MFT unterstützt werden. Diese Werte werden aus der Registrierung übernommen und dienen als Hinweis für die Anwendung. MFT unterstützt möglicherweise zusätzliche Formate. Zum Festlegen des tatsächlichen Eingabeformats müssen Sie die MFT erstellen und [**DANNTransform::SetInputType aufrufen.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype)

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps \| UWP-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows UWP-Apps für Server 2008 \[ \| R2-Desktop-Apps\]<br/>                           |
| Header<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Transformieren von Attributen](transform-attributes.md)
</dt> </dl>

 

 




