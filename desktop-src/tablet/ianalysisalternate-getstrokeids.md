---
description: Gibt die Strich Bezeichner zurück, die diesem ianalysisalternate-Element zugeordnet sind.
ms.assetid: 495d485f-0d16-4085-9213-cc55f3f259f0
title: 'Ianalysisalternate:: GetStrokeIds-Methode (iacom. h)'
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
ms.openlocfilehash: 80882a83e9a0fa9bf973990a689e2abf1a52a870
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862731"
---
# <a name="ianalysisalternategetstrokeids-method"></a>Ianalysisalternate:: GetStrokeIds-Methode

Gibt die Strich Bezeichner zurück, die diesem [**ianalysisalternate**](ianalysisalternate.md)-Element zugeordnet sind.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetStrokeIds(
  [in, out] ULONG *pulStrokeIdsCount,
  [out]     LONG  **pplStrokeIds
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pulstrokeidscount* \[ in, out\]
</dt> <dd>

Ein Zeiger auf einen **ulong** -Wert, der auf die Anzahl von Strich Bezeichners festgelegt ist, die diesem [**ianalysisalternate**](ianalysisalternate.md)-Element zugeordnet sind.

</dd> <dt>

*pplstrokeids* \[ vorgenommen\]
</dt> <dd>

\[Out, size \_ ist ( \* *pulstrokeidscount* \* sizeof (Long))\]

Ein Array von **Long** der Länge *pulstrokeidscount* , das auf die Strich Bezeichner festgelegt wird, die mit diesem [**ianalysisalternate**](ianalysisalternate.md)verknüpft sind.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

> [!Caution]  
> Um einen Speicherplatz zu vermeiden, verwenden Sie " [CoTaskMemFree](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) ", um den Arbeitsspeicher aus \* *pplstrokeids* freizugeben, wenn Sie die Informationen nicht mehr benötigen.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Iacom. h (erfordert auch iacom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ianalysisalternate**](ianalysisalternate.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

