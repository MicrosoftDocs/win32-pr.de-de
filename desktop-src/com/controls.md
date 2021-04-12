---
title: Steuerelemente (com)
description: Steuerelemente
ms.assetid: 73947c81-6727-4112-9da0-efa60360f458
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f440fff8f855f70c1a5ab3df78a6f6f6ed365ea
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104339997"
---
# <a name="controls-com"></a><span data-ttu-id="8975c-103">Steuerelemente (com)</span><span class="sxs-lookup"><span data-stu-id="8975c-103">Controls (COM)</span></span>

<span data-ttu-id="8975c-104">Bei einem ActiveX-Steuerelement handelt es sich in Wirklichkeit nur um einen anderen Begriff für das OLE-Objekt.</span><span class="sxs-lookup"><span data-stu-id="8975c-104">An ActiveX control is really just another term for OLE object or more specifically, COM object.</span></span> <span data-ttu-id="8975c-105">Anders ausgedrückt: ein Steuerelement ist zumindest ein COM-Objekt, das die [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) -Schnittstelle unterstützt und auch selbst registriert wird.</span><span class="sxs-lookup"><span data-stu-id="8975c-105">In other words, a control, at the very least, is some COM object that supports the [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) interface and is also self-registering.</span></span> <span data-ttu-id="8975c-106">Über [**IUnknown:: QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) kann ein Container die Gültigkeitsdauer des Steuer Elements verwalten und den vollständigen Umfang der Funktionalität eines Steuer Elements auf der Grundlage der verfügbaren Schnittstellen dynamisch ermitteln.</span><span class="sxs-lookup"><span data-stu-id="8975c-106">Through [**IUnknown::QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) a container can manage the lifetime of the control as well as dynamically discover the full extent of a control's functionality based on the available interfaces.</span></span> <span data-ttu-id="8975c-107">Dadurch kann ein Steuerelement so wenig Funktionalität implementieren, wie es benötigt, anstatt eine große Anzahl von Schnittstellen zu unterstützen, die tatsächlich nichts Unternehmen.</span><span class="sxs-lookup"><span data-stu-id="8975c-107">This allows a control to implement as little functionality as it needs to, instead of supporting a large number of interfaces that actually don't do anything.</span></span> <span data-ttu-id="8975c-108">Kurz gesagt, diese minimale Anforderung für nichts mehr als **IUnknown** ermöglicht es, dass alle Steuerelemente so einfach wie möglich sind.</span><span class="sxs-lookup"><span data-stu-id="8975c-108">In short, this minimal requirement for nothing more than **IUnknown** allows any control to be as lightweight as it can.</span></span>

<span data-ttu-id="8975c-109">Kurz gesagt, außer [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) und Selbstregistrierung gibt es keine anderen Anforderungen an ein Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="8975c-109">In short, other than [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) and self-registration, there are no other requirements for a control.</span></span> <span data-ttu-id="8975c-110">Es gibt jedoch Konventionen, die berücksichtigen sollten, was die Unterstützung einer Schnittstelle in Bezug auf Funktionen bedeutet, die für den Container durch das Steuerelement bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="8975c-110">There are, however, conventions that should be followed about what the support of an interface means in terms of functionality provided to the container by the control.</span></span> <span data-ttu-id="8975c-111">In diesem Abschnitt wird dann beschrieben, was es bedeutet, dass ein Steuerelement eine Schnittstelle unterstützt, sowie Methoden, Eigenschaften und Ereignisse, die ein Steuerelement als Baseline bereitstellen sollte, wenn es eine Gelegenheit zum unterstützen von Methoden, Eigenschaften und Ereignissen hat.</span><span class="sxs-lookup"><span data-stu-id="8975c-111">This section then describes what it means for a control to actually support an interface, as well as methods, properties, and events that a control should provide as a baseline if it has occasion to support methods, properties, and events.</span></span>

<span data-ttu-id="8975c-112">Weitere Informationen finden Sie unter den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="8975c-112">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="8975c-113">Selbstregistrierung für Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="8975c-113">Self Registration for Controls</span></span>](self-registration-for-controls.md)
-   [<span data-ttu-id="8975c-114">Was bedeutet Unterstützung für eine Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="8975c-114">What Support for an Interface Means</span></span>](what-support-for-an-interface-means.md)
-   [<span data-ttu-id="8975c-115">Persistenzschnittstellen</span><span class="sxs-lookup"><span data-stu-id="8975c-115">Persistence Interfaces</span></span>](persistence-interfaces.md)
-   [<span data-ttu-id="8975c-116">Optionale Methoden in Steuerungs Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="8975c-116">Optional Methods in Control Interfaces</span></span>](optional-methods-in-control-interfaces.md)
-   [<span data-ttu-id="8975c-117">Class Factory-Optionen</span><span class="sxs-lookup"><span data-stu-id="8975c-117">Class Factory Options</span></span>](class-factory-options.md)
-   [<span data-ttu-id="8975c-118">Verfügbar machen von Eigenschaften über IDispatch</span><span class="sxs-lookup"><span data-stu-id="8975c-118">Exposing Properties through IDispatch</span></span>](properties.md)
-   [<span data-ttu-id="8975c-119">Verfügbar machen von Methoden über IDispatch</span><span class="sxs-lookup"><span data-stu-id="8975c-119">Exposing Methods through IDispatch</span></span>](exposing-methods-through-idispatch.md)
-   [<span data-ttu-id="8975c-120">Ereignisse in Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="8975c-120">Events in Controls</span></span>](events-in-controls.md)
-   [<span data-ttu-id="8975c-121">Eigenschaftenseiten</span><span class="sxs-lookup"><span data-stu-id="8975c-121">Property Pages</span></span>](property-pages.md)
-   [<span data-ttu-id="8975c-122">Ambient-Eigenschaften für Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="8975c-122">Ambient Properties for Controls</span></span>](ambient-properties-for-controls.md)
-   [<span data-ttu-id="8975c-123">Verwenden der Container-Funktionalität</span><span class="sxs-lookup"><span data-stu-id="8975c-123">Using the Container's Functionality</span></span>](using-the-container-s-functionality.md)

## <a name="related-topics"></a><span data-ttu-id="8975c-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8975c-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8975c-125">ActiveX-Steuerelement-und Steuerelement Container</span><span class="sxs-lookup"><span data-stu-id="8975c-125">ActiveX Control and Control Container Guidelines</span></span>](activex-control-and-control-container-guidelines.md)
</dt> </dl>

 

 




