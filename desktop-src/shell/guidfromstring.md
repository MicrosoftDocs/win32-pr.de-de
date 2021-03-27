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
ms.openlocfilehash: a29a2138f4bcc7435a0d7864f65dd60ab16519c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864939"
---
# <a name="guidfromstring-function"></a>GUIDFromString-Funktion

\[" **GUIDFromString** " ist über Windows XP mit Service Pack 2 (SP2) oder Windows Vista verfügbar. Sie wird möglicherweise in nachfolgenden Versionen geändert oder ist nicht verfügbar. Anwendungen sollten anstelle dieser Funktion " [**CLSIDFromString**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromstring) " oder " [**IIDFromString**](/windows/win32/api/combaseapi/nf-combaseapi-iidfromstring) " verwenden.\]

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

*PSZ* \[ in\]
</dt> <dd>

Typ: **LPCTSTR**

Ein Zeiger auf die zu konvertierende NULL-terminierte Zeichenfolge. Die Zeichenfolge sollte in der folgenden Form vorliegen:

{00000000-0000-0000-0000-000000000000}

</dd> <dt>

*pguid* \[ vorgenommen\]
</dt> <dd>

Typ: **lpguid**

Zeiger auf einen Puffer, um die GUID zu erhalten, wenn diese Methode zurückgegeben wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **bool**

**True** , wenn die GUID erfolgreich erstellt wurde. andernfalls **false**.

## <a name="remarks"></a>Bemerkungen

Diese Funktion wird nicht in einem Header deklariert oder nach Name aus einer DLL-Datei exportiert. Sie muss aus Shell32.dll als Ordnungszahl 703 für **guidfromstraninga** und Ordnungszahl 704 für **guidfromstringw** geladen werden.

Sie können auch von Shlwapi.dll als Ordnungszahl 269 für **guidfromstraninga** und Ordnungszahl 270 für **guidfromstringw** aufgerufen werden.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **Guidfromstringw** (Unicode) und **guidfromstraninga** (ANSI)<br/>                |



 

 
