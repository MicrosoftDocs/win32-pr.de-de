---
title: Kategorisierung nach Container Funktionen
description: Komponenten erfordern häufig bestimmte Funktionen aus dem Container und funktionieren nicht mit einem Container, der keine Unterstützung bietet.
ms.assetid: 11002f3e-17de-4e05-a2df-0c9e6326846d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 987546c20ff77a40666bb74689466a15fab989a6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037530"
---
# <a name="categorizing-by-container-capabilities"></a><span data-ttu-id="a6736-103">Kategorisierung nach Container Funktionen</span><span class="sxs-lookup"><span data-stu-id="a6736-103">Categorizing by Container Capabilities</span></span>

<span data-ttu-id="a6736-104">Komponenten erfordern häufig bestimmte Funktionen aus dem Container und funktionieren nicht mit einem Container, der keine Unterstützung bietet.</span><span class="sxs-lookup"><span data-stu-id="a6736-104">Components often require certain functionality from the container and will not work with a container that does not provide the support.</span></span> <span data-ttu-id="a6736-105">Die Benutzeroberfläche sollte Komponenten herausfiltern, die Funktionen erfordern, die der Container nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a6736-105">The user interface should filter out components that require functionality the container does not support.</span></span> <span data-ttu-id="a6736-106">Um dies zu erreichen, können Komponenten nach den erforderlichen Container Funktionen kategorisiert werden.</span><span class="sxs-lookup"><span data-stu-id="a6736-106">To accomplish this, components can be categorized by the required container functionality.</span></span>

<span data-ttu-id="a6736-107">Ein Beispiel für Komponenten, die Funktionen aus dem Container erfordern und nicht in Containern funktionieren, die diese Funktionalität nicht unterstützen, sind einfache Frame-OLE-Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="a6736-107">An example of components that require functionality from the container and do not work in containers that do not support that functionality are simple frame OLE controls.</span></span> <span data-ttu-id="a6736-108">Die Kategorisierung nach Container Funktionen erfolgt durch einen zusätzlichen Registrierungsschlüssel innerhalb des CLSID-Schlüssels der Komponente:</span><span class="sxs-lookup"><span data-stu-id="a6736-108">Categorizing by container capabilities is accomplished by an additional registry key within the component's CLSID key:</span></span>

``` syntax
;The CLSID for "Simple Frame Control" is {123456FF-ABCD-4321-0101-00000000000C}HKEY_CASSES_ROOT\CLSID\{12346FF-ABCD-4321-0101-00000000000C}\Implemented Categories
;The CATID for "Control" is {40FC6ED4-2438-11cf-A3DB-080036F12502} HKEY_CLASSES_ROOT\CLSID\{123456FF-ABCD-4321-0101-00000000000C}Implemented Categories\{40FC6ED4-2438-11cf-A3DB-080036F12502}
;The CATID for simple frame controls is {...CATID_SimpleFrameControl...} HKEY_CLASSES_ROOT\CLSID\{123456FF-ABCD-4321-0101-00000000000C}Implemented Categories\{...CATID_SimpleFrameControl...}
HKEY_CLASSES_ROOT\CLSID\{123456FF-ABCD-4321-0101-00000000000C}Required Categories\{...CATID_SimpleFrameControl...}
 
```

<span data-ttu-id="a6736-109">Wie in diesem Beispiel gezeigt, kann eine Komponente zu Komponenten Kategorien gehören, die auf unterstützte Funktionen hinweisen, sowie auf Komponenten Kategorien, die die erforderliche Funktionalität angeben.</span><span class="sxs-lookup"><span data-stu-id="a6736-109">As shown in this example, a component can belong to component categories that indicate supported functionality as well as to component categories that indicate required functionality.</span></span>

<span data-ttu-id="a6736-110">Im folgenden Beispiel ist das Schaltflächen-Steuerelement ein generisches OLE-Steuerelement, das keine zusätzliche Funktionalität unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a6736-110">In the following example, the button control is a generic OLE control that supports no additional functionality.</span></span> <span data-ttu-id="a6736-111">Es funktioniert in jedem OLE-Steuerelement Container.</span><span class="sxs-lookup"><span data-stu-id="a6736-111">It will work in any OLE control container.</span></span>

``` syntax
HKEY_CLASSES_ROOT\CLSID\{...CLSID_Button...}\Implemented Categories
HKEY_CLASSES_ROOT\CLSID\{...CLSID_Button...}\Implemented Categories\{...CATID_Control...}
 
```

