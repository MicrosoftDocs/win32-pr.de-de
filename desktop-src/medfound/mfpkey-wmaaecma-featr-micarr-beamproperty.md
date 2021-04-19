---
description: Gibt an, welcher Strahl der sprach Erfassungs-DSP für die Verarbeitung von mikrofonarrays verwendet.
ms.assetid: 9ed761da-3f1b-47e8-b71f-becc56fe8801
title: MFPKEY_WMAAECMA_FEATR_MICARR_BEAM-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9165eec0dee87fa5d9f6a751f41e81d0de2d9958
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360136"
---
# <a name="mfpkey_wmaaecma_featr_micarr_beam-property"></a>Mfpkey \_ wmaaecma \_ featr \_ micarr- \_ Eigenschaft (Eigenschaft)

Gibt an, welcher Strahl der sprach Erfassungs-DSP für die Verarbeitung von mikrofonarrays verwendet.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.

## <a name="data-type"></a>Datentyp

VT \_ I4

## <a name="applies-to"></a>Gilt für

-   [Sprach Erfassungs-DSP](voicecapturedmo.md)

## <a name="remarks"></a>Bemerkungen

Legen Sie diese Eigenschaft fest, wenn der Wert der Eigenschaft " [mfpkey \_ wmaaecma \_ featr \_ micarr \_ Mode](mfpkey-wmaaecma-featr-micarr-modeproperty.md) " micarray \_ extern \_ Beam ist.

Wenn der Wert von " [**mfpkey \_ wmaaecma \_ featr \_ micarr \_ Mode**](mfpkey-wmaaecma-featr-micarr-modeproperty.md) " micarray \_ Single \_ Beam ist, können Sie diese Eigenschaft lesen, um abzufragen, welcher Strahl vom DSP ausgewählt wurde.

Diese Eigenschaft kann die folgenden Werte aufweisen. Werte sind horizontal in Grad.



| Wert | BESCHREIBUNG              |
|-------|--------------------------|
| 0     | -50 Grad.             |
| 1     | -40 Grad.             |
| 2     | -30 Grad.             |
| 3     | -20 Grad.             |
| 4     | -10 Grad.             |
| 5     | 0 Grad (Mittelstrahl). |
| 6     | 10 Grad.              |
| 7     | 20 Grad.              |
| 8     | 30 Grad.              |
| 9     | 40 Grad.              |
| 10    | 50 Grad.              |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften von Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Sprach Erfassungs-DSP](voicecapturedmo.md)
</dt> </dl>

 

 
