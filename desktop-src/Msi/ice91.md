---
description: ICE91 gibt eine Warnung aus, wenn eine Datei, eine INI-Datei oder eine Verknüpfungs Datei in einem Verzeichnis pro Benutzer installiert wird.
ms.assetid: 1834d841-b1d9-4646-8057-a41dd88310b6
title: ICE91
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91f5723369c21894817dacbc1755430a31f17199
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350818"
---
# <a name="ice91"></a><span data-ttu-id="88065-103">ICE91</span><span class="sxs-lookup"><span data-stu-id="88065-103">ICE91</span></span>

<span data-ttu-id="88065-104">ICE91 gibt eine Warnung aus, wenn eine Datei, eine INI-Datei oder eine Verknüpfungs Datei in einem Verzeichnis pro Benutzer installiert wird.</span><span class="sxs-lookup"><span data-stu-id="88065-104">ICE91 posts a warning if a file, .ini file, or shortcut file is installed into a per-user only directory.</span></span> <span data-ttu-id="88065-105">Diese Warnungen sind harmlos, wenn das Paket nur für die Installation im Einzelbenutzer- [Installations Kontext](installation-context.md) und nie für Installationen pro Computer verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="88065-105">These warnings are harmless if the package is only used for installation in the per-user [installation context](installation-context.md) and never used for per-machine installations.</span></span>

<span data-ttu-id="88065-106">Dateien, INI-Dateien oder Verknüpfungen in Verzeichnissen pro Benutzer werden im Profil eines bestimmten Benutzers installiert.</span><span class="sxs-lookup"><span data-stu-id="88065-106">Files, .ini files, or shortcuts in per-user only directories are installed into a particular user's profile.</span></span> <span data-ttu-id="88065-107">Selbst wenn der Benutzer die Eigenschaft " [**ALLUSERS**](allusers.md) " für eine Installation pro Computer festlegt, werden Dateien, INI-Dateien oder Verknüpfungen in benutzerspezifischen Verzeichnissen nicht in das Profil "alle Benutzer" kopiert und sind anderen Benutzern nicht zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="88065-107">Even if the user sets the [**ALLUSERS**](allusers.md) property for a per-machine installations, files, .ini files, or shortcuts in per-user only directories are not copied in to the "All Users" profile and are not available to other users.</span></span> <span data-ttu-id="88065-108">Die Verzeichnisse pro Benutzer sind nicht mit der Eigenschaft " **ALLUSERS** " unterschiedlich.</span><span class="sxs-lookup"><span data-stu-id="88065-108">The per-user only directories do not vary with the **ALLUSERS** property.</span></span> <span data-ttu-id="88065-109">Im folgenden finden Sie eine Liste der Verzeichnisse pro Benutzer:</span><span class="sxs-lookup"><span data-stu-id="88065-109">The following is a list of the per-user only directories:</span></span>

-   <span data-ttu-id="88065-110">AppDataFolder</span><span class="sxs-lookup"><span data-stu-id="88065-110">AppDataFolder</span></span>
-   <span data-ttu-id="88065-111">FavoritesFolder</span><span class="sxs-lookup"><span data-stu-id="88065-111">FavoritesFolder</span></span>
-   <span data-ttu-id="88065-112">"Netthoodfolder"</span><span class="sxs-lookup"><span data-stu-id="88065-112">NetHoodFolder</span></span>
-   <span data-ttu-id="88065-113">PersonalFolder</span><span class="sxs-lookup"><span data-stu-id="88065-113">PersonalFolder</span></span>
-   <span data-ttu-id="88065-114">Printhoodfolder</span><span class="sxs-lookup"><span data-stu-id="88065-114">PrintHoodFolder</span></span>
-   <span data-ttu-id="88065-115">Recentfolder</span><span class="sxs-lookup"><span data-stu-id="88065-115">RecentFolder</span></span>
-   <span data-ttu-id="88065-116">Ordner "SendTo"</span><span class="sxs-lookup"><span data-stu-id="88065-116">SendToFolder</span></span>
-   <span data-ttu-id="88065-117">Mypicturesfolder</span><span class="sxs-lookup"><span data-stu-id="88065-117">MyPicturesFolder</span></span>
-   <span data-ttu-id="88065-118">Localappdatafolder</span><span class="sxs-lookup"><span data-stu-id="88065-118">LocalAppDataFolder</span></span>

## <a name="result"></a><span data-ttu-id="88065-119">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="88065-119">Result</span></span>

<span data-ttu-id="88065-120">ICE91 gibt die folgenden Warnungen aus.</span><span class="sxs-lookup"><span data-stu-id="88065-120">ICE91 posts the following warnings.</span></span>