<span data-ttu-id="a6736-112">Vergleichen Sie das vorangehende Beispiel mit dem nächsten Beispiel, in dem mydbcontrol Visual Basic Datenbindung verwenden kann, wenn es vom Container unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="a6736-112">Compare the preceding example with the next example in which the MyDBControl can use Visual Basic data binding if the container supports it.</span></span> <span data-ttu-id="a6736-113">Sie wurde jedoch so definiert, dass Sie in Containern funktioniert, die keine Visual Basic Datenbindung unterstützen (möglicherweise durch eine andere Datenbank-API):</span><span class="sxs-lookup"><span data-stu-id="a6736-113">However, it has been defined so that it will work in containers that do not support Visual Basic data binding (perhaps by a different database API):</span></span>

``` syntax
HKEY_CLASSES_ROOT\CLSID\{...CLSID_MyDBControl...}\Implemented Categories
HKEY_CLASSES_ROOT\CLSID\{...CLSID_MyDBControl...}\Implemented Categories\{...CATID_Control...}
HKEY_CLASSES_ROOT\CLSID\{...CLSID_MyDBControl...}\Implemented Categories\{...CATID_VBDatabound...}
 
```

<span data-ttu-id="a6736-114">Das GroupBox-Steuerelement ist ein einfaches Frame-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="a6736-114">The GroupBox control is a simple frame control.</span></span> <span data-ttu-id="a6736-115">Er basiert auf dem Container, der die [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) -Schnittstelle implementiert, und funktioniert nur in solchen Containern ordnungsgemäß:</span><span class="sxs-lookup"><span data-stu-id="a6736-115">It relies on the container implementing the [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) interface and will work correctly only in such containers:</span></span>

``` syntax
HKEY_CLASSES_ROOT\CLSID\{...CLSID_GroupBox...}\Implemented Categories
HKEY_CLASSES_ROOT\CLSID\{...CLSID_GroupBox...}\Implemented Categories\{...CATID_Control...}
HKEY_CLASSES_ROOT\CLSID\{...CLSID_GroupBox...}\Implemented Categories\{...CATID_SimpleFrame...}
HKEY_CLASSES_ROOT\CLSID\{...CLSID_GroupBox...}\Required Categories\{...CATID_SimpleFrame...}
 
```

<span data-ttu-id="a6736-116">Ein Container, der Visual Basic Daten gebundene Steuerelemente unterstützt, aber keine einfachen Frame Steuerelemente unterstützt, würde das CATID- \_ Steuerelement und CATID \_ vbdatbound an die Benutzeroberfläche des einfügesteuerelements</span><span class="sxs-lookup"><span data-stu-id="a6736-116">A container that supports Visual Basic data bound controls but does not support simple frame controls would specify CATID\_Control and CATID\_VBDatabound to the insert control user interface.</span></span> <span data-ttu-id="a6736-117">Die Liste der Steuerelemente, die dem Benutzer angezeigt werden, enthält die CLSID \_ -Schaltfläche und die CLSID \_ mydbcontrol.</span><span class="sxs-lookup"><span data-stu-id="a6736-117">The list of controls displayed to the user would contain the CLSID\_Button and CLSID\_MyDBControl.</span></span> <span data-ttu-id="a6736-118">Die CLSID- \_ GroupBox wird nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a6736-118">CLSID\_GroupBox would not be displayed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a6736-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a6736-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a6736-120">Zuordnen von Symbolen zu einer Kategorie</span><span class="sxs-lookup"><span data-stu-id="a6736-120">Associating Icons with a Category</span></span>](associating-icons-with-a-category.md)
</dt> <dt>

[<span data-ttu-id="a6736-121">Kategorisierung nach Komponenten Funktionen</span><span class="sxs-lookup"><span data-stu-id="a6736-121">Categorizing by Component Capabilities</span></span>](categorizing-by-component-capabilities.md)
</dt> <dt>

[<span data-ttu-id="a6736-122">Standardklassen und-Zuordnungen</span><span class="sxs-lookup"><span data-stu-id="a6736-122">Default Classes and Associations</span></span>](default-classes-and-associations.md)
</dt> <dt>

[<span data-ttu-id="a6736-123">Definieren von Komponenten Kategorien</span><span class="sxs-lookup"><span data-stu-id="a6736-123">Defining Component Categories</span></span>](defining-component-categories.md)
</dt> <dt>

[<span data-ttu-id="a6736-124">Der Komponenten Kategorien-Manager</span><span class="sxs-lookup"><span data-stu-id="a6736-124">The Component Categories Manager</span></span>](the-component-categories-manager.md)
</dt> </dl>

 

 




