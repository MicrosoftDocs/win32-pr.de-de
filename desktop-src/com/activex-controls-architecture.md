---
title: ActiveX-Steuerelement Architektur
description: ActiveX-Steuerelemente bauen auf einer Grundlage von vielen Objekten auf niedrigerer Ebene und Schnittstellen in OLE auf. Die exakten Schnittstellen, die in einem Steuerelement verfügbar sind, variieren je nach Funktionalität. In diesem Abschnitt werden die Funktionen, die ein Steuerelement möglicherweise bereitstellt, näher betrachtet.
ms.assetid: 42959a11-8bfb-4f7e-ba27-5dc1ed49cdaa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d0592d774e1930623803d0769fb7890709a2f21
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709552"
---
# <a name="activex-controls-architecture"></a><span data-ttu-id="c5413-105">ActiveX-Steuerelement Architektur</span><span class="sxs-lookup"><span data-stu-id="c5413-105">ActiveX Controls Architecture</span></span>

<span data-ttu-id="c5413-106">ActiveX-Steuerelemente bauen auf einer Grundlage von vielen Objekten auf niedrigerer Ebene und Schnittstellen in OLE auf.</span><span class="sxs-lookup"><span data-stu-id="c5413-106">ActiveX controls technology builds on a foundation of many lower-level objects and interfaces in OLE.</span></span> <span data-ttu-id="c5413-107">Die exakten Schnittstellen, die in einem Steuerelement verfügbar sind, variieren je nach Funktionalität.</span><span class="sxs-lookup"><span data-stu-id="c5413-107">The exact interfaces available on a control vary with its capabilities.</span></span> <span data-ttu-id="c5413-108">In diesem Abschnitt werden die Funktionen, die ein Steuerelement möglicherweise bereitstellt, näher betrachtet.</span><span class="sxs-lookup"><span data-stu-id="c5413-108">This section takes a closer look at the capabilities a control might provide.</span></span>

<span data-ttu-id="c5413-109">ActiveX-Steuerelemente werden verwendet, um die Bausteine zum Erstellen von Benutzeroberflächen in Anwendungen bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="c5413-109">ActiveX controls are used to provide the building blocks for creating user interfaces in applications.</span></span> <span data-ttu-id="c5413-110">Beispielsweise ist eine Schaltfläche, die eine Aktion in der Containeranwendung initiiert, wenn darauf geklickt wird, ein einfaches Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="c5413-110">For example, a button that initiates some action in the container application when it is clicked is a simple control.</span></span> <span data-ttu-id="c5413-111">Die folgenden Aspekte sind an der Bereitstellung dieser Benutzeroberflächen Bausteine beteiligt:</span><span class="sxs-lookup"><span data-stu-id="c5413-111">The following aspects are involved in providing these user interface building blocks:</span></span>

-   <span data-ttu-id="c5413-112">Ein-Steuerelement kann in seinen Container Client eingebettet werden, um Benutzeroberflächen Aktivitäten innerhalb des Clients zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="c5413-112">A control can be embedded within its container client to support some user interface activity within the client.</span></span> <span data-ttu-id="c5413-113">Folglich muss ein Steuerelement eine visuelle Darstellung von sich selbst bereitstellen, wenn es in den Container eingebettet ist und eine Möglichkeit bieten muss, seinen Zustand zu speichern, z. b. seine Eigenschaftswerte und seine Position innerhalb des Containers.</span><span class="sxs-lookup"><span data-stu-id="c5413-113">Thus, a control needs to provide a visual representation of itself when it is embedded within the container and needs to provide a way to save its state, for example, its property values and its position within its container.</span></span> <span data-ttu-id="c5413-114">Der Client muss die Verwendung eines Containers mit eingebetteten Objekten unterstützen.</span><span class="sxs-lookup"><span data-stu-id="c5413-114">The client must support being a container with objects embedded in it.</span></span>
-   <span data-ttu-id="c5413-115">Wenn Sie das Steuerelement mit einer Tastatur oder Maus aktivieren, initiiert der Endbenutzer eine Aktion in der Client Anwendung.</span><span class="sxs-lookup"><span data-stu-id="c5413-115">By activating the control using a keyboard or mouse, the end user initiates some action in the client application.</span></span> <span data-ttu-id="c5413-116">Folglich muss ein Steuerelement auf die Tastatur Aktivität reagieren und in der Lage sein, mit seinem Client zu kommunizieren, damit er den Container seiner Aktivitäten benachrichtigen und Ereignisse im Client auslöst.</span><span class="sxs-lookup"><span data-stu-id="c5413-116">Thus, a control must respond to keyboard activity and must be able to communicate with its client so it can notify its container of its activities and trigger events in the client.</span></span>
-   <span data-ttu-id="c5413-117">Der Client stellt in der Regel auch eine Programmiersprache bereit, über die der Endbenutzer Aktionen initiieren kann, die von den Eigenschaften und Methoden des Steuer Elements bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="c5413-117">The client also typically provides a programming language through which the end user can initiate actions provided by the control's properties and methods.</span></span> <span data-ttu-id="c5413-118">Folglich muss ein Steuerelement Automation und eine Reihe von Entwurfszeit-und Lauf Zeit Features unterstützen.</span><span class="sxs-lookup"><span data-stu-id="c5413-118">Thus, a control must support automation and some set of design-time versus run-time features as well.</span></span>

