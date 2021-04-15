---
description: Benutzer Benutzerinformationen sind Puffer, die von einem Ende einer Verbindung zu einem anderen übertragen werden können. Diese Informationen gelten speziell für den ISDN Q. 931-Standard. Informationen zur Bedeutung und Verwendung dieser Daten finden Sie in der Dokumentation Ihres Dienstanbietern.
ms.assetid: 7040ab51-184e-4ffc-9333-b82ae5a5a7f3
title: Benutzer Benutzerinformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d4539db192b9c24b5d71dfb60a2129e66b6658b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529705"
---
# <a name="user-user-information"></a>Benutzer Benutzerinformationen

Benutzer Benutzerinformationen sind Puffer, die von einem Ende einer Verbindung zu einem anderen übertragen werden können. Diese Informationen gelten speziell für den ISDN Q. 931-Standard. Informationen zur Bedeutung und Verwendung dieser Daten finden Sie in der Dokumentation Ihres Dienstanbieters.

Nicht alle Dienstanbieter unterstützen die Verwendung dieser Informationen.

* * TAPI 2. x: * *[**linegetcallinfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwcalldatasize** und **dwcalldataoffset** Member von [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo), [**linesenduseruserinfo**](/windows/win32/api/tapi/nf-tapi-linesenduseruserinfo)

* * TAPI 3. x: * *[**itcallinfo:: getcallinfobuffer**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-getcallinfobuffer), aufgerufen mit dem **CIB \_ useruserinfo** -Member des [**CallInfo- \_ Puffers**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_buffer), [**itcallinfo:: releaseuseruserinfo**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-releaseuseruserinfo)

 

 
