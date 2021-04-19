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
# <a name="impersonation-tokens"></a><span data-ttu-id="74476-103">Identitätswechsel Token</span><span class="sxs-lookup"><span data-stu-id="74476-103">Impersonation Tokens</span></span>

<span data-ttu-id="74476-104">Ein Identitätswechsel Thread verfügt über zwei [*Zugriffs Token*](/windows/desktop/SecGloss/a-gly):</span><span class="sxs-lookup"><span data-stu-id="74476-104">An impersonating thread has two [*access tokens*](/windows/desktop/SecGloss/a-gly):</span></span>

-   <span data-ttu-id="74476-105">Ein [*Primäres Zugriffs Token*](/windows/desktop/SecGloss/p-gly) , das den [*Sicherheitskontext*](/windows/desktop/SecGloss/s-gly) des Servers beschreibt.</span><span class="sxs-lookup"><span data-stu-id="74476-105">A [*primary access token*](/windows/desktop/SecGloss/p-gly) that describes the [*security context*](/windows/desktop/SecGloss/s-gly) of the server.</span></span> <span data-ttu-id="74476-106">Um ein Handle für dieses Token abzurufen, müssen Sie die [**OpenProcessToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocesstoken) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="74476-106">To get a handle to this token, call the [**OpenProcessToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocesstoken) function.</span></span>
-   <span data-ttu-id="74476-107">Ein Identitätswechsel-Zugriffs Token, das den Sicherheitskontext des Clients beschreibt, dessen Identität angenommen wird.</span><span class="sxs-lookup"><span data-stu-id="74476-107">An impersonation access token that describes the security context of the client being impersonated.</span></span> <span data-ttu-id="74476-108">Um ein Handle für dieses Token abzurufen, wenden Sie die [**openthletotokenfunktion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthreadtoken) an.</span><span class="sxs-lookup"><span data-stu-id="74476-108">To get a handle to this token, call the [**OpenThreadToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthreadtoken) function.</span></span>

<span data-ttu-id="74476-109">Ein Server kann das Identitätswechsel [*Token*](/windows/desktop/SecGloss/i-gly) in den folgenden Funktionen verwenden:</span><span class="sxs-lookup"><span data-stu-id="74476-109">A server can use the [*impersonation token*](/windows/desktop/SecGloss/i-gly) in the following functions:</span></span>

-   <span data-ttu-id="74476-110">In den Funktionen [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck), [**accesscheckbytype**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheckbytype)und [**accesscheckbytyperesultlist**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) , um zu bestimmen, ob eine [*Sicherheits Beschreibung*](/windows/desktop/SecGloss/s-gly) dem Client eine Gruppe von Zugriffsrechten zulässt.</span><span class="sxs-lookup"><span data-stu-id="74476-110">In the [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck), [**AccessCheckByType**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheckbytype), and [**AccessCheckByTypeResultList**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) functions to determine whether a [*security descriptor*](/windows/desktop/SecGloss/s-gly) allows the client a set of access rights.</span></span>
-   <span data-ttu-id="74476-111">In der [**Funktion "**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) ", um die Berechtigungen des Clients zu aktivieren oder zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="74476-111">In the [**AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) function to enable or disable the client's privileges.</span></span>
-   <span data-ttu-id="74476-112">In der [**privilegecheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-privilegecheck) -Funktion, um zu bestimmen, ob ein Berechtigungs Satz im Token des Clients aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="74476-112">In the [**PrivilegeCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-privilegecheck) function to determine whether a set of privileges are enabled in the client's token.</span></span>
-   <span data-ttu-id="74476-113">In Funktionen, die Einträge im Sicherheits Ereignisprotokoll generieren, z. b. [**objectopenauditalarm**](/windows/desktop/api/Winbase/nf-winbase-objectopenauditalarma) oder [**privilegedserviceauditalarm**](/windows/desktop/api/Winbase/nf-winbase-privilegedserviceauditalarma).</span><span class="sxs-lookup"><span data-stu-id="74476-113">In functions that generate entries in the security event log, such as [**ObjectOpenAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-objectopenauditalarma) or [**PrivilegedServiceAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-privilegedserviceauditalarma).</span></span> <span data-ttu-id="74476-114">Diese Funktionen verwenden ein Identitätswechsel Token, um Informationen über den Client für den Protokolleintrag zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="74476-114">These functions use an impersonation token to get information about the client for the log entry.</span></span>

 

 
