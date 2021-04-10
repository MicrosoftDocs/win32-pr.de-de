---
description: Das Address-Objekt stellt eine Entität dar, die Aufrufe ausführen oder empfangen kann.
ms.assetid: ab6db262-f99e-4027-9525-7597fcf02e72
title: Address-Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3ae91e70d6d8efb56321ca4619c6eb973799024
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866615"
---
# <a name="address-object"></a><span data-ttu-id="300d1-103">Address-Objekt</span><span class="sxs-lookup"><span data-stu-id="300d1-103">Address Object</span></span>

<span data-ttu-id="300d1-104">Das Address-Objekt stellt eine Entität dar, die Aufrufe ausführen oder empfangen kann.</span><span class="sxs-lookup"><span data-stu-id="300d1-104">The Address object represents an entity that can make or receive calls.</span></span> <span data-ttu-id="300d1-105">Dieses Objekt macht Schnittstellen und Methoden verfügbar, mit denen eine Anwendung eine Reihe von Vorgängen ausführen kann, wie z. b.:</span><span class="sxs-lookup"><span data-stu-id="300d1-105">This object exposes interfaces and methods that allow an application to perform a number of operations, such as:</span></span>

-   <span data-ttu-id="300d1-106">Ermitteln, ob eine angegebene Adresse einen bestimmten Satz von Medientyp Anforderungen unterstützen kann.</span><span class="sxs-lookup"><span data-stu-id="300d1-106">Discover whether a specified address can support a particular set of media type needs.</span></span>
-   <span data-ttu-id="300d1-107">Listet die derzeit der Adresse zugeordneten Aufrufe auf.</span><span class="sxs-lookup"><span data-stu-id="300d1-107">Enumerate calls currently associated with the address.</span></span>
-   <span data-ttu-id="300d1-108">Aufrufe erstellen oder weiterleiten.</span><span class="sxs-lookup"><span data-stu-id="300d1-108">Create or forward calls.</span></span>
-   <span data-ttu-id="300d1-109">Den Namen des zugeordneten Dienstanbieters erhalten.</span><span class="sxs-lookup"><span data-stu-id="300d1-109">Get the name of the associated service provider.</span></span>
-   <span data-ttu-id="300d1-110">Wenn ein Medien Dienstanbieter vorhanden ist, erhalten Sie Schnittstellen Zeiger, die eine ausführliche Terminal Bearbeitung ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="300d1-110">If a media service provider exists, get interface pointers that allow detailed terminal manipulation.</span></span>
-   <span data-ttu-id="300d1-111">Dient zum erhalten und Festlegen anderer Informationen, z. b. ob eine Nachricht wartet.</span><span class="sxs-lookup"><span data-stu-id="300d1-111">Get and set other information, such as whether a message is waiting.</span></span>

<span data-ttu-id="300d1-112">Die meisten Adressen sind einem Terminal zugeordnet, dies ist jedoch nicht gleichmäßig der Fall.</span><span class="sxs-lookup"><span data-stu-id="300d1-112">Most addresses are associated with a terminal, but this is not uniformly the case.</span></span> <span data-ttu-id="300d1-113">Ein Remote-TSP, der den Zugriff auf die Geräte auf einem Server ermöglicht, verfügt beispielsweise über eine Adresse auf dem lokalen Computer, aber nicht über ein Terminal.</span><span class="sxs-lookup"><span data-stu-id="300d1-113">For example, a remote TSP that provides access to equipment on a server will have an address on the local machine but not a terminal.</span></span> <span data-ttu-id="300d1-114">Einem Modem losen Modem ist auch kein Terminal mit seiner Adresse zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="300d1-114">A speakerless modem also has no terminal associated with its address.</span></span>

<span data-ttu-id="300d1-115">Wenn einer Adresse kein Terminal zugeordnet ist, wird die [**itterminalsupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport) -Schnittstelle für das Objekt nicht verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="300d1-115">If an address does not have an associated terminal, the [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport) interface is not exposed on the object.</span></span>

<span data-ttu-id="300d1-116">Das Beispiel zum [Auswählen eines Adress](select-an-address.md) Codes zeigt den grundlegenden Prozess zum Abrufen eines Adress Objekt Zeigers.</span><span class="sxs-lookup"><span data-stu-id="300d1-116">The [Select an Address](select-an-address.md) code example shows the basic process for acquiring an address object pointer.</span></span>

<span data-ttu-id="300d1-117">Eine Liste aller dem Adress Objekt zugeordneten Schnittstellen finden Sie unter [Adress Objekt Schnittstellen](address-object-interfaces.md) .</span><span class="sxs-lookup"><span data-stu-id="300d1-117">See [Address Object Interfaces](address-object-interfaces.md) for a list of all interfaces associated with the Address object.</span></span>

 

 
