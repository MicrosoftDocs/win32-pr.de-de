---
description: Entwickler von Windows Installer Paketen können einen benutzerdefinierten Aktionstyp 17 verwenden, wenn die Standard Aktionen nicht ausreichen, um die Installation auszuführen.
ms.assetid: 99efd6d5-e0a3-4e66-ae55-252d19090d31
title: Benutzerdefinierter Aktionstyp 17
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b53d0046cb7515d701eb1bae3d10de0570ee5843
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348999"
---
# <a name="custom-action-type-17"></a><span data-ttu-id="41c92-103">Benutzerdefinierter Aktionstyp 17</span><span class="sxs-lookup"><span data-stu-id="41c92-103">Custom Action Type 17</span></span>

<span data-ttu-id="41c92-104">Diese benutzerdefinierte Aktion ruft eine Dynamic Link Library (dll) auf, die in C oder C++ geschrieben ist.</span><span class="sxs-lookup"><span data-stu-id="41c92-104">This custom action calls a dynamic link library (DLL) written in C or C++.</span></span>

## <a name="source"></a><span data-ttu-id="41c92-105">`Source`</span><span class="sxs-lookup"><span data-stu-id="41c92-105">Source</span></span>

<span data-ttu-id="41c92-106">Die dll wird während der aktuellen Sitzung mit der Anwendung installiert.</span><span class="sxs-lookup"><span data-stu-id="41c92-106">The DLL is installed with the application during the current session.</span></span> <span data-ttu-id="41c92-107">Das Quellfeld der [Tabelle "CustomAction](customaction-table.md) " enthält einen Schlüssel für die [Dateitabelle](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="41c92-107">The Source field of the [CustomAction table](customaction-table.md) contains a key to the [File table](file-table.md).</span></span> <span data-ttu-id="41c92-108">Der Speicherort des benutzerdefinierten Aktionscodes wird durch die Auflösung des Zielpfads für diese Datei bestimmt. Daher muss diese benutzerdefinierte Aktion aufgerufen werden, nachdem diese Datei installiert und vor dem Entfernen entfernt wurde.</span><span class="sxs-lookup"><span data-stu-id="41c92-108">The location of the custom action code is determined by the resolution of the target path for this file; therefore this custom action must be called after that file has been installed and before it is removed.</span></span>

## <a name="type-value"></a><span data-ttu-id="41c92-109">Typwert</span><span class="sxs-lookup"><span data-stu-id="41c92-109">Type Value</span></span>

<span data-ttu-id="41c92-110">Fügen Sie den folgenden Wert in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um den grundlegenden numerischen Typ anzugeben.</span><span class="sxs-lookup"><span data-stu-id="41c92-110">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type.</span></span>



| <span data-ttu-id="41c92-111">Konstanten</span><span class="sxs-lookup"><span data-stu-id="41c92-111">Constants</span></span>                                                          | <span data-ttu-id="41c92-112">Hexadezimal</span><span class="sxs-lookup"><span data-stu-id="41c92-112">Hexadecimal</span></span> | <span data-ttu-id="41c92-113">Decimal</span><span class="sxs-lookup"><span data-stu-id="41c92-113">Decimal</span></span> |
|--------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="41c92-114">**msidbcustomaktiontypedll**  +  **msidbcustomaktiontypesourcefile**</span><span class="sxs-lookup"><span data-stu-id="41c92-114">**msidbCustomActionTypeDll** + **msidbCustomActionTypeSourceFile**</span></span> | <span data-ttu-id="41c92-115">0x011</span><span class="sxs-lookup"><span data-stu-id="41c92-115">0x011</span></span>       | <span data-ttu-id="41c92-116">17</span><span class="sxs-lookup"><span data-stu-id="41c92-116">17</span></span>      |



 

## <a name="target"></a><span data-ttu-id="41c92-117">Ziel</span><span class="sxs-lookup"><span data-stu-id="41c92-117">Target</span></span>

<span data-ttu-id="41c92-118">Die dll wird über den Einstiegspunkt aufgerufen, der im Feld Ziel der [Tabelle CustomAction](customaction-table.md)benannt ist. dabei wird ein einzelnes Argument übergeben, das das Handle für die aktuelle Installationssitzung ist.</span><span class="sxs-lookup"><span data-stu-id="41c92-118">The DLL is called through the entry point named in the Target field of the [CustomAction table](customaction-table.md), passing a single argument that is the handle to the current install session.</span></span> <span data-ttu-id="41c92-119">Der in der Tabelle angegebene Einstiegspunkt Name muss mit dem aus der DLL exportierten Namen identisch sein.</span><span class="sxs-lookup"><span data-stu-id="41c92-119">The entry point name specified in the table must match that exported from the DLL.</span></span> <span data-ttu-id="41c92-120">Beachten Sie, dass die Einstiegs Funktion nicht von einem angegeben wird. Die DEF-Datei oder eine/Export: Linker-Spezifikation, der Name kann einen vorangeführenden Unterstrich und ein @4 Suffix "" aufweisen.</span><span class="sxs-lookup"><span data-stu-id="41c92-120">Note that if the entry function is not specified by a .DEF file or by a /EXPORT: linker specification, the name may have a leading underscore and a "@4" suffix.</span></span> <span data-ttu-id="41c92-121">Die aufgerufene Funktion muss die Aufruf \_ \_ Konvention stdcall angeben.</span><span class="sxs-lookup"><span data-stu-id="41c92-121">The called function must specify the \_\_stdcall calling convention.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="41c92-122">Rückgabe Verarbeitungsoptionen</span><span class="sxs-lookup"><span data-stu-id="41c92-122">Return Processing Options</span></span>

<span data-ttu-id="41c92-123">Schließen Sie optionale Flagbits in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um die Rückgabe Verarbeitungsoptionen anzugeben.</span><span class="sxs-lookup"><span data-stu-id="41c92-123">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify return processing options.</span></span> <span data-ttu-id="41c92-124">Eine Beschreibung der Optionen und Werte finden Sie unter " [benutzerdefinierte Aktion: Rückgabe Verarbeitungsoptionen](custom-action-return-processing-options.md)".</span><span class="sxs-lookup"><span data-stu-id="41c92-124">For a description of the options and the values, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="41c92-125">Ausführungszeit Planungsoptionen</span><span class="sxs-lookup"><span data-stu-id="41c92-125">Execution Scheduling Options</span></span>

<span data-ttu-id="41c92-126">Schließen Sie optionale Flagbits in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um Optionen für die Ausführungsplanung anzugeben.</span><span class="sxs-lookup"><span data-stu-id="41c92-126">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify execution scheduling options.</span></span> <span data-ttu-id="41c92-127">Diese Optionen steuern die mehrfache Ausführung von benutzerdefinierten Aktionen.</span><span class="sxs-lookup"><span data-stu-id="41c92-127">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="41c92-128">Eine Beschreibung der Optionen finden Sie unter Optionen für die [Ausführungsplanung für benutzerdefinierte Aktionen](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="41c92-128">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="41c92-129">Ausführungs Optionen für In-Script</span><span class="sxs-lookup"><span data-stu-id="41c92-129">In-Script Execution Options</span></span>

<span data-ttu-id="41c92-130">Schließen Sie optionale Flagbits in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um eine in-Script-Ausführungs Option anzugeben.</span><span class="sxs-lookup"><span data-stu-id="41c92-130">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify an in-script execution option.</span></span> <span data-ttu-id="41c92-131">Diese Optionen kopieren den Aktions Code in das Ausführungs-, Rollback-oder Commit-Skript.</span><span class="sxs-lookup"><span data-stu-id="41c92-131">These options copy the action code into the execution, rollback, or commit script.</span></span> <span data-ttu-id="41c92-132">Eine Beschreibung der Optionen finden Sie unter [benutzerdefinierte Aktion In-Script Ausführungs Optionen](custom-action-in-script-execution-options.md).</span><span class="sxs-lookup"><span data-stu-id="41c92-132">For a description of the options, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

## <a name="return-values"></a><span data-ttu-id="41c92-133">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="41c92-133">Return Values</span></span>

<span data-ttu-id="41c92-134">Siehe [Rückgabewerte für benutzerdefinierte Aktionen](custom-action-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="41c92-134">See [Custom Action Return Values](custom-action-return-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="41c92-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="41c92-135">Remarks</span></span>

<span data-ttu-id="41c92-136">Eine benutzerdefinierte Aktion, die eine Dynamic Link Library (dll) aufruft, erfordert ein Handle für die Installationssitzung.</span><span class="sxs-lookup"><span data-stu-id="41c92-136">A custom action that calls a dynamic-link library (DLL) requires a handle to the installation session.</span></span> <span data-ttu-id="41c92-137">Wenn es sich auch um eine benutzerdefinierte Aktion für die verzögerte Ausführung handelt, ist die Sitzung während der Ausführung des Installations Skripts möglicherweise nicht mehr vorhanden.</span><span class="sxs-lookup"><span data-stu-id="41c92-137">If this is also a deferred execution custom action, the session may no longer exist during execution of the installation script.</span></span> <span data-ttu-id="41c92-138">Informationen dazu, wie eine benutzerdefinierte Aktion dieses Typs Kontextinformationen abrufen kann, finden Sie unter Abrufen von [Kontextinformationen für benutzerdefinierte Aktionen der verzögerten Ausführung](obtaining-context-information-for-deferred-execution-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="41c92-138">For information on how a custom action of this type can obtain context information, see [Obtaining Context Information for Deferred Execution Custom Actions](obtaining-context-information-for-deferred-execution-custom-actions.md).</span></span>

<span data-ttu-id="41c92-139">Benutzerdefinierte Aktionen werden in einem separaten Thread ausgeführt und haben möglicherweise begrenzten Zugriff auf das System.</span><span class="sxs-lookup"><span data-stu-id="41c92-139">Custom actions execute in a separate thread, and may have limited access to the system.</span></span> <span data-ttu-id="41c92-140">Benutzerdefinierte Aktionen, die asynchron ausgeführt werden, blockieren den Hauptthread entweder beim Beenden der aktuellen Sequenz oder der Installationssitzung, bis Sie zurückkehren.</span><span class="sxs-lookup"><span data-stu-id="41c92-140">Custom actions that run asynchronously block the main thread at the termination of either the current sequence or the install session until they return.</span></span>

<span data-ttu-id="41c92-141">Benutzerdefinierte Aktionen, die auf eine installierte Datei als Quelle verweisen, z. b. benutzerdefinierter Aktionstyp 17 (dll), müssen die folgenden Sequenz Einschränkungen einhalten:</span><span class="sxs-lookup"><span data-stu-id="41c92-141">Custom actions that reference an installed file as their source, such as Custom Action Type 17 (DLL), must adhere to the following sequencing restrictions:</span></span>

-   <span data-ttu-id="41c92-142">Die benutzerdefinierte Aktion muss nach der [costfinalize-Aktion](costfinalize-action.md)sequenziert werden.</span><span class="sxs-lookup"><span data-stu-id="41c92-142">The custom action must be sequenced after the [CostFinalize action](costfinalize-action.md).</span></span> <span data-ttu-id="41c92-143">Dadurch kann die benutzerdefinierte Aktion den Pfad auflösen, der zum Auffinden der dll erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="41c92-143">This is so that the custom action can resolve the path needed to locate the DLL.</span></span>
-   <span data-ttu-id="41c92-144">Wenn die Quelldatei nicht bereits auf dem Computer installiert ist, müssen die benutzerdefinierten Aktionen (in Skripts) dieses Typs nach der [InstallFiles-Aktion](installfiles-action.md)sequenziert werden.</span><span class="sxs-lookup"><span data-stu-id="41c92-144">If the source file is not already installed on the computer, deferred (in-script) custom actions of this type must be sequenced after the [InstallFiles action](installfiles-action.md).</span></span>
-   <span data-ttu-id="41c92-145">Wenn die Quelldatei nicht bereits auf dem Computer installiert ist, müssen nicht verzögerte benutzerdefinierte Aktionen dieses Typs nach der [InstallFinalize-Aktion](installfinalize-action.md)sequenziert werden.</span><span class="sxs-lookup"><span data-stu-id="41c92-145">If the source file is not already installed on the computer, non-deferred custom actions of this type must be sequenced after the [InstallFinalize action](installfinalize-action.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="41c92-146">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="41c92-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="41c92-147">Benutzerdefinierte \_ Aktionen</span><span class="sxs-lookup"><span data-stu-id="41c92-147">Custom\_Actions</span></span>](custom-actions.md)
</dt> <dt>

[<span data-ttu-id="41c92-148">Benutzerdefinierte Aktionen für verzögerte Ausführung</span><span class="sxs-lookup"><span data-stu-id="41c92-148">Deferred Execution Custom Actions</span></span>](deferred-execution-custom-actions.md)
</dt> <dt>

[<span data-ttu-id="41c92-149">Dynamic Link Libraries</span><span class="sxs-lookup"><span data-stu-id="41c92-149">Dynamic-Link Libraries</span></span>](dynamic-link-libraries.md)
</dt> </dl>

 

 



