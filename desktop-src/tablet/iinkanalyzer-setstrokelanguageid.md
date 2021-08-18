---
description: Ändert den Gebietsschemabezeichner für den angegebenen Strich.
ms.assetid: 3714462d-0391-481f-968a-3c121b7dd538
title: IInkAnalyzer::SetStrokeLanguageId-Methode (IACom.h)
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
ms.openlocfilehash: fc91d7d8a710d2640c31e639146bd6a2fd1deac854420d7ceac1bbfdd778022c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119091480"
---
# <a name="iinkanalyzersetstrokelanguageid-method"></a>IInkAnalyzer::SetStrokeLanguageId-Methode

Ändert den Gebietsschemabezeichner für den angegebenen Strich.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetStrokeLanguageId(
  [in] LONG lStrokeId,
  [in] LONG lStrokeLCID
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lStrokeId* \[ In\]
</dt> <dd>

Der Bezeichner des Strichs, dem der Gebietsschemabezeichner zugewiesen werden soll.

</dd> <dt>

*lStrokeLCID* \[ In\]
</dt> <dd>

Der Gebietsschemabezeichner, der dem Strich zugewiesen werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter Klassen und Schnittstellen – [Ink-Analyse.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Hinweise

Das Gebietsschema eines Strichs wird festgelegt, wenn Sie den Strich hinzufügen, indem Sie [**die IInkAnalyzer::AddStroke-Methode,**](iinkanalyzer-addstroke.md) [**die IInkAnalyzer::AddStrokeForLanguage-Methode,**](iinkanalyzer-addstrokeforlanguage.md)die [**IInkAnalyzer::AddStrokes-Methode**](iinkanalyzer-addstrokes.md)oder die [**IInkAnalyzer::AddStrokesForLanguage-Methode**](iinkanalyzer-addstrokesforlanguage.md)aufrufen. Rufen Sie die [**IInkAnalyzer::GetStrokeLanguageId-Methode**](iinkanalyzer-getstrokelanguageid.md)auf, um das gebietsschema abzurufen, das derzeit einem Strich zugewiesen ist.

Der angegebene Strich wird in einen nicht klassifizierten Freihandknoten verschoben (siehe [**IContextNode::GetType),**](icontextnode-gettype.md)der Striche derselben Sprache enthält. Wenn kein solcher [**IContextNode**](icontextnode.md) vorhanden ist, erstellt diese Methode einen neuen nicht klassifizierten Ink-Knoten und verschiebt den Strich darauf. Ein nicht klassifizierter Freihandknoten ist ein **IContextNode** mit dem Typ UnclassifiedInk.

Wenn diese Methode einen Strich aus einem [**IContextNode**](icontextnode.md) verschiebt, der kein nicht klassifizierter Freihandknoten ist, fügt diese Methode auch das umgebende Feld des Strichs dem geänderten Bereich des Freihandanalysetools hinzu (siehe [**IInkAnalyzer::GetDirtyRegion-Methode).**](iinkanalyzer-getdirtyregion.md)

Diese Methode bewegt keinen Strich, wenn der *lStrokeLCID-Parameter* mit dem aktuellen Sprachbezeichner des Strichs übereinstimmt.

Wenn der angegebene Strich nicht dem [**IInkAnalyzer**](iinkanalyzer.md)zugeordnet ist, gibt diese Methode zurück, ohne den **IInkAnalyzer** zu aktualisieren.

Weitere Informationen zu Sprachbezeichnern finden Sie unter [Sprachbezeichnerkonstanten und Zeichenfolgen.](/windows/desktop/Intl/language-identifier-constants-and-strings)

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

[**IInkAnalyzer::GetStrokeLanguageId-Methode**](iinkanalyzer-getstrokelanguageid.md)
</dt> <dt>

[**IInkAnalyzer::SetStrokesLanguageId-Methode**](iinkanalyzer-setstrokeslanguageid.md)
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

