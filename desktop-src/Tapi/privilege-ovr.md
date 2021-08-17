---
description: Berechtigung bezieht sich darauf, ob eine Anwendung die Sitzung besitzt oder überwacht.
ms.assetid: 0c02a88a-370f-4eb9-ba64-07a382bd2e87
title: Berechtigung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4423b5eb1d50f5a7329726ab2e01040971daecca7e603247c49bcbc1d7c6d570
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060578"
---
# <a name="privilege"></a>Berechtigung

Berechtigung bezieht sich darauf, ob eine Anwendung die Sitzung besitzt oder überwacht. Wenn die Anwendung die Sitzung besitzt, kann sie eine Vielzahl von Sitzungsvorgängen ausführen. Wenn die Anwendung nur überwacht, erhält sie Zustandsmeldungen und kann auf Sitzungsinformationen zugreifen, aber jeder Versuch, die meisten Vorgänge durchzuführen, führt zu einem Fehler.

Während der Initialisierung teilt eine Anwendung TAPI mit, welche Berechtigungsstufe für welche Adressen erforderlich ist. TAPI bietet eingehende Sitzungen nur für Anwendungen an, die entweder für Besitzer- oder Besitzer- und Monitorberechtigungen registriert wurden.

Die Berechtigungen einer Anwendung für eine Sitzung, die sie erstellt, sind immer Besitzer.

**TAPI 2.x:** Siehe [**lineGetCallStatus**](/windows/win32/api/tapi/nf-tapi-linegetcallstatus), **dwCallPrivilege-Mitglied** von [**LINECALLSTATUS**](/windows/win32/api/tapi/ns-tapi-linecallstatus), [**lineSetCallPrivilege**](/windows/win32/api/tapi/nf-tapi-linesetcallprivilege).

**TAPI 3.x:** Weitere Informationen finden Sie unter [**ITCallInfo::get \_ Privilege**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_privilege), [**ITCallInfo::get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong), aufgerufen mit dem **CIL \_ NUMBEROFOWNERS-** oder **CIL \_ NUMBEROFMONITORS-Member** von [**CALLINFO \_ LONG.**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)

 

 
