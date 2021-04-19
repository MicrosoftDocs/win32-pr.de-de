---
description: Die MsiAssembly-Tabelle und die MsiAssemblyName-Tabelle geben Windows Installer Einstellungen für Common Language Runtime Assemblys und Win32-Assemblys an.
ms.assetid: cfe9a0a3-e40f-4c59-b2e4-ad7654528e3b
title: MsiAssemblyName-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12008682c82d7be20ed8713d8dc1c416f9c7065c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357075"
---
# <a name="msiassemblyname-table"></a><span data-ttu-id="51262-103">MsiAssemblyName-Tabelle</span><span class="sxs-lookup"><span data-stu-id="51262-103">MsiAssemblyName Table</span></span>

<span data-ttu-id="51262-104">Die [MsiAssembly-Tabelle](msiassembly-table.md) und die MsiAssemblyName-Tabelle geben Windows Installer Einstellungen für Common Language Runtime Assemblys und Win32-Assemblys an.</span><span class="sxs-lookup"><span data-stu-id="51262-104">The [MsiAssembly Table](msiassembly-table.md) and MsiAssemblyName Table specify Windows Installer settings for common language runtime assemblies and Win32 assemblies.</span></span> <span data-ttu-id="51262-105">Weitere Informationen finden Sie unter Installieren von Assemblys [im globalen Assemblycache](installation-of-assemblies-to-the-global-assembly-cache.md) und [Installieren von Win32](installation-of-win32-assemblies.md)-Assemblys.</span><span class="sxs-lookup"><span data-stu-id="51262-105">For information see, [Installation of Assemblies to the Global Assembly Cache](installation-of-assemblies-to-the-global-assembly-cache.md) and [Installation of Win32 Assemblies](installation-of-win32-assemblies.md).</span></span>

<span data-ttu-id="51262-106">Die MsiAssemblyName-Tabelle gibt das Schema für die Elemente eines starken Assemblycache-namens für eine .NET Framework-oder Win32-Assembly an.</span><span class="sxs-lookup"><span data-stu-id="51262-106">The MsiAssemblyName Table specifies the schema for the elements of a strong assembly cache name for a .NET Framework or Win32 assembly.</span></span> <span data-ttu-id="51262-107">Der Name wird erstellt, indem alle Elemente mit dem gleichen Komponenten Schlüssel angehängt werden \_ .</span><span class="sxs-lookup"><span data-stu-id="51262-107">The name is constructed by appending all elements with the same Component\_ key.</span></span> <span data-ttu-id="51262-108">Siehe folgendes Beispiel.</span><span class="sxs-lookup"><span data-stu-id="51262-108">See the following example.</span></span>

<span data-ttu-id="51262-109">Windows Installer können Win32 [-](side-by-side-assemblies.md)Assemblys als parallele Assemblys installieren.</span><span class="sxs-lookup"><span data-stu-id="51262-109">Windows Installer can install Win32 assemblies as [side-by-side assemblies](side-by-side-assemblies.md).</span></span> <span data-ttu-id="51262-110">Weitere Informationen finden Sie in der [API](../sbscs/side-by-side-assembly-api.md)für parallele Assemblys.</span><span class="sxs-lookup"><span data-stu-id="51262-110">For more information, see the [Side-by-Side Assembly API](../sbscs/side-by-side-assembly-api.md).</span></span>

<span data-ttu-id="51262-111">Die MsiAssemblyName-Tabelle weist die folgenden Spalten auf.</span><span class="sxs-lookup"><span data-stu-id="51262-111">The MsiAssemblyName Table has the following columns.</span></span>



