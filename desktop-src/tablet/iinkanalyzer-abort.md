---
description: Bricht den aktuellen Analyse Vorgang ab.
ms.assetid: 909bfa66-b6df-4730-95b7-809fc2170e85
title: 'Iinkanalyzer:: Abort-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.Abort
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: eac96809bfbe41e7d6a070782da3ffd0f6407c60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349013"
---
# <a name="iinkanalyzerabort-method"></a>Iinkanalyzer:: Abort-Methode

Bricht den aktuellen Analyse Vorgang ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT Abort(
  [out] IAnalysisRegion **ppAbortedRegion
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppabortedregion* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen [**ianalysisregion**](ianalysisregion.md) , der den geänderten Bereich darstellt (siehe [**iinkanalyzer:: getdirtyregion-Methode**](iinkanalyzer-getdirtyregion.md)) des aktuellen Analyse Vorgangs.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

Nennen Sie [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) für *ppabortedregion* , wenn Sie das-Objekt nicht mehr verwenden müssen.

Mit dieser Methode wird der aktuelle Analyse Vorgang abgebrochen.

Wenn *ppabortedregion* den Wert **null** hat, führt diese Methode den Abbruch wie üblich aus, da dies darauf hinweist, dass der Aufrufer keinen Interesse am Rückgabewert hat.

Die **iinkanalyzer:: Abort-Methode** deaktiviert die [**\_ ianalysisevents:: results**](-ianalysisevents-results.md) -und [**\_ ianalysisevents:: Activity**](-ianalysisevents-activity.md) -Ereignisse für den aktuellen Analyse Vorgang.

Die **iinkanalyzer:: Abort-Methode** wird asynchron ausgeführt, bis der aktuelle Hintergrundanalyse Vorgang abgebrochen wird. Da der abbruchprozess asynchron ist, kann die Anwendung andere Aufgaben ausführen, während die aktuellen Analyse Operations abgebrochen werden.

Wenn keine Analyse Vorgänge ausgeführt werden, gibt diese Methode einen leeren Analysebereich zurück.

Wenn ein Analyse Vorgang ausgeführt wird, bricht diese Methode den Vorgang ab.

Wenn synchrone und asynchrone Analyse Vorgänge ausgeführt werden, bricht diese Methode den synchronen Vorgang ab.

Wenn diese Methode mehrmals für denselben Analyse Vorgang aufgerufen wird, gibt der erste Aufruf den geänderten Bereich für den Vorgang zurück, und die nachfolgenden Aufrufe geben einen leeren Bereich zurück.

Wenn Ihre Anwendung ihre eigene Datenstruktur verwaltet, die mit der von [**iinkanalyzer**](iinkanalyzer.md)synchronisiert ist, kann durch das Aufrufen der **iinkanalyzer:: Abort-Methode** das Dokument mit partiellen Ergebnissen belassen werden. Um dies zu vermeiden, müssen Sie die **iinkanalyzer:: Abort-Methode** nicht zwischen dem Zeitpunkt aufrufen, an dem der **iinkanalyzer** das [**\_ ianalysisproxyevents:: InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md) -Ereignis empfängt, und dem Zeitpunkt, an dem **iinkanalyzer** das [**\_ ianalysitsvents::**](-ianalysisevents-intermediateresults.md) - [**\_ results**](-ianalysisevents-results.md) -Ereignis empfängt.

Weitere Informationen zum Synchronisieren Ihrer Anwendungsdaten mit der Ink Analyzer finden Sie unter [Daten Proxy mit Ink-Analyse](data-proxy-with-ink-analysis.md).

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

[**Iinkanalyzer:: getdirtyregion-Methode**](iinkanalyzer-getdirtyregion.md)
</dt> <dt>

[**Iinkanalyzer:: setdirtyregion-Methode**](iinkanalyzer-setdirtyregion.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

