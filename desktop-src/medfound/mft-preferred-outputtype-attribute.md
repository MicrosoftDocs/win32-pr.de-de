---
description: Gibt das bevorzugte Ausgabeformat für einen Encoder an.
ms.assetid: 36a09696-3fe7-41a0-93f1-712220f88b04
title: MFT_PREFERRED_OUTPUTTYPE_Attribute-Attribut (MF Transform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13cd079bee65f5324987d9b38dca845ec5b85f83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863956"
---
# <a name="mft_preferred_outputtype_attribute-attribute"></a>MFT- \_ bevorzugtes \_ OutputType- \_ Attribut Attribut

Gibt das bevorzugte Ausgabeformat für einen Encoder an.

## <a name="data-type"></a>Datentyp

**[**Imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) \** _ als " _*IUnknown \** " gespeichert_

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut abzurufen, nennen Sie [_ *imfattributes:: getunknown* *](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).

Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: setunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).

## <a name="applies-to"></a>Gilt für:

[**Imfaktivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)

## <a name="remarks"></a>Bemerkungen

Dieses Attribut kann für das Aktivierungs Objekt festgelegt werden, das von der [**msmekreatetransformaktivierungs**](/windows/desktop/api/mftransform/nf-mftransform-mfcreatetransformactivate) -Funktion zurückgegeben wird. Das-Attribut wird nur angewendet, wenn das Aktivierungs Objekt zum Erstellen eines Encoders konfiguriert ist. Der Wert des-Attributs ist ein Medientyp. Das Aktivierungs Objekt legt diesen Ausgabetyp für den Encoder fest.

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

 

 




