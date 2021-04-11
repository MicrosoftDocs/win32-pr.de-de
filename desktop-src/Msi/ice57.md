---
description: ICE57 überprüft, ob einzelne Komponenten nicht Computer-und benutzerspezifische Daten kombinieren. Diese benutzerdefinierte Ice-Aktion überprüft Registrierungseinträge, Dateien, Verzeichnis Schlüssel Pfade und nicht angekündigte Verknüpfungen.
ms.assetid: 3c82efa7-9cf3-4bcd-8ec4-b81d1d7aa0a6
title: ICE57
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a59d609e5d7de0011666be0b5cc5e76417d8e67d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217351"
---
# <a name="ice57"></a><span data-ttu-id="cc850-104">ICE57</span><span class="sxs-lookup"><span data-stu-id="cc850-104">ICE57</span></span>

<span data-ttu-id="cc850-105">ICE57 überprüft, ob einzelne Komponenten nicht Computer-und benutzerspezifische Daten kombinieren.</span><span class="sxs-lookup"><span data-stu-id="cc850-105">ICE57 validates that individual components do not mix per-machine and per-user data.</span></span> <span data-ttu-id="cc850-106">Diese benutzerdefinierte Ice-Aktion überprüft Registrierungseinträge, Dateien, Verzeichnis Schlüssel Pfade und nicht angekündigte Verknüpfungen.</span><span class="sxs-lookup"><span data-stu-id="cc850-106">This ICE custom action checks registry entries, files, directory key paths, and non-advertised shortcuts.</span></span>

<span data-ttu-id="cc850-107">Das Kombinieren von Benutzer-und computerspezifischen Daten in der gleichen Komponente kann dazu führen, dass die Komponente für einige Benutzer in einer Umgebung mit mehreren Benutzern nur teilweise installiert wird.</span><span class="sxs-lookup"><span data-stu-id="cc850-107">Mixing per-user and per-machine data in the same component could result in only partial installation of the component for some users in a multi-user environment.</span></span>

<span data-ttu-id="cc850-108">Siehe die Eigenschaft " [**ALLUSERS**](allusers.md) ".</span><span class="sxs-lookup"><span data-stu-id="cc850-108">See the [**ALLUSERS**](allusers.md) property.</span></span>

## <a name="result"></a><span data-ttu-id="cc850-109">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="cc850-109">Result</span></span>

<span data-ttu-id="cc850-110">ICE57 gibt einen Fehler aus, wenn eine Komponente gefunden wird, die sowohl Computer-als auch benutzerspezifische Registrierungseinträge, Dateien, Verzeichnis Schlüssel Pfade oder nicht angekündigte Verknüpfungen enthält.</span><span class="sxs-lookup"><span data-stu-id="cc850-110">ICE57 posts an error if it finds any component that contains both a per-machine and per-user registry entries, files, directory key paths, or non-advertised shortcuts.</span></span>

## <a name="example"></a><span data-ttu-id="cc850-111">Beispiel</span><span class="sxs-lookup"><span data-stu-id="cc850-111">Example</span></span>

<span data-ttu-id="cc850-112">ICE57reports die folgenden Fehler für das gezeigte Beispiel.</span><span class="sxs-lookup"><span data-stu-id="cc850-112">ICE57reports the following errors for the example shown.</span></span>

``` syntax
Component 'Component1' has both per-user and per-machine 
    data with a per-machine KeyPath. 
 
WARNING: Component 'Component2' has both per-user and 
    per-machine data with an HKCU Registry KeyPath. 
 
Component 'Component3' has a registry entry that 
    can be either per-user or per-machine and a per-machine KeyPath. 
 
Component 'Component4' has both per-user data and 
    a keypath that can be either per-user or per-machine.
```

