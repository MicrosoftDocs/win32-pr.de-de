---
description: Schränkt den Bereich von IAnalysisRegion auf den Teil des Bereichs ein, der die angegebene IAnalysisRegion nicht überschneidet.
ms.assetid: 7a11d2a8-c2ca-4088-b932-8a6c3e789b7f
title: IAnalysisRegion::ExcludeRegion-Methode (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.ExcludeRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 4a26bc234a5a99d2ba692b02097d348b83878c47ea3c9a1cbd21e1558fc41950
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092351"
---
# <a name="ianalysisregionexcluderegion-method"></a>IAnalysisRegion::ExcludeRegion-Methode

Schränkt den Bereich von [**IAnalysisRegion**](ianalysisregion.md) auf den Teil des Bereichs ein, der die angegebene **IAnalysisRegion** nicht überschneidet.

## <a name="syntax"></a>Syntax


```C++
HRESULT ExcludeRegion(
  [in] IAnalysisRegion *pRegionToExclude
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pRegionToExclude* \[ In\]
</dt> <dd>

Die [**IAnalysisRegion,**](ianalysisregion.md) die aus dieser **IAnalysisRegion** ausgeschlossen werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter Klassen und Schnittstellen – [Ink-Analyse.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Hinweise

Wenn sich die beiden Bereiche nicht überschneiden, bleibt diese [**IAnalysisRegion**](ianalysisregion.md) unverändert.

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

 

 




