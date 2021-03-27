---
description: 'Das System speichert Benutzerprofil Informationen in einem bestimmten Verzeichnis, das in verschiedenen Versionen von Windows unterschiedliche Namen hat: &\# 0034; Dokumente und Einstellungen&\# 0034; in Windows XP und &\# 0034; Benutzer&\# 0034; in Windows Vista und höher.'
title: Profile-Verzeichnis
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 41056f40-fa1a-488a-b213-49cbdd8d4fdf
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 3eb310434e5665dd8f28a661785403d72c4c1e46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104979952"
---
# <a name="profiles-directory"></a><span data-ttu-id="ab80c-103">Profile-Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="ab80c-103">Profiles Directory</span></span>

<span data-ttu-id="ab80c-104">Das System speichert Benutzerprofil Informationen in einem bestimmten Verzeichnis, das in verschiedenen Versionen von Windows unterschiedliche Namen hat: "Dokumente und Einstellungen" in Windows XP und "Benutzer" in Windows Vista und höher.</span><span class="sxs-lookup"><span data-stu-id="ab80c-104">The system stores user profile information in a specific directory, which has different names in different versions of Windows: "Documents and Settings" in Windows XP and "Users" in Windows Vista and later.</span></span> <span data-ttu-id="ab80c-105">Verwenden Sie zum Abrufen des Pfads für das Verzeichnis "Profile" die Funktion " [**GetProfilesDirectory**](/windows/desktop/api/Userenv/nf-userenv-getprofilesdirectorya) ".</span><span class="sxs-lookup"><span data-stu-id="ab80c-105">To obtain the path of the profiles directory, use the [**GetProfilesDirectory**](/windows/desktop/api/Userenv/nf-userenv-getprofilesdirectorya) function.</span></span>

<span data-ttu-id="ab80c-106">Das Verzeichnis "Profile" enthält die folgenden Unterverzeichnisse für Benutzerprofile.</span><span class="sxs-lookup"><span data-stu-id="ab80c-106">The profiles directory contains the following subdirectories for user profiles.</span></span>



| <span data-ttu-id="ab80c-107">Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="ab80c-107">Directory</span></span>                                      | <span data-ttu-id="ab80c-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ab80c-108">Description</span></span>                                                                                                                                |
|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab80c-109">ProgramData (Windows Vista oder höher)/all Benutzer</span><span class="sxs-lookup"><span data-stu-id="ab80c-109">ProgramData (Windows Vista or later)/All Users</span></span> | <span data-ttu-id="ab80c-110">Programminformationen, die für alle Benutzer gelten.</span><span class="sxs-lookup"><span data-stu-id="ab80c-110">Program information that applies to all users.</span></span> <span data-ttu-id="ab80c-111">Das Verzeichnis "alle Benutzer" ist in Windows Vista oder höher für die Abwärtskompatibilität weiterhin vorhanden.</span><span class="sxs-lookup"><span data-stu-id="ab80c-111">The All Users directory still exists in Windows Vista or later, for backward compatibility.</span></span> |
| <span data-ttu-id="ab80c-112">Standard</span><span class="sxs-lookup"><span data-stu-id="ab80c-112">Default</span></span>                                        | <span data-ttu-id="ab80c-113">Profilinformationen, die für den Standardbenutzer gelten.</span><span class="sxs-lookup"><span data-stu-id="ab80c-113">Profile information that applies to the default user.</span></span>                                                                                      |
| <span data-ttu-id="ab80c-114">*Benutzer*</span><span class="sxs-lookup"><span data-stu-id="ab80c-114">*User*</span></span>                                         | <span data-ttu-id="ab80c-115">Profilinformationen, die für den angegebenen Benutzer gelten.</span><span class="sxs-lookup"><span data-stu-id="ab80c-115">Profile information that applies to the specified user.</span></span> <span data-ttu-id="ab80c-116">Jeder Benutzer verfügt über ein eigenes Profil Unterverzeichnis.</span><span class="sxs-lookup"><span data-stu-id="ab80c-116">Each user has their own profile subdirectory.</span></span>                                      |



 

<span data-ttu-id="ab80c-117">Rufen Sie die [**getallusersprofiledirectory**](/windows/desktop/api/Userenv/nf-userenv-getallusersprofiledirectorya) -Funktion auf, um den Speicherort des Verzeichnisses ProgramData/all users zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="ab80c-117">To obtain the location of the ProgramData/All Users directory, call the [**GetAllUsersProfileDirectory**](/windows/desktop/api/Userenv/nf-userenv-getallusersprofiledirectorya) function.</span></span> <span data-ttu-id="ab80c-118">Dieses Verzeichnis enthält die folgenden Unterverzeichnisse:</span><span class="sxs-lookup"><span data-stu-id="ab80c-118">This directory contains the following subdirectories:</span></span>