<span data-ttu-id="cc850-113">[Komponenten Tabelle](component-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="cc850-113">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="cc850-114">Komponente</span><span class="sxs-lookup"><span data-stu-id="cc850-114">Component</span></span>  | <span data-ttu-id="cc850-115">Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="cc850-115">Directory</span></span>  | <span data-ttu-id="cc850-116">Attribute</span><span class="sxs-lookup"><span data-stu-id="cc850-116">Attributes</span></span> | <span data-ttu-id="cc850-117">KEYPATH</span><span class="sxs-lookup"><span data-stu-id="cc850-117">KeyPath</span></span> |
|------------|------------|------------|---------|
| <span data-ttu-id="cc850-118">Component1</span><span class="sxs-lookup"><span data-stu-id="cc850-118">Component1</span></span> | <span data-ttu-id="cc850-119">Directoren</span><span class="sxs-lookup"><span data-stu-id="cc850-119">DirectoryA</span></span> | <span data-ttu-id="cc850-120">0</span><span class="sxs-lookup"><span data-stu-id="cc850-120">0</span></span>          | <span data-ttu-id="cc850-121">Mit der</span><span class="sxs-lookup"><span data-stu-id="cc850-121">FileA</span></span>   |
| <span data-ttu-id="cc850-122">Component2</span><span class="sxs-lookup"><span data-stu-id="cc850-122">Component2</span></span> | <span data-ttu-id="cc850-123">Directoren</span><span class="sxs-lookup"><span data-stu-id="cc850-123">DirectoryA</span></span> | <span data-ttu-id="cc850-124">4</span><span class="sxs-lookup"><span data-stu-id="cc850-124">4</span></span>          | <span data-ttu-id="cc850-125">Regkeyb</span><span class="sxs-lookup"><span data-stu-id="cc850-125">RegKeyB</span></span> |
| <span data-ttu-id="cc850-126">Component3</span><span class="sxs-lookup"><span data-stu-id="cc850-126">Component3</span></span> | <span data-ttu-id="cc850-127">Directoren</span><span class="sxs-lookup"><span data-stu-id="cc850-127">DirectoryA</span></span> | <span data-ttu-id="cc850-128">0</span><span class="sxs-lookup"><span data-stu-id="cc850-128">0</span></span>          | <span data-ttu-id="cc850-129">Filec</span><span class="sxs-lookup"><span data-stu-id="cc850-129">FileC</span></span>   |
| <span data-ttu-id="cc850-130">Component4</span><span class="sxs-lookup"><span data-stu-id="cc850-130">Component4</span></span> | <span data-ttu-id="cc850-131">Directoren</span><span class="sxs-lookup"><span data-stu-id="cc850-131">DirectoryA</span></span> | <span data-ttu-id="cc850-132">4</span><span class="sxs-lookup"><span data-stu-id="cc850-132">4</span></span>          | <span data-ttu-id="cc850-133">Regkeyd</span><span class="sxs-lookup"><span data-stu-id="cc850-133">RegKeyD</span></span> |



 

<span data-ttu-id="cc850-134">[Registrierungs Tabelle](registry-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="cc850-134">[Registry Table](registry-table.md) (partial)</span></span>



| <span data-ttu-id="cc850-135">Registrierung</span><span class="sxs-lookup"><span data-stu-id="cc850-135">Registry</span></span> | <span data-ttu-id="cc850-136">Root</span><span class="sxs-lookup"><span data-stu-id="cc850-136">Root</span></span> | <span data-ttu-id="cc850-137">Komponente\_</span><span class="sxs-lookup"><span data-stu-id="cc850-137">Component\_</span></span> |
|----------|------|-------------|
| <span data-ttu-id="cc850-138">Regkeya</span><span class="sxs-lookup"><span data-stu-id="cc850-138">RegKeyA</span></span>  | <span data-ttu-id="cc850-139">1</span><span class="sxs-lookup"><span data-stu-id="cc850-139">1</span></span>    | <span data-ttu-id="cc850-140">Component1</span><span class="sxs-lookup"><span data-stu-id="cc850-140">Component1</span></span>  |
| <span data-ttu-id="cc850-141">Regkeyb</span><span class="sxs-lookup"><span data-stu-id="cc850-141">RegKeyB</span></span>  | <span data-ttu-id="cc850-142">1</span><span class="sxs-lookup"><span data-stu-id="cc850-142">1</span></span>    | <span data-ttu-id="cc850-143">Component2</span><span class="sxs-lookup"><span data-stu-id="cc850-143">Component2</span></span>  |
| <span data-ttu-id="cc850-144">Regkeyc</span><span class="sxs-lookup"><span data-stu-id="cc850-144">RegKeyC</span></span>  | <span data-ttu-id="cc850-145">-1</span><span class="sxs-lookup"><span data-stu-id="cc850-145">-1</span></span>   | <span data-ttu-id="cc850-146">Component3</span><span class="sxs-lookup"><span data-stu-id="cc850-146">Component3</span></span>  |
| <span data-ttu-id="cc850-147">Regkeyd</span><span class="sxs-lookup"><span data-stu-id="cc850-147">RegKeyD</span></span>  | <span data-ttu-id="cc850-148">-1</span><span class="sxs-lookup"><span data-stu-id="cc850-148">-1</span></span>   | <span data-ttu-id="cc850-149">Component4</span><span class="sxs-lookup"><span data-stu-id="cc850-149">Component4</span></span>  |



 

<span data-ttu-id="cc850-150">[Dateitabelle](file-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="cc850-150">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="cc850-151">File</span><span class="sxs-lookup"><span data-stu-id="cc850-151">File</span></span>  | <span data-ttu-id="cc850-152">Komponente\_</span><span class="sxs-lookup"><span data-stu-id="cc850-152">Component\_</span></span> |
|-------|-------------|
| <span data-ttu-id="cc850-153">Mit der</span><span class="sxs-lookup"><span data-stu-id="cc850-153">FileA</span></span> | <span data-ttu-id="cc850-154">Component1</span><span class="sxs-lookup"><span data-stu-id="cc850-154">Component1</span></span>  |
| <span data-ttu-id="cc850-155">FileB</span><span class="sxs-lookup"><span data-stu-id="cc850-155">FileB</span></span> | <span data-ttu-id="cc850-156">Component2</span><span class="sxs-lookup"><span data-stu-id="cc850-156">Component2</span></span>  |
| <span data-ttu-id="cc850-157">Filec</span><span class="sxs-lookup"><span data-stu-id="cc850-157">FileC</span></span> | <span data-ttu-id="cc850-158">Component3</span><span class="sxs-lookup"><span data-stu-id="cc850-158">Component3</span></span>  |
| <span data-ttu-id="cc850-159">Fassung</span><span class="sxs-lookup"><span data-stu-id="cc850-159">FileD</span></span> | <span data-ttu-id="cc850-160">Component4</span><span class="sxs-lookup"><span data-stu-id="cc850-160">Component4</span></span>  |



 

[<span data-ttu-id="cc850-161">Verzeichnis Tabelle</span><span class="sxs-lookup"><span data-stu-id="cc850-161">Directory Table</span></span>](directory-table.md)



| <span data-ttu-id="cc850-162">Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="cc850-162">Directory</span></span>  | <span data-ttu-id="cc850-163">Über \_ geordnetes Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="cc850-163">Directory\_Parent</span></span> | <span data-ttu-id="cc850-164">DefaultDir</span><span class="sxs-lookup"><span data-stu-id="cc850-164">DefaultDir</span></span> |
|------------|-------------------|------------|
| <span data-ttu-id="cc850-165">TARGETDIR</span><span class="sxs-lookup"><span data-stu-id="cc850-165">TARGETDIR</span></span>  |                   | <span data-ttu-id="cc850-166">SourceDir</span><span class="sxs-lookup"><span data-stu-id="cc850-166">SourceDir</span></span>  |
| <span data-ttu-id="cc850-167">Directoren</span><span class="sxs-lookup"><span data-stu-id="cc850-167">DirectoryA</span></span> | <span data-ttu-id="cc850-168">TARGETDIR</span><span class="sxs-lookup"><span data-stu-id="cc850-168">TARGETDIR</span></span>         | <span data-ttu-id="cc850-169">Directoren</span><span class="sxs-lookup"><span data-stu-id="cc850-169">DirectoryA</span></span> |



 

<span data-ttu-id="cc850-170">Um die Fehler zu beheben, müssen Sie die Anwendung so neu organisieren, dass jede Komponente nur Benutzer-oder Computer spezifische Ressourcen und nicht beides enthält.</span><span class="sxs-lookup"><span data-stu-id="cc850-170">To fix the errors, reorganize the application such that each component contains only per-user or per-machine resources, and not both.</span></span>

<span data-ttu-id="cc850-171">Die erste Fehlermeldung wird gepostet, weil Component1 die Datei (pro Computer) und den HKCU-Registrierungsschlüssel regkeya (pro Benutzer) enthält.</span><span class="sxs-lookup"><span data-stu-id="cc850-171">The first error message is posted because Component1 contains FileA (per-machine) and the HKCU registry key RegKeyA (per user).</span></span>

## <a name="related-topics"></a><span data-ttu-id="cc850-172">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="cc850-172">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cc850-173">Ice-Referenz</span><span class="sxs-lookup"><span data-stu-id="cc850-173">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



