---
description: Führt synchrone frei Hand Eingaben aus.
ms.assetid: 957845f3-96b4-4184-aaec-e266cbe47e46
title: 'Iinkanalyzer:: Analysis-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.Analyze
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 2867064067b902105508a7742c6fec88fdcd58be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345738"
---
# <a name="iinkanalyzeranalyze-method"></a>Iinkanalyzer:: analysierungsmethode

Führt synchrone frei Hand Eingaben aus.

## <a name="syntax"></a>Syntax


```C++
HRESULT Analyze(
  [out] IAnalysisStatus **ppStatus
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppstatus* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen [**ianalysisstatus**](ianalysisstatus.md) , der den Status des Analyse Vorgangs beschreibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

> [!Caution]  
> Um einen Speicherplatz zu vermeiden, nennen Sie [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) für *ppstatus* , wenn Sie den Analyse Status nicht mehr verwenden müssen.

 

Diese Methode startet einen Vorgang für die synchrone frei Hand Eingabe. Die frei Hand Analyse umfasst layoutanalysen, schreiben und Zeichnen von Klassifizierungen und Handschrifterkennung. Diese Methode gibt zurück, nachdem der Analyse Vorgang beendet wurde.

Diese Methode gibt einen **E- \_ Zeiger** zurück, wenn *ppstatus* **null** ist.

Während eines Aufrufens der **iinkanalyzer:: Analysis-Methode** oder der [**iinkanalyzer:: BackgroundAnalyze-Methode**](iinkanalyzer-backgroundanalyze.md)analysiert [**iinkanalyzer**](iinkanalyzer.md) frei Hand Eingaben innerhalb des geänderten Bereichs (siehe [**iinkanalyzer:: getdirtyregion-Methode**](iinkanalyzer-getdirtyregion.md)). Allerdings kann der **iinkanalyzer** den Analyse Vorgang erweitern, um benachbarte Regionen einzubeziehen.

Diese Methode legt den geänderten Bereich des [**iinkanalyzer**](iinkanalyzer.md) -Objekts auf einen leeren Bereich fest. Wenn von einem anderen Thread noch nicht analysierte Stroke-Daten hinzugefügt wurden, fügt **iinkanalyzer** das umgebende Feld der nicht analysierten Striche während der ababstimmungs Phase der Analyse dem geänderten Bereich hinzu.

Diese Methode gibt einen Fehler zurück, wenn die Anwendung das [**\_ ianalysisevents:: updatestrokescache**](-ianalysisevents-updatestrokescache.md) -Ereignis nicht behandelt.

Der [**iinkanalyzer**](iinkanalyzer.md) gibt nicht die [**\_ ianalysitsvents:: results**](-ianalysisevents-results.md) -und [**\_ ianalysitsvents:: IntermediateResults**](-ianalysisevents-intermediateresults.md) -Ereignisse als Reaktion auf diese Methode aus.

Verwenden Sie die [**iinkanalyzer:: setanalysismodes-Methode**](iinkanalyzer-setanalysismodes.md), um die Art der Datenflussanalyse zu ändern

Weitere Informationen zur frei Hand Analyse finden Sie unter Übersicht über die Handschrift [Analyse](ink-analysis-overview.md).

## <a name="examples"></a>Beispiele

Das folgende Beispiel führt eine Vordergrund-Ink-Analyse durch


```C++
// Perform synchronous ink analysis.
IAnalysisStatus *pAnalysisStatus = NULL;
hr = this->m_spIInkAnalyzer->Analyze(&pAnalysisStatus);

if (SUCCEEDED(hr))
{
    // Insert code that processes the analysis results.
}

// Release this reference to the analysis status.
if (pAnalysisStatus != NULL)
{
    pAnalysisStatus->Release();
    pAnalysisStatus = NULL;
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

[**Iinkanalyzer:: getdirtyregion-Methode**](iinkanalyzer-getdirtyregion.md)
</dt> <dt>

[**Iinkanalyzer:: setdirtyregion-Methode**](iinkanalyzer-setdirtyregion.md)
</dt> <dt>

[**Iinkanalyzer:: GetRootNode-Methode**](iinkanalyzer-getrootnode.md)
</dt> <dt>

[**Iinkanalyzer:: BackgroundAnalyze-Methode**](iinkanalyzer-backgroundanalyze.md)
</dt> </dl>

 

