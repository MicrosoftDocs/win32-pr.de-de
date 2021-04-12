---
description: Ändert den Bereich, der seit dem letzten Analyse Vorgang geändert wurde.
ms.assetid: 1484fd96-2791-4583-b13b-e5a8275ecb0e
title: 'Iinkanalyzer:: setdirtyregion-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SetDirtyRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 72278dd9fe1d772d4ef340d25694d42f9c48ed7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129440"
---
# <a name="iinkanalyzersetdirtyregion-method"></a>Iinkanalyzer:: setdirtyregion-Methode

Ändert den Bereich, der seit dem letzten Analyse Vorgang geändert wurde.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetDirtyRegion(
  [in] IAnalysisRegion *pDirtyRegion
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pdirtyregion* \[ in\]
</dt> <dd>

Eine [**ianalysisregion**](ianalysisregion.md) , die den Bereich beschreibt, der seit dem letzten Analyse Vorgang geändert wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

Mit dieser Methode werden die Bereiche identifiziert, die analysiert oder erneut analysiert werden müssen. Alle [**iinkanalyzer**](iinkanalyzer.md) -Methoden, die Strich Daten hinzufügen, aktualisieren oder entfernen, aktualisieren den geänderten Bereich. So markieren Sie einen Bereich manuell für eine erneute Analyse:

1.  Der geänderte Bereich wird mithilfe der [**iinkanalyzer:: getdirtyregion-Methode abgerufen**](iinkanalyzer-getdirtyregion.md).
2.  Verwenden Sie die [**ianalysisregion:: unionregion-Methode**](ianalysisregion-unionregion.md) oder die [**ianalysisregion:: unionrechteck-Methode**](ianalysisregion-unionrectangle.md) , um den Bereich aus Schritt 1 dem Bereich hinzuzufügen.
3.  Verwenden Sie die **iinkanalyzer:: setdirtyregion-Methode** , um den geänderten Bereich zu aktualisieren.

Der [**iinkanalyzer**](iinkanalyzer.md) analysiert frei Hand Eingaben innerhalb des geänderten Bereichs während eines Aufrufes der [**iinkanalyzer:: Analysis-Methode**](iinkanalyzer-analyze.md) oder der [**iinkanalyzer:: BackgroundAnalyze-Methode**](iinkanalyzer-backgroundanalyze.md). Allerdings kann der **iinkanalyzer** den Analyse Vorgang erweitern, um benachbarte Regionen einzubeziehen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Iacom. h (erfordert auch iacom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iinkanalyzer**](iinkanalyzer.md)
</dt> <dt>

[**Iinkanalyzer:: analysierungsmethode**](iinkanalyzer-analyze.md)
</dt> <dt>

[**Iinkanalyzer:: BackgroundAnalyze-Methode**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[**Iinkanalyzer:: AddStroke-Methode**](iinkanalyzer-addstroke.md)
</dt> <dt>

[**Iinkanalyzer:: addstrokeforlanguage-Methode**](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[**Iinkanalyzer:: AddStrokes-Methode**](iinkanalyzer-addstrokes.md)
</dt> <dt>

[**Iinkanalyzer:: addstrokesforlanguage-Methode**](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[**Iinkanalyzer:: RemoveStroke-Methode**](iinkanalyzer-removestroke.md)
</dt> <dt>

[**Iinkanalyzer:: RemoveStrokes-Methode**](iinkanalyzer-removestrokes.md)
</dt> <dt>

[**Iinkanalyzer:: UpdateStrokesData-Methode**](iinkanalyzer-updatestrokesdata.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

 




