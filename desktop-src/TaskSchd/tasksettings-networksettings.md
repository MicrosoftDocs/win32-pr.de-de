---
title: Tasksettings. networksettings (Eigenschaft)
description: Ruft bei der Skripterstellung das Netzwerk Einstellungs Objekt ab, das einen Netzwerk Profil Bezeichner und-Namen enthält, oder legt dieses fest.
ms.assetid: 3d368f6c-4534-4e71-8fbd-84361730a3e2
keywords:
- Die networksettings-Eigenschaft Taskplaner
- Networksettings-Eigenschaft Taskplaner, tasksettings-Objekt
- Tasksettings-Objekt Taskplaner, networksettings-Eigenschaft
topic_type:
- apiref
api_name:
- TaskSettings.NetworkSettings
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68c81350c8516a47eb7eb160541b86945c86e29b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740425"
---
# <a name="tasksettingsnetworksettings-property"></a>Tasksettings. networksettings (Eigenschaft)

Ruft bei der Skripterstellung das Netzwerk Einstellungs Objekt ab, das einen Netzwerk Profil Bezeichner und-Namen enthält, oder legt dieses fest. Wenn die [**runonlyifnetworkavailable**](tasksettings-runonlyifnetworkavailable.md) -Eigenschaft von [**tasksettings**](tasksettings.md) den Wert **true** hat und in der **networksettings** -Eigenschaft eine Netzwerk-propfile angegeben ist, wird die Aufgabe nur ausgeführt, wenn das angegebene Netzwerk Profil verfügbar ist.

## <a name="syntax"></a>Syntax


```VB
TaskSettings.NetworkSettings As NetworkSettings
```



## <a name="property-value"></a>Eigenschaftswert

Ein [**networksettings**](networksettings.md) -Objekt, das einen Netzwerk Profil Bezeichner und-Namen enthält.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Tasksettings**](tasksettings.md)
</dt> <dt>

[**NetworkSettings**](networksettings.md)
</dt> </dl>

 

 





