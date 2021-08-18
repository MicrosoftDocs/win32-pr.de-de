---
description: Ruft Analysewechsel für die Knoten in einer angegebenen IContextNodes-Auflistung ab.
ms.assetid: 7d047808-4360-442d-8fd9-4ee4aeeed2c9
title: IInkAnalyzer::GetAlternatesForContextNodes-Methode (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetAlternatesForContextNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: bc282906bae70a28f612a8c1fd0a5a67ea1343c73f5ededf0d6c85a8bfd60aa0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939859"
---
# <a name="iinkanalyzergetalternatesforcontextnodes-method"></a>IInkAnalyzer::GetAlternatesForContextNodes-Methode

Ruft Analysewechsel für die Knoten in einer angegebenen [**IContextNodes-Auflistung**](icontextnodes.md) ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetAlternatesForContextNodes(
  [in]  IContextNodes      *pContextNodes,
  [in]  ULONG              ulMaximumAlternates,
  [out] AnalysisAlternates **ppAlternates
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pContextNodes* \[ In\]
</dt> <dd>

Die [**IContextNodes-Auflistung,**](icontextnodes.md) für die die Analysealternativen zurückgegeben werden.

</dd> <dt>

*ulMaximumAlternates* \[ In\]
</dt> <dd>

Die maximale Anzahl von Alternativen, die zurückgegeben werden sollen.

</dd> <dt>

*ppAlternates* \[ out\]
</dt> <dd>

Das [**IAnalysisAlternates-Objekt,**](ianalysisalternates.md) das die Analysealternativen enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter Klassen und Schnittstellen – [Ink-Analyse.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Hinweise

> [!Caution]  
> Um einen Speicherverlust zu vermeiden, rufen Sie [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) auf *ppAlternates* auf, wenn Sie das Objekt nicht mehr verwenden müssen.

 

Das oberste [**IAnalysisAlternate**](ianalysisalternate.md) wird als erste Alternative der Auflistung zurückgegeben.

Die [**IContextNode-Objekte**](icontextnode.md) in *pContextNodes* müssen keine angrenzenden Bereiche des Dokuments darstellen.

Für jeden Analysehinweis in Knoten gibt [**IInkAnalyzer**](iinkanalyzer.md) nur die obere Alternative zurück.

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

[**IAnalysisAlternate**](ianalysisalternate.md)
</dt> <dt>

[**IAnalysisAlternates**](ianalysisalternates.md)
</dt> <dt>

[**IInkAnalyzer::GetAlternates-Methode**](iinkanalyzer-getalternates.md)
</dt> <dt>

[**IInkAnalyzer::GetAlternatesForStrokes-Methode**](iinkanalyzer-getalternatesforstrokes.md)
</dt> <dt>

[**IInkAnalyzer::ModifyTopAlternate-Methode**](iinkanalyzer-modifytopalternate.md)
</dt> <dt>

[**IInkAnalyzer::ModifyTopAlternateWithConfirmation-Methode**](iinkanalyzer-modifytopalternatewithconfirmation.md)
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

