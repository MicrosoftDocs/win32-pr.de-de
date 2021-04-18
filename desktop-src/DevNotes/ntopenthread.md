---
description: Öffnet ein Handle für ein Thread Objekt mit dem angegebenen Zugriff.
ms.assetid: 85148f27-cfb4-4a33-8bcc-e48d2c2e3c51
title: Ntopenthread-Funktion
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
ms.openlocfilehash: 8c1b64d2e024f3905d171ab5ca90e59df929ffc0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372059"
---
# <a name="ntopenthread-function"></a>Ntopenthread-Funktion

\[Diese Funktion kann ohne vorherige Ankündigung geändert oder aus Windows entfernt werden. Verwenden Sie stattdessen die [**openthread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthread) -Funktion.\]

Öffnet ein Handle für ein Thread Objekt mit dem angegebenen Zugriff.

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

*Threadhandle* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine Variable, die das Thread Objekt Handle empfängt.

</dd> <dt>

*DesiredAccess* \[ in\]
</dt> <dd>

Ein [**Zugriffs \_ Masken**](../secauthz/access-mask-format.md) Datentyp, der die gewünschten Zugriffs Typen für das Thread Objekt bereitstellt.

</dd> <dt>

*Objectattributes* \[ in\]
</dt> <dd>

Ein Zeiger auf eine [Objekt \_ Attribut](https://msdn.microsoft.com/library/aa491657.aspx) Struktur. Der **objectName** -Member dieser Struktur muss NULL sein.

**Windows Server 2003 und Windows XP:** Der **objectName** -Member dieser Struktur kann auf einen Objektnamen zeigen. Wenn **objectName** nicht NULL ist, muss der *ClientID-* Parameter NULL sein.

</dd> <dt>

*ClientID* \[ in\]
</dt> <dd>

Ein Zeiger auf eine **Client- \_ ID** -Struktur, die den Thread identifiziert, dessen Thread geöffnet werden soll.

**Windows Server 2003 und Windows XP:** Ein Zeiger auf eine **Client- \_ ID** -Struktur, die den Thread identifiziert, dessen Thread geöffnet werden soll. Dieser Parameter kann NULL sein. Wenn dieser Parameter nicht NULL ist, muss der **objectName** -Member der Struktur, auf die durch den *objectattributes* -Parameter verwiesen wird, NULL sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den **NTSTATUS** -oder-Fehlercode zurück.

Die Formulare und die Bedeutung von **NTSTATUS** -Fehlercodes sind in der Header Datei "NTSTATUS. h" aufgeführt, die im WDK verfügbar ist, und werden in der WDK-Dokumentation beschrieben.

## <a name="remarks"></a>Bemerkungen

Dieser Funktion ist keine Header Datei zugeordnet. Die zugehörige Import Bibliothek ntdll. lib ist im WDK verfügbar. Sie können auch die [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit Ntdll.dll zu verknüpfen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 
