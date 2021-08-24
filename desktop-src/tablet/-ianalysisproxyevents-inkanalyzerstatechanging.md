---
description: Tritt ein, bevor IInkAnalyzer Analyseergebnisse abgleicht, sodass eine Anwendung Daten mit dem IInkAnalyzer synchronisieren kann.
ms.assetid: 9daa8723-5234-40d9-ac41-6dcca988a8b4
title: _IAnalysisProxyEvents::InkAnalyzerStateChanging-Ereignis (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.InkAnalyzerStateChanging
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: d4e32685e25e4c942b3c723df2152b1064bed59599fda54fcac00e22aab04206
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119884080"
---
# <a name="_ianalysisproxyeventsinkanalyzerstatechanging-event"></a>\_IAnalysisProxyEvents::InkAnalyzerStateChanging-Ereignis

Tritt auf, bevor [**IInkAnalyzer**](iinkanalyzer.md) Analyseergebnisse abgleicht, sodass eine Anwendung Daten mit dem **IInkAnalyzer** synchronisieren kann.

## <a name="syntax"></a>Syntax


```C++
HRESULT InkAnalyzerStateChanging(
  [in] IInkAnalyzer *pInkAnalyzer
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pInkAnalyzer* \[ In\]
</dt> <dd>

Der [**IInkAnalyzer,**](iinkanalyzer.md) der seine Analyseergebnisse abstimmen soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter Klassen und Schnittstellen – [Ink-Analyse.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Hinweise

Verwenden Sie dieses Ereignis, wenn Ihre Anwendung ihre eigene Datenstruktur verwaltet, die mit der des [**IInkAnalyzer**](iinkanalyzer.md)synchronisiert wird. Wenn **IInkAnalyzer** dieses Ereignis auslöst, sollte Ihre Anwendung die Unterknoten des Stammknotens des Freihandanalysetools auffüllen (siehe [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md) und [**IInkAnalyzer::GetRootNode-Methode).**](iinkanalyzer-getrootnode.md)

[**IInkAnalyzer**](iinkanalyzer.md) löst dieses Ereignis aus, nachdem es das [**\_ IAnalysisEvents::ReadyToReconcile-Ereignis**](-ianalysisevents-readytoreconcile.md) auslöst. Dieses Ereignis wird nur bei der Hintergrundanalyse auslöst.

Sperren Sie Ihre Datenstruktur, wenn [**IInkAnalyzer**](iinkanalyzer.md) das **\_ IAnalysisProxyEvents::InkAnalyzerStateChanging-Ereignis** auslöst. Änderungen an der Datenstruktur während dieser Phase der Analyse können Fehler bei der Ink-Analyse und -Synchronisierung verursachen. Entsperren Sie Ihre Datenstruktur, wenn **IInkAnalyzer** das [**\_ Ereignis IAnalysisEvents::IntermediateResults**](-ianalysisevents-intermediateresults.md) oder [**\_ IAnalysisEvents::Results**](-ianalysisevents-results.md) auslöst.

Weitere Informationen zum Synchronisieren Ihrer Anwendungsdaten mit [**IInkAnalyzer**](iinkanalyzer.md)finden Sie unter [Datenproxy mit Freihandanalyse.](data-proxy-with-ink-analysis.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (erfordert auch IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**\_IAnalysisProxyEvents**](-ianalysisproxyevents.md)
</dt> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**IInkAnalyzer::Analyze-Methode**](iinkanalyzer-analyze.md)
</dt> <dt>

[**IInkAnalyzer::BackgroundAnalyze-Methode**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

 




