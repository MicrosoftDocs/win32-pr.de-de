---
description: Schränkt den Bereich von IAnalysisRegion auf den Teil des Bereichs ein, der das angegebene Rechteck nicht überschneidet.
ms.assetid: a35b8bfc-a87a-4e9a-908f-2b13a128d222
title: IAnalysisRegion::ExcludeRectangle-Methode (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.ExcludeRectangle
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 63fd4a8faaa371e8403930f53022e221836b6f5692295d87623cb75ff34a60c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118045398"
---
# <a name="ianalysisregionexcluderectangle-method"></a>IAnalysisRegion::ExcludeRectangle-Methode

Schränkt den Bereich von [**IAnalysisRegion**](ianalysisregion.md) auf den Teil des Bereichs ein, der das angegebene Rechteck nicht überschneidet.

## <a name="syntax"></a>Syntax


```C++
HRESULT ExcludeRectangle(
  [in] RECT *pExcludingRectangle
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pExcludingRectangle* \[ In\]
</dt> <dd>

Das Rechteck, das aus dieser [**IAnalysisRegion**](ianalysisregion.md)ausgeschlossen werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter Klassen und Schnittstellen – [Ink-Analyse.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Hinweise

Die Rechteckkoordinaten befinden sich in HIMETRIC-Einheiten.

Wenn sich die beiden Bereiche nicht überschneiden, bleibt die [**IAnalysisRegion**](ianalysisregion.md) unverändert.

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

[**IAnalysisRegion::ExcludeRegion-Methode**](ianalysisregion-excluderegion.md)
</dt> <dt>

[**IAnalysisRegion::IntersectRectangle-Methode**](ianalysisregion-intersectrectangle.md)
</dt> <dt>

[**IAnalysisRegion::IntersectRegion-Methode**](ianalysisregion-intersectregion.md)
</dt> <dt>

[**IAnalysisRegion::UnionRectangle-Methode**](ianalysisregion-unionrectangle.md)
</dt> <dt>

[**IAnalysisRegion::UnionRegion-Methode**](ianalysisregion-unionregion.md)
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

 




