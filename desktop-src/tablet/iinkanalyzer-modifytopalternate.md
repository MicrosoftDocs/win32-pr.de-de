---
description: Ändert die aktuelle obere Alternative in die angegebene Alternative und löscht den Bestätigungstyp für alle IContextNode-Objekte, die der Alternativen zugeordnet sind.
ms.assetid: a4ff7e82-623f-4501-9641-5235c3083757
title: IInkAnalyzer::ModifyTopAlternate-Methode (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.ModifyTopAlternate
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: b35cda4534bc5c791e4815c584f6da5d9972c018283b6c9385f6bad998187505
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092040"
---
# <a name="iinkanalyzermodifytopalternate-method"></a>IInkAnalyzer::ModifyTopAlternate-Methode

Ändert die aktuelle obere Alternative in die angegebene Alternative und löscht den Bestätigungstyp für alle [**IContextNode-Objekte,**](icontextnode.md) die der Alternativen zugeordnet sind.

## <a name="syntax"></a>Syntax


```C++
HRESULT ModifyTopAlternate(
  [in] IAnalysisAlternate *pAlternate
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pAlternate* \[ In\]
</dt> <dd>

Das [**IAnalysisAlternate-Objekt,**](ianalysisalternate.md) das die neue obere Alternative enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter Klassen und Schnittstellen – [Ink-Analyse.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Hinweise

Verwenden Sie zum Abrufen alternativer Analysemethoden [**die IInkAnalyzer::GetAlternates-Methode,**](iinkanalyzer-getalternates.md) [**die IInkAnalyzer::GetAlternatesForContextNodes-Methode**](iinkanalyzer-getalternatesforcontextnodes.md)oder die [**IInkAnalyzer::GetAlternatesForStrokes-Methode.**](iinkanalyzer-getalternatesforstrokes.md) Verwenden Sie die [**IAnalysisAlternate::GetAlternateNodes-Methode,**](ianalysisalternate-getalternatenodes.md)um die [**IContextNode-Objekte**](icontextnode.md) abzurufen, die einer alternativen Analyse zugeordnet sind.

Verwenden Sie [**IContextNode::Confirm**](icontextnode-confirm.md), um den Bestätigungstyp für einen Kontextknoten zu ändern.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (erfordert auch IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IAnalysisAlternate**](ianalysisalternate.md)
</dt> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**ConfirmationType**](confirmationtype.md)
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

 




