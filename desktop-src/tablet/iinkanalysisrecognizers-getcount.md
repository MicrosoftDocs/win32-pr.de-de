---
description: Ruft die Anzahl der iinkanalysiserkenzer-Objekte in dieser Auflistung ab.
ms.assetid: dfb5c530-b481-4c60-b7fe-87fe162de270
title: 'Iinkanalysiserkenzers:: GetCount-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizers.GetCount
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: e65f8399c661d551e805abe5f1c5db33eb0b154a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526510"
---
# <a name="iinkanalysisrecognizersgetcount-method"></a>Iinkanalysiserkenzers:: GetCount-Methode

Ruft die Anzahl der [**iinkanalysiserkenzer**](iinkanalysisrecognizer.md) -Objekte in dieser Auflistung ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetCount(
  [out, retval] ULONG *pulCount
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pulCount* \[ Out, retval\]
</dt> <dd>

Die Anzahl der [**iinkanalysiserkenzer**](iinkanalysisrecognizer.md) -Objekte in dieser Auflistung.

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

[**Inkanalysiserkenzers**](iinkanalysisrecognizers.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

 




