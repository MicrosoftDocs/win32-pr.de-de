---
description: Die getprotocolfromtable-Funktion gibt ein Handle für ein Protokoll&\# 8212; basierend auf einer angegebenen Übergabe Tabelle und einem angegebenen Wert zurück.
ms.assetid: 34b07079-0b20-40d8-a529-4179ecc68ebf
title: Getprotocolfromtable-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetProtocolFromTable
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 498892fc2cc5ada2e177b8fb3f70f40a1ef10dfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958709"
---
# <a name="getprotocolfromtable-function"></a>Getprotocolfromtable-Funktion

Die **getprotocolfromtable** -Funktion gibt ein Handle für ein Protokoll zurück, das auf einer angegebenen Übergabe Tabelle und einem angegebenen Wert basiert.

## <a name="syntax"></a>Syntax


```C++
HPROTOCOL WINAPI GetProtocolFromTable(
  _In_  LPHANDOFFTABLE hTable,
  _In_  DWORD          ItemToFind,
  _Out_ PDWORD_PTR     lpInstData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*htable* \[ in\]
</dt> <dd>

Handle für eine Übergabe Tabelle.

</dd> <dt>

*Itemtefind* \[ in\]
</dt> <dd>

Der Wert, der verwendet wird, um das Protokoll in einer Übergabe Tabelle zu suchen. Der Wert muss in den Protokolldaten verfügbar sein.

</dd> <dt>

*lpinstdata* \[ vorgenommen\]
</dt> <dd>

Wenn Sie in der Übergabe Tabelle verfügbar sind, Instanzdaten für das nächste Protokoll. Instanzdaten dürfen nicht länger sein als eine Länge von DWORD \_ ptr.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert ein Protokoll handle.

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert **null**.

## <a name="remarks"></a>Bemerkungen

Beim Implementieren der " [Erkennungs](recognizeframe.md) Funktion"-Exportfunktion wird die **getprotocolfromtable** -Funktion verwendet, um ein Handle für das nächste Protokoll zu erhalten. Die **getprotocolfromtable** -Funktion wird aufgerufen, um ein Handle aus dem nächsten Protokoll abzurufen, wenn das Protokoll angibt, welches Protokoll befolgt wird.

**Instanzdaten**

Instanzdaten können beliebige Daten sein, die kleiner oder gleich einem DWORD- \_ ptr sind, oder ein Zeiger auf Daten, wie z. b. unformatierte Frame-Daten, die nicht vom Parser zugeordnet oder freigegeben werden müssen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Bibliothek<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Erkenzeframe](recognizeframe.md)
</dt> </dl>

 

 




