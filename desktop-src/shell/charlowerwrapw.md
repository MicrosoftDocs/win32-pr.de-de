---
description: Konvertiert eine Unicode-Zeichenfolge oder ein einzelnes Zeichen in Kleinbuchstaben.
ms.assetid: 09b7cf8e-6aed-40f4-9dfa-29be3559ae89
title: CharLowerWrapW-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CharLowerWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: c9a02e89713dd82de63817c00d5402fabe991fed565ebe33fa40286ad30058d4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119710750"
---
# <a name="charlowerwrapw-function"></a>CharLowerWrapW-Funktion

\[**CharLowerWrapW** ist für die Verwendung in Windows XP verfügbar. In nachfolgenden Versionen ist sie möglicherweise nicht verfügbar. Sie sollten [**CharLowerW**](/windows/win32/api/winuser/nf-winuser-charlowera) an seiner Stelle verwenden.\]

Konvertiert eine Unicode-Zeichenfolge oder ein einzelnes Zeichen in Kleinbuchstaben. Wenn der Operand eine Zeichenfolge ist, konvertiert die Funktion die Zeichen an Ort und Stelle.

> [!Note]  
> **CharLowerWrapW** ist ein Wrapper für die **CharLowerW-Funktion.** Weitere Hinweise zur Verwendung finden Sie auf der Seite [**CharLower.**](/windows/win32/api/winuser/nf-winuser-charlowera)

 

## <a name="syntax"></a>Syntax


```C++
LPWSTR CharLowerWrapW(
  _Inout_ LPWSTR pch
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pch* \[ in, out\]
</dt> <dd>

Typ: **LPWSTR**

Ein Zeiger auf eine mit NULL beendete Unicode-Zeichenfolge oder ein einzelnes Zeichen. Wenn das obere Wort dieses Parameters 0 (null) ist, darf das niedrigwertigen Wort nur ein einzelnes Zeichen enthalten, das konvertiert werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **LPWSTR**

Wenn *pch* eine Zeichenfolge ist, gibt die Funktion einen Zeiger auf die konvertierte Zeichenfolge zurück. Da die Zeichenfolge an Ort und Stelle konvertiert wird, ist der Rückgabewert gleich *pch.*

Wenn *pch* ein einzelnes Zeichen ist, ist der Rückgabewert ein 32-Bit-Wert, dessen hochwertiges Wort 0 (null) ist und das konvertierte Zeichen enthält.

Es gibt keinen Hinweis auf Erfolg oder Fehler. Fehler sind selten. Es gibt keine erweiterten Fehlerinformationen für diese Funktion. Rufen Sie [**getLastError nicht auf.**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)

## <a name="remarks"></a>Hinweise

Die bevorzugte Methode ist die Verwendung [**von CharLowerW**](/windows/win32/api/winuser/nf-winuser-charlowera) in Verbindung mit microsoft Layer for Unicode (MSLU).

**CharLowerWrapW** muss mithilfe der Ordnungszahl 38 direkt Shlwapi.dll aufgerufen werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shlwapi.dll (Version 5.0 oder höher)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CharLower**](/windows/win32/api/winuser/nf-winuser-charlowera)
</dt> </dl>

 

 
