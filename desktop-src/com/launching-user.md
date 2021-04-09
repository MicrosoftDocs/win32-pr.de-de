---
title: Benutzer wird gestartet
description: Benutzer wird gestartet
ms.assetid: ea5140b6-0a79-4149-b845-4f6388e89104
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf6fb60652bff77eb27a33ec8a8a8d40db0f0023
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103858491"
---
# <a name="launching-user"></a><span data-ttu-id="61ae8-103">Benutzer wird gestartet</span><span class="sxs-lookup"><span data-stu-id="61ae8-103">Launching User</span></span>

<span data-ttu-id="61ae8-104">Dies ist die Standardeinstellung für die Anwendungs Identität.</span><span class="sxs-lookup"><span data-stu-id="61ae8-104">This is the default setting for the application identity.</span></span> <span data-ttu-id="61ae8-105">Wenn der Start Benutzer für die Identität der Anwendung ausgewählt wird, erhält jedes Client Konto eine neue Instanz des Servers, und jeder Server erhält seine eigene [Fenster Station](/windows/desktop/winstation/window-stations).</span><span class="sxs-lookup"><span data-stu-id="61ae8-105">When the launching user is chosen for the application's identity, each client account gets a new instance of the server and each server gets its own [window station](/windows/desktop/winstation/window-stations).</span></span> <span data-ttu-id="61ae8-106">Aufgrund der separaten Server Instanzen ist das Starten des Benutzers die Sicherheitsschutz-Identitäts Einstellung auf höchster Ebene.</span><span class="sxs-lookup"><span data-stu-id="61ae8-106">Because of the separate server instances, launching user is the highest-level security protection identity setting.</span></span> <span data-ttu-id="61ae8-107">Es gibt jedoch endliche Grenzwerte für den Ressourcenverbrauch.</span><span class="sxs-lookup"><span data-stu-id="61ae8-107">However, there are finite limits on resource consumption.</span></span> <span data-ttu-id="61ae8-108">Außerdem wird jede GUI, die der Server anzeigt, vom Client nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="61ae8-108">Also, any GUI the server displays will not be seen by the client.</span></span>

<span data-ttu-id="61ae8-109">Wenn die Anwendung über die Identität des Start Benutzers verfügt, wird Sie mit einem Identitätswechsel Token ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="61ae8-109">If the application has the identity of the launching user, it runs with an impersonation token.</span></span> <span data-ttu-id="61ae8-110">Weitere Informationen zu Identitäts [Wechsel-und](cloaking.md)Zugriffs Token finden Sie unter Identitätswechsel [Ebenen](impersonation-levels.md) und-Verschleierung.</span><span class="sxs-lookup"><span data-stu-id="61ae8-110">For more information about impersonation and access tokens, see [Impersonation Levels](impersonation-levels.md) and [Cloaking](cloaking.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="61ae8-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="61ae8-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="61ae8-112">Anwendungs Identität</span><span class="sxs-lookup"><span data-stu-id="61ae8-112">Application Identity</span></span>](application-identity.md)
</dt> <dt>

[<span data-ttu-id="61ae8-113">Interaktiver Benutzer</span><span class="sxs-lookup"><span data-stu-id="61ae8-113">Interactive User</span></span>](interactive-user.md)
</dt> <dt>

[<span data-ttu-id="61ae8-114">Dienst Identität</span><span class="sxs-lookup"><span data-stu-id="61ae8-114">Service Identity</span></span>](service-identity.md)
</dt> <dt>

[<span data-ttu-id="61ae8-115">Angegebener Benutzer</span><span class="sxs-lookup"><span data-stu-id="61ae8-115">Specified User</span></span>](specified-user.md)
</dt> </dl>

 

 