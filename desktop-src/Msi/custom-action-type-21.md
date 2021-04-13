---
description: Entwickler von Windows Installer Paketen können einen benutzerdefinierten Aktionstyp 21 verwenden, wenn die Standard Aktionen nicht ausreichen, um die Installation auszuführen.
ms.assetid: 0b28ad22-4e3a-49f2-8eed-2341a91eb67c
title: Benutzerdefinierter Aktionstyp 21
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c5bb7482c2f7c7b6cbd85af7a6f01cc83edbb89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348998"
---
# <a name="custom-action-type-21"></a><span data-ttu-id="f9e71-103">Benutzerdefinierter Aktionstyp 21</span><span class="sxs-lookup"><span data-stu-id="f9e71-103">Custom Action Type 21</span></span>

<span data-ttu-id="f9e71-104">Diese benutzerdefinierte Aktion wird in JScript geschrieben, z. b. ECMA 262.</span><span class="sxs-lookup"><span data-stu-id="f9e71-104">This custom action is written in JScript, such as ECMA 262.</span></span> <span data-ttu-id="f9e71-105">Die Windows Installer unterstützt JScript 1,0 nicht.</span><span class="sxs-lookup"><span data-stu-id="f9e71-105">Windows Installer does not support JScript 1.0.</span></span> <span data-ttu-id="f9e71-106">Weitere Informationen finden Sie unter [Skripts](scripts.md).</span><span class="sxs-lookup"><span data-stu-id="f9e71-106">For more information, see [Scripts](scripts.md).</span></span>

## <a name="source"></a><span data-ttu-id="f9e71-107">`Source`</span><span class="sxs-lookup"><span data-stu-id="f9e71-107">Source</span></span>

