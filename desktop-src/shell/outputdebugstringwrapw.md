---
description: Sendet eine Unicode-Zeichenfolge zur Anzeige an den Debugger.
ms.assetid: 26cf4750-8ca1-4a9a-8378-d65ed288b358
title: OutputDebugStringWrapW-Funktion (Shlwapip.h)
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
ms.openlocfilehash: cce8754b01ddf156951964b7189b4a7189759c52cdcd08e08091ca62b2e950bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117858789"
---
# <a name="outputdebugstringwrapw-function"></a>OutputDebugStringWrapW-Funktion

\[Diese Funktion ist für die Verwendung in Windows XP verfügbar. In nachfolgenden Versionen ist sie möglicherweise nicht verfügbar. Verwenden Sie [**OutputDebugStringW**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) an seiner Stelle.\]

Sendet eine Unicode-Zeichenfolge zur Anzeige an den Debugger.

> [!Note]  
> **OutputDebugStringWrapW** ist ein Wrapper für die **OutputDebugStringW-Funktion.** Weitere Nutzungshinweise finden Sie auf der Seite [**OutputDebugString.**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa)

 

## <a name="syntax"></a>Syntax


```C++
void OutputDebugStringWrapW(
  _In_ LPCWSTR lpOutputString
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lpOutputString* \[ In\]
</dt> <dd>

Typ: **LPCWSTR**

Ein Zeiger auf die auf NULL endende Unicode-Zeichenfolge, die angezeigt werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

**OutputDebugStringWrapW** bietet die Möglichkeit, Unicode-Zeichenfolgen in Betriebssystemen vor Windows XP zu verwenden. Die bevorzugte Methode ist die Verwendung von [**OutputDebugStringW**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) in Verbindung mit der Microsoft Layer for Unicode (MSLU).

**OutputDebugStringWrapW** muss direkt über Shlwapi.dll aufgerufen werden, wobei Ordinalzahl 115 verwendet wird.

Wenn die Anwendung über keinen Debugger verfügt, zeigt der Systemdebugger die Zeichenfolge an. Wenn die Anwendung über keinen Debugger verfügt und der Systemdebugger nicht aktiv ist, führt **OutputDebugStringWrapW** nichts aus.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>Shlwapip.h</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shlwapi.dll (Version 5.0 oder höher)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Outputdebugstring**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa)
</dt> </dl>

 

 
