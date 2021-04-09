---
description: Entwickler von Windows Installer Paketen können einen benutzerdefinierten Aktionstyp 18 verwenden, wenn die Standard Aktionen nicht ausreichen, um die Installation auszuführen.
ms.assetid: 8a7311a6-41c6-431e-982d-60bacf06454e
title: Benutzerdefinierter Aktionstyp 18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48a669fe3caa532b3a365f1056ca2b36f490ab95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960712"
---
# <a name="custom-action-type-18"></a><span data-ttu-id="e5c98-103">Benutzerdefinierter Aktionstyp 18</span><span class="sxs-lookup"><span data-stu-id="e5c98-103">Custom Action Type 18</span></span>

<span data-ttu-id="e5c98-104">Diese benutzerdefinierte Aktion ruft eine ausführbare Datei auf, die mit einer Befehlszeile gestartet wurde</span><span class="sxs-lookup"><span data-stu-id="e5c98-104">This custom action calls an executable launched with a command line.</span></span>

## <a name="source"></a><span data-ttu-id="e5c98-105">`Source`</span><span class="sxs-lookup"><span data-stu-id="e5c98-105">Source</span></span>

<span data-ttu-id="e5c98-106">Die ausführbare Datei wird aus einer Datei generiert, die mit der Anwendung installiert wird.</span><span class="sxs-lookup"><span data-stu-id="e5c98-106">The executable is generated from a file installed with the application.</span></span> <span data-ttu-id="e5c98-107">Das Quellfeld der [Tabelle "CustomAction](customaction-table.md) " enthält einen Schlüssel für die [Dateitabelle](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="e5c98-107">The Source field of the [CustomAction table](customaction-table.md) contains a key to the [File table](file-table.md).</span></span> <span data-ttu-id="e5c98-108">Der Speicherort des benutzerdefinierten Aktionscodes wird durch die Auflösung des Zielpfads für diese Datei bestimmt. Daher muss diese benutzerdefinierte Aktion aufgerufen werden, nachdem die Datei installiert und vor dem Entfernen entfernt wurde.</span><span class="sxs-lookup"><span data-stu-id="e5c98-108">The location of the custom action code is determined by the resolution of the target path for this file; therefore this custom action must be called after the file has been installed and before it is removed.</span></span>

## <a name="type-value"></a><span data-ttu-id="e5c98-109">Typwert</span><span class="sxs-lookup"><span data-stu-id="e5c98-109">Type Value</span></span>

<span data-ttu-id="e5c98-110">Fügen Sie den folgenden Wert in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um den grundlegenden numerischen Typ anzugeben.</span><span class="sxs-lookup"><span data-stu-id="e5c98-110">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type.</span></span>



| <span data-ttu-id="e5c98-111">Konstanten</span><span class="sxs-lookup"><span data-stu-id="e5c98-111">Constants</span></span>                                                          | <span data-ttu-id="e5c98-112">Hexadezimal</span><span class="sxs-lookup"><span data-stu-id="e5c98-112">Hexadecimal</span></span> | <span data-ttu-id="e5c98-113">Decimal</span><span class="sxs-lookup"><span data-stu-id="e5c98-113">Decimal</span></span> |
|--------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="e5c98-114">**msidbcustomaktiontypeexe**  +  **msidbcustomaktiontypesourcefile**</span><span class="sxs-lookup"><span data-stu-id="e5c98-114">**msidbCustomActionTypeExe** + **msidbCustomActionTypeSourceFile**</span></span> | <span data-ttu-id="e5c98-115">0x012</span><span class="sxs-lookup"><span data-stu-id="e5c98-115">0x012</span></span>       | <span data-ttu-id="e5c98-116">18</span><span class="sxs-lookup"><span data-stu-id="e5c98-116">18</span></span>      |



 

## <a name="target"></a><span data-ttu-id="e5c98-117">Ziel</span><span class="sxs-lookup"><span data-stu-id="e5c98-117">Target</span></span>

<span data-ttu-id="e5c98-118">Die Ziel Spalte der [Tabelle CustomAction](customaction-table.md) enthält die Befehlszeilen Zeichenfolge für die in der Spalte Quelle identifizierte ausführbare Datei.</span><span class="sxs-lookup"><span data-stu-id="e5c98-118">The Target column of the [CustomAction table](customaction-table.md) contains the command line string for the executable identified in the Source column.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="e5c98-119">Rückgabe Verarbeitungsoptionen</span><span class="sxs-lookup"><span data-stu-id="e5c98-119">Return Processing Options</span></span>

<span data-ttu-id="e5c98-120">Schließen Sie optionale Flagbits in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um die Rückgabe Verarbeitungsoptionen anzugeben.</span><span class="sxs-lookup"><span data-stu-id="e5c98-120">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify return processing options.</span></span> <span data-ttu-id="e5c98-121">Eine Beschreibung der Optionen und Werte finden Sie unter " [benutzerdefinierte Aktion: Rückgabe Verarbeitungsoptionen](custom-action-return-processing-options.md)".</span><span class="sxs-lookup"><span data-stu-id="e5c98-121">For a description of the options and the values, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="e5c98-122">Ausführungszeit Planungsoptionen</span><span class="sxs-lookup"><span data-stu-id="e5c98-122">Execution Scheduling Options</span></span>

<span data-ttu-id="e5c98-123">Schließen Sie optionale Flagbits in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um Optionen für die Ausführungsplanung anzugeben.</span><span class="sxs-lookup"><span data-stu-id="e5c98-123">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify execution scheduling options.</span></span> <span data-ttu-id="e5c98-124">Diese Optionen steuern die mehrfache Ausführung von benutzerdefinierten Aktionen.</span><span class="sxs-lookup"><span data-stu-id="e5c98-124">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="e5c98-125">Eine Beschreibung der Optionen finden Sie unter Optionen für die [Ausführungsplanung für benutzerdefinierte Aktionen](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="e5c98-125">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="e5c98-126">Ausführungs Optionen für In-Script</span><span class="sxs-lookup"><span data-stu-id="e5c98-126">In-Script Execution Options</span></span>

<span data-ttu-id="e5c98-127">Schließen Sie optionale Flagbits in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um eine in-Script-Ausführungs Option anzugeben.</span><span class="sxs-lookup"><span data-stu-id="e5c98-127">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify an in-script execution option.</span></span> <span data-ttu-id="e5c98-128">Diese Optionen kopieren den Aktions Code in das Ausführungs-, Rollback-oder Commit-Skript.</span><span class="sxs-lookup"><span data-stu-id="e5c98-128">These options copy the action code into the execution, rollback, or commit script.</span></span> <span data-ttu-id="e5c98-129">Eine Beschreibung der Optionen finden Sie unter [benutzerdefinierte Aktion In-Script Ausführungs Optionen](custom-action-in-script-execution-options.md).</span><span class="sxs-lookup"><span data-stu-id="e5c98-129">For a description of the options, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

## <a name="return-values"></a><span data-ttu-id="e5c98-130">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="e5c98-130">Return Values</span></span>

<span data-ttu-id="e5c98-131">Benutzerdefinierte Aktionen, die [ausführbare Dateien](executable-files.md) sind, müssen für Erfolg den Wert 0 zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="e5c98-131">Custom actions that are [executable files](executable-files.md) must return a value of 0 for success.</span></span> <span data-ttu-id="e5c98-132">Der Installer interpretiert jeden anderen Rückgabewert als Fehler.</span><span class="sxs-lookup"><span data-stu-id="e5c98-132">The installer interprets any other return value as failure.</span></span> <span data-ttu-id="e5c98-133">Wenn Sie Rückgabewerte ignorieren möchten, legen Sie das **msidbcustomaction typecontinue** -Bitflag im type-Feld der CustomAction-Tabelle fest.</span><span class="sxs-lookup"><span data-stu-id="e5c98-133">To ignore return values, set the **msidbCustomActionTypeContinue** bit flag in the Type field of the CustomAction table.</span></span>

## <a name="remarks"></a><span data-ttu-id="e5c98-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e5c98-134">Remarks</span></span>

<span data-ttu-id="e5c98-135">Eine benutzerdefinierte Aktion, die eine ausführbare Datei startet, benötigt eine Befehlszeile, die häufig Eigenschaften enthält, die dynamisch festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="e5c98-135">A custom action that launches an executable takes a command line, which commonly contains properties that are designated dynamically.</span></span> <span data-ttu-id="e5c98-136">Wenn es sich auch um eine [benutzerdefinierte Aktion für die verzögerte Ausführung](deferred-execution-custom-actions.md)handelt, verwendet das Installationsprogramm [**zum Erstellen**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) des Prozesses den Prozess, wenn [**die benutzerdefinierte**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) Aktion aus dem Installationsskript aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="e5c98-136">If this is also a [deferred execution custom action](deferred-execution-custom-actions.md), the installer uses [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) or [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) to create the process when the custom action is invoked from the installation script.</span></span>

<span data-ttu-id="e5c98-137">Benutzerdefinierte Aktionen, die auf eine installierte Datei als Quelle verweisen, z. b. der benutzerdefinierte Aktionstyp 18 (exe), müssen die folgenden Sequenz Einschränkungen einhalten:</span><span class="sxs-lookup"><span data-stu-id="e5c98-137">Custom actions that reference an installed file as their source, such as Custom Action Type 18 (EXE), must adhere to the following sequencing restrictions:</span></span>

-   <span data-ttu-id="e5c98-138">Die benutzerdefinierte Aktion muss nach der [costfinalize-Aktion](costfinalize-action.md)sequenziert werden.</span><span class="sxs-lookup"><span data-stu-id="e5c98-138">The custom action must be sequenced after the [CostFinalize action](costfinalize-action.md).</span></span> <span data-ttu-id="e5c98-139">Dadurch kann die benutzerdefinierte Aktion den Pfad auflösen, der zum Auffinden der exe benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="e5c98-139">This is so that the custom action can resolve the path needed to locate the EXE.</span></span>
-   <span data-ttu-id="e5c98-140">Wenn die Quelldatei nicht bereits auf dem Computer installiert ist, müssen die benutzerdefinierten Aktionen (in Skripts) dieses Typs nach der [InstallFiles-Aktion](installfiles-action.md)sequenziert werden.</span><span class="sxs-lookup"><span data-stu-id="e5c98-140">If the source file is not already installed on the computer, deferred (in-script) custom actions of this type must be sequenced after the [InstallFiles action](installfiles-action.md).</span></span>
-   <span data-ttu-id="e5c98-141">Wenn die Quelldatei nicht bereits auf dem Computer installiert ist, müssen nicht verzögerte benutzerdefinierte Aktionen dieses Typs nach der [InstallFinalize-Aktion](installfinalize-action.md)sequenziert werden.</span><span class="sxs-lookup"><span data-stu-id="e5c98-141">If the source file is not already installed on the computer, non-deferred custom actions of this type must be sequenced after the [InstallFinalize action](installfinalize-action.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e5c98-142">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e5c98-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5c98-143">Benutzerdefinierte \_ Aktionen</span><span class="sxs-lookup"><span data-stu-id="e5c98-143">Custom\_Actions</span></span>](custom-actions.md)
</dt> <dt>

[<span data-ttu-id="e5c98-144">Ausführbare Dateien</span><span class="sxs-lookup"><span data-stu-id="e5c98-144">Executable Files</span></span>](executable-files.md)
</dt> </dl>

 

 
