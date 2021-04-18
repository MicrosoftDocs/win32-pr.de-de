---
title: Angegebener Benutzer
description: Angegebener Benutzer
ms.assetid: ec7684fb-a9f1-4ef2-a7d4-07caf24b6023
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acce63aa502a8966cd0eb53c90dcca3c4454e80b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340204"
---
# <a name="specified-user"></a><span data-ttu-id="d495d-103">Angegebener Benutzer</span><span class="sxs-lookup"><span data-stu-id="d495d-103">Specified User</span></span>

<span data-ttu-id="d495d-104">Die Angabe eines bestimmten Benutzers (und des Benutzer Kennworts) ist die bevorzugte Identität für com-Server.</span><span class="sxs-lookup"><span data-stu-id="d495d-104">Specifying a particular user (and the user's password) is the preferred identity for COM servers.</span></span> <span data-ttu-id="d495d-105">Der Grund für die bevorzugte Identität ist, dass auf dem Computer, auf dem der Server ausgeführt wird, auf dem Server ausgeführt werden muss, auf dem der Server ausgeführt wird, und jeder Client mit derselben Instanz des Servers kommuniziert, wenn der Server seine Klassenfactory als Mehrfachverwendung registriert.</span><span class="sxs-lookup"><span data-stu-id="d495d-105">The reason this identity is preferred is that no one has to be logged on the machine where the server is running for the server to run, and every client talks to the same instance of the server if the server registers its class factory as multi-use.</span></span> <span data-ttu-id="d495d-106">Wenn der Server über eine grafische Benutzeroberfläche verfügt, sollten Sie diese Identität nicht auswählen. Wenn Sie dies tun, wird der Benutzer nicht in der Lage sein, die Benutzeroberfläche anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="d495d-106">If the server has a GUI, you should not choose this identity; if you do, the user will not be able to see the user interface.</span></span>

<span data-ttu-id="d495d-107">Diese Art von Server verfügt über ein primäres Token und kann auf Remote Ressourcen zugreifen, bei denen ein Server mit der Start-Benutzer-Identität möglicherweise nicht in der Lage ist.</span><span class="sxs-lookup"><span data-stu-id="d495d-107">This type of server has a primary token and can access remote resources where a server that has the launching-user identity might not be able to.</span></span> <span data-ttu-id="d495d-108">Weitere Informationen zu Identitäts [Wechsel-und](cloaking.md)Zugriffs Token finden Sie unter Identitätswechsel [Ebenen](impersonation-levels.md) und-Verschleierung.</span><span class="sxs-lookup"><span data-stu-id="d495d-108">For more information about impersonation and access tokens, see [Impersonation Levels](impersonation-levels.md) and [Cloaking](cloaking.md).</span></span>

<span data-ttu-id="d495d-109">Das Ausführen von als festes Benutzerkonto ist sicherer als die interaktive Benutzeridentität, da diese Identität der Anwendung nur von einem Benutzer mit dem Kennwort eines bestimmten Benutzers zugewiesen werden kann.</span><span class="sxs-lookup"><span data-stu-id="d495d-109">Running as a fixed user account is more secure than the interactive user identity because this identity can be assigned to the application only by someone who has the specific user's password.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d495d-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d495d-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d495d-111">Anwendungs Identität</span><span class="sxs-lookup"><span data-stu-id="d495d-111">Application Identity</span></span>](application-identity.md)
</dt> <dt>

[<span data-ttu-id="d495d-112">Interaktiver Benutzer</span><span class="sxs-lookup"><span data-stu-id="d495d-112">Interactive User</span></span>](interactive-user.md)
</dt> <dt>

[<span data-ttu-id="d495d-113">Benutzer wird gestartet</span><span class="sxs-lookup"><span data-stu-id="d495d-113">Launching User</span></span>](launching-user.md)
</dt> <dt>

[<span data-ttu-id="d495d-114">Dienst Identität</span><span class="sxs-lookup"><span data-stu-id="d495d-114">Service Identity</span></span>](service-identity.md)
</dt> </dl>

 

 




