---
title: Kategorisierung nach Komponenten Funktionen
description: Komponenten Kategorien können verwendet werden, um eine Teilmenge aller installierten Komponenten anzuzeigen.
ms.assetid: 522af5d7-ba7b-4127-9cdb-48ef4d0f8e65
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff44e03e9eae0226ac57279c37d4a5dfd32fc6bd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341434"
---
# <a name="categorizing-by-component-capabilities"></a><span data-ttu-id="531db-103">Kategorisierung nach Komponenten Funktionen</span><span class="sxs-lookup"><span data-stu-id="531db-103">Categorizing by Component Capabilities</span></span>

<span data-ttu-id="531db-104">Komponenten Kategorien können verwendet werden, um eine Teilmenge aller installierten Komponenten anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="531db-104">Component categories can be used to display a subset of all of the installed components.</span></span> <span data-ttu-id="531db-105">Jede Komponenten Kategorie wird durch eine GUID identifiziert, die als Kategorie-ID (CATID) bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="531db-105">Each component category is identified by a GUID, referred to as a Category ID (CATID).</span></span> <span data-ttu-id="531db-106">Jede CATID verfügt über eine Liste von mit dem Gebiets Schema markierten, lesbaren Namen.</span><span class="sxs-lookup"><span data-stu-id="531db-106">Each CATID has a list of locale-tagged, human-readable names associated with it.</span></span> <span data-ttu-id="531db-107">Eine Auflistung der CATIDs und der lesbaren Namen wird an einem bekannten Speicherort in der Registrierung gespeichert.</span><span class="sxs-lookup"><span data-stu-id="531db-107">A listing of the CATIDs and the human-readable names is stored in a well-known location in the registry.</span></span>

<span data-ttu-id="531db-108">Beispielsweise können alle Komponenten, die die Funktionalität für die Einbettung von OLE-Dokumenten implementieren, in einer Komponenten Kategorie klassifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="531db-108">For example, all components that implement the functionality for OLE document embedding can be classified within a component category.</span></span> <span data-ttu-id="531db-109">In der Vergangenheit wurden diese Objekte durch den Schlüssel "Insertable" in der Registrierung identifiziert.</span><span class="sxs-lookup"><span data-stu-id="531db-109">In the past, these objects would have been identified by the "Insertable" key in the registry.</span></span> <span data-ttu-id="531db-110">Um stattdessen Komponenten Kategorien zu verwenden, werden der Registrierung die folgenden Informationen hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="531db-110">To use component categories instead, the following information would be added to the registry:</span></span>

```
HKEY_CLASSES_ROOT\Component Categories\{40FC6ED3-2438-11cf-A3DB-080036F12502}
   (Default) = ""
   409 = "Embeddable Objects"
```

<span data-ttu-id="531db-111">Jede Klasse, die die Funktionalität implementiert, die einer Komponenten Kategorie entspricht, listet die Kategorie-ID für diese Kategorie innerhalb des CLSID-Schlüssels in der Registrierung auf.</span><span class="sxs-lookup"><span data-stu-id="531db-111">Each class that implements the functionality corresponding to a component category lists the category ID for that category within the CLSID key in the registry.</span></span> <span data-ttu-id="531db-112">Da eine einzelne Komponente eine große Bandbreite von Funktionen unterstützen kann, können Komponenten mehreren Komponenten Kategorien angehören.</span><span class="sxs-lookup"><span data-stu-id="531db-112">Because a single component can support a wide range of functionality, components can belong to multiple component categories.</span></span> <span data-ttu-id="531db-113">Beispielsweise kann ein bestimmtes OLE-Steuerelement sämtliche Funktionen unterstützen, die für die Teilnahme als OLE-Dokument Einbettung, Microsoft Visual Basic-Datenbindung und Internet Funktionalität erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="531db-113">For example, a particular OLE control might support all of the functionality required to participate as OLE document embedding, Microsoft Visual Basic data binding, and Internet functionality.</span></span> <span data-ttu-id="531db-114">Für ein solches Steuerelement sind die folgenden Informationen im CLSID-Schlüssel in der Registrierung gespeichert:</span><span class="sxs-lookup"><span data-stu-id="531db-114">Such a control would have the following information stored in its CLSID key in the registry:</span></span>

``` syntax
;The CLSID for "My Super OLE Control" is {12345678-ABCD-4321-0101-00000000000C}HKEY_CLASSES_ROOT\CLSID\{12345678-ABCD-4321-0101-00000000000C}\Implemented Categories
;The CATID for "Insertable" is {40FC6ED3-2438-11cf-A3DB-080036F12502} HKEY_CLASSES_ROOT\CLSID\{12345678-ABCD-4321-0101-00000000000C}Implemented Categories\{40FC6ED3-2438-11cf-A3DB-080036F12502}
;The CATID for "Control" is {40FC6ED4-2438-11cf-A3DB-080036F12502} HKEY_CLASSES_ROOT\CLSID\{12345678-ABCD-4321-0101-00000000000C}Implemented Categories\{40FC6ED4-2438-11cf-A3DB-080036F12502}
;The CATID for an internet aware control is {...CATID_InternetAware...} HKEY_CLASSES_ROOT\CLSID\{12345678-ABCD-4321-0101-00000000000C}Implemented Categories\{...CATID_InternetAware...}
 
```

<span data-ttu-id="531db-115">Mit diesen Informationen kann ein Container die auf einem System installierten Steuerelemente auflisten und nur die Steuerelemente anzeigen, die die für den Container erforderliche Funktionalität unterstützen.</span><span class="sxs-lookup"><span data-stu-id="531db-115">With this information, a container can enumerate the controls installed on a system and display only those controls that support the functionality required by the container.</span></span> <span data-ttu-id="531db-116">Die Verwendung von Komponenten Kategorien bietet eine Möglichkeit, Komponenten nach den implementierten Funktionen der Komponente zu kategorisieren.</span><span class="sxs-lookup"><span data-stu-id="531db-116">The use of component categories provides a way to categorize components by the implemented functionality of the component.</span></span>

## <a name="related-topics"></a><span data-ttu-id="531db-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="531db-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="531db-118">Zuordnen von Symbolen zu einer Kategorie</span><span class="sxs-lookup"><span data-stu-id="531db-118">Associating Icons with a Category</span></span>](associating-icons-with-a-category.md)
</dt> <dt>

[<span data-ttu-id="531db-119">Kategorisierung nach Container Funktionen</span><span class="sxs-lookup"><span data-stu-id="531db-119">Categorizing by Container Capabilities</span></span>](categorizing-by-container-capabilities.md)
</dt> <dt>

[<span data-ttu-id="531db-120">Standardklassen und-Zuordnungen</span><span class="sxs-lookup"><span data-stu-id="531db-120">Default Classes and Associations</span></span>](default-classes-and-associations.md)
</dt> <dt>

[<span data-ttu-id="531db-121">Definieren von Komponenten Kategorien</span><span class="sxs-lookup"><span data-stu-id="531db-121">Defining Component Categories</span></span>](defining-component-categories.md)
</dt> <dt>

[<span data-ttu-id="531db-122">Der Komponenten Kategorien-Manager</span><span class="sxs-lookup"><span data-stu-id="531db-122">The Component Categories Manager</span></span>](the-component-categories-manager.md)
</dt> </dl>

 

 




