---
description: Ändert den Typ des angegebenen Strichs.
ms.assetid: 1608fed1-cd6c-46c3-a35f-3d262279ec2e
title: 'Iinkanalyzer:: SetStrokeType-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SetStrokeType
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 8a5f77cbefb200bad973c0f2cf28fea5d3efe1da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129436"
---
# <a name="iinkanalyzersetstroketype-method"></a>Iinkanalyzer:: SetStrokeType-Methode

Ändert den Typ des angegebenen Strichs.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetStrokeType(
  [in] LONG       lStrokeId,
  [in] StrokeType StrokeType
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lstrokeid* \[ in\]
</dt> <dd>

Der Strich Bezeichner des Strichs, dem *StrokeType* zugewiesen werden soll.

</dd> <dt>

*StrokeType* \[ in\]
</dt> <dd>

Der [**StrokeType**](stroketype.md) -Wert, der dem Strich zugewiesen werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

Wenn der Typ des Strichs der [**StrokeType**](stroketype.md) -Wert **\_ nicht klassifiziert** ist, klassifiziert [**iinkanalyzer**](iinkanalyzer.md) den Strich während der frei Hand Analyse. Andernfalls verwendet **iinkanalyzer** den Typ, der auf dem Strich festgelegt ist.

Der Wert von "Stroke Type" wird von [**iinkanalyzer**](iinkanalyzer.md) nicht als Teil der Ink-Analyse festgelegt. Verwenden Sie die **iinkanalyzer:: SetStrokeType-Methode** oder die [**iinkanalyzer:: SetStrokesType-Methode**](iinkanalyzer-setstrokestype.md), um den strichentyp anzugeben oder zu ändern.

Wenn ein Strich einem [**icontextnode**](icontextnode.md) zugeordnet ist, bei dem es sich nicht um einen nicht klassifizierten frei Hand Knoten handelt (siehe [**icontextnode:: GetType**](icontextnode-gettype.md)), verschiebt diese Methode den Strich auf einen nicht klassifizierten Ink-Knoten, der Striche derselben Sprache enthält. Wenn kein solcher Kontext Knoten vorhanden ist, erstellt diese Methode einen neuen nicht klassifizierten frei Hand Knoten und fügt diesen dem Strich hinzu. Bei einem nicht klassifizierten Ink-Knoten handelt es sich um einen **icontextnode** , der vom Typ unclassimeedink ist.

Wenn diese Methode einen Strich von einem [**icontextnode**](icontextnode.md) verschiebt, bei dem es sich nicht um einen nicht klassifizierten frei Hand Knoten handelt, fügt diese Methode auch das umgebende Feld des Strichs zum geänderten Bereich der Ink Analyzer hinzu (siehe [**iinkanalyzer:: getdirtyregion-Methode**](iinkanalyzer-getdirtyregion.md)).

Diese Methode verschiebt keinen Strich, wenn der *StrokeType* -Parameter mit dem aktuellen Typ des Strichs übereinstimmt.

Beim Festlegen des Strich Typs für Striche, die einem ContextNode zugeordnet sind, für das NodeTypeAndProperties bestätigt ist, wird eine InvalidOperationException ausgelöst.

Wenn der angegebene Strich nicht mit [**iinkanalyzer**](iinkanalyzer.md)verknüpft ist, gibt diese Methode zurück, ohne **iinkanalyzer** zu aktualisieren.

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

[**Iinkanalyzer:: SetStrokesType-Methode**](iinkanalyzer-setstrokestype.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

 




