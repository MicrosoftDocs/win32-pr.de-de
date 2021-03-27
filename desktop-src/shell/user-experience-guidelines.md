---
description: Die Hauptverantwortung für alle System Steuerungselemente besteht darin, ein Fenster anzuzeigen, in dem der Benutzereinstellungen anzeigen und bearbeiten kann.
title: Richtlinien zur Benutzerfreundlichkeit
ms.topic: article
ms.date: 09/24/2020
ms.assetid: f03a154b-9781-4718-8244-3d57fee0755e
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: e25f8885c2444a51d5d5d8cc917121c7f3b26a09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104995102"
---
# <a name="user-experience-guidelines"></a><span data-ttu-id="63751-103">Richtlinien zur Benutzerfreundlichkeit</span><span class="sxs-lookup"><span data-stu-id="63751-103">User Experience Guidelines</span></span>

<span data-ttu-id="63751-104">Die Hauptverantwortung für alle System Steuerungselemente besteht darin, ein Fenster anzuzeigen, in dem der Benutzereinstellungen anzeigen und bearbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="63751-104">The primary responsibility of any Control Panel item is to display a window that allows the user to view and manipulate settings.</span></span> <span data-ttu-id="63751-105">Weitere Informationen zum Verhalten und zum Entwurf von System Steuerungselementen finden Sie in den [Richtlinien zur Benutzerfreundlichkeit](../uxguide/winenv-ctrl-panels.md) in den Steuerungs Bereichen.</span><span class="sxs-lookup"><span data-stu-id="63751-105">See the [Control Panels user experience (UX) guidelines](../uxguide/winenv-ctrl-panels.md) for the behavior and design of Control Panel items.</span></span> <span data-ttu-id="63751-106">Die in diesem Thema erläuterten Richtlinien zeigen eine Aufgaben Fluss Methode zum Organisieren eines System Steuerungs Elements.</span><span class="sxs-lookup"><span data-stu-id="63751-106">The guidelines discussed in that topic show a task flow method of organizing a Control Panel item.</span></span> <span data-ttu-id="63751-107">Dadurch werden die wichtigsten Einstellungen auf einer Startseite platziert.</span><span class="sxs-lookup"><span data-stu-id="63751-107">This places the most important settings on a home page.</span></span> <span data-ttu-id="63751-108">Weniger häufig verwendete Einstellungen werden auf der Seite "Sprachanrufe" platziert, oder der Zugriff erfolgt über Links in einem Seitenbereich.</span><span class="sxs-lookup"><span data-stu-id="63751-108">Less frequently used settings are placed on spoke pages or accessed from links in a side pane.</span></span>

<span data-ttu-id="63751-109">Die Systemsteuerung umfasst viele Elemente, die diese Richtlinien einhalten, wie z. b. das Easy Access Center und das Netzwerk-und Freigabe Center.</span><span class="sxs-lookup"><span data-stu-id="63751-109">The Control Panel includes many items that follow these guidelines, such as Ease of Access Center and Network and Sharing Center.</span></span> <span data-ttu-id="63751-110">Andere System Steuerungselemente verwenden das Format des Dialogfeld Eigenschaften Blatts im Registerkarten Format, wie in früheren Versionen von Windows.</span><span class="sxs-lookup"><span data-stu-id="63751-110">Other Control Panel items use the tabbed dialog property sheet format as in earlier versions of Windows.</span></span> <span data-ttu-id="63751-111">Beispiele hierfür sind die Maus Element-und Internet Optionen.</span><span class="sxs-lookup"><span data-stu-id="63751-111">Examples include the Mouse item and Internet Options.</span></span> <span data-ttu-id="63751-112">Die Verwendung des Eigenschaften Blatt Formats sollte eingestellt werden.</span><span class="sxs-lookup"><span data-stu-id="63751-112">Use of the property sheet format should be discontinued.</span></span> <span data-ttu-id="63751-113">Wenn Sie neue System Steuerungselemente erstellen, befolgen Sie die Richtlinien für den Task Ablauf.</span><span class="sxs-lookup"><span data-stu-id="63751-113">If you create new Control Panel items, you should follow the task flow guidelines.</span></span>

