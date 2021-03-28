---
description: Standardmäßig werden ab Windows Vista-System Steuerungselemente nicht angezeigt, wenn Windows im abgesicherten Modus ausgeführt wird.
title: Zugreifen auf die Systemsteuerung im abgesicherten Modus
ms.topic: article
ms.date: 05/31/2018
ms.assetid: f37bcb0f-9417-4cc4-a57d-4f67a9ccda19
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 0f7a401bbc22a7f8de3618f844bfe463fa3baa50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977416"
---
# <a name="accessing-the-control-panel-in-safe-mode"></a><span data-ttu-id="ab1eb-103">Zugreifen auf die Systemsteuerung im abgesicherten Modus</span><span class="sxs-lookup"><span data-stu-id="ab1eb-103">Accessing the Control Panel in Safe Mode</span></span>

<span data-ttu-id="ab1eb-104">Standardmäßig werden ab Windows Vista-System Steuerungselemente nicht angezeigt, wenn Windows im abgesicherten Modus ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ab1eb-104">By default, as of Windows Vista Control Panel items are not shown when Windows is run in safe mode.</span></span> <span data-ttu-id="ab1eb-105">Damit ein neues System Steuerungselement im abgesicherten Modus angezeigt werden kann, können für den Elementtyp geeignete Registrierungs Werte festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="ab1eb-105">To allow a new Control Panel item to be viewed in safe mode, registry values appropriate to the item type can be set.</span></span> <span data-ttu-id="ab1eb-106">Die Werte werden wie folgt interpretiert:</span><span class="sxs-lookup"><span data-stu-id="ab1eb-106">The values are interpreted as follows:</span></span>



| <span data-ttu-id="ab1eb-107">Wert</span><span class="sxs-lookup"><span data-stu-id="ab1eb-107">Value</span></span> | <span data-ttu-id="ab1eb-108">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="ab1eb-108">Meaning</span></span>                                                            |
|-------|--------------------------------------------------------------------|
| <span data-ttu-id="ab1eb-109">1</span><span class="sxs-lookup"><span data-stu-id="ab1eb-109">1</span></span>     | <span data-ttu-id="ab1eb-110">Das Element sollte nur im minimal abgesicherten Modus angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="ab1eb-110">The item should appear in minimal safe mode only.</span></span>                  |
| <span data-ttu-id="ab1eb-111">2</span><span class="sxs-lookup"><span data-stu-id="ab1eb-111">2</span></span>     | <span data-ttu-id="ab1eb-112">Das Element sollte nur im abgesicherten Modus angezeigt werden, wenn das Netzwerk aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="ab1eb-112">The item should appear in safe mode only if networking is enabled.</span></span> |
| <span data-ttu-id="ab1eb-113">3</span><span class="sxs-lookup"><span data-stu-id="ab1eb-113">3</span></span>     | <span data-ttu-id="ab1eb-114">Das Element sollte immer in beliebiger Form Abgesicherter Modus angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="ab1eb-114">The item should always appear in any form of safe mode.</span></span>            |



 

<span data-ttu-id="ab1eb-115">Dieses Beispiel zeigt die Einträge, die für ein Element erforderlich sind, das als cpl-oder DLL-Datei implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="ab1eb-115">This example shows the entries required for an item implemented as a .cpl or .dll file.</span></span> <span data-ttu-id="ab1eb-116">Er gibt an, dass das Element im abgesicherten Modus mit Netzwerk angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ab1eb-116">It specifies that the item should appear in safe mode with networking.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Control Panel
                  Extended Properties
                     System.ControlPanel.EnableInSafeMode
                        %ProgramFiles%\MyCorp\MyApp\MyCpl.cpl = [REG_DWORD] 2
```

<span data-ttu-id="ab1eb-117">Dieses Beispiel zeigt die Einträge, die für ein Element erforderlich sind, das als exe-Datei implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="ab1eb-117">This example shows the entries required for an item implemented as a .exe file.</span></span> <span data-ttu-id="ab1eb-118">Gibt an, dass das Element in beliebiger Form Abgesicherter Modus angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ab1eb-118">It specifies that the item should appear in any form of safe mode.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}
         System.ControlPanel.EnableInSafeMode = [REG_DWORD] 3
```

## <a name="related-topics"></a><span data-ttu-id="ab1eb-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ab1eb-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ab1eb-120">System Steuerungselemente</span><span class="sxs-lookup"><span data-stu-id="ab1eb-120">Control Panel Items</span></span>](control-panel-applications.md)
</dt> <dt>

[<span data-ttu-id="ab1eb-121">Richtlinien zur Benutzerfreundlichkeit</span><span class="sxs-lookup"><span data-stu-id="ab1eb-121">User Experience Guidelines</span></span>](user-experience-guidelines.md)
</dt> <dt>

[<span data-ttu-id="ab1eb-122">System Steuerungselemente werden registriert</span><span class="sxs-lookup"><span data-stu-id="ab1eb-122">Registering Control Panel Items</span></span>](registering-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="ab1eb-123">Verwenden von CPlApplet</span><span class="sxs-lookup"><span data-stu-id="ab1eb-123">Using CPLApplet</span></span>](using-cplapplet.md)
</dt> <dt>

[<span data-ttu-id="ab1eb-124">Nachrichtenverarbeitung in der Systemsteuerung</span><span class="sxs-lookup"><span data-stu-id="ab1eb-124">Control Panel Message Processing</span></span>](message-processing.md)
</dt> <dt>

[<span data-ttu-id="ab1eb-125">Ausführen von System Steuerungselementen</span><span class="sxs-lookup"><span data-stu-id="ab1eb-125">Executing Control Panel Items</span></span>](executing-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="ab1eb-126">Erweitern von System Steuerungselementen</span><span class="sxs-lookup"><span data-stu-id="ab1eb-126">Extending System Control Panel Items</span></span>](extending-system-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="ab1eb-127">Zuweisen von System Steuerungs Kategorien</span><span class="sxs-lookup"><span data-stu-id="ab1eb-127">Assigning Control Panel Categories</span></span>](assigning-control-panel-categories.md)
</dt> <dt>

[<span data-ttu-id="ab1eb-128">Erstellen von durchsuchbaren Aufgaben Verknüpfungen für ein System Steuerungselement</span><span class="sxs-lookup"><span data-stu-id="ab1eb-128">Creating Searchable Task Links for a Control Panel Item</span></span>](creating-searchable-task-links.md)
</dt> </dl>

 

 



