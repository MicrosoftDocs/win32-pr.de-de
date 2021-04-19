---
description: Einige Funktionen erfordern spezielle Berechtigungen, um ordnungsgemäß auszuführen.
ms.assetid: b25db548-d5ab-4276-9b50-36d030909384
title: Ausführen mit besonderen Berechtigungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53be662d187ef27c7afc12b031f2d8de225d34c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369043"
---
# <a name="running-with-special-privileges"></a><span data-ttu-id="3b597-103">Ausführen mit besonderen Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="3b597-103">Running with Special Privileges</span></span>

<span data-ttu-id="3b597-104">Einige Funktionen erfordern spezielle [Berechtigungen](/windows/desktop/SecAuthZ/privileges) , um ordnungsgemäß auszuführen.</span><span class="sxs-lookup"><span data-stu-id="3b597-104">Some functions require special [privileges](/windows/desktop/SecAuthZ/privileges) to run correctly.</span></span> <span data-ttu-id="3b597-105">In einigen Fällen kann die Funktion nur von bestimmten Benutzern oder von Mitgliedern bestimmter Gruppen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="3b597-105">In some cases, the function can only be run by certain users or by members of certain groups.</span></span> <span data-ttu-id="3b597-106">Die häufigste Anforderung ist, dass der Benutzer ein lokaler Administrator ist.</span><span class="sxs-lookup"><span data-stu-id="3b597-106">The most common requirement is that the user be a local administrator.</span></span> <span data-ttu-id="3b597-107">Für andere Funktionen ist es erforderlich, dass das Konto des Benutzers über bestimmte Berechtigungen verfügt.</span><span class="sxs-lookup"><span data-stu-id="3b597-107">Other functions require the user's account to have specific privileges enabled.</span></span>

<span data-ttu-id="3b597-108">Um die Möglichkeit zu verringern, dass nicht autorisierter Code die Kontrolle erhält, sollte das System mit den geringsten Berechtigungen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="3b597-108">To reduce the possibility of unauthorized code being able to get control, the system should run with the least privilege necessary.</span></span> <span data-ttu-id="3b597-109">Anwendungen, die Funktionen anrufen müssen, die besondere Berechtigungen erfordern, können das System für Angriffe durch Hacker offenlegen.</span><span class="sxs-lookup"><span data-stu-id="3b597-109">Applications that need to call functions that require special privileges can leave the system open to attack by hackers.</span></span> <span data-ttu-id="3b597-110">Solche Anwendungen sollten so konzipiert sein, dass Sie für kurze Zeiträume ausgeführt werden und den Benutzer über die betroffenen Sicherheitsrisiken informieren.</span><span class="sxs-lookup"><span data-stu-id="3b597-110">Such applications should be designed to run for short periods of time and should inform the user of the security implications involved.</span></span>

<span data-ttu-id="3b597-111">Informationen dazu, wie Sie unterschiedliche Benutzer ausführen und Berechtigungen in Ihrer Anwendung aktivieren, finden Sie in den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="3b597-111">For information about how to run as different users and how to enable privileges in your application, see the following topics:</span></span><dl>

[<span data-ttu-id="3b597-112">Ausführen mit Administrator Rechten</span><span class="sxs-lookup"><span data-stu-id="3b597-112">Running with Administrator Privileges</span></span>](running-with-administrator-privileges.md)  
[<span data-ttu-id="3b597-113">Benutzer werden zur Anmelde Informationen aufgefordert</span><span class="sxs-lookup"><span data-stu-id="3b597-113">Asking the User for Credentials</span></span>](asking-the-user-for-credentials.md)  
[<span data-ttu-id="3b597-114">Ändern von Berechtigungen in einem Token</span><span class="sxs-lookup"><span data-stu-id="3b597-114">Changing Privileges in a Token</span></span>](changing-privileges-in-a-token.md)  
[<span data-ttu-id="3b597-115">Zuweisen von Berechtigungen zu einem Konto</span><span class="sxs-lookup"><span data-stu-id="3b597-115">Assigning Privileges to an Account</span></span>](assigning-privileges-to-an-account.md)  
</dl>

 

 
