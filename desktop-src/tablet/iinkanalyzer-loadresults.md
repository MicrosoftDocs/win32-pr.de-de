---
description: Lädt gespeicherte Analyseergebnisse in iinkanalyzer.
ms.assetid: 7634dbe2-1857-497c-81b5-76b92fed862d
title: 'Iinkanalyzer:: loadresults-Methode (iacom. h)'
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
ms.openlocfilehash: 76c7fed63b38f1b4fc058fbe7676a727c2d47f19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485075"
---
# <a name="iinkanalyzerloadresults-method"></a>Iinkanalyzer:: loadresults-Methode

Lädt gespeicherte Analyseergebnisse in [**iinkanalyzer**](iinkanalyzer.md).

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

*uldatasize* \[ in\]
</dt> <dd>

Die Anzahl von Bytes in *pbserializedresults*.

</dd> <dt>

*pbserializedresults* \[ in\]
</dt> <dd>

Die serialisierten Analyseergebnisse.

</dd> <dt>

*ulstrokeidscount* \[ in\]
</dt> <dd>

Die Anzahl der Strich Bezeichner.

</dd> <dt>

*ploriginalstrokeids* \[ in\]
</dt> <dd>

Das Array der ursprünglichen Strich Bezeichner.

</dd> <dt>

*plnewstrokeids* \[ in\]
</dt> <dd>

Das Array neuer Strich Bezeichner.

</dd> <dt>

*pferfolgreich* \[ Out, retval\]
</dt> <dd>

**Variant \_ TRUE** , wenn das Laden erfolgreich war. Andernfalls ist der Wert **\_ false**.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

Wenn [**iinkanalyzer**](iinkanalyzer.md) aus den gespeicherten Ergebnissen einen [**icontextnode**](icontextnode.md) hinzufügt, wird dem **icontextnode** eine neue Globally Unique Identifier (GUID) zugewiesen (siehe [**icontextnode:: GetPropertyData**](icontextnode-getpropertydata.md) und [Kontext Knoten Eigenschaften](context-node-properties.md)).

Mit dieser Methode werden die gespeicherten Analyseergebnisse der vorhandenen [**icontextnode**](icontextnode.md) -Struktur hinzugefügt. Um sicherzustellen, dass die kombinierten Ergebnisse ordnungsgemäß geordnet sind, fügen Sie den Bereich mit den geladenen Kontext Knoten dem geänderten Bereich des [**iinkanalyzer**](iinkanalyzer.md) -Objekts hinzu (siehe [**iinkanalyzer:: getdirtyregion-Methode**](iinkanalyzer-getdirtyregion.md)), und analysieren Sie die frei Hand Eingaben erneut.

Die Methoden Methoden [**iinkanalyzer:: SaveResults**](iinkanalyzer-saveresults.md), [**iinkanalyzer:: saveresultsfornodes**](iinkanalyzer-saveresultsfornodes.md)und [**iinkanalyzer:: saveresultsforstriche**](iinkanalyzer-saveresultsforstrokes.md) speichern die Paketdaten nicht zusammen mit den Analyseergebnissen.

Jeder Bezeichner in *ploriginalstrokeids* ist der Strich Bezeichner für den Strich in den gespeicherten Analyseergebnissen. Jeder Bezeichner in *plnewstrokeids* ist der neue Bezeichner, mit dem der ursprüngliche Bezeichner in den geladenen Analyseergebnissen ersetzt werden soll.

Wenn ein gespeicherter Analyse Hinweis einen Konflikt mit einem vorhandenen Analyse Hinweis verursacht, lädt der [**iinkanalyzer**](iinkanalyzer.md) den gespeicherten Hinweis nicht, lädt jedoch die restlichen gespeicherten Ergebnisse. Wenn jedoch **iinkanalyzer** Ergebnisse für einen Strich lädt, der sich innerhalb des Bereichs eines gespeicherten Analyse Hinweises befindet, dass der **iinkanalyzer** nicht geladen wird, fügt **iinkanalyzer** das umgebende Feld des Strichs dem geänderten Bereich des **iinkanalyzer** -Objekts hinzu. Wenn **iinkanalyzer** Ergebnisse für einen Strich lädt, der sich innerhalb eines vorhandenen Analyse Hinweises befindet, fügt der **iinkanalyzer** auch das umgebende Feld des Strichs dem geänderten Bereich des **iinkanalyzer** -Objekts hinzu. Weitere Informationen zu Analyse hinweisen finden Sie unter [Eigenschaften des Analysis-Hinweises](analysis-hint-properties.md).

Diese Methode kann die Ereignisse [**\_ ianalysisproxyevents:: ContextNodeCreated**](-ianalysisproxyevents-contextnodecreated.md), [**\_ ianalysisproxyevents:: contextnodelta inkadditions**](-ianalysisproxyevents-contextnodelinkadding.md)und [**\_ ianalysisproxyevents:: contextnodepropertiesaktualisierten**](-ianalysisproxyevents-contextnodepropertiesupdated.md) beim Laden der gespeicherten Ergebnisse hervorrufen.

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

[**Icontextnode**](icontextnode.md)
</dt> <dt>

[**Iinkanalyzer:: getdirtyregion-Methode**](iinkanalyzer-getdirtyregion.md)
</dt> <dt>

[**Iinkanalyzer:: setdirtyregion-Methode**](iinkanalyzer-setdirtyregion.md)
</dt> <dt>

[**Iinkanalyzer:: SaveResults-Methode**](iinkanalyzer-saveresults.md)
</dt> <dt>

[**Iinkanalyzer:: saveresultsfornodes-Methode**](iinkanalyzer-saveresultsfornodes.md)
</dt> <dt>

[**Iinkanalyzer:: saveresultsforstrokes-Methode**](iinkanalyzer-saveresultsforstrokes.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

 




