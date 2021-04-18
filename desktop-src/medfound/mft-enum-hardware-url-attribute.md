---
description: Enthält den symbolischen Link für eine hardwarebasierte Media Foundation Transformation (MFT).
ms.assetid: 7e153051-a167-4ff7-8178-b290d8a1345e
title: MFT_ENUM_HARDWARE_URL_Attribute-Attribut (MF Transform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 539aa1ecbf8bf322e7397a50bb16175dbcca806f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215417"
---
# <a name="mft_enum_hardware_url_attribute-attribute"></a>Attribut Attribut für MFT-Aufzählungs \_ \_ Hardware- \_ URL \_

Enthält den symbolischen Link für eine hardwarebasierte Media Foundation Transformation (MFT).

## <a name="data-type"></a>Datentyp

**WCHAR \** _

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut abzurufen, nennen Sie [_ *imfattributes:: GetString* *](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).

Um dieses Attribut festzulegen, müssen Sie [**imfattributes:: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)aufrufen.

## <a name="remarks"></a>Bemerkungen

Dieses Attribut wird von hardwarebasierten MFTs unterstützt. Der Wert des-Attributs ist die symbolische Verknüpfung für den Gerätetreiber. Dieses Attribut wird auch für die [**imfaktivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) -Zeiger festgelegt, die von der [**msumex**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) -Funktion zugewiesen werden, wenn diese Zeiger hardwarebasierte MFTs darstellen.

Die symbolische Verknüpfung sollte als nicht transparente Zeichenfolge betrachtet werden. Um den anzeigen Amen für ein Gerät zu erhalten, Fragen Sie das MFT-Attribut " [ \_ Friendly \_ Name](mft-friendly-name-attribute.md) " ab.

Für Software-MFTs sollte dieses Attribut nicht festgelegt werden.

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

[Hardware-MFTs](hardware-mfts.md)
</dt> <dt>

[Transformations Attribute](transform-attributes.md)
</dt> </dl>

 

 




