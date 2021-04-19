---
description: Schränkt den Bereich von ianalysisregion auf den Bereich ein, der durch die Schnittmenge mit der angegebenen ianalysisregion erstellt wurde.
ms.assetid: 02b3049f-ada9-4de3-a7a2-f9ff8313fbab
title: 'Ianalysisregion:: intersectregion-Methode (iacom. h)'
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
ms.openlocfilehash: 7ff3caad382e54f41685f6102edafdeb86b813c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345126"
---
# <a name="ianalysisregionintersectregion-method"></a>Ianalysisregion:: intersectregion-Methode

Schränkt den Bereich von [**ianalysisregion**](ianalysisregion.md) auf den Bereich ein, der durch die Schnittmenge mit der angegebenen **ianalysisregion** erstellt wurde.

## <a name="syntax"></a>Syntax


```C++
HRESULT IntersectRegion(
  [in] IAnalysisRegion *pRegionToIntersect
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pregionintersect* \[ in\]
</dt> <dd>

Der [**ianalysisregion**](ianalysisregion.md) , mit der die Schnittmenge gebildet werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

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

[**Ianalysisregion:: intersectrechteck-Methode**](ianalysisregion-intersectrectangle.md)
</dt> <dt>

[**Ianalysisregion:: unionrechteck-Methode**](ianalysisregion-unionrectangle.md)
</dt> <dt>

[**Ianalysisregion:: unionregion-Methode**](ianalysisregion-unionregion.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

 




