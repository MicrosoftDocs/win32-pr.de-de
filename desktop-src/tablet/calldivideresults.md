---
description: Ruft Analyseergebnisse aus dem InkDivider-Objekt ab.
ms.assetid: 7fc2bb5a-172f-4f4e-84dd-e31925f86982
title: CallDivideResults-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CallDivideResults
api_type:
- LibDef
api_location:
- InkDiv.dll
- InkDiv.dll.dll
ms.openlocfilehash: 2e5f3060f261ba84b70272ed358a7c544f2b0e1582de310ed759b4ea40714359
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967759"
---
# <a name="calldivideresults-function"></a>CallDivideResults-Funktion

Ruft Analyseergebnisse aus dem [**InkDivider-Objekt**](inkdivider-class.md) ab.

Diese Funktion ist nicht für die Verwendung durch Anwendungscode vorgesehen.

## <a name="syntax"></a>Syntax


```C++
HRESULT WINAPI CallDivideResults(
  _In_  INT_PTR   hDivider,
  _Out_ int       aWordStrokeIds[],
  _Out_ int       aLineStrokeIds[],
  _Out_ int       aParagraphStrokeIds[],
  _Out_ int       aDrawingStrokeIds[],
  _Out_ SAFEARRAY **pastrWords,
  _Out_ SAFEARRAY **pastrLines,
  _Out_ SAFEARRAY **pastrParagraphs,
  _Out_ int       *aWordRotationCenterX,
  _Out_ int       *aWordRotationCenterY,
  _Out_ float     *aWordAngle,
  _Out_ int       *aLineRotationCenterX,
  _Out_ int       *aLineRotationCenterY,
  _Out_ float     *aLineAngle
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hDivider* \[ In\]
</dt> <dd>

Ein Handle für das [**InkDivider-Objekt.**](inkdivider-class.md)

</dd> <dt>

*aWordStrokeIds* \[ out\]
</dt> <dd>

Ein Array von Bezeichnern, die dem Wort zugeordnet sind, das an die [**InkDivider-Klasse**](inkdivider-class.md) übergeben wird.

</dd> <dt>

*aLineStrokeIds* \[ out\]
</dt> <dd>

Ein Array von [**ID-Eigenschaften**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) für die [**IInkStrokeDisp-Objekte,**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) die der Zeile zugeordnet sind, die an die [**InkDivider-Klasse**](inkdivider-class.md) übergeben wird.

</dd> <dt>

*aParagraphStrokeIds* \[ out\]
</dt> <dd>

Ein Array der [**ID-Eigenschaften**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) für die [**IInkStrokeDisp-Objekte,**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) die dem Absatz aus der [**InkDivider-Klasse**](inkdivider-class.md) zugeordnet sind.

</dd> <dt>

*aDrawingStrokeIds* \[ out\]
</dt> <dd>

Ein Array von [**ID-Eigenschaften**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) für die [**IInkStrokeDisp-Objekte,**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) die der Zeichnung aus der [**InkDivider-Klasse**](inkdivider-class.md) zugeordnet sind.

</dd> <dt>

*pastrWords* \[ out\]
</dt> <dd>

Ein Array von Wörtern, die von der Ink-Analyse zurückgegeben werden.

</dd> <dt>

*pastrLines* \[ out\]
</dt> <dd>

Ein Array von Zeilen, die von der Ink-Analyse zurückgegeben werden.

</dd> <dt>

*pastrParagraphs* \[ out\]
</dt> <dd>

Ein Array von Absätzen, die von der Ink-Analyse zurückgegeben werden.

</dd> <dt>

*aWordRotationCenterX* \[ out\]
</dt> <dd>

Ein Array der Mittelpunkte der Wörter entlang der X-Achse aus der Ink-Analyse.

</dd> <dt>

*aWordRotationCenterY* \[ out\]
</dt> <dd>

Ein Array der Mittelpunkte der Wörter entlang der y-Achse aus der Ink-Analyse.

</dd> <dt>

*aWordAngle* \[ out\]
</dt> <dd>

Ein Array mit den Winkeln, um die die Wörter gedreht werden sollen, um optimale Analyseergebnisse zu erzielen.

</dd> <dt>

*aLineRotationCenterX* \[ out\]
</dt> <dd>

Ein Array, das die Mittelpunkte der Linien entlang der x-Achse enthält.

</dd> <dt>

*aLineRotationCenterY* \[ out\]
</dt> <dd>

Ein Array, das die Mittelpunkte der Linien entlang der y-Achse enthält.

</dd> <dt>

*aLineAngle* \[ out\]
</dt> <dd>

Ein Array mit den Winkeln, um die die Linien gedreht werden sollen, um optimale Analyseergebnisse zu erzielen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                   | Beschreibung                                                       |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Die Funktion wurde erfolgreich ausgeführt.<br/>                                |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Der *hDivider-Parameter* ist ungültig.<br/>                   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Es konnte nicht genügend Arbeitsspeicher zum Speichern der Ergebnisse belegt werden.<br/> |



 

## <a name="remarks"></a>Hinweise

Um Speicherverluste zu vermeiden, müssen Sie die Ressourcen für *pastrWords,* *pastrLines* und *pastrParagraphs* freigeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                         |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                             |
| Bibliothek<br/>                  | <dl> <dt>InkDiv.dll</dt> </dl> |



 

 




