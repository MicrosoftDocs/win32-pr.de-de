---
description: Entfernt den angegebenen Strich aus iinkanalyzer.
ms.assetid: e182ae35-854e-401d-8e26-aee645c05430
title: 'Iinkanalyzer:: RemoveStroke-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.RemoveStroke
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 03952e6e14679c53f7b65f21463fc0457f302b8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526486"
---
# <a name="iinkanalyzerremovestroke-method"></a>Iinkanalyzer:: RemoveStroke-Methode

Entfernt den angegebenen Strich aus [**iinkanalyzer**](iinkanalyzer.md).

## <a name="syntax"></a>Syntax


```C++
HRESULT RemoveStroke(
  [in] LONG *plStrokeId
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*plstrokeid* \[ in\]
</dt> <dd>

Der Strich Bezeichner.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

Diese Methode entfernt die Paketdaten für den angegebenen Strich und verweist auf den angegebenen Strich aus dem [**iinkanalyzer**](iinkanalyzer.md).

Mit dieser Methode wird der Strich aus dem Blatt Kontext Knoten entfernt, der auf den Strich verweist. Wenn der [**icontextnode**](icontextnode.md) nicht mehr auf Striche verweist, löscht diese Methode den **icontextnode** -und alle Vorgänger- **icontextnode** -Objekte, die keine untergeordneten Knoten mehr aufweisen.

Nachdem diese Methode den Strich aus dem [**icontextnode**](icontextnode.md)entfernt hat, aktualisiert Sie den geänderten Bereich des [**iinkanalyzer**](iinkanalyzer.md) -Objekts (siehe [**iinkanalyzer:: getdirtyregion-Methode**](iinkanalyzer-getdirtyregion.md)), um das umgebende Feld des entfernten Strichs einzuschließen.

Wenn *plstrokeid* keinen dem [**iinkanalyzer**](iinkanalyzer.md)zugeordneten Strich identifiziert, gibt diese Methode zurück, ohne den Ink Analyzer zu aktualisieren.

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

[**Iinkanalyzer:: RemoveStrokes-Methode**](iinkanalyzer-removestrokes.md)
</dt> <dt>

[**Iinkanalyzer:: getdirtyregion-Methode**](iinkanalyzer-getdirtyregion.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

 




