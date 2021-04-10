---
title: Integration von Erweiterungen durch ADSI
description: Richtlinien, die beschreiben, wie ADSI mit Erweiterungen interagiert.
ms.assetid: 00301551-ec56-4cb4-8e77-264c3ad48814
ms.tgt_platform: multiple
keywords:
- Erweiterungen ADSI
- ADSI und Erweiterungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 956a76954851ea54b4eae99bfa45102a3b2fefa5
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104039603"
---
# <a name="how-adsi-integrates-extensions"></a><span data-ttu-id="98121-105">Integration von Erweiterungen durch ADSI</span><span class="sxs-lookup"><span data-stu-id="98121-105">How ADSI Integrates Extensions</span></span>

<span data-ttu-id="98121-106">In den folgenden Richtlinien wird beschrieben, wie ADSI mit Erweiterungen interagiert:</span><span class="sxs-lookup"><span data-stu-id="98121-106">The following guidelines describe how ADSI interacts with extensions:</span></span>

-   <span data-ttu-id="98121-107">Etwas wird an ein ADSI-Verzeichnis Objekt gebunden.</span><span class="sxs-lookup"><span data-stu-id="98121-107">Something binds to an ADSI directory object.</span></span> <span data-ttu-id="98121-108">Beispiel: "LDAP://CN = JeffSmith, OU = Sales, DC = fabrikam, DC = com".</span><span class="sxs-lookup"><span data-stu-id="98121-108">For example, "LDAP://CN=JeffSmith,OU=Sales,DC=Fabrikam,DC=COM".</span></span>
-   <span data-ttu-id="98121-109">ADSI identifiziert, dass das Objekt in der **User** -Klasse vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="98121-109">ADSI identifies that the object is in the **user** class.</span></span>
-   <span data-ttu-id="98121-110">ADSI führt eine Suche in der Registrierung durch und identifiziert die Erweiterungs-CLSIDs für den **Benutzer**.</span><span class="sxs-lookup"><span data-stu-id="98121-110">ADSI performs a lookup in the registry and identifies the extension CLSIDs for **user**.</span></span> <span data-ttu-id="98121-111">Beachten Sie, dass ADSI diese Daten zwischenspeichert.</span><span class="sxs-lookup"><span data-stu-id="98121-111">Be aware that ADSI caches this data.</span></span>
-   <span data-ttu-id="98121-112">Die **QueryInterface** -Methode wird für IID \_ imyextension aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="98121-112">Something calls the **QueryInterface** method for IID\_IMyExtension.</span></span> <span data-ttu-id="98121-113">ADSI durchsucht die Schnittstellen, die dem **User** -Objekt zugeordnet sind, beginnend mit seinen eigenen Schnittstellen und untersucht dann Erweiterungs Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="98121-113">ADSI searches the interfaces associated with the **user** object, starting with its own interfaces, then looking at extension interfaces.</span></span>
-   <span data-ttu-id="98121-114">Wenn eine Entsprechung gefunden wird, erstellt ADSI eine Instanz der Komponente, die IID \_ imyextension unterstützt, und ruft **QueryInterface** für die Erweiterung auf.</span><span class="sxs-lookup"><span data-stu-id="98121-114">If a match is found, ADSI creates an instance of the component that supports IID\_IMyExtension, and calls **QueryInterface** for the extension.</span></span> <span data-ttu-id="98121-115">Die resultierende Schnittstelle wird zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="98121-115">The resulting interface is returned.</span></span>
-   <span data-ttu-id="98121-116">Der Benutzer verwendet diese Schnittstelle, um die Schnittstellen Methoden aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="98121-116">The user uses this interface to call the interface methods.</span></span>
-   <span data-ttu-id="98121-117">Als Nächstes ruft der Client **QueryInterface** für IID \_ iyourextension auf, die sich in einer anderen Komponente befindet.</span><span class="sxs-lookup"><span data-stu-id="98121-117">Next, the client calls **QueryInterface** for IID\_IYourExtension, which is in a different component.</span></span> <span data-ttu-id="98121-118">Diese Komponente delegiert diesen **QueryInterface** -Aufrufe an die [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle des Aggregators, bei der es sich um ADSI selbst handelt.</span><span class="sxs-lookup"><span data-stu-id="98121-118">This component delegates this **QueryInterface** call to the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface of the aggregator, which happens to be ADSI itself.</span></span>
-   <span data-ttu-id="98121-119">Erneut durchsucht ADSI die Schnittstellen und erstellt die Komponenteninstanz.</span><span class="sxs-lookup"><span data-stu-id="98121-119">Again, ADSI searches the interfaces and creates the component instance.</span></span>

 

 