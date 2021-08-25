---
description: Schränkt den Bereich dieser IAnalysisRegion auf den Bereich ein, der durch die Schnittmenge mit dem angegebenen Rechteck erstellt wurde.
ms.assetid: de6b565f-34c1-4551-ab92-db6bacb8608d
title: IAnalysisRegion::IntersectRectangle-Methode (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.IntersectRectangle
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 074e3cee4cd20a35c780ce0c644b24c7688956d85a631f3563dd678c70c82822
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119935490"
---
# <a name="ianalysisregionintersectrectangle-method"></a>IAnalysisRegion::IntersectRectangle-Methode

Schränkt den Bereich dieser [**IAnalysisRegion**](ianalysisregion.md) auf den Bereich ein, der durch die Schnittmenge mit dem angegebenen Rechteck erstellt wurde.

## <a name="syntax"></a>Syntax


```C++
HRESULT IntersectRectangle(
  [in] RECT *pIntersectingRectangle
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pIntersectingRectangle* \[ In\]
</dt> <dd>

Ein Zeiger auf das Rechteck, mit dem sich in Freihandraumkoordinaten überschneiden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter Klassen und Schnittstellen – [Ink-Analyse.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Hinweise

Die Rechteckkoordinaten befinden sich in HIMETRIC-Einheiten.

Wenn sich die beiden Bereiche nicht überschneiden, ist der neue Bereich leer.

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

[**IAnalysisRegion::IntersectRegion-Methode**](ianalysisregion-intersectregion.md)
</dt> <dt>

[**IAnalysisRegion::UnionRectangle-Methode**](ianalysisregion-unionrectangle.md)
</dt> <dt>

[**IAnalysisRegion::UnionRegion-Methode**](ianalysisregion-unionregion.md)
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

 




