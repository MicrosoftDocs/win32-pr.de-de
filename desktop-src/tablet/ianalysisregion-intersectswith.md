---
description: Bestimmt, ob sich der Bereich des ianalysisregion mit dem angegebenen Rechteck überschneidet.
ms.assetid: 683c3ad8-0236-474e-a16d-6164c2244cfb
title: 'Ianalysisregion:: interseczwith-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.IntersectsWith
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 99ff1ce8d3039b04d83f9cdd5c1d6aebe00be407
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526552"
---
# <a name="ianalysisregionintersectswith-method"></a>Ianalysisregion:: interseczwith-Methode

Bestimmt, ob sich der Bereich des [**ianalysisregion**](ianalysisregion.md) mit dem angegebenen Rechteck überschneidet.

## <a name="syntax"></a>Syntax


```C++
HRESULT IntersectsWith(
  [in]  RECT         *pRectangle,
  [out] VARIANT_BOOL *pfIsIntersecting
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*prätangle* \[ in\]
</dt> <dd>

Ein Zeiger auf das Rechteck, mit dem in den Freihand Raumkoordinaten verglichen werden soll.

</dd> <dt>

*pfisintersecting* \[ vorgenommen\]
</dt> <dd>

**Variant \_ TRUE** , wenn sich der Bereich von [**ianalysisregion**](ianalysisregion.md) mit dem angegebenen Rechteck überschneidet. Andernfalls ist der Wert **\_ false**.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

Der Vergleich erfolgt in freistellungenkoordinaten.

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

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

 




