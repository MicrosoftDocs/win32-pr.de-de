---
title: IdleSettings.RestartOnIdle-Eigenschaft
description: Ruft für die Skripterstellung einen booleschen Wert ab, der angibt, ob der Task neu gestartet wird, wenn der Computer mehr als einmal in eine Leerlaufbedingung übergeht, oder legt diesen fest.
ms.assetid: c77b6f5f-659c-4aa0-a5f7-39c01e5ca65e
keywords:
- RestartOnIdle-Eigenschaft Taskplaner
- RestartOnIdle-Eigenschaft Taskplaner , IdleSettings-Objekt
- IdleSettings-Objekt Taskplaner , RestartOnIdle-Eigenschaft
topic_type:
- apiref
api_name:
- IdleSettings.RestartOnIdle
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa405ce4090a080106ec030acbe0ca7211b1c6f94e5874729226ce6adfafa652
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117760077"
---
# <a name="idlesettingsrestartonidle-property"></a>IdleSettings.RestartOnIdle-Eigenschaft

Ruft für die Skripterstellung einen booleschen Wert ab, der angibt, ob der Task neu gestartet wird, wenn der Computer mehr als einmal in eine Leerlaufbedingung übergeht, oder legt diesen fest.

## <a name="syntax"></a>Syntax


```VB
IdleSettings.RestartOnIdle As Boolean
```



## <a name="property-value"></a>Eigenschaftswert

Ein boolescher Wert, der angibt, ob der Task neu gestartet werden muss, wenn der Computer mehr als einmal in eine Leerlaufbedingung eintritt. Die Standardeinstellung lautet „false“.

## <a name="remarks"></a>Hinweise

Diese Eigenschaft wird nur verwendet, wenn die [**IdleSettings.StopOnIdleEnd-Eigenschaft**](idlesettings-stoponidleend.md) auf True festgelegt ist.

Beim Lesen oder Schreiben von XML für eine Aufgabe wird diese Einstellung im [**RestartOnIdle-Element**](taskschedulerschema-restartonidle-idlesettingstype-element.md) des Taskplaner Schemas angegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> <dt>

[**IdleSettings**](idlesettings.md)
</dt> </dl>

 

 





