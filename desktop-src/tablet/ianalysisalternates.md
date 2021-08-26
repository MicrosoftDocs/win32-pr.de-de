---
description: Enthält eine Auflistung von -Objekten, die die IAnalysisAlternate-Schnittstelle implementieren und das Ergebnis der Ink-Analyse sind.
ms.assetid: 53802a62-4425-40fd-bf48-0da55ea8ffbe
title: IAnalysisAlternates-Schnittstelle (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternates
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: e2643ef8ea90d029aee6bd0673931d27e9987b0af0a898e854cb87d74a89c0af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120058090"
---
# <a name="ianalysisalternates-interface"></a>IAnalysisAlternates-Schnittstelle

Enthält eine Auflistung von -Objekten, die die [**IAnalysisAlternate-Schnittstelle**](ianalysisalternate.md) implementieren und das Ergebnis der Ink-Analyse sind.

## <a name="members"></a>Member

Die **IAnalysisAlternates-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IAnalysisAlternates** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IAnalysisAlternates-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                   | BESCHREIBUNG                                                                                                                                      |
|:-------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetAnalysisAlternate**](ianalysisalternates-getanalysisalternate.md) | Ruft das [**IAnalysisAlternate-Objekt**](ianalysisalternate.md) am angegebenen Index in der Auflistung ab.<br/>                   |
| [**GetCount**](ianalysisalternates-getcount.md)                         | Ruft die Anzahl der [**IAnalysisAlternate-Objekte**](ianalysisalternate.md) ab, die in der **IAnalysisAlternates-Auflistung enthalten** sind.<br/> |



 

## <a name="remarks"></a>Hinweise

Diese Schnittstelle entspricht der [**System.Windows. Ink.AnalysisCore.AnalysisAlternateBaseCollection-Klasse**](/previous-versions/ms610094(v=vs.100)) im .NET Framework.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (erfordert auch IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IAnalysisAlternate**](ianalysisalternate.md)
</dt> <dt>

[**IInkAnalyzer::GetAlternates-Methode**](iinkanalyzer-getalternates.md)
</dt> <dt>

[**IInkAnalyzer::GetAlternatesForContextNodes-Methode**](iinkanalyzer-getalternatesforcontextnodes.md)
</dt> <dt>

[**IInkAnalyzer::GetAlternatesForStrokes-Methode**](iinkanalyzer-getalternatesforstrokes.md)
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

