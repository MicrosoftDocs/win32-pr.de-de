---
description: Ruft den Fehlercode für den Hintergrund-Ink-Analysevorgang ab, wenn ein Fehler aufgetreten ist.
ms.assetid: 0255751e-9b2a-46f1-aa45-6509f9d1c658
title: IAnalysisWarning::GetBackgroundError-Methode (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisWarning.GetBackgroundError
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: aa8c9c3c60f51ffd854ccdfebb6538337e7676a8c63e45899737333c41d99aad
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057960"
---
# <a name="ianalysiswarninggetbackgrounderror-method"></a>IAnalysisWarning::GetBackgroundError-Methode

Ruft den Fehlercode für den Hintergrund-Ink-Analysevorgang ab, wenn ein Fehler aufgetreten ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetBackgroundError();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter Klassen und Schnittstellen – [Ink-Analyse.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Hinweise

Wenn ein Fehler innerhalb eines Hintergrundanalysevorgangs auftritt, kann [**IInkAnalyzer**](iinkanalyzer.md) den Fehlercode nicht zurückgeben, da er in einem anderen Thread auftritt. Stattdessen empfängt der [**\_ IAnalysisEvents::Results-Ereignishandler**](-ianalysisevents-results.md) einen [**IAnalysisStatus,**](ianalysisstatus.md) der ein [**IAnalysisWarning**](ianalysiswarning.md) mit einem [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) von **AnalysisWarningCode \_ BackgroundException** enthält. Diese **IAnalysisWarning** enthält den Fehlercode für den Hintergrundanalysevorgang. Im Allgemeinen gibt der **\_ IAnalysisEvents::Results-Ereignishandler** diesen Fehlercode zurück, damit er an anderer Stelle in Ihrer Anwendung behandelt werden kann.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (erfordert auch IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IAnalysisWarning**](ianalysiswarning.md)
</dt> <dt>

[**IAnalysisStatus**](ianalysisstatus.md)
</dt> <dt>

[**IInkAnalyzer::BackgroundAnalyze-Methode**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[**\_IAnalysisEvents::Results**](-ianalysisevents-results.md)
</dt> <dt>

[**Analysiswarningcode**](/windows/desktop/tablet/analysiswarningcode)
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

