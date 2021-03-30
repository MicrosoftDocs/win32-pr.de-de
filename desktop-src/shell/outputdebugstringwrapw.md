---
description: Sendet eine Unicode-Zeichenfolge zur Anzeige an den Debugger.
ms.assetid: 26cf4750-8ca1-4a9a-8378-d65ed288b358
title: Outputdebug-Funktion (shlwapip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OutputDebugStringWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: e8213aee48a90a816e2968aac115159472ed7b8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104994822"
---
# <a name="outputdebugstringwrapw-function"></a>Outputdebug-Funktion

\[Diese Funktion ist für die Verwendung in Windows XP verfügbar. Sie ist möglicherweise in nachfolgenden Versionen nicht verfügbar. Verwenden Sie [**outputentbugstringw**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) an seiner Stelle.\]

Sendet eine Unicode-Zeichenfolge zur Anzeige an den Debugger.

> [!Note]  
> **Outputentbugstringwrapw** ist ein Wrapper für die **outputdebug** -Funktion. Weitere Hinweise zur Verwendung finden Sie auf der Seite [**OutputDebugString**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) .

 

## <a name="syntax"></a>Syntax


```C++
void OutputDebugStringWrapW(
  _In_ LPCWSTR lpOutputString
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lpoutputstring* \[ in\]
</dt> <dd>

Typ: **LPCWSTR**

Ein Zeiger auf die auf NULL endende Unicode-Zeichenfolge, die angezeigt werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

**Outputdebugstringwrapw** bietet die Möglichkeit, Unicode-Zeichen folgen in Betriebssystemen vor Windows XP zu verwenden. Die bevorzugte Methode ist die Verwendung von [**OutputDebugStringW**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) in Verbindung mit der Microsoft-Schicht für Unicode (MSLU).

**Outputdebug-wrapw** muss direkt aus Shlwapi.dll aufgerufen werden. dabei wird die Ordnungszahl 115 verwendet.

Wenn die Anwendung über keinen Debugger verfügt, zeigt der System Debugger die Zeichenfolge an. Wenn die Anwendung keinen Debugger hat und der System Debugger nicht aktiv ist, führt **outputdebugstringwrapw keine Aktion** aus.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, Windows XP \[ Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>Shlwapip. h</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shlwapi.dll (Version 5,0 oder höher)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**OutputDebugString**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa)
</dt> </dl>

 

 
