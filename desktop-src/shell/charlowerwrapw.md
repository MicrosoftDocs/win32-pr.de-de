---
description: Konvertiert eine Unicode-Zeichenfolge oder ein einzelnes Zeichen in Kleinbuchstaben.
ms.assetid: 09b7cf8e-6aed-40f4-9dfa-29be3559ae89
title: Charlowerwrapw-Funktion
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
ms.openlocfilehash: 3911e0366d30f3eb9420391f9d06867ded73530e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525400"
---
# <a name="charlowerwrapw-function"></a>Charlowerwrapw-Funktion

\[**Charlowerwrapw** ist für die Verwendung in Windows XP verfügbar. Sie ist möglicherweise in nachfolgenden Versionen nicht verfügbar. Sie sollten " [**charlowerw**](/windows/win32/api/winuser/nf-winuser-charlowera) " an seiner Stelle verwenden.\]

Konvertiert eine Unicode-Zeichenfolge oder ein einzelnes Zeichen in Kleinbuchstaben. Wenn der Operand eine Zeichenfolge ist, konvertiert die-Funktion die Zeichen an Ort und Stelle.

> [!Note]  
> **Charlowerwrapw** ist ein Wrapper für die Funktion " **charlowerw** ". Weitere Hinweise zur Verwendung finden Sie auf der Seite [**charlower**](/windows/win32/api/winuser/nf-winuser-charlowera) .

 

## <a name="syntax"></a>Syntax


```C++
LPWSTR CharLowerWrapW(
  _Inout_ LPWSTR pch
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PCH* \[ in, out\]
</dt> <dd>

Typ: **LPWSTR**

Ein Zeiger auf eine NULL-terminierte Unicode-Zeichenfolge oder ein einzelnes Zeichen. Wenn das höchst wertige Wort dieses Parameters NULL ist, muss das nieder wertige Wort nur ein einzelnes Zeichen enthalten, das konvertiert werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **LPWSTR**

Wenn *PCH* eine Zeichenfolge ist, gibt die Funktion einen Zeiger auf die konvertierte Zeichenfolge zurück. Da die Zeichenfolge direkt konvertiert wird, entspricht der Rückgabewert dem *PCH*.

Wenn *PCH* ein einzelnes Zeichen ist, ist der Rückgabewert ein 32-Bit-Wert, dessen hohes Wort 0 (null) ist, und das nieder wertige Wort enthält das konvertierte Zeichen.

Es gibt keinen Hinweis auf Erfolg oder Fehler. Der Fehler tritt selten auf. Es sind keine erweiterten Fehlerinformationen für diese Funktion vorhanden. " [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)" nicht aufrufen.

## <a name="remarks"></a>Bemerkungen

Die bevorzugte Methode ist die Verwendung von [**charlowerw**](/windows/win32/api/winuser/nf-winuser-charlowera) in Verbindung mit der Microsoft-Schicht für Unicode (MSLU).

**Charlowerwrapw** muss direkt aus Shlwapi.dll aufgerufen werden. dabei wird die Ordnungszahl 38 verwendet.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, Windows XP \[ Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shlwapi.dll (Version 5,0 oder höher)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Charlower**](/windows/win32/api/winuser/nf-winuser-charlowera)
</dt> </dl>

 

 
