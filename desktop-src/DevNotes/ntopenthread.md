---
description: Öffnet ein Handle für ein Threadobjekt mit dem angegebenen Zugriff.
ms.assetid: 85148f27-cfb4-4a33-8bcc-e48d2c2e3c51
title: NtOpenThread-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtOpenThread
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: e5f459b12d90a12b7c75aabd44d25f6fcf352aff8914e6d991471acaee400260
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079690"
---
# <a name="ntopenthread-function"></a>NtOpenThread-Funktion

\[Diese Funktion kann ohne weitere Ankündigung geändert oder Windows entfernt werden. Verwenden Sie [**stattdessen die OpenThread-Funktion.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthread)\]

Öffnet ein Handle für ein Threadobjekt mit dem angegebenen Zugriff.

## <a name="syntax"></a>Syntax


```C++
NTSTATUS NtOpenThread(
  _Out_ PHANDLE            ThreadHandle,
  _In_  ACCESS_MASK        DesiredAccess,
  _In_  POBJECT_ATTRIBUTES ObjectAttributes,
  _In_  PCLIENT_ID         ClientId
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ThreadHandle* \[ out\]
</dt> <dd>

Ein Zeiger auf eine Variable, die das Threadobjekthand handle empfängt.

</dd> <dt>

*DesiredAccess* \[ In\]
</dt> <dd>

Ein [**ACCESS \_ MASK-Datentyp,**](../secauthz/access-mask-format.md) der die gewünschten Zugriffstypen für das Threadobjekt bietet.

</dd> <dt>

*ObjectAttributes* \[ In\]
</dt> <dd>

Ein Zeiger auf eine [OBJECT \_ ATTRIBUTES-Struktur.](https://msdn.microsoft.com/library/aa491657.aspx) Der **ObjectName-Member** dieser Struktur muss NULL sein.

**Windows Server 2003 und Windows XP:** Der **ObjectName-Member** dieser Struktur kann auf einen Objektnamen verweisen. Wenn **ObjectName nicht** NULL ist, muss der *ClientId-Parameter* NULL sein.

</dd> <dt>

*ClientId* \[ In\]
</dt> <dd>

Ein Zeiger auf eine **\_ CLIENT-ID-Struktur,** die den Thread identifiziert, dessen Thread geöffnet werden soll.

**Windows Server 2003 und Windows XP:** Ein Zeiger auf eine **\_ CLIENT-ID-Struktur,** die den Thread identifiziert, dessen Thread geöffnet werden soll. Dieser Parameter kann NULL sein. Wenn dieser Parameter nicht NULL ist, muss der **ObjectName-Member** der Struktur, auf die der *ObjectAttributes-Parameter* verweist, NULL sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **NTSTATUS- oder** Fehlercode zurück.

Die Formulare und die Bedeutung von **NTSTATUS-Fehlercodes** sind in der im WDK verfügbaren Ntstatus.h-Headerdatei aufgeführt und in der WDK-Dokumentation beschrieben.

## <a name="remarks"></a>Hinweise

Dieser Funktion ist keine Headerdatei zugeordnet. Die zugeordnete Importbibliothek Ntdll.lib ist im WDK verfügbar. Sie können auch die [**Funktionen LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) verwenden, um eine dynamische Verknüpfung mit Ntdll.dll.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 
