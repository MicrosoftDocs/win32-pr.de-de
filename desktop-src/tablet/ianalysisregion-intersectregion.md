---
description: Schränkt den Bereich von IAnalysisRegion auf den Bereich ein, der durch seine Schnittmenge mit der angegebenen IAnalysisRegion erstellt wurde.
ms.assetid: 02b3049f-ada9-4de3-a7a2-f9ff8313fbab
title: IAnalysisRegion::IntersectRegion-Methode (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.IntersectRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 0db58dcc7fc1c1e7458cf804eb82af236de8f1997ddcc658391da19641d1cfdb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120058080"
---
# <a name="ianalysisregionintersectregion-method"></a>IAnalysisRegion::IntersectRegion-Methode

Schränkt den Bereich von [**IAnalysisRegion**](ianalysisregion.md) auf den Bereich ein, der durch seine Schnittmenge mit dem angegebenen **IAnalysisRegion** erstellt wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT IntersectRegion(
  [in] IAnalysisRegion *pRegionToIntersect
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pRegionToIntersect* \[ In\]
</dt> <dd>

Die [**IAnalysisRegion,**](ianalysisregion.md) mit der sich die Daten überschneiden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter Klassen und Schnittstellen – [Ink-Analyse.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Hinweise

Wenn sich die beiden Bereiche nicht überschneiden, ist der neue Bereich leer.

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
</dt> <dt>

[**IAnalysisRegion::ExcludeRectangle**](ianalysisregion-excluderectangle.md)
</dt> <dt>

[**IAnalysisRegion::ExcludeRegion-Methode**](ianalysisregion-excluderegion.md)
</dt> <dt>

[**IAnalysisRegion::IntersectRectangle-Methode**](ianalysisregion-intersectrectangle.md)
</dt> <dt>

[**IAnalysisRegion::UnionRectangle-Methode**](ianalysisregion-unionrectangle.md)
</dt> <dt>

[**IAnalysisRegion::UnionRegion-Methode**](ianalysisregion-unionregion.md)
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

 




