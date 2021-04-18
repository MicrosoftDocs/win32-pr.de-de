---
description: Erweitert den Bereich dieses ianalysisregion auf den Bereich, der durch die zugehörige Union mit dem angegebenen Rechteck erstellt wurde.
ms.assetid: 9b12f509-4f6a-43b0-9639-bef060fd6d50
title: 'Ianalysisregion:: unionrechteck-Methode (iacom. h)'
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
ms.openlocfilehash: 3a28a60eae95641225dd9c01791d89a9c38ada82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368101"
---
# <a name="ianalysisregionunionrectangle-method"></a>Ianalysisregion:: unionrechteck-Methode

Erweitert den Bereich dieses [**ianalysisregion**](ianalysisregion.md) auf den Bereich, der durch die zugehörige Union mit dem angegebenen Rechteck erstellt wurde.

## <a name="syntax"></a>Syntax


```C++
HRESULT UnionRectangle(
  [in] RECT *pRectangle
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*prätangle* \[ in\]
</dt> <dd>

Ein Zeiger auf das Rechteck, mit dem die Kombination in frei Hand Raumkoordinaten kombiniert werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

Die Rechteck Koordinaten befinden sich in HIMETRIC-Einheiten.

Wenn einer der Bereiche unbegrenzt ist, ist der neue Bereich ebenfalls unendlich.

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

[**Ianalysisregion:: excluderectangle**](ianalysisregion-excluderectangle.md)
</dt> <dt>

[**Ianalysisregion:: excluderegion-Methode**](ianalysisregion-excluderegion.md)
</dt> <dt>

[**Ianalysisregion:: intersectrechteck-Methode**](ianalysisregion-intersectrectangle.md)
</dt> <dt>

[**Ianalysisregion:: intersectregion-Methode**](ianalysisregion-intersectregion.md)
</dt> <dt>

[**Ianalysisregion:: unionregion-Methode**](ianalysisregion-unionregion.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

 




