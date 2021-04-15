---
title: Der Komponenten Kategorien-Manager
description: Der Komponenten Kategorien-Manager
ms.assetid: bd43ef98-2299-4c8a-9f35-bf9aceb074ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fdf301e1b344bbc2403fd656dd90447ccffc357
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471220"
---
# <a name="the-component-categories-manager"></a><span data-ttu-id="b4180-103">Der Komponenten Kategorien-Manager</span><span class="sxs-lookup"><span data-stu-id="b4180-103">The Component Categories Manager</span></span>

<span data-ttu-id="b4180-104">Um die Verarbeitung von Komponenten Kategorien zu vereinfachen und die Konsistenz der Registrierung zu gewährleisten, stellt das System den Komponenten Kategorien-Manager bereit, ein COM-Objekt mit einer CLSID der CLSID \_ stdcomponentcategoriesmgr.</span><span class="sxs-lookup"><span data-stu-id="b4180-104">To facilitate the handling of component categories and to guarantee consistency of the registry, the system provides the Component Categories Manager, a COM object with a CLSID of CLSID\_StdComponentCategoriesMgr.</span></span> <span data-ttu-id="b4180-105">Dieses com-Objekt stellt die folgenden Schnittstellen bereit:</span><span class="sxs-lookup"><span data-stu-id="b4180-105">This COM object provides the following interfaces:</span></span>

-   [<span data-ttu-id="b4180-106">**Ialisierungsinformationen**</span><span class="sxs-lookup"><span data-stu-id="b4180-106">**ICatInformation**</span></span>](/windows/desktop/api/ComCat/nn-comcat-icatinformation)
-   [<span data-ttu-id="b4180-107">**I-Register**</span><span class="sxs-lookup"><span data-stu-id="b4180-107">**ICatRegister**</span></span>](/windows/desktop/api/ComCat/nn-comcat-icatregister)

<span data-ttu-id="b4180-108">[**Itorinformation**](/windows/desktop/api/ComCat/nn-comcat-icatinformation) stellt Methoden zum Abrufen von Informationen über die von einer bestimmten Klasse implementierten oder benötigten Kategorien bereit und stellt Informationen zu den auf einem bestimmten Computer registrierten Kategorien bereit.</span><span class="sxs-lookup"><span data-stu-id="b4180-108">[**ICatInformation**](/windows/desktop/api/ComCat/nn-comcat-icatinformation) provides methods for obtaining information about the categories implemented or required by a certain class and provides information about the categories registered on a given machine.</span></span>

<span data-ttu-id="b4180-109">[**Ikatregister**](/windows/desktop/api/ComCat/nn-comcat-icatregister) stellt Methoden zum Registrieren und Aufheben der Registrierung von Komponenten Kategorieinformationen in der Registrierung bereit.</span><span class="sxs-lookup"><span data-stu-id="b4180-109">[**ICatRegister**](/windows/desktop/api/ComCat/nn-comcat-icatregister) provides methods for registering and unregistering component category information in the registry.</span></span> <span data-ttu-id="b4180-110">Dies schließt sowohl die lesbaren Namen von Kategorien als auch die Kategorien ein, die von einer bestimmten Komponente oder Klasse implementiert oder benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="b4180-110">This includes both the human-readable names of categories and the categories implemented or required by a given component or class.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b4180-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b4180-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b4180-112">Zuordnen von Symbolen zu einer Kategorie</span><span class="sxs-lookup"><span data-stu-id="b4180-112">Associating Icons with a Category</span></span>](associating-icons-with-a-category.md)
</dt> <dt>

[<span data-ttu-id="b4180-113">Kategorisierung nach Komponenten Funktionen</span><span class="sxs-lookup"><span data-stu-id="b4180-113">Categorizing by Component Capabilities</span></span>](categorizing-by-component-capabilities.md)
</dt> <dt>

[<span data-ttu-id="b4180-114">Kategorisierung nach Container Funktionen</span><span class="sxs-lookup"><span data-stu-id="b4180-114">Categorizing by Container Capabilities</span></span>](categorizing-by-container-capabilities.md)
</dt> <dt>

[<span data-ttu-id="b4180-115">Standardklassen und-Zuordnungen</span><span class="sxs-lookup"><span data-stu-id="b4180-115">Default Classes and Associations</span></span>](default-classes-and-associations.md)
</dt> <dt>

[<span data-ttu-id="b4180-116">Definieren von Komponenten Kategorien</span><span class="sxs-lookup"><span data-stu-id="b4180-116">Defining Component Categories</span></span>](defining-component-categories.md)
</dt> </dl>

 

 




