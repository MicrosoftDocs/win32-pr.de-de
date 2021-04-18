---
description: Ruft Informationen zum angegebenen Verzeichnis Objekt ab.
ms.assetid: a2c67c4d-4753-4d47-a404-31d067a78bf4
title: Ntquerydirectoryobject-Funktion
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
ms.openlocfilehash: 99567d4784b121631089e723e1bd736e60a9cf54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364866"
---
# <a name="ntquerydirectoryobject-function"></a>Ntquerydirectoryobject-Funktion

\[Diese Funktion kann in Zukunft geändert oder nicht mehr verfügbar sein.\]

Ruft Informationen zum angegebenen Verzeichnis Objekt ab.

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

*Directoryhandle* \[ in\]
</dt> <dd>

Ein Handle für das Verzeichnis Objekt.

</dd> <dt>

*Puffer* \[ Out, optional\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der die Verzeichnisinformationen empfängt. Dieser Puffer empfängt mindestens eine **Objekt \_ Verzeichnis \_ Informations** Struktur, die letzte **null** ist, gefolgt von Zeichen folgen, die die Namen der Verzeichniseinträge enthalten. Weitere Informationen finden Sie in den Hinweisen.

</dd> <dt>

*Länge* \[ in\]
</dt> <dd>

Die Größe des vom Benutzer bereitgestellten Ausgabepuffers in Bytes.

</dd> <dt>

*Returnsingleentry* \[ in\]
</dt> <dd>

Gibt an, ob die Funktion nur einen einzelnen Eintrag zurückgeben soll.

</dd> <dt>

*Restarstcan* \[ in\]
</dt> <dd>

Gibt an, ob die Überprüfung neu gestartet oder die Enumeration mit den im *Kontext* Parameter übergebenen Informationen fortgesetzt werden soll.

</dd> <dt>

*Kontext* \[ in, out\]
</dt> <dd>

Der enumerationskontext.

</dd> <dt>

*Returnlength* \[ Out, optional\]
</dt> <dd>

Ein Zeiger auf eine Variable, die die Länge der im Ausgabepuffer zurückgegebenen Verzeichnisinformationen in Bytes empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Funktion gibt **Status \_ Erfolg** oder einen Fehlerstatus zurück.

## <a name="remarks"></a>Bemerkungen

Im folgenden finden Sie die Definition der **Objekt \_ Verzeichnis \_ Informations** Struktur.

``` syntax
typedef struct _OBJECT_DIRECTORY_INFORMATION {
    UNICODE_STRING Name;
    UNICODE_STRING TypeName;
} OBJECT_DIRECTORY_INFORMATION, *POBJECT_DIRECTORY_INFORMATION;
```

Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ntopendirectoryobject**](ntopendirectoryobject.md)
</dt> </dl>

 

 