<span data-ttu-id="c5413-119">Aufgrund der Rolle beim Bereitstellen von Benutzeroberflächen Bausteinen unterstützt ein Steuerelement in der Regel Features in den folgenden Bereichen mithilfe von OLE-Technologien, wie hier gezeigt:</span><span class="sxs-lookup"><span data-stu-id="c5413-119">As a result of its role in providing user interface building blocks, a control typically supports features in the following areas using OLE technologies as indicated:</span></span>

<dl> <dt>

<span data-ttu-id="c5413-120"><span id="Properties_and_methods"></span><span id="properties_and_methods"></span><span id="PROPERTIES_AND_METHODS"></span>Eigenschaften und Methoden</span><span class="sxs-lookup"><span data-stu-id="c5413-120"><span id="Properties_and_methods"></span><span id="properties_and_methods"></span><span id="PROPERTIES_AND_METHODS"></span>Properties and methods</span></span>
</dt> <dd>

<span data-ttu-id="c5413-121">Wie jedes OLE-Objekt kann ein Steuerelement einen Großteil seiner Funktionen über einen Satz eingehender Schnittstellen mit Eigenschaften und Methoden bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="c5413-121">Like any OLE object, a control can provide much of its functionality through a set of incoming interfaces with properties and methods.</span></span> <span data-ttu-id="c5413-122">Der Container kann zusätzliche Ambient-Eigenschaften bereitstellen, und er kann die Erweiterung der Eigenschaften des Steuer Elements durch Aggregation unterstützen.</span><span class="sxs-lookup"><span data-stu-id="c5413-122">The container can supply additional ambient properties, and it can support extending the control's properties through aggregation.</span></span> <span data-ttu-id="c5413-123">Diese Features verbleibenden sich auf OLE-Automatisierung, Eigenschaften Seiten, Verbindungs fähige Objekte und ActiveX-Steuerelement Technologien.</span><span class="sxs-lookup"><span data-stu-id="c5413-123">These features rest on OLE automation, property pages, connectable objects, and ActiveX control technologies.</span></span>

</dd> <dt>

<span data-ttu-id="c5413-124"><span id="Events"></span><span id="events"></span><span id="EVENTS"></span>Fall</span><span class="sxs-lookup"><span data-stu-id="c5413-124"><span id="Events"></span><span id="events"></span><span id="EVENTS"></span>Events</span></span>
</dt> <dd>

<span data-ttu-id="c5413-125">Zusätzlich zur Bereitstellung von Eigenschaften und Methoden kann ein ActiveX-Steuerelement auch ausgehende Schnittstellen bereitstellen, um den Client über Ereignisse zu benachrichtigen.</span><span class="sxs-lookup"><span data-stu-id="c5413-125">In addition to providing properties and methods, an ActiveX control can also provide outgoing interfaces to notify its client of events.</span></span> <span data-ttu-id="c5413-126">Der Client muss die Behandlung dieser Ereignisse unterstützen.</span><span class="sxs-lookup"><span data-stu-id="c5413-126">The client must support handling of these events.</span></span> <span data-ttu-id="c5413-127">Diese Features verwenden OLE-Automatisierung und Verbindungs fähige Objekte.</span><span class="sxs-lookup"><span data-stu-id="c5413-127">These features use OLE automation and connectable objects.</span></span>

</dd> <dt>

<span data-ttu-id="c5413-128"><span id="Visual_representation"></span><span id="visual_representation"></span><span id="VISUAL_REPRESENTATION"></span>Visuelle Darstellung</span><span class="sxs-lookup"><span data-stu-id="c5413-128"><span id="Visual_representation"></span><span id="visual_representation"></span><span id="VISUAL_REPRESENTATION"></span>Visual representation</span></span>
</dt> <dd>

