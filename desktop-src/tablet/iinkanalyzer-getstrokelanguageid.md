---
description: Gibt den Gebiets Schema Bezeichner des angegebenen Strichs zurück.
ms.assetid: a5fb9b7a-ed3e-4552-9412-39529203bd81
title: 'Iinkanalyzer:: GetStrokeLanguageId-Methode (iacom. h)'
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
ms.openlocfilehash: a231dde453467ad2973d729fa068cedcc35151c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751801"
---
# <a name="iinkanalyzergetstrokelanguageid-method"></a>Iinkanalyzer:: GetStrokeLanguageId-Methode

Gibt den Gebiets Schema Bezeichner des angegebenen Strichs zurück.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetStrokeLanguageId(
  [in]  LONG lStrokeId,
  [out] LONG *lStrokeLCID
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lstrokeid* \[ in\]
</dt> <dd>

Der Strich Bezeichner.

</dd> <dt>

*lstrokelcid* \[ vorgenommen\]
</dt> <dd>

Der Gebiets Schema Bezeichner für den angegebenen Strich.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

Das Gebiets Schema des Strichs wird festgelegt, wenn Sie den Strich durch Aufrufen von [**iinkanalyzer:: AddStroke Method**](iinkanalyzer-addstroke.md), [**iinkanalyzer:: addstrokeforlanguage-Methode**](iinkanalyzer-addstrokeforlanguage.md), [**iinkanalyzer:: addstriche**](iinkanalyzer-addstrokes.md)-Methode oder [**iinkanalyzer:: addstrokesforlanguage**](iinkanalyzer-addstrokesforlanguage.md)-Methode hinzufügen. Um das Gebiets Schema des Strichs zu ändern, verwenden Sie die [**iinkanalyzer:: SetStrokeLanguageId-Methode**](iinkanalyzer-setstrokelanguageid.md) oder die [**iinkanalyzer:: SetStrokesLanguageId-Methode**](iinkanalyzer-setstrokeslanguageid.md).

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

[**Iinkanalyzer:: SetStrokeLanguageId-Methode**](iinkanalyzer-setstrokelanguageid.md)
</dt> <dt>

[**Iinkanalyzer:: SetStrokesLanguageId-Methode**](iinkanalyzer-setstrokeslanguageid.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

 




