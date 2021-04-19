---
description: Ruft die ID-Eigenschaften für die IInkStrokeDisp-Objekte des entsprechenden Worts, der Zeile, des Absatzes oder der Zeichnung ab, die durch eine Handschrift Analyse bestimmt werden.
ms.assetid: f05ffa3b-2a47-46fe-bb8f-e682aa094b69
title: Calldivideresultstrokeids-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CallDivideResultsStrokeIds
api_type:
- LibDef
api_location:
- InkDiv.dll
- InkDiv.dll.dll
ms.openlocfilehash: ee690c9564df3b8c75eca6eec8eeb88b7531f4ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344630"
---
# <a name="calldivideresultsstrokeids-function"></a>Calldivideresultstrokeids-Funktion

Ruft die [**ID**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) -Eigenschaften für die [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) -Objekte des entsprechenden Worts, der Zeile, des Absatzes oder der Zeichnung ab, die durch eine Handschrift Analyse bestimmt werden.

Diese Funktion ist nicht für die Verwendung durch den Anwendungscode vorgesehen.

## <a name="syntax"></a>Syntax


```C++
HRESULT WINAPI CallDivideResultsStrokeIds(
  _In_  INT_PTR hDivider,
  _Out_ int     aWordStrokeIds[],
  _Out_ int     aLineStrokeIds[],
  _Out_ int     aParagraphStrokeIds[],
  _Out_ int     aDrawingStrokeIds[]
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hdivider* \[ in\]
</dt> <dd>

Ein Handle für das [Divider](the-divider-object.md) -Objekt.

</dd> <dt>

*awordstrokeids \[ \]* \[out\]
</dt> <dd>

Ein Array der Strich-IDs der frei Hand Eingaben im Wort.

</dd> <dt>

*alinestrokeids \[ \]* \[out\]
</dt> <dd>

Ein Array der Strich-IDs der frei Hand Eingabe in der Zeile.

</dd> <dt>

*aparagphstrokeids \[ \]* \[out\]
</dt> <dd>

Ein Array der Strich-IDs der frei Hand Eingaben im Absatz.

</dd> <dt>

*adrawingstrokeids \[ \]* \[out\]
</dt> <dd>

Ein Array der Strich-IDs der frei Hand Eingaben in der Zeichnung.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                  | Beschreibung                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Die Funktion wurde erfolgreich ausgeführt.<br/>              |
| <dl> <dt>**E \_ invalidArg**</dt> </dl> | Der *hdivider* -Parameter ist ungültig.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                         |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                             |
| Bibliothek<br/>                  | <dl> <dt>InkDiv.dll</dt> </dl> |



 

 




