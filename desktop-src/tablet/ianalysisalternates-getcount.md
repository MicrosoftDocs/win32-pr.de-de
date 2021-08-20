---
description: Ruft die Anzahl der IAnalysisAlternate-Objekte ab, die in der IAnalysisAlternates-Auflistung enthalten sind.
ms.assetid: 17b71b5a-638a-4e6e-a43b-4ca3c8eba257
title: IAnalysisAlternates::GetCount-Methode (IACom.h)
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
ms.openlocfilehash: 84ff5941d4db6ca569c8a7a10a622e4b3dcdfc947284064fa009e030adae1493
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967489"
---
# <a name="ianalysisalternatesgetcount-method"></a>IAnalysisAlternates::GetCount-Methode

Ruft die Anzahl der [**IAnalysisAlternate-Objekte**](ianalysisalternate.md) ab, die in der [**IAnalysisAlternates-Auflistung enthalten**](ianalysisalternates.md) sind.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetCount(
  [out] ULONG *pulCount
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pulCount* \[ out\]
</dt> <dd>

Eine 32-Bit-Ganzzahl ohne Vorzeichen, die auf die Anzahl der [**IAnalysisAlternate-Objekte**](ianalysisalternate.md) in der [**IAnalysisAlternates-Auflistung festgelegt**](ianalysisalternates.md) ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen – Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (erfordert auch IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IAnalysisAlternates**](ianalysisalternates.md)
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

 




