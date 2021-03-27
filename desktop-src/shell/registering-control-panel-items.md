---
description: System Steuerungselemente müssen registriert werden, damit Sie im Fenster "Systemsteuerung" angezeigt werden.
title: System Steuerungselemente werden registriert
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 6f21f223-a293-47b5-95e9-06b7a4ff1652
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 05c2a652314babc212e17b48198e9441f4d3465d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131844"
---
# <a name="registering-control-panel-items"></a><span data-ttu-id="d6430-103">System Steuerungselemente werden registriert</span><span class="sxs-lookup"><span data-stu-id="d6430-103">Registering Control Panel Items</span></span>

<span data-ttu-id="d6430-104">System Steuerungselemente müssen registriert werden, damit Sie im Fenster "Systemsteuerung" angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="d6430-104">Control Panel items must be registered in order to appear in the Control Panel window.</span></span> <span data-ttu-id="d6430-105">Wenn das System Steuerungselement als Teil einer exe-Datei implementiert ist, wird es als Befehls Objekt registriert.</span><span class="sxs-lookup"><span data-stu-id="d6430-105">If the Control Panel item is implemented as part of a .exe file then it is registered as a command object.</span></span> <span data-ttu-id="d6430-106">Die Registrierung unterscheidet sich, wenn das Element als DLL-Datei implementiert ist, die die [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) -Funktion exportiert.</span><span class="sxs-lookup"><span data-stu-id="d6430-106">Registration differs if the item is implemented as a .dll file that exports the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function.</span></span>

<span data-ttu-id="d6430-107">Bestimmte Anforderungen werden in den folgenden Themen behandelt:</span><span class="sxs-lookup"><span data-stu-id="d6430-107">Specific requirements are discussed in these topics:</span></span>

-   [<span data-ttu-id="d6430-108">Registrieren von ausführbaren System Steuerungselementen</span><span class="sxs-lookup"><span data-stu-id="d6430-108">How To Register Executable Control Panel Items</span></span>](how-to-register-an-executable-control-panel-item-registration-.md)
-   [<span data-ttu-id="d6430-109">Registrieren von dll-System Steuerungselementen</span><span class="sxs-lookup"><span data-stu-id="d6430-109">How To Register DLL Control Panel Items</span></span>](how-to-register-dll-control-panel-item-registration-.md)

## <a name="related-topics"></a><span data-ttu-id="d6430-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d6430-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d6430-111">System Steuerungselemente</span><span class="sxs-lookup"><span data-stu-id="d6430-111">Control Panel Items</span></span>](control-panel-applications.md)
</dt> <dt>

[<span data-ttu-id="d6430-112">Richtlinien zur Benutzerfreundlichkeit</span><span class="sxs-lookup"><span data-stu-id="d6430-112">User Experience Guidelines</span></span>](user-experience-guidelines.md)
</dt> <dt>

[<span data-ttu-id="d6430-113">Verwenden von CPlApplet</span><span class="sxs-lookup"><span data-stu-id="d6430-113">Using CPLApplet</span></span>](using-cplapplet.md)
</dt> <dt>

[<span data-ttu-id="d6430-114">Nachrichtenverarbeitung in der Systemsteuerung</span><span class="sxs-lookup"><span data-stu-id="d6430-114">Control Panel Message Processing</span></span>](message-processing.md)
</dt> <dt>

[<span data-ttu-id="d6430-115">Ausführen von System Steuerungselementen</span><span class="sxs-lookup"><span data-stu-id="d6430-115">Executing Control Panel Items</span></span>](executing-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="d6430-116">Erweitern von System Steuerungselementen</span><span class="sxs-lookup"><span data-stu-id="d6430-116">Extending System Control Panel Items</span></span>](extending-system-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="d6430-117">Zuweisen von System Steuerungs Kategorien</span><span class="sxs-lookup"><span data-stu-id="d6430-117">Assigning Control Panel Categories</span></span>](assigning-control-panel-categories.md)
</dt> <dt>

[<span data-ttu-id="d6430-118">Erstellen von durchsuchbaren Aufgaben Verknüpfungen für ein System Steuerungselement</span><span class="sxs-lookup"><span data-stu-id="d6430-118">Creating Searchable Task Links for a Control Panel Item</span></span>](creating-searchable-task-links.md)
</dt> <dt>

[<span data-ttu-id="d6430-119">Zugreifen auf die Systemsteuerung im abgesicherten Modus unter Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d6430-119">Accessing the Control Panel in Safe Mode under Windows Vista</span></span>](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 
