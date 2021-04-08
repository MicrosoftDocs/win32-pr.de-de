---
description: Die Verzeichnis Tabelle gibt das Verzeichnis Layout für das Produkt an. Jede Zeile der Tabelle gibt ein Verzeichnis an, das sowohl an der Quelle als auch am Ziel liegt.
ms.assetid: eaca30cb-fec1-49ca-8b23-5e54c583e3e2
title: Verzeichnis Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 273445aef67e3f166255321d0ac0ccf1aee37515
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960058"
---
# <a name="directory-table"></a><span data-ttu-id="75b61-104">Verzeichnis Tabelle</span><span class="sxs-lookup"><span data-stu-id="75b61-104">Directory Table</span></span>

<span data-ttu-id="75b61-105">Die Verzeichnis Tabelle gibt das Verzeichnis Layout für das Produkt an.</span><span class="sxs-lookup"><span data-stu-id="75b61-105">The Directory table specifies the directory layout for the product.</span></span> <span data-ttu-id="75b61-106">Jede Zeile der Tabelle gibt ein Verzeichnis an, das sowohl an der Quelle als auch am Ziel liegt.</span><span class="sxs-lookup"><span data-stu-id="75b61-106">Each row of the table indicates a directory both at the source and the target.</span></span>

<span data-ttu-id="75b61-107">Die Verzeichnis Tabelle enthält die folgenden Spalten.</span><span class="sxs-lookup"><span data-stu-id="75b61-107">The Directory table has the following columns.</span></span>



