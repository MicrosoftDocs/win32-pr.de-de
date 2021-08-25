---
description: Gibt an, welcher Balken der Spracherfassungs-DSP für die Mikrofonarrayverarbeitung verwendet.
ms.assetid: 9ed761da-3f1b-47e8-b71f-becc56fe8801
title: MFPKEY_WMAAECMA_FEATR_MICARR_BEAM-Eigenschaft (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b9a91cef7d270af37adc8fda9805d7bf275ef9877883ed8ff8cfdbf9e7a55e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119953530"
---
# <a name="mfpkey_wmaaecma_featr_micarr_beam-property"></a>MFPKEY \_ WMAAECMA \_ FEATR \_ MICARR-EIGENSCHAFT \_ "BALKEN"

Gibt an, welcher Balken der Spracherfassungs-DSP für die Mikrofonarrayverarbeitung verwendet.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.

## <a name="data-type"></a>Datentyp

VT \_ I4

## <a name="applies-to"></a>Gilt für

-   [Spracherfassungs-DSP](voicecapturedmo.md)

## <a name="remarks"></a>Hinweise

Legen Sie diese Eigenschaft fest, wenn der Wert der [MFPKEY \_ WMAAECMA \_ FEATR \_ MICARR \_ MODE-Eigenschaft](mfpkey-wmaaecma-featr-micarr-modeproperty.md) MICARRAY \_ EXTERN \_ BALKEN ist.

Wenn der Wert von [**MFPKEY \_ WMAAECMA \_ FEATR \_ MICARR \_ MODE**](mfpkey-wmaaecma-featr-micarr-modeproperty.md) MICARRAY \_ SINGLE BEAM \_ lautet, können Sie diese Eigenschaft lesen, um abzufragen, welcher Balken vom DSP ausgewählt wurde.

Diese Eigenschaft kann die folgenden Werte aufweisen. Die Werte sind in Grad horizontal.



| Wert | BESCHREIBUNG              |
|-------|--------------------------|
| 0     | -50 Grad.             |
| 1     | -40 Grad.             |
| 2     | -30 Grad.             |
| 3     | -20 Grad.             |
| 4     | -10 Grad.             |
| 5     | 0 Grad (Mittelbalken). |
| 6     | 10 Grad.              |
| 7     | 20 Grad.              |
| 8     | 30 Grad.              |
| 9     | 40 Grad.              |
| 10    | 50 Grad.              |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Media Foundation-Eigenschaften](media-foundation-properties.md)
</dt> <dt>

[Spracherfassungs-DSP](voicecapturedmo.md)
</dt> </dl>

 

 
