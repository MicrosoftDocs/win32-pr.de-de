---
description: Setzt einen Datei Suchvorgang fort.
ms.assetid: 5b1a8f67-7fce-4ba5-918d-826bdaca1947
title: Cscfindnextfilew-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSCFindNextFileW
api_type:
- DllExport
api_location:
- Cscmig.dll
ms.openlocfilehash: 50b387a1ff99a95fcbe0fae8fe8ad93d14c335b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351352"
---
# <a name="cscfindnextfilew-function"></a>Cscfindnextfilew-Funktion

\[Diese Funktion wird nicht unterstützt und sollte nicht verwendet werden.\]

Setzt einen Datei Suchvorgang fort.

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI CSCFindNextFileW(
  _In_  HANDLE           hFind,
  _Out_ WIN32_FIND_DATAW *lpFind32,
  _Out_ LPDWORD          lpdwStatus,
  _Out_ LPDWORD          lpdwPinCount,
  _Out_ LPDWORD          lpdwHintFlags,
  _In_  FILETIME         *lpOrgFileTime
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hfind* \[ in\]
</dt> <dd>

Ein Suchhandle, das von der [**cscfindfirstfilew**](cscfindfirstfilew.md) -Funktion zurückgegeben wird.

</dd> <dt>

*lpFind32* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf die [**Win32 \_ - \_ Daten**](/windows/win32/api/minwinbase/ns-minwinbase-win32_find_dataa) Struktur, die Informationen über die Datei oder das Unterverzeichnis empfängt.

</dd> <dt>

*lpdwstatus* \[ vorgenommen\]
</dt> <dd>

Ein NTSTATUS-Code, der den Status des Aufrufes angibt.

</dd> <dt>

*lpdwpincount* \[ vorgenommen\]
</dt> <dd>

Dieser Parameter ist ungleich 0 (null), wenn die Datei offline verfügbar gemacht wurde, andernfalls 0.

</dd> <dt>

*lpdwhintflags* \[ vorgenommen\]
</dt> <dd>

Dieser Parameter kann einen der folgenden Werte annehmen.



| Wert                                                                                                                                                                                                                                                                                | Bedeutung                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FLAG_CSC_HINT_PIN_USER"></span><span id="flag_csc_hint_pin_user"></span><dl> <dt>**Flag \_ CSC- \_ Hinweis- \_ Pin- \_ Benutzer**</dt> <dt>0x01</dt> </dl>                                | Ein Benutzer hat die Datei offline verfügbar gemacht.<br/>                                                                                                |
| <span id="FLAG_CSC_HINT_PIN_INHERIT_USER"></span><span id="flag_csc_hint_pin_inherit_user"></span><dl> <dt>**Flag \_ CSC- \_ Hinweis- \_ Pin \_ erben \_ Benutzer**</dt> <dt>0x02</dt> </dl>       | Ein Benutzer hat das übergeordnete Element offline verfügbar gemacht und als übergeordnetes Element gekennzeichnet, sodass die untergeordneten Elemente offline verfügbar sind.<br/>                           |
| <span id="FLAG_CSC_HINT_PIN_INHERIT_SYSTEM"></span><span id="flag_csc_hint_pin_inherit_system"></span><dl> <dt>**Flag \_ CSC- \_ Hinweis- \_ Pin \_ erbt \_ System**</dt> <dt>0x04</dt> </dl> | Ein Administrator oder eine Gruppenrichtlinie hat das übergeordnete Element offline zur Verfügung gestellt und als übergeordnetes Element gekennzeichnet, sodass die untergeordneten Elemente offline verfügbar sind.<br/> |
| <span id="FLAG_CSC_HINT_PIN_SYSTEM"></span><span id="flag_csc_hint_pin_system"></span><dl> <dt>**Flag \_ CSC- \_ Hinweis- \_ Pin- \_ System**</dt> <dt>0x10</dt> </dl>                          | Die Datei wurde von einem Administrator oder einer Gruppenrichtlinie offline verfügbar gemacht.<br/>                                                                      |



 

</dd> <dt>

*lporgfiletime* \[ in\]
</dt> <dd>

Ein Zeiger auf eine [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) -Struktur, um die Datums-und Uhrzeit Informationen für die Datei oder das Unterverzeichnis zu erhalten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt **true** zurück, wenn Sie erfolgreich ist. Andernfalls wird **false** zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|---------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Cscmig.dll</dt> </dl> |



 

 
