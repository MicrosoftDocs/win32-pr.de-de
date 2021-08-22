---
description: Ändert den Locale Identifier für die angegebenen Striche.
ms.assetid: 39dd24d5-4381-4b51-8d95-7d936fd69d47
title: IInkAnalyzer::SetStrokesLanguageId-Methode (IACom.h)
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
ms.openlocfilehash: 2a063180d89fd9f29ebcacd5b9cbd9e98e4299d82aac2328b08624e3c1557249
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119590340"
---
# <a name="iinkanalyzersetstrokeslanguageid-method"></a>IInkAnalyzer::SetStrokesLanguageId-Methode

Ändert den Locale Identifier für die angegebenen Striche.

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

*ulStrokeIdCount* \[ In\]
</dt> <dd>

Die Anzahl der Strichbezeichner in *plStrokes*.

</dd> <dt>

*plStrokes* \[ In\]
</dt> <dd>

Das Array von Bezeichnern für die Striche, denen der Locale Identifier zugewiesen werden soll.

</dd> <dt>

*lStrokesLCID* \[ In\]
</dt> <dd>

Der Den Strichen zu zuweisende Lokalbezeichner.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen – Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Hinweise

Das Locale eines Strichs wird festgelegt, wenn Sie den Strich durch Aufrufen der [**IInkAnalyzer::AddStroke-Methode,**](iinkanalyzer-addstroke.md) [**der IInkAnalyzer::AddStrokeForLanguage-Methode,**](iinkanalyzer-addstrokeforlanguage.md) [**der IInkAnalyzer::AddStrokes-Methode**](iinkanalyzer-addstrokes.md)oder der [**IInkAnalyzer::AddStrokesForLanguage-Methode hinzufügen.**](iinkanalyzer-addstrokesforlanguage.md) Rufen Sie die [**IInkAnalyzer::GetStrokeLanguageId-Methode**](iinkanalyzer-getstrokelanguageid.md)auf, um das derzeit einem Strich zugewiesene Locale zu erhalten.

Die angegebenen Striche werden in einen nicht klassifizierten Ink-Knoten verschoben (siehe [**IContextNode::GetType),**](icontextnode-gettype.md)der Striche derselben Sprache enthält. Wenn kein solcher [**IContextNode vorhanden**](icontextnode.md) ist, erstellt diese Methode einen neuen nicht klassifizierten Ink-Knoten und verschiebt die Striche darauf. Ein nicht klassifizierter Ink-Knoten ist ein **IContextNode mit** dem Typ UnclassifiedInk.

Wenn diese Methode Striche von einem [**IContextNode**](icontextnode.md) verschiebt, der kein nicht klassifizierter Ink-Knoten ist, fügt diese Methode auch die Begrenzungsfelder der Striche zum verfälschten Bereich des Ink Analyzers hinzu (siehe [**IInkAnalyzer::GetDirtyRegion-Methode**](iinkanalyzer-getdirtyregion.md)).

Diese Methode bewegt keinen Strich, wenn der *lStrokeLCID-Parameter* dem aktuellen Sprachbezeichner des Strichs entspricht.

Wenn ein angegebener Strich nicht dem [**IInkAnalyzer**](iinkanalyzer.md)zugeordnet ist, ignoriert diese Methode den Bezeichner.

Wenn keiner der angegebenen Striche einen Strich identifiziert, der [**dem IInkAnalyzer**](iinkanalyzer.md)zugeordnet ist, gibt diese Methode zurück, ohne **IInkAnalyzer zu aktualisieren.**

Diese Methode gibt einen Fehlercode zurück, wenn strokeIds NULL **ist.**

Weitere Informationen zu Sprachbezeichnern finden Sie unter [Sprachbezeichnerkonst konstanten und Zeichenfolgen](/windows/desktop/Intl/language-identifier-constants-and-strings).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (erfordert auch IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Siehe auch

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

[**IInkAnalyzer::SetStrokeLanguageId-Methode**](iinkanalyzer-setstrokelanguageid.md)
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

