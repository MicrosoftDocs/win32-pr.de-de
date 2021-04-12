---
description: Führt eine asynchrone Handschrift Analyse aus.
ms.assetid: 36427b80-5e3b-4c9a-bb49-e6b7f9301cbd
title: 'Iinkanalyzer:: BackgroundAnalyze-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.BackgroundAnalyze
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 606e1444f66884564a6b9f2007adfc26b2eb2ed1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526504"
---
# <a name="iinkanalyzerbackgroundanalyze-method"></a>Iinkanalyzer:: BackgroundAnalyze-Methode

Führt eine asynchrone Handschrift Analyse aus.

## <a name="syntax"></a>Syntax


```C++
HRESULT BackgroundAnalyze();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

Wenn diese Methode aufgerufen wird, führt [**iinkanalyzer**](iinkanalyzer.md) die Handschrift Analyse in einem Hintergrund Thread aus.

Diese Methode gibt **S \_ false** zurück und startet unter den folgenden Umständen keinen neuen Hintergrundanalyse Vorgang.

-   [**Iinkanalyzer**](iinkanalyzer.md) führt zurzeit eine Hintergrundanalyse durch.
-   der geänderte Bereich (siehe [**iinkanalyzer:: getdirtyregion-Methode**](iinkanalyzer-getdirtyregion.md)) stellt einen leeren Bereich dar.

Der [**iinkanalyzer**](iinkanalyzer.md) analysiert frei Hand Eingaben innerhalb des geänderten Bereichs während eines Aufrufes der [**iinkanalyzer:: Analysis-Methode**](iinkanalyzer-analyze.md) oder der **iinkanalyzer:: BackgroundAnalyze-Methode**. Allerdings kann der **iinkanalyzer** den Analyse Vorgang erweitern, um benachbarte Regionen einzubeziehen.

Diese Methode legt den geänderten Bereich auf einen leeren Bereich fest.

Wenn dem [**iinkanalyzer**](iinkanalyzer.md) nach dem Ansichts Vorgang der **iinkanalyzer:: BackgroundAnalyze-Methode** Stroke-Daten hinzugefügt wurden, kann der **iinkanalyzer** den geänderten Bereich während der ababstimmungs Phase der frei Hand Analyse aktualisieren.

Die Einstellung für die Analyse Modi (siehe [**iinkanalyzer:: getanalysismodes-Methode**](iinkanalyzer-getanalysismodes.md)) gibt an, wie [**iinkanalyzer**](iinkanalyzer.md) eine Hintergrundanalyse ausführt. Weitere Informationen zur frei Hand Analyse finden Sie unter Übersicht über die Handschrift [Analyse](ink-analysis-overview.md).

Diese Methode gibt unter den folgenden Umständen einen Fehlercode zurück.

-   Die Anwendung hat den [**AnalysisModes**](analysismodes.md) -Wert **AnalysisModes \_** in der [**iinkanalyzer**](iinkanalyzer.md) -Methode festgelegt (siehe [**iinkanalyzer:: setanalysismodes-Methode**](iinkanalyzer-setanalysismodes.md)) und behandelt nicht das [**\_ ianalysisevents:: IntermediateResults**](-ianalysisevents-intermediateresults.md) -Ereignis.
-   Die Anwendung hat den [**AnalysisModes**](analysismodes.md) -Wert **AnalysisModes \_ automatikreversöhnung** in [**iinkanalyzer**](iinkanalyzer.md) gelöscht (siehe [**iinkanalyzer:: setanalysismodes-Methode**](iinkanalyzer-setanalysismodes.md)) und behandelt nicht das [**\_ ianalysisevents:: Read ytoreconcile**](-ianalysisevents-readytoreconcile.md) -Ereignis.
-   Das [**\_ ianalysisevents:: results**](-ianalysisevents-results.md) -Ereignis wird von der Anwendung nicht behandelt.
-   Das [**\_ ianalysisevents:: updatestrokescache**](-ianalysisevents-updatestrokescache.md) -Ereignis wird von der Anwendung nicht behandelt.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird der geänderte Bereich der Ink Analyzer überprüft und dann die Hintergrund-Ink-Analyse initiiert, wenn der geänderte Bereich nicht leer ist.


```C++
// Check that the ink analyzer's dirty region is not empty.
IAnalysisRegion *pDirtyRegion;
hr = this->m_spIInkAnalyzer->GetDirtyRegion(&pDirtyRegion);

if (SUCCEEDED(hr))
{
    VARIANT_BOOL bIsEmpty;
    hr = pDirtyRegion->IsEmpty(&bIsEmpty);

    if (SUCCEEDED(hr))
    {
        if (!bIsEmpty)
        {
            // Insert code that prepares the application for background
            // ink analysis here.

            // Start background ink analysis. The _IAnalysisEvents::Results
            // event signals when background ink analysis is complete.
            hr = this->m_spIInkAnalyzer->BackgroundAnalyze();
        }
    }
}

// Free the memory for the dirty region.
if (pDirtyRegion != NULL)
{
    pDirtyRegion->Release();
}
```



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

[**AnalysisModes**](analysismodes.md)
</dt> <dt>

[**Iinkanalyzer:: analysierungsmethode**](iinkanalyzer-analyze.md)
</dt> <dt>

[**Iinkanalyzer:: getanalysismodes-Methode**](iinkanalyzer-getanalysismodes.md)
</dt> <dt>

[**Iinkanalyzer:: abtanalysismodes-Methode**](iinkanalyzer-setanalysismodes.md)
</dt> <dt>

[**Iinkanalyzer:: getdirtyregion-Methode**](iinkanalyzer-getdirtyregion.md)
</dt> <dt>

[**Iinkanalyzer:: setdirtyregion-Methode**](iinkanalyzer-setdirtyregion.md)
</dt> <dt>

[**Iinkanalyzer:: GetRootNode-Methode**](iinkanalyzer-getrootnode.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

 




