---
description: Testet, ob das InkDivider-Objekt die inkrecognizercontext-Klasse zum Analysieren von Wörtern verwenden kann.
ms.assetid: fd848fcc-5258-401f-8b51-b9d57da173da
title: Erkennzercontextset-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RecognizerContextSet
api_type:
- LibDef
api_location:
- InkDiv.dll
- InkDiv.dll.dll
ms.openlocfilehash: 51e75b810c2103afed2e8ac8a28706b9c9af5da0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865812"
---
# <a name="recognizercontextset-function"></a>Erkennzercontextset-Funktion

Testet, ob das [**InkDivider**](inkdivider-class.md) -Objekt die [**inkrecognizercontext**](inkrecognizercontext-class.md) -Klasse zum Analysieren von Wörtern verwenden kann.

Diese Funktion ist nicht für die Verwendung durch den Anwendungscode vorgesehen.

## <a name="syntax"></a>Syntax


```C++
HRESULT WINAPI RecognizerContextSet(
  _In_ INT_PTR hDivider
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hdivider* \[ in\]
</dt> <dd>

Ein Handle für das [**InkDivider**](inkdivider-class.md) -Objekt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                  | Beschreibung                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Die Funktion wurde erfolgreich ausgeführt.<br/>              |
| <dl> <dt>**E \_ invalidArg**</dt> </dl> | Der *pdivider* -Parameter ist ungültig.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                         |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                             |
| Bibliothek<br/>                  | <dl> <dt>InkDiv.dll</dt> </dl> |



 

 




