---
description: Entwickler von Windows Installer Paketen können einen benutzerdefinierten Aktionstyp 22 verwenden, wenn die Standard Aktionen nicht ausreichen, um die Installation auszuführen.
ms.assetid: 6838f59b-e1bc-42c6-a7fe-3d32791adfac
title: Benutzerdefinierter Aktionstyp 22
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a00b4772b1d2532c0291223cc5c4b6a63ead9324
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350629"
---
# <a name="custom-action-type-22"></a><span data-ttu-id="69d35-103">Benutzerdefinierter Aktionstyp 22</span><span class="sxs-lookup"><span data-stu-id="69d35-103">Custom Action Type 22</span></span>

<span data-ttu-id="69d35-104">Diese benutzerdefinierte Aktion wird in VBScript geschrieben.</span><span class="sxs-lookup"><span data-stu-id="69d35-104">This custom action is written in VBScript.</span></span> <span data-ttu-id="69d35-105">Siehe auch [Skripts](scripts.md).</span><span class="sxs-lookup"><span data-stu-id="69d35-105">See also [Scripts](scripts.md).</span></span>

## <a name="source"></a><span data-ttu-id="69d35-106">`Source`</span><span class="sxs-lookup"><span data-stu-id="69d35-106">Source</span></span>

<span data-ttu-id="69d35-107">Das Skript wird während der aktuellen Sitzung mit der Anwendung installiert.</span><span class="sxs-lookup"><span data-stu-id="69d35-107">The script is installed with the application during the current session.</span></span> <span data-ttu-id="69d35-108">Das Quellfeld der [Tabelle "CustomAction](customaction-table.md) " enthält einen Schlüssel für die [Dateitabelle](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="69d35-108">The Source field of the [CustomAction table](customaction-table.md) contains a key to the [File table](file-table.md).</span></span> <span data-ttu-id="69d35-109">Der Speicherort des benutzerdefinierten Aktionscodes wird durch die Auflösung des Zielpfads für diese Datei bestimmt. Daher muss diese benutzerdefinierte Aktion aufgerufen werden, nachdem die Datei installiert und vor dem Entfernen entfernt wurde.</span><span class="sxs-lookup"><span data-stu-id="69d35-109">The location of the custom action code is determined by the resolution of the target path for this file; therefore this custom action must be called after the file has been installed and before it is removed.</span></span>

## <a name="type-value"></a><span data-ttu-id="69d35-110">Typwert</span><span class="sxs-lookup"><span data-stu-id="69d35-110">Type Value</span></span>

<span data-ttu-id="69d35-111">Fügen Sie den folgenden Wert in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um den grundlegenden numerischen Typ einer benutzerdefinierten 32-Bit-Aktion anzugeben.</span><span class="sxs-lookup"><span data-stu-id="69d35-111">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type of a 32-bit custom action.</span></span>



| <span data-ttu-id="69d35-112">Konstanten</span><span class="sxs-lookup"><span data-stu-id="69d35-112">Constants</span></span>                                                               | <span data-ttu-id="69d35-113">Hexadezimal</span><span class="sxs-lookup"><span data-stu-id="69d35-113">Hexadecimal</span></span> | <span data-ttu-id="69d35-114">Decimal</span><span class="sxs-lookup"><span data-stu-id="69d35-114">Decimal</span></span> |
|-------------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="69d35-115">**msidbcustomaktiontypevbscript**  +  **msidbcustomaktiontypesourcefile**</span><span class="sxs-lookup"><span data-stu-id="69d35-115">**msidbCustomActionTypeVBScript** + **msidbCustomActionTypeSourceFile**</span></span> | <span data-ttu-id="69d35-116">0x016</span><span class="sxs-lookup"><span data-stu-id="69d35-116">0x016</span></span>       | <span data-ttu-id="69d35-117">22</span><span class="sxs-lookup"><span data-stu-id="69d35-117">22</span></span>      |



 

<span data-ttu-id="69d35-118">Windows Installer können benutzerdefinierte 64-Bit-Aktionen auf 64-Bit-Betriebssystemen verwenden.</span><span class="sxs-lookup"><span data-stu-id="69d35-118">Windows Installer may use 64-bit custom actions on 64-bit operating systems.</span></span> <span data-ttu-id="69d35-119">Eine benutzerdefinierte 64-Bit-Aktion, die auf Skripts basiert, muss das **msidbCustomActionType64BitScript** -Bit in den numerischen Typ einschließen.</span><span class="sxs-lookup"><span data-stu-id="69d35-119">A 64-bit custom action based on scripts must include the **msidbCustomActionType64BitScript** bit in its numeric type.</span></span> <span data-ttu-id="69d35-120">Weitere Informationen finden Sie unter [benutzerdefinierte 64-Bit-Aktionen](64-bit-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="69d35-120">For information see [64-bit Custom Actions](64-bit-custom-actions.md).</span></span> <span data-ttu-id="69d35-121">Fügen Sie den folgenden Wert in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um den grundlegenden numerischen Typ einer benutzerdefinierten 64-Bit-Aktion anzugeben.</span><span class="sxs-lookup"><span data-stu-id="69d35-121">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type of a 64-bit custom action.</span></span>



| <span data-ttu-id="69d35-122">Konstanten</span><span class="sxs-lookup"><span data-stu-id="69d35-122">Constants</span></span>                                                                                                      | <span data-ttu-id="69d35-123">Hexadezimal</span><span class="sxs-lookup"><span data-stu-id="69d35-123">Hexadecimal</span></span> | <span data-ttu-id="69d35-124">Decimal</span><span class="sxs-lookup"><span data-stu-id="69d35-124">Decimal</span></span> |
|----------------------------------------------------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="69d35-125">**msidbcustomaktiontypevbscript**  +  **msidbcustomaktiontypesourcefile**  +  **msidbCustomActionType64BitScript**</span><span class="sxs-lookup"><span data-stu-id="69d35-125">**msidbCustomActionTypeVBScript** + **msidbCustomActionTypeSourceFile** + **msidbCustomActionType64BitScript**</span></span> | <span data-ttu-id="69d35-126">0x0001016</span><span class="sxs-lookup"><span data-stu-id="69d35-126">0x0001016</span></span>   | <span data-ttu-id="69d35-127">4118</span><span class="sxs-lookup"><span data-stu-id="69d35-127">4118</span></span>    |



 

## <a name="target"></a><span data-ttu-id="69d35-128">Ziel</span><span class="sxs-lookup"><span data-stu-id="69d35-128">Target</span></span>

<span data-ttu-id="69d35-129">Das Zielfeld der [CustomAction-Tabelle](customaction-table.md) enthält eine optionale Skriptfunktion.</span><span class="sxs-lookup"><span data-stu-id="69d35-129">The Target field of the [CustomAction table](customaction-table.md) contains an optional script function.</span></span> <span data-ttu-id="69d35-130">Die Verarbeitung sendet zuerst das Skript für die Verarbeitung und ruft dann die optionale Skriptfunktion auf.</span><span class="sxs-lookup"><span data-stu-id="69d35-130">Processing first sends the script for parsing and then calls the optional script function.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="69d35-131">Rückgabe Verarbeitungsoptionen</span><span class="sxs-lookup"><span data-stu-id="69d35-131">Return Processing Options</span></span>

<span data-ttu-id="69d35-132">Schließen Sie optionale Flagbits in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um die Rückgabe Verarbeitungsoptionen anzugeben.</span><span class="sxs-lookup"><span data-stu-id="69d35-132">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify return processing options.</span></span> <span data-ttu-id="69d35-133">Eine Beschreibung der Optionen und Werte finden Sie unter " [benutzerdefinierte Aktion: Rückgabe Verarbeitungsoptionen](custom-action-return-processing-options.md)".</span><span class="sxs-lookup"><span data-stu-id="69d35-133">For a description of the options and the values, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="69d35-134">Ausführungszeit Planungsoptionen</span><span class="sxs-lookup"><span data-stu-id="69d35-134">Execution Scheduling Options</span></span>

<span data-ttu-id="69d35-135">Schließen Sie optionale Flagbits in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um Optionen für die Ausführungsplanung anzugeben.</span><span class="sxs-lookup"><span data-stu-id="69d35-135">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify execution scheduling options.</span></span> <span data-ttu-id="69d35-136">Diese Optionen steuern die mehrfache Ausführung von benutzerdefinierten Aktionen.</span><span class="sxs-lookup"><span data-stu-id="69d35-136">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="69d35-137">Eine Beschreibung der Optionen finden Sie unter Optionen für die [Ausführungsplanung für benutzerdefinierte Aktionen](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="69d35-137">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="69d35-138">Ausführungs Optionen für In-Script</span><span class="sxs-lookup"><span data-stu-id="69d35-138">In-Script Execution Options</span></span>

<span data-ttu-id="69d35-139">Schließen Sie optionale Flagbits in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um eine in-Script-Ausführungs Option anzugeben.</span><span class="sxs-lookup"><span data-stu-id="69d35-139">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify an in-script execution option.</span></span> <span data-ttu-id="69d35-140">Diese Optionen kopieren den Aktions Code in das Ausführungs-, Rollback-oder Commit-Skript.</span><span class="sxs-lookup"><span data-stu-id="69d35-140">These options copy the action code into the execution, rollback, or commit script.</span></span> <span data-ttu-id="69d35-141">Eine Beschreibung der Optionen finden Sie unter [benutzerdefinierte Aktion In-Script Ausführungs Optionen](custom-action-in-script-execution-options.md).</span><span class="sxs-lookup"><span data-stu-id="69d35-141">For a description of the options, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

## <a name="return-values"></a><span data-ttu-id="69d35-142">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="69d35-142">Return Values</span></span>

<span data-ttu-id="69d35-143">Optionale Funktionen, die im Skript geschrieben werden, müssen einen der Werte zurückgeben, die unter [Rückgabewerte der benutzerdefinierten Aktionen JScript und VBScript](return-values-of-jscript-and-vbscript-custom-actions.md)beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="69d35-143">Optional functions written in script must return one of the values described in [Return Values of JScript and VBScript Custom Actions](return-values-of-jscript-and-vbscript-custom-actions.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="69d35-144">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="69d35-144">Remarks</span></span>

<span data-ttu-id="69d35-145">Für eine benutzerdefinierte Aktion, die in JScript oder VBScript geschrieben ist, ist das install [**Session-Objekt**](session-object.md)erforderlich.</span><span class="sxs-lookup"><span data-stu-id="69d35-145">A custom action that is written in JScript or VBScript requires the install [**Session Object**](session-object.md).</span></span> <span data-ttu-id="69d35-146">Dies ist vom Typ **Sitzungs Objekt** , und das Installationsprogramm fügt es dem Skript mit dem Namen "Session" an.</span><span class="sxs-lookup"><span data-stu-id="69d35-146">This is of the type **Session Object** and the installer attaches it to the script with the name "Session".</span></span> <span data-ttu-id="69d35-147">Da das **Sitzungs** Objekt während eines Installations Rollbacks möglicherweise nicht vorhanden ist, muss eine verzögerte benutzerdefinierte Aktion, die im Skript geschrieben ist, eine der Methoden oder Eigenschaften des **Sitzungs** Objekts verwenden, das im Abschnitt Abrufen von [Kontextinformationen für benutzerdefinierte Aktionen für die verzögerte Ausführung](obtaining-context-information-for-deferred-execution-custom-actions.md) beschrieben wird, um den Kontext abzurufen.</span><span class="sxs-lookup"><span data-stu-id="69d35-147">Because the **Session** object may not exist during an installation rollback, a deferred custom action written in script must use one of the methods or properties of the **Session** object described in the section [Obtaining Context Information for Deferred Execution Custom Actions](obtaining-context-information-for-deferred-execution-custom-actions.md) to retrieve its context.</span></span>

<span data-ttu-id="69d35-148">Benutzerdefinierte Aktionen, die auf eine installierte Datei als Quelle verweisen, z. b. benutzerdefinierter Aktionstyp 22 (vbcript), müssen die folgenden Sequenz Einschränkungen einhalten:</span><span class="sxs-lookup"><span data-stu-id="69d35-148">Custom actions that reference an installed file as their source, such as Custom Action Type 22 (VBcript), must adhere to the following sequencing restrictions:</span></span>

-   <span data-ttu-id="69d35-149">Die benutzerdefinierte Aktion muss nach der [costfinalize-Aktion](costfinalize-action.md)sequenziert werden.</span><span class="sxs-lookup"><span data-stu-id="69d35-149">The custom action must be sequenced after the [CostFinalize action](costfinalize-action.md).</span></span> <span data-ttu-id="69d35-150">Dadurch kann die benutzerdefinierte Aktion den Pfad auflösen, der zum Auffinden der Quelldatei, die das VBScript enthält, benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="69d35-150">This is so that the custom action can resolve the path needed to locate the source file containing the VBScript.</span></span>
-   <span data-ttu-id="69d35-151">Wenn die Quelldatei nicht bereits auf dem Computer installiert ist, müssen die benutzerdefinierten Aktionen (in Skripts) dieses Typs nach der [InstallFiles-Aktion](installfiles-action.md)sequenziert werden.</span><span class="sxs-lookup"><span data-stu-id="69d35-151">If the source file is not already installed on the computer, deferred (in-script) custom actions of this type must be sequenced after the [InstallFiles action](installfiles-action.md).</span></span>
-   <span data-ttu-id="69d35-152">Wenn die Quelldatei nicht bereits auf dem Computer installiert ist, müssen nicht verzögerte benutzerdefinierte Aktionen dieses Typs nach der [InstallFinalize-Aktion](installfinalize-action.md)sequenziert werden.</span><span class="sxs-lookup"><span data-stu-id="69d35-152">If the source file is not already installed on the computer, non-deferred custom actions of this type must be sequenced after the [InstallFinalize action](installfinalize-action.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="69d35-153">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="69d35-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="69d35-154">Benutzerdefinierte \_ Aktionen</span><span class="sxs-lookup"><span data-stu-id="69d35-154">Custom\_Actions</span></span>](custom-actions.md)
</dt> </dl>

 

 



