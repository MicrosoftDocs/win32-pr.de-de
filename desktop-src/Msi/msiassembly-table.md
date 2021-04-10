---
description: Die MsiAssembly-Tabelle gibt Windows Installer Einstellungen für Microsoft .net Frameworkassemblys und Win32-Assemblys an Weitere Informationen finden Sie unter Installieren von Assemblys im globalen Assemblycache und Installieren von Win32-Assemblys.
ms.assetid: 3a8cd206-0112-4840-8c9d-773483f5c771
title: MsiAssembly-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b54bd6e58e2ff6d12c582309c23856a7bb825b2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960835"
---
# <a name="msiassembly-table"></a><span data-ttu-id="5bc36-104">MsiAssembly-Tabelle</span><span class="sxs-lookup"><span data-stu-id="5bc36-104">MsiAssembly Table</span></span>

<span data-ttu-id="5bc36-105">Die MsiAssembly-Tabelle gibt Windows Installer Einstellungen für Microsoft .net Frameworkassemblys und Win32-Assemblys an</span><span class="sxs-lookup"><span data-stu-id="5bc36-105">The MsiAssembly Table specifies Windows Installer settings for Microsoft .NET Framework assemblies and Win32 assemblies.</span></span> <span data-ttu-id="5bc36-106">Weitere Informationen finden Sie unter [Installieren von](installation-of-assemblies-to-the-global-assembly-cache.md) Assemblys im globalen Assemblycache und [Installieren von Win32](installation-of-win32-assemblies.md)-Assemblys.</span><span class="sxs-lookup"><span data-stu-id="5bc36-106">For more information, see [Installation of Assemblies to the Global Assembly Cache](installation-of-assemblies-to-the-global-assembly-cache.md) and [Installation of Win32 Assemblies](installation-of-win32-assemblies.md).</span></span>

<span data-ttu-id="5bc36-107">Unter Windows XP können Windows Installer [Win32-Assemblys als parallele](side-by-side-assemblies.md)Assemblys installieren.</span><span class="sxs-lookup"><span data-stu-id="5bc36-107">On Windows XP, Windows Installer can install Win32 assemblies as [side-by-side assemblies](side-by-side-assemblies.md).</span></span> <span data-ttu-id="5bc36-108">Weitere Informationen finden Sie in der [API](../sbscs/side-by-side-assembly-api.md)für parallele Assemblys.</span><span class="sxs-lookup"><span data-stu-id="5bc36-108">For more information, see the [Side-by-Side Assembly API](../sbscs/side-by-side-assembly-api.md).</span></span>

<span data-ttu-id="5bc36-109">**Windows 2000:** Diese Funktion wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5bc36-109">**Windows 2000:** This feature is not supported.</span></span>

<span data-ttu-id="5bc36-110">Die MsiAssembly-Tabelle weist die folgenden Spalten auf.</span><span class="sxs-lookup"><span data-stu-id="5bc36-110">The MsiAssembly Table has the following columns.</span></span>



