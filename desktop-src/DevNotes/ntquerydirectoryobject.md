---
description: Ruft Informationen zum angegebenen Verzeichnisobjekt ab.
ms.assetid: a2c67c4d-4753-4d47-a404-31d067a78bf4
title: NtQueryDirectoryObject-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtQueryDirectoryObject
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 11c7240cf63fa2f7e13338a0e0459e172e41aa1ed71db90c661b8aad0915d670
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079670"
---
# <a name="ntquerydirectoryobject-function"></a>NtQueryDirectoryObject-Funktion

\[Diese Funktion kann in Zukunft geändert oder nicht mehr verfügbar sein.\]

Ruft Informationen zum angegebenen Verzeichnisobjekt ab.

## <a name="syntax"></a>Syntax


```C++
NTSTATUS WINAPI NtQueryDirectoryObject(
  _In_      HANDLE  DirectoryHandle,
  _Out_opt_ PVOID   Buffer,
  _In_      ULONG   Length,
  _In_      BOOLEAN ReturnSingleEntry,
  _In_      BOOLEAN RestartScan,
  _Inout_   PULONG  Context,
  _Out_opt_ PULONG  ReturnLength
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*DirectoryHandle* \[ In\]
</dt> <dd>

Ein Handle für das Verzeichnisobjekt.

</dd> <dt>

*Puffer* \[ out, optional\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der die Verzeichnisinformationen empfängt. Dieser Puffer empfängt mindestens eine **OBJECT \_ DIRECTORY \_ INFORMATION-Struktur,** die letzte ist **NULL,** gefolgt von Zeichenfolgen, die die Namen der Verzeichniseinträge enthalten. Weitere Informationen finden Sie in den Hinweisen.

</dd> <dt>

*Länge* \[ In\]
</dt> <dd>

Die Größe des vom Benutzer bereitgestellten Ausgabepuffers in Bytes.

</dd> <dt>

*ReturnSingleEntry* \[ In\]
</dt> <dd>

Gibt an, ob die Funktion nur einen einzelnen Eintrag zurückgeben soll.

</dd> <dt>

*RestartScan* \[ In\]
</dt> <dd>

Gibt an, ob die Überprüfung neu gestartet oder die Enumeration mithilfe der im *Context-Parameter* übergebenen Informationen fortgesetzt werden soll.

</dd> <dt>

*Kontext* \[ in, out\]
</dt> <dd>

Der Enumerationskontext.

</dd> <dt>

*ReturnLength* \[ out, optional\]
</dt> <dd>

Ein Zeiger auf eine Variable, die die Länge der im Ausgabepuffer zurückgegebenen Verzeichnisinformationen in Bytes empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Funktion gibt **STATUS \_ SUCCESS** oder einen Fehlerstatus zurück.

## <a name="remarks"></a>Hinweise

Im Folgenden wird die Definition der **OBJECT \_ DIRECTORY \_ INFORMATION-Struktur** angezeigt.

``` syntax
typedef struct _OBJECT_DIRECTORY_INFORMATION {
    UNICODE_STRING Name;
    UNICODE_STRING TypeName;
} OBJECT_DIRECTORY_INFORMATION, *POBJECT_DIRECTORY_INFORMATION;
```

Dieser Funktion ist keine Importbibliothek oder Headerdatei zugeordnet. Sie müssen sie mithilfe der [**Funktionen LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**NtOpenDirectoryObject**](ntopendirectoryobject.md)
</dt> </dl>

 

 
