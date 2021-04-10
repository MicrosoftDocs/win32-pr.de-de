---
description: Wird für Benachrichtigungen registriert, wenn eine DLL zum ersten Mal geladen wird. Diese Benachrichtigung tritt auf, bevor die dynamische Verknüpfung stattfindet.
ms.assetid: c2757aa0-76fa-427a-a4f6-cb26e7f7d0d1
title: Ldrregisterdllnotification-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LdrRegisterDllNotification
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: 82ec05a24f4cccc89cece666b18cb63412a78259
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041345"
---
# <a name="ldrregisterdllnotification-function"></a>Ldrregisterdllnotification-Funktion

\[Diese Funktion kann ohne vorherige Ankündigung geändert oder aus Windows entfernt werden.\]

Wird für Benachrichtigungen registriert, wenn eine DLL zum ersten Mal geladen wird. Diese Benachrichtigung tritt auf, bevor die dynamische Verknüpfung stattfindet.

## <a name="syntax"></a>Syntax


```C++
NTSTATUS NTAPI LdrRegisterDllNotification(
  _In_     ULONG                          Flags,
  _In_     PLDR_DLL_NOTIFICATION_FUNCTION NotificationFunction,
  _In_opt_ PVOID                          Context,
  _Out_    PVOID                          *Cookie
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Flags* \[in\]
</dt> <dd>

Dieser Parameter muss NULL sein.

</dd> <dt>

*Notificationfunction* \[ in\]
</dt> <dd>

Ein Zeiger auf eine [*ldrdllnotification*](ldrdllnotification.md) -Rückruffunktion, die aufgerufen wird, wenn die dll geladen wird.

</dd> <dt>

*Kontext* \[ in, optional\]
</dt> <dd>

Ein Zeiger auf die Kontext Daten für die Rückruffunktion.

</dd> <dt>

*Cookie* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine Variable, um einen Bezeichner für die Rückruffunktion zu erhalten. Dieser Bezeichner wird verwendet, um die Registrierung der Benachrichtigungs Rückruffunktion aufzuheben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, wird der **Status \_ erfolgreich** zurückgegeben.

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

[*Ldrdllnotification*](ldrdllnotification.md)
</dt> <dt>

[**Ldrunregisterdllnotification**](ldrunregisterdllnotification.md)
</dt> </dl>

 

 
