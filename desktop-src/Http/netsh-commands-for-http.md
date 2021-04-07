---
title: Netsh-Befehle für http
description: Sie können die Netsh-Befehle für den HTTP-Kontext verwenden, um HTTP.sys Einstellungen und Parameter abzufragen und zu konfigurieren.
ms.assetid: 695c309c-ab43-4c6a-b5f6-5bb9f715bf71
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55f6e0fdd0813284e36d2fb9fb826929c67df63c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712534"
---
# <a name="netsh-commands-for-http"></a><span data-ttu-id="4b149-103">Netsh-Befehle für http</span><span class="sxs-lookup"><span data-stu-id="4b149-103">Netsh commands for HTTP</span></span>

<span data-ttu-id="4b149-104">Sie können die Netsh-Befehle für den HTTP-Kontext verwenden, um HTTP.sys Einstellungen und Parameter abzufragen und zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="4b149-104">You can use the Netsh commands for HTTP context to query and configure HTTP.sys settings and parameters.</span></span>

<span data-ttu-id="4b149-105">Sie können diese Befehle an der Eingabeaufforderung im Windows Vista-Betriebssystem oder an der Eingabeaufforderung für den **netsh http** -Kontext ausführen.</span><span class="sxs-lookup"><span data-stu-id="4b149-105">You can run these commands at the command prompt in the Windows Vista operating system or at the command prompt for the **netsh http** context.</span></span> <span data-ttu-id="4b149-106">Damit diese Befehle an der Eingabeaufforderung in Windows Vista ausgeführt werden können, müssen Sie **netsh http** eingeben, bevor Sie Befehle und Parameter eingeben, wie Sie in der folgenden Syntax angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="4b149-106">For these commands to work at the command prompt in Windows Vista, you must type **netsh http** before typing commands and parameters as they appear in the syntax below.</span></span> <span data-ttu-id="4b149-107">Zum Anzeigen der Hilfe für einen Befehl an der Eingabeaufforderung geben Sie \* CommandName \***/?** ein, wobei *CommandName* der Name des Befehls ist.</span><span class="sxs-lookup"><span data-stu-id="4b149-107">To view help for a command at the command prompt, type \*CommandName\***/?**, where *CommandName* is the name of the command.</span></span>

<span data-ttu-id="4b149-108">Informationen zum Anzeigen der Befehlssyntax finden Sie in den folgenden Befehlen:</span><span class="sxs-lookup"><span data-stu-id="4b149-108">To view the command syntax, see the commands:</span></span>

-   [<span data-ttu-id="4b149-109">**add iplisten**</span><span class="sxs-lookup"><span data-stu-id="4b149-109">**add iplisten**</span></span>](add-iplisten.md)
-   [<span data-ttu-id="4b149-110">**add sslcert**</span><span class="sxs-lookup"><span data-stu-id="4b149-110">**add sslcert**</span></span>](add-sslcert.md)
-   [<span data-ttu-id="4b149-111">**add timeout**</span><span class="sxs-lookup"><span data-stu-id="4b149-111">**add timeout**</span></span>](add-timeout.md)
-   [<span data-ttu-id="4b149-112">**add urlacl**</span><span class="sxs-lookup"><span data-stu-id="4b149-112">**add urlacl**</span></span>](add-urlacl.md)
-   [<span data-ttu-id="4b149-113">**Cache löschen**</span><span class="sxs-lookup"><span data-stu-id="4b149-113">**delete cache**</span></span>](delete-cache.md)
-   [<span data-ttu-id="4b149-114">**delete iplisten**</span><span class="sxs-lookup"><span data-stu-id="4b149-114">**delete iplisten**</span></span>](delete-iplisten.md)
-   [<span data-ttu-id="4b149-115">**delete sslcert**</span><span class="sxs-lookup"><span data-stu-id="4b149-115">**delete sslcert**</span></span>](delete-sslcert.md)
-   [<span data-ttu-id="4b149-116">**delete timeout**</span><span class="sxs-lookup"><span data-stu-id="4b149-116">**delete timeout**</span></span>](delete-timeout.md)
-   [<span data-ttu-id="4b149-117">**delete urlacl**</span><span class="sxs-lookup"><span data-stu-id="4b149-117">**delete urlacl**</span></span>](delete-urlacl.md)
-   [<span data-ttu-id="4b149-118">**flush logbuffer**</span><span class="sxs-lookup"><span data-stu-id="4b149-118">**flush logbuffer**</span></span>](flush-logbuffer.md)
-   [<span data-ttu-id="4b149-119">**show cachestate**</span><span class="sxs-lookup"><span data-stu-id="4b149-119">**show cachestate**</span></span>](show-cachestate.md)
-   [<span data-ttu-id="4b149-120">**show iplisten**</span><span class="sxs-lookup"><span data-stu-id="4b149-120">**show iplisten**</span></span>](show-iplisten.md)
-   [<span data-ttu-id="4b149-121">**show servicestate**</span><span class="sxs-lookup"><span data-stu-id="4b149-121">**show servicestate**</span></span>](show-servicestate.md)
-   [<span data-ttu-id="4b149-122">**show sslcert**</span><span class="sxs-lookup"><span data-stu-id="4b149-122">**show sslcert**</span></span>](show-sslcert.md)
-   [<span data-ttu-id="4b149-123">**show timeout**</span><span class="sxs-lookup"><span data-stu-id="4b149-123">**show timeout**</span></span>](show-timeout.md)
-   [<span data-ttu-id="4b149-124">**show urlacl**</span><span class="sxs-lookup"><span data-stu-id="4b149-124">**show urlacl**</span></span>](show-urlacl.md)

 

 




