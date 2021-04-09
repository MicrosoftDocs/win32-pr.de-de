---
description: Wenn terminaldienstedienste aktiviert sind, muss die Gina Winlogon-Unterstützungsfunktionen anrufen, um das Setup für die einzelnen Benutzer abzuschließen, die Anmelde Informationen einer Terminaldienste-Client Sitzung abzufragen und die Verbindung mit einer Terminaldienste-Netzwerksitzung zu trennen. Beachten Sie, dass Gina-DLLs in Windows Vista ignoriert werden.
ms.assetid: 70b55b99-b350-4638-84ba-e5580d9d992f
title: Terminal Dienste-Gina-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19452fb73f00ef4ace0dd85083578334b6fb1038
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862399"
---
# <a name="terminal-services-gina-functions"></a><span data-ttu-id="16e09-103">Terminal Dienste-Gina-Funktionen</span><span class="sxs-lookup"><span data-stu-id="16e09-103">Terminal Services GINA Functions</span></span>

<span data-ttu-id="16e09-104">Wenn terminaldienstedienste aktiviert sind, muss die [*Gina*](../secgloss/g-gly.md) [*Winlogon*](../secgloss/w-gly.md) -Unterstützungsfunktionen anrufen, um das Setup für die einzelnen Benutzer abzuschließen, die [*Anmelde*](../secgloss/c-gly.md) Informationen einer Terminaldienste-Client Sitzung abzufragen und die Verbindung mit einer Terminaldienste-Netzwerksitzung zu trennen.</span><span class="sxs-lookup"><span data-stu-id="16e09-104">When Terminal Services are enabled, the [*GINA*](../secgloss/g-gly.md) must call [*Winlogon*](../secgloss/w-gly.md) support functions to complete the setup for each user, to query the [*credentials*](../secgloss/c-gly.md) of a Terminal Services client session, and to disconnect from a Terminal Services network session.</span></span>

> [!Note]  
> <span data-ttu-id="16e09-105">Gina-DLLs werden in Windows Vista ignoriert.</span><span class="sxs-lookup"><span data-stu-id="16e09-105">GINA DLLs are ignored in Windows Vista.</span></span>

 

<span data-ttu-id="16e09-106">Diese Unterstützungsfunktionen umfassen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="16e09-106">These support functions include the following.</span></span>



| <span data-ttu-id="16e09-107">Funktion</span><span class="sxs-lookup"><span data-stu-id="16e09-107">Function</span></span>                                                                     | <span data-ttu-id="16e09-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="16e09-108">Description</span></span>                                                                                         |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="16e09-109">**WlxWin31Migrate**</span><span class="sxs-lookup"><span data-stu-id="16e09-109">**WlxWin31Migrate**</span></span>](/windows/win32/api/winwlx/nc-winwlx-pwlx_win31_migrate)                                   | <span data-ttu-id="16e09-110">Schließt die Einrichtung des Benutzers ab.</span><span class="sxs-lookup"><span data-stu-id="16e09-110">Completes the setup of the user.</span></span>                                                                    |
| [<span data-ttu-id="16e09-111">**Wlxqueryclientanmelde Informationen**</span><span class="sxs-lookup"><span data-stu-id="16e09-111">**WlxQueryClientCredentials**</span></span>](/windows/win32/api/winwlx/nc-winwlx-pwlx_query_client_credentials)               | <span data-ttu-id="16e09-112">Wird aufgerufen, um die Anmelde Informationen von Remote Clients abzufragen, die keine Internetconnector-Lizenz verwenden.</span><span class="sxs-lookup"><span data-stu-id="16e09-112">Called to query the credentials of remote clients that are not using an Internet connector license.</span></span> |
| [<span data-ttu-id="16e09-113">**Wlxqueryinetconnector-Anmelde Informationen**</span><span class="sxs-lookup"><span data-stu-id="16e09-113">**WlxQueryInetConnectorCredentials**</span></span>](/windows/win32/api/winwlx/nc-winwlx-pwlx_query_ic_credentials) | <span data-ttu-id="16e09-114">Wird aufgerufen, um die Anmelde Informationen von Remote Clients abzufragen, die eine Internetconnector-Lizenz verwenden.</span><span class="sxs-lookup"><span data-stu-id="16e09-114">Called to query the credentials of remote clients that are using an Internet connector license.</span></span>     |
| [<span data-ttu-id="16e09-115">**Wlxqueryterminalservicesdata**</span><span class="sxs-lookup"><span data-stu-id="16e09-115">**WlxQueryTerminalServicesData**</span></span>](/windows/win32/api/winwlx/nc-winwlx-pwlx_query_terminal_services_data)         | <span data-ttu-id="16e09-116">Wird aufgerufen, um die Konfigurationsinformationen für Terminaldienstebenutzer abzurufen.</span><span class="sxs-lookup"><span data-stu-id="16e09-116">Called to retrieve Terminal Services user configuration information.</span></span>                                |
| [<span data-ttu-id="16e09-117">**Wlxdisconnect**</span><span class="sxs-lookup"><span data-stu-id="16e09-117">**WlxDisconnect**</span></span>](/windows/win32/api/winwlx/nc-winwlx-pwlx_disconnect)                                       | <span data-ttu-id="16e09-118">Wird aufgerufen, um die Verbindung mit einer Terminal Dienste-Netzwerksitzung zu trennen</span><span class="sxs-lookup"><span data-stu-id="16e09-118">Called to disconnect from a Terminal Services network session.</span></span>                                      |



 

<span data-ttu-id="16e09-119">Um auf diese Winlogon-Unterstützungsfunktionen zugreifen zu können, muss die Gina-DLL die [**wlx Dispatch-Struktur der \_ \_ Version \_ 1 \_ 3**](/windows/desktop/api/Winwlx/ns-winwlx-wlx_dispatch_version_1_3) verwenden.</span><span class="sxs-lookup"><span data-stu-id="16e09-119">In order to access these Winlogon support functions, the GINA DLL must use the [**WLX\_DISPATCH\_VERSION\_1\_3**](/windows/desktop/api/Winwlx/ns-winwlx-wlx_dispatch_version_1_3) structure.</span></span> <span data-ttu-id="16e09-120">In der [**wlxaushandlungs**](/windows/desktop/api/Winwlx/nf-winwlx-wlxnegotiate) -Funktion von Gina müssen beide Parameter mindestens wlx, \_ Version \_ 1 \_ 3, aufweisen.</span><span class="sxs-lookup"><span data-stu-id="16e09-120">In the GINA's [**WlxNegotiate**](/windows/desktop/api/Winwlx/nf-winwlx-wlxnegotiate) function, both parameters must be at least WLX\_VERSION\_1\_3.</span></span>

 

 
