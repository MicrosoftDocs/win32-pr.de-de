---
description: Entfernt die angegebenen Striche aus iinkanalyzer.
ms.assetid: ea7c8a9f-a427-4781-b5ba-97ffd983dbe5
title: 'Iinkanalyzer:: RemoveStrokes-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.RemoveStrokes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 00f065e01f9a4ff1459988d76fc9393ba24aa894
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129449"
---
# <a name="iinkanalyzerremovestrokes-method"></a>Iinkanalyzer:: RemoveStrokes-Methode

Entfernt die angegebenen Striche aus [**iinkanalyzer**](iinkanalyzer.md).

## <a name="syntax"></a>Syntax


```C++
HRESULT RemoveStrokes(
  [in] ULONG ulStrokeIdCount,
  [in] LONG  *plStrokes
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

Die Bezeichner für die Striche, die entfernt werden sollen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

Diese Methode entfernt die Paketdaten für-und-Verweise auf die angegebenen Striche aus [**iinkanalyzer**](iinkanalyzer.md).

Diese Methode entfernt die Striche aus dem Blatt Kontext Knoten, der auf die Striche verweist. Wenn ein [**icontextnode**](icontextnode.md) nicht mehr auf Striche verweist, löscht diese Methode den **icontextnode** -und alle Vorgänger- **icontextnode** -Objekte, die keine untergeordneten Knoten mehr aufweisen.

Nachdem diese Methode die Striche aus dem [**icontextnode**](icontextnode.md)entfernt hat, aktualisiert Sie den geänderten Bereich des [**iinkanalyzer**](iinkanalyzer.md) -Objekts (siehe [**iinkanalyzer:: getdirtyregion-Methode**](iinkanalyzer-getdirtyregion.md)), um das umgebende Feld der entfernten Striche einzubeziehen.

Wenn ein in *plstrokes* identifizierter Strich nicht mit [**iinkanalyzer**](iinkanalyzer.md)verknüpft ist, ignoriert diese Methode den Bezeichner.

Wenn keiner der in *plstrokes* identifizierten Striche mit der Ink Analyzer verknüpft ist, gibt diese Methode zurück, ohne [**iinkanalyzer**](iinkanalyzer.md)zu aktualisieren.

Diese Methode gibt den Fehlercode zurück, wenn *plstrokes* NULL ist.

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

[**Iinkanalyzer:: RemoveStroke-Methode**](iinkanalyzer-removestroke.md)
</dt> <dt>

[**Iinkanalyzer:: getdirtyregion-Methode**](iinkanalyzer-getdirtyregion.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

 




