---
description: Mit Wiederherstellungsoptionen können Anforderer angepasste Wiederherstellungsoptionen an Writer übermitteln.
ms.assetid: 364550a1-070a-4f7e-bd62-84672959dc21
title: Festlegen der VSS-Wiederherstellungsoptionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c814ffb94f25229e7f3e17f592c631f13b6717e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347105"
---
# <a name="setting-vss-restore-options"></a><span data-ttu-id="d52ff-103">Festlegen der VSS-Wiederherstellungsoptionen</span><span class="sxs-lookup"><span data-stu-id="d52ff-103">Setting VSS Restore Options</span></span>

<span data-ttu-id="d52ff-104">Mit Wiederherstellungsoptionen können Anforderer angepasste Wiederherstellungsoptionen an Writer übermitteln.</span><span class="sxs-lookup"><span data-stu-id="d52ff-104">Restore options allow requesters to communicate customized restore options to writers.</span></span>

## <a name="restore-options"></a><span data-ttu-id="d52ff-105">Wiederherstellungsoptionen</span><span class="sxs-lookup"><span data-stu-id="d52ff-105">Restore Options</span></span>

<span data-ttu-id="d52ff-106">Durch die Standardisierung des Formats der Wiederherstellungsoptionen können Writer und Anforderer gängige benutzerdefinierte Anforderungen verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="d52ff-106">Standardizing the format of the restore options allow writers and requesters to handle common custom requests.</span></span> <span data-ttu-id="d52ff-107">Wiederherstellungsoptionen werden von der anfordernden Person festgelegt, indem die [**IVssBackupComponents:: setrestoreoptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions) -Methode bis zu einmal pro ausgewählter Sicherungs Komponente aufgerufen wird, bevor die [**IVssBackupComponents::P**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) -Methode zum erneuten Ausführen aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="d52ff-107">Restore options are set by the requester by calling the [**IVssBackupComponents::SetRestoreOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions) method up to once per selected-for-backup component before calling the [**IVssBackupComponents::PreRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) method.</span></span> <span data-ttu-id="d52ff-108">Die Zeichenfolge, die im *wszrestoreoptions* -Parameter an die Methode "\* **trestoreoptions** " übergeben wird, kann mehrere Werte enthalten, wie unten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="d52ff-108">The string passed in the *wszRestoreOptions* parameter to the **SetRestoreOptions** method can contain multiple values, as described below.</span></span>

## <a name="format"></a><span data-ttu-id="d52ff-109">Format</span><span class="sxs-lookup"><span data-stu-id="d52ff-109">Format</span></span>

<span data-ttu-id="d52ff-110">Das Format der Wiederherstellungsoptionen ist ein oder mehrere durch Trennzeichen getrennte Name-Wert-Paare, und der Name wird optional mit dem Namen der Unterkomponente, für die er gilt, als Präfix vorangestellt.</span><span class="sxs-lookup"><span data-stu-id="d52ff-110">The format of restore options, is one or more comma-separated name/value pairs, and the name is optionally prefixed with the name of the subcomponent to which it applies.</span></span> <span data-ttu-id="d52ff-111">Bei Komponentennamen und Optionsnamen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="d52ff-111">The component names and option names are case-insensitive.</span></span> <span data-ttu-id="d52ff-112">Die Groß-/Kleinschreibung der Werte wird vom Writer festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d52ff-112">The case-sensitivity of the values is determined by the writer.</span></span> <span data-ttu-id="d52ff-113">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="d52ff-113">For example:</span></span>

``` syntax
"Child1":"Option1"="Value1","Option2"="Value2","Child2\Grandchild3":"Option3"="Value3"
```

<span data-ttu-id="d52ff-114">In diesem Beispiel gilt "Option1" nur für die Unterkomponente "child1" und deren Nachfolger, "option2" gilt für alle Komponenten und deren Nachfolger, und "Option3" gilt nur für die \\ unter Komponenten "child2 Grandchild3" und deren Nachfolger.</span><span class="sxs-lookup"><span data-stu-id="d52ff-114">In this example, "Option1" only applies to the "Child1" subcomponent and its descendants, "Option2" applies to all components and their descendants, and "Option3" applies only to the "Child2\\Grandchild3" subcomponents and its descendants.</span></span>

<span data-ttu-id="d52ff-115">Die Methode "\* [**trestoreoptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions) " kann nur für Komponenten aufgerufen werden, die für die Sicherung ausgewählt werden können, während Nachfolger Knoten möglicherweise nicht für die Sicherung auswählbar sind. Sie können für die Wiederherstellung ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="d52ff-115">The [**SetRestoreOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions) method can only be called on components that are selectable for backup, while descendant nodes may not be selectable for backup, they may be selectable for restore.</span></span>

## <a name="common-restore-options"></a><span data-ttu-id="d52ff-116">Allgemeine Wiederherstellungsoptionen</span><span class="sxs-lookup"><span data-stu-id="d52ff-116">Common Restore Options</span></span>

<span data-ttu-id="d52ff-117">Diese allgemeinen Wiederherstellungsoptionen wurden definiert, um die Interoperabilität zwischen Writern und Anforderern zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="d52ff-117">These common restore options have been defined to increase interoperability between writers and requesters.</span></span>

