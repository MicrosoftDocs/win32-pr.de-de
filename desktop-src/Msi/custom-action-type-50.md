---
description: Entwickler von Windows Installer Paketen können einen benutzerdefinierten Aktionstyp 50 verwenden, wenn die Standard Aktionen nicht ausreichen, um die Installation auszuführen.
ms.assetid: fc8a875d-21e3-452a-8455-80835b52b256
title: Benutzerdefinierter Aktionstyp 50
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5f3a80de730eb727c40c871070ab9e5b2470f98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362393"
---
# <a name="custom-action-type-50"></a><span data-ttu-id="9c003-103">Benutzerdefinierter Aktionstyp 50</span><span class="sxs-lookup"><span data-stu-id="9c003-103">Custom Action Type 50</span></span>

<span data-ttu-id="9c003-104">Diese benutzerdefinierte Aktion ruft eine ausführbare Datei auf, die mit einer Befehlszeile gestartet wurde</span><span class="sxs-lookup"><span data-stu-id="9c003-104">This custom action calls an executable launched with a command line.</span></span>

<span data-ttu-id="9c003-105">Siehe auch [ausführbare Dateien](executable-files.md).</span><span class="sxs-lookup"><span data-stu-id="9c003-105">See also [Executable Files](executable-files.md).</span></span>

## <a name="source"></a><span data-ttu-id="9c003-106">`Source`</span><span class="sxs-lookup"><span data-stu-id="9c003-106">Source</span></span>

<span data-ttu-id="9c003-107">Die ausführbare Datei wird aus einer vorhandenen Datei generiert.</span><span class="sxs-lookup"><span data-stu-id="9c003-107">The executable is generated from an existing file.</span></span> <span data-ttu-id="9c003-108">Das Quellfeld der [Tabelle CustomAction](customaction-table.md) enthält einen Schlüssel für die [Eigenschaften Tabelle](property-table.md) für eine Eigenschaft, die den vollständigen Pfad zur ausführbaren Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="9c003-108">The Source field of the [CustomAction table](customaction-table.md) contains a key to the [Property table](property-table.md) for a property that contains the full path to the executable file.</span></span>

## <a name="type-value"></a><span data-ttu-id="9c003-109">Typwert</span><span class="sxs-lookup"><span data-stu-id="9c003-109">Type Value</span></span>

<span data-ttu-id="9c003-110">Fügen Sie den folgenden Wert in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um den grundlegenden numerischen Typ anzugeben.</span><span class="sxs-lookup"><span data-stu-id="9c003-110">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type.</span></span>



| <span data-ttu-id="9c003-111">Konstanten</span><span class="sxs-lookup"><span data-stu-id="9c003-111">Constants</span></span>                                                        | <span data-ttu-id="9c003-112">Hexadezimal</span><span class="sxs-lookup"><span data-stu-id="9c003-112">Hexadecimal</span></span> | <span data-ttu-id="9c003-113">Decimal</span><span class="sxs-lookup"><span data-stu-id="9c003-113">Decimal</span></span> |
|------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="9c003-114">**msidbcustomaktiontypeexe**  +  **msidbcustomaktiontypeproperty**</span><span class="sxs-lookup"><span data-stu-id="9c003-114">**msidbCustomActionTypeExe** + **msidbCustomActionTypeProperty**</span></span> | <span data-ttu-id="9c003-115">0x032</span><span class="sxs-lookup"><span data-stu-id="9c003-115">0x032</span></span>       | <span data-ttu-id="9c003-116">50</span><span class="sxs-lookup"><span data-stu-id="9c003-116">50</span></span>      |



 

## <a name="target"></a><span data-ttu-id="9c003-117">Ziel</span><span class="sxs-lookup"><span data-stu-id="9c003-117">Target</span></span>

<span data-ttu-id="9c003-118">Die Ziel Spalte der [Tabelle CustomAction](customaction-table.md) enthält die Befehlszeilen Zeichenfolge für die in der Spalte Quelle identifizierte ausführbare Datei.</span><span class="sxs-lookup"><span data-stu-id="9c003-118">The Target column of the [CustomAction table](customaction-table.md) contains the command line string for the executable identified in the Source column.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="9c003-119">Rückgabe Verarbeitungsoptionen</span><span class="sxs-lookup"><span data-stu-id="9c003-119">Return Processing Options</span></span>

