---
description: Jeder Typ von sicherungsfähigem Objekt verfügt über einen Satz von Zugriffsrechten, die vorgängen entsprechen, die für diesen Objekttyp spezifisch sind.
ms.assetid: f43bccce-0f8c-4732-b678-5fd3218a9f84
title: Standardzugriffsrechte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56067a4ed31f9506aee0b326e82a9bd5b4b49b02d12e6d401cc04f8262b19da0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119907110"
---
# <a name="standard-access-rights"></a>Standardzugriffsrechte

Jeder Typ von sicherungsfähigem Objekt verfügt über einen Satz von Zugriffsrechten, die vorgängen entsprechen, die für diesen Objekttyp spezifisch sind. Zusätzlich zu diesen objektspezifischen Zugriffsrechten gibt es eine Reihe von Standardzugriffsrechten, die Vorgängen entsprechen, die den meisten Typen von sicherungsbaren Objekten gemeinsam sind.

Das [Format der Zugriffsmaske](access-mask-format.md) enthält eine Reihe von Bits für die Standardzugriffsrechte. Die folgenden Windows Konstanten für Standardzugriffsrechte werden in Winnt.h definiert.



| Konstante      | Bedeutung                                                                                                                                                                                                                                                                                                                                      |
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Delete        | Das Recht, das Objekt zu löschen.                                                                                                                                                                                                                                                                                                              |
| \_READ-STEUERELEMENT | Das Recht, die Informationen im [*Sicherheitsdeskriptor*](/windows/desktop/SecGloss/s-gly)des Objekts zu lesen, ohne die Informationen in der Systemzugriffssteuerungsliste (SACL). [](/windows/desktop/SecGloss/s-gly) |
| SYNCHRONIZE   | Das Recht, das Objekt für die Synchronisierung zu verwenden. Dadurch kann ein Thread warten, bis sich das Objekt im signalisierten Zustand befindet. Einige Objekttypen unterstützen dieses Zugriffsrecht nicht.                                                                                                                                                                |
| \_SCHREIB-DAC    | Das Recht, die DACL [*(Discretionary Access Control List)*](/windows/desktop/SecGloss/d-gly) im Sicherheitsdeskriptor des Objekts zu ändern.                                                                                                                    |
| WRITE \_ OWNER  | Das Recht, in der Sicherheitsbeschreibung des Objekts den Besitzer zu ändern.                                                                                                                                                                                                                                                                           |



 

Winnt.h definiert auch die folgenden Kombinationen der Standardkonst constants für Zugriffsrechte.



| Konstante                   | Bedeutung                                                                           |
|----------------------------|-----------------------------------------------------------------------------------|
| STANDARD \_ RIGHTS \_ ALL      | Kombiniert DELETE-, READ \_ CONTROL-, WRITE \_ DAC-, WRITE \_ OWNER- und SYNCHRONIZE-Zugriff. |
| STANDARD \_ RIGHTS \_ EXECUTE  | Derzeit als read \_ control definiert.                                         |
| STANDARD \_ RIGHTS \_ READ     | Derzeit als read \_ control definiert.                                         |
| STANDARDRECHTE \_ \_ ERFORDERLICH | Kombiniert DELETE-, READ \_ CONTROL-, WRITE \_ DAC- und WRITE \_ OWNER-Zugriff.              |
| STANDARD \_ RIGHTS \_ WRITE    | Derzeit als read \_ control definiert.                                         |



 

 

 