| <span data-ttu-id="88065-121">ICE91-Warnung</span><span class="sxs-lookup"><span data-stu-id="88065-121">ICE91 warning</span></span>                                                                                                                                                                                                                            | <span data-ttu-id="88065-122">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="88065-122">Description</span></span>                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88065-123">Die Datei ' \[ 1 \] ' wird im pro-Benutzerverzeichnis ' \[ 2 ' installiert \] , das sich nicht basierend auf dem [**ALLUSERS**](allusers.md) -Wert unterscheidet.</span><span class="sxs-lookup"><span data-stu-id="88065-123">The file '\[1\]' will be installed to the per user directory '\[2\]' that does not vary based on [**ALLUSERS**](allusers.md) value.</span></span> <span data-ttu-id="88065-124">Diese Datei wird nicht in das Profil jedes Benutzers kopiert, auch wenn eine Installation pro Computer gewünscht ist.</span><span class="sxs-lookup"><span data-stu-id="88065-124">This file won't be copied to each user's profile even if a per machine installation is desired.</span></span>     | <span data-ttu-id="88065-125">Die Datei wird in einem Verzeichnis pro Benutzer installiert.</span><span class="sxs-lookup"><span data-stu-id="88065-125">The file is installed into a per-user only directory.</span></span> <span data-ttu-id="88065-126">Sie wird während einer Installation pro Computer nicht in den Profilen der einzelnen Benutzer installiert.</span><span class="sxs-lookup"><span data-stu-id="88065-126">It is not installed into each user's profile during a per-machine installation.</span></span>      |
| <span data-ttu-id="88065-127">Die IniFile ' \[ 1 \] ' wird im pro-Benutzerverzeichnis ' \[ 2 ' installiert \] , das je nach Wert von [**ALLUSERS**](allusers.md) nicht unterschiedlich ist.</span><span class="sxs-lookup"><span data-stu-id="88065-127">The IniFile '\[1\]' will be installed to the per user directory '\[2\]' that does not vary based on [**ALLUSERS**](allusers.md) value.</span></span> <span data-ttu-id="88065-128">Diese Datei wird nicht in das Profil jedes Benutzers kopiert, auch wenn eine Installation pro Computer gewünscht ist.</span><span class="sxs-lookup"><span data-stu-id="88065-128">This file won't be copied to each user's profile even if a per machine installation is desired.</span></span>  | <span data-ttu-id="88065-129">Die INI-Datei wird in einem Verzeichnis pro Benutzer installiert.</span><span class="sxs-lookup"><span data-stu-id="88065-129">The .ini file is installed into a per-user only directory.</span></span> <span data-ttu-id="88065-130">Sie wird während einer Installation pro Computer nicht in den Profilen der einzelnen Benutzer installiert.</span><span class="sxs-lookup"><span data-stu-id="88065-130">It is not installed into each user's profile during a per-machine installation.</span></span> |
| <span data-ttu-id="88065-131">Die Verknüpfung ' \[ 1 \] ' wird im pro-Benutzerverzeichnis ' \[ 2 ' installiert \] , das je nach Wert von [**ALLUSERS**](allusers.md) nicht variiert.</span><span class="sxs-lookup"><span data-stu-id="88065-131">The shortcut '\[1\]' will be installed to the per user directory '\[2\]' that does not vary based on [**ALLUSERS**](allusers.md) value.</span></span> <span data-ttu-id="88065-132">Diese Datei wird nicht in das Profil jedes Benutzers kopiert, auch wenn eine Installation pro Computer gewünscht ist.</span><span class="sxs-lookup"><span data-stu-id="88065-132">This file won't be copied to each user's profile even if a per machine installation is desired.</span></span> | <span data-ttu-id="88065-133">Die Verknüpfung wird in einem Verzeichnis pro Benutzer installiert.</span><span class="sxs-lookup"><span data-stu-id="88065-133">The shortcut is installed into a per-user only directory.</span></span> <span data-ttu-id="88065-134">Sie wird während einer Installation pro Computer nicht in den Profilen der einzelnen Benutzer installiert.</span><span class="sxs-lookup"><span data-stu-id="88065-134">It is not installed into each user's profile during a per-machine installation.</span></span>  |



 

## <a name="example"></a><span data-ttu-id="88065-135">Beispiel</span><span class="sxs-lookup"><span data-stu-id="88065-135">Example</span></span>

<span data-ttu-id="88065-136">ICE91 meldet die folgenden Warnungen für das Beispiel:</span><span class="sxs-lookup"><span data-stu-id="88065-136">ICE91 reports the following warnings for the example:</span></span>

``` syntax
The file 'File1' will be installed to the per user directory 'MyPicturesFolder' that does not vary based on ALLUSERS value. This file won't be copied to each user's profile even if a per machine installation is desired.

The IniFile 'IniFile1' will be installed to the per user directory 'MyIniDir' that does not vary based on ALLUSERS value. This file won't be copied to each user's profile even if a per machine installation is desired.

The shortcut 'Shortcut1' will be installed to the per user directory 'MyShortcutDir' that does not vary based on ALLUSERS value. This file won't be copied to each user's profile even if a per machine installation is desired.
```

