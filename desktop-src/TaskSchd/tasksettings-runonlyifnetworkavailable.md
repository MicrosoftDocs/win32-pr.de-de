---
title: Tasksettings. runonlyifnetworkavailable (Eigenschaft)
description: Ruft bei der Skripterstellung einen booleschen Wert ab, der angibt, dass die Taskplaner den Task nur dann ausführen, wenn ein Netzwerk verfügbar ist, oder legt diesen fest.
ms.assetid: 1a2b085f-0572-47d3-ac1f-0032c8427af0
keywords:
- Runonlyifnetworkavailable-Eigenschaft Taskplaner
- Runonlyifnetworkavailable-Eigenschaft Taskplaner, tasksettings-Objekt
- Tasksettings-Objekt Taskplaner, runonlyifnetworkavailable-Eigenschaft
topic_type:
- apiref
api_name:
- TaskSettings.RunOnlyIfNetworkAvailable
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8225d836e5bc87abd5ce9b6c311b4af527561d41
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859138"
---
# <a name="tasksettingsrunonlyifnetworkavailable-property"></a>Tasksettings. runonlyifnetworkavailable (Eigenschaft)

Ruft bei der Skripterstellung einen booleschen Wert ab, der angibt, dass die Taskplaner den Task nur dann ausführen, wenn ein Netzwerk verfügbar ist, oder legt diesen fest.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
TaskSettings.RunOnlyIfNetworkAvailable As Boolean
```



## <a name="property-value"></a>Eigenschaftswert

Wenn true, gibt die-Eigenschaft an, dass die Taskplaner die Aufgabe nur dann ausführen soll, wenn ein Netzwerk verfügbar ist. Die Standardeinstellung lautet „false“.

## <a name="remarks"></a>Bemerkungen

Beim Lesen oder Schreiben von XML für eine Aufgabe wird diese Einstellung im [**runonlyifnetworkavailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) -Element des Taskplaner-Schemas angegeben.

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

 

 





