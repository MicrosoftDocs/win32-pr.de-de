---
description: Ruft das iinkanalysiserkenzer-Element am angegebenen Index ab.
ms.assetid: e4db56c6-7c15-4336-bc0a-f50222c3520e
title: 'Iinkanalysiserkenzers:: getinkanalysiserkenzer-Methode (iacom. h)'
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
ms.openlocfilehash: 1008ae0b26d30233c3b00167391523d321cd381e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485091"
---
# <a name="iinkanalysisrecognizersgetinkanalysisrecognizer-method"></a>Iinkanalysiserkenzers:: getinkanalysiserkenzer-Methode

Ruft das [**iinkanalysiserkenzer**](iinkanalysisrecognizer.md) -Element am angegebenen Index ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetInkAnalysisRecognizer(
  [in]  ULONG                  ulIndex,
  [out] IInkAnalysisRecognizer **ppInkAnalysisRecognizer
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ulindex* \[ in\]
</dt> <dd>

Der null basierte Index des abzurufenden [**iinkanalysiserkenzer**](iinkanalysisrecognizer.md) -Objekts.

</dd> <dt>

*ppinkanalysiserkenzer* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf [**iinkanalysiserkenzer**](iinkanalysisrecognizer.md) am angegebenen Index.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

> [!Caution]  
> Um einen Speicherplatz zu vermeiden, nennen Sie [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) für \* *ppinkanalysiserkenzer* , wenn Sie die Handschrifterkennung nicht mehr verwenden müssen.

 

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

 

