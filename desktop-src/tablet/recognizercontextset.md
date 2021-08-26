---
description: Testet, ob das InkDivider-Objekt die InkRecognizerContext-Klasse zum Analysieren von Wörtern verwenden kann.
ms.assetid: fd848fcc-5258-401f-8b51-b9d57da173da
title: RecognizerContextSet-Funktion
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
ms.openlocfilehash: fee6fa3f9f9743f048cab4d9bee5af3fa9215ca903227acd0aa67cb68037550d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119934710"
---
# <a name="recognizercontextset-function"></a>RecognizerContextSet-Funktion

Testet, ob das [**InkDivider-Objekt**](inkdivider-class.md) die [**InkRecognizerContext-Klasse**](inkrecognizercontext-class.md) zum Analysieren von Wörtern verwenden kann.

Diese Funktion ist nicht für die Verwendung durch Anwendungscode vorgesehen.

## <a name="syntax"></a>Syntax


```C++
HRESULT WINAPI RecognizerContextSet(
  _In_ INT_PTR hDivider
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hDivider* \[ In\]
</dt> <dd>

Ein Handle für das [**InkDivider-Objekt.**](inkdivider-class.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                  | Beschreibung                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Die Funktion wurde erfolgreich ausgeführt.<br/>              |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Der *pDivider-Parameter* ist ungültig.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                         |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                             |
| Bibliothek<br/>                  | <dl> <dt>InkDiv.dll</dt> </dl> |



 

 




