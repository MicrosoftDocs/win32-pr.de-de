---
description: Ändert den Gebiets Schema Bezeichner für die angegebenen Striche.
ms.assetid: 39dd24d5-4381-4b51-8d95-7d936fd69d47
title: 'Iinkanalyzer:: SetStrokesLanguageId-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SetStrokesLanguageId
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 84d2e4b9e3ac24fc73eddc4f84bcc9337cb4c372
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345121"
---
# <a name="iinkanalyzersetstrokeslanguageid-method"></a>Iinkanalyzer:: SetStrokesLanguageId-Methode

Ändert den Gebiets Schema Bezeichner für die angegebenen Striche.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetStrokesLanguageId(
  [in] ULONG ulStrokeIdCount,
  [in] LONG  *plStrokes,
  [in] LONG  lStrokesLCID
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ulstrokeidcount* \[ in\]
</dt> <dd>

Die Anzahl der Stroke-IDs in *plstrokes*.

</dd> <dt>

*pltakte* \[ in\]
</dt> <dd>

Das Array von Bezeichnern für die Striche, denen der Gebiets Schema Bezeichner zugewiesen werden soll.

</dd> <dt>

*lstrokeslcid* \[ in\]
</dt> <dd>

Der Gebiets Schema Bezeichner, der den Strichen zugewiesen werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

Das Gebiets Schema eines Strichs wird festgelegt, wenn Sie den Strich durch Aufrufen von [**iinkanalyzer:: AddStroke Method**](iinkanalyzer-addstroke.md), [**iinkanalyzer:: addstrokeforlanguage-Methode**](iinkanalyzer-addstrokeforlanguage.md), [**iinkanalyzer:: addstriche**](iinkanalyzer-addstrokes.md)-Methode oder [**iinkanalyzer:: addstrokesforlanguage**](iinkanalyzer-addstrokesforlanguage.md)-Methode hinzufügen. Um das Gebiets Schema abzurufen, das momentan einem Strich zugewiesen ist, müssen Sie die [**iinkanalyzer:: GetStrokeLanguageId-Methode**](iinkanalyzer-getstrokelanguageid.md)aufrufen.

Die angegebenen Striche werden auf einen nicht klassifizierten frei Hand Knoten verschoben (siehe [**icontextnode:: GetType**](icontextnode-gettype.md)), der Striche derselben Sprache enthält. Wenn kein solcher [**icontextnode**](icontextnode.md) vorhanden ist, erstellt diese Methode einen neuen nicht klassifizierten frei Hand Knoten und verschiebt die Striche darauf. Bei einem nicht klassifizierten Ink-Knoten handelt es sich um einen **icontextnode** mit dem Typ unclassimeedink.

Wenn diese Methode Striche von einem [**icontextnode**](icontextnode.md) verschiebt, bei dem es sich nicht um einen nicht klassifizierten frei Hand Knoten handelt, fügt diese Methode auch die Begrenzungs Felder der Striche in den geänderten Bereich der Ink Analyzer ein (siehe [**iinkanalyzer:: getdirtyregion-Methode**](iinkanalyzer-getdirtyregion.md)).

Diese Methode verschiebt keinen Strich, wenn der *lstrokelcid* -Parameter mit dem aktuellen sprach Bezeichner des Strichs übereinstimmt.

Wenn ein angegebener Strich nicht mit [**iinkanalyzer**](iinkanalyzer.md)verknüpft ist, ignoriert diese Methode den Bezeichner.

Wenn keiner der angegebenen Striche einen Strich identifiziert, der dem [**iinkanalyzer**](iinkanalyzer.md)zugeordnet ist, gibt diese Methode zurück, ohne **iinkanalyzer** zu aktualisieren.

Diese Methode gibt einen Fehlercode zurück, wenn strokeIds **null** ist.

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

[**Iinkanalyzer:: SetStrokeLanguageId-Methode**](iinkanalyzer-setstrokelanguageid.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