| <span data-ttu-id="5bc36-111">Spalte</span><span class="sxs-lookup"><span data-stu-id="5bc36-111">Column</span></span>            | <span data-ttu-id="5bc36-112">Typ</span><span class="sxs-lookup"><span data-stu-id="5bc36-112">Type</span></span>                         | <span data-ttu-id="5bc36-113">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="5bc36-113">Key</span></span> | <span data-ttu-id="5bc36-114">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="5bc36-114">Nullable</span></span> |
|-------------------|------------------------------|-----|----------|
| <span data-ttu-id="5bc36-115">Komponente\_</span><span class="sxs-lookup"><span data-stu-id="5bc36-115">Component\_</span></span>       | [<span data-ttu-id="5bc36-116">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="5bc36-116">Identifier</span></span>](identifier.md) | <span data-ttu-id="5bc36-117">J</span><span class="sxs-lookup"><span data-stu-id="5bc36-117">Y</span></span>   | <span data-ttu-id="5bc36-118">N</span><span class="sxs-lookup"><span data-stu-id="5bc36-118">N</span></span>        |
| <span data-ttu-id="5bc36-119">Funktion\_</span><span class="sxs-lookup"><span data-stu-id="5bc36-119">Feature\_</span></span>         | [<span data-ttu-id="5bc36-120">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="5bc36-120">Identifier</span></span>](identifier.md) | <span data-ttu-id="5bc36-121">N</span><span class="sxs-lookup"><span data-stu-id="5bc36-121">N</span></span>   | <span data-ttu-id="5bc36-122">N</span><span class="sxs-lookup"><span data-stu-id="5bc36-122">N</span></span>        |
| <span data-ttu-id="5bc36-123">Datei \_ Manifest</span><span class="sxs-lookup"><span data-stu-id="5bc36-123">File\_Manifest</span></span>    | [<span data-ttu-id="5bc36-124">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="5bc36-124">Identifier</span></span>](identifier.md) | <span data-ttu-id="5bc36-125">N</span><span class="sxs-lookup"><span data-stu-id="5bc36-125">N</span></span>   | <span data-ttu-id="5bc36-126">J</span><span class="sxs-lookup"><span data-stu-id="5bc36-126">Y</span></span>        |
| <span data-ttu-id="5bc36-127">Datei \_ Anwendung</span><span class="sxs-lookup"><span data-stu-id="5bc36-127">File\_Application</span></span> | [<span data-ttu-id="5bc36-128">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="5bc36-128">Identifier</span></span>](identifier.md) | <span data-ttu-id="5bc36-129">N</span><span class="sxs-lookup"><span data-stu-id="5bc36-129">N</span></span>   | <span data-ttu-id="5bc36-130">J</span><span class="sxs-lookup"><span data-stu-id="5bc36-130">Y</span></span>        |
| <span data-ttu-id="5bc36-131">Attribute</span><span class="sxs-lookup"><span data-stu-id="5bc36-131">Attributes</span></span>        | [<span data-ttu-id="5bc36-132">Integer</span><span class="sxs-lookup"><span data-stu-id="5bc36-132">Integer</span></span>](integer.md)       | <span data-ttu-id="5bc36-133">N</span><span class="sxs-lookup"><span data-stu-id="5bc36-133">N</span></span>   | <span data-ttu-id="5bc36-134">J</span><span class="sxs-lookup"><span data-stu-id="5bc36-134">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="5bc36-135">Spalten</span><span class="sxs-lookup"><span data-stu-id="5bc36-135">Columns</span></span>

<dl> <dt>

<span data-ttu-id="5bc36-136"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Zulieferern\_</span><span class="sxs-lookup"><span data-stu-id="5bc36-136"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="5bc36-137">Der Schlüssel in der [Komponenten Tabelle](component-table.md) , der die Windows Installer Komponente angibt, die diese Assembly enthält.</span><span class="sxs-lookup"><span data-stu-id="5bc36-137">The key into the [Component Table](component-table.md) that specifies the Windows Installer component that contains this assembly.</span></span>

<span data-ttu-id="5bc36-138">Der Wert in diesem Feld darf nicht auf NULL festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="5bc36-138">The value in this field must not be set to null.</span></span> <span data-ttu-id="5bc36-139">Das Feld "KEYPATH" der Komponente in der [Komponenten Tabelle](component-table.md) darf nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="5bc36-139">The component KeyPath field in the [Component Table](component-table.md) must not be null.</span></span>

<span data-ttu-id="5bc36-140">Bei Win32-Assemblys kann der KEYPATH der Komponente nicht die im Datei Manifest angegebene Manifest-Datei sein \_ .</span><span class="sxs-lookup"><span data-stu-id="5bc36-140">For Win32 assemblies, the component KeyPath cannot be the manifest file that is specified in File\_Manifest.</span></span> <span data-ttu-id="5bc36-141">Das Manifest kann der KEYPATH für eine .NET Framework-oder Richtlinienassembly sein.</span><span class="sxs-lookup"><span data-stu-id="5bc36-141">The manifest can be the keypath for a .NET Framework or policy assembly.</span></span>

</dd> <dt>

<span data-ttu-id="5bc36-142"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Befinden\_</span><span class="sxs-lookup"><span data-stu-id="5bc36-142"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Feature\_</span></span>
</dt> <dd>

