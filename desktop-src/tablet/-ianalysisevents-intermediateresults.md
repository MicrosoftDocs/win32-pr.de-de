---
description: Tritt ein, wenn die aktuelle Zwischenanalysephase abgeschlossen ist.
ms.assetid: 9ade61f4-bcfe-4c49-bda1-b60aaf780935
title: _IAnalysisEvents::IntermediateResults-Ereignis (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisEvents.IntermediateResults
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 9efead00094fdcd773c3ac90b0d626e2036030171bcf3be011323b6da70fb665
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117857196"
---
# <a name="_ianalysiseventsintermediateresults-event"></a>\_IAnalysisEvents::IntermediateResults-Ereignis

Tritt ein, wenn die aktuelle Zwischenanalysephase abgeschlossen ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT IntermediateResults(
  [in] IInkAnalyzer    *pInkAnalyzer,
  [in] IAnalysisStatus *pAnalysisStatus
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pInkAnalyzer* \[ In\]
</dt> <dd>

Der [**IInkAnalyzer,**](iinkanalyzer.md) der die Analyse durchführen soll.

</dd> <dt>

*pAnalysisStatus* \[ In\]
</dt> <dd>

Das [**IAnalysisStatus-Objekt,**](ianalysisstatus.md) das den Status der Zwischenergebnisse darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen – Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Hinweise

Der [**IInkAnalyzer löst**](iinkanalyzer.md) dieses Ereignis aus, nachdem er die Zwischenergebnisse für die aktuelle Analysephase abgeglichen hat.

Wenn Ihre Anwendung eine eigene Datenstruktur verwaltet, die mit der von [**IInkAnalyzer**](iinkanalyzer.md)synchronisiert wird, gibt dieses Ereignis an, dass **der IInkAnalyzer** die Änderungen an seinen internen Daten für diese Analysephase abgeschlossen hat.

Sperren Sie Ihre Datenstruktur, wenn [**IInkAnalyzer**](iinkanalyzer.md) das [**\_ IAnalysisProxyEvents::InkAnalyzerStateChanging-Ereignis**](-ianalysisproxyevents-inkanalyzerstatechanging.md) löst. Änderungen an Ihrer Datenstruktur während dieser Analysephase können Fehler bei der Ink-Analyse und -Synchronisierung verursachen. Sie können Ihre Datenstruktur entsperren, wenn **der IInkAnalyzer** das **\_ IAnalysisEvents::IntermediateResults-** oder [**\_ IAnalysisEvents::Results-Ereignis ausgibt.**](-ianalysisevents-results.md)

Weitere Informationen zum Synchronisieren Ihrer Anwendungsdaten mit [**IInkAnalyzer**](iinkanalyzer.md)finden Sie unter [Datenproxy mit Ink-Analyse.](data-proxy-with-ink-analysis.md)

Der [**IInkAnalyzer**](iinkanalyzer.md) generiert Nur dann Zwischenergebnisse, wenn für seine Analysemodi das **AnalysisModes \_ IntermediateResults-Flag** festgelegt ist (siehe [**IInkAnalyzer::GetAnalysisModes-Methode**](iinkanalyzer-getanalysismodes.md)).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (erfordert auch IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**\_IAnalysisEvents**](-ianalysisevents.md)
</dt> <dt>

[**Analysismodes**](analysismodes.md)
</dt> <dt>

[**\_IAnalysisEvents::Results**](-ianalysisevents-results.md)
</dt> <dt>

[**\_IAnalysisProxyEvents**](-ianalysisproxyevents.md)
</dt> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IInkAnalyzer::Analyze-Methode**](iinkanalyzer-analyze.md)
</dt> <dt>

[**IInkAnalyzer::BackgroundAnalyze-Methode**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>
