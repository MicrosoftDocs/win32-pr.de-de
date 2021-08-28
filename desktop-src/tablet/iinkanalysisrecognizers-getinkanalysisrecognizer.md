---
description: Ruft den IInkAnalysisRecognizer am angegebenen Index ab.
ms.assetid: e4db56c6-7c15-4336-bc0a-f50222c3520e
title: IInkAnalysisRecognizers::GetInkAnalysisRecognizer-Methode (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizers.GetInkAnalysisRecognizer
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 6755b82beaea1bec9a38b9c15ea57a97c1d19fc4eecb5a2b55c80e2070562d07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967339"
---
# <a name="iinkanalysisrecognizersgetinkanalysisrecognizer-method"></a>IInkAnalysisRecognizers::GetInkAnalysisRecognizer-Methode

Ruft den [**IInkAnalysisRecognizer am**](iinkanalysisrecognizer.md) angegebenen Index ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetInkAnalysisRecognizer(
  [in]  ULONG                  ulIndex,
  [out] IInkAnalysisRecognizer **ppInkAnalysisRecognizer
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ulIndex* \[ In\]
</dt> <dd>

Der nullbasierte Index des [**zu erhaltenden IInkAnalysisRecognizer-Objekts.**](iinkanalysisrecognizer.md)

</dd> <dt>

*ppInkAnalysisRecognizer* \[ out\]
</dt> <dd>

Ein Zeiger auf den [**IInkAnalysisRecognizer am**](iinkanalysisrecognizer.md) angegebenen Index.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen – Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Hinweise

> [!Caution]  
> Um einen Arbeitsspeicherverlust zu vermeiden, rufen Sie [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) auf \* *ppInkAnalysisRecognizer* auf, wenn Sie die Freitextanalyse-Recognizer nicht mehr verwenden müssen.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (erfordert auch IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**InkAnalysisRecognizers**](iinkanalysisrecognizers.md)
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

