---
title: Autorisierungs Dienste
description: Ein Autorisierungs Dienst ist die Methode, die der SSP zum Autorisieren des Zugriffs auf eine Remote Prozedur verwendet. SSPs können mehr als einen Autorisierungs Dienst bereitstellen. Sie wählen jedoch in der Regel eine Standardeinstellung aus.
ms.assetid: 5ea3cde9-96e9-4208-bb61-d0f98f23b90c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 548f834c69726425a52a033e0dbb08bf6f1f3a38
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037272"
---
# <a name="authorization-services"></a><span data-ttu-id="d4f87-105">Autorisierungs Dienste</span><span class="sxs-lookup"><span data-stu-id="d4f87-105">Authorization Services</span></span>

<span data-ttu-id="d4f87-106">Ein Autorisierungs Dienst ist die Methode, die der SSP zum Autorisieren des Zugriffs auf eine Remote Prozedur verwendet.</span><span class="sxs-lookup"><span data-stu-id="d4f87-106">An authorization service is the method that the SSP uses to authorize access to a remote procedure.</span></span> <span data-ttu-id="d4f87-107">SSPs können mehr als einen Autorisierungs Dienst bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="d4f87-107">SSPs can provide more than one authorization service.</span></span> <span data-ttu-id="d4f87-108">Sie wählen jedoch in der Regel eine Standardeinstellung aus.</span><span class="sxs-lookup"><span data-stu-id="d4f87-108">However, they usually select one as a default.</span></span>

<span data-ttu-id="d4f87-109">Die Anwendung kann die Standard Autorisierungs Methode für den aktuellen SSP verwenden, oder Sie kann eine-Methode angeben.</span><span class="sxs-lookup"><span data-stu-id="d4f87-109">Your application can use the default authorization method for the current SSP, or it can specify one.</span></span> <span data-ttu-id="d4f87-110">Derzeit werden von Microsoft RPC zwei Autorisierungs Methoden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d4f87-110">At present, Microsoft RPC supports two methods of authorization.</span></span> <span data-ttu-id="d4f87-111">Eine besteht darin, dass der Server Autorisierung basierend auf dem Namen des Client Programms bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="d4f87-111">One is for the server to provide authorization based on the name of the client program.</span></span> <span data-ttu-id="d4f87-112">Die andere ist, dass der Server die Anmelde Informationen des Clients mit der Zugriffs Steuerungs Liste (Access Control List, ACL) des Servers vergleicht.</span><span class="sxs-lookup"><span data-stu-id="d4f87-112">The other is for the server to compare the client's authentication credentials against the server's access control list (ACL).</span></span>

<span data-ttu-id="d4f87-113">Eine Liste der Autorisierungs Dienste finden Sie unter [Authorization-Service-Konstanten](authorization-service-constants.md).</span><span class="sxs-lookup"><span data-stu-id="d4f87-113">For a list of authorization services, see [Authorization-Service Constants](authorization-service-constants.md).</span></span>

> [!Note]  
> <span data-ttu-id="d4f87-114">Es wird empfohlen, dass der Entwickler RPC \_ C \_ Authz \_ None verwendet.</span><span class="sxs-lookup"><span data-stu-id="d4f87-114">It is recommended that developers use RPC\_C\_AUTHZ\_NONE.</span></span>

 

 

 




