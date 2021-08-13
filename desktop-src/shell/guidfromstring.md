---
description: Konvertiert eine Zeichenfolge in eine GUID.
ms.assetid: 109b99e6-7409-44e0-932c-658be66651f4
title: GUIDFromString-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GUIDFromString
- GUIDFromStringA
- GUIDFromStringW
api_type:
- DllExport
api_location:
- Shell32.dll
- API-MS-Win-shlwapi-ie-l1-1-0.dll
- shlwapi.dll
ms.openlocfilehash: 38dd6d6365c3b306e63634fee02ac7add07b1bf262598efc88ffec2595e14c82
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119351060"
---
# <a name="guidfromstring-function"></a>GUIDFromString-Funktion

\[**GUIDFromString** ist über Windows XP mit Service Pack 2 (SP2) oder Windows Vista verfügbar. Sie kann in nachfolgenden Versionen geändert oder nicht verfügbar sein. Anwendungen sollten ANSTELLE dieser Funktion [**CLSIDFromString**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromstring) oder [**IIDFromString**](/windows/win32/api/combaseapi/nf-combaseapi-iidfromstring) verwenden.\]

Konvertiert eine Zeichenfolge in eine GUID.

## <a name="syntax"></a>Syntax


```C++
BOOL GUIDFromString(
  _In_  LPCTSTR psz,
  _Out_ LPGUID  pguid
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*psz* \[ In\]
</dt> <dd>

Typ: **LPCTSTR**

Ein Zeiger auf die auf NULL endende Zeichenfolge, die konvertiert werden soll. Die Zeichenfolge sollte folgendes Format haben:

{00000000-0000-0000-0000-000000000000}

</dd> <dt>

*pguid* \[ out\]
</dt> <dd>

Typ: **LPGUID**

Zeiger auf einen Puffer, der die GUID empfängt, wenn diese Methode zurückgegeben wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **BOOL**

**TRUE,** wenn die GUID erfolgreich erstellt wurde; Andernfalls **FALSE**.

## <a name="remarks"></a>Hinweise

Diese Funktion wird nicht in einem Header deklariert oder anhand des Namens aus einer .dll Datei exportiert. Sie muss aus Shell32.dll als Ordnungszahl 703 für **GUIDFromStringA** und ordinal 704 für **GUIDFromStringW** geladen werden.

Der Zugriff ist auch über Shlwapi.dll als Ordnungszahl 269 für **GUIDFromStringA** und Ordnungszahl 270 für **GUIDFromStringW** möglich.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **GUIDFromStringW** (Unicode) und **GUIDFromStringA** (ANSI)<br/>                |



 

 
