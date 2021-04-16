---
description: Beachten Sie, dass Sie nicht die Reihenfolge angeben können, in der der Installer mithilfe der SelfRegModules-und selfunregmodules-Aktionen selbst registrierte DLLs registriert bzw. die Registrierung aufheben kann.
ms.assetid: 46ee5ea2-35fd-4352-8a45-572d6fb5e080
title: Angeben der Reihenfolge der Selbstregistrierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d99587f6e6bdd8726f2cdc584fc2f399d81ae91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485379"
---
# <a name="specifying-the-order-of-self-registration"></a><span data-ttu-id="74dc5-103">Angeben der Reihenfolge der Selbstregistrierung</span><span class="sxs-lookup"><span data-stu-id="74dc5-103">Specifying the Order of Self Registration</span></span>

<span data-ttu-id="74dc5-104">Beachten Sie, dass Sie nicht die Reihenfolge angeben können, in der der Installer mithilfe der [SelfRegModules](selfregmodules-action.md) -und [selfunregmodules](selfunregmodules-action.md) -Aktionen selbst registrierte DLLs registriert bzw. die Registrierung aufheben kann.</span><span class="sxs-lookup"><span data-stu-id="74dc5-104">Note that you cannot specify the order in which the installer registers or unregisters self-registering DLLs by using the [SelfRegModules](selfregmodules-action.md) and [SelfUnRegModules](selfunregmodules-action.md) actions.</span></span> <span data-ttu-id="74dc5-105">Diese Aktionen registrieren alle in der [Tabelle selfreg](selfreg-table.md)aufgeführten Module.</span><span class="sxs-lookup"><span data-stu-id="74dc5-105">These actions register all the modules listed in the [SelfReg table](selfreg-table.md).</span></span> <span data-ttu-id="74dc5-106">Der Installer führt keine Selbstregistrierung von exe-Dateien durch.</span><span class="sxs-lookup"><span data-stu-id="74dc5-106">The installer does not self-register .exe files.</span></span>

<span data-ttu-id="74dc5-107">Um die Reihenfolge anzugeben, in der das Installationsprogramm Module registriert oder die Registrierung der Module aufgehoben wird, müssen Sie für jedes Modul zwei [benutzerdefinierte Aktionen](custom-actions.md) verwenden.</span><span class="sxs-lookup"><span data-stu-id="74dc5-107">To specify the order in which the installer registers or unregisters modules, you must use two [custom actions](custom-actions.md) for each module.</span></span> <span data-ttu-id="74dc5-108">Eine benutzerdefinierte Aktion für "DllRegisterServer" und eine zweite für "DllUnregisterServer".</span><span class="sxs-lookup"><span data-stu-id="74dc5-108">One custom action for DllRegisterServer and a second for DllUnregisterServer.</span></span> <span data-ttu-id="74dc5-109">Diese benutzerdefinierten Aktionen müssen dann in der [InstallExecuteSequence-Tabelle](installexecutesequence-table.md) an dem Punkt in der Sequenz erstellt werden, wo die dll registriert oder die Registrierung aufgehoben werden soll.</span><span class="sxs-lookup"><span data-stu-id="74dc5-109">These custom actions must then be authored in the [InstallExecuteSequence table](installexecutesequence-table.md) at the point in the sequence wherever the DLL is to be registered or unregistered.</span></span>

<span data-ttu-id="74dc5-110">Im folgenden Beispiel wird veranschaulicht, wie die-Datenbank erstellt wird, um die Selbstregistrierung einer DLL an einem bestimmten Punkt in der Aktions Sequenz zu planen.</span><span class="sxs-lookup"><span data-stu-id="74dc5-110">The following example illustrates how to author the database to schedule the self-registration of a DLL at a particular point in the action sequence.</span></span>

