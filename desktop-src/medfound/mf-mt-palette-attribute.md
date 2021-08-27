---
description: Enthält die Paletteneinträge für einen Videomedientyp. Verwenden Sie dieses Attribut für palettierte Videoformate, z. B. RGB 8.
ms.assetid: 3efc124b-073e-4c48-9550-c100e29f2d6f
title: MF_MT_PALETTE-Attribut (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a20623262be0129cabf5675fd4cd1a37ec2fb61b6b9a0dd5e135fa9e48e1abb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118741655"
---
# <a name="mf_mt_palette-attribute"></a>MF \_ MT \_ PALETTE-Attribut

Enthält die Paletteneinträge für einen Videomedientyp. Verwenden Sie dieses Attribut für palettierte Videoformate, z. B. RGB 8.

## <a name="data-type"></a>Datentyp

Bytearray

## <a name="remarks"></a>Hinweise

Die Attributdaten sind ein Array von [**MFPaletteEntry-Unions.**](/windows/win32/api/mfobjects/ns-mfobjects-mfpaletteentry)

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Vista-Desktop-Apps \| UWP-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows UWP-Apps für Server \[ 2008-Desktop-Apps \|\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**ATTRIBUTEAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**ATTRIBUTEAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**ARCHEMEDIATYPE**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Medientypattribute](media-type-attributes.md)
</dt> </dl>

 

 