| <span data-ttu-id="51262-112">Spalte</span><span class="sxs-lookup"><span data-stu-id="51262-112">Column</span></span>      | <span data-ttu-id="51262-113">Typ</span><span class="sxs-lookup"><span data-stu-id="51262-113">Type</span></span>                         | <span data-ttu-id="51262-114">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="51262-114">Key</span></span> | <span data-ttu-id="51262-115">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="51262-115">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="51262-116">Komponente\_</span><span class="sxs-lookup"><span data-stu-id="51262-116">Component\_</span></span> | [<span data-ttu-id="51262-117">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="51262-117">Identifier</span></span>](identifier.md) | <span data-ttu-id="51262-118">J</span><span class="sxs-lookup"><span data-stu-id="51262-118">Y</span></span>   | <span data-ttu-id="51262-119">N</span><span class="sxs-lookup"><span data-stu-id="51262-119">N</span></span>        |
| <span data-ttu-id="51262-120">Name</span><span class="sxs-lookup"><span data-stu-id="51262-120">Name</span></span>        | [<span data-ttu-id="51262-121">Text</span><span class="sxs-lookup"><span data-stu-id="51262-121">Text</span></span>](text.md)             | <span data-ttu-id="51262-122">J</span><span class="sxs-lookup"><span data-stu-id="51262-122">Y</span></span>   | <span data-ttu-id="51262-123">N</span><span class="sxs-lookup"><span data-stu-id="51262-123">N</span></span>        |
| <span data-ttu-id="51262-124">Wert</span><span class="sxs-lookup"><span data-stu-id="51262-124">Value</span></span>       | [<span data-ttu-id="51262-125">Text</span><span class="sxs-lookup"><span data-stu-id="51262-125">Text</span></span>](text.md)             | <span data-ttu-id="51262-126">N</span><span class="sxs-lookup"><span data-stu-id="51262-126">N</span></span>   | <span data-ttu-id="51262-127">N</span><span class="sxs-lookup"><span data-stu-id="51262-127">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="51262-128">Spalten</span><span class="sxs-lookup"><span data-stu-id="51262-128">Columns</span></span>

<dl> <dt>

<span data-ttu-id="51262-129"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Zulieferern\_</span><span class="sxs-lookup"><span data-stu-id="51262-129"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="51262-130">Der Schlüssel in die [Komponenten Tabelle](component-table.md) , der die Windows Installer Komponente angibt, die diese Assembly enthält.</span><span class="sxs-lookup"><span data-stu-id="51262-130">Key into the [Component Table](component-table.md) that specifies the Windows Installer component that contains this assembly.</span></span>

</dd> <dt>

<span data-ttu-id="51262-131"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Benennen</span><span class="sxs-lookup"><span data-stu-id="51262-131"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="51262-132">Der Name des Attributs, das dem in der Spalte Wert angegebenen Wert zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="51262-132">Name of the attribute associated with the value specified in the Value column.</span></span>

</dd> <dt>

<span data-ttu-id="51262-133"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Wert</span><span class="sxs-lookup"><span data-stu-id="51262-133"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span>
</dt> <dd>

<span data-ttu-id="51262-134">Der Wert, der dem in der Spalte Name angegebenen Namen zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="51262-134">Value associated with the name specified in the Name column.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="51262-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="51262-135">Remarks</span></span>

<span data-ttu-id="51262-136">Die in der MsiAssemblyName-Tabelle erstellten Informationen müssen mit den Informationen in der Manifest-Datei der Assembly identisch sein.</span><span class="sxs-lookup"><span data-stu-id="51262-136">The information authored into the MsiAssemblyName Table must match the information in the manifest file of the assembly.</span></span> <span data-ttu-id="51262-137">Wenn die Informationen in der Manifest-und der MsiAssemblyName-Tabelle nicht stimmen, kann beim Entfernen der Anwendung die Assembly auf dem Computer belassen werden.</span><span class="sxs-lookup"><span data-stu-id="51262-137">If the information in the manifest and MsiAssemblyName Table do not match, removal of the application can leave the assembly on the computer.</span></span>

<span data-ttu-id="51262-138">Für Win32-Assemblys muss in der Tabelle MsiAssemblyName eine Zeile für jeden der folgenden Einträge im Feld Name vorhanden sein: Type, Name, Version, Language, PublicKeyToken und ProcessorArchitecture.</span><span class="sxs-lookup"><span data-stu-id="51262-138">For Win32 assemblies there must be a row in the MsiAssemblyName Table for each of the following entries in the Name field: type, name, version, language, publicKeyToken and processorArchitecture.</span></span> <span data-ttu-id="51262-139">Der entsprechende Wert für jeden Namen kann in das Wertfeld eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="51262-139">The corresponding value for each name can be entered into the Value field.</span></span> <span data-ttu-id="51262-140">Die Name-Wert-Paare in der MsiAssemblyName-Tabelle müssen den Attributen Type, Name, Version, Language, PublicKeyToken und ProcessorArchitecture im Manifest der Assembly entsprechen.</span><span class="sxs-lookup"><span data-stu-id="51262-140">The name-value pairs in MsiAssemblyName Table must match the type, name, version, language, publicKeyToken and processorArchitecture attributes in the manifest of the assembly.</span></span>