<span data-ttu-id="74dc5-111">[Dateitabelle](file-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="74dc5-111">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="74dc5-112">File</span><span class="sxs-lookup"><span data-stu-id="74dc5-112">File</span></span>  | <span data-ttu-id="74dc5-113">Komponente\_</span><span class="sxs-lookup"><span data-stu-id="74dc5-113">Component\_</span></span> | <span data-ttu-id="74dc5-114">FileName</span><span class="sxs-lookup"><span data-stu-id="74dc5-114">FileName</span></span>  | <span data-ttu-id="74dc5-115">Sequenz</span><span class="sxs-lookup"><span data-stu-id="74dc5-115">Sequence</span></span> |
|-------|-------------|-----------|----------|
| <span data-ttu-id="74dc5-116">Datei "mydll</span><span class="sxs-lookup"><span data-stu-id="74dc5-116">mydll</span></span> | <span data-ttu-id="74dc5-117">MyComponent</span><span class="sxs-lookup"><span data-stu-id="74dc5-117">myComponent</span></span> | <span data-ttu-id="74dc5-118">Mydll.dll</span><span class="sxs-lookup"><span data-stu-id="74dc5-118">Mydll.dll</span></span> | <span data-ttu-id="74dc5-119">13</span><span class="sxs-lookup"><span data-stu-id="74dc5-119">13</span></span>       |



 

<span data-ttu-id="74dc5-120">[Komponenten Tabelle](component-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="74dc5-120">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="74dc5-121">Komponente</span><span class="sxs-lookup"><span data-stu-id="74dc5-121">Component</span></span>   | <span data-ttu-id="74dc5-122">ComponentID</span><span class="sxs-lookup"><span data-stu-id="74dc5-122">ComponentId</span></span> | <span data-ttu-id="74dc5-123">Verzeichnis\_</span><span class="sxs-lookup"><span data-stu-id="74dc5-123">Directory\_</span></span> | <span data-ttu-id="74dc5-124">KEYPATH</span><span class="sxs-lookup"><span data-stu-id="74dc5-124">KeyPath</span></span> |
|-------------|-------------|-------------|---------|
| <span data-ttu-id="74dc5-125">MyComponent</span><span class="sxs-lookup"><span data-stu-id="74dc5-125">myComponent</span></span> | <span data-ttu-id="74dc5-126">{*GUID*}</span><span class="sxs-lookup"><span data-stu-id="74dc5-126">{*a GUID*}</span></span>  | <span data-ttu-id="74dc5-127">myFolder</span><span class="sxs-lookup"><span data-stu-id="74dc5-127">myFolder</span></span>    | <span data-ttu-id="74dc5-128">Datei "mydll</span><span class="sxs-lookup"><span data-stu-id="74dc5-128">mydll</span></span>   |



 

[<span data-ttu-id="74dc5-129">Verzeichnis Tabelle</span><span class="sxs-lookup"><span data-stu-id="74dc5-129">Directory Table</span></span>](directory-table.md)



| <span data-ttu-id="74dc5-130">Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="74dc5-130">Directory</span></span> | <span data-ttu-id="74dc5-131">Über \_ geordnetes Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="74dc5-131">Directory\_Parent</span></span> | <span data-ttu-id="74dc5-132">DefaultDir</span><span class="sxs-lookup"><span data-stu-id="74dc5-132">DefaultDir</span></span>          |
|-----------|-------------------|---------------------|
| <span data-ttu-id="74dc5-133">TARGETDIR</span><span class="sxs-lookup"><span data-stu-id="74dc5-133">TARGETDIR</span></span> |                   | <span data-ttu-id="74dc5-134">SourceDir</span><span class="sxs-lookup"><span data-stu-id="74dc5-134">SourceDir</span></span>           |
| <span data-ttu-id="74dc5-135">myFolder</span><span class="sxs-lookup"><span data-stu-id="74dc5-135">myFolder</span></span>  | <span data-ttu-id="74dc5-136">TARGETDIR</span><span class="sxs-lookup"><span data-stu-id="74dc5-136">TARGETDIR</span></span>         | <span data-ttu-id="74dc5-137">Ordner "MyFolder" \|</span><span class="sxs-lookup"><span data-stu-id="74dc5-137">myFolder\|My Folder</span></span> |



 

[<span data-ttu-id="74dc5-138">Tabelle "CustomAction"</span><span class="sxs-lookup"><span data-stu-id="74dc5-138">CustomAction Table</span></span>](customaction-table.md)



| <span data-ttu-id="74dc5-139">Aktion</span><span class="sxs-lookup"><span data-stu-id="74dc5-139">Action</span></span>     | <span data-ttu-id="74dc5-140">type</span><span class="sxs-lookup"><span data-stu-id="74dc5-140">Type</span></span> | <span data-ttu-id="74dc5-141">`Source`</span><span class="sxs-lookup"><span data-stu-id="74dc5-141">Source</span></span>   | <span data-ttu-id="74dc5-142">Ziel</span><span class="sxs-lookup"><span data-stu-id="74dc5-142">Target</span></span>                                     |
|------------|------|----------|--------------------------------------------|
| <span data-ttu-id="74dc5-143">mydllreg</span><span class="sxs-lookup"><span data-stu-id="74dc5-143">mydllREG</span></span>   | <span data-ttu-id="74dc5-144">3170</span><span class="sxs-lookup"><span data-stu-id="74dc5-144">3170</span></span> | <span data-ttu-id="74dc5-145">myFolder</span><span class="sxs-lookup"><span data-stu-id="74dc5-145">myFolder</span></span> | <span data-ttu-id="74dc5-146">" \[ System Folder \] msiexec"/y " \[ \# Datei" myDll \] "</span><span class="sxs-lookup"><span data-stu-id="74dc5-146">"\[SystemFolder\]msiexec" /y "\[\#mydll\]"</span></span> |
| <span data-ttu-id="74dc5-147">mydllunreg</span><span class="sxs-lookup"><span data-stu-id="74dc5-147">mydllUNREG</span></span> | <span data-ttu-id="74dc5-148">3170</span><span class="sxs-lookup"><span data-stu-id="74dc5-148">3170</span></span> | <span data-ttu-id="74dc5-149">myFolder</span><span class="sxs-lookup"><span data-stu-id="74dc5-149">myFolder</span></span> | <span data-ttu-id="74dc5-150">" \[ System Folder \] msiexec" "/z" \[ \# Datei "myDll \] "</span><span class="sxs-lookup"><span data-stu-id="74dc5-150">"\[SystemFolder\]msiexec" /z "\[\#mydll\]"</span></span> |



 

<span data-ttu-id="74dc5-151">[InstallExecuteSequence-Tabelle](installexecutesequence-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="74dc5-151">[InstallExecuteSequence Table](installexecutesequence-table.md) (partial)</span></span>



| <span data-ttu-id="74dc5-152">Aktion</span><span class="sxs-lookup"><span data-stu-id="74dc5-152">Action</span></span>           | <span data-ttu-id="74dc5-153">Bedingung</span><span class="sxs-lookup"><span data-stu-id="74dc5-153">Condition</span></span>         | <span data-ttu-id="74dc5-154">Sequenz</span><span class="sxs-lookup"><span data-stu-id="74dc5-154">Sequence</span></span> |
|------------------|-------------------|----------|
| <span data-ttu-id="74dc5-155">Selfunregmodules</span><span class="sxs-lookup"><span data-stu-id="74dc5-155">SelfUnregModules</span></span> |                   | <span data-ttu-id="74dc5-156">2200</span><span class="sxs-lookup"><span data-stu-id="74dc5-156">2200</span></span>     |
| <span data-ttu-id="74dc5-157">mydllunreg</span><span class="sxs-lookup"><span data-stu-id="74dc5-157">mydllUNREG</span></span>       | <span data-ttu-id="74dc5-158">$MyComponent = 2</span><span class="sxs-lookup"><span data-stu-id="74dc5-158">$myComponent=2</span></span>    | <span data-ttu-id="74dc5-159">2201</span><span class="sxs-lookup"><span data-stu-id="74dc5-159">2201</span></span>     |
| <span data-ttu-id="74dc5-160">RemoveFiles</span><span class="sxs-lookup"><span data-stu-id="74dc5-160">RemoveFiles</span></span>      |                   | <span data-ttu-id="74dc5-161">3500</span><span class="sxs-lookup"><span data-stu-id="74dc5-161">3500</span></span>     |
| <span data-ttu-id="74dc5-162">InstallFiles</span><span class="sxs-lookup"><span data-stu-id="74dc5-162">InstallFiles</span></span>     |                   | <span data-ttu-id="74dc5-163">4000</span><span class="sxs-lookup"><span data-stu-id="74dc5-163">4000</span></span>     |
| <span data-ttu-id="74dc5-164">SelfRegModules</span><span class="sxs-lookup"><span data-stu-id="74dc5-164">SelfRegModules</span></span>   |                   | <span data-ttu-id="74dc5-165">6500</span><span class="sxs-lookup"><span data-stu-id="74dc5-165">6500</span></span>     |
| <span data-ttu-id="74dc5-166">mydllreg</span><span class="sxs-lookup"><span data-stu-id="74dc5-166">mydllREG</span></span>         | <span data-ttu-id="74dc5-167">$MyComponent>2</span><span class="sxs-lookup"><span data-stu-id="74dc5-167">$myComponent>2</span></span> | <span data-ttu-id="74dc5-168">6501</span><span class="sxs-lookup"><span data-stu-id="74dc5-168">6501</span></span>     |



 

 

 



