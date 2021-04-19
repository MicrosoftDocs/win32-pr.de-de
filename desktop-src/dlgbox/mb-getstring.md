---
title: MB_GetString-Funktion (User. h)
description: Gibt Zeichen folgen für standardmäßige Meldungs Feld Schaltflächen
ms.assetid: D2AF238D-F5A8-477D-BF47-0F5D4D68B27E
keywords:
- Dialog Felder für die MB_GetString Funktion
topic_type:
- apiref
api_name:
- MB_GetString
api_location:
- user32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eafd33f268f2ef1ef87755b79aba6d5d0aa77bb7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362063"
---
# <a name="mb_getstring-function"></a>MB \_ GetString-Funktion

Gibt Zeichen folgen für standardmäßige Meldungs Feld Schaltflächen

## <a name="syntax"></a>Syntax


```C++
LPCWSTR WINAPI MB_GetString(
   UINT wBtn
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wbtn* 
</dt> <dd>

Die ID der zurück zugebende Zeichenfolge. Diese werden durch die Befehls-ID-Werte des Dialog Felds identifiziert, die in winuser. h aufgeführt sind.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Zeichenfolge oder NULL, wenn Sie nicht gefunden wurde.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>User. h</dt> </dl>     |
| Bibliothek<br/> | <dl> <dt>User32. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>User32.dll</dt> </dl> |



 

 





