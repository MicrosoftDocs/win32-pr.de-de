---
description: Wenn Ihr Netzwerkanbieter das Durchsuchen der Netzwerkressourcen unterstützen muss, sollten die folgenden Funktionen implementiert werden. MPR ruft diese Funktionen auf, um die Ressourcen aufzuzählen.
ms.assetid: 9f7c0e5b-1358-43f8-84e4-26e84a2275ba
title: Enumerationsfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2670424be1540aad3e46e32c5b0606eb02e04bdc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041670"
---
# <a name="enumeration-functions"></a><span data-ttu-id="f53be-104">Enumerationsfunktionen</span><span class="sxs-lookup"><span data-stu-id="f53be-104">Enumeration Functions</span></span>

<span data-ttu-id="f53be-105">Wenn Ihr Netzwerkanbieter das Durchsuchen der Netzwerkressourcen unterstützen muss, sollten die folgenden Funktionen implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="f53be-105">If your network provider needs to support browsing of its network resources, it should implement the following functions.</span></span> <span data-ttu-id="f53be-106">MPR ruft diese Funktionen auf, um die Ressourcen aufzuzählen.</span><span class="sxs-lookup"><span data-stu-id="f53be-106">MPR calls these functions to enumerate the resources.</span></span>

<span data-ttu-id="f53be-107">Es ist nicht erforderlich, dass ein Netzwerkanbieter eine der-Enumerationsfunktionen implementiert.</span><span class="sxs-lookup"><span data-stu-id="f53be-107">A network provider is not required to implement any of the enumeration functions.</span></span> <span data-ttu-id="f53be-108">Wenn ein Netzwerkanbieter jedoch entweder " [**npopenenum**](/windows/desktop/api/Npapi/nf-npapi-npopenenum)", " [**npoumresource**](/windows/desktop/api/Npapi/nf-npapi-npenumresource)" oder " [**npcloseenum**](/windows/desktop/api/Npapi/nf-npapi-npcloseenum)" implementiert, muss er auch die anderen beiden Enumerationsfunktionen implementieren.</span><span class="sxs-lookup"><span data-stu-id="f53be-108">If, however, a network provider implements either [**NPOpenEnum**](/windows/desktop/api/Npapi/nf-npapi-npopenenum), [**NPEnumResource**](/windows/desktop/api/Npapi/nf-npapi-npenumresource), or [**NPCloseEnum**](/windows/desktop/api/Npapi/nf-npapi-npcloseenum), it must also implement the other two enumeration functions.</span></span>



| <span data-ttu-id="f53be-109">Funktion</span><span class="sxs-lookup"><span data-stu-id="f53be-109">Function</span></span>                                                     | <span data-ttu-id="f53be-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f53be-110">Description</span></span>                                                                                                                                                         |
|--------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f53be-111">**Npopenum**</span><span class="sxs-lookup"><span data-stu-id="f53be-111">**NPOpenEnum**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npopenenum)                             | <span data-ttu-id="f53be-112">Öffnet eine Enumeration von Netzwerkressourcen oder vorhandenen Verbindungen.</span><span class="sxs-lookup"><span data-stu-id="f53be-112">Opens an enumeration of network resources or existing connections.</span></span>                                                                                                  |
| [<span data-ttu-id="f53be-113">**Npumschlag Resource**</span><span class="sxs-lookup"><span data-stu-id="f53be-113">**NPEnumResource**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npenumresource)                     | <span data-ttu-id="f53be-114">Führt eine Enumeration für ein von [**npopenum**](/windows/desktop/api/Npapi/nf-npapi-npopenenum)zurück gegebenes Handle aus.</span><span class="sxs-lookup"><span data-stu-id="f53be-114">Performs an enumeration on a handle returned by [**NPOpenEnum**](/windows/desktop/api/Npapi/nf-npapi-npopenenum).</span></span>                                                                                   |
| [<span data-ttu-id="f53be-115">**Npcloseenum**</span><span class="sxs-lookup"><span data-stu-id="f53be-115">**NPCloseEnum**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npcloseenum)                           | <span data-ttu-id="f53be-116">Schließt eine Enumeration.</span><span class="sxs-lookup"><span data-stu-id="f53be-116">Closes an enumeration.</span></span>                                                                                                                                              |
| [<span data-ttu-id="f53be-117">**Npgetresourceinformation**</span><span class="sxs-lookup"><span data-stu-id="f53be-117">**NPGetResourceInformation**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npgetresourceinformation) | <span data-ttu-id="f53be-118">Bestimmt, ob der Anbieter der richtige Anbieter ist, um auf eine Anforderung für eine angegebene Netzwerkressource zu antworten, und gibt Informationen über den Ressourcentyp zurück.</span><span class="sxs-lookup"><span data-stu-id="f53be-118">Determines whether the provider is the correct provider to respond to a request for a specified network resource and returns information about the resource's type.</span></span> |
| [<span data-ttu-id="f53be-119">**Npgetresourceparent**</span><span class="sxs-lookup"><span data-stu-id="f53be-119">**NPGetResourceParent**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npgetresourceparent)           | <span data-ttu-id="f53be-120">Gibt das übergeordnete Element einer angegebenen Netzwerkressource in der durchsuchen-Hierarchie zurück.</span><span class="sxs-lookup"><span data-stu-id="f53be-120">Returns the parent of a specified network resource in the browse hierarchy.</span></span>                                                                                         |



 

 

 