<span data-ttu-id="51262-141">Für private Common Language Runtime-Assemblys (.net Frameworkversionen 1,0 und 1,1) muss die MsiAssemblyName-Tabelle eine Zeile für jeden der folgenden Einträge im Name-Feld enthalten: Name, Version und Kultur.</span><span class="sxs-lookup"><span data-stu-id="51262-141">For private common language runtime assemblies (.NET Frameworkversions 1.0 and 1.1), the MsiAssemblyName Table must include a row for each of the following entries in the Name field: Name, Version, and Culture.</span></span> <span data-ttu-id="51262-142">Der entsprechende Wert für jeden Namen kann in das Wertfeld eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="51262-142">The corresponding value for each Name can be entered into the Value field.</span></span>

<span data-ttu-id="51262-143">Für globale Common Language Runtime Assemblys (.NET Framework Versionen 1,0 und 1,1) muss die MsiAssemblyName-Tabelle eine Zeile für jeden der folgenden Einträge im Feld Name enthalten: Name, Version, Kultur und PublicKeyToken.</span><span class="sxs-lookup"><span data-stu-id="51262-143">For global common language runtime assemblies (.NET Framework versions 1.0 and 1.1), the MsiAssemblyName Table must include a row for each of the following entries in the Name field: Name, Version, Culture, and PublicKeyToken.</span></span> <span data-ttu-id="51262-144">Der entsprechende Wert für jeden Namen kann in das Wertfeld eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="51262-144">The corresponding value for each Name can be entered into the Value field.</span></span>

<span data-ttu-id="51262-145">Der .NET Framework Version 1,1 ist die Mindestversion, die verwendet werden kann, um ein direktes Update einer globalen Common Language Runtime Assembly auszuführen.</span><span class="sxs-lookup"><span data-stu-id="51262-145">The .NET Framework version 1.1 is the minimum version that can be used to perform an in-place update of a global common language runtime assembly.</span></span> <span data-ttu-id="51262-146">Sie können die Eigenschaft " [**MsiNetAssemblySupport**](msinetassemblysupport.md) " für die Version überprüfen.</span><span class="sxs-lookup"><span data-stu-id="51262-146">You can check the [**MsiNetAssemblySupport**](msinetassemblysupport.md) property for the version.</span></span> <span data-ttu-id="51262-147">Die MsiAssemblyName-Tabelle muss auch ein fileversion-Feld aufweisen, da diese Art von Assemblyaktualisierung nur die Dateiversion ändert.</span><span class="sxs-lookup"><span data-stu-id="51262-147">The MsiAssemblyName Table must also have a FileVersion field because this type of assembly update only changes the FileVersion.</span></span> <span data-ttu-id="51262-148">Weitere Informationen finden Sie unter [Aktualisieren](updating-assemblies.md)von Assemblys.</span><span class="sxs-lookup"><span data-stu-id="51262-148">For more information, see [Updating Assemblies](updating-assemblies.md).</span></span>

<span data-ttu-id="51262-149">Das Assemblymanifest für Componenta könnte z. b. einen assemblyIdentity-Abschnitt für eine Win32-Assembly wie folgt enthalten.</span><span class="sxs-lookup"><span data-stu-id="51262-149">For example, the assembly manifest for ComponentA might have an assemblyIdentity section as follows for a Win32 assembly.</span></span>

``` syntax
<assemblyIdentity type="win32" name="ms-sxstest-simple" version="1.0.0.0" language="en" publicKeyToken="1111111111222222" processorArchitecture="x86"/>
```