<span data-ttu-id="88065-137">[Dateitabelle](file-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="88065-137">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="88065-138">File</span><span class="sxs-lookup"><span data-stu-id="88065-138">File</span></span>  | <span data-ttu-id="88065-139">Komponente\_</span><span class="sxs-lookup"><span data-stu-id="88065-139">Component\_</span></span> |
|-------|-------------|
| <span data-ttu-id="88065-140">Datei1</span><span class="sxs-lookup"><span data-stu-id="88065-140">File1</span></span> | <span data-ttu-id="88065-141">C1</span><span class="sxs-lookup"><span data-stu-id="88065-141">C1</span></span>          |



 

<span data-ttu-id="88065-142">[Komponenten Tabelle](component-table.md) (teilweise) (teilweise) (teilweise) (teilweise)</span><span class="sxs-lookup"><span data-stu-id="88065-142">[Component Table](component-table.md) (partial) (partial) (partial) (partial)</span></span>



| <span data-ttu-id="88065-143">Komponente</span><span class="sxs-lookup"><span data-stu-id="88065-143">Component</span></span> | <span data-ttu-id="88065-144">Verzeichnis\_</span><span class="sxs-lookup"><span data-stu-id="88065-144">Directory\_</span></span> |
|-----------|-------------|
| <span data-ttu-id="88065-145">C1</span><span class="sxs-lookup"><span data-stu-id="88065-145">C1</span></span>        | <span data-ttu-id="88065-146">"MyDir"</span><span class="sxs-lookup"><span data-stu-id="88065-146">MyDir</span></span>       |



 

[<span data-ttu-id="88065-147">INIFILE-Tabelle</span><span class="sxs-lookup"><span data-stu-id="88065-147">IniFile Table</span></span>](inifile-table.md)



| <span data-ttu-id="88065-148">INIFILE</span><span class="sxs-lookup"><span data-stu-id="88065-148">IniFile</span></span>  | <span data-ttu-id="88065-149">Dirproperty</span><span class="sxs-lookup"><span data-stu-id="88065-149">DirProperty</span></span> |
|----------|-------------|
| <span data-ttu-id="88065-150">IniFile1</span><span class="sxs-lookup"><span data-stu-id="88065-150">IniFile1</span></span> | <span data-ttu-id="88065-151">Myinidir</span><span class="sxs-lookup"><span data-stu-id="88065-151">MyIniDir</span></span>    |



 

[<span data-ttu-id="88065-152">Verknüpfungs Tabelle</span><span class="sxs-lookup"><span data-stu-id="88065-152">Shortcut Table</span></span>](shortcut-table.md)



| <span data-ttu-id="88065-153">Abkürzung</span><span class="sxs-lookup"><span data-stu-id="88065-153">Shortcut</span></span>  | <span data-ttu-id="88065-154">Verzeichnis\_</span><span class="sxs-lookup"><span data-stu-id="88065-154">Directory\_</span></span>   |
|-----------|---------------|
| <span data-ttu-id="88065-155">Shortcut1</span><span class="sxs-lookup"><span data-stu-id="88065-155">Shortcut1</span></span> | <span data-ttu-id="88065-156">Myshortcutdir</span><span class="sxs-lookup"><span data-stu-id="88065-156">MyShortcutDir</span></span> |



 

[<span data-ttu-id="88065-157">Verzeichnis Tabelle</span><span class="sxs-lookup"><span data-stu-id="88065-157">Directory Table</span></span>](directory-table.md)



| <span data-ttu-id="88065-158">Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="88065-158">Directory</span></span>     | <span data-ttu-id="88065-159">Über \_ geordnetes Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="88065-159">Directory\_Parent</span></span>  |
|---------------|--------------------|
| <span data-ttu-id="88065-160">"MyDir"</span><span class="sxs-lookup"><span data-stu-id="88065-160">MyDir</span></span>         | <span data-ttu-id="88065-161">FavoritesFolder</span><span class="sxs-lookup"><span data-stu-id="88065-161">FavoritesFolder</span></span>    |
| <span data-ttu-id="88065-162">Myinidir</span><span class="sxs-lookup"><span data-stu-id="88065-162">MyIniDir</span></span>      | <span data-ttu-id="88065-163">Localappdatafolder</span><span class="sxs-lookup"><span data-stu-id="88065-163">LocalAppDataFolder</span></span> |
| <span data-ttu-id="88065-164">Myshortcutdir</span><span class="sxs-lookup"><span data-stu-id="88065-164">MyShortcutDir</span></span> | <span data-ttu-id="88065-165">PersonalFolder</span><span class="sxs-lookup"><span data-stu-id="88065-165">PersonalFolder</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="88065-166">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="88065-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="88065-167">Ice-Referenz</span><span class="sxs-lookup"><span data-stu-id="88065-167">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



