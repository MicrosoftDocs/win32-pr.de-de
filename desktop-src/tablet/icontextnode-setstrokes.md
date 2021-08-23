---
description: Ordnet diesem IContextNode die angegebenen Striche zu.
ms.assetid: 5ce8893a-da59-4cec-a349-d5ffc4f43905
title: IContextNode::SetStrokes-Methode (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.SetStrokes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 67834a10e5e08070c991af76fe19b720853789a9f5e2c771f5c1ed0dc4fc9754
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119552600"
---
# <a name="icontextnodesetstrokes-method"></a>IContextNode::SetStrokes-Methode

Ordnet diesem [**IContextNode die angegebenen Striche zu.**](icontextnode.md)

## <a name="syntax"></a>Syntax


```C++
HRESULT SetStrokes(
  [in] ULONG ulStrokeIdsCount,
  [in] LONG  *plStrokeIds
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ulStrokeIdsCount* \[ In\]
</dt> <dd>

Die Anzahl der Strichbezeichner in *plStrokeIds*.

</dd> <dt>

*plStrokeIds* \[ In\]
</dt> <dd>

Die Bezeichner der Striche, die diesem [**IContextNode -Objekt zugeordnet werden.**](icontextnode.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen – Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Hinweise

Diese Methode aktualisiert nicht den geänderten Bereich des Ink Analyzers (siehe [**IInkAnalyzer::GetDirtyRegion-Methode**](iinkanalyzer-getdirtyregion.md)).

Verwenden Sie diese Methode, wenn Ihre Anwendung eine eigene Datenstruktur verwaltet, die mit der von [**IInkAnalyzer synchronisiert wird.**](iinkanalyzer.md) Verwenden Sie diese Methode, um einem bestimmten Kontextknoten Strichdaten zu zuweisen. Weitere Informationen zum Synchronisieren Ihrer Anwendungsdaten mit **IInkAnalyzer** finden Sie unter [Datenproxy mit Ink-Analyse.](data-proxy-with-ink-analysis.md)

Wenn einer der angegebenen Striche bereits dem [**IInkAnalyzer**](iinkanalyzer.md)zugeordnet ist, gibt diese Methode **E \_ INVALIDARG zurück.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (erfordert auch IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**IInkAnalyzer::AddStroke-Methode**](iinkanalyzer-addstroke.md)
</dt> <dt>

[**IInkAnalyzer::AddStrokeForLanguage-Methode**](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[**IInkAnalyzer::AddStrokes-Methode**](iinkanalyzer-addstrokes.md)
</dt> <dt>

[**IInkAnalyzer::AddStrokesForLanguage-Methode**](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[**IInkAnalyzer::AddStrokesToCustomRecognizer-Methode**](iinkanalyzer-addstrokestocustomrecognizer.md)
</dt> <dt>

[**IInkAnalyzer::AddStrokeToCustomRecognizer-Methode**](iinkanalyzer-addstroketocustomrecognizer.md)
</dt> <dt>

[**IInkAnalyzer::RemoveStroke-Methode**](iinkanalyzer-removestroke.md)
</dt> <dt>

[**IInkAnalyzer::RemoveStrokes-Methode**](iinkanalyzer-removestrokes.md)
</dt> <dt>

[**IContextNode::GetStrokeId**](icontextnode-getstrokeid.md)
</dt> <dt>

[**IContextNode::GetStrokeIds**](icontextnode-getstrokeids.md)
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

 




