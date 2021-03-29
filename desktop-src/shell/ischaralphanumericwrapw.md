---
description: Bestimmt, ob ein Zeichen entweder ein alphabetisches oder ein numerisches Zeichen ist.
ms.assetid: d4b01ba5-e42a-4040-a763-ecef0c73977f
title: Ischaralpha anumschlag wrapw-Funktion
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
ms.openlocfilehash: bf7f1b4db54cc5374214ff45b51579556dc22062
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978121"
---
# <a name="ischaralphanumericwrapw-function"></a>Ischaralpha anumschlag wrapw-Funktion

\[**Ischaralpha anumschlag wrapw** ist für die Verwendung in Windows XP verfügbar. Sie wird in nachfolgenden Versionen nicht verfügbar sein. Sie sollten [**ischaralpha annumericw**](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica) anstelle von verwenden.\]

Bestimmt, ob ein Zeichen entweder ein alphabetisches oder ein numerisches Zeichen ist. Diese Bestimmung basiert auf der Semantik der Sprache, die während des Setups oder über die Systemsteuerung vom Benutzer ausgewählt wurde.

> [!Note]  
> **Ischaralpha anumericwrapw** ist ein Wrapper für die **ischaralpha anumericw** -Funktion. Weitere Hinweise zur Verwendung finden Sie auf der [**ischaralpha numerischen**](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica) Seite.

 

## <a name="syntax"></a>Syntax


```C++
BOOL IsCharAlphaNumericWrapW(
  _In_ WCHAR ch
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ch* \[ in\]
</dt> <dd>

Typ: **WCHAR**

Das zu testende Unicode-Zeichen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **bool**

Wenn das Zeichen alphanumerisch ist, ist der Rückgabewert ungleich 0 (null).

Wenn das Zeichen nicht alphanumerisch ist, ist der Rückgabewert 0 (null). Um erweiterte Fehlerinformationen zu erhalten, rufen Sie [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) auf.

## <a name="remarks"></a>Bemerkungen

**Ischaralpha anenumericwrapw** bietet die Möglichkeit, Unicode-Zeichen folgen in älteren Betriebssystemen als Windows XP zu verwenden. Die bevorzugte Methode ist die Verwendung von [**ischaralpha annumericw**](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica) in Verbindung mit der Microsoft-Schicht für Unicode (MSLU).

**Ischaralpha anumschlag wrapw** muss direkt aus Shlwapi.dll aufgerufen werden, und zwar mithilfe von Ordnungszahl 28.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, Windows XP \[ Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shlwapi.dll (Version 5,0 oder höher)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Ischaralpha numerisch**](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica)
</dt> </dl>

 

 
