---
description: Schränkt den Bereich von ianalysisregion auf den Teil des Bereichs ein, der den angegebenen ianalysisregion nicht überschneidet.
ms.assetid: 7a11d2a8-c2ca-4088-b932-8a6c3e789b7f
title: 'Ianalysisregion:: excluderegion-Methode (iacom. h)'
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
ms.openlocfilehash: 13324d872a76a9184e6ea67b227dbd7444684bb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526558"
---
# <a name="ianalysisregionexcluderegion-method"></a>Ianalysisregion:: excluderegion-Methode

Schränkt den Bereich von [**ianalysisregion**](ianalysisregion.md) auf den Teil des Bereichs ein, der den angegebenen **ianalysisregion** nicht überschneidet.

## <a name="syntax"></a>Syntax


```C++
HRESULT ExcludeRegion(
  [in] IAnalysisRegion *pRegionToExclude
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pregionto Exclude* \[ in\]
</dt> <dd>

Der [**ianalysisregion**](ianalysisregion.md) , der aus dieser **ianalysisregion** ausgeschlossen werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

Wenn sich die beiden Bereiche nicht überschneiden, wird dieser [**ianalysisregion**](ianalysisregion.md) unverändert.

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

 

 




