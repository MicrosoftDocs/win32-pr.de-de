---
description: Die getpropertytext-Funktion gibt einen Zeiger auf den Eigenschafts Text zurück.
ms.assetid: 1bcbdbb8-4ec5-4cea-a1c6-4a1f37476f50
title: Getpropertytext-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPropertyText
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 10dbabf32840d2ae5f965687a6261b8bec27a1a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342749"
---
# <a name="getpropertytext-function"></a>Getpropertytext-Funktion

Die **getpropertytext** -Funktion gibt einen Zeiger auf den Eigenschafts Text zurück.

## <a name="syntax"></a>Syntax


```C++
LPSTR WINAPI GetPropertyText(
  _In_ HFRAME         hFrame,
  _In_ LPPROPERTYINST lpPI,
  _In_ LPSTR          szBuffer,
  _In_ DWORD          BufferSize
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hframe* \[ in\]
</dt> <dd>

Handle für den Frame.

</dd> <dt>

*lppi* \[ in\]
</dt> <dd>

Zeiger auf eine Eigenschaften Instanz.

</dd> <dt>

*szBuffer* \[ in\]
</dt> <dd>

Ein Zeiger auf die Zeichenfolge der Eigenschaften Text.

</dd> <dt>

*BufferSize* \[ in\]
</dt> <dd>

Größe des Textzeichen folgen Puffers.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert ein Zeiger auf den Eigenschaften Text.

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert **null**.

## <a name="remarks"></a>Bemerkungen

[*Experten*](e.md) und [*Parser*](p.md) können die **getpropertytext** -Funktion aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Bibliothek<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




