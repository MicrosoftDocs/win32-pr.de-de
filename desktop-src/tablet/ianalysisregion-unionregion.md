---
description: Erweitert den Bereich dieses ianalysisregion auf den Bereich, der von seiner Union mit dem angegebenen ianalysisregion erstellt wurde.
ms.assetid: cc3ec5c6-98ff-442e-a1e8-d1a57752ad56
title: 'Ianalysisregion:: unionregion-Methode (iacom. h)'
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
ms.openlocfilehash: 587986973c4ae4bebaeed3c031c746bc4f842c42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368100"
---
# <a name="ianalysisregionunionregion-method"></a>Ianalysisregion:: unionregion-Methode

Erweitert den Bereich dieses [**ianalysisregion**](ianalysisregion.md) auf den Bereich, der von seiner Union mit dem angegebenen **ianalysisregion** erstellt wurde.

## <a name="syntax"></a>Syntax


```C++
HRESULT UnionRegion(
  [in] IAnalysisRegion *pRegionToUnion
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pregionin Union* \[ in\]
</dt> <dd>

Der [**ianalysisregion**](ianalysisregion.md) , mit dem kombiniert werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

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

[**Ianalysisregion:: unionrechteck-Methode**](ianalysisregion-unionrectangle.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

 




