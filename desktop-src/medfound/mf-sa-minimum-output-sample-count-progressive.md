---
description: Gibt die Mindestanzahl von progressiven Stichproben an, die die Microsoft Media Foundation-Transformation (MFT) zu einem bestimmten Zeitpunkt zulassen sollte.
ms.assetid: C1F27F39-FADA-4644-ACD6-B02EAD9CFFE7
title: MF_SA_MINIMUM_OUTPUT_SAMPLE_COUNT_PROGRESSIVE Attribut (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48df5262e225b8768d3251f9768cf2156ee2acacb19ca70752ae5bf989b682ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955430"
---
# <a name="mf_sa_minimum_output_sample_count_progressive-attribute"></a>MF \_ SA MINIMUM OUTPUT SAMPLE COUNT \_ \_ \_ \_ \_ PROGRESSIVE-Attribut

Gibt die Mindestanzahl von progressiven Stichproben an, die die Microsoft Media Foundation-Transformation (MFT) zu einem bestimmten Zeitpunkt zulassen sollte.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Hinweise

Dieses Attribut gilt nur für MFTs, die einen Kreispuffer verwenden, um ihre eigenen Ausgabebeispiele zuzuordnen. Andere MFTs ignorieren dieses Attribut.

So legen Sie dieses Attribut fest:

1.  Rufen Sie [**ÜBERTRANSFORM::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) für den Decoder auf, um einen [**POINTERAttributes-Zeiger**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) abzurufen.
2.  Rufen Sie [**DIE ATTRIBUTEAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) auf, um das Attribut hinzuzufügen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 \|Desktop-Apps UWP-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 \|Desktop-Apps UWP-Apps\]<br/>                              |
| Header<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




