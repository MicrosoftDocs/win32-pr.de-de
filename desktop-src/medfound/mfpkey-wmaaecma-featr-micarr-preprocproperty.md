---
description: Gibt an, ob der Spracherfassungs-DSP die Vorverarbeitung des Mikrofonarrays ausführt.
ms.assetid: 0f197165-e6e5-456b-9615-1edc8ada7bb5
title: MFPKEY_WMAAECMA_FEATR_MICARR_PREPROC-Eigenschaft (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebbba5faeb1a1e70feb1ef6182d3ac2a397a52c4a56f27e767be93f4a3fff773
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117873014"
---
# <a name="mfpkey_wmaaecma_featr_micarr_preproc-property"></a>MFPKEY \_ WMAAECMA \_ FEATR \_ MICARR \_ PREPROC-Eigenschaft

Gibt an, ob der Spracherfassungs-DSP die Vorverarbeitung des Mikrofonarrays ausführt.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.

## <a name="data-type"></a>Datentyp

VT \_ BOOL

## <a name="default-value"></a>Standardwert

VARIANT \_ TRUE

## <a name="applies-to"></a>Gilt für

-   [Spracherfassungs-DSP](voicecapturedmo.md)

## <a name="remarks"></a>Hinweise

Bei der Vorverarbeitung können stehende Töne entfernt werden, die die Verarbeitung beeinträchtigen, z. B. ein Ton mit fester Tonhöhe.

Diese Eigenschaft kann die folgenden Werte aufweisen.



| Wert          | Beschreibung            |
|----------------|------------------------|
| VARIANT \_ FALSE | Deaktivieren Sie die Vorverarbeitung. |
| VARIANT \_ TRUE  | Aktivieren Sie die Vorverarbeitung.  |



 

Der Standardwert dieser Eigenschaft ist VARIANT \_ TRUE (aktiviert). Bevor Sie diese Eigenschaft festlegen, müssen Sie die [MFPKEY \_ WMAAECMA \_ FEATURE \_ MODE-Eigenschaft](mfpkey-wmaaecma-feature-modeproperty.md) auf VARIANT \_ TRUE festlegen.

Der DSP verwendet diese Eigenschaft nur, wenn die Mikrofonarrayverarbeitung aktiviert ist.

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

 

 
