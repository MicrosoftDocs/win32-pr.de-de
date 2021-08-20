---
description: Tritt auf, wenn die IInkAnalyzer::Analyze-Methode oder die IInkAnalyzer::BackgroundAnalyze-Methode aufgerufen wird.
ms.assetid: 339b41c6-f388-4b81-b2bc-3705b39d9cc9
title: _IAnalysisEvents::Activity-Ereignis (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisEvents.Activity
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: bc0a0fd1ad5434116dc7333899329384eae4b9c6dbf7c386e1e2e048f8431d21
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118047360"
---
# <a name="_ianalysiseventsactivity-event"></a>\_IAnalysisEvents::Activity-Ereignis

Tritt auf, wenn die [**IInkAnalyzer::Analyze-Methode**](iinkanalyzer-analyze.md) oder [**die IInkAnalyzer::BackgroundAnalyze-Methode**](iinkanalyzer-backgroundanalyze.md) aufgerufen wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT Activity();
```



## <a name="parameters"></a>Parameter

Dieses Ereignis verfügt über keine Parameter.

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen – Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Hinweise

Dieses Ereignis gibt an, dass [**der IInkAnalyzer**](iinkanalyzer.md) eine Ink-Analyse vorgibt. Dieses Ereignis gibt nicht den Fortschritt des Ink-Analyse-Vorgangs an.

Implementieren Sie einen **\_ IAnalysisEvents::Activity-Ereignishandler,** um eine der folgenden Aufgaben zu erstellen:

-   Geben Sie dem Benutzer an, dass die Ink-Analyse durchgeführt wird.
-   Verarbeiten von Benutzereingaben während der synchronen Analyse.
-   Empfangen von Benachrichtigungen über Systemanforderungen, z. B. das Neupaintieren des Anwendungsfensters, während der Ink-Analyse.

Der [**IInkAnalyzer**](iinkanalyzer.md) löst dieses Ereignis häufig während der Layoutanalysephase und der Schreib- und Zeichnungklassifizierungsphase der Ink-Analyse aus. Der **IInkAnalyzer löst** dieses Ereignis während der Handschrifterkennungsphase vor und nach dem Zugriff auf eine Ink-Erkennung aus.

Die Anzahl der Aktivitätsereignisse, die [**von IInkAnalyzer**](iinkanalyzer.md) generiert werden, ist von folgenden Faktoren betroffen:

-   Die Ink-Erkennung, die der [**IInkAnalyzer**](iinkanalyzer.md) auf die Ink-Erkennung angewendet.
-   Die Anzahl und Länge der Striche, die der [**IInkAnalyzer**](iinkanalyzer.md) analysiert.
-   Die Anzahl der Striche, die als Schreiben klassifiziert sind.

Weitere Informationen zum Synchronisieren Ihrer Anwendungsdaten mit [**IInkAnalyzer**](iinkanalyzer.md)finden Sie unter [Datenproxy mit Ink-Analyse.](data-proxy-with-ink-analysis.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (erfordert auch IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_IAnalysisEvents**](-ianalysisevents.md)
</dt> <dt>

[**\_IAnalysisProxyEvents**](-ianalysisproxyevents.md)
</dt> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)
</dt> <dt>

[**IInkAnalyzer::Analyze-Methode**](iinkanalyzer-analyze.md)
</dt> <dt>

[**IInkAnalyzer::BackgroundAnalyze-Methode**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

 




