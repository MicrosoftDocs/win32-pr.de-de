---
description: Enthält die Paletteneinträge für einen Video Medientyp. Verwenden Sie dieses Attribut für Paletten-Videoformate, wie z. b. RGB 8.
ms.assetid: 3efc124b-073e-4c48-9550-c100e29f2d6f
title: MF_MT_PALETTE-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45dcfc596ae463cf642cc462da1c73dc641356d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106355655"
---
# <a name="mf_mt_palette-attribute"></a>MF- \_ MT- \_ Palette-Attribut

Enthält die Paletteneinträge für einen Video Medientyp. Verwenden Sie dieses Attribut für Paletten-Videoformate, wie z. b. RGB 8.

## <a name="data-type"></a>Datentyp

Bytearray

## <a name="remarks"></a>Bemerkungen

Bei den Attributdaten handelt es sich um ein Array von [**MF-etteentry**](/windows/win32/api/mfobjects/ns-mfobjects-mfpaletteentry) -Unions.

Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista \[ -Desktop-Apps \| UWP-apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**Imfattributes:: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**Imfattributes:: setBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**IMF MediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Medientyp Attribute](media-type-attributes.md)
</dt> </dl>

 

 




