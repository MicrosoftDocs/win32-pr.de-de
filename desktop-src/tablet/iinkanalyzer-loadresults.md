---
description: Lädt gespeicherte Analyseergebnisse in IInkAnalyzer.
ms.assetid: 7634dbe2-1857-497c-81b5-76b92fed862d
title: IInkAnalyzer::LoadResults-Methode (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.LoadResults
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 47f385334f1b16f3d7de46b8cfc53ee6b94f485c9768f973b745af335cd5c12f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119713380"
---
# <a name="iinkanalyzerloadresults-method"></a>IInkAnalyzer::LoadResults-Methode

Lädt gespeicherte Analyseergebnisse in [**IInkAnalyzer.**](iinkanalyzer.md)

## <a name="syntax"></a>Syntax


```C++
HRESULT LoadResults(
  [in]          ULONG        ulDataSize,
  [in]          BYTE         *pbSerializedResults,
  [in]          ULONG        ulStrokeIdsCount,
  [in]          LONG         *plOriginalStrokeIds,
  [in]          LONG         *plNewStrokeIds,
  [out, retval] VARIANT_BOOL *pfSuccessful
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ulDataSize* \[ In\]
</dt> <dd>

Die Anzahl der Bytes in *pbSerializedResults.*

</dd> <dt>

*pbSerializedResults* \[ In\]
</dt> <dd>

Die serialisierten Analyseergebnisse.

</dd> <dt>

*ulStrokeIdsCount* \[ In\]
</dt> <dd>

Die Anzahl der Strichbezeichner.

</dd> <dt>

*plOriginalStrokeIds* \[ In\]
</dt> <dd>

Das Array ursprünglicher Strichbezeichner.

</dd> <dt>

*plNewStrokeIds* \[ In\]
</dt> <dd>

Das Array neuer Strichbezeichner.

</dd> <dt>

*pfSuccessful* \[ out, retval\]
</dt> <dd>

**VARIANT \_ TRUE,** wenn das Laden erfolgreich war; Andernfalls **VARIANT \_ FALSE**.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter Klassen und Schnittstellen – [Ink-Analyse.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Hinweise

Wenn [**IInkAnalyzer**](iinkanalyzer.md) einen [**IContextNode**](icontextnode.md) aus den gespeicherten Ergebnissen hinzufügt, weist er dem **IContextNode** einen neuen guid (Globally Unique Identifier) zu (siehe [**IContextNode::GetPropertyData**](icontextnode-getpropertydata.md) und [Kontextknoteneigenschaften](context-node-properties.md)).

Diese Methode fügt die gespeicherten Analyseergebnisse der vorhandenen [**IContextNode-Struktur**](icontextnode.md) hinzu. Um sicherzustellen, dass die kombinierten Ergebnisse ordnungsgemäß sortiert sind, fügen Sie den Bereich mit den geladenen Kontextknoten dem geänderten Bereich des [**IInkAnalyzer-Objekts**](iinkanalyzer.md) hinzu (siehe [**IInkAnalyzer::GetDirtyRegion-Methode),**](iinkanalyzer-getdirtyregion.md)undanalysieren Sie die Freihand erneut.

Die [**IInkAnalyzer::SaveResults-Methode,**](iinkanalyzer-saveresults.md) [**die IInkAnalyzer::SaveResultsForNodes-Methode**](iinkanalyzer-saveresultsfornodes.md)und die [**IInkAnalyzer::SaveResultsForStrokes-Methode**](iinkanalyzer-saveresultsforstrokes.md) speichern die Paketdaten nicht zusammen mit den Analyseergebnissen.

Jeder Bezeichner in *plOriginalStrokeIds* ist der Strichbezeichner für den Strich in den gespeicherten Analyseergebnissen. Jeder Bezeichner in *plNewStrokeIds* ist der neue Bezeichner, durch den der ursprüngliche Bezeichner in den geladenen Analyseergebnissen ersetzt werden soll.

Wenn ein gespeicherter Analysehinweis mit einem vorhandenen Analysehinweis in Konflikt steht, lädt [**IInkAnalyzer**](iinkanalyzer.md) den gespeicherten Hinweis nicht, sondern die restlichen gespeicherten Ergebnisse. Wenn der **IInkAnalyzer** jedoch Ergebnisse für einen Strich lädt, der sich im Bereich eines gespeicherten Analysehinweises befindet, dass der **IInkAnalyzer** nicht geladen wird, fügt **IInkAnalyzer** den Begrenzungsbereich des Strichs dem geänderten Bereich des **IInkAnalyzer-Objekts** hinzu. Wenn der **IInkAnalyzer** Ergebnisse für einen Strich lädt, der sich im Bereich eines vorhandenen Analysehinweises befindet, fügt **der IInkAnalyzer** auch den Begrenzungsbereich des Strichs dem geänderten Bereich des **IInkAnalyzer-Objekts** hinzu. Weitere Informationen zu Analysehinweisen finden Sie unter [Analysis Hint Properties](analysis-hint-properties.md).

Diese Methode kann die Ereignisse [**\_ IAnalysisProxyEvents::ContextNodeCreated,**](-ianalysisproxyevents-contextnodecreated.md) [**\_ IAnalysisProxyEvents::ContextNodeLinkAdding**](-ianalysisproxyevents-contextnodelinkadding.md)und [**\_ IAnalysisProxyEvents::ContextNodePropertiesUpdated**](-ianalysisproxyevents-contextnodepropertiesupdated.md) auslösen, während die gespeicherten Ergebnisse geladen werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (erfordert auch IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**IInkAnalyzer::GetDirtyRegion-Methode**](iinkanalyzer-getdirtyregion.md)
</dt> <dt>

[**IInkAnalyzer::SetDirtyRegion-Methode**](iinkanalyzer-setdirtyregion.md)
</dt> <dt>

[**IInkAnalyzer::SaveResults-Methode**](iinkanalyzer-saveresults.md)
</dt> <dt>

[**IInkAnalyzer::SaveResultsForNodes-Methode**](iinkanalyzer-saveresultsfornodes.md)
</dt> <dt>

[**IInkAnalyzer::SaveResultsForStrokes-Methode**](iinkanalyzer-saveresultsforstrokes.md)
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

 