| <span data-ttu-id="75b61-108">Spalte</span><span class="sxs-lookup"><span data-stu-id="75b61-108">Column</span></span>            | <span data-ttu-id="75b61-109">Typ</span><span class="sxs-lookup"><span data-stu-id="75b61-109">Type</span></span>                         | <span data-ttu-id="75b61-110">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="75b61-110">Key</span></span> | <span data-ttu-id="75b61-111">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="75b61-111">Nullable</span></span> |
|-------------------|------------------------------|-----|----------|
| <span data-ttu-id="75b61-112">Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="75b61-112">Directory</span></span>         | [<span data-ttu-id="75b61-113">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="75b61-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="75b61-114">J</span><span class="sxs-lookup"><span data-stu-id="75b61-114">Y</span></span>   | <span data-ttu-id="75b61-115">N</span><span class="sxs-lookup"><span data-stu-id="75b61-115">N</span></span>        |
| <span data-ttu-id="75b61-116">Über \_ geordnetes Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="75b61-116">Directory\_Parent</span></span> | [<span data-ttu-id="75b61-117">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="75b61-117">Identifier</span></span>](identifier.md) | <span data-ttu-id="75b61-118">N</span><span class="sxs-lookup"><span data-stu-id="75b61-118">N</span></span>   | <span data-ttu-id="75b61-119">J</span><span class="sxs-lookup"><span data-stu-id="75b61-119">Y</span></span>        |
| <span data-ttu-id="75b61-120">DefaultDir</span><span class="sxs-lookup"><span data-stu-id="75b61-120">DefaultDir</span></span>        | [<span data-ttu-id="75b61-121">DefaultDir</span><span class="sxs-lookup"><span data-stu-id="75b61-121">DefaultDir</span></span>](defaultdir.md) | <span data-ttu-id="75b61-122">N</span><span class="sxs-lookup"><span data-stu-id="75b61-122">N</span></span>   | <span data-ttu-id="75b61-123">N</span><span class="sxs-lookup"><span data-stu-id="75b61-123">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="75b61-124">Spalten</span><span class="sxs-lookup"><span data-stu-id="75b61-124">Columns</span></span>

<dl> <dt>

<span data-ttu-id="75b61-125"><span id="Directory"></span><span id="directory"></span><span id="DIRECTORY"></span>Befinden</span><span class="sxs-lookup"><span data-stu-id="75b61-125"><span id="Directory"></span><span id="directory"></span><span id="DIRECTORY"></span>Directory</span></span>
</dt> <dd>

<span data-ttu-id="75b61-126">Die Verzeichnis Spalte enthält einen eindeutigen Bezeichner für ein Verzeichnis oder einen Verzeichnispfad.</span><span class="sxs-lookup"><span data-stu-id="75b61-126">The Directory column contains a unique identifier for a directory or directory path.</span></span> <span data-ttu-id="75b61-127">Diese Spalte kann den Namen einer Eigenschaft enthalten, die auf den vollständigen Pfad eines Zielverzeichnisses festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="75b61-127">This column can contain the name of a property that is set to the full path of a target directory.</span></span> <span data-ttu-id="75b61-128">Wenn diese Spalte eine Eigenschaft enthält, übernimmt das Zielverzeichnis den in der Spalte DefaultDir angegebenen Namen und übernimmt das übergeordnete Verzeichnis, das in der übergeordneten Spalte des Verzeichnisses angegeben ist \_ .</span><span class="sxs-lookup"><span data-stu-id="75b61-128">If this column contains a property, the target directory takes the name specified in the DefaultDir column and takes the parent directory specified in the Directory\_Parent column.</span></span>

<span data-ttu-id="75b61-129">Das Quellverzeichnis nimmt immer den in der Spalte DefaultDir angegebenen Namen an und übernimmt das übergeordnete Verzeichnis, das in der übergeordneten Spalte des Verzeichnisses angegeben ist \_ .</span><span class="sxs-lookup"><span data-stu-id="75b61-129">The source directory always takes the name specified in the DefaultDir column and takes the parent directory specified in the Directory\_Parent column.</span></span>

<span data-ttu-id="75b61-130">Wenn die \_ übergeordnete Spalte des Verzeichnisses entweder NULL oder gleich dem Wert der Verzeichnis Spalte ist, stellt die Verzeichnis Spalte ein Stammverzeichnis dar.</span><span class="sxs-lookup"><span data-stu-id="75b61-130">If the Directory\_Parent column is either null or equal to the value of the Directory column, the Directory column represents a root target directory.</span></span> <span data-ttu-id="75b61-131">In der Verzeichnis Tabelle kann nur ein Stammverzeichnis angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="75b61-131">Only one root directory may be specified in the Directory table.</span></span>

</dd> <dt>

<span data-ttu-id="75b61-132"><span id="Directory_Parent"></span><span id="directory_parent"></span><span id="DIRECTORY_PARENT"></span>Über \_ geordnetes Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="75b61-132"><span id="Directory_Parent"></span><span id="directory_parent"></span><span id="DIRECTORY_PARENT"></span>Directory\_Parent</span></span>
</dt> <dd>

<span data-ttu-id="75b61-133">Diese Spalte ist ein Verweis auf das übergeordnete Verzeichnis des Verzeichnisses.</span><span class="sxs-lookup"><span data-stu-id="75b61-133">This column is a reference to the directory's parent directory.</span></span> <span data-ttu-id="75b61-134">Ein Datensatz mit einer über \_ geordneten Verzeichnis Spalte, die gleich NULL oder gleich der Verzeichnis Spalte ist, stellt ein Stammverzeichnis dar.</span><span class="sxs-lookup"><span data-stu-id="75b61-134">A record that has a Directory\_Parent column equal to null or equal to the Directory column represents a root directory.</span></span> <span data-ttu-id="75b61-135">Der vollständige Pfad des übergeordneten Verzeichnisses wird in der übergeordneten Spalte des Verzeichnisses als Verweis aufgelöst \_ . ist ein externer Schlüssel in der Verzeichnis Spalte.</span><span class="sxs-lookup"><span data-stu-id="75b61-135">The full path of the parent directory is resolved by reference in the Directory\_Parent column is an external key into the Directory column.</span></span> <span data-ttu-id="75b61-136">Wenn ein Ordner z. b. über ein übergeordnetes Verzeichnis namens pdir verfügt, wird das übergeordnete Verzeichnis von pdir in der über \_ geordneten Spalte des Verzeichnisses der Zeile mit pdir in der Spalte Verzeichnis angegeben.</span><span class="sxs-lookup"><span data-stu-id="75b61-136">For example, if a folder has a parent directory named PDIR, the parent directory of PDIR is given in the Directory\_Parent column of the row with PDIR in the Directory column.</span></span>

</dd> <dt>

<span data-ttu-id="75b61-137"><span id="DefaultDir"></span><span id="defaultdir"></span><span id="DEFAULTDIR"></span>DefaultDir</span><span class="sxs-lookup"><span data-stu-id="75b61-137"><span id="DefaultDir"></span><span id="defaultdir"></span><span id="DEFAULTDIR"></span>DefaultDir</span></span>
</dt> <dd>

<span data-ttu-id="75b61-138">Die DefaultDir-Spalte enthält den Namen des Verzeichnisses (lokalisierbar) unter dem übergeordneten Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="75b61-138">The DefaultDir column contains the directory's name (localizable)under the parent directory.</span></span> <span data-ttu-id="75b61-139">Standardmäßig ist dies der Name des Zielverzeichnisses und des Quell Verzeichnisses.</span><span class="sxs-lookup"><span data-stu-id="75b61-139">By default, this is the name of both the target and source directories.</span></span> <span data-ttu-id="75b61-140">Um verschiedene Quell-und Zielverzeichnis Namen anzugeben, trennen Sie die Ziel-und Quellnamen durch einen Doppelpunkt wie folgt: \[ TargetName \] : \[ SourceName \] .</span><span class="sxs-lookup"><span data-stu-id="75b61-140">To specify different source and target directory names, separate the target and source names with a colon as follows: \[targetname\]:\[sourcename\].</span></span>

<span data-ttu-id="75b61-141">Wenn der Wert der über \_ geordneten Verzeichnis Spalte NULL oder gleich der Verzeichnis Spalte ist, gibt die DefaultDir-Spalte den Namen eines Stamm Quell Verzeichnisses an.</span><span class="sxs-lookup"><span data-stu-id="75b61-141">If the value of the Directory\_Parent column is null or is equal to the Directory column, the DefaultDir column specifies the name of a root source directory.</span></span>

<span data-ttu-id="75b61-142">Bei einem nicht stammenden Quellverzeichnis gibt ein Punkt (.), der in der DefaultDir-Spalte für den Quellverzeichnis Namen oder den Zielverzeichnis Namen eingegeben wird, an, dass sich das Verzeichnis in seinem übergeordneten Verzeichnis ohne Unterverzeichnis befinden soll.</span><span class="sxs-lookup"><span data-stu-id="75b61-142">For a non-root source directory, a period (.) entered in the DefaultDir column for the source directory name or the target directory name indicates the directory should be located in its parent directory without a subdirectory.</span></span>

<span data-ttu-id="75b61-143">Die Verzeichnisnamen in dieser Spalte können als kurze \| Dateiname-Paare mit langer Dateiname formatiert werden.</span><span class="sxs-lookup"><span data-stu-id="75b61-143">The directory names in this column may be formatted as short filename \| long filename pairs.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="75b61-144">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="75b61-144">Remarks</span></span>

<span data-ttu-id="75b61-145">Jeder Datensatz in der Tabelle stellt ein Verzeichnis sowohl im Quell-als auch im Ziel Abbild dar.</span><span class="sxs-lookup"><span data-stu-id="75b61-145">Each record in the table represents a directory in both the source and the destination images.</span></span> <span data-ttu-id="75b61-146">Die Verzeichnis Tabelle muss ein einzelnes Stammverzeichnis mit einem Verzeichnis Spaltenwert angeben, der der [**TARGETDIR**](targetdir.md) -Eigenschaft entspricht.</span><span class="sxs-lookup"><span data-stu-id="75b61-146">The Directory table must specify a single root directory with a Directory column value equal to the [**TARGETDIR**](targetdir.md) property.</span></span>

<span data-ttu-id="75b61-147">Installieren Sie für eine [Administrative Installation](administrative-installation.md)das administrative image im Stammverzeichnis TARGETDIR, und verwenden Sie die Quellverzeichnis Namen, um die Zielverzeichnisse aufzulösen.</span><span class="sxs-lookup"><span data-stu-id="75b61-147">For an [administrative installation](administrative-installation.md), install the administrative image into the root directory named TARGETDIR and use the source directory names to resolve the target directories.</span></span>

<span data-ttu-id="75b61-148">Beachten Sie, dass das Installationsprogramm eine Reihe von Standard [Eigenschaften](properties.md) für Systemordner Pfade festlegt.</span><span class="sxs-lookup"><span data-stu-id="75b61-148">Note the installer sets a number of standard [properties](properties.md) to system folder paths.</span></span> <span data-ttu-id="75b61-149">Eine Liste der Eigenschaften, die auf Systemordner festgelegt sind, finden Sie in der [Eigenschafts Referenz](property-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="75b61-149">See the [Property Reference](property-reference.md) for a list of the properties that are set to system folders.</span></span>

<span data-ttu-id="75b61-150">Die Verzeichnis Auflösung erfolgt während der [Aktion "costfinalize](costfinalize-action.md) " und wird wie folgt ausgeführt:</span><span class="sxs-lookup"><span data-stu-id="75b61-150">Directory resolution is performed during the [CostFinalize action](costfinalize-action.md) and is done as follows:</span></span>

### <a name="root-destination-directory"></a><span data-ttu-id="75b61-151">Stammverzeichnis</span><span class="sxs-lookup"><span data-stu-id="75b61-151">Root Destination Directory</span></span>

<span data-ttu-id="75b61-152">Es darf nur ein einzelnes Stammverzeichnis vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="75b61-152">There may only be a single root destination directory.</span></span> <span data-ttu-id="75b61-153">Zum Angeben des Stammverzeichnis Verzeichnisses legen Sie die Spalte Verzeichnis auf die Eigenschaft [**TARGETDIR**](targetdir.md) und die Spalte DefaultDir auf die Eigenschaft [**SourceDir**](sourcedir.md) fest.</span><span class="sxs-lookup"><span data-stu-id="75b61-153">To specify the root destination directory, set the Directory column to the [**TARGETDIR**](targetdir.md) property and the DefaultDir column to the [**SourceDir**](sourcedir.md) property.</span></span> <span data-ttu-id="75b61-154">Wenn die Eigenschaft **TARGETDIR** definiert ist, wird das Zielverzeichnis in den Wert der Eigenschaft aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="75b61-154">If the **TARGETDIR** property is defined, the destination directory is resolved to the property's value.</span></span> <span data-ttu-id="75b61-155">Wenn die **TARGETDIR** -Eigenschaft nicht definiert ist, wird der Pfad mithilfe der [**ROOTDRIVE**](rootdrive.md) -Eigenschaft aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="75b61-155">If the **TARGETDIR** property is undefined, the [**ROOTDRIVE**](rootdrive.md) property is used to resolve the path.</span></span>

### <a name="root-source-directory"></a><span data-ttu-id="75b61-156">Stamm Quellverzeichnis</span><span class="sxs-lookup"><span data-stu-id="75b61-156">Root Source Directory</span></span>

<span data-ttu-id="75b61-157">Der Wert der DefaultDir-Spalte für den Stammverzeichnis Eintrag muss auf die [**SourceDir**](sourcedir.md) -Eigenschaft festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="75b61-157">The value of the DefaultDir column for the root directory entry must be set to the [**SourceDir**](sourcedir.md) property.</span></span>

### <a name="non-root-destination-directories"></a><span data-ttu-id="75b61-158">Nicht Stamm Verzeichnisse (Ziel)</span><span class="sxs-lookup"><span data-stu-id="75b61-158">Non-root Destination Directories</span></span>

<span data-ttu-id="75b61-159">Der Verzeichnis Wert für ein nicht-Stammverzeichnis wird auch als Name einer Eigenschaft interpretiert, die den Speicherort des Ziels definiert.</span><span class="sxs-lookup"><span data-stu-id="75b61-159">The Directory value for a non-root directory is also interpreted as the name of a property defining the location of the destination.</span></span> <span data-ttu-id="75b61-160">Wenn die Eigenschaft definiert ist, wird das Zielverzeichnis in den Wert der Eigenschaft aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="75b61-160">If the property is defined, the destination directory is resolved to the property's value.</span></span> <span data-ttu-id="75b61-161">Wenn die Eigenschaft nicht definiert ist, wird das Zielverzeichnis in ein Unterverzeichnis unter dem aufgelösten Zielverzeichnis für den über \_ geordneten Verzeichniseintrag aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="75b61-161">If the property is not defined, the destination directory is resolved to a subdirectory beneath the resolved destination directory for the Directory\_Parent entry.</span></span> <span data-ttu-id="75b61-162">Der DefaultDir-Wert definiert den Namen des Unterverzeichnisses.</span><span class="sxs-lookup"><span data-stu-id="75b61-162">The DefaultDir value defines the name of the subdirectory.</span></span>

### <a name="non-root-source-directories"></a><span data-ttu-id="75b61-163">Nicht Stamm Quellverzeichnisse</span><span class="sxs-lookup"><span data-stu-id="75b61-163">Non-root Source Directories</span></span>

<span data-ttu-id="75b61-164">Das Quellverzeichnis für ein nicht-Stammverzeichnis wird in ein Unterverzeichnis des aufgelösten Quell Verzeichnisses für den über \_ geordneten Verzeichniseintrag aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="75b61-164">The source directory for a non-root directory is resolved to a subdirectory of the resolved source directory for the Directory\_Parent entry.</span></span> <span data-ttu-id="75b61-165">Der DefaultDir-Wert definiert den Namen des Unterverzeichnisses.</span><span class="sxs-lookup"><span data-stu-id="75b61-165">Again, the DefaultDir value defines the name of the subdirectory.</span></span>

### <a name="short-or-long-file-names"></a><span data-ttu-id="75b61-166">Kurze oder lange Dateinamen</span><span class="sxs-lookup"><span data-stu-id="75b61-166">Short or Long File Names</span></span>

<span data-ttu-id="75b61-167">Beim Auflösen von Zielverzeichnissen werden die in der DefaultDir-Spalte angegebenen kurzen Dateinamen verwendet, wenn entweder die [**shortfileames**](shortfilenames.md) -Eigenschaft festgelegt ist oder das Volume, auf dem sich das Verzeichnis befindet, keine langen Dateinamen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="75b61-167">When resolving destination directories, the short file names specified in the DefaultDir column are used if either the [**SHORTFILENAMES**](shortfilenames.md) property is set or the volume the directory is located on does not support long file names.</span></span> <span data-ttu-id="75b61-168">Andernfalls wird der lange Dateiname verwendet.</span><span class="sxs-lookup"><span data-stu-id="75b61-168">Otherwise, the long file name is used.</span></span>

<span data-ttu-id="75b61-169">Beachten Sie Folgendes: Wenn die Verzeichnisse während der costfinalize-Aktion aufgelöst werden, werden die Schlüssel in der Verzeichnis Tabelle zu [Eigenschaften](properties.md) , die auf Verzeichnispfade festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="75b61-169">Note that when the directories are resolved during the CostFinalize action, the keys in the Directory table become [properties](properties.md) set to directory paths.</span></span>

[<span data-ttu-id="75b61-170">Tabelle "Buildordner"</span><span class="sxs-lookup"><span data-stu-id="75b61-170">CreateFolder Table</span></span>](createfolder-table.md)

<span data-ttu-id="75b61-171">Informationen zum Erstellen von leeren Ordnern während einer Installation finden Sie in der [Tabelle "Tabelle](createfolder-table.md)".</span><span class="sxs-lookup"><span data-stu-id="75b61-171">For creating empty folders during an installation, see [CreateFolder Table](createfolder-table.md).</span></span>

[<span data-ttu-id="75b61-172">Verwenden der Verzeichnis Tabelle</span><span class="sxs-lookup"><span data-stu-id="75b61-172">Using the Directory Table</span></span>](using-the-directory-table.md)

<span data-ttu-id="75b61-173">Weitere Informationen zur Verzeichnis Tabelle, einschließlich Beispielen, finden Sie unter [Verwenden der Verzeichnis Tabelle](using-the-directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="75b61-173">For more information about the Directory table, including samples, see [Using the Directory Table](using-the-directory-table.md).</span></span>

## <a name="validation"></a><span data-ttu-id="75b61-174">Überprüfen</span><span class="sxs-lookup"><span data-stu-id="75b61-174">Validation</span></span>

<dl>

[<span data-ttu-id="75b61-175">ICE03</span><span class="sxs-lookup"><span data-stu-id="75b61-175">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="75b61-176">ICE06</span><span class="sxs-lookup"><span data-stu-id="75b61-176">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="75b61-177">ICE07</span><span class="sxs-lookup"><span data-stu-id="75b61-177">ICE07</span></span>](ice07.md)  
[<span data-ttu-id="75b61-178">ICE30</span><span class="sxs-lookup"><span data-stu-id="75b61-178">ICE30</span></span>](ice30.md)  
[<span data-ttu-id="75b61-179">ICE32</span><span class="sxs-lookup"><span data-stu-id="75b61-179">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="75b61-180">ICE38</span><span class="sxs-lookup"><span data-stu-id="75b61-180">ICE38</span></span>](ice38.md)  
[<span data-ttu-id="75b61-181">ICE46</span><span class="sxs-lookup"><span data-stu-id="75b61-181">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="75b61-182">ICE48</span><span class="sxs-lookup"><span data-stu-id="75b61-182">ICE48</span></span>](ice48.md)  
[<span data-ttu-id="75b61-183">ICE56</span><span class="sxs-lookup"><span data-stu-id="75b61-183">ICE56</span></span>](ice56.md)  
[<span data-ttu-id="75b61-184">ICE57</span><span class="sxs-lookup"><span data-stu-id="75b61-184">ICE57</span></span>](ice57.md)  
[<span data-ttu-id="75b61-185">ICE64</span><span class="sxs-lookup"><span data-stu-id="75b61-185">ICE64</span></span>](ice64.md)  
[<span data-ttu-id="75b61-186">ICE88</span><span class="sxs-lookup"><span data-stu-id="75b61-186">ICE88</span></span>](ice88.md)  
[<span data-ttu-id="75b61-187">ICE90</span><span class="sxs-lookup"><span data-stu-id="75b61-187">ICE90</span></span>](ice90.md)  
[<span data-ttu-id="75b61-188">ICE91</span><span class="sxs-lookup"><span data-stu-id="75b61-188">ICE91</span></span>](ice91.md)  
[<span data-ttu-id="75b61-189">ICE99</span><span class="sxs-lookup"><span data-stu-id="75b61-189">ICE99</span></span>](ice99.md)  
</dl>

 

 



