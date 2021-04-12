---
description: Schränkt den Bereich dieses ianalysisregion auf den Bereich ein, der durch die Schnittmenge mit dem angegebenen Rechteck erstellt wurde.
ms.assetid: de6b565f-34c1-4551-ab92-db6bacb8608d
title: 'Ianalysisregion:: intersectrechteck-Methode (iacom. h)'
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
ms.openlocfilehash: 4ce0e514b24aba0331d9ea604333680db1c67c8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526555"
---
# <a name="ianalysisregionintersectrectangle-method"></a>Ianalysisregion:: intersectrechteck-Methode

Schränkt den Bereich dieses [**ianalysisregion**](ianalysisregion.md) auf den Bereich ein, der durch die Schnittmenge mit dem angegebenen Rechteck erstellt wurde.

## <a name="syntax"></a>Syntax


```C++
HRESULT IntersectRectangle(
  [in] RECT *pIntersectingRectangle
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pintersectingrechteck* \[ in\]
</dt> <dd>

Ein Zeiger auf das Rechteck, mit dem die Schnittmenge in Freihand Raumkoordinaten gebildet werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

Die Rechteck Koordinaten befinden sich in HIMETRIC-Einheiten.

Wenn sich die beiden Bereiche nicht überschneiden, ist der neue Bereich leer.

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

[**Ianalysisregion:: intersectregion-Methode**](ianalysisregion-intersectregion.md)
</dt> <dt>

[**Ianalysisregion:: unionrechteck-Methode**](ianalysisregion-unionrectangle.md)
</dt> <dt>

[**Ianalysisregion:: unionregion-Methode**](ianalysisregion-unionregion.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

 




