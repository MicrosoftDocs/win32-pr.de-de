---
description: Gibt die Strichbezeichner zurück, die diesem IAnalysisAlternate zugeordnet sind.
ms.assetid: 495d485f-0d16-4085-9213-cc55f3f259f0
title: IAnalysisAlternate::GetStrokeIds-Methode (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternate.GetStrokeIds
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 2682107a58f126011c4d80a02a119219ccea0976408937e19eb7b511eb82cff9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967499"
---
# <a name="ianalysisalternategetstrokeids-method"></a>IAnalysisAlternate::GetStrokeIds-Methode

Gibt die Strichbezeichner zurück, die diesem [**IAnalysisAlternate**](ianalysisalternate.md)zugeordnet sind.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetStrokeIds(
  [in, out] ULONG *pulStrokeIdsCount,
  [out]     LONG  **pplStrokeIds
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pulStrokeIdsCount* \[ in, out\]
</dt> <dd>

Ein Zeiger auf ein **ULONG,** das auf die Anzahl der Strichbezeichner festgelegt ist, die diesem [**IAnalysisAlternate**](ianalysisalternate.md)zugeordnet sind.

</dd> <dt>

*pplStrokeIds* \[ out\]
</dt> <dd>

\[out, size \_ is( \* *pulStrokeIdsCount* \* sizeof(LONG))\]

Ein Array von **LONG** der Länge *pulStrokeIdsCount,* das auf die Strichbezeichner festgelegt ist, die diesem [**IAnalysisAlternate**](ianalysisalternate.md)zugeordnet sind.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter Klassen und Schnittstellen – [Ink-Analyse.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Hinweise

> [!Caution]  
> Um einen Speicherverlust zu vermeiden, verwenden Sie [CoTaskMemFree,](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) um den Arbeitsspeicher von \* *pplStrokeIds* freizugeben, wenn Sie die Informationen nicht mehr benötigen.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (erfordert auch IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IAnalysisAlternate**](ianalysisalternate.md)
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

