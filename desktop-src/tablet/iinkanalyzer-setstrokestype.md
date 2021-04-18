---
description: Ändert den Typ der angegebenen Striche.
ms.assetid: 8d954a7d-c987-41cf-9933-b2e6bacc9489
title: 'Iinkanalyzer:: SetStrokesType-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SetStrokesType
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: de3f4e56b24226c2f74c6572561082c1d00afc8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344457"
---
# <a name="iinkanalyzersetstrokestype-method"></a>Iinkanalyzer:: SetStrokesType-Methode

Ändert den Typ der angegebenen Striche.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetStrokesType(
  [in] ULONG      strokeIdCount,
  [in] LONG       *plStrokes,
  [in] StrokeType StrokeType
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*strokeidcount* \[ in\]
</dt> <dd>

Die Anzahl der Stroke-IDs in *plstrokes*.

</dd> <dt>

*pltakte* \[ in\]
</dt> <dd>

Ein Array, das die Strich Bezeichner der Striche enthält, denen *StrokeType* zugewiesen werden soll.

</dd> <dt>

*StrokeType* \[ in\]
</dt> <dd>

Der [**StrokeType**](stroketype.md) -Wert, der den Strichen zugewiesen werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

Wenn der Typ des Strichs der [**StrokeType**](stroketype.md) -Wert **\_ nicht klassifiziert** ist, klassifiziert [**iinkanalyzer**](iinkanalyzer.md) den Strich während der frei Hand Analyse. Andernfalls verwendet **iinkanalyzer** den Typ, der auf dem Strich festgelegt ist.

Der Wert von "Stroke Type" wird von [**iinkanalyzer**](iinkanalyzer.md) nicht als Teil der Ink-Analyse festgelegt. Verwenden Sie die [**iinkanalyzer:: SetStrokeType-Methode**](iinkanalyzer-setstroketype.md) oder die **iinkanalyzer:: SetStrokesType-Methode**, um den strichentyp anzugeben oder zu ändern.

Wenn ein Strich einem [**icontextnode**](icontextnode.md) zugeordnet ist, bei dem es sich nicht um einen nicht klassifizierten frei Hand Knoten handelt (siehe [**icontextnode:: GetType**](icontextnode-gettype.md)), verschiebt diese Methode den Strich auf einen nicht klassifizierten Ink-Knoten, der Striche derselben Sprache enthält. Wenn kein solcher Kontext Knoten vorhanden ist, erstellt diese Methode einen neuen nicht klassifizierten frei Hand Knoten und fügt diesen dem Strich hinzu. Bei einem nicht klassifizierten Ink-Knoten handelt es sich um einen **icontextnode** , der vom Typ unclassimeedink ist.

Wenn diese Methode einen Strich von einem [**icontextnode**](icontextnode.md) verschiebt, bei dem es sich nicht um einen nicht klassifizierten frei Hand Knoten handelt, fügt diese Methode auch das umgebende Feld des Strichs zum geänderten Bereich der Ink Analyzer hinzu (siehe [**iinkanalyzer:: getdirtyregion-Methode**](iinkanalyzer-getdirtyregion.md)).

Diese Methode verschiebt keinen Strich, wenn der *StrokeType* -Parameter mit dem aktuellen Typ des Strichs übereinstimmt.

Wenn ein in *strokeIds* identifizierter Strich nicht mit [**iinkanalyzer**](iinkanalyzer.md)verknüpft ist, ignoriert diese Methode den Bezeichner.

Wenn keiner der angegebenen Striche einen Strich identifiziert, der dem [**iinkanalyzer**](iinkanalyzer.md)zugeordnet ist, gibt diese Methode zurück, ohne **iinkanalyzer** zu aktualisieren.

Beim Festlegen des Strich Typs für Striche, die einem ContextNode zugeordnet sind, für das NodeTypeAndProperties bestätigt ist, wird eine InvalidOperationException ausgelöst.

Diese Methode gibt einen Fehlercode zurück, wenn *plstrokes* **null** ist.

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

[**Iinkanalyzer:: GetStrokeType-Methode**](iinkanalyzer-getstroketype.md)
</dt> <dt>

[**Iinkanalyzer:: SetStrokeType-Methode**](iinkanalyzer-setstroketype.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

 




