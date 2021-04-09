---
description: Verschiebt den angegebenen iinkanalysiserkenzer an die erste Position in der Liste der frei Hand erkenungen des iinkanalyzer-Objekts.
ms.assetid: 9126187f-02dd-4988-91b8-c4f3d3b6f773
title: 'Iinkanalyzer:: sethighestpriorityinkanalysiserkenzer-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SetHighestPriorityInkAnalysisRecognizer
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 534b94e4f2964aa81f04e0adac6f45f346c530c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862683"
---
# <a name="iinkanalyzersethighestpriorityinkanalysisrecognizer-method"></a>Iinkanalyzer:: sethighestpriorityinkanalysiserkenzer-Methode

Verschiebt den angegebenen [**iinkanalysiserkenzer**](iinkanalysisrecognizer.md) an die erste Position in der Liste der frei Hand erkenungen des [**iinkanalyzer**](iinkanalyzer.md) -Objekts.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetHighestPriorityInkAnalysisRecognizer(
  [in] IInkAnalysisRecognizer *pInkAnalysisRecognizer
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pinkanalysiserkenzer* \[ in\]
</dt> <dd>

Der [**iinkanalysiserkenzer**](iinkanalysisrecognizer.md) , der an der ersten Position platziert werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

Um die Liste der frei Hand erkenungen in der Reihenfolge der Priorität abzurufen, wenden Sie sich an die [**iinkanalyzer:: getinkanalysiserkenzersbypriority-Methode**](iinkanalyzer-getinkanalysisrecognizersbypriority.md).

Diese Methode wirkt sich nicht auf die Reihenfolge der restlichen [**iinkanalysiserkenzer**](iinkanalysisrecognizer.md) -Objekte in der Liste der frei Hand erkenungen des [**iinkanalyzer**](iinkanalyzer.md) -Objekts aus.

Die Reihenfolge der von der [**iinkanalyzer:: getinkanalysiserkenzersbypriority-Methode**](iinkanalyzer-getinkanalysisrecognizersbypriority.md) zurückgegebenen Handschrift erkenungen gibt die Reihenfolge an, in der [**iinkanalyzer**](iinkanalyzer.md) die verfügbaren [**iinkanalysiserkenzer**](iinkanalysisrecognizer.md) -Objekte auswertet.

Die Verwendung der frei Hand erkenungen wird basierend auf ihrer Reihenfolge in der Liste ausgewertet.

Während der Handschrift Analyse durchläuft [**iinkanalyzer**](iinkanalyzer.md) die frei Hand erkenungen in der Liste, bis eine Erkennung gefunden wird, die die Sprache und andere Eigenschaften der Striche unterstützt. Diese Erkennung wird zur frei Handerkennung für diese Striche verwendet.

Wenn [**iinkanalyzer**](iinkanalyzer.md) keinen [**iinkanalysiserkenzer**](iinkanalysisrecognizer.md) findet, der einen Satz von Strichen während der Analyse unterstützt, generiert **iinkanalyzer** eine [**ianalysiswarning**](ianalysiswarning.md) mit dem Warnungs Code **AnalysisWarningCode \_ inkanalysiserkenzernotinstallierte** (siehe [**ianalysiswarning:: getwarningcode**](ianalysiswarning-getwarningcode.md)).

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

[**Iinkanalyzer:: getinkanalysiserkenzersbypriority-Methode**](iinkanalyzer-getinkanalysisrecognizersbypriority.md)
</dt> <dt>

[**Iinkanalysiserkenzers**](iinkanalysisrecognizers.md)
</dt> <dt>

[**Ianalysiswarning**](ianalysiswarning.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

 




