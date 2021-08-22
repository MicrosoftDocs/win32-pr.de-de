---
description: Erweitert den Bereich dieser IAnalysisRegion auf den Bereich, der durch seine Vereinigung mit dem angegebenen Rechteck erstellt wurde.
ms.assetid: 9b12f509-4f6a-43b0-9639-bef060fd6d50
title: IAnalysisRegion::UnionRectangle-Methode (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.UnionRectangle
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: da3eefb3a527646ba416d62783421d6dfe9be5706c0527df7eb321d3945b6f92
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119596751"
---
# <a name="ianalysisregionunionrectangle-method"></a>IAnalysisRegion::UnionRectangle-Methode

Erweitert den Bereich dieser [**IAnalysisRegion**](ianalysisregion.md) auf den Bereich, der durch seine Vereinigung mit dem angegebenen Rechteck erstellt wurde.

## <a name="syntax"></a>Syntax


```C++
HRESULT UnionRectangle(
  [in] RECT *pRectangle
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pRectangle* \[ In\]
</dt> <dd>

Ein Zeiger auf das Rechteck, mit dem kombiniert werden soll, in Freihandraumkoordinaten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter Klassen und Schnittstellen – [Ink-Analyse.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Hinweise

Die Rechteckkoordinaten befinden sich in HIMETRIC-Einheiten.

Wenn einer der Bereiche unendlich ist, ist der neue Bereich ebenfalls unendlich.

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

[**IAnalysisRegion::IntersectRegion-Methode**](ianalysisregion-intersectregion.md)
</dt> <dt>

[**IAnalysisRegion::UnionRegion-Methode**](ianalysisregion-unionregion.md)
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

 




