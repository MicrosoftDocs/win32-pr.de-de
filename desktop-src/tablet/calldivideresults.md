---
description: Ruft Analyseergebnisse aus dem InkDivider-Objekt ab.
ms.assetid: 7fc2bb5a-172f-4f4e-84dd-e31925f86982
title: Calldivideresults-Funktion
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
ms.openlocfilehash: 11878e6a0ac953b9b7eb27ce21bb67001f9d88d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127820"
---
# <a name="calldivideresults-function"></a>Calldivideresults-Funktion

Ruft Analyseergebnisse aus dem [**InkDivider**](inkdivider-class.md) -Objekt ab.

Diese Funktion ist nicht für die Verwendung durch den Anwendungscode vorgesehen.

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

*hdivider* \[ in\]
</dt> <dd>

Ein Handle für das [**InkDivider**](inkdivider-class.md) -Objekt.

</dd> <dt>

*awordstrokeids* \[ vorgenommen\]
</dt> <dd>

Ein Array von Bezeichner, die dem Wort zugeordnet sind, das an die [**InkDivider**](inkdivider-class.md) -Klasse weitergeleitet wird.

</dd> <dt>

*alinestrokeids* \[ vorgenommen\]
</dt> <dd>

Ein Array von [**ID**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) -Eigenschaften für die [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) -Objekte, die der Zeile zugeordnet sind, die an die [**InkDivider**](inkdivider-class.md) -Klasse weitergeleitet wird.

</dd> <dt>

*aparagphstrokeids* \[ vorgenommen\]
</dt> <dd>

Ein Array der [**ID**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) -Eigenschaften für die [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) -Objekte, die dem Absatz der [**InkDivider**](inkdivider-class.md) -Klasse zugeordnet sind.

</dd> <dt>

*adrawingstrokeids* \[ vorgenommen\]
</dt> <dd>

Ein Array von [**ID**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) -Eigenschaften für die [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) -Objekte, die der Zeichnung aus der [**InkDivider**](inkdivider-class.md) -Klasse zugeordnet sind.

</dd> <dt>

*paarwörter* \[ vorgenommen\]
</dt> <dd>

Ein Array von Wörtern, das von der Ink-Analyse zurückgegeben wird

</dd> <dt>

*Paare* \[ vorgenommen\]
</dt> <dd>

Ein Array von Zeilen, die von der Ink-Analyse zurückgegeben werden

</dd> <dt>

*Paare* \[ vorgenommen\]
</dt> <dd>

Ein Array von Absätzen, die von der Ink-Analyse zurückgegeben werden

</dd> <dt>

*awordrotationcenterx* \[ vorgenommen\]
</dt> <dd>

Ein Array von den Mittelpunkten der Wörter entlang der x-Achse aus der Ink-Analyse.

</dd> <dt>

*awordrotationcentery* \[ vorgenommen\]
</dt> <dd>

Ein Array von den Mittelpunkten der Wörter entlang der y-Achse aus der Ink-Analyse.

</dd> <dt>

*awordangle* \[ vorgenommen\]
</dt> <dd>

Ein Array mit den Winkeln, nach denen die Wörter für optimale Analyseergebnisse gedreht werden.

</dd> <dt>

*alinerotationcenterx* \[ vorgenommen\]
</dt> <dd>

Ein Array, das die Mittelpunkte der Linien entlang der x-Achse enthält.

</dd> <dt>

*alinerotationcentery* \[ vorgenommen\]
</dt> <dd>

Ein Array, das die Mittelpunkte der Linien entlang der y-Achse enthält.

</dd> <dt>

*alineangle* \[ vorgenommen\]
</dt> <dd>

Ein Array, das die Winkel enthält, nach denen die Linien für optimale Analyseergebnisse gedreht werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                   | Beschreibung                                                       |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Die Funktion wurde erfolgreich ausgeführt.<br/>                                |
| <dl> <dt>**E \_ invalidArg**</dt> </dl>  | Der *hdivider* -Parameter ist ungültig.<br/>                   |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Es konnte nicht genügend Arbeitsspeicher belegt werden, um die Ergebnisse zu speichern.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Um Speicher Verluste zu vermeiden, müssen Sie die Ressourcen für " *paarweise*", " *paarweise*" und " *paarweise*" freigeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                         |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                             |
| Bibliothek<br/>                  | <dl> <dt>InkDiv.dll</dt> </dl> |



 

 




