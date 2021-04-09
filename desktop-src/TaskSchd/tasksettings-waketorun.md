---
title: Tasksettings. waketor UN-Eigenschaft
description: Ruft bei der Skripterstellung einen booleschen Wert ab oder legt diesen fest, der angibt, dass die Taskplaner den Computer reaktivieren wird, wenn die Aufgabe ausgeführt wird.
ms.assetid: 51f83637-5bae-48c6-b750-b4467e651cec
keywords:
- Eigenschaft "waketor UN" Taskplaner
- Waketorun-Eigenschaft Taskplaner, tasksettings-Objekt
- Tasksettings-Objekt Taskplaner, waketorun-Eigenschaft
topic_type:
- apiref
api_name:
- TaskSettings.WakeToRun
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b563fd1ecd27914e84043b85c44f0cf5262e9fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740801"
---
# <a name="tasksettingswaketorun-property"></a>Tasksettings. waketor UN-Eigenschaft

Ruft bei der Skripterstellung einen booleschen Wert ab oder legt diesen fest, der angibt, dass die Taskplaner den Computer reaktivieren wird, wenn die Aufgabe ausgeführt wird.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
TaskSettings.WakeToRun As Boolean
```



## <a name="property-value"></a>Eigenschaftswert

Wenn true, gibt die-Eigenschaft an, dass der Computer vom Taskplaner aktiviert wird, wenn die Aufgabe ausgeführt wird.

## <a name="remarks"></a>Bemerkungen

Wenn der Taskplaner-Dienst den Computer zum Ausführen einer Aufgabe aktiviert, bleibt der Bildschirm möglicherweise deaktiviert, auch wenn sich der Computer nicht mehr im Standbymodus oder Ruhezustand befindet. Der Bildschirm wird eingeschaltet, wenn Windows Vista erkennt, dass ein Benutzer die Verwendung des Computers zurückgegeben hat.

Beim Lesen oder Schreiben von XML für eine Aufgabe wird diese Einstellung im [**waketorun-**](taskschedulerschema-waketorun-settingstype-element.md) Element des Taskplaner-Schemas angegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





