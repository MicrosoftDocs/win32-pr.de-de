---
description: Enthält eine Auflistung von-Objekten, die die ianalysisalternate-Schnittstelle implementieren und die das Ergebnis der frei Hand Analyse sind.
ms.assetid: 53802a62-4425-40fd-bf48-0da55ea8ffbe
title: Ianalysisalteraten-Schnittstelle (iacom. h)
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
ms.openlocfilehash: 4e43feaa40f519707531894936bf34ce19e57723
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106372839"
---
# <a name="ianalysisalternates-interface"></a>Ianalysisalteraten-Schnittstelle

Enthält eine Auflistung von-Objekten, die die [**ianalysisalternate**](ianalysisalternate.md) -Schnittstelle implementieren und die das Ergebnis der frei Hand Analyse sind.

## <a name="members"></a>Member

Die **ianalysisalteraten** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Ianalysisalteraten** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ianalysisalteraten** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                   | BESCHREIBUNG                                                                                                                                      |
|:-------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Getanalysisalternate**](ianalysisalternates-getanalysisalternate.md) | Ruft das [**ianalysisalternate**](ianalysisalternate.md) -Objekt am angegebenen Index in der Collection ab.<br/>                   |
| [**GetCount**](ianalysisalternates-getcount.md)                         | Ruft die Anzahl der [**ianalysisalternate**](ianalysisalternate.md) -Objekte ab, die in der **ianalysisalteraten** -Auflistung enthalten sind.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Schnittstelle entspricht der [**System. Windows. Ink. AnalysisCore. AnalysisAlternateBaseCollection**](/previous-versions/ms610094(v=vs.100)) -Klasse in der .NET Framework.

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

[**Iinkanalyzer:: getalteraten-Methode**](iinkanalyzer-getalternates.md)
</dt> <dt>

[**Iinkanalyzer:: getalternatesforcontextnodes-Methode**](iinkanalyzer-getalternatesforcontextnodes.md)
</dt> <dt>

[**Iinkanalyzer:: getalternatesforstrokes-Methode**](iinkanalyzer-getalternatesforstrokes.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

