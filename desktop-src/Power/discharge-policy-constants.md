---
description: In der folgenden Liste werden die Entlade Richtlinien Konstanten beschrieben.
ms.assetid: a085709e-1c61-4ae2-832e-fda59479cef6
title: Entlade Richtlinien Konstanten (WinNT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 052d07a5fe538543b66ec8d48c940f63fe82a682
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349856"
---
# <a name="discharge-policy-constants"></a>Entlade Richtlinien Konstanten

In der folgenden Liste werden die Entlade Richtlinien Konstanten beschrieben.



| Konstante/Wert                                                                                                                                                                                                                                            | BESCHREIBUNG                                                                                                                                                                                     |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DISCHARGE_POLICY_CRITICAL"></span><span id="discharge_policy_critical"></span><dl> <dt>**Entladen \_ Richtlinien \_ kritisch**</dt> <dt>0</dt> </dl> | Welche der Einstellungen für die Akku Entlade Richtlinie [**( \_ Systemenergie \_ Pegel**](/windows/desktop/api/WinNT/ns-winnt-system_power_level) -Strukturen) wird verwendet, wenn die Akkukapazität unter den kritischen Schwellenwert fällt.<br/> |
| <span id="DISCHARGE_POLICY_LOW"></span><span id="discharge_policy_low"></span><dl> <dt>**Entladen \_ Richtlinie \_ niedrig**</dt> <dt>1</dt> </dl>                | Welche der Einstellungen für die Akku Entlade Richtlinie [**( \_ Systemenergie \_ Pegel**](/windows/desktop/api/WinNT/ns-winnt-system_power_level) -Strukturen) wird verwendet, wenn der Akku unter den unteren Schwellenwert entladen wird.<br/>      |
| <span id="NUM_DISCHARGE_POLICIES"></span><span id="num_discharge_policies"></span><dl> <dt>**NUM \_ Entlade \_ Richtlinien**</dt> <dt>4</dt> </dl>          | Anzahl der Einstellungen für die Akku Entlade Richtlinie ([**\_ \_ systemstromseenstrukturen**](/windows/desktop/api/WinNT/ns-winnt-system_power_level) ).<br/>                                                           |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                   |
| Header<br/>                   | <dl> <dt>WinNT. h (Include Windows. h)</dt> </dl> |



 

 




