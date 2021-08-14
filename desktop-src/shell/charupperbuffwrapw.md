---
description: Konvertiert Kleinbuchstaben in einem Puffer in Großbuchstaben.
ms.assetid: 63293fda-6f55-419a-b5b4-7a3ada31580c
title: CharUpperBuffWrapW-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CharUpperBuffWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: 288a119586e9f2e58172daaba33a8b9f27c791aa0005b5349f47cb0b2670a631
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117861555"
---
# <a name="charupperbuffwrapw-function"></a>CharUpperBuffWrapW-Funktion

\[**CharUpperBuffWrapW** ist für die Verwendung in Windows XP verfügbar. In nachfolgenden Versionen ist sie möglicherweise nicht verfügbar. Sie sollten [**CharUpperBuffW**](/windows/win32/api/winuser/nf-winuser-charupperbuffa) an seiner Stelle verwenden.\]

Konvertiert Kleinbuchstaben in einem Puffer in Großbuchstaben. Die Funktion konvertiert die Zeichen an Ort und Stelle.

> [!Note]  
> **CharUpperBuffWrapW** ist ein Wrapper für die **CharUpperBuffW-Funktion.** Weitere Nutzungshinweise finden Sie auf der [**CharUpperBuff-Seite.**](/windows/win32/api/winuser/nf-winuser-charupperbuffa)

 

## <a name="syntax"></a>Syntax


```C++
DWORD CharUpperBuffWrapW(
  _In_ LPWSTR pch,
  _In_ DWORD  cchLength
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pch* \[ In\]
</dt> <dd>

Typ: **LPWSTR**

Ein Zeiger auf einen Puffer, der ein oder mehrere zu verarbeitende Unicode-Zeichen enthält.

</dd> <dt>

*cchLength* \[ In\]
</dt> <dd>

Typ: **DWORD**

Gibt die Größe des Puffers in Zeichen an, auf den *pch* zeigt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **DWORD**

Die Anzahl der verarbeiteten Zeichen.

## <a name="remarks"></a>Hinweise

Die bevorzugte Methode ist die Verwendung von [**CharUpperBuffW**](/windows/win32/api/winuser/nf-winuser-charupperbuffa) in Verbindung mit der Microsoft Layer for Unicode (MSLU).

**CharUpperBuffWrapW** muss direkt über Shlwapi.dll aufgerufen werden, wobei Ordinalzahl 44 verwendet wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shlwapi.dll (Version 5.0 oder höher)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CharUpperBuff**](/windows/win32/api/winuser/nf-winuser-charupperbuffa)
</dt> </dl>

 

 