<span data-ttu-id="9c003-120">Schließen Sie optionale Flagbits in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um die Rückgabe Verarbeitungsoptionen anzugeben.</span><span class="sxs-lookup"><span data-stu-id="9c003-120">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify return processing options.</span></span> <span data-ttu-id="9c003-121">Eine Beschreibung der Optionen und Werte finden Sie unter " [benutzerdefinierte Aktion: Rückgabe Verarbeitungsoptionen](custom-action-return-processing-options.md)".</span><span class="sxs-lookup"><span data-stu-id="9c003-121">For a description of the options and the values, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="9c003-122">Ausführungszeit Planungsoptionen</span><span class="sxs-lookup"><span data-stu-id="9c003-122">Execution Scheduling Options</span></span>

<span data-ttu-id="9c003-123">Schließen Sie optionale Flagbits in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um Optionen für die Ausführungsplanung anzugeben.</span><span class="sxs-lookup"><span data-stu-id="9c003-123">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify execution scheduling options.</span></span> <span data-ttu-id="9c003-124">Diese Optionen steuern die mehrfache Ausführung von benutzerdefinierten Aktionen.</span><span class="sxs-lookup"><span data-stu-id="9c003-124">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="9c003-125">Eine Beschreibung der Optionen finden Sie unter Optionen für die [Ausführungsplanung für benutzerdefinierte Aktionen](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="9c003-125">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="9c003-126">Ausführungs Optionen für In-Script</span><span class="sxs-lookup"><span data-stu-id="9c003-126">In-Script Execution Options</span></span>

<span data-ttu-id="9c003-127">Schließen Sie optionale Flagbits in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um eine in-Script-Ausführungs Option anzugeben.</span><span class="sxs-lookup"><span data-stu-id="9c003-127">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify an in-script execution option.</span></span> <span data-ttu-id="9c003-128">Diese Optionen kopieren den Aktions Code in das Ausführungs-, Rollback-oder Commit-Skript.</span><span class="sxs-lookup"><span data-stu-id="9c003-128">These options copy the action code into the execution, rollback, or commit script.</span></span> <span data-ttu-id="9c003-129">Eine Beschreibung der Optionen finden Sie unter [benutzerdefinierte Aktion In-Script Ausführungs Optionen](custom-action-in-script-execution-options.md).</span><span class="sxs-lookup"><span data-stu-id="9c003-129">For a description of the options, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

## <a name="return-values"></a><span data-ttu-id="9c003-130">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="9c003-130">Return Values</span></span>

<span data-ttu-id="9c003-131">Benutzerdefinierte Aktionen, die [ausführbare Dateien](executable-files.md) sind, müssen für Erfolg den Wert 0 zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="9c003-131">Custom actions that are [executable files](executable-files.md) must return a value of 0 for success.</span></span> <span data-ttu-id="9c003-132">Der Installer interpretiert jeden anderen Rückgabewert als Fehler.</span><span class="sxs-lookup"><span data-stu-id="9c003-132">The installer interprets any other return value as failure.</span></span> <span data-ttu-id="9c003-133">Zum Ignorieren von Rückgabe Werten legen Sie das Bitflag " **msidbcustomaction typecontinue** " im type-Feld der Tabelle "CustomAction" fest.</span><span class="sxs-lookup"><span data-stu-id="9c003-133">To ignore return values set the **msidbCustomActionTypeContinue** bit flag in the Type field of the CustomAction table.</span></span>

## <a name="remarks"></a><span data-ttu-id="9c003-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9c003-134">Remarks</span></span>

<span data-ttu-id="9c003-135">Eine benutzerdefinierte Aktion, die eine ausführbare Datei startet, benötigt eine Befehlszeile, die häufig Eigenschaften enthält, die dynamisch festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="9c003-135">A custom action that launches an executable takes a command line, which commonly contains properties that are designated dynamically.</span></span> <span data-ttu-id="9c003-136">Wenn es sich auch um eine [benutzerdefinierte Aktion für die verzögerte Ausführung](deferred-execution-custom-actions.md)handelt, verwendet das Installationsprogramm zum Erstellen des Prozesses den Prozess, wenn die benutzerdefinierte Aktion aus dem Installationsskript aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="9c003-136">If this is also a [deferred execution custom action](deferred-execution-custom-actions.md), the installer uses CreateProcessAsUser or CreateProcess to create the process when the custom action is invoked from the installation script.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9c003-137">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9c003-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9c003-138">Benutzerdefinierte \_ Aktionen</span><span class="sxs-lookup"><span data-stu-id="9c003-138">Custom\_Actions</span></span>](custom-actions.md)
</dt> </dl>

 

 



