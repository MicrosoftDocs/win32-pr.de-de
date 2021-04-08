---
description: Die aufruferidentifikation stellt beim Empfang einer eingehenden Sitzung Informationen über die aufrufende Partei bereit. Eine Anwendung verwendet diese Daten in der Regel als Teil einer Statusmeldung für einen Benutzer.
ms.assetid: aaaa5eae-e917-44a7-b9c5-97ca2d9a4eec
title: Aufruferkennung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93513e3d94fac9c550b23651b3987bc794905beb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866592"
---
# <a name="caller-identification"></a>Aufruferkennung

Die aufruferidentifikation stellt beim Empfang einer eingehenden Sitzung Informationen über die aufrufende Partei bereit. Eine Anwendung verwendet diese Daten in der Regel als Teil einer Statusmeldung für einen Benutzer.

Diese Informationen sind nicht immer sofort verfügbar. Eine Anwendung, die diese Informationen verwenden und überprüft hat, ob der Dienstanbieter Sie unterstützt, sollte mehrmals überprüft werden, bevor davon ausgegangen wird, dass die Informationen nicht verfügbar sind.

Nicht alle Dienstanbieter unterstützen die Verwendung dieser Informationen.

**TAPI 2. x:** Weitere Informationen finden Sie unter [**linegetcallinfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwcalleridflags**, **dwcalleridsize**, **dwcalleridoffset**, **dwcalleridnamesize**, **dwcalleridnameoffset** und **dwcalleridadresssstype** Members von *lpcallinfo*).

**TAPI 3. x:** Siehe [**itcallinfo:: get \_ callinfolong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (**cil \_ calleridadresssstype** Member von [**CallInfo \_ Long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)), [**itcallinfo:: get \_ callinfostring**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfostring) (**CIS \_ CallerIDName** und **CIS \_ CallerIDName** Member von [**CallInfo \_ String**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_string)).

 

 
