---
description: Die loaddword-Funktion wird vom Monitor aufgerufen, um eine DWORD-Variable mit einem Wert festzulegen, der aus einer HTML-Konfigurations Zeichenfolgen-Variablen entnommen wurde.
ms.assetid: 18a7beba-01f4-4f92-99bf-067f79f25db0
title: Loaddword-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadDWORD
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 1c66566090e38fc936a5616c8782284ad795df29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362734"
---
# <a name="loaddword-function"></a>Loaddword-Funktion

Die **loaddword** -Funktion wird vom Monitor aufgerufen, um eine **DWORD** -Variable mit einem Wert festzulegen, der aus einer HTML-Konfigurations Zeichenfolgen-Variablen entnommen wurde.

## <a name="syntax"></a>Syntax


```C++
BOOL LoadDWORD(
  _In_ const char  *pConfig,
  _In_ const char  *pVarName,
  _In_       DWORD *pValue
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pConfig* \[ in\]
</dt> <dd>

Zeiger auf die HTML-Konfigurations Zeichenfolge, die von der [Imonitor::D oconfigure](imonitor-doconfigure.md) -Methode an den Monitor übermittelt wurde.

</dd> <dt>

*pvarname* \[ in\]
</dt> <dd>

Zeiger auf den Namen der Variablen in der Konfigurations Zeichenfolge.

</dd> <dt>

*pValue* \[ in\]
</dt> <dd>

Ein Zeiger auf die **DWORD** -Variable, die auf den Wert der Konfigurations Zeichen folgen Variablen festgelegt ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist (wenn der Variablenname gefunden wurde und eine Zeichenfolge ungleich 0 (null) aufweist), wird das **DWORD** eingefügt, und der Rückgabewert ist " **true**".

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert **false**.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Bibliothek<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




