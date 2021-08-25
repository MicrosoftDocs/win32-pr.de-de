---
description: Erläutert die Verwendung von Identitätswechseltoken in der Zugriffssteuerung.
ms.assetid: 74fcb0e3-303a-4a5e-9eb6-2aad3a4944db
title: Identitätswechseltoken
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67acf48a1f274703850fc8bfc2167014708124c46743f416591510b6c9ab559b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119908140"
---
# <a name="impersonation-tokens"></a>Identitätswechseltoken

Ein Identitätswechselthread verfügt über zwei [*Zugriffstoken:*](/windows/desktop/SecGloss/a-gly)

-   Ein [*primäres Zugriffstoken,*](/windows/desktop/SecGloss/p-gly) das den [*Sicherheitskontext des*](/windows/desktop/SecGloss/s-gly) Servers beschreibt. Um ein Handle für dieses Token abzurufen, rufen Sie die [**OpenProcessToken-Funktion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocesstoken) auf.
-   Ein Identitätswechsel-Zugriffstoken, das den Sicherheitskontext des Clients beschreibt, für den die Identität angenommen wird. Um ein Handle für dieses Token abzurufen, rufen Sie die [**OpenThreadToken-Funktion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthreadtoken) auf.

Ein Server kann das [*Identitätswechseltoken*](/windows/desktop/SecGloss/i-gly) in den folgenden Funktionen verwenden:

-   In den [**Funktionen AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck), [**AccessCheckByType**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheckbytype)und [**AccessCheckByTypeResultList**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) bestimmen Sie, ob ein [*Sicherheitsdeskriptor*](/windows/desktop/SecGloss/s-gly) dem Client einen Satz von Zugriffsrechten zulässt.
-   Aktivieren oder deaktivieren Sie in der [**Funktion AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) die Berechtigungen des Clients.
-   In der [**PrivilegeCheck-Funktion,**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-privilegecheck) um zu bestimmen, ob ein Satz von Berechtigungen im Token des Clients aktiviert ist.
-   In Funktionen, die Einträge im Sicherheitsereignisprotokoll generieren, z. B. [**ObjectOpenAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-objectopenauditalarma) oder [**PrivilegedServiceAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-privilegedserviceauditalarma). Diese Funktionen verwenden ein Identitätswechseltoken, um Informationen zum Client für den Protokolleintrag abzurufen.

 

 
