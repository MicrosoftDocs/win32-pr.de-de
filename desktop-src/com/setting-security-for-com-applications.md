---
title: Festlegen der Sicherheit für COM-Anwendungen
description: Festlegen der Sicherheit für COM-Anwendungen
ms.assetid: 5b615007-e04b-41be-872c-20e0ea818ff1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a8dd705015aaa2ca1965d07c556ff3d55aada00
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103857019"
---
# <a name="setting-security-for-com-applications"></a><span data-ttu-id="31068-103">Festlegen der Sicherheit für COM-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="31068-103">Setting Security for COM Applications</span></span>

<span data-ttu-id="31068-104">Es gibt mehrere Möglichkeiten, die Sicherheit für Ihre Anwendungen zu steuern.</span><span class="sxs-lookup"><span data-stu-id="31068-104">There are several ways you can help control security for your applications.</span></span> <span data-ttu-id="31068-105">Sie können die Standard Sicherheitseinstellungen eines Computers ändern, die von allen Anwendungen auf dem Computer verwendet werden, die keine eigenen Sicherheitswerte bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="31068-105">You can change a computer's default security settings, which are used by all applications on the computer that do not supply their own security values.</span></span> <span data-ttu-id="31068-106">Sie können die Sicherheit für einen bestimmten Prozess entweder mithilfe von Dcomcnfg.exe oder durch Aufrufen von [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)festlegen.</span><span class="sxs-lookup"><span data-stu-id="31068-106">You can set security for a particular process, either by using Dcomcnfg.exe or by calling [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="31068-107">Sie können Sicherheitseinstellungen auch Programm gesteuert auf der Schnittstellen Proxy Ebene steuern.</span><span class="sxs-lookup"><span data-stu-id="31068-107">You can also programmatically control security settings at the interface proxy level.</span></span>

<span data-ttu-id="31068-108">Die folgenden Themen enthalten Verfahren zum Festlegen der Sicherheit:</span><span class="sxs-lookup"><span data-stu-id="31068-108">The following topics provide procedures that explain how to set security:</span></span>

-   [<span data-ttu-id="31068-109">Ändern der Sicherheits Standardwerte für einen Computer</span><span class="sxs-lookup"><span data-stu-id="31068-109">Modifying the Security Defaults for a Computer</span></span>](modifying-the-security-defaults-for-a-computer.md)
-   [<span data-ttu-id="31068-110">Festlegen Process-Wide Sicherheit</span><span class="sxs-lookup"><span data-stu-id="31068-110">Setting Process-Wide Security</span></span>](setting-processwide-security.md)
-   [<span data-ttu-id="31068-111">Festlegen der Sicherheit auf der Ebene des Schnittstellen Proxys</span><span class="sxs-lookup"><span data-stu-id="31068-111">Setting Security at the Interface Proxy Level</span></span>](setting-security-at-the-interface-proxy-level.md)

## <a name="related-topics"></a><span data-ttu-id="31068-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="31068-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="31068-113">Sicherheit in com</span><span class="sxs-lookup"><span data-stu-id="31068-113">Security in COM</span></span>](security-in-com.md)
</dt> </dl>

 

 




