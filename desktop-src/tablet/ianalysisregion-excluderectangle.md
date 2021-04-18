---
description: Schränkt den Bereich von ianalysisregion auf den Teil des Bereichs ein, der das angegebene Rechteck nicht überschneidet.
ms.assetid: a35b8bfc-a87a-4e9a-908f-2b13a128d222
title: 'Ianalysisregion:: excluderectangle-Methode (iacom. h)'
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
ms.openlocfilehash: 684ce2ceb57c7954c732fb2816aca50fcbae5297
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347200"
---
# <a name="ianalysisregionexcluderectangle-method"></a>Ianalysisregion:: excluderectangle-Methode

Schränkt den Bereich von [**ianalysisregion**](ianalysisregion.md) auf den Teil des Bereichs ein, der das angegebene Rechteck nicht überschneidet.

## <a name="syntax"></a>Syntax


```C++
HRESULT ExcludeRectangle(
  [in] RECT *pExcludingRectangle
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pexcludingrechteck* \[ in\]
</dt> <dd>

Das Rechteck, das aus diesem [**ianalysisregion**](ianalysisregion.md)ausgeschlossen werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

Die Rechteck Koordinaten befinden sich in HIMETRIC-Einheiten.

Wenn sich die beiden Bereiche nicht überschneiden, ist [**ianalysisregion**](ianalysisregion.md) unverändert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Iacom. h (erfordert auch iacom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ianalysisregion**](ianalysisregion.md)
</dt> <dt>

[**Ianalysisregion:: excluderegion-Methode**](ianalysisregion-excluderegion.md)
</dt> <dt>

[**Ianalysisregion:: intersectrechteck-Methode**](ianalysisregion-intersectrectangle.md)
</dt> <dt>

[**Ianalysisregion:: intersectregion-Methode**](ianalysisregion-intersectregion.md)
</dt> <dt>

[**Ianalysisregion:: unionrechteck-Methode**](ianalysisregion-unionrectangle.md)
</dt> <dt>

[**Ianalysisregion:: unionregion-Methode**](ianalysisregion-unionregion.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

 




