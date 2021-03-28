---
description: In diesem Abschnitt werden die von der Shell implementierten Windows-Objekte beschrieben.
title: Shellobjekte für Skripterstellung und Microsoft-Visual Basic
ms.topic: article
ms.date: 05/31/2018
ms.assetid: eee58404-808b-451c-8325-8dcd9537fd11
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 52958c68edfd81771267c7a7ed29e42ab8ed1d5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529423"
---
# <a name="shell-objects-for-scripting-and-microsoft-visual-basic"></a><span data-ttu-id="51a29-103">Shellobjekte für Skripterstellung und Microsoft-Visual Basic</span><span class="sxs-lookup"><span data-stu-id="51a29-103">Shell Objects for Scripting and Microsoft Visual Basic</span></span>

<span data-ttu-id="51a29-104">In diesem Abschnitt werden die von der Shell implementierten Windows-Objekte beschrieben.</span><span class="sxs-lookup"><span data-stu-id="51a29-104">This section describes the Windows objects implemented by the Shell.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="51a29-105">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="51a29-105">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="51a29-106">Thema</span><span class="sxs-lookup"><span data-stu-id="51a29-106">Topic</span></span></th>
<th><span data-ttu-id="51a29-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="51a29-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="51a29-108"><a href="didiskquotauser-object.md"><strong>Didiskquotauser</strong></a></span><span class="sxs-lookup"><span data-stu-id="51a29-108"><a href="didiskquotauser-object.md"><strong>DIDiskQuotaUser</strong></a></span></span><br/></td>
<td><span data-ttu-id="51a29-109">Ermöglicht einem Client, die globalen Datenträger Kontingent Einstellungen eines NTFS-Volumes zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="51a29-109">Allows a client to manage an NTFS volume's global disk quota settings.</span></span> <span data-ttu-id="51a29-110">Dieses Objekt stellt die wesentlichen Funktionen der <a href="didiskquotauser-object.md"><strong>didiskquotauser</strong></a> -Schnittstelle für Skript-und Microsoft Visual Basic-basierte Anwendungen zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="51a29-110">This object makes the essential functionality of the <a href="didiskquotauser-object.md"><strong>DIDiskQuotaUser</strong></a> interface available to scripting and Microsoft Visual Basic-based applications.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="51a29-111"><a href="diskquotacontrol-object.md"><strong>Diskquotacontrol</strong></a></span><span class="sxs-lookup"><span data-stu-id="51a29-111"><a href="diskquotacontrol-object.md"><strong>DiskQuotaControl</strong></a></span></span><br/></td>
<td><span data-ttu-id="51a29-112">Ermöglicht es einem Administrator, die Datenträger Kontingent Eigenschaften eines Volumes zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="51a29-112">Allows an administrator to manage a volume's disk quota properties.</span></span> <span data-ttu-id="51a29-113">Das NTFS-Dateisystem ermöglicht einem Administrator, die Datenträger Verwendung auf einem freigegebenen Volume zu verwalten, indem jedem Benutzer eine angegebene Menge an Speicherplatz oder <em>Kontingent Limit</em>zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="51a29-113">The NTFS file system allows an administrator to manage disk usage on a shared volume by allocating a specified amount of disk space, or <em>quota limit</em>, to each user.</span></span> <span data-ttu-id="51a29-114">Mit diesem Objekt können Sie die Standard Kontingent Grenze festlegen, die automatisch allen neuen Benutzern zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="51a29-114">You can use this object to set the default quota limit that will be automatically assigned to all new users.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="51a29-115"><a href="dshellwindowsevents.md"><strong>Dshellwindowgvents</strong></a></span><span class="sxs-lookup"><span data-stu-id="51a29-115"><a href="dshellwindowsevents.md"><strong>DShellWindowsEvents</strong></a></span></span><br/></td>
<td><span data-ttu-id="51a29-116">Empfängt <a href="/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows"><strong>IShellWindows</strong></a> -Fenster Registrierungs Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="51a29-116">Receives <a href="/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows"><strong>IShellWindows</strong></a> window registration events.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="51a29-117"><a href="folder.md"><strong>Ordner</strong></a></span><span class="sxs-lookup"><span data-stu-id="51a29-117"><a href="folder.md"><strong>Folder</strong></a></span></span><br/></td>
<td><span data-ttu-id="51a29-118">Stellt einen Shellordner dar.</span><span class="sxs-lookup"><span data-stu-id="51a29-118">Represents a Shell folder.</span></span> <span data-ttu-id="51a29-119">Dieses Objekt enthält Eigenschaften und Methoden, mit denen Sie Informationen zum Ordner abrufen können.</span><span class="sxs-lookup"><span data-stu-id="51a29-119">This object contains properties and methods that allow you to retrieve information about the folder.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="51a29-120"><a href="folder2-object.md"><strong>Folder2</strong></a></span><span class="sxs-lookup"><span data-stu-id="51a29-120"><a href="folder2-object.md"><strong>Folder2</strong></a></span></span><br/></td>
<td><span data-ttu-id="51a29-121">Erweitert das <a href="folder.md"><strong>Ordner</strong></a> Objekt, um Offline Ordner zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="51a29-121">Extends the <a href="folder.md"><strong>Folder</strong></a> object to support offline folders.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="51a29-122"><a href="folderitem.md"><strong>Von folderItem</strong></a></span><span class="sxs-lookup"><span data-stu-id="51a29-122"><a href="folderitem.md"><strong>FolderItem</strong></a></span></span><br/></td>
<td><span data-ttu-id="51a29-123">Stellt ein Element in einem Shellordner dar.</span><span class="sxs-lookup"><span data-stu-id="51a29-123">Represents an item in a Shell folder.</span></span> <span data-ttu-id="51a29-124">Dieses Objekt enthält Eigenschaften und Methoden, mit denen Sie Informationen über das Element abrufen können.</span><span class="sxs-lookup"><span data-stu-id="51a29-124">This object contains properties and methods that allow you to retrieve information about the item.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="51a29-125"><a href="folderitems.md"><strong>Folderitems</strong></a></span><span class="sxs-lookup"><span data-stu-id="51a29-125"><a href="folderitems.md"><strong>FolderItems</strong></a></span></span><br/></td>
<td><span data-ttu-id="51a29-126">Stellt die Auflistung von Elementen in einem Shellordner dar.</span><span class="sxs-lookup"><span data-stu-id="51a29-126">Represents the collection of items in a Shell folder.</span></span> <span data-ttu-id="51a29-127">Dieses Objekt enthält Eigenschaften und Methoden, mit denen Sie Informationen über die Auflistung abrufen können.</span><span class="sxs-lookup"><span data-stu-id="51a29-127">This object contains properties and methods that allow you to retrieve information about the collection.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="51a29-128"><a href="folderitems2-object.md"><strong>FolderItems2</strong></a></span><span class="sxs-lookup"><span data-stu-id="51a29-128"><a href="folderitems2-object.md"><strong>FolderItems2</strong></a></span></span><br/></td>
<td><span data-ttu-id="51a29-129">Erweitert das <a href="folderitems.md"><strong>folderitems</strong></a> -Objekt.</span><span class="sxs-lookup"><span data-stu-id="51a29-129">Extends the <a href="folderitems.md"><strong>FolderItems</strong></a> object.</span></span> <span data-ttu-id="51a29-130">Es wird eine zusätzliche Methode unterstützt.</span><span class="sxs-lookup"><span data-stu-id="51a29-130">It supports one additional method.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="51a29-131"><a href="folderitems3-object.md"><strong>FolderItems3</strong></a></span><span class="sxs-lookup"><span data-stu-id="51a29-131"><a href="folderitems3-object.md"><strong>FolderItems3</strong></a></span></span><br/></td>
<td><span data-ttu-id="51a29-132">Erweitert das <a href="folderitems2-object.md"><strong>FolderItems2</strong></a> -Objekt.</span><span class="sxs-lookup"><span data-stu-id="51a29-132">Extends the <a href="folderitems2-object.md"><strong>FolderItems2</strong></a> object.</span></span> <span data-ttu-id="51a29-133">Dieses Objekt unterstützt eine zusätzliche Methode und Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="51a29-133">This object supports an additional method and property.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="51a29-134"><a href="folderitemverb.md"><strong>Folderitemverb</strong></a></span><span class="sxs-lookup"><span data-stu-id="51a29-134"><a href="folderitemverb.md"><strong>FolderItemVerb</strong></a></span></span><br/></td>
<td><span data-ttu-id="51a29-135">Stellt ein einzelnes Verb dar, das einem Element zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="51a29-135">Represents a single verb available to an item.</span></span> <span data-ttu-id="51a29-136">Dieses Objekt enthält Eigenschaften und Methoden, mit denen Sie Informationen über das Verb abrufen können.</span><span class="sxs-lookup"><span data-stu-id="51a29-136">This object contains properties and methods that allow you to retrieve information about the verb.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="51a29-137"><a href="folderitemverbs.md"><strong>Folderitemverbs</strong></a></span><span class="sxs-lookup"><span data-stu-id="51a29-137"><a href="folderitemverbs.md"><strong>FolderItemVerbs</strong></a></span></span><br/></td>
<td><span data-ttu-id="51a29-138">Stellt die Auflistung von Verben für ein Element in einem Shellordner dar.</span><span class="sxs-lookup"><span data-stu-id="51a29-138">Represents the collection of verbs for an item in a Shell folder.</span></span> <span data-ttu-id="51a29-139">Dieses Objekt enthält Eigenschaften und Methoden, mit denen Sie Informationen über die Auflistung abrufen können.</span><span class="sxs-lookup"><span data-stu-id="51a29-139">This object contains properties and methods that allow you to retrieve information about the collection.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="51a29-140"><a href="ishelldispatch.md"><strong>Ishelldispatch</strong></a></span><span class="sxs-lookup"><span data-stu-id="51a29-140"><a href="ishelldispatch.md"><strong>IShellDispatch</strong></a></span></span><br/></td>
<td><span data-ttu-id="51a29-141">Stellt ein Objekt in der Shell dar.</span><span class="sxs-lookup"><span data-stu-id="51a29-141">Represents an object in the Shell.</span></span> <span data-ttu-id="51a29-142">Es werden Methoden bereitgestellt, um die Shell zu steuern und um Befehle in der Shell auszuführen.</span><span class="sxs-lookup"><span data-stu-id="51a29-142">Methods are provided to control the Shell and to execute commands within the Shell.</span></span> <span data-ttu-id="51a29-143">Es gibt auch Methoden zum Abrufen anderer shellbezogener Objekte.</span><span class="sxs-lookup"><span data-stu-id="51a29-143">There are also methods to obtain other Shell-related objects.</span></span> <br/>
<blockquote>
[!Note]<br /><span data-ttu-id="51a29-144">
<a href="ishelldispatch.md"><strong>Ishelldispatch</strong></a> wird implementiert und über das <a href="shell.md"><strong>Shellobjekt</strong></a> aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="51a29-144">
<a href="ishelldispatch.md"><strong>IShellDispatch</strong></a> is implemented and accessed through the <a href="shell.md"><strong>Shell</strong></a> object.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="51a29-145"><a href="ishelldispatch2-object.md"><strong>IShellDispatch2</strong></a></span><span class="sxs-lookup"><span data-stu-id="51a29-145"><a href="ishelldispatch2-object.md"><strong>IShellDispatch2</strong></a></span></span><br/></td>
<td><span data-ttu-id="51a29-146">Erweitert das <a href="ishelldispatch.md"><strong>ishelldispatch</strong></a> -Objekt mit einer Reihe von neuen Funktionen.</span><span class="sxs-lookup"><span data-stu-id="51a29-146">Extends the <a href="ishelldispatch.md"><strong>IShellDispatch</strong></a> object with a variety of new functionality.</span></span> <br/>
<blockquote>
[!Note]<br /><span data-ttu-id="51a29-147">
<a href="ishelldispatch2-object.md"><strong>IShellDispatch2</strong></a> wird implementiert, und der Zugriff erfolgt über das <a href="shell.md"><strong>Shellobjekt</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="51a29-147">
<a href="ishelldispatch2-object.md"><strong>IShellDispatch2</strong></a> is implemented and accessed through the <a href="shell.md"><strong>Shell</strong></a> object.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="51a29-148"><a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a></span><span class="sxs-lookup"><span data-stu-id="51a29-148"><a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a></span></span><br/></td>
<td><span data-ttu-id="51a29-149">Erweitert das <a href="ishelldispatch2-object.md"><strong>IShellDispatch2</strong></a> -Objekt.</span><span class="sxs-lookup"><span data-stu-id="51a29-149">Extends the <a href="ishelldispatch2-object.md"><strong>IShellDispatch2</strong></a> object.</span></span> <span data-ttu-id="51a29-150"><a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a> unterstützt eine neue Methode zusätzlich zu den Eigenschaften und Methoden, die von <strong>IShellDispatch2</strong>unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="51a29-150"><a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a> supports one new method in addition to the properties and methods supported by <strong>IShellDispatch2</strong>.</span></span> <br/>
<blockquote>
[!Note]<br /><span data-ttu-id="51a29-151">
<a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a> wird implementiert, und der Zugriff erfolgt über das <a href="shell.md"><strong>Shellobjekt</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="51a29-151">
<a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a> is implemented and accessed through the <a href="shell.md"><strong>Shell</strong></a> object.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="51a29-152"><a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a></span><span class="sxs-lookup"><span data-stu-id="51a29-152"><a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a></span></span><br/></td>
<td><span data-ttu-id="51a29-153">Erweitert das <a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a> -Objekt.</span><span class="sxs-lookup"><span data-stu-id="51a29-153">Extends the <a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a> object.</span></span> <span data-ttu-id="51a29-154">Zusätzlich zu den Eigenschaften und Methoden, die von <strong>IShellDispatch3</strong>unterstützt werden, unterstützt <a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a> vier zusätzliche Methoden.</span><span class="sxs-lookup"><span data-stu-id="51a29-154">In addition to the properties and methods supported by <strong>IShellDispatch3</strong>, <a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a> supports four additional methods.</span></span> <br/>
<blockquote>
[!Note]<br /><span data-ttu-id="51a29-155">
<a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a> wird implementiert, und der Zugriff erfolgt über das <a href="shell.md"><strong>Shellobjekt</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="51a29-155">
<a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a> is implemented and accessed through the <a href="shell.md"><strong>Shell</strong></a> object.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="51a29-156"><a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a></span><span class="sxs-lookup"><span data-stu-id="51a29-156"><a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a></span></span><br/></td>
<td><span data-ttu-id="51a29-157">Erweitert das <a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a> -Objekt.</span><span class="sxs-lookup"><span data-stu-id="51a29-157">Extends the <a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a> object.</span></span> <span data-ttu-id="51a29-158">Zusätzlich zu den Eigenschaften und Methoden, die von <strong>IShellDispatch4</strong>unterstützt werden, fügt <a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a> eine Methode hinzu, die geöffnete Fenster in einem 3D-Stapel anzeigt.</span><span class="sxs-lookup"><span data-stu-id="51a29-158">In addition to the properties and methods supported by <strong>IShellDispatch4</strong>, <a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a> adds a method that displays open windows in a 3D stack.</span></span> <br/>
<blockquote>
[!Note]<br /><span data-ttu-id="51a29-159">
<a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a> wird implementiert, und der Zugriff erfolgt über das <a href="shell.md"><strong>Shellobjekt</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="51a29-159">
<a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a> is implemented and accessed through the <a href="shell.md"><strong>Shell</strong></a> object.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="51a29-160"><a href="ishelldispatch6.md"><strong>IShellDispatch6</strong></a></span><span class="sxs-lookup"><span data-stu-id="51a29-160"><a href="ishelldispatch6.md"><strong>IShellDispatch6</strong></a></span></span><br/></td>
<td><span data-ttu-id="51a29-161">Erweitert das <a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a> -Objekt.</span><span class="sxs-lookup"><span data-stu-id="51a29-161">Extends the <a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a> object.</span></span> <span data-ttu-id="51a29-162">Zusätzlich zu den Eigenschaften und Methoden, die von <strong>IShellDispatch5</strong>unterstützt werden, fügt <a href="ishelldispatch6.md"><strong>IShellDispatch6</strong></a> eine Methode hinzu, die den Suchbereich apps anzeigt.</span><span class="sxs-lookup"><span data-stu-id="51a29-162">In addition to the properties and methods supported by <strong>IShellDispatch5</strong>, <a href="ishelldispatch6.md"><strong>IShellDispatch6</strong></a> adds a method that displays the Apps Search pane.</span></span> <br/>
<blockquote>
[!Note]<br /><span data-ttu-id="51a29-163">
<a href="ishelldispatch6.md"><strong>IShellDispatch6</strong></a> wird implementiert, und der Zugriff erfolgt über das <a href="shell.md"><strong>Shellobjekt</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="51a29-163">
<a href="ishelldispatch6.md"><strong>IShellDispatch6</strong></a> is implemented and accessed through the <a href="shell.md"><strong>Shell</strong></a> object.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="51a29-164"><a href="ishelllinkdual2-object.md"><strong>IShellLinkDual2</strong></a></span><span class="sxs-lookup"><span data-stu-id="51a29-164"><a href="ishelllinkdual2-object.md"><strong>IShellLinkDual2</strong></a></span></span><br/></td>
<td><span data-ttu-id="51a29-165">Erweitert das <a href="shelllinkobject-object.md"><strong>shelllinkobject</strong></a> -Objekt und unterstützt eine zusätzliche Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="51a29-165">Extends the <a href="shelllinkobject-object.md"><strong>ShellLinkObject</strong></a> object and supports one additional property.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="51a29-166"><a href="newwdevents.md"><strong>Newwentvents</strong></a></span><span class="sxs-lookup"><span data-stu-id="51a29-166"><a href="newwdevents.md"><strong>NewWDEvents</strong></a></span></span><br/></td>
<td><span data-ttu-id="51a29-167">Erweitert das <a href="webwizardhost.md"><strong>webwizardhost</strong></a> -Objekt durch Aktivieren von serverseitigen Seiten, die in einem Assistenten gehostet werden, um zu überprüfen, ob der Benutzer über eine Microsoft-Konto authentifiziert wurde.</span><span class="sxs-lookup"><span data-stu-id="51a29-167">Extends the <a href="webwizardhost.md"><strong>WebWizardHost</strong></a> object by enabling server-side pages hosted in a wizard to verify that the user has been authenticated through a Microsoft account.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="51a29-168"><a href="shell.md"><strong>Shell</strong></a></span><span class="sxs-lookup"><span data-stu-id="51a29-168"><a href="shell.md"><strong>Shell</strong></a></span></span><br/></td>
<td><span data-ttu-id="51a29-169">Stellt die-Objekte in der Shell dar.</span><span class="sxs-lookup"><span data-stu-id="51a29-169">Represents the objects in the Shell.</span></span> <span data-ttu-id="51a29-170">Es werden Methoden bereitgestellt, um die Shell zu steuern und um Befehle in der Shell auszuführen.</span><span class="sxs-lookup"><span data-stu-id="51a29-170">Methods are provided to control the Shell and to execute commands within the Shell.</span></span> <span data-ttu-id="51a29-171">Es gibt auch Methoden zum Abrufen anderer shellbezogener Objekte.</span><span class="sxs-lookup"><span data-stu-id="51a29-171">There are also methods to obtain other Shell-related objects.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="51a29-172"><a href="shellfolderitem-object.md"><strong>Shellfolderitem</strong></a></span><span class="sxs-lookup"><span data-stu-id="51a29-172"><a href="shellfolderitem-object.md"><strong>ShellFolderItem</strong></a></span></span><br/></td>
<td><span data-ttu-id="51a29-173">Erweitert das <a href="folderitem.md"><strong>folderItem</strong></a> -Objekt.</span><span class="sxs-lookup"><span data-stu-id="51a29-173">Extends the <a href="folderitem.md"><strong>FolderItem</strong></a> object.</span></span> <span data-ttu-id="51a29-174">Zusätzlich zu den Eigenschaften und Methoden, die von <strong>folderItem</strong>unterstützt werden, verfügt <a href="shellfolderitem-object.md"><strong>shellfolderitem</strong></a> über zwei zusätzliche Methoden.</span><span class="sxs-lookup"><span data-stu-id="51a29-174">In addition to the properties and methods supported by <strong>FolderItem</strong>, <a href="shellfolderitem-object.md"><strong>ShellFolderItem</strong></a> has two additional methods.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="51a29-175"><a href="shellfolderview.md"><strong>Shellfolderview</strong></a></span><span class="sxs-lookup"><span data-stu-id="51a29-175"><a href="shellfolderview.md"><strong>ShellFolderView</strong></a></span></span><br/></td>
<td><span data-ttu-id="51a29-176">Stellt die Objekte in einer Ansicht dar und stellt Eigenschaften und Methoden bereit, die zum Abrufen von Informationen über den Inhalt der Ansicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="51a29-176">Represents the objects in a view and provides properties and methods used to obtain information about the contents of the view.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="51a29-177"><a href="shellfolderviewoc-object.md"><strong>Shellfolderviewoc</strong></a></span><span class="sxs-lookup"><span data-stu-id="51a29-177"><a href="shellfolderviewoc-object.md"><strong>ShellFolderViewOC</strong></a></span></span><br/></td>
<td><span data-ttu-id="51a29-178">Leitet die von einem angegebenen <a href="shellfolderview.md"><strong>shellfolderview</strong></a> -Objekt ausgelösten Ereignisse an entsprechende <a href="shellfolderviewoc-object.md"><strong>shellfolderviewoc</strong></a> -Ereignishandler weiter.</span><span class="sxs-lookup"><span data-stu-id="51a29-178">Forwards the events fired by a specified <a href="shellfolderview.md"><strong>ShellFolderView</strong></a> object to corresponding <a href="shellfolderviewoc-object.md"><strong>ShellFolderViewOC</strong></a> event handlers.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="51a29-179"><a href="shelllinkobject-object.md"><strong>Shelllinkobject</strong></a></span><span class="sxs-lookup"><span data-stu-id="51a29-179"><a href="shelllinkobject-object.md"><strong>ShellLinkObject</strong></a></span></span><br/></td>
<td><span data-ttu-id="51a29-180">Verwaltet shelllinks.</span><span class="sxs-lookup"><span data-stu-id="51a29-180">Manages Shell links.</span></span> <span data-ttu-id="51a29-181">Dieses Objekt stellt einen Großteil der Funktionen der <a href="/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka"><strong>IShellLink</strong></a> -Schnittstelle für Skript Anwendungen zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="51a29-181">This object makes much of the functionality of the <a href="/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka"><strong>IShellLink</strong></a> interface available to scripting applications.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="51a29-182"><a href="shelluihelper.md"><strong>Shelluihelper</strong></a></span><span class="sxs-lookup"><span data-stu-id="51a29-182"><a href="shelluihelper.md"><strong>ShellUIHelper</strong></a></span></span><br/></td>
<td><span data-ttu-id="51a29-183">Wird von der Shell implementiert, um Skripts und Visual Basic Entwicklern zu helfen, einige der in der Shell verfügbaren Features zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="51a29-183">Implemented by the Shell to help script and Visual Basic developers use some of the features available in the Shell.</span></span> <span data-ttu-id="51a29-184">Das <a href="shelluihelper.md"><strong>shelluihelper</strong></a> -Objekt hat keine Eigenschaften oder Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="51a29-184">The <a href="shelluihelper.md"><strong>ShellUIHelper</strong></a> object does not have any properties or events.</span></span> <span data-ttu-id="51a29-185">Es werden Methoden bereitgestellt, um der Shell Elemente hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="51a29-185">Methods are provided to add items to the Shell.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="51a29-186"><a href="shellwindows.md"><strong>Shellwindows</strong></a></span><span class="sxs-lookup"><span data-stu-id="51a29-186"><a href="shellwindows.md"><strong>ShellWindows</strong></a></span></span><br/></td>
<td><span data-ttu-id="51a29-187">Stellt eine Auflistung der geöffneten Fenster dar, die zur Shell gehören.</span><span class="sxs-lookup"><span data-stu-id="51a29-187">Represents a collection of the open windows that belong to the Shell.</span></span> <span data-ttu-id="51a29-188">Mit diesen Objekten verknüpfte Methoden können Befehle in der Shell Steuern und ausführen sowie andere shellbezogene Objekte abrufen.</span><span class="sxs-lookup"><span data-stu-id="51a29-188">Methods associated with this objects can control and execute commands within the Shell, and obtain other Shell-related objects.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="51a29-189"><a href="webwizardhost.md"><strong>Webwizardhost</strong></a></span><span class="sxs-lookup"><span data-stu-id="51a29-189"><a href="webwizardhost.md"><strong>WebWizardHost</strong></a></span></span><br/></td>
<td><span data-ttu-id="51a29-190">Macht Methoden verfügbar, mit denen HTML-Seiten aktiviert werden, die in einer Assistenten Erweiterung gehostet werden, um mit dem Assistenten zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="51a29-190">Exposes methods that enable HTML pages which are hosted in a wizard extension to communicate with the wizard.</span></span><br/></td>
</tr>
</tbody>
</table>



 

 

 




