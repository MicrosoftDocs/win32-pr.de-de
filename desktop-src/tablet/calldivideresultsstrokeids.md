---
description: Ruft die Id-Eigenschaften für die IInkStrokeDisp-Objekte des entsprechenden Worts, der Zeile, des Absatzes oder der Zeichnung ab, die von der Freihandanalyse bestimmt werden.
ms.assetid: f05ffa3b-2a47-46fe-bb8f-e682aa094b69
title: CallDivideResultsStrokeIds-Funktion
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
ms.openlocfilehash: 64b3e4180a34c45890408f8ba92cc79465fffa7f1028152e27f8d5c0aa40e3e1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120009130"
---
# <a name="calldivideresultsstrokeids-function"></a>CallDivideResultsStrokeIds-Funktion

Ruft die [**Id-Eigenschaften**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) für die [**IInkStrokeDisp-Objekte**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) des entsprechenden Worts, der Zeile, des Absatzes oder der Zeichnung ab, die von der Freihandanalyse bestimmt werden.

Diese Funktion ist nicht für die Verwendung durch Anwendungscode vorgesehen.

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

*hDivider* \[ In\]
</dt> <dd>

Ein Handle für das [Divider-Objekt.](the-divider-object.md)

</dd> <dt>

*aWordStrokeIds \[ \]* \[out\]
</dt> <dd>

Ein Array der Strich-IDs der Ink im Wort.

</dd> <dt>

*aLineStrokeIds \[ \]* \[out\]
</dt> <dd>

Ein Array der Strich-IDs der Ink in der Zeile.

</dd> <dt>

*aParagraphStrokeIds \[ \]* \[out\]
</dt> <dd>

Ein Array der Strich-IDs der Ink im Absatz.

</dd> <dt>

*aDrawingStrokeIds \[ \]* \[out\]
</dt> <dd>

Ein Array der Strich-IDs der Ink in der Zeichnung.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                  | Beschreibung                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Die Funktion wurde erfolgreich ausgeführt.<br/>              |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Der *hDivider-Parameter* ist ungültig.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                         |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                             |
| Bibliothek<br/>                  | <dl> <dt>InkDiv.dll</dt> </dl> |



 

 




