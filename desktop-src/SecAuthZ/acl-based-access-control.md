---
description: Ebenso wie das System Sicherheits Deskriptoren zum Steuern des Zugriffs auf Sicherungs fähige Objekte verwendet, kann ein Server Sicherheits Deskriptoren verwenden, um den Zugriff auf seine privaten Objekte zu steuern. Weitere Informationen zum Windows-Sicherheitsmodell finden Sie unter Access Control Modell.
ms.assetid: d6219438-711a-4eda-a893-9095bce3a07d
title: ACL-basiertes Access Control
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b477f998b7866c66860b94c3ff1266392f49373
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756184"
---
# <a name="acl-based-access-control"></a><span data-ttu-id="002e6-104">ACL-basiertes Access Control</span><span class="sxs-lookup"><span data-stu-id="002e6-104">ACL-based Access Control</span></span>

<span data-ttu-id="002e6-105">Ebenso wie das System [Sicherheits Deskriptoren](security-descriptors.md) zum Steuern des Zugriffs auf Sicherungs fähige Objekte verwendet, kann ein Server Sicherheits Deskriptoren verwenden, um den Zugriff auf seine privaten Objekte zu steuern.</span><span class="sxs-lookup"><span data-stu-id="002e6-105">Just as the system uses [security descriptors](security-descriptors.md) to control access to securable objects, a server can use security descriptors to control access to its private objects.</span></span> <span data-ttu-id="002e6-106">Weitere Informationen zum Windows-Sicherheitsmodell finden Sie unter [Access Control Modell](access-control-model.md).</span><span class="sxs-lookup"><span data-stu-id="002e6-106">For more information about the Windows security model, see [Access Control Model](access-control-model.md).</span></span>

<span data-ttu-id="002e6-107">Ein geschützter Server kann [eine Sicherheits Beschreibung](security-descriptors-for-private-objects.md) mit einer DACL erstellen, die die Zugriffs Typen angibt, die für verschiedene [Treuhänder](trustees.md)zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="002e6-107">A protected server can [create a security descriptor](security-descriptors-for-private-objects.md) with a DACL that specifies the types of access allowed for various [trustees](trustees.md).</span></span> <span data-ttu-id="002e6-108">In einem einfachen Fall könnte der Server einen einzelnen Sicherheits Deskriptor erstellen, um den [Zugriff auf alle Daten und Funktionen des Servers zu steuern](checking-access-to-private-objects.md).</span><span class="sxs-lookup"><span data-stu-id="002e6-108">In a simple case, the server could create a single security descriptor to [control access to all of the server's data and functionality](checking-access-to-private-objects.md).</span></span> <span data-ttu-id="002e6-109">Um eine präzisere Granularität des Schutzes zu erzielen, könnte der Server Sicherheits Deskriptoren für die einzelnen privaten Objekte oder für verschiedene Arten von Funktionen erstellen.</span><span class="sxs-lookup"><span data-stu-id="002e6-109">For a finer granularity of protection, the server could create security descriptors for each of its private objects, or for different types of functionality.</span></span>

<span data-ttu-id="002e6-110">Wenn ein Client z. b. den Server auffordert, ein neues Objekt in einer Datenbank zu erstellen, könnte der Server eine Sicherheits Beschreibung für das neue private Objekt erstellen.</span><span class="sxs-lookup"><span data-stu-id="002e6-110">For example, when a client asks the server to create a new object in a database, the server could create a security descriptor for the new private object.</span></span> <span data-ttu-id="002e6-111">Der Server kann dann die Sicherheits Beschreibung mit dem privaten Objekt in der Datenbank speichern.</span><span class="sxs-lookup"><span data-stu-id="002e6-111">The server could then store the security descriptor with the private object in the database.</span></span> <span data-ttu-id="002e6-112">Wenn ein Client versucht, auf das Objekt zuzugreifen, ruft der Server die Sicherheits Beschreibung ab, um die Zugriffsrechte des Clients zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="002e6-112">When a client tries to access the object, the server retrieves the security descriptor to check the client's access rights.</span></span> <span data-ttu-id="002e6-113">Beachten Sie, dass es in einer Sicherheits Beschreibung nichts gibt, das Sie dem Objekt oder der Funktionalität zuordnet, das Sie schützt.</span><span class="sxs-lookup"><span data-stu-id="002e6-113">It is important to note that there is nothing in a security descriptor that associates it with the object or functionality it is protecting.</span></span> <span data-ttu-id="002e6-114">Stattdessen ist es für den geschützten Server, die Zuordnung aufrechtzuerhalten.</span><span class="sxs-lookup"><span data-stu-id="002e6-114">Instead, it is up to the protected server to maintain the association.</span></span>

<span data-ttu-id="002e6-115">Der Zugriff auf das private Objekt kann auch überwacht werden.</span><span class="sxs-lookup"><span data-stu-id="002e6-115">Access to the private object can also be audited.</span></span> <span data-ttu-id="002e6-116">Eine Beschreibung hierzu finden Sie unter Überwachen des [Zugriffs auf private Objekte](auditing-access-to-private-objects.md) .</span><span class="sxs-lookup"><span data-stu-id="002e6-116">Refer to [Auditing Access to Private Objects](auditing-access-to-private-objects.md) for a description of this.</span></span>

 

 



