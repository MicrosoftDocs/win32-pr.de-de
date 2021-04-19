---
description: Die Berechtigung bezieht sich darauf, ob eine Anwendung die Sitzung besitzt oder überwacht.
ms.assetid: 0c02a88a-370f-4eb9-ba64-07a382bd2e87
title: Berechtigung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc2f773edb05afc029a8f9fb6b014cd8a737eef0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352457"
---
# <a name="privilege"></a>Berechtigung

Die Berechtigung bezieht sich darauf, ob eine Anwendung die Sitzung besitzt oder überwacht. Wenn die Anwendung die Sitzung besitzt, kann eine Vielzahl von Sitzungs Vorgängen durchgeführt werden. Wenn die Anwendung nur überwacht wird, empfängt Sie Zustands Meldungen und kann auf Sitzungsinformationen zugreifen, aber jeder Versuch, die meisten Vorgänge auszuführen, führt zu einem Fehler.

Während der Initialisierung teilt eine Anwendung TAPI mit, welche Berechtigungsebene für welche Adressen erforderlich ist. TAPI bietet eingehende Sitzungen nur für Anwendungen, die entweder für Besitzer-oder Besitzer-und Überwachungs Berechtigungen registriert sind.

Die Berechtigung einer Anwendung für eine Sitzung, die erstellt wird, ist immer Owner.

**TAPI 2. x:** Weitere Informationen finden Sie unter [**linegetcallstatus**](/windows/win32/api/tapi/nf-tapi-linegetcallstatus), **dwcallprivilege** -Member von [**linecallstatus**](/windows/win32/api/tapi/ns-tapi-linecallstatus), [**linesetcallprivilege**](/windows/win32/api/tapi/nf-tapi-linesetcallprivilege).

**TAPI 3. x:** Weitere Informationen finden [**Sie unter itcallinfo:: get- \_ Berechtigung**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_privilege), [**itcallinfo:: get \_ callinfolong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong), aufgerufen mit dem **cil- \_ numofowners** oder **cil- \_ numofmonitors** -Member von [**CallInfo \_ Long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long).

 

 
