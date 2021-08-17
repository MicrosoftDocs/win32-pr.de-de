---
description: Legt die LineHeight-Eigenschaft für das InkDivider-Objekt fest.
ms.assetid: ce5e40c5-faa1-4d66-94f4-d5bd1a11ee4c
title: SetLineHeight-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetLineHeight
api_type:
- LibDef
api_location:
- InkDiv.dll
- InkDiv.dll.dll
ms.openlocfilehash: 2c6a176b5878b7aaee4a0e51a5a366302b13a1a643453ad2c6d57e103362c4fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966819"
---
# <a name="setlineheight-function"></a>SetLineHeight-Funktion

Legt die [**LineHeight-Eigenschaft**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_lineheight) für das [**InkDivider-Objekt**](inkdivider-class.md) fest.

Diese Hilfsfunktion ist nicht für die Verwendung durch Anwendungscode vorgesehen.

## <a name="syntax"></a>Syntax


```C++
HRESULT WINAPI SetLineHeight(
  _In_ INT_PTR hDivider,
  _In_ LONG    lLineHeight
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hDivider* \[ In\]
</dt> <dd>

Ein Handle für das [**InkDivider-Objekt.**](inkdivider-class.md)

</dd> <dt>

*lLineHeight* \[ In\]
</dt> <dd>

Die [**LineHeight-Eigenschaft**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_lineheight) des [**InkDivider-Objekts**](inkdivider-class.md) in HIMETRIC-Einheiten.

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



 

 
