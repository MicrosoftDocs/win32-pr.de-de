---
description: System Steuerungselemente sind DLLs oder ausführbare Dateien (exe-Dateien), mit denen Benutzer die Umgebung von Windows konfigurieren können. Der Zugriff erfolgt in der Regel durch Klicken auf ein Symbol in der Systemsteuerung.
title: Implementieren von System Steuerungselementen
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2e61cbc0-fbb5-4680-8123-f8ffdcf98210
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 310d01f07d40cef69c6be30231bbf4780a1d8838
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977368"
---
# <a name="implementing-control-panel-items"></a><span data-ttu-id="e4dfa-104">Implementieren von System Steuerungselementen</span><span class="sxs-lookup"><span data-stu-id="e4dfa-104">Implementing Control Panel Items</span></span>

<span data-ttu-id="e4dfa-105">System Steuerungselemente sind DLLs oder ausführbare Dateien (exe-Dateien), mit denen Benutzer die Umgebung von Windows konfigurieren können.</span><span class="sxs-lookup"><span data-stu-id="e4dfa-105">Control Panel items are DLLs or executable (.exe) files that let users configure the environment of Windows.</span></span> <span data-ttu-id="e4dfa-106">Der Zugriff erfolgt in der Regel durch Klicken auf ein Symbol in der Systemsteuerung.</span><span class="sxs-lookup"><span data-stu-id="e4dfa-106">They are typically accessed by clicking an icon in the Control Panel.</span></span>

<span data-ttu-id="e4dfa-107">In diesem Abschnitt werden die System Steuerungselemente beschrieben und erläutert, wie Sie erstellt und registriert werden, damit Sie in der Systemsteuerung ordnungsgemäß angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="e4dfa-107">This section describes Control Panel items and explains how to create and register them so that they appear appropriately in the Control Panel.</span></span> <span data-ttu-id="e4dfa-108">Für Windows Vista sind Informationen enthalten, in denen Sie erfahren, wie Sie Aufgaben Verknüpfungen hinzufügen, die unter dem System Steuerungselement und in den Suchergebnissen der Systemsteuerung angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="e4dfa-108">For Windows Vista, information is included that tells you how to add task links that appear under the Control Panel item and in Control Panel search results.</span></span>

-   [<span data-ttu-id="e4dfa-109">Richtlinien zur Benutzerfreundlichkeit</span><span class="sxs-lookup"><span data-stu-id="e4dfa-109">User Experience Guidelines</span></span>](user-experience-guidelines.md)
-   [<span data-ttu-id="e4dfa-110">System Steuerungselemente werden registriert</span><span class="sxs-lookup"><span data-stu-id="e4dfa-110">Registering Control Panel Items</span></span>](registering-control-panel-items.md)
-   [<span data-ttu-id="e4dfa-111">Registrieren von ausführbaren System Steuerungselementen</span><span class="sxs-lookup"><span data-stu-id="e4dfa-111">How To Register Executable Control Panel Items</span></span>](how-to-register-an-executable-control-panel-item-registration-.md)
-   [<span data-ttu-id="e4dfa-112">Registrieren von dll-System Steuerungselementen</span><span class="sxs-lookup"><span data-stu-id="e4dfa-112">How To Register DLL Control Panel Items</span></span>](how-to-register-dll-control-panel-item-registration-.md)
-   [<span data-ttu-id="e4dfa-113">Verwenden von CPlApplet</span><span class="sxs-lookup"><span data-stu-id="e4dfa-113">Using CPLApplet</span></span>](using-cplapplet.md)
-   [<span data-ttu-id="e4dfa-114">Nachrichtenverarbeitung in der Systemsteuerung</span><span class="sxs-lookup"><span data-stu-id="e4dfa-114">Control Panel Message Processing</span></span>](message-processing.md)
-   [<span data-ttu-id="e4dfa-115">Ausführen von System Steuerungselementen</span><span class="sxs-lookup"><span data-stu-id="e4dfa-115">Executing Control Panel Items</span></span>](executing-control-panel-items.md)
-   [<span data-ttu-id="e4dfa-116">Erweitern von System Steuerungselementen</span><span class="sxs-lookup"><span data-stu-id="e4dfa-116">Extending System Control Panel Items</span></span>](extending-system-control-panel-items.md)
-   [<span data-ttu-id="e4dfa-117">Zuweisen von System Steuerungs Kategorien</span><span class="sxs-lookup"><span data-stu-id="e4dfa-117">Assigning Control Panel Categories</span></span>](assigning-control-panel-categories.md)
-   [<span data-ttu-id="e4dfa-118">Erstellen von durchsuchbaren Aufgaben Verknüpfungen für ein System Steuerungselement</span><span class="sxs-lookup"><span data-stu-id="e4dfa-118">Creating Searchable Task Links for a Control Panel Item</span></span>](creating-searchable-task-links.md)
-   [<span data-ttu-id="e4dfa-119">Zugreifen auf die Systemsteuerung im abgesicherten Modus</span><span class="sxs-lookup"><span data-stu-id="e4dfa-119">Accessing the Control Panel in Safe Mode</span></span>](accessing-the-cp-in-safe-mode-under-vista.md)
-   [<span data-ttu-id="e4dfa-120">Kanonische Namen von System Steuerungselementen</span><span class="sxs-lookup"><span data-stu-id="e4dfa-120">Canonical Names of Control Panel Items</span></span>](controlpanel-canonical-names.md)

 

 



