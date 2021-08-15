---
description: Entfernt die angegebenen Striche aus dem IInkAnalyzer.
ms.assetid: ea7c8a9f-a427-4781-b5ba-97ffd983dbe5
title: IInkAnalyzer::RemoveStrokes-Methode (IACom.h)
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
ms.openlocfilehash: e6d53d21df9734ee43cdda618c5221fd83300598d46b51bd366c50fedf5cec45
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092020"
---
# <a name="iinkanalyzerremovestrokes-method"></a>IInkAnalyzer::RemoveStrokes-Methode

Entfernt die angegebenen Striche aus dem [**IInkAnalyzer**](iinkanalyzer.md).

## <a name="syntax"></a>Syntax


```C++
HRESULT RemoveStrokes(
  [in] ULONG ulStrokeIdCount,
  [in] LONG  *plStrokes
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ulStrokeIdCount* \[ In\]
</dt> <dd>

Die Anzahl der Strichbezeichner in *plStrokes*.

</dd> <dt>

*plStrokes* \[ In\]
</dt> <dd>

Die Bezeichner für die zu entfernenden Striche.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter Klassen und Schnittstellen – [Ink-Analyse.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Hinweise

Diese Methode entfernt die Paketdaten für und Verweise auf die angegebenen Striche aus dem [**IInkAnalyzer**](iinkanalyzer.md).

Diese Methode entfernt die Striche aus dem Blattkontextknoten, der auf die Striche verweist. Wenn ein [**IContextNode**](icontextnode.md) nicht mehr auf Striche verweist, löscht diese Methode die **IContextNode-Objekte** und alle übergeordneten **IContextNode-Objekte,** die keine untergeordneten Knoten mehr haben.

Nachdem diese Methode die Striche aus dem [**IContextNode**](icontextnode.md)entfernt hat, aktualisiert sie den geänderten Bereich des [**IInkAnalyzer-Objekts**](iinkanalyzer.md) (siehe [**IInkAnalyzer::GetDirtyRegion-Methode),**](iinkanalyzer-getdirtyregion.md)um den Begrenzungsfeld der entfernten Striche einzuschließen.

Wenn ein in *plStrokes* identifizierter Strich nicht dem [**IInkAnalyzer**](iinkanalyzer.md)zugeordnet ist, ignoriert diese Methode den Bezeichner.

Wenn dem Freihandanalyseprogramm keiner der in *plStrokes identifizierten Striche* zugeordnet ist, gibt diese Methode zurück, ohne den [**IInkAnalyzer**](iinkanalyzer.md)zu aktualisieren.

Diese Methode gibt den Fehlercode und zurück, wenn *plStrokes* NULL ist.

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

[**IInkAnalyzer::AddStroke-Methode**](iinkanalyzer-addstroke.md)
</dt> <dt>

[**IInkAnalyzer::AddStrokeForLanguage-Methode**](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[**IInkAnalyzer::AddStrokes-Methode**](iinkanalyzer-addstrokes.md)
</dt> <dt>

[**IInkAnalyzer::AddStrokesForLanguage-Methode**](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[**IInkAnalyzer::RemoveStroke-Methode**](iinkanalyzer-removestroke.md)
</dt> <dt>

[**IInkAnalyzer::GetDirtyRegion-Methode**](iinkanalyzer-getdirtyregion.md)
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

 




