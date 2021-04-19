---
description: Gibt an, ob imftransform MEPolicySet-Abschluss Benachrichtigungen empfangen möchte.
title: MFT_POLICY_SET_AWARE (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2effa9eab2b0b126c2849d39ce7ffe3f62d81e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345264"
---
# <a name="mft_policy_set_aware-attribute"></a>MFT- \_ Richtlinien \_ Satz fähiges \_ Attribut

Wenn ungleich 0 (null), gibt an, dass die **imftransform** -Meldung über das Beenden von [MEPolicySet](./mepolicyset.md) -Benachrichtigungen empfangen möchte

## <a name="data-type"></a>Datentyp

**UInt32** (als **bool** behandelt)

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Gilt für:

[**Imfinputtrustauthority**](/windows/win32/api/mfidl/nn-mfidl-imfinputtrustauthority)

## <a name="remarks"></a>Bemerkungen

Dieses attributetett kann von einer **imfinputtrustauthority** -Entschlüsselung verwendet werden. Eine Implementierung eines Inhalts Entschlüsselungs Moduls (CDM) kann eine Implementierung von **imfinputtrustauthority** enthalten. Der Zugriff auf das **imfinputtrustauthority** -Objekt erfolgt über [IMF contentdecryptionmodule:: foratetrustedinput](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmodule-createtrustedinput).


Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10 April 2020-Update   <br/>                                        |
| Header<br/>                   | <dl> <dt>"MF Transform. h"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt>  <dt>

[Transformations Attribute](transform-attributes.md)
</dt> </dl>

 

 
