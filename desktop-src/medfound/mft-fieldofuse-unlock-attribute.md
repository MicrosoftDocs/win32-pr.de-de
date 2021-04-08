---
description: Enthält einen imffieldofusemftunlock-Zeiger, der zum Entsperren einer Media Foundation Transformation (MFT) verwendet werden kann. Die imffieldofusemftunlock-Schnittstelle wird verwendet, um ein MFT mit Einschränkungen für das Feld zu entsperren.
ms.assetid: 7f48967e-375a-4019-b14f-2f457b616cc0
title: MFT_FIELDOFUSE_UNLOCK_Attribute-Attribut (MF Transform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85f02fbc032f16406a2b4407b197dc6140774001
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755272"
---
# <a name="mft_fieldofuse_unlock_attribute-attribute"></a>MFT \_ fieldofuse \_ Unlock \_ Attribute-Attribut

Enthält einen [**imffieldofusemftunlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) -Zeiger, der zum Entsperren einer Media Foundation Transformation (MFT) verwendet werden kann. Die **imffieldofusemftunlock** -Schnittstelle wird verwendet, um ein MFT mit Einschränkungen für das Feld zu entsperren.

## <a name="data-type"></a>Datentyp

**[**Imffieldofusemftunlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) \** _ als " _*IUnknown \** " gespeichert_

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut abzurufen, nennen Sie [_ *imfattributes:: getunknown* *](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).

Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: setunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).

## <a name="remarks"></a>Bemerkungen

Weitere Informationen zu diesem Attribut finden Sie unter [Einschränkungen](field-of-use-restrictions.md)für das Feld "Verwendung".

Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ -Desktop-Apps \| UWP-apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2 \[ -Desktop-Apps \| UWP-apps\]<br/>                           |
| Header<br/>                   | <dl> <dt>"MF Transform. h"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Einschränkungen bei der Verwendung des Felds](field-of-use-restrictions.md)
</dt> <dt>

[**MF | atetransformaktivierungs**](/windows/desktop/api/mftransform/nf-mftransform-mfcreatetransformactivate)
</dt> </dl>

 

 




