---
description: Wenn eine Anwendung eine Sitzung umleitet, behält TAPI Identifikationsinformationen zu dem Speicherort bei, an dem die Sitzung umgeleitet wurde, sowie den Speicherort, an den Sie umgeleitet wurde.
ms.assetid: 08484b38-7c97-4acc-921e-0f566b2d3415
title: Umleitungs Identifikation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8316b7d1566a24ead21f7b1fdf2d16b1c48a2b15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366268"
---
# <a name="redirect-identification"></a>Umleitungs Identifikation

Wenn eine Anwendung eine Sitzung [umleitet](redirect-ovr.md) , behält TAPI Identifikationsinformationen zu dem Speicherort bei, an dem die Sitzung umgeleitet wurde, sowie den Speicherort, an den Sie umgeleitet wurde.

"Umleiten" bezieht sich auf den Speicherort, der den Umleitungs Vorgang aufgerufen hat. "Umleitung" identifiziert das neue Ziel für die Sitzung.

Nicht alle Dienstanbieter unterstützen die Verwendung dieser Informationen.

* * TAPI 2. x: * *[**linegetcallinfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwredirectionidsize**, **dwredirectionidoffset**, **dwredirectionidnamesize**, **dwredirectionidnameoffset**, **dwredirectingidsize**, **dwredirectingidoffset**, **dwredirectingidnameoffset** Member von  [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)

* * TAPI 3. x: * *[**itcallinfo:: get \_ callinfostring**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfostring)aufgerufen mit dem **CIS \_ redirectionidname**, **CIS \_ redirectionidnumber**, **CIS \_ redirectingidname** oder **CIS \_ redirectingidnumber** -Member der [**CallInfo- \_ Zeichenfolge**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_string)

 

 
