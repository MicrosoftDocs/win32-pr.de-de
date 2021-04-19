---
description: Ruft das Ziel einer symbolischen Verknüpfung ab.
ms.assetid: 10a6676c-96f7-4758-8868-bbccd37b5019
title: Ntquerysymboliclinkobject-Funktion
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
ms.openlocfilehash: c79b7b40e0d3c8622ee263d96836f738d76942ae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354076"
---
# <a name="ntquerysymboliclinkobject-function"></a>Ntquerysymboliclinkobject-Funktion

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

*Linkhandle* \[ in\]
</dt> <dd>

Ein Handle für das symbolische Verknüpfungs Objekt.

</dd> <dt>

*LinkTarget* \[ in, out\]
</dt> <dd>

Ein Zeiger auf eine initialisierte Unicode-Zeichenfolge, die das Ziel der symbolischen Verknüpfung empfängt. Die **MaximumLength** -und **buffer** -Elemente müssen festgelegt werden, wenn der-Befehl fehlschlägt.

</dd> <dt>

*Rückkehrnedlength* \[ Out, optional\]
</dt> <dd>

Ein Zeiger auf eine Variable, die die Länge der Unicode-Zeichenfolge empfängt, die im *LinkTarget* -Parameter zurückgegeben wird. Wenn die Funktion den **Status \_ Puffer \_ zu \_ klein** zurückgibt, erhält diese Variable die erforderliche Puffergröße.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Funktion gibt **Status \_ Erfolg** oder einen Fehlerstatus zurück.

## <a name="remarks"></a>Bemerkungen

Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ntopensymboliclinkobject**](ntopensymboliclinkobject.md)
</dt> </dl>

 

 