<span data-ttu-id="f9e71-108">Das Skript wird während der aktuellen Sitzung mit der Anwendung installiert.</span><span class="sxs-lookup"><span data-stu-id="f9e71-108">The script is installed with the application during the current session.</span></span> <span data-ttu-id="f9e71-109">Das Quellfeld der [Tabelle "CustomAction](customaction-table.md) " enthält einen Schlüssel für die [Dateitabelle](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="f9e71-109">The Source field of the [CustomAction table](customaction-table.md) contains a key to the [File table](file-table.md).</span></span> <span data-ttu-id="f9e71-110">Der Speicherort des benutzerdefinierten Aktionscodes wird durch die Auflösung des Zielpfads für diese Datei bestimmt. Daher muss diese benutzerdefinierte Aktion aufgerufen werden, nachdem die Datei installiert und vor dem Entfernen entfernt wurde.</span><span class="sxs-lookup"><span data-stu-id="f9e71-110">The location of the custom action code is determined by the resolution of the target path for this file; therefore this custom action must be called after the file has been installed and before it is removed.</span></span>

## <a name="type-value"></a><span data-ttu-id="f9e71-111">Typwert</span><span class="sxs-lookup"><span data-stu-id="f9e71-111">Type Value</span></span>

<span data-ttu-id="f9e71-112">Fügen Sie den folgenden Wert in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um den grundlegenden numerischen Typ einer benutzerdefinierten 32-Bit-Aktion anzugeben.</span><span class="sxs-lookup"><span data-stu-id="f9e71-112">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type of a 32-bit custom action.</span></span>



| <span data-ttu-id="f9e71-113">Konstanten</span><span class="sxs-lookup"><span data-stu-id="f9e71-113">Constants</span></span>                                                              | <span data-ttu-id="f9e71-114">Hexadezimal</span><span class="sxs-lookup"><span data-stu-id="f9e71-114">Hexadecimal</span></span> | <span data-ttu-id="f9e71-115">Decimal</span><span class="sxs-lookup"><span data-stu-id="f9e71-115">Decimal</span></span> |
|------------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="f9e71-116">**msidbcustomaktiontypejscript**  +  **msidbcustomaktiontypesourcefile**</span><span class="sxs-lookup"><span data-stu-id="f9e71-116">**msidbCustomActionTypeJScript** + **msidbCustomActionTypeSourceFile**</span></span> | <span data-ttu-id="f9e71-117">0x015</span><span class="sxs-lookup"><span data-stu-id="f9e71-117">0x015</span></span>       | <span data-ttu-id="f9e71-118">21</span><span class="sxs-lookup"><span data-stu-id="f9e71-118">21</span></span>      |



 

<span data-ttu-id="f9e71-119">Windows Installer können [benutzerdefinierte 64-Bit-Aktionen](64-bit-custom-actions.md) auf 64-Bit-Betriebssystemen verwenden.</span><span class="sxs-lookup"><span data-stu-id="f9e71-119">Windows Installer may use [64-bit Custom Actions](64-bit-custom-actions.md) on 64-bit operating systems.</span></span> <span data-ttu-id="f9e71-120">Eine benutzerdefinierte 64-Bit-Aktion, die auf Skripts basiert, muss das **msidbCustomActionType64BitScript** -Bit in den numerischen Typ einschließen.</span><span class="sxs-lookup"><span data-stu-id="f9e71-120">A 64-bit custom action based on scripts must include the **msidbCustomActionType64BitScript** bit in its numeric type.</span></span> <span data-ttu-id="f9e71-121">Weitere Informationen finden Sie unter benutzerdefinierte 64-Bit-Aktionen.</span><span class="sxs-lookup"><span data-stu-id="f9e71-121">For information see 64-bit Custom Actions.</span></span> <span data-ttu-id="f9e71-122">Fügen Sie den folgenden Wert in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um den grundlegenden numerischen Typ einer benutzerdefinierten 64-Bit-Aktion anzugeben.</span><span class="sxs-lookup"><span data-stu-id="f9e71-122">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type of a 64-bit custom action.</span></span>



| <span data-ttu-id="f9e71-123">Konstanten</span><span class="sxs-lookup"><span data-stu-id="f9e71-123">Constants</span></span>                                                                                                     | <span data-ttu-id="f9e71-124">Hexadezimal</span><span class="sxs-lookup"><span data-stu-id="f9e71-124">Hexadecimal</span></span> | <span data-ttu-id="f9e71-125">Decimal</span><span class="sxs-lookup"><span data-stu-id="f9e71-125">Decimal</span></span> |
|---------------------------------------------------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="f9e71-126">**msidbcustomaktiontypejscript**  +  **msidbcustomaktiontypesourcefile**  +  **msidbCustomActionType64BitScript**</span><span class="sxs-lookup"><span data-stu-id="f9e71-126">**msidbCustomActionTypeJScript** + **msidbCustomActionTypeSourceFile** + **msidbCustomActionType64BitScript**</span></span> | <span data-ttu-id="f9e71-127">0x0001015</span><span class="sxs-lookup"><span data-stu-id="f9e71-127">0x0001015</span></span>   | <span data-ttu-id="f9e71-128">4117</span><span class="sxs-lookup"><span data-stu-id="f9e71-128">4117</span></span>    |



 

## <a name="target"></a><span data-ttu-id="f9e71-129">Ziel</span><span class="sxs-lookup"><span data-stu-id="f9e71-129">Target</span></span>

<span data-ttu-id="f9e71-130">Das Zielfeld der [CustomAction-Tabelle](customaction-table.md) enthält eine optionale Skriptfunktion.</span><span class="sxs-lookup"><span data-stu-id="f9e71-130">The Target field of the [CustomAction table](customaction-table.md) contains an optional script function.</span></span> <span data-ttu-id="f9e71-131">Die Verarbeitung sendet zuerst das Skript für die Verarbeitung und ruft dann die optionale Skriptfunktion auf.</span><span class="sxs-lookup"><span data-stu-id="f9e71-131">Processing first sends the script for parsing and then calls the optional script function.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="f9e71-132">Rückgabe Verarbeitungsoptionen</span><span class="sxs-lookup"><span data-stu-id="f9e71-132">Return Processing Options</span></span>

<span data-ttu-id="f9e71-133">Schließen Sie optionale Flagbits in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um die Rückgabe Verarbeitungsoptionen anzugeben.</span><span class="sxs-lookup"><span data-stu-id="f9e71-133">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify return processing options.</span></span> <span data-ttu-id="f9e71-134">Eine Beschreibung der Optionen und Werte finden Sie unter " [benutzerdefinierte Aktion: Rückgabe Verarbeitungsoptionen](custom-action-return-processing-options.md)".</span><span class="sxs-lookup"><span data-stu-id="f9e71-134">For a description of the options and the values, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="f9e71-135">Ausführungszeit Planungsoptionen</span><span class="sxs-lookup"><span data-stu-id="f9e71-135">Execution Scheduling Options</span></span>

<span data-ttu-id="f9e71-136">Schließen Sie optionale Flagbits in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um Optionen für die Ausführungsplanung anzugeben.</span><span class="sxs-lookup"><span data-stu-id="f9e71-136">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify execution scheduling options.</span></span> <span data-ttu-id="f9e71-137">Diese Optionen steuern die mehrfache Ausführung von benutzerdefinierten Aktionen.</span><span class="sxs-lookup"><span data-stu-id="f9e71-137">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="f9e71-138">Eine Beschreibung der Optionen finden Sie unter Optionen für die [Ausführungsplanung für benutzerdefinierte Aktionen](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="f9e71-138">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="f9e71-139">Ausführungs Optionen für In-Script</span><span class="sxs-lookup"><span data-stu-id="f9e71-139">In-Script Execution Options</span></span>

<span data-ttu-id="f9e71-140">Schließen Sie optionale Flagbits in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um eine in-Script-Ausführungs Option anzugeben.</span><span class="sxs-lookup"><span data-stu-id="f9e71-140">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify an in-script execution option.</span></span> <span data-ttu-id="f9e71-141">Diese Optionen kopieren den Aktions Code in das Ausführungs-, Rollback-oder Commit-Skript.</span><span class="sxs-lookup"><span data-stu-id="f9e71-141">These options copy the action code into the execution, rollback, or commit script.</span></span> <span data-ttu-id="f9e71-142">Eine Beschreibung der Optionen finden Sie unter [benutzerdefinierte Aktion In-Script Ausführungs Optionen](custom-action-in-script-execution-options.md).</span><span class="sxs-lookup"><span data-stu-id="f9e71-142">For a description of the options, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

## <a name="return-values"></a><span data-ttu-id="f9e71-143">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="f9e71-143">Return Values</span></span>

<span data-ttu-id="f9e71-144">Optionale Funktionen, die im Skript geschrieben werden, müssen einen der Werte zurückgeben, die unter [Rückgabewerte der benutzerdefinierten Aktionen JScript und VBScript](return-values-of-jscript-and-vbscript-custom-actions.md)beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="f9e71-144">Optional functions written in script must return one of the values described in [Return Values of JScript and VBScript Custom Actions](return-values-of-jscript-and-vbscript-custom-actions.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f9e71-145">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f9e71-145">Remarks</span></span>

<span data-ttu-id="f9e71-146">Eine benutzerdefinierte Aktion, die in JScript oder VBScript geschrieben ist, erfordert das Installations [**Sitzungs**](session-object.md) Objekt.</span><span class="sxs-lookup"><span data-stu-id="f9e71-146">A custom action that is written in JScript or VBScript requires the installation [**Session**](session-object.md) object.</span></span> <span data-ttu-id="f9e71-147">Das Installationsprogramm fügt das **Sitzungs Objekt** mit dem Namen "Session" an das Skript an.</span><span class="sxs-lookup"><span data-stu-id="f9e71-147">The installer attaches the **Session Object** to the script with the name "Session".</span></span> <span data-ttu-id="f9e71-148">Da das **Sitzungs** Objekt während eines Installations Rollbacks möglicherweise nicht vorhanden ist, muss eine verzögerte benutzerdefinierte Aktion, die im Skript geschrieben ist, eine der Methoden oder Eigenschaften des **Sitzungs** Objekts verwenden, das im Abschnitt Abrufen von [Kontextinformationen für benutzerdefinierte Aktionen für die verzögerte Ausführung](obtaining-context-information-for-deferred-execution-custom-actions.md) beschrieben wird, um den Kontext abzurufen.</span><span class="sxs-lookup"><span data-stu-id="f9e71-148">Because the **Session** object may not exist during an installation rollback, a deferred custom action written in script must use one of the methods or properties of the **Session** object described in the section [Obtaining Context Information for Deferred Execution Custom Actions](obtaining-context-information-for-deferred-execution-custom-actions.md) to retrieve its context.</span></span>

<span data-ttu-id="f9e71-149">Benutzerdefinierte Aktionen, die auf eine installierte Datei als Quelle verweisen, z. b. benutzerdefinierter Aktionstyp 21 (JScript), müssen die folgenden Sequenz Einschränkungen einhalten:</span><span class="sxs-lookup"><span data-stu-id="f9e71-149">Custom actions that reference an installed file as their source, such as Custom Action Type 21 (JScript), must adhere to the following sequencing restrictions:</span></span>

-   <span data-ttu-id="f9e71-150">Die benutzerdefinierte Aktion muss nach der [costfinalize-Aktion](costfinalize-action.md)sequenziert werden.</span><span class="sxs-lookup"><span data-stu-id="f9e71-150">The custom action must be sequenced after the [CostFinalize action](costfinalize-action.md).</span></span> <span data-ttu-id="f9e71-151">Dadurch kann die benutzerdefinierte Aktion den Pfad auflösen, der zum Auffinden der Quelldatei, die das JScript enthält, benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="f9e71-151">This is so that the custom action can resolve the path needed to locate the source file containing the JScript.</span></span>
-   <span data-ttu-id="f9e71-152">Wenn die Quelldatei nicht bereits auf dem Computer installiert ist, müssen die benutzerdefinierten Aktionen (in Skripts) dieses Typs nach der [InstallFiles-Aktion](installfiles-action.md)sequenziert werden.</span><span class="sxs-lookup"><span data-stu-id="f9e71-152">If the source file is not already installed on the computer, deferred (in-script) custom actions of this type must be sequenced after the [InstallFiles action](installfiles-action.md).</span></span>
-   <span data-ttu-id="f9e71-153">Wenn die Quelldatei nicht bereits auf dem Computer installiert ist, müssen nicht verzögerte benutzerdefinierte Aktionen dieses Typs nach der [InstallFinalize-Aktion](installfinalize-action.md)sequenziert werden.</span><span class="sxs-lookup"><span data-stu-id="f9e71-153">If the source file is not already installed on the computer, non-deferred custom actions of this type must be sequenced after the [InstallFinalize action](installfinalize-action.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f9e71-154">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f9e71-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f9e71-155">Benutzerdefinierte \_ Aktionen</span><span class="sxs-lookup"><span data-stu-id="f9e71-155">Custom\_Actions</span></span>](custom-actions.md)
</dt> </dl>

 

 