<span data-ttu-id="51262-150">Füllen Sie in diesem Fall die MsiAssemblyName-Tabelle wie folgt auf.</span><span class="sxs-lookup"><span data-stu-id="51262-150">In this case, populate the MsiAssemblyName Table as follows.</span></span>



| <span data-ttu-id="51262-151">Komponente</span><span class="sxs-lookup"><span data-stu-id="51262-151">Component</span></span>  | <span data-ttu-id="51262-152">Name</span><span class="sxs-lookup"><span data-stu-id="51262-152">Name</span></span>                  | <span data-ttu-id="51262-153">Wert</span><span class="sxs-lookup"><span data-stu-id="51262-153">Value</span></span>             |
|------------|-----------------------|-------------------|
| <span data-ttu-id="51262-154">Componenta</span><span class="sxs-lookup"><span data-stu-id="51262-154">ComponentA</span></span> | <span data-ttu-id="51262-155">type</span><span class="sxs-lookup"><span data-stu-id="51262-155">type</span></span>                  | <span data-ttu-id="51262-156">Win32</span><span class="sxs-lookup"><span data-stu-id="51262-156">win32</span></span>             |
| <span data-ttu-id="51262-157">Componenta</span><span class="sxs-lookup"><span data-stu-id="51262-157">ComponentA</span></span> | <span data-ttu-id="51262-158">name</span><span class="sxs-lookup"><span data-stu-id="51262-158">name</span></span>                  | <span data-ttu-id="51262-159">MS-sxstest-Simple</span><span class="sxs-lookup"><span data-stu-id="51262-159">ms-sxstest-simple</span></span> |
| <span data-ttu-id="51262-160">Componenta</span><span class="sxs-lookup"><span data-stu-id="51262-160">ComponentA</span></span> | <span data-ttu-id="51262-161">version</span><span class="sxs-lookup"><span data-stu-id="51262-161">version</span></span>               | <span data-ttu-id="51262-162">1.0.0.0</span><span class="sxs-lookup"><span data-stu-id="51262-162">1.0.0.0</span></span>           |
| <span data-ttu-id="51262-163">Componenta</span><span class="sxs-lookup"><span data-stu-id="51262-163">ComponentA</span></span> | <span data-ttu-id="51262-164">language</span><span class="sxs-lookup"><span data-stu-id="51262-164">language</span></span>              | <span data-ttu-id="51262-165">en</span><span class="sxs-lookup"><span data-stu-id="51262-165">en</span></span>                |
| <span data-ttu-id="51262-166">Componenta</span><span class="sxs-lookup"><span data-stu-id="51262-166">ComponentA</span></span> | <span data-ttu-id="51262-167">PublicKeyToken</span><span class="sxs-lookup"><span data-stu-id="51262-167">publicKeyToken</span></span>        | <span data-ttu-id="51262-168">1111111111222222</span><span class="sxs-lookup"><span data-stu-id="51262-168">1111111111222222</span></span>  |
| <span data-ttu-id="51262-169">Componenta</span><span class="sxs-lookup"><span data-stu-id="51262-169">ComponentA</span></span> | <span data-ttu-id="51262-170">processorArchitecture</span><span class="sxs-lookup"><span data-stu-id="51262-170">processorArchitecture</span></span> | <span data-ttu-id="51262-171">x86</span><span class="sxs-lookup"><span data-stu-id="51262-171">x86</span></span>               |



 

## <a name="validation"></a><span data-ttu-id="51262-172">Überprüfen</span><span class="sxs-lookup"><span data-stu-id="51262-172">Validation</span></span>

<dl>

[<span data-ttu-id="51262-173">ICE03</span><span class="sxs-lookup"><span data-stu-id="51262-173">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="51262-174">ICE06</span><span class="sxs-lookup"><span data-stu-id="51262-174">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="51262-175">ICE32</span><span class="sxs-lookup"><span data-stu-id="51262-175">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="51262-176">ICE66</span><span class="sxs-lookup"><span data-stu-id="51262-176">ICE66</span></span>](ice66.md)  
[<span data-ttu-id="51262-177">ICE83</span><span class="sxs-lookup"><span data-stu-id="51262-177">ICE83</span></span>](ice83.md)  
</dl>

 

 