| <span data-ttu-id="ab80c-119">Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="ab80c-119">Directory</span></span>  | <span data-ttu-id="ab80c-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ab80c-120">Description</span></span>                          |
|------------|--------------------------------------|
| <span data-ttu-id="ab80c-121">Desktop</span><span class="sxs-lookup"><span data-stu-id="ab80c-121">Desktop</span></span>    | <span data-ttu-id="ab80c-122">Verknüpfungen, die auf dem Desktop angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ab80c-122">Shortcuts to display on the desktop.</span></span> |
| <span data-ttu-id="ab80c-123">Startmenü</span><span class="sxs-lookup"><span data-stu-id="ab80c-123">Start Menu</span></span> | <span data-ttu-id="ab80c-124">Menü Elemente für das **Startmenü** .</span><span class="sxs-lookup"><span data-stu-id="ab80c-124">Menu items for the **Start** menu.</span></span>   |



 

<span data-ttu-id="ab80c-125">Um den Speicherort des Standardbenutzer Verzeichnisses abzurufen, rufen Sie die [**GetDefaultUserProfileDirectory**](/windows/desktop/api/Userenv/nf-userenv-getdefaultuserprofiledirectorya) -Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="ab80c-125">To obtain the location of the default user's directory, call the [**GetDefaultUserProfileDirectory**](/windows/desktop/api/Userenv/nf-userenv-getdefaultuserprofiledirectorya) function.</span></span> <span data-ttu-id="ab80c-126">Um den Speicherort des Verzeichnisses eines bestimmten Benutzers abzurufen, rufen Sie die [**getuserprofiledirectory**](/windows/desktop/api/Userenv/nf-userenv-getuserprofiledirectorya) -Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="ab80c-126">To obtain the location of a particular user's directory, call the [**GetUserProfileDirectory**](/windows/desktop/api/Userenv/nf-userenv-getuserprofiledirectorya) function.</span></span> <span data-ttu-id="ab80c-127">Sowohl der Standardbenutzer als auch bestimmte Benutzerverzeichnisse enthalten die folgenden Unterverzeichnisse.</span><span class="sxs-lookup"><span data-stu-id="ab80c-127">Both the default user and specific user directories contain the following subdirectories.</span></span> <span data-ttu-id="ab80c-128">Kursiv formatiertes Verzeichnis geben Verzeichnisse an, die standardmäßig ausgeblendet sind.</span><span class="sxs-lookup"><span data-stu-id="ab80c-128">Directories in italics indicate directories that are hidden by default.</span></span> <span data-ttu-id="ab80c-129">Sie können diese Verzeichnisse anzeigen, indem Sie die Option Ausgeblendete **Dateien, Ordner und Laufwerke anzeigen** im System Steuerungselement **Ordneroptionen** auswählen.</span><span class="sxs-lookup"><span data-stu-id="ab80c-129">You can view these directories by selecting the **Show hidden files, folders, and drives** option in the **Folder Options** control panel item.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ab80c-130">Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="ab80c-130">Directory</span></span></th>
<th><span data-ttu-id="ab80c-131">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ab80c-131">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ab80c-132">Anwendungsdaten</span><span class="sxs-lookup"><span data-stu-id="ab80c-132">Application Data</span></span></td>
<td><span data-ttu-id="ab80c-133">Anwendungsspezifische Daten.</span><span class="sxs-lookup"><span data-stu-id="ab80c-133">Application-specific data.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ab80c-134">Cookies</span><span class="sxs-lookup"><span data-stu-id="ab80c-134">Cookies</span></span></td>
<td><span data-ttu-id="ab80c-135">Windows Internet Explorer-Cookies.</span><span class="sxs-lookup"><span data-stu-id="ab80c-135">Windows Internet Explorer cookies.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ab80c-136">Desktop</span><span class="sxs-lookup"><span data-stu-id="ab80c-136">Desktop</span></span></td>
<td><span data-ttu-id="ab80c-137">Verknüpfungen, die auf dem Desktop angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ab80c-137">Shortcuts to display on the desktop.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ab80c-138">Favoriten</span><span class="sxs-lookup"><span data-stu-id="ab80c-138">Favorites</span></span></td>
<td><span data-ttu-id="ab80c-139">Links zu bevorzugten Websites.</span><span class="sxs-lookup"><span data-stu-id="ab80c-139">Links to favorite websites.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ab80c-140">Lokale Einstellungen</span><span class="sxs-lookup"><span data-stu-id="ab80c-140">Local Settings</span></span></td>
<td><span data-ttu-id="ab80c-141">Anwendungseinstellungen und Daten, die nicht mit dem Profil wechseln.</span><span class="sxs-lookup"><span data-stu-id="ab80c-141">Application settings and data that do not roam with the profile.</span></span> <span data-ttu-id="ab80c-142">In der Regel sind die Einstellungen oder Daten in diesem Verzeichnis Computer spezifisch, oder Sie sind zu groß, um effektiv zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="ab80c-142">Usually the settings or data in this directory are computer-specific, or they are too large to roam effectively.</span></span> <span data-ttu-id="ab80c-143">Dieses Verzeichnis enthält die folgenden Unterordner:</span><span class="sxs-lookup"><span data-stu-id="ab80c-143">This directory contains the following subfolders:</span></span>
<ul>
<li><span data-ttu-id="ab80c-144">Anwendungsdaten</span><span class="sxs-lookup"><span data-stu-id="ab80c-144">Application Data</span></span></li>
<li><span data-ttu-id="ab80c-145">Verlauf</span><span class="sxs-lookup"><span data-stu-id="ab80c-145">History</span></span></li>
<li><span data-ttu-id="ab80c-146">Temp</span><span class="sxs-lookup"><span data-stu-id="ab80c-146">Temp</span></span></li>
<li><span data-ttu-id="ab80c-147">Temporäre Internetdateien</span><span class="sxs-lookup"><span data-stu-id="ab80c-147">Temporary Internet Files</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ab80c-148">Meine Dokumente</span><span class="sxs-lookup"><span data-stu-id="ab80c-148">My Documents</span></span></td>
<td><span data-ttu-id="ab80c-149">Der Standard Speicherort für Dokumente, die der Benutzer erstellt.</span><span class="sxs-lookup"><span data-stu-id="ab80c-149">The default location for documents that the user creates.</span></span> <span data-ttu-id="ab80c-150">Anwendungen sollten Dokument Dateien standardmäßig in diesem Verzeichnis speichern.</span><span class="sxs-lookup"><span data-stu-id="ab80c-150">Applications should save document files to this directory by default.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ab80c-151"><em>Nicht mehr</em></span><span class="sxs-lookup"><span data-stu-id="ab80c-151"><em>NetHood</em></span></span></td>
<td><span data-ttu-id="ab80c-152">Verknüpfungen zu Netzwerk-Nachbarschafts Elementen.</span><span class="sxs-lookup"><span data-stu-id="ab80c-152">Shortcuts to Network Neighborhood items.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ab80c-153"><em>Printhood</em></span><span class="sxs-lookup"><span data-stu-id="ab80c-153"><em>PrintHood</em></span></span></td>
<td><span data-ttu-id="ab80c-154">Verknüpfungen zu Drucker Ordner Elementen.</span><span class="sxs-lookup"><span data-stu-id="ab80c-154">Shortcuts to printer folder items.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ab80c-155"><em>Zuletzt verwendete</em></span><span class="sxs-lookup"><span data-stu-id="ab80c-155"><em>Recent</em></span></span></td>
<td><span data-ttu-id="ab80c-156">Verknüpfungen zu den zuletzt verwendeten Dokumenten.</span><span class="sxs-lookup"><span data-stu-id="ab80c-156">Shortcuts to the most recently used documents.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ab80c-157">SendTo</span><span class="sxs-lookup"><span data-stu-id="ab80c-157">SendTo</span></span></td>
<td><span data-ttu-id="ab80c-158">Verknüpfungen zu Speicherorten, an die der Benutzer häufig Dateien sendet.</span><span class="sxs-lookup"><span data-stu-id="ab80c-158">Shortcuts to locations to which the user often sends files.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ab80c-159">Startmenü</span><span class="sxs-lookup"><span data-stu-id="ab80c-159">Start Menu</span></span></td>
<td><span data-ttu-id="ab80c-160">Menü Elemente für das <strong>Startmenü</strong> .</span><span class="sxs-lookup"><span data-stu-id="ab80c-160">Menu items for the <strong>Start</strong> menu.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ab80c-161"><em>Vorlagen</em></span><span class="sxs-lookup"><span data-stu-id="ab80c-161"><em>Templates</em></span></span></td>
<td><span data-ttu-id="ab80c-162">Verknüpfungen zu Vorlagen Elementen.</span><span class="sxs-lookup"><span data-stu-id="ab80c-162">Shortcuts to template items.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="ab80c-163">Wenn Sie den Speicherort der Unterverzeichnisse dieser Verzeichnisse abrufen möchten, verwenden Sie die Funktionen " [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) " oder " [**shgetknownfolderpath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) ".</span><span class="sxs-lookup"><span data-stu-id="ab80c-163">To obtain the location of subdirectories of these directories, use the [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) or [**SHGetKnownFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) functions.</span></span>

 

 



