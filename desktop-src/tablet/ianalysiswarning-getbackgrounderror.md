---
description: Ruft den Fehlercode für den Vorgang der Hintergrund Handschrift Analyse ab, wenn ein Fehler aufgetreten ist.
ms.assetid: 0255751e-9b2a-46f1-aa45-6509f9d1c658
title: 'Ianalysiswarning:: getbackgrounderror-Methode (iacom. h)'
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
ms.openlocfilehash: 4367b1d52ee5d2a3bb65af0e4edd4922b8ae9a92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214677"
---
# <a name="ianalysiswarninggetbackgrounderror-method"></a>Ianalysiswarning:: getbackgrounderror-Methode

Ruft den Fehlercode für den Vorgang der Hintergrund Handschrift Analyse ab, wenn ein Fehler aufgetreten ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetBackgroundError();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

Wenn ein Fehler in einem Hintergrundanalyse Vorgang auftritt, kann [**iinkanalyzer**](iinkanalyzer.md) den Fehlercode nicht zurückgeben, da er in einem anderen Thread auftritt. Stattdessen erhält der [**\_ ianalysisevents:: results**](-ianalysisevents-results.md) -Ereignishandler einen [**ianalysisstatus**](ianalysisstatus.md) , der eine [**ianalysiswarning**](ianalysiswarning.md) mit einem [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) von **AnalysisWarningCode \_ BackgroundException** enthält. Dieses **ianalysiswarning** -Element enthält den Fehlercode für den Hintergrundanalyse Vorgang. Im Allgemeinen gibt der **\_ ianalysisevents:: results** -Ereignishandler diesen Fehlercode zurück, sodass er an anderer Stelle in der Anwendung behandelt werden kann.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Iacom. h (erfordert auch iacom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ianalysiswarning**](ianalysiswarning.md)
</dt> <dt>

[**Ianalysisstatus**](ianalysisstatus.md)
</dt> <dt>

[**Iinkanalyzer:: BackgroundAnalyze-Methode**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[**\_Ianalysil Vents:: results**](-ianalysisevents-results.md)
</dt> <dt>

[**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

