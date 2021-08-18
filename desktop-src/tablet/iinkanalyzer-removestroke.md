---
description: Entfernt den angegebenen Strich aus dem IInkAnalyzer.
ms.assetid: e182ae35-854e-401d-8e26-aee645c05430
title: IInkAnalyzer::RemoveStroke-Methode (IACom.h)
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
ms.openlocfilehash: dd0a972ed776c40fc42d695df2058c62f9af84f8fc09155758d197772e9abfc7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092010"
---
# <a name="iinkanalyzerremovestroke-method"></a>IInkAnalyzer::RemoveStroke-Methode

Entfernt den angegebenen Strich aus dem [**IInkAnalyzer**](iinkanalyzer.md).

## <a name="syntax"></a>Syntax


```C++
HRESULT RemoveStroke(
  [in] LONG *plStrokeId
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*plStrokeId* \[ In\]
</dt> <dd>

Der Strichbezeichner.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter Klassen und Schnittstellen – [Ink-Analyse.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Hinweise

Diese Methode entfernt die Paketdaten für und verweist auf den angegebenen Strich aus dem [**IInkAnalyzer**](iinkanalyzer.md).

Diese Methode entfernt den Strich aus dem Blattkontextknoten, der auf den Strich verweist. Wenn [**der IContextNode**](icontextnode.md) nicht mehr auf Striche verweist, löscht diese Methode die **IContextNode-Objekte** und alle übergeordneten **IContextNode-Objekte,** die keine untergeordneten Knoten mehr haben.

Nachdem diese Methode den Strich aus dem [**IContextNode**](icontextnode.md)entfernt hat, aktualisiert sie den geänderten Bereich des [**IInkAnalyzer-Objekts**](iinkanalyzer.md) (siehe [**IInkAnalyzer::GetDirtyRegion-Methode),**](iinkanalyzer-getdirtyregion.md)um den Begrenzungsfeld des entfernten Strichs einzuschließen.

Wenn *plStrokeId* keinen Strich identifiziert, der [**IInkAnalyzer**](iinkanalyzer.md)zugeordnet ist, gibt diese Methode zurück, ohne die Freihandanalyse zu aktualisieren.

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

[**IInkAnalyzer::RemoveStrokes-Methode**](iinkanalyzer-removestrokes.md)
</dt> <dt>

[**IInkAnalyzer::GetDirtyRegion-Methode**](iinkanalyzer-getdirtyregion.md)
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

 




