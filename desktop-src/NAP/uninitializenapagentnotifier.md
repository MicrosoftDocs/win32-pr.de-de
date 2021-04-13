---
title: Uninitializenapagentnotifier-Funktion (naputil. h)
description: Abonniert den aufrufenden Prozess von NAPAgent-Status Änderungs Benachrichtigungen und Benachrichtigungen über Quarantäne Zustandsänderungen.
ms.assetid: b676ee33-caf6-48f0-acf8-5be1b23c62fe
keywords:
- Uninitializenapagentnotifier-Funktion NAP
topic_type:
- apiref
api_name:
- UninitializeNapAgentNotifier
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5d68b43fba64be82908d73803113f871b08c93c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391774"
---
# <a name="uninitializenapagentnotifier-function"></a>Uninitializenapagentnotifier-Funktion

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **uninitializenapagentnotifier** -Funktion hebt den aufrufenden Prozess von NAPAgent-Status Änderungs Benachrichtigungen und Benachrichtigungen über Quarantäne Zustandsänderungen auf. Diese Benachrichtigungen werden vom NAPAgent-Dienst bereitgestellt.

## <a name="syntax"></a>Syntax


```C++
NAPAPI VOID WINAPI UninitializeNapAgentNotifier(
  _In_ NapNotifyType type
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Typ* \[ in\]
</dt> <dd>

Ein [**napnotifytype**](/windows/win32/api/naptypes/ne-naptypes-napnotifytype) -Wert, der den Typ der Dienst Benachrichtigungen angibt, von denen abgemeldet werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion verfügt über keine Rückgabewerte.

## <a name="remarks"></a>Bemerkungen

Diese Funktion ist nicht threadsicher.

Jeder Prozess, der die NAPAgent-Dienst Benachrichtigungen des angegebenen *Typs* abonniert hat, muss **uninitializenapagentnotifier** anrufen, um Benachrichtigungen zu kündigen. Wenn ein Prozess mehr als einen Benachrichtigungstyp abonniert, muss er für jeden Benachrichtigungstyp einmal **uninitializenapagentnotifier** aufgerufen werden.

Diese Funktion führt nicht automatisch zu einem Fehler, wenn der Prozess zuvor nicht [**initializenapagentnotifier**](initializenapagentnotifier.md) für den Benachrichtigungstyp aufgerufen hat.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Naputil. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Initializenapagentnotifier**](initializenapagentnotifier.md)
</dt> </dl>

 

 





