---
description: Ändert den Gebiets Schema Bezeichner für den angegebenen Strich.
ms.assetid: 3714462d-0391-481f-968a-3c121b7dd538
title: 'Iinkanalyzer:: SetStrokeLanguageId-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SetStrokeLanguageId
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: e103683d85ff971a8f0daff2574e97672dd5a84b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526474"
---
# <a name="iinkanalyzersetstrokelanguageid-method"></a>Iinkanalyzer:: SetStrokeLanguageId-Methode

Ändert den Gebiets Schema Bezeichner für den angegebenen Strich.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetStrokeLanguageId(
  [in] LONG lStrokeId,
  [in] LONG lStrokeLCID
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lstrokeid* \[ in\]
</dt> <dd>

Der Bezeichner des Strichs, dem der Gebiets Schema Bezeichner zugewiesen werden soll.

</dd> <dt>

*lstrokelcid* \[ in\]
</dt> <dd>

Der Gebiets Schema Bezeichner, der dem Strich zugewiesen werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

Das Gebiets Schema eines Strichs wird festgelegt, wenn Sie den Strich durch Aufrufen von [**iinkanalyzer:: AddStroke Method**](iinkanalyzer-addstroke.md), [**iinkanalyzer:: addstrokeforlanguage-Methode**](iinkanalyzer-addstrokeforlanguage.md), [**iinkanalyzer:: addstriche**](iinkanalyzer-addstrokes.md)-Methode oder [**iinkanalyzer:: addstrokesforlanguage**](iinkanalyzer-addstrokesforlanguage.md)-Methode hinzufügen. Um das Gebiets Schema abzurufen, das momentan einem Strich zugewiesen ist, müssen Sie die [**iinkanalyzer:: GetStrokeLanguageId-Methode**](iinkanalyzer-getstrokelanguageid.md)aufrufen.

Der angegebene Strich wird in einen nicht klassifizierten frei Hand Knoten verschoben (siehe [**icontextnode:: GetType**](icontextnode-gettype.md)), der Striche derselben Sprache enthält. Wenn kein solcher [**icontextnode**](icontextnode.md) vorhanden ist, erstellt diese Methode einen neuen nicht klassifizierten frei Hand Knoten und verschiebt den Strich darauf. Bei einem nicht klassifizierten Ink-Knoten handelt es sich um einen **icontextnode** mit dem Typ unclassimeedink.

Wenn diese Methode einen Strich von einem [**icontextnode**](icontextnode.md) verschiebt, bei dem es sich nicht um einen nicht klassifizierten frei Hand Knoten handelt, fügt diese Methode auch das umgebende Feld des Strichs zum geänderten Bereich der Ink Analyzer hinzu (siehe [**iinkanalyzer:: getdirtyregion-Methode**](iinkanalyzer-getdirtyregion.md)).

Diese Methode verschiebt keinen Strich, wenn der *lstrokelcid* -Parameter mit dem aktuellen sprach Bezeichner des Strichs übereinstimmt.

Wenn der angegebene Strich nicht mit [**iinkanalyzer**](iinkanalyzer.md)verknüpft ist, gibt diese Methode zurück, ohne **iinkanalyzer** zu aktualisieren.

Weitere Informationen zu sprach Bezeichnern finden Sie unter [sprach Bezeichner-Konstanten und-](/windows/desktop/Intl/language-identifier-constants-and-strings)Zeichen folgen.

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

[**Iinkanalyzer:: AddStroke-Methode**](iinkanalyzer-addstroke.md)
</dt> <dt>

[**Iinkanalyzer:: addstrokeforlanguage-Methode**](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[**Iinkanalyzer:: AddStrokes-Methode**](iinkanalyzer-addstrokes.md)
</dt> <dt>

[**Iinkanalyzer:: addstrokesforlanguage-Methode**](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[**Iinkanalyzer:: GetStrokeLanguageId-Methode**](iinkanalyzer-getstrokelanguageid.md)
</dt> <dt>

[**Iinkanalyzer:: SetStrokesLanguageId-Methode**](iinkanalyzer-setstrokeslanguageid.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

