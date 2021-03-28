---
description: Einige der in der Systemsteuerung gefundenen Systemelemente sind erweiterbar. Um eine System Steuerungs Erweiterung zu installieren, registrieren Sie Ihre Shellerweiterung wie folgt, wobei Name der vordefinierte Name des System Elements ist (siehe Tabelle unten).
title: Erweitern von System Steuerungselementen
ms.topic: article
ms.date: 05/31/2018
ms.assetid: b8b18b71-c95f-4c71-8df4-fe9342ce0165
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 9b0f6628d7bc75378915c1d9f3e20327478742df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104993870"
---
# <a name="extending-system-control-panel-items"></a><span data-ttu-id="0e5c4-104">Erweitern von System Steuerungselementen</span><span class="sxs-lookup"><span data-stu-id="0e5c4-104">Extending System Control Panel Items</span></span>

<span data-ttu-id="0e5c4-105">Einige der in der Systemsteuerung gefundenen Systemelemente sind erweiterbar.</span><span class="sxs-lookup"><span data-stu-id="0e5c4-105">Some of the system items found in the Control Panel are extensible.</span></span> <span data-ttu-id="0e5c4-106">Um eine System Steuerungs Erweiterung zu installieren, registrieren Sie Ihre Shellerweiterung wie folgt, wobei *Name* der vordefinierte Name des System Elements ist (siehe Tabelle unten).</span><span class="sxs-lookup"><span data-stu-id="0e5c4-106">To install a Control Panel extension, register your Shell extension as follows, where *name* is the predefined name of the system item (see table below).</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Controls Folder
                  name
                     shellex
                        PropertySheetHandlers
