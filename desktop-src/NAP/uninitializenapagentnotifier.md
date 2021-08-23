---
title: UninitializeNapAgentNotifier-Funktion (NapUtil.h)
description: Kündigen des Aufrufens von NapAgent-Statusänderungsbenachrichtigungen und Quarantänestatusänderungsbenachrichtigungen.
ms.assetid: b676ee33-caf6-48f0-acf8-5be1b23c62fe
keywords:
- NAP-Funktion "UninitializeNapAgentNotifier"
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
ms.openlocfilehash: b474ea95dcb2e3bd5c756cefa825463f3384e798492ccdcf794641a16fbfc450
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065260"
---
# <a name="uninitializenapagentnotifier-function"></a>UninitializeNapAgentNotifier-Funktion

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **UninitializeNapAgentNotifier-Funktion** kündigen das Abonnement des aufrufenden Prozesses von NapAgent-Statusänderungsbenachrichtigungen und Quarantänezustandsänderungsbenachrichtigungen. Diese Benachrichtigungen werden vom NapAgent-Dienst bereitgestellt.

## <a name="syntax"></a>Syntax


```C++
NAPAPI VOID WINAPI UninitializeNapAgentNotifier(
  _In_ NapNotifyType type
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Type (Typ)* \[ In\]
</dt> <dd>

Ein [**NapNotifyType-Wert,**](/windows/win32/api/naptypes/ne-naptypes-napnotifytype) der den Typ der Dienstbenachrichtigungen angibt, von denen das Abonnement gekündigt werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion verfügt über keine Rückgabewerte.

## <a name="remarks"></a>Hinweise

Diese Funktion ist nicht threadsicher.

Jeder Prozess, der NapAgent-Dienstbenachrichtigungen des angegebenen *Typs* abonniert hat, muss **UninitializeNapAgentNotifier** aufrufen, um das Abonnement von Benachrichtigungen zu kündigen. Wenn ein Prozess mehrere Benachrichtigungstypen abonniert hat, muss er für jeden Benachrichtigungstyp einmal **UninitializeNapAgentNotifier** aufrufen.

Diese Funktion schlägt im Hintergrund fehl, wenn der Prozess zuvor nicht [**InitializeNapAgentNotifier**](initializenapagentnotifier.md) für den Benachrichtigungstyp aufgerufen hat.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>NapUtil.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**InitializeNapAgentNotifier**](initializenapagentnotifier.md)
</dt> </dl>

 

 





