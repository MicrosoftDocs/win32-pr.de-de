---
description: Ordnet diesem icontextnode die angegebenen Striche zu.
ms.assetid: 5ce8893a-da59-4cec-a349-d5ffc4f43905
title: 'Icontextnode:: setstrokes-Methode (iacom. h)'
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
ms.openlocfilehash: be7fd1645af70e34c747894bc8ab4317b08e2d70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347197"
---
# <a name="icontextnodesetstrokes-method"></a>Icontextnode:: setstrokes-Methode

Ordnet diesem [**icontextnode**](icontextnode.md)die angegebenen Striche zu.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetStrokes(
  [in] ULONG ulStrokeIdsCount,
  [in] LONG  *plStrokeIds
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ulstrokeidscount* \[ in\]
</dt> <dd>

Die Anzahl der Stroke-IDs in *plstrokeids*.

</dd> <dt>

*plstrokeids* \[ in\]
</dt> <dd>

Die Bezeichner der Striche, die diesem [**icontextnode**](icontextnode.md)zugeordnet werden sollen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

Mit dieser Methode wird der geänderte Bereich der Ink Analyzer nicht aktualisiert (Weitere Informationen finden Sie unter [**iinkanalyzer:: getdirtyregion-Methode**](iinkanalyzer-getdirtyregion.md)).

Verwenden Sie diese Methode, wenn Ihre Anwendung ihre eigene Datenstruktur verwaltet, die mit der von [**iinkanalyzer**](iinkanalyzer.md)synchronisiert wird. Verwenden Sie diese Methode, um einem bestimmten Kontext Knoten hubdaten zuzuweisen. Weitere Informationen zum Synchronisieren von Anwendungsdaten mit **iinkanalyzer** finden Sie unter [Daten Proxy mit Ink-Analyse](data-proxy-with-ink-analysis.md).

Wenn einer der angegebenen Striche bereits mit [**iinkanalyzer**](iinkanalyzer.md)verknüpft ist, gibt diese Methode **E \_ invalidArg** zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Iacom. h (erfordert auch iacom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Icontextnode**](icontextnode.md)
</dt> <dt>

[**Iinkanalyzer:: AddStroke-Methode**](iinkanalyzer-addstroke.md)
</dt> <dt>

[**Iinkanalyzer:: addstrokeforlanguage-Methode**](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[**Iinkanalyzer:: AddStrokes-Methode**](iinkanalyzer-addstrokes.md)
</dt> <dt>

[**Iinkanalyzer:: addstrokesforlanguage-Methode**](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[**Iinkanalyzer:: addstrokestocustomerkenzer-Methode**](iinkanalyzer-addstrokestocustomrecognizer.md)
</dt> <dt>

[**Iinkanalyzer:: addstrokedecustomerkenzer-Methode**](iinkanalyzer-addstroketocustomrecognizer.md)
</dt> <dt>

[**Iinkanalyzer:: RemoveStroke-Methode**](iinkanalyzer-removestroke.md)
</dt> <dt>

[**Iinkanalyzer:: RemoveStrokes-Methode**](iinkanalyzer-removestrokes.md)
</dt> <dt>

[**Icontextnode:: getstrokeid**](icontextnode-getstrokeid.md)
</dt> <dt>

[**Icontextnode:: GetStrokeIds**](icontextnode-getstrokeids.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

 




