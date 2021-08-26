---
description: Bricht die zuvor registrierte DLL-Ladebenachrichtigung ab, indem die LdrRegisterDllNotification-Funktion aufgerufen wird.
ms.assetid: 18c3a027-e3cb-4083-afdc-00f416a70d8c
title: LdrUnregisterDllNotification-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LdrUnregisterDllNotification
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: c70a732f1e1d1dd71db8d89489066547ee5238e89cf992fca9f2b04759b4c9ba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120001300"
---
# <a name="ldrunregisterdllnotification-function"></a>LdrUnregisterDllNotification-Funktion

\[Diese Funktion kann ohne weitere Ankündigung geändert oder aus Windows entfernt werden.\]

Bricht die zuvor registrierte DLL-Ladebenachrichtigung ab, indem die [**LdrRegisterDllNotification-Funktion**](ldrregisterdllnotification.md) aufgerufen wird.

## <a name="syntax"></a>Syntax


```C++
NTSTATUS NTAPI LdrUnregisterDllNotification(
  _In_ PVOID Cookie
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Cookie* \[ In\]
</dt> <dd>

Ein Zeiger auf den Rückrufbezeichner, der vom [**LdrRegisterDllNotification-Aufruf**](ldrregisterdllnotification.md) empfangen wurde, der für die Benachrichtigung registriert wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **NTSTATUS-** oder Fehlercode zurück.

Wenn die Funktion erfolgreich ist, wird **STATUS \_ SUCCESS** zurückgegeben.

Wenn die Rückruffunktion nicht gefunden wird, gibt die Funktion **STATUS DLL NOT FOUND \_ \_ \_ zurück.**

Die Formulare und die Bedeutung von **NTSTATUS-Fehlercodes** sind in der im WDK verfügbaren Headerdatei "Ntstatus.h" aufgeführt und in der WDK-Dokumentation beschrieben.

## <a name="remarks"></a>Hinweise

Dieser Funktion ist keine Headerdatei zugeordnet. Die zugeordnete Importbibliothek Ntdll.lib ist im WDK verfügbar. Sie können auch die [**Funktionen LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) verwenden, um dynamisch mit Ntdll.dll zu verknüpfen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Ntdll.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**LdrRegisterDllNotification**](ldrregisterdllnotification.md)
</dt> </dl>

 

 
