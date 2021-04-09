---
description: Die Peer Identity Manager-API ermöglicht es Ihnen, Peer Identitäten in einer Peer Anwendung zu erstellen, aufzulisten und zu bearbeiten.
ms.assetid: c1b2a587-71c7-4623-a318-4624dad7feba
title: Informationen zu Identity Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfe66e21bf6c131006ed98c7f5f211c316464ebe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865175"
---
# <a name="about-identity-manager"></a><span data-ttu-id="9e82c-103">Informationen zu Identity Manager</span><span class="sxs-lookup"><span data-stu-id="9e82c-103">About Identity Manager</span></span>

<span data-ttu-id="9e82c-104">Die Peer Identity Manager-API ermöglicht es Ihnen, Peer Identitäten in einer Peer Anwendung zu erstellen, aufzulisten und zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="9e82c-104">The Peer Identity Manager API allows you to create, enumerate, and manipulate peer identities in a peer application.</span></span> <span data-ttu-id="9e82c-105">Sie können die mit dieser API erstellten Peer Identitäten als Eingabe für die Peer Gruppierung und die PNRP-Namespace Anbieter-APIs (Peer Name Resolution Protocol) verwenden.</span><span class="sxs-lookup"><span data-stu-id="9e82c-105">You can use the peer identities created using this API as input for the Peer Grouping and Peer Name Resolution Protocol (PNRP) Namespace Provider APIs.</span></span>

## <a name="peer-identity-manager-best-practices"></a><span data-ttu-id="9e82c-106">Bewährte Methoden für Peer Identity Manager</span><span class="sxs-lookup"><span data-stu-id="9e82c-106">Peer Identity Manager Best Practices</span></span>

<span data-ttu-id="9e82c-107">Jeder Benutzer sollte über einige Peer Identitäten verfügen, die für die Peer Aktivitäten verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="9e82c-107">Each user should have a few peer identities that they can use for the peer activities.</span></span> <span data-ttu-id="9e82c-108">Beispielsweise kann ein Benutzer über zwei Peer Identitäten für Arbeit und Freizeit verfügen.</span><span class="sxs-lookup"><span data-stu-id="9e82c-108">For example, a user might have two peer identities for work and leisure.</span></span>

<span data-ttu-id="9e82c-109">Eine gut entworfene Peer Anwendung ermöglicht es Benutzern, eine zu verwendende Peer Identität auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="9e82c-109">A well-designed peer application allows a user to select a peer identity to use.</span></span> <span data-ttu-id="9e82c-110">Ein Benutzer kann eine neue Peer Identität erstellen, wenn keine der vorhandenen Peer Identitäten für die Verwendung mit einer Anwendung geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="9e82c-110">A user can create a new peer identity if none of the existing peer identities are appropriate to use with an application.</span></span>

<span data-ttu-id="9e82c-111">Eine gut entworfene Peer Anwendung steuert außerdem die Anzahl der von ihr erstellten Identitäten.</span><span class="sxs-lookup"><span data-stu-id="9e82c-111">A well-designed peer application also controls the number of identities that it creates.</span></span> <span data-ttu-id="9e82c-112">Wenn eine Anwendung eine temporäre Peer Identität erstellt, muss die Anwendung die Peer Identität löschen, wenn die Identität nicht benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="9e82c-112">If an application creates a temporary peer identity, the application must delete the peer identity when the identity is not needed.</span></span> <span data-ttu-id="9e82c-113">Wenn eine Anwendung diese Wartung nicht durchführt, kann der Peer Identity Manager möglicherweise keine Peer Identitäten erstellen, bis einige Peer Identitäten entfernt wurden.</span><span class="sxs-lookup"><span data-stu-id="9e82c-113">If an application does not perform this maintenance, the Peer Identity Manager may not be able to create peer identities until some peer identities are removed.</span></span>

 

 



