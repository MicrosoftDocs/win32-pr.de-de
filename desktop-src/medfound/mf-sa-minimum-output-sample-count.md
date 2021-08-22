---
description: Gibt die maximale Anzahl von Ausgabebeispielen an, die eine Microsoft Media Foundation-Transformation (MFT) jederzeit in der Pipeline ausstehend ist.
ms.assetid: 53D393B4-BFF1-430F-9CD1-5071336E6F04
title: MF_SA_MINIMUM_OUTPUT_SAMPLE_COUNT-Attribut (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79a7d00fcb5a11d756ed4848e3e600a6fd1cca32203ff7234cb01963dfcb5149
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663910"
---
# <a name="mf_sa_minimum_output_sample_count-attribute"></a>MF \_ SA MINIMUM OUTPUT SAMPLE \_ \_ \_ \_ COUNT-Attribut

Gibt die maximale Anzahl von Ausgabebeispielen an, die eine Microsoft Media Foundation-Transformation (MFT) jederzeit in der Pipeline ausstehend ist.

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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Transformieren von Attributen](transform-attributes.md)
</dt> </dl>

 

 




