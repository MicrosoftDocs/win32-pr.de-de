---
description: Öffnet einen vorhandenen symbolischen Link.
ms.assetid: 37684707-4f65-4904-8bfc-d0679ebbd924
title: Ntopensymboliclinkobject-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtOpenSymbolicLinkObject
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 3cd5091fe19631079ff3c51d9d6ba7777970a854
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357715"
---
# <a name="ntopensymboliclinkobject-function"></a>Ntopensymboliclinkobject-Funktion

\[Diese Funktion kann in Zukunft geändert oder nicht mehr verfügbar sein.\]

Öffnet einen vorhandenen symbolischen Link.

## <a name="syntax"></a>Syntax


```C++
NTSTATUS WINAPI NtOpenSymbolicLinkObject(
  _Out_ PHANDLE            LinkHandle,
  _In_  ACCESS_MASK        DesiredAccess,
  _In_  POBJECT_ATTRIBUTES ObjectAttributes
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Linkhandle* \[ vorgenommen\]
</dt> <dd>

Ein Handle für das neu geöffnete symbolische Verknüpfungs Objekt.

</dd> <dt>

*DesiredAccess* \[ in\]
</dt> <dd>

Eine [**Zugriffs \_ Maske**](../secauthz/access-mask.md) , die den angeforderten Zugriff auf das Verzeichnis Objekt angibt. Es ist typisch, den generischen Lesevorgang zu verwenden, \_ damit das Handle an die [**ntquerydirectoryobject**](ntquerydirectoryobject.md) -Funktion weitergeleitet werden kann.

</dd> <dt>

*Objectattributes* \[ in\]
</dt> <dd>

Die Attribute für das Verzeichnis Objekt. Um die **Objekt \_ Attribut** Struktur zu initialisieren, verwenden Sie das **initializeobjectattributes** -Makro. Wenn der Aufrufer nicht in einem System Thread Kontext ausgeführt wird, muss er das **obj \_ - \_ KERNELHANDLE-** Flag angeben, wenn die Struktur initialisiert wird. Weitere Informationen finden Sie in der Dokumentation für diese Elemente in der Dokumentation für das WDK.

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

[**Ntquerydirectoryobject**](ntquerydirectoryobject.md)
</dt> </dl>

 

 
