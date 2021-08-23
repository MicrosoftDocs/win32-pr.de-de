---
description: Enthält einen POINTERFieldOfUseMFTUnlock-Zeiger, der zum Entsperren einer Media Foundation-Transformation (MFT) verwendet werden kann. Mithilfe der SCHNITTSTELLE "UNLOCKFieldOfUseMFTUnlock" wird ein MFT entsperrt, für den Einschränkungen für verwendungsbezogene Felder gelten.
ms.assetid: 7f48967e-375a-4019-b14f-2f457b616cc0
title: MFT_FIELDOFUSE_UNLOCK_Attribute Attribut (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 476ae7ffdc6de506b4dbc2f49ec7a6b19b01affafd53f0c9495f9f5c396c5caf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973069"
---
# <a name="mft_fieldofuse_unlock_attribute-attribute"></a>MFT \_ FIELDOFUSE \_ \_ UNLOCK-Attributattribut

Enthält einen [**POINTERFieldOfUseMFTUnlock-Zeiger,**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) der zum Entsperren einer Media Foundation-Transformation (MFT) verwendet werden kann. Mithilfe **der SCHNITTSTELLE "UNLOCKFieldOfUseMFTUnlock"** wird ein MFT entsperrt, für den Einschränkungen für verwendungsbezogene Felder gelten.

## <a name="data-type"></a>Datentyp

**[**STANFIELDOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) \* *_ gespeichert als _* Iunknown\***

## <a name="getset"></a>Abrufen/Festlegen

Rufen Sie ZUM Abrufen dieses [**Attributs DIE ATTRIBUTEAttributes::GetUnknown auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)

Um dieses Attribut festzulegen, rufen Sie [**DIE ATTRIBUTEAttributes::SetUnknown auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)

## <a name="remarks"></a>Hinweise

Weitere Informationen zu diesem Attribut finden Sie unter [Field of Use Restrictions](field-of-use-restrictions.md).

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps \| UWP-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2 \[ Desktop-Apps \| UWP-Apps\]<br/>                           |
| Header<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Einschränkungen des Verwendungsbereichs](field-of-use-restrictions.md)
</dt> <dt>

[**MFCreateTransformActivate**](/windows/desktop/api/mftransform/nf-mftransform-mfcreatetransformactivate)
</dt> </dl>

 

 




