---
title: Sammlungen und Gruppen
description: ADSI verwendet Sammlungsobjekte, um beliebige beliebige Elemente in einem Verzeichnisdienst darzustellen, die mit demselben Datentyp dargestellt werden können.
ms.assetid: 03257cc9-f354-4e1c-8880-936a7acac3ef
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, using, Collections und Groups
- Sammlungen ADSI
- Gruppen-ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9f0f4d699d8dde0c3d70c7449dfe146212b2b30
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103949101"
---
# <a name="collections-and-groups"></a><span data-ttu-id="bc11f-106">Sammlungen und Gruppen</span><span class="sxs-lookup"><span data-stu-id="bc11f-106">Collections and Groups</span></span>

<span data-ttu-id="bc11f-107">ADSI verwendet Sammlungsobjekte, um beliebige beliebige Elemente in einem Verzeichnisdienst darzustellen, die mit demselben Datentyp dargestellt werden können.</span><span class="sxs-lookup"><span data-stu-id="bc11f-107">ADSI uses collection objects to represent any arbitrary set of items in a directory service that can be represented using the same data type.</span></span> <span data-ttu-id="bc11f-108">Sammlungsobjekte werden als eine Reihe von **Variant** -Werten definiert, die einen der gültigen Automatisierungs Datentypen darstellen.</span><span class="sxs-lookup"><span data-stu-id="bc11f-108">Collection objects are defined as a set of **VARIANT** values, representing any of the valid Automation data types.</span></span> <span data-ttu-id="bc11f-109">Auflistungs Objekte können permanente Informationen darstellen, z. b. Zugriffs Steuerungs Listen und flüchtige Informationen, wie z. b. Druckaufträge in einer Druck Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="bc11f-109">Collection objects can represent both persistent information such as access-control lists and volatile information such as print jobs in a print queue.</span></span>

<span data-ttu-id="bc11f-110">Die com-Standard Konvention zum Auflisten des Inhalts eines Auflistungs Objekts (oder eines Container Objekts) besteht darin, ein Enumeratorobjekt zu erstellen, das [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant)unterstützt, das über Methoden zum Durchlaufen der Liste der Auflistungs Objekte verfügt.</span><span class="sxs-lookup"><span data-stu-id="bc11f-110">The standard COM convention for listing the contents of a collection (or container) object is to create an enumerator object that supports [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant), which has methods to step through the list of collection objects.</span></span> <span data-ttu-id="bc11f-111">Die Schnittstellen in ADSI, die die **get \_ \_ NewEnum** -Methode bereitstellen (Beachten Sie die zwei Unterstriche), sind [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer), [**iadsmembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers) und [**iadscollection**](/windows/desktop/api/Iads/nn-iads-iadscollection).</span><span class="sxs-lookup"><span data-stu-id="bc11f-111">The interfaces in ADSI that supply the **get\_\_NewEnum** method (note the two underscores) are [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer), [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers) and [**IADsCollection**](/windows/desktop/api/Iads/nn-iads-iadscollection).</span></span> <span data-ttu-id="bc11f-112">ADSI stellt außerdem die Hilfsfunktionen [**ADsBuildEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator) und [**adsenumeratenext**](/windows/desktop/api/Adshlp/nf-adshlp-adsenumeratenext) für C-und C++-Programme bereit, um die Enumeration zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="bc11f-112">ADSI also supplies the helper functions [**ADsBuildEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator) and [**ADsEnumerateNext**](/windows/desktop/api/Adshlp/nf-adshlp-adsenumeratenext) for C and C++ programs to simplify enumeration.</span></span> <span data-ttu-id="bc11f-113">Automatisierungs Clients verwenden implizit eine Enumeration, wenn **Sie in** einer **for** -Schleife aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="bc11f-113">Automation clients use enumeration implicitly when they call **Next** in a **For** loop.</span></span>

<span data-ttu-id="bc11f-114">Gruppen sind einfach Sammlungen von Objekten, die die [**iadsmembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers) -Schnittstelle unterstützen.</span><span class="sxs-lookup"><span data-stu-id="bc11f-114">Groups are simply collections of objects supporting the [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers) interface.</span></span>

 

 