---
description: Bestimmt, ob ein Zeichen entweder ein alphabetisches oder ein numerisches Zeichen ist.
ms.assetid: d4b01ba5-e42a-4040-a763-ecef0c73977f
title: IsCharAlphaNumericWrapW-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IsCharAlphaNumericWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: bf0a9752162c1593928e1bed270859ec4166230fe1f7e2d46d979c5c989ca237
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118452995"
---
# <a name="ischaralphanumericwrapw-function"></a>IsCharAlphaNumericWrapW-Funktion

\[**IsCharAlphaNumericWrapW** ist für die Verwendung in Windows XP verfügbar. Sie ist in nachfolgenden Versionen nicht verfügbar. Sie sollten [**IsCharAlphaNumericW**](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica) an seiner Stelle verwenden.\]

Bestimmt, ob ein Zeichen entweder ein alphabetisches oder ein numerisches Zeichen ist. Diese Bestimmung basiert auf der Semantik der Sprache, die der Benutzer während des Setups oder über Systemsteuerung ausgewählt hat.

> [!Note]  
> **IsCharAlphaNumericWrapW** ist ein Wrapper für die **IsCharAlphaNumericW-Funktion.** Weitere Nutzungshinweise finden Sie auf der [**IsCharAlphaNumeric-Seite.**](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica)

 

## <a name="syntax"></a>Syntax


```C++
BOOL IsCharAlphaNumericWrapW(
  _In_ WCHAR ch
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ch* \[ In\]
</dt> <dd>

Typ: **WCHAR**

Das unicode-Zeichen, das getestet werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **BOOL**

Wenn das Zeichen alphanumerisch ist, ist der Rückgabewert ungleich 0 (null).

Wenn das Zeichen nicht alphanumerisch ist, ist der Rückgabewert 0 (null). Um erweiterte Fehlerinformationen zu erhalten, rufen Sie [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) auf.

## <a name="remarks"></a>Bemerkungen

**IsCharAlphaNumericWrapW** bietet die Möglichkeit, Unicode-Zeichenfolgen in Betriebssystemen vor Windows XP zu verwenden. Die bevorzugte Methode ist die Verwendung von [**IsCharAlphaNumericW**](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica) in Verbindung mit der Microsoft Layer for Unicode (MSLU).

**IsCharAlphaNumericWrapW** muss direkt über Shlwapi.dll aufgerufen werden, wobei Ordinalzahl 28 verwendet wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shlwapi.dll (Version 5.0 oder höher)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IsCharAlphaNumeric**](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica)
</dt> </dl>

 

 
