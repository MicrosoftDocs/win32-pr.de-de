---
description: Bestimmt, ob die angegebene IAnalysisRegion den gleichen Wert wie das aktuelle IAnalysisRegion-Objekt enthält.
ms.assetid: 44c09cfe-65fc-4175-ad05-01c605218c58
title: IAnalysisRegion::EqualsRegion-Methode (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.EqualsRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: aecf7bd065c2da0c507c2424c0305526510c9d4f64844dfa229183cf43d5554a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119596800"
---
# <a name="ianalysisregionequalsregion-method"></a>IAnalysisRegion::EqualsRegion-Methode

Bestimmt, ob die angegebene [**IAnalysisRegion**](ianalysisregion.md) den gleichen Wert wie das aktuelle **IAnalysisRegion-Objekt** enthält.

## <a name="syntax"></a>Syntax


```C++
HRESULT EqualsRegion(
  [in]  IAnalysisRegion *pOtherRegion,
  [out] VARIANT_BOOL    *pfRegionsEqual
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pOtherRegion* \[ In\]
</dt> <dd>

Das [**IAnalysisRegion-Objekt,**](ianalysisregion.md) das mit dem aktuellen **IAnalysisRegion** verglichen werden soll.

</dd> <dt>

*pfRegionsEqual* \[ out\]
</dt> <dd>

**VARIANT \_ TRUE,** wenn die angegebene [**IAnalysisRegion**](ianalysisregion.md) den gleichen Wert wie die aktuelle IAnalysisRegion enthält; Andernfalls **VARIANT \_ FALSE**.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter Klassen und Schnittstellen – [Ink-Analyse.](classes-and-interfaces---ink-analysis.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (erfordert auch IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IAnalysisRegion**](ianalysisregion.md)
</dt> </dl>

 

 




