---
description: Erläutert die Verwendung von Identitätswechsel Token in der Zugriffs Steuerung.
ms.assetid: 74fcb0e3-303a-4a5e-9eb6-2aad3a4944db
title: Identitätswechsel Token
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f468a4c7a9c6ff04a4481ffe7347e227a447db8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369777"
---
# <a name="impersonation-tokens"></a>Identitätswechsel Token

Ein Identitätswechsel Thread verfügt über zwei [*Zugriffs Token*](/windows/desktop/SecGloss/a-gly):

-   Ein [*Primäres Zugriffs Token*](/windows/desktop/SecGloss/p-gly) , das den [*Sicherheitskontext*](/windows/desktop/SecGloss/s-gly) des Servers beschreibt. Um ein Handle für dieses Token abzurufen, müssen Sie die [**OpenProcessToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocesstoken) -Funktion aufrufen.
-   Ein Identitätswechsel-Zugriffs Token, das den Sicherheitskontext des Clients beschreibt, dessen Identität angenommen wird. Um ein Handle für dieses Token abzurufen, wenden Sie die [**openthletotokenfunktion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthreadtoken) an.

Ein Server kann das Identitätswechsel [*Token*](/windows/desktop/SecGloss/i-gly) in den folgenden Funktionen verwenden:

-   In den Funktionen [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck), [**accesscheckbytype**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheckbytype)und [**accesscheckbytyperesultlist**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) , um zu bestimmen, ob eine [*Sicherheits Beschreibung*](/windows/desktop/SecGloss/s-gly) dem Client eine Gruppe von Zugriffsrechten zulässt.
-   In der [**Funktion "**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) ", um die Berechtigungen des Clients zu aktivieren oder zu deaktivieren.
-   In der [**privilegecheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-privilegecheck) -Funktion, um zu bestimmen, ob ein Berechtigungs Satz im Token des Clients aktiviert ist.
-   In Funktionen, die Einträge im Sicherheits Ereignisprotokoll generieren, z. b. [**objectopenauditalarm**](/windows/desktop/api/Winbase/nf-winbase-objectopenauditalarma) oder [**privilegedserviceauditalarm**](/windows/desktop/api/Winbase/nf-winbase-privilegedserviceauditalarma). Diese Funktionen verwenden ein Identitätswechsel Token, um Informationen über den Client für den Protokolleintrag zu erhalten.

 

 
