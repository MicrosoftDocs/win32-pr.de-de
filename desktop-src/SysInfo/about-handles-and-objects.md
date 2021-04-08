---
description: Das System verwendet Objekte und Handles, um den Zugriff auf Systemressourcen aus zwei Hauptgründen zu regulieren.
ms.assetid: 122acb9e-2a1b-480b-9207-5cc6bbe6b6d4
title: Informationen zu Handles und Objekten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c7474c11298166cc8d63032c6e1d8f84e6db249
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103959853"
---
# <a name="about-handles-and-objects"></a><span data-ttu-id="6fe8e-103">Informationen zu Handles und Objekten</span><span class="sxs-lookup"><span data-stu-id="6fe8e-103">About Handles and Objects</span></span>

<span data-ttu-id="6fe8e-104">Das System verwendet Objekte und Handles, um den Zugriff auf Systemressourcen aus zwei Hauptgründen zu regulieren.</span><span class="sxs-lookup"><span data-stu-id="6fe8e-104">The system uses objects and handles to regulate access to system resources for two main reasons.</span></span> <span data-ttu-id="6fe8e-105">Zunächst wird durch die Verwendung von-Objekten sichergestellt, dass Microsoft die Systemfunktionalität aktualisieren kann, solange die ursprüngliche Objektschnittstelle beibehalten wird.</span><span class="sxs-lookup"><span data-stu-id="6fe8e-105">First, the use of objects ensures that Microsoft can update system functionality, as long as the original object interface is maintained.</span></span> <span data-ttu-id="6fe8e-106">Wenn nachfolgende Versionen des Systems freigegeben werden, können Sie das aktualisierte Objekt mit geringem oder ohne zusätzliche Arbeit verwenden.</span><span class="sxs-lookup"><span data-stu-id="6fe8e-106">When subsequent versions of the system are released, you can use the updated object with little or no additional work.</span></span>

<span data-ttu-id="6fe8e-107">Zweitens ermöglicht die Verwendung von-Objekten das Nutzen der Windows-Sicherheit.</span><span class="sxs-lookup"><span data-stu-id="6fe8e-107">Secondly, the use of objects enables you to take advantage of Windows security.</span></span> <span data-ttu-id="6fe8e-108">Jedes-Objekt verfügt über eine eigene Zugriffs Steuerungs Liste (ACL), die die Aktionen angibt, die ein Prozess für das Objekt ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="6fe8e-108">Each object has its own access-control list (ACL) that specifies the actions a process can perform on the object.</span></span> <span data-ttu-id="6fe8e-109">Das System überprüft die ACL eines Objekts jedes Mal, wenn eine Anwendung ein Handle für das Objekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="6fe8e-109">The system examines an object's ACL each time an application creates a handle to the object.</span></span> <span data-ttu-id="6fe8e-110">Weitere Informationen finden Sie unter [Zugriffssteuerung](/windows/desktop/SecAuthZ/access-control).</span><span class="sxs-lookup"><span data-stu-id="6fe8e-110">For more information, see [Access Control](/windows/desktop/SecAuthZ/access-control).</span></span>

-   [<span data-ttu-id="6fe8e-111">Objekt-Manager</span><span class="sxs-lookup"><span data-stu-id="6fe8e-111">Object Manager</span></span>](object-manager.md)
-   [<span data-ttu-id="6fe8e-112">Objektschnittstelle</span><span class="sxs-lookup"><span data-stu-id="6fe8e-112">Object Interface</span></span>](object-interface.md)
-   [<span data-ttu-id="6fe8e-113">Objektnamespaces</span><span class="sxs-lookup"><span data-stu-id="6fe8e-113">Object Namespaces</span></span>](/windows/desktop/Sync/object-namespaces)
-   [<span data-ttu-id="6fe8e-114">Einschränkungen behandeln</span><span class="sxs-lookup"><span data-stu-id="6fe8e-114">Handle Limitations</span></span>](handle-limitations.md)
-   [<span data-ttu-id="6fe8e-115">Behandlung von Vererbung</span><span class="sxs-lookup"><span data-stu-id="6fe8e-115">Handle Inheritance</span></span>](handle-inheritance.md)

 

 