```

<span data-ttu-id="0e5c4-107">Dies ähnelt der Art und Weise, wie Sie eine Erweiterung für ein vordefiniertes Shellobjekt registrieren würden.</span><span class="sxs-lookup"><span data-stu-id="0e5c4-107">This is similar to the way you would register an extension for a predefined Shell object.</span></span> <span data-ttu-id="0e5c4-108">Da es sich bei den einzigen Shellerweiterungen, die von System Steuerungselementen unterstützt werden, um Eigenschaften Blätter handelt, muss die Registrierung unter dem Unterschlüssel **shellex** \\ **propertysheethandlers** abgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="0e5c4-108">Because the only Shell extensions supported by Control Panel items are property sheets, the registration must be under the **shellex**\\**PropertySheetHandlers** subkey.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0e5c4-109">System Steuerungselement</span><span class="sxs-lookup"><span data-stu-id="0e5c4-109">Control Panel item</span></span></th>
<th><span data-ttu-id="0e5c4-110"><em>name</em></span><span class="sxs-lookup"><span data-stu-id="0e5c4-110"><em>name</em></span></span></th>
<th><span data-ttu-id="0e5c4-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0e5c4-111">Remarks</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0e5c4-112">Anzeige</span><span class="sxs-lookup"><span data-stu-id="0e5c4-112">Display</span></span></td>
<td><span data-ttu-id="0e5c4-113">Schreibtisch</span><span class="sxs-lookup"><span data-stu-id="0e5c4-113">Desk</span></span></td>
<td><span data-ttu-id="0e5c4-114">Unterstützt auch die Ersetzung der <strong>Desktop</strong> Seite.</span><span class="sxs-lookup"><span data-stu-id="0e5c4-114">Also supports replacement of the <strong>Desktop</strong> page.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="0e5c4-115">Dies wird unter Windows Vista nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0e5c4-115">This is no longer supported under Windows Vista.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0e5c4-116">Anzeigeeinstellungen erweitert</span><span class="sxs-lookup"><span data-stu-id="0e5c4-116">Display Settings Advanced</span></span></td>
<td><span data-ttu-id="0e5c4-117">Sicherungsmedium</span><span class="sxs-lookup"><span data-stu-id="0e5c4-117">Device</span></span></td>
<td><span data-ttu-id="0e5c4-118">Nicht Hardware spezifische erweiterte Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="0e5c4-118">Nonhardware-specific advanced properties.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="0e5c4-119">Dies wird unter Windows Vista nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0e5c4-119">This is no longer supported under Windows Vista.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0e5c4-120">Anzeigeeinstellungen erweitert</span><span class="sxs-lookup"><span data-stu-id="0e5c4-120">Display Settings Advanced</span></span></td>
<td><span data-ttu-id="0e5c4-121">Anzeige</span><span class="sxs-lookup"><span data-stu-id="0e5c4-121">Display</span></span></td>
<td><span data-ttu-id="0e5c4-122">Hardware spezifische erweiterte Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="0e5c4-122">Hardware-specific advanced properties.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="0e5c4-123">Dies wird unter Windows Vista nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0e5c4-123">This is no longer supported under Windows Vista.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0e5c4-124">Internetoptionen</span><span class="sxs-lookup"><span data-stu-id="0e5c4-124">Internet Options</span></span></td>
<td><span data-ttu-id="0e5c4-125">Internet</span><span class="sxs-lookup"><span data-stu-id="0e5c4-125">Internet</span></span></td>
<td><span data-ttu-id="0e5c4-126">Die maximal zulässige Anzahl von Erweiterungs Seiten ist 18.</span><span class="sxs-lookup"><span data-stu-id="0e5c4-126">The maximum number of extension pages is 18.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0e5c4-127">Tastatur</span><span class="sxs-lookup"><span data-stu-id="0e5c4-127">Keyboard</span></span></td>
<td><span data-ttu-id="0e5c4-128">Tastatur</span><span class="sxs-lookup"><span data-stu-id="0e5c4-128">Keyboard</span></span></td>
<td><span data-ttu-id="0e5c4-129">Die maximal zulässige Anzahl von Erweiterungs Seiten ist 30.</span><span class="sxs-lookup"><span data-stu-id="0e5c4-129">The maximum number of extension pages is 30.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0e5c4-130">Maus</span><span class="sxs-lookup"><span data-stu-id="0e5c4-130">Mouse</span></span></td>
<td><span data-ttu-id="0e5c4-131">Maus</span><span class="sxs-lookup"><span data-stu-id="0e5c4-131">Mouse</span></span></td>
<td><span data-ttu-id="0e5c4-132">Unterstützt auch das Ersetzen von Standardseiten.</span><span class="sxs-lookup"><span data-stu-id="0e5c4-132">Also supports replacement of standard pages.</span></span> <span data-ttu-id="0e5c4-133">Die maximal zulässige Anzahl von Erweiterungs Seiten ist 8.</span><span class="sxs-lookup"><span data-stu-id="0e5c4-133">The maximum number of extension pages is 8.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0e5c4-134">Energieoptionen</span><span class="sxs-lookup"><span data-stu-id="0e5c4-134">Power Options</span></span></td>
<td><span data-ttu-id="0e5c4-135">Power</span><span class="sxs-lookup"><span data-stu-id="0e5c4-135">Power</span></span></td>
<td><span data-ttu-id="0e5c4-136">Die maximale Anzahl von Seiten, einschließlich Standardseiten, ist 18.</span><span class="sxs-lookup"><span data-stu-id="0e5c4-136">The maximum number of pages, including standard pages, is 18.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0e5c4-137">System</span><span class="sxs-lookup"><span data-stu-id="0e5c4-137">System</span></span></td>
<td><span data-ttu-id="0e5c4-138">System</span><span class="sxs-lookup"><span data-stu-id="0e5c4-138">System</span></span></td>
<td><span data-ttu-id="0e5c4-139">Die maximal zulässige Anzahl von Erweiterungs Seiten ist 8.</span><span class="sxs-lookup"><span data-stu-id="0e5c4-139">The maximum number of extension pages is 8.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="0e5c4-140">Dies wird unter Windows Vista nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0e5c4-140">This is no longer supported under Windows Vista.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="0e5c4-141">Das **Element "** Software" in der Windows XP-Systemsteuerung ist kein Eigenschaften Blatt und kann daher nicht durch die hier beschriebenen Methoden erweitert werden.</span><span class="sxs-lookup"><span data-stu-id="0e5c4-141">The **Add or Remove Programs** item in the Windows XP Control Panel is not a property sheet and therefore cannot be extended by the methods discussed here.</span></span> <span data-ttu-id="0e5c4-142">Stattdessen wird der Inhalt von Anwendungs Verlegern abgerufen.</span><span class="sxs-lookup"><span data-stu-id="0e5c4-142">Instead, its content is obtained from application publishers.</span></span> <span data-ttu-id="0e5c4-143">Weitere Informationen zum Hinzufügen von Inhalten zum **Hinzufügen oder Entfernen von Programmen finden Sie** unter [**iapppublisher**](/windows/desktop/api/Shappmgr/nn-shappmgr-iapppublisher), [**ienumpublishedapps**](/windows/desktop/api/Shappmgr/nn-shappmgr-ienumpublishedapps)und [**ipublishedapp**](/windows/desktop/api/Shappmgr/nn-shappmgr-ipublishedapp).</span><span class="sxs-lookup"><span data-stu-id="0e5c4-143">For more information on adding content to **Add or Remove Programs**, see [**IAppPublisher**](/windows/desktop/api/Shappmgr/nn-shappmgr-iapppublisher), [**IEnumPublishedApps**](/windows/desktop/api/Shappmgr/nn-shappmgr-ienumpublishedapps), and [**IPublishedApp**](/windows/desktop/api/Shappmgr/nn-shappmgr-ipublishedapp).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0e5c4-144">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0e5c4-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0e5c4-145">System Steuerungselemente</span><span class="sxs-lookup"><span data-stu-id="0e5c4-145">Control Panel Items</span></span>](control-panel-applications.md)
</dt> <dt>

[<span data-ttu-id="0e5c4-146">Richtlinien zur Benutzerfreundlichkeit</span><span class="sxs-lookup"><span data-stu-id="0e5c4-146">User Experience Guidelines</span></span>](user-experience-guidelines.md)
</dt> <dt>

[<span data-ttu-id="0e5c4-147">System Steuerungselemente werden registriert</span><span class="sxs-lookup"><span data-stu-id="0e5c4-147">Registering Control Panel Items</span></span>](registering-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="0e5c4-148">Verwenden von CPlApplet</span><span class="sxs-lookup"><span data-stu-id="0e5c4-148">Using CPLApplet</span></span>](using-cplapplet.md)
</dt> <dt>

[<span data-ttu-id="0e5c4-149">Nachrichtenverarbeitung in der Systemsteuerung</span><span class="sxs-lookup"><span data-stu-id="0e5c4-149">Control Panel Message Processing</span></span>](message-processing.md)
</dt> <dt>

[<span data-ttu-id="0e5c4-150">Ausführen von System Steuerungselementen</span><span class="sxs-lookup"><span data-stu-id="0e5c4-150">Executing Control Panel Items</span></span>](executing-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="0e5c4-151">Zuweisen von System Steuerungs Kategorien</span><span class="sxs-lookup"><span data-stu-id="0e5c4-151">Assigning Control Panel Categories</span></span>](assigning-control-panel-categories.md)
</dt> <dt>

[<span data-ttu-id="0e5c4-152">Erstellen von durchsuchbaren Aufgaben Verknüpfungen für ein System Steuerungselement</span><span class="sxs-lookup"><span data-stu-id="0e5c4-152">Creating Searchable Task Links for a Control Panel Item</span></span>](creating-searchable-task-links.md)
</dt> <dt>

[<span data-ttu-id="0e5c4-153">Zugreifen auf die Systemsteuerung im abgesicherten Modus unter Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0e5c4-153">Accessing the Control Panel in Safe Mode under Windows Vista</span></span>](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 




