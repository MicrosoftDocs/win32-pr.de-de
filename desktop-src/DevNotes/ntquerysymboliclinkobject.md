---
description: Ruft das Ziel einer symbolischen Verknüpfung ab.
ms.assetid: 10a6676c-96f7-4758-8868-bbccd37b5019
title: NtQuerySymbolicLinkObject-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtQuerySymbolicLinkObject
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 805f3de5da380c4749e58dd7467f1f4ccb2471119ffed81b79695a98feb1b090
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118003630"
---
# <a name="ntquerysymboliclinkobject-function"></a>NtQuerySymbolicLinkObject-Funktion

\[Diese Funktion kann in Zukunft geändert oder nicht mehr verfügbar sein.\]

Ruft das Ziel einer symbolischen Verknüpfung ab.

## <a name="syntax"></a>Syntax


```C++
NTSTATUS WINAPI NtQuerySymbolicLinkObject(
  _In_      HANDLE          LinkHandle,
  _Inout_   PUNICODE_STRING LinkTarget,
  _Out_opt_ PULONG          ReturnedLength
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*LinkHandle* \[ In\]
</dt> <dd>

Ein Handle für das symbolische Verknüpfungsobjekt.

</dd> <dt>

*LinkTarget* \[ in, out\]
</dt> <dd>

Ein Zeiger auf eine initialisierte Unicode-Zeichenfolge, die das Ziel der symbolischen Verknüpfung empfängt. Die **Member MaximumLength** und **Buffer** müssen festgelegt werden, wenn der Aufruf fehlschlägt.

</dd> <dt>

*ReturnedLength* \[ out, optional\]
</dt> <dd>

Ein Zeiger auf eine Variable, die die Länge der im *LinkTarget-Parameter zurückgegebenen Unicode-Zeichenfolge empfängt.* Wenn die Funktion **STATUS BUFFER TOO SMALL \_ \_ \_ zurückgibt,** erhält diese Variable die erforderliche Puffergröße.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Funktion gibt **STATUS \_ SUCCESS oder** einen Fehlerstatus zurück.

## <a name="remarks"></a>Hinweise

Dieser Funktion ist keine Importbibliothek oder Headerdatei zugeordnet. Sie müssen sie mithilfe der [**Funktionen LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**NtOpenSymbolicLinkObject**](ntopensymboliclinkobject.md)
</dt> </dl>

 

 