<span data-ttu-id="63751-114">In der Vergangenheit wurden System Steuerungselemente als cpl-Dateien verpackt.</span><span class="sxs-lookup"><span data-stu-id="63751-114">In the past, Control Panel items were packaged as .cpl files.</span></span> <span data-ttu-id="63751-115">Dies ist nicht mehr erforderlich.</span><span class="sxs-lookup"><span data-stu-id="63751-115">That is no longer necessary.</span></span> <span data-ttu-id="63751-116">Neue System Steuerungselemente müssen als eigenständige exe-Datei oder als befehlszeilenflag für die ausführbare Hauptdatei der Anwendung implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="63751-116">New Control Panel items should be implemented as a standalone .exe file or as a command-line flag option for the application's main executable file.</span></span>

> [!Note]  
> <span data-ttu-id="63751-117">Auf 64-Bit-Systemen werden in der Systemsteuerung die System Steuerungselemente 32-Bit angezeigt, wenn die Option " **32-Bit-System Steuerungselemente anzeigen** " ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="63751-117">On 64-bit systems, 32-bit Control Panel items are displayed in the Control Panel when the **View 32-bit Control Panel Items folder** option is selected.</span></span> <span data-ttu-id="63751-118">Die 32-Bit-Elemente müssen sich im Ordner% systemroot% \\ syswow64 befinden, der angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="63751-118">The 32-bit items must be located in the %SystemRoot%\\SysWOW64 folder to be displayed.</span></span> <span data-ttu-id="63751-119">Sie erfordern keine weitere Registrierung.</span><span class="sxs-lookup"><span data-stu-id="63751-119">They do not require any further registration.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="63751-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="63751-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="63751-121">System Steuerungselemente</span><span class="sxs-lookup"><span data-stu-id="63751-121">Control Panel Items</span></span>](control-panel-applications.md)
</dt> <dt>

[<span data-ttu-id="63751-122">System Steuerungselemente werden registriert</span><span class="sxs-lookup"><span data-stu-id="63751-122">Registering Control Panel Items</span></span>](registering-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="63751-123">Verwenden von CPlApplet</span><span class="sxs-lookup"><span data-stu-id="63751-123">Using CPLApplet</span></span>](using-cplapplet.md)
</dt> <dt>

[<span data-ttu-id="63751-124">Nachrichtenverarbeitung in der Systemsteuerung</span><span class="sxs-lookup"><span data-stu-id="63751-124">Control Panel Message Processing</span></span>](message-processing.md)
</dt> <dt>

[<span data-ttu-id="63751-125">Ausführen von System Steuerungselementen</span><span class="sxs-lookup"><span data-stu-id="63751-125">Executing Control Panel Items</span></span>](executing-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="63751-126">Erweitern von System Steuerungselementen</span><span class="sxs-lookup"><span data-stu-id="63751-126">Extending System Control Panel Items</span></span>](extending-system-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="63751-127">Zuweisen von System Steuerungs Kategorien</span><span class="sxs-lookup"><span data-stu-id="63751-127">Assigning Control Panel Categories</span></span>](assigning-control-panel-categories.md)
</dt> <dt>

[<span data-ttu-id="63751-128">Erstellen von durchsuchbaren Aufgaben Verknüpfungen für ein System Steuerungselement</span><span class="sxs-lookup"><span data-stu-id="63751-128">Creating Searchable Task Links for a Control Panel Item</span></span>](creating-searchable-task-links.md)
</dt> <dt>

[<span data-ttu-id="63751-129">Zugreifen auf die Systemsteuerung im abgesicherten Modus</span><span class="sxs-lookup"><span data-stu-id="63751-129">Accessing the Control Panel in Safe Mode</span></span>](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 



