---
description: Erweitert den Bereich dieser IAnalysisRegion auf den Bereich, der durch seine Vereinigung mit der angegebenen IAnalysisRegion erstellt wurde.
ms.assetid: cc3ec5c6-98ff-442e-a1e8-d1a57752ad56
title: IAnalysisRegion::UnionRegion-Methode (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.UnionRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 760296552dc13ac394d4554903d84f596faba14318db9af3145c79f156c736fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118720007"
---
# <a name="ianalysisregionunionregion-method"></a>IAnalysisRegion::UnionRegion-Methode

Erweitert den Bereich dieser [**IAnalysisRegion**](ianalysisregion.md) auf den Bereich, der durch seine Vereinigung mit der angegebenen **IAnalysisRegion erstellt wurde.**

## <a name="syntax"></a>Syntax


```C++
HRESULT UnionRegion(
  [in] IAnalysisRegion *pRegionToUnion
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pRegionToUnion* \[ In\]
</dt> <dd>

Die [**IAnalysisRegion,**](ianalysisregion.md) mit der kombiniert werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen – Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Hinweise

Wenn einer der beiden Flächen unendlich ist, ist der neue Bereich ebenfalls unendlich.

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

[**IAnalysisRegion::ExcludeRectangle**](ianalysisregion-excluderectangle.md)
</dt> <dt>

[**IAnalysisRegion::ExcludeRegion-Methode**](ianalysisregion-excluderegion.md)
</dt> <dt>

[**IAnalysisRegion::IntersectRectangle-Methode**](ianalysisregion-intersectrectangle.md)
</dt> <dt>

[**IAnalysisRegion::IntersectRegion-Methode**](ianalysisregion-intersectregion.md)
</dt> <dt>

[**IAnalysisRegion::UnionRectangle-Methode**](ianalysisregion-unionrectangle.md)
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

 




