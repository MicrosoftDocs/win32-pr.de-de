---
title: Überlegungen zur IPropertySetStorage-Implementierung
description: Wenn Sie erwägen, eine Implementierung der IPropertySetStorage-Schnittstelle bereitzustellen, die das com-Eigenschaften Satz Format liest und schreibt, werden mehrere Probleme auftreten. Dies wird in den folgenden Abschnitten beschrieben.
ms.assetid: 055da516-ed42-49ec-b20c-a5e98718bea8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f7532211668fa1ecf290484a707b19e1c263b9d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712738"
---
# <a name="ipropertysetstorage-implementation-considerations"></a><span data-ttu-id="53ea2-104">Überlegungen zur IPropertySetStorage-Implementierung</span><span class="sxs-lookup"><span data-stu-id="53ea2-104">IPropertySetStorage Implementation Considerations</span></span>

<span data-ttu-id="53ea2-105">Wenn Sie erwägen, eine Implementierung der [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) -Schnittstelle bereitzustellen, die das com-Eigenschaften Satz Format liest und schreibt, werden mehrere Probleme auftreten.</span><span class="sxs-lookup"><span data-stu-id="53ea2-105">Several issues arise when considering how to provide an implementation of the [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) interface that reads and writes the COM property set format.</span></span> <span data-ttu-id="53ea2-106">Dies wird in den folgenden Abschnitten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="53ea2-106">The following sections describe these considerations.</span></span>

-   [<span data-ttu-id="53ea2-107">Namen in IStorage</span><span class="sxs-lookup"><span data-stu-id="53ea2-107">Names in IStorage</span></span>](names-in-istorage.md)
-   [<span data-ttu-id="53ea2-108">Speicher-und Streamobjekte für einen Eigenschaften Satz</span><span class="sxs-lookup"><span data-stu-id="53ea2-108">Storage and Stream Objects for a Property Set</span></span>](storage-vs--stream-for-a-property-set.md)
-   [<span data-ttu-id="53ea2-109">Festlegen des Eigenschafts Satz-Klassen Bezeichners</span><span class="sxs-lookup"><span data-stu-id="53ea2-109">Setting the Property Set Class Identifier</span></span>](setting-the-property-set-class-identifier.md)
-   [<span data-ttu-id="53ea2-110">Synchronisierungs Punkte</span><span class="sxs-lookup"><span data-stu-id="53ea2-110">Synchronization Points</span></span>](synchronization-points.md)
-   [<span data-ttu-id="53ea2-111">Codepages und Unicode-Zeichen folgen</span><span class="sxs-lookup"><span data-stu-id="53ea2-111">Code Pages and Unicode Strings</span></span>](code-pages-and-unicode-strings.md)
-   [<span data-ttu-id="53ea2-112">Wörterbuch</span><span class="sxs-lookup"><span data-stu-id="53ea2-112">Dictionary</span></span>](dictionary.md)
-   [<span data-ttu-id="53ea2-113">Extensions (Erweiterungen)</span><span class="sxs-lookup"><span data-stu-id="53ea2-113">Extensions</span></span>](extensions.md)
-   [<span data-ttu-id="53ea2-114">Eigenschaftensetserialisierung</span><span class="sxs-lookup"><span data-stu-id="53ea2-114">Property Set Serialization</span></span>](version-0-vs--version-1-property-set-serialization.md)

<span data-ttu-id="53ea2-115">Weitere Informationen finden Sie unter " [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) " im Abschnitt "Referenz" unter "Schnittstellen".</span><span class="sxs-lookup"><span data-stu-id="53ea2-115">For more information, see [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) in the Reference section under Interfaces.</span></span>

 

 




