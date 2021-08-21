---
description: Bestimmt, ob sich der Bereich von IAnalysisRegion mit dem angegebenen Rechteck überschneidet.
ms.assetid: 683c3ad8-0236-474e-a16d-6164c2244cfb
title: IAnalysisRegion::IntersectsWith-Methode (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.IntersectsWith
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 04613e061929bba04c14be37914b22a51de0377f125b21fa29db9c56fc8dfeff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118720017"
---
# <a name="ianalysisregionintersectswith-method"></a>IAnalysisRegion::IntersectsWith-Methode

Bestimmt, ob sich der Bereich von [**IAnalysisRegion**](ianalysisregion.md) mit dem angegebenen Rechteck überschneidet.

## <a name="syntax"></a>Syntax


```C++
HRESULT IntersectsWith(
  [in]  RECT         *pRectangle,
  [out] VARIANT_BOOL *pfIsIntersecting
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pRectangle* \[ In\]
</dt> <dd>

Ein Zeiger auf das Rechteck, mit dem verglichen werden soll, in Freihandraumkoordinaten.

</dd> <dt>

*pfIsIntersecting* \[ out\]
</dt> <dd>

**VARIANT \_ TRUE,** wenn sich der Bereich von [**IAnalysisRegion**](ianalysisregion.md) mit dem angegebenen Rechteck überschneidet; Andernfalls **VARIANT \_ FALSE**.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter Klassen und Schnittstellen – [Ink-Analyse.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Hinweise

Der Vergleich erfolgt in Freihandraumkoordinaten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (erfordert auch IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IAnalysisRegion**](ianalysisregion.md)
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

 