<span data-ttu-id="5bc36-143">Schlüssel in der [Featuretabelle](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="5bc36-143">Key into the [Feature Table](feature-table.md).</span></span>

<span data-ttu-id="5bc36-144">Wenn die Assembly durch eine Featureinstallation installiert werden muss, installiert Windows Installer das Feature, auf das dieses Feld verweist.</span><span class="sxs-lookup"><span data-stu-id="5bc36-144">When the assembly must be installed by a feature installation, Windows Installer installs the feature pointed to by this field.</span></span>

</dd> <dt>

<span data-ttu-id="5bc36-145"><span id="File_Manifest"></span><span id="file_manifest"></span><span id="FILE_MANIFEST"></span>Datei \_ Manifest</span><span class="sxs-lookup"><span data-stu-id="5bc36-145"><span id="File_Manifest"></span><span id="file_manifest"></span><span id="FILE_MANIFEST"></span>File\_Manifest</span></span>
</dt> <dd>

<span data-ttu-id="5bc36-146">Ein externer Schlüssel in die [Dateitabelle](file-table.md) , der die Datei angibt, die das Manifest für eine .NET Framework Assembly oder eine Win32-Assembly enthält.</span><span class="sxs-lookup"><span data-stu-id="5bc36-146">An external key into the [File Table](file-table.md) that specifies the file that contains the manifest for a .NET Framework assembly or Win32 assembly.</span></span>

<span data-ttu-id="5bc36-147">Geben Sie diese Datei für eine Win32-Assembly nicht als komponentenschlüsselpfad-Datei im KEYPATH-Feld der [Komponenten Tabelle](component-table.md)an.</span><span class="sxs-lookup"><span data-stu-id="5bc36-147">For a Win32 assembly, do not specify this file as the component key path file in the KeyPath field of the [Component Table](component-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="5bc36-148"><span id="File_Application"></span><span id="file_application"></span><span id="FILE_APPLICATION"></span>Datei \_ Anwendung</span><span class="sxs-lookup"><span data-stu-id="5bc36-148"><span id="File_Application"></span><span id="file_application"></span><span id="FILE_APPLICATION"></span>File\_Application</span></span>
</dt> <dd>

<span data-ttu-id="5bc36-149">Wenn Sie die Assembly an einem privaten Speicherort installieren möchten, geben Sie die Schlüssel Pfad Datei für die Assemblykomponente in dieses Feld ein.</span><span class="sxs-lookup"><span data-stu-id="5bc36-149">To install the assembly at a private location, enter the key path file for the assembly component in this field.</span></span>

<span data-ttu-id="5bc36-150">Dies ist der Wert, der im Feld KEYPATH der [Komponenten Tabelle](component-table.md)angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="5bc36-150">This is the value that appears in the KeyPath field of the [Component Table](component-table.md).</span></span> <span data-ttu-id="5bc36-151">Das Installationsprogramm kann dann die Assembly in der Verzeichnisstruktur der in der [Verzeichnis Tabelle](directory-table.md)angegebenen Komponente installieren.</span><span class="sxs-lookup"><span data-stu-id="5bc36-151">The Installer can then install the assembly to the directory structure of the component that is specified in the [Directory Table](directory-table.md).</span></span> <span data-ttu-id="5bc36-152">Dieses Feld muss NULL sein, wenn die Assembly im globalen Assemblycache installiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="5bc36-152">This field must be null if the assembly is to be installed into the global assembly cache.</span></span>

</dd> <dt>

<span data-ttu-id="5bc36-153"><span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Legt</span><span class="sxs-lookup"><span data-stu-id="5bc36-153"><span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>
</dt> <dd>

<span data-ttu-id="5bc36-154">Geben Sie einen Wert von 1 (eins) für eine Win32-Assembly ein.</span><span class="sxs-lookup"><span data-stu-id="5bc36-154">Enter a value of 1 (one) for a Win32 assembly.</span></span> <span data-ttu-id="5bc36-155">Geben Sie für eine .NET Framework Assembly den Wert 0 (null) ein.</span><span class="sxs-lookup"><span data-stu-id="5bc36-155">Enter a value of 0 (zero) for a .NET Framework assembly.</span></span>

<span data-ttu-id="5bc36-156">Wenn die Attribut Spalte NULL ist, behandelt das Installationsprogramm die Assembly als .NET Framework Assembly.</span><span class="sxs-lookup"><span data-stu-id="5bc36-156">If the Attributes column is NULL, the Installer treats the assembly as a .NET Framework assembly.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5bc36-157">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5bc36-157">Remarks</span></span>

<span data-ttu-id="5bc36-158">Wenn mindestens ein Eintrag in der MsiAssembly-Tabelle vorhanden ist, muss die [InstallExecuteSequence-Tabelle](installexecutesequence-table.md) die [msipublishassemblyaktion](msipublishassemblies-action.md)und die [msiunpublishassemblyaktion](msiunpublishassemblies-action.md)enthalten.</span><span class="sxs-lookup"><span data-stu-id="5bc36-158">If there is at least one entry in the MsiAssembly Table, the [InstallExecuteSequence Table](installexecutesequence-table.md) must contain the [MsiPublishAssemblies Action](msipublishassemblies-action.md), and [MsiUnpublishAssemblies Action](msiunpublishassemblies-action.md).</span></span>

<span data-ttu-id="5bc36-159">Da für-Assemblys nach dem Commit kein Rollback ausgeführt werden kann, wird in Windows Installer ein zweistufiger Installationsvorgang verwendet.</span><span class="sxs-lookup"><span data-stu-id="5bc36-159">Because assemblies cannot be rolled back after they are committed, Windows Installer uses a two-step installation process.</span></span> <span data-ttu-id="5bc36-160">Die Schnittstellen zu den Assemblys werden während der Installations Vorgänge erstellt, die von der [msipublishassemblyaktion](msipublishassemblies-action.md)generiert werden.</span><span class="sxs-lookup"><span data-stu-id="5bc36-160">The interfaces to the assemblies are created during the installation operations that are generated by the [MsiPublishAssemblies Action](msipublishassemblies-action.md).</span></span>

<span data-ttu-id="5bc36-161">Die Assemblys werden erst nach erfolgreicher Ausführung der [InstallFinalize-Aktion](installfinalize-action.md)committet.</span><span class="sxs-lookup"><span data-stu-id="5bc36-161">The assemblies are not committed until successful execution of the [InstallFinalize Action](installfinalize-action.md).</span></span> <span data-ttu-id="5bc36-162">Dies bedeutet Folgendes: Wenn Sie eine benutzerdefinierte Aktion oder Ressource erstellen, die von der Assembly abhängig ist, muss Sie nach der [InstallFinalize-Aktion](installfinalize-action.md)sequenziert werden.</span><span class="sxs-lookup"><span data-stu-id="5bc36-162">This means that if you author a custom action or resource that relies on the assembly, it must be sequenced after the [InstallFinalize Action](installfinalize-action.md).</span></span> <span data-ttu-id="5bc36-163">Wenn Sie z. b. einen Dienst starten müssen, der von einer Assembly im globalen Assemblycache (GAC) abhängt, müssen Sie den Start des Dienstanbieter nach der [InstallFinalize-Aktion](installfinalize-action.md)planen.</span><span class="sxs-lookup"><span data-stu-id="5bc36-163">For example, if you need to start a service that depends on an assembly in the Global Assembly Cache (GAC), you must schedule the starting of that service after the [InstallFinalize Action](installfinalize-action.md).</span></span> <span data-ttu-id="5bc36-164">Dies bedeutet, dass Sie die [ServiceControl-Tabelle](servicecontrol-table.md) nicht verwenden können, um den Dienst zu starten. stattdessen müssen Sie eine benutzerdefinierte Aktion verwenden, die nach InstallFinalize sequenziert wird.</span><span class="sxs-lookup"><span data-stu-id="5bc36-164">This means you cannot use the [ServiceControl Table](servicecontrol-table.md) to start the service, instead you must use a custom action that is sequenced after InstallFinalize.</span></span>

## <a name="validation"></a><span data-ttu-id="5bc36-165">Überprüfen</span><span class="sxs-lookup"><span data-stu-id="5bc36-165">Validation</span></span>

<dl>

[<span data-ttu-id="5bc36-166">ICE03</span><span class="sxs-lookup"><span data-stu-id="5bc36-166">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="5bc36-167">ICE06</span><span class="sxs-lookup"><span data-stu-id="5bc36-167">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="5bc36-168">ICE32</span><span class="sxs-lookup"><span data-stu-id="5bc36-168">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="5bc36-169">ICE66</span><span class="sxs-lookup"><span data-stu-id="5bc36-169">ICE66</span></span>](ice66.md)  
[<span data-ttu-id="5bc36-170">ICE83</span><span class="sxs-lookup"><span data-stu-id="5bc36-170">ICE83</span></span>](ice83.md)  
[<span data-ttu-id="5bc36-171">ICE94</span><span class="sxs-lookup"><span data-stu-id="5bc36-171">ICE94</span></span>](ice94.md)  
</dl>

 

 
