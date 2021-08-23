---
description: Sucht im Offlinedateien Cache nach einer Datei, die die angegebenen Kriterien erfüllt.
ms.assetid: 09de6c55-fc37-4c0a-b5a0-ea73f06793d5
title: CSCFindFirstFileW-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSCFindFirstFileW
api_type:
- DllExport
api_location:
- Cscmig.dll
ms.openlocfilehash: 7289fb19a0062ce66212927bbe3e77c9e90c54ceb1980f83265000cc228e27ab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119833410"
---
# <a name="cscfindfirstfilew-function"></a>CSCFindFirstFileW-Funktion

\[Diese Funktion wird nicht unterstützt und sollte nicht verwendet werden.\]

Sucht im Offlinedateien Cache nach einer Datei, die die angegebenen Kriterien erfüllt.

## <a name="syntax"></a>Syntax


```C++
HANDLE WINAPI CSCFindFirstFileW(
  _In_  LPCWSTR          lpszFileName,
  _Out_ WIN32_FIND_DATAW *lpFind32,
  _Out_ LPDWORD          lpdwStatus,
  _Out_ LPDWORD          lpdwPinCount,
  _Out_ LPDWORD          lpdwHintFlags,
  _Out_ FILETIME         *lpOrgFileTime
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lpszFileName* \[ In\]
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die ein gültiges UNC-Verzeichnis oder einen gültigen UNC-Pfad angibt.

</dd> <dt>

*lpFind32* \[ out\]
</dt> <dd>

Ein Zeiger auf die [**WIN32 \_ FIND \_ DATA-Struktur,**](/windows/win32/api/minwinbase/ns-minwinbase-win32_find_dataa) die Informationen über die Datei oder das Unterverzeichnis empfängt.

</dd> <dt>

*lpdwStatus* \[ out\]
</dt> <dd>

Ein NTSTATUS-Code, der den Status des Aufrufs angibt.

</dd> <dt>

*lpdwPinCount* \[ out\]
</dt> <dd>

Dieser Parameter ist ungleich 0 (null), wenn die Datei offline verfügbar gemacht wurde, andernfalls 0.

</dd> <dt>

*lpdwHintFlags* \[ out\]
</dt> <dd>

Dieser Parameter kann einen der folgenden Werte annehmen.



| Wert                                                                                                                                                                                                                                                                                | Bedeutung                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FLAG_CSC_HINT_PIN_USER"></span><span id="flag_csc_hint_pin_user"></span><dl> <dt>**FLAG \_ BENUTZER-0X01 MIT \_ CSC-HINWEIS \_ ANHEFTEN \_**</dt> <dt></dt> </dl>                                | Ein Benutzer hat die Datei offline verfügbar gemacht.<br/>                                                                                                |
| <span id="FLAG_CSC_HINT_PIN_INHERIT_USER"></span><span id="flag_csc_hint_pin_inherit_user"></span><dl> <dt>**FLAG \_ CSC \_ HINT \_ PIN INHERIT \_ \_ USER**</dt> <dt>0x02</dt> </dl>       | Ein Benutzer hat das übergeordnete Element offline verfügbar gemacht und das übergeordnete Element so gekennzeichnet, dass seine untergeordneten Elemente offline verfügbar sind.<br/>                           |
| <span id="FLAG_CSC_HINT_PIN_INHERIT_SYSTEM"></span><span id="flag_csc_hint_pin_inherit_system"></span><dl> <dt>**FLAG \_ CSC \_ HINT \_ PIN INHERIT \_ \_ SYSTEM**</dt> <dt>0x04</dt> </dl> | Ein Administrator oder eine Gruppenrichtlinie hat das übergeordnete Element offline verfügbar gemacht und das übergeordnete Element so gekennzeichnet, dass seine untergeordneten Elemente offline verfügbar sind.<br/> |
| <span id="FLAG_CSC_HINT_PIN_SYSTEM"></span><span id="flag_csc_hint_pin_system"></span><dl> <dt>**FLAG \_ CSC \_ HINT \_ PIN \_ SYSTEM**</dt> <dt>0x10</dt> </dl>                          | Ein Administrator oder eine Gruppenrichtlinie hat die Datei offline verfügbar gemacht.<br/>                                                                      |



 

</dd> <dt>

*lpOrgFileTime* \[ out\]
</dt> <dd>

Ein Zeiger auf eine [**FILETIME-Struktur,**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) um die Datums- und Uhrzeitinformationen für die Datei oder das Unterverzeichnis zu erhalten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Suchhandle, das in einem nachfolgenden Aufruf von [**CSCFindNextFileW**](cscfindnextfilew.md) oder [**CSCFindClose**](cscfindclose.md)verwendet wird.

Wenn bei der Ausführung der Funktion ein Fehler auftritt, lautet der Rückgabewert **INVALID\_HANDLE\_VALUE**.

## <a name="remarks"></a>Hinweise

Dieser Funktion ist keine Importbibliothek oder Headerdatei zugeordnet. Sie müssen sie mithilfe der [**Funktionen LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|---------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Cscmig.dll</dt> </dl> |



 

 
