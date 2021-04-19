---
description: Com+-Anwendungen werden erstellt.
ms.assetid: 32828d4d-aa98-4e6a-b7de-2ec832024517
title: Com+-Anwendungen werden erstellt.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e42a4b7ad18dab3f7163f527626322e05671e7be
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345462"
---
# <a name="creating-com-applications"></a><span data-ttu-id="60fb0-103">Com+-Anwendungen werden erstellt.</span><span class="sxs-lookup"><span data-stu-id="60fb0-103">Creating COM+ Applications</span></span>

<span data-ttu-id="60fb0-104">In diesem Abschnitt wird beschrieben, wie Sie eine neue (leere) com+-Anwendung erstellen und dieser Anwendung dann Komponenten hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="60fb0-104">This section describes how to create a new (empty) COM+ application and then add components to that application.</span></span> <span data-ttu-id="60fb0-105">Außerdem wird beschrieben, wie COM-Komponenten hinzugefügt und aus vorhandenen COM+-Anwendungen entfernt werden und wie Komponenten von einer COM+-Anwendung in eine andere verschoben und kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="60fb0-105">It also describes how to add COM components to, and remove them from, existing COM+ applications, and how to move and copy components from one COM+ application to another.</span></span>



| <span data-ttu-id="60fb0-106">Thema</span><span class="sxs-lookup"><span data-stu-id="60fb0-106">Topic</span></span>                                                                                                       | <span data-ttu-id="60fb0-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="60fb0-107">Description</span></span>                                                                        |
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="60fb0-108">Eine neue COM+-Anwendung wird erstellt.</span><span class="sxs-lookup"><span data-stu-id="60fb0-108">Creating a New COM+ Application</span></span>](creating-a-new-com--application.md)<br/>                           | <span data-ttu-id="60fb0-109">Hier wird beschrieben, wie eine neue COM+-Anwendung erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="60fb0-109">Describes how to create a new COM+ application.</span></span><br/>                         |
| [<span data-ttu-id="60fb0-110">Installieren neuer Komponenten</span><span class="sxs-lookup"><span data-stu-id="60fb0-110">Installing New Components</span></span>](installing-new-components.md)<br/>                                       | <span data-ttu-id="60fb0-111">Hier wird beschrieben, wie neue Komponenten installiert werden.</span><span class="sxs-lookup"><span data-stu-id="60fb0-111">Describes how to install new components.</span></span><br/>                                |
| [<span data-ttu-id="60fb0-112">Importieren von Komponenten</span><span class="sxs-lookup"><span data-stu-id="60fb0-112">Importing Components</span></span>](importing-components.md)<br/>                                                 | <span data-ttu-id="60fb0-113">Beschreibt, wie-Komponenten importiert werden.</span><span class="sxs-lookup"><span data-stu-id="60fb0-113">Describes how to import components.</span></span><br/>                                     |
| [<span data-ttu-id="60fb0-114">Entfernen einer Komponente aus einer COM+-Anwendung</span><span class="sxs-lookup"><span data-stu-id="60fb0-114">Removing a Component from a COM+ Application</span></span>](removing-a-component-from-a-com--application.md)<br/> | <span data-ttu-id="60fb0-115">Beschreibt, wie eine Komponente aus einer COM+-Anwendung gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="60fb0-115">Describes how to delete a component from a COM+ application.</span></span><br/>            |
| [<span data-ttu-id="60fb0-116">Verschieben von Komponenten</span><span class="sxs-lookup"><span data-stu-id="60fb0-116">Moving Components</span></span>](moving-components.md)<br/>                                                       | <span data-ttu-id="60fb0-117">Beschreibt, wie eine Komponente von einer COM+-Anwendung in eine andere verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="60fb0-117">Describes how to move a component from one COM+ application to another.</span></span><br/> |
| [<span data-ttu-id="60fb0-118">Kopieren von Komponenten</span><span class="sxs-lookup"><span data-stu-id="60fb0-118">Copying Components</span></span>](copying-components.md)<br/>                                                     | <span data-ttu-id="60fb0-119">Beschreibt, wie eine Komponente von einer COM+-Anwendung in eine andere kopiert wird.</span><span class="sxs-lookup"><span data-stu-id="60fb0-119">Describes how to copy a component from one COM+ application to another.</span></span><br/> |
| [<span data-ttu-id="60fb0-120">Eine COM+-Anwendung wird gelöscht.</span><span class="sxs-lookup"><span data-stu-id="60fb0-120">Deleting a COM+ Application</span></span>](deleting-a-com--application.md)<br/>                                   | <span data-ttu-id="60fb0-121">Beschreibt, wie eine COM+-Anwendung gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="60fb0-121">Describes how to delete a COM+ application.</span></span><br/>                             |



 

<span data-ttu-id="60fb0-122">Konzeptionelle Informationen zu den in diesem Abschnitt beschriebenen Verfahren finden Sie unter [com+-Anwendungs Übersicht](com--application-overview.md) und Bereitstellen von [com+-Anwendungen](deploying-com--applications.md).</span><span class="sxs-lookup"><span data-stu-id="60fb0-122">For conceptual information on the procedures described in this section, see [COM+ Application Overview](com--application-overview.md) and [Deploying COM+ Applications](deploying-com--applications.md).</span></span>

<span data-ttu-id="60fb0-123">Informationen zu den administrativen Aufgaben beim Exportieren und Installieren von com+-Anwendungen finden Sie unter "Installieren von com+-Anwendungen" im Administrator Handbuch für Komponenten Dienste.</span><span class="sxs-lookup"><span data-stu-id="60fb0-123">For procedural information on the administrative tasks involved in exporting and installing COM+ applications, see "Installing COM+ Applications" in the Component Services Administrator's Guide.</span></span>

## <a name="related-topics"></a><span data-ttu-id="60fb0-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="60fb0-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="60fb0-125">Automatisieren der com+-Verwaltung</span><span class="sxs-lookup"><span data-stu-id="60fb0-125">Automating COM+ Administration</span></span>](automating-com--administration.md)
</dt> <dt>

[<span data-ttu-id="60fb0-126">Com+-Anwendungen werden konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="60fb0-126">Configuring COM+ Applications</span></span>](configuring-com--applications.md)
</dt> <dt>

[<span data-ttu-id="60fb0-127">Konvertierung von MTS-Paketen in com+-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="60fb0-127">Conversion of MTS Packages to COM+ Applications</span></span>](conversion-of-mts-packages-to-com--applications.md)
</dt> </dl>

 

 




