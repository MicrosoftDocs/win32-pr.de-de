---
description: Enthält Konfigurations Eigenschaften für einen Encoder.
ms.assetid: f9bd8a50-e43e-4668-86a0-c9d5f517f4cf
title: MFT_PREFERRED_ENCODER_PROFILE-Attribut (MF Transform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfdc85ead0fe813215b3edaea14833400df5445d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959238"
---
# <a name="mft_preferred_encoder_profile-attribute"></a>"MFT \_ Preferred \_ Encoder profile"- \_ Attribut

Enthält Konfigurations Eigenschaften für einen Encoder.

## <a name="data-type"></a>Datentyp

**[**Imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) \** _ als " _*IUnknown \** " gespeichert_

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut abzurufen, nennen Sie [_ *imfattributes:: getunknown* *](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).

Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: setunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).

## <a name="applies-to"></a>Gilt für:

[**Imfaktivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)

## <a name="remarks"></a>Bemerkungen

Dieses Attribut kann für das Aktivierungs Objekt festgelegt werden, das von der [**msmekreatetransformaktivierungs**](/windows/desktop/api/mftransform/nf-mftransform-mfcreatetransformactivate) -Funktion zurückgegeben wird. Das-Attribut wird nur angewendet, wenn das Aktivierungs Objekt zum Erstellen eines Encoders konfiguriert ist. Der Wert des-Attributs ist ein Zeiger auf einen Attribut Speicher, der wiederum Eigenschaften enthält, die für den Encoder festgelegt werden sollen.

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

[**MF | atetransformaktivierungs**](/windows/desktop/api/mftransform/nf-mftransform-mfcreatetransformactivate)
</dt> <dt>

[Transformations Attribute](transform-attributes.md)
</dt> </dl>

 

 