<span data-ttu-id="c5413-129">Ein Steuerelement kann die Positionierung und Anzeige innerhalb des Containers unterstützen.</span><span class="sxs-lookup"><span data-stu-id="c5413-129">A control can support positioning and displaying itself within its container.</span></span> <span data-ttu-id="c5413-130">Der Container positioniert das Steuerelement und bestimmt seine Größe.</span><span class="sxs-lookup"><span data-stu-id="c5413-130">The container positions the control and determines its size.</span></span> <span data-ttu-id="c5413-131">Diese Features verwenden Verbund Dokument Technologie, einschließlich OLE-Drag & Drop-Technologie.</span><span class="sxs-lookup"><span data-stu-id="c5413-131">These features use compound document technology, including OLE drag and drop technology.</span></span>

</dd> <dt>

<span data-ttu-id="c5413-132"><span id="Keyboard_handling"></span><span id="keyboard_handling"></span><span id="KEYBOARD_HANDLING"></span>Tastatur Behandlung</span><span class="sxs-lookup"><span data-stu-id="c5413-132"><span id="Keyboard_handling"></span><span id="keyboard_handling"></span><span id="KEYBOARD_HANDLING"></span>Keyboard handling</span></span>
</dt> <dd>

<span data-ttu-id="c5413-133">Ein Steuerelement kann auf Tastaturbeschleuniger reagieren, sodass der Endbenutzer Aktionen initiieren kann, die vom Steuerelement ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="c5413-133">A control can respond to keyboard accelerators so the end-user can initiate actions performed by the control.</span></span> <span data-ttu-id="c5413-134">Der Container verwaltet die Tastatur Aktivität für alle eingebetteten Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="c5413-134">The container manages keyboard activity for all its embedded controls.</span></span> <span data-ttu-id="c5413-135">Diese Features verwenden Steuerungs-und Verbund Dokument Technologien.</span><span class="sxs-lookup"><span data-stu-id="c5413-135">These features use control and compound document technologies.</span></span>

</dd> <dt>

<span data-ttu-id="c5413-136"><span id="Persistence"></span><span id="persistence"></span><span id="PERSISTENCE"></span>Persistenz</span><span class="sxs-lookup"><span data-stu-id="c5413-136"><span id="Persistence"></span><span id="persistence"></span><span id="PERSISTENCE"></span>Persistence</span></span>
</dt> <dd>

<span data-ttu-id="c5413-137">Ein Steuerelement kann seinen Zustand speichern.</span><span class="sxs-lookup"><span data-stu-id="c5413-137">A control can save its state.</span></span> <span data-ttu-id="c5413-138">Der Client verwaltet die Persistenz der eingebetteten Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="c5413-138">The client manages the persistence of its embedded controls.</span></span> <span data-ttu-id="c5413-139">Diese Features verwenden strukturierte Speicher-und objektpersistenztechnologien.</span><span class="sxs-lookup"><span data-stu-id="c5413-139">These features use structured storage and object persistence technologies.</span></span>

</dd> <dt>

<span data-ttu-id="c5413-140"><span id="Registration_and_licensing"></span><span id="registration_and_licensing"></span><span id="REGISTRATION_AND_LICENSING"></span>Registrierung und Lizenzierung</span><span class="sxs-lookup"><span data-stu-id="c5413-140"><span id="Registration_and_licensing"></span><span id="registration_and_licensing"></span><span id="REGISTRATION_AND_LICENSING"></span>Registration and licensing</span></span>
</dt> <dd>

<span data-ttu-id="c5413-141">Ein Steuerelement unterstützt in der Regel die Selbstregistrierung und erstellt einen Satz von Registrierungs Einträgen, wenn er instanziiert wird.</span><span class="sxs-lookup"><span data-stu-id="c5413-141">A control typically supports self-registration and creates a set of registry entries when it is instantiated.</span></span> <span data-ttu-id="c5413-142">Ein Steuerelement kann auch lizenziert werden, um eine unbefugte Verwendung zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="c5413-142">A control can also be licensed to help prevent unauthorized use.</span></span>

</dd> </dl>

<span data-ttu-id="c5413-143">Die meisten dieser Features umfassen sowohl das-Steuerelement als auch den Client Container.</span><span class="sxs-lookup"><span data-stu-id="c5413-143">Most of these features involve both the control and its client container.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c5413-144">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c5413-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c5413-145">ActiveX-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="c5413-145">ActiveX Controls</span></span>](activex-controls.md)
</dt> </dl>

 

 




