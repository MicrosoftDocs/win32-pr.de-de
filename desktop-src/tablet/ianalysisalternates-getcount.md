---
description: Ruft die Anzahl der ianalysisalternate-Objekte ab, die in der ianalysisalteraten-Auflistung enthalten sind.
ms.assetid: 17b71b5a-638a-4e6e-a43b-4ca3c8eba257
title: 'Ianalysisalteraten:: GetCount-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternates.GetCount
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 6300ff994d7bd49461e9be39aa433586ecaabc75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360054"
---
# <a name="ianalysisalternatesgetcount-method"></a>Ianalysisalterniert:: GetCount-Methode

Ruft die Anzahl der [**ianalysisalternate**](ianalysisalternate.md) -Objekte ab, die in der [**ianalysisalteraten**](ianalysisalternates.md) -Auflistung enthalten sind.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetCount(
  [out] ULONG *pulCount
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pulCount* \[ vorgenommen\]
</dt> <dd>

Eine Ganzzahl ohne Vorzeichen 32 ohne Vorzeichen, die auf die Anzahl der [**ianalysisalternate**](ianalysisalternate.md) -Objekte festgelegt ist, die in der [**ianalysisalteraten**](ianalysisalternates.md) -Auflistung enthalten sind.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Iacom. h (erfordert auch iacom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ianalysisalteraten**](ianalysisalternates.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

 




