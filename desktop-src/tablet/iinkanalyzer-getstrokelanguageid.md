---
description: Gibt den Gebietsschemabezeichner des angegebenen Strichs zurück.
ms.assetid: a5fb9b7a-ed3e-4552-9412-39529203bd81
title: IInkAnalyzer::GetStrokeLanguageId-Methode (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetStrokeLanguageId
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 8b61bfa61b4e4aa2c8415c9596cb97a3b0c1313cf3a080d065a7c82e4d69b84d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119713390"
---
# <a name="iinkanalyzergetstrokelanguageid-method"></a>IInkAnalyzer::GetStrokeLanguageId-Methode

Gibt den Gebietsschemabezeichner des angegebenen Strichs zurück.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetStrokeLanguageId(
  [in]  LONG lStrokeId,
  [out] LONG *lStrokeLCID
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lStrokeId* \[ In\]
</dt> <dd>

Der Strichbezeichner.

</dd> <dt>

*lStrokeLCID* \[ out\]
</dt> <dd>

Der Gebietsschemabezeichner für den angegebenen Strich.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter Klassen und Schnittstellen – [Ink-Analyse.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Hinweise

Das Gebietsschema des Strichs wird festgelegt, wenn Sie den Strich hinzufügen, indem Sie [**die IInkAnalyzer::AddStroke-Methode,**](iinkanalyzer-addstroke.md) [**die IInkAnalyzer::AddStrokeForLanguage-Methode,**](iinkanalyzer-addstrokeforlanguage.md)die [**IInkAnalyzer::AddStrokes-Methode**](iinkanalyzer-addstrokes.md)oder [**die IInkAnalyzer::AddStrokesForLanguage-Methode**](iinkanalyzer-addstrokesforlanguage.md)aufrufen. Verwenden Sie zum Ändern des Gebietsschemas des Strichs die [**IInkAnalyzer::SetStrokeLanguageId-Methode**](iinkanalyzer-setstrokelanguageid.md) oder [**die IInkAnalyzer::SetStrokesLanguageId-Methode.**](iinkanalyzer-setstrokeslanguageid.md)

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

[**IInkAnalyzer::SetStrokeLanguageId-Methode**](iinkanalyzer-setstrokelanguageid.md)
</dt> <dt>

[**IInkAnalyzer::SetStrokesLanguageId-Methode**](iinkanalyzer-setstrokeslanguageid.md)
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

 




