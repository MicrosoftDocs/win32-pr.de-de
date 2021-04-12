---
description: Bricht die dll-Lade Benachrichtigung ab, die zuvor durch Aufrufen der ldrregisterdllnotification-Funktion registriert wurde.
ms.assetid: 18c3a027-e3cb-4083-afdc-00f416a70d8c
title: Ldrunregisterdllnotification-Funktion
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
ms.openlocfilehash: 1fee03b4a06d274b495070eb40833b270a795158
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104392922"
---
# <a name="ldrunregisterdllnotification-function"></a>Ldrunregisterdllnotification-Funktion

\[Diese Funktion kann ohne vorherige Ankündigung geändert oder aus Windows entfernt werden.\]

Bricht die dll-Lade Benachrichtigung ab, die zuvor durch Aufrufen der [**ldrregisterdllnotification**](ldrregisterdllnotification.md) -Funktion registriert wurde.

## <a name="syntax"></a>Syntax


```C++
NTSTATUS NTAPI LdrUnregisterDllNotification(
  _In_ PVOID Cookie
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Cookie* \[ in\]
</dt> <dd>

Ein Zeiger auf den Rückruf Bezeichner, der vom [**ldrregisterdllnotification**](ldrregisterdllnotification.md) -Befehl empfangen wurde, der für die Benachrichtigung registriert ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den **NTSTATUS** -oder-Fehlercode zurück.

Wenn die Funktion erfolgreich ausgeführt wird, wird der **Status \_ erfolgreich** zurückgegeben.

Wenn die Rückruffunktion nicht gefunden wird, gibt die Funktion die **Status- \_ dll \_ nicht \_ gefunden** zurück.

Die Formulare und die Bedeutung von **NTSTATUS** -Fehlercodes sind in der Header Datei "NTSTATUS. h" aufgeführt, die im WDK verfügbar ist, und werden in der WDK-Dokumentation beschrieben.

## <a name="remarks"></a>Bemerkungen

Dieser Funktion ist keine Header Datei zugeordnet. Die zugehörige Import Bibliothek ntdll. lib ist im WDK verfügbar. Sie können auch die [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit Ntdll.dll zu verknüpfen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Ntdll.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ldrregisterdllnotification**](ldrregisterdllnotification.md)
</dt> </dl>

 

 