-   <span data-ttu-id="d52ff-118">Tärer</span><span class="sxs-lookup"><span data-stu-id="d52ff-118">Authoritative</span></span>

    <span data-ttu-id="d52ff-119">Die "autoritative"-Option unterstützt mehrere "Item"-Werte, aber nur einen "All"-Wert.</span><span class="sxs-lookup"><span data-stu-id="d52ff-119">The "Authoritative" option supports multiple "Item" values, but only one "All" value.</span></span>

    <span data-ttu-id="d52ff-120">Diese gesamte Komponente ist autoritativ.</span><span class="sxs-lookup"><span data-stu-id="d52ff-120">This entire component is authoritative.</span></span>

    ``` syntax
    "Authoritative"="All"
    ```

    <span data-ttu-id="d52ff-121">Nur das angegebene Element ist autoritativ.</span><span class="sxs-lookup"><span data-stu-id="d52ff-121">Only the specified item is authoritative.</span></span> <span data-ttu-id="d52ff-122">Das Format des benannten Elements wird vom Writer definiert.</span><span class="sxs-lookup"><span data-stu-id="d52ff-122">The format of the named item is defined by the writer.</span></span> <span data-ttu-id="d52ff-123">Allgemeine Bezeichnungen sind " \* ", um alle Dateien anzugeben, "..." , um alle Dateien und Unterverzeichnisse der angegebenen Komponente anzugeben.</span><span class="sxs-lookup"><span data-stu-id="d52ff-123">Common designations are "\*" to indicate all files, "..." to indicate all files and subdirectories of the specified component.</span></span>

    ``` syntax
    "Authoritative"="Item:XXX"
    ```

-   <span data-ttu-id="d52ff-124">Roll Forward</span><span class="sxs-lookup"><span data-stu-id="d52ff-124">Roll Forward</span></span>

    <span data-ttu-id="d52ff-125">Nachdem eine Datenbank wieder hergestellt wurde, führen Schreiber in der Regel einen Rollup durch Protokolle durch, um die Datenbank auf den neuesten Stand zu bringen</span><span class="sxs-lookup"><span data-stu-id="d52ff-125">After a database is restored, writers usually roll forward through logs to bring the database up to date.</span></span> <span data-ttu-id="d52ff-126">Bei inkrementellen oder differenziellen Wiederherstellungen verwendet der Anforderer die [**IVssBackupComponents:: setadditionalrestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setadditionalrestores) -Methode, um das Verhalten der Protokoll Behandlung teilweise zu steuern. diese Wiederherstellungsoption ermöglicht eine präzisetere Steuerung.</span><span class="sxs-lookup"><span data-stu-id="d52ff-126">In the case of incremental or differential restores, the requester uses the [**IVssBackupComponents::SetAdditionalRestores**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setadditionalrestores) method to partially control the log-handling behavior - this restore option allows more granular control.</span></span>

    <span data-ttu-id="d52ff-127">Führen Sie kein Roll Through für Protokolle durch.</span><span class="sxs-lookup"><span data-stu-id="d52ff-127">Do not roll through logs.</span></span>

    ``` syntax
    "Roll Forward"="None"
    ```

    <span data-ttu-id="d52ff-128">Durchlaufen Sie alle Protokolle.</span><span class="sxs-lookup"><span data-stu-id="d52ff-128">Roll through all logs.</span></span>

    ``` syntax
    "Roll Forward"="All"
    ```

    <span data-ttu-id="d52ff-129">Rollover der Protokolle bis zum angegebenen Punkt.</span><span class="sxs-lookup"><span data-stu-id="d52ff-129">Roll through logs up to specified point.</span></span> <span data-ttu-id="d52ff-130">Das Format des angegebenen Punkts wird vom Writer definiert.</span><span class="sxs-lookup"><span data-stu-id="d52ff-130">The format of the specified point is defined by the writer.</span></span>

    ``` syntax
    "Roll Forward"="Partial:XXX"
    ```

-   <span data-ttu-id="d52ff-131">Name der neuen Komponente</span><span class="sxs-lookup"><span data-stu-id="d52ff-131">New Component Name</span></span>

    <span data-ttu-id="d52ff-132">Ein Writer möchte möglicherweise eine Komponente in einem neuen Namen wiederherstellen.</span><span class="sxs-lookup"><span data-stu-id="d52ff-132">A writer may want to restore a component to a new name.</span></span> <span data-ttu-id="d52ff-133">Beispielsweise die Wiederherstellung einer Datenbank unter einem anderen Namen, um ein einzelnes Element wiederherzustellen. Wenn Sie denselben Namen wiederherstellen, werden alle Daten, die wir empfehlen, dass Writer einen gültigen logischen Pfad und Komponentennamen als Wert dieser Optionen akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="d52ff-133">For example, restoring a database to a different name to restore an individual item; restoring to the same name would please all data We recommend that writers accept a valid logical path and component name as this options' value.</span></span> <span data-ttu-id="d52ff-134">Dies wird häufig mit einem [*gerichteten Ziel*](vssgloss-d.md)verwendet.</span><span class="sxs-lookup"><span data-stu-id="d52ff-134">This will often be used with a [*directed target*](vssgloss-d.md).</span></span>

    ``` syntax
    "New Component Name"="Logical Path\Component Name"
    ```

 

 



