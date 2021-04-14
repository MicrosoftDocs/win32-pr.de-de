---
title: Tasksettings. aktivierte Eigenschaft
description: Ruft bei der Skripterstellung einen booleschen Wert ab, der angibt, dass der Task aktiviert ist, oder legt ihn fest. Der Task kann nur ausgeführt werden, wenn diese Einstellung auf "true" festgelegt ist.
ms.assetid: af8aa237-3402-4a82-b6ef-b713e1757d3a
keywords:
- Aktivierte Eigenschaften Taskplaner
- Aktivierte Eigenschaften Taskplaner, tasksettings-Objekt
- Tasksettings-Objekt Taskplaner, aktivierte Eigenschaft
topic_type:
- apiref
api_name:
- TaskSettings.Enabled
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6805d7b754ac2c3553d5fde91826ffa192b91d97
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392036"
---
# <a name="tasksettingsenabled-property"></a>Tasksettings. aktivierte Eigenschaft

Ruft bei der Skripterstellung einen booleschen Wert ab, der angibt, dass der Task aktiviert ist, oder legt ihn fest. Der Task kann nur ausgeführt werden, wenn diese Einstellung auf "true" festgelegt ist.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
TaskSettings.Enabled As Boolean
```



## <a name="property-value"></a>Eigenschaftswert

True gibt an, dass die Aufgabe aktiviert ist. Der Wert false gibt an, dass der Task nicht aktiviert ist.

## <a name="remarks"></a>Bemerkungen

Beim Lesen oder Schreiben von XML für eine Aufgabe wird diese Einstellung im [**aktivierten (settingstype)**](taskschedulerschema-enabled-settingstype-element.md) -Element des Taskplaner-Schemas angegeben.

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

 

 





