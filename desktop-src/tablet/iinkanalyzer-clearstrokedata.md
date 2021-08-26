---
description: Löscht Strichpaketdaten aus IInkAnalyzer.
ms.assetid: c87a1e73-5e3f-4d27-93e9-e30d9ec5d9e3
title: IInkAnalyzer::ClearStrokeData-Methode (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.ClearStrokeData
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 3413d8d6fb322030afdcffb97e8739ae4ca5e2314fe968f366ce25e58d90351e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057870"
---
# <a name="iinkanalyzerclearstrokedata-method"></a>IInkAnalyzer::ClearStrokeData-Methode

Löscht Strichpaketdaten aus dem [**IInkAnalyzer.**](iinkanalyzer.md)

## <a name="syntax"></a>Syntax


```C++
HRESULT ClearStrokeData(
  [in] LONG lStrokeId
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lStrokeId* \[ In\]
</dt> <dd>

Der Bezeichner des Strichs, für den die Paketdaten gelöscht werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter Klassen und Schnittstellen – [Ink-Analyse.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Hinweise

Verwenden Sie diese Methode, wenn sich Paketdaten für einen Strich ändern, z. B. wenn ein Strich verschoben oder anderweitig transformiert wird. [**IInkAnalyzer**](iinkanalyzer.md) löst das [**\_ IAnalysisEvents::UpdateStrokesCache-Ereignis**](-ianalysisevents-updatestrokescache.md) aus, wenn Strichpaketdaten von einem Strich benötigt werden, für den die Paketdaten gelöscht wurden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (erfordert auch IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IInkAnalyzer::UpdateStrokesData-Methode**](iinkanalyzer-updatestrokesdata.md)
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

 




