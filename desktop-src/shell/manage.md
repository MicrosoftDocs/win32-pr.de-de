---
description: Die Shell bietet eine Reihe von Möglichkeiten zum Verwalten von Dateisystemen.
ms.assetid: d9ffda6f-adc0-44a3-b410-e23bf5f4f165
title: Verwalten des Dateisystems
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee0f3b47e17e691c540a9775f3b8588b311b9878
ms.sourcegitcommit: 822413efb4a70dd464e5db4d9e8693ef74f8132f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/09/2021
ms.locfileid: "113581618"
---
# <a name="managing-the-file-system"></a><span data-ttu-id="0e34b-103">Verwalten des Dateisystems</span><span class="sxs-lookup"><span data-stu-id="0e34b-103">Managing the File System</span></span>

<span data-ttu-id="0e34b-104">Die Shell bietet eine Reihe von Möglichkeiten zum Verwalten von Dateisystemen.</span><span class="sxs-lookup"><span data-stu-id="0e34b-104">The Shell provides a number of ways to manage file systems.</span></span> <span data-ttu-id="0e34b-105">Die Shell stellt die Funktion [**SHFileOperation bereit,**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa)mit der eine Anwendung Dateien programmgesteuert verschieben, kopieren, umbenennen und löschen kann.</span><span class="sxs-lookup"><span data-stu-id="0e34b-105">The Shell provides a function, [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa), that allows an application to programmatically move, copy, rename, and delete files.</span></span> <span data-ttu-id="0e34b-106">Die Shell unterstützt auch einige zusätzliche Dateiverwaltungsfunktionen.</span><span class="sxs-lookup"><span data-stu-id="0e34b-106">The Shell also supports some additional file management capabilities.</span></span>

-   <span data-ttu-id="0e34b-107">HTML-Dokumente können mit verwandten Dateien wie Grafikdateien oder Stylesheets *verbunden* werden.</span><span class="sxs-lookup"><span data-stu-id="0e34b-107">HTML documents can be *connected* to related files, such as graphics files or style sheets.</span></span> <span data-ttu-id="0e34b-108">Wenn das Dokument verschoben oder kopiert wird, werden die verbundenen Dateien ebenfalls automatisch verschoben oder kopiert.</span><span class="sxs-lookup"><span data-stu-id="0e34b-108">When the document is moved or copied, the connected files are automatically moved or copied as well.</span></span>
-   <span data-ttu-id="0e34b-109">Für Systeme, die für mehrere Benutzer verfügbar sind, können Dateien pro Benutzer verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="0e34b-109">For systems that are available to more than one user, files can be managed on a per-user basis.</span></span> <span data-ttu-id="0e34b-110">Benutzer haben einfachen Zugriff auf ihre Datendateien, aber nicht auf Dateien, die anderen Benutzern gehören.</span><span class="sxs-lookup"><span data-stu-id="0e34b-110">Users have easy access to their data files, but not to files belonging to other users.</span></span>
-   <span data-ttu-id="0e34b-111">Wenn Dokumentdateien hinzugefügt oder geändert werden, können sie der Shell-Liste der zuletzt verwendeten Dokumente hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="0e34b-111">If document files are added or modified, they can be added to the Shell's list of recent documents.</span></span> <span data-ttu-id="0e34b-112">Wenn der Benutzer auf dem Startmenü auf den Befehl **Dokumente** klickt, wird eine Liste mit Links zu den Dokumenten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0e34b-112">When the user clicks the **Documents** command on the Start menu, a list of links to the documents appears.</span></span>

<span data-ttu-id="0e34b-113">In diesem Dokument wird erläutert, wie diese Dateiverwaltungstechnologien funktionieren.</span><span class="sxs-lookup"><span data-stu-id="0e34b-113">This document discusses how these file management technologies work.</span></span> <span data-ttu-id="0e34b-114">Anschließend wird beschrieben, wie Sie die Shell zum Verschieben, Kopieren, Umbenennen und Löschen von Dateien verwenden und objekte im Papierkorb verwalten.</span><span class="sxs-lookup"><span data-stu-id="0e34b-114">It then outlines how to use the Shell to move, copy, rename, and delete files, and how to manage objects in the Recycle Bin.</span></span>

-   [<span data-ttu-id="0e34b-115">Dateiverwaltung pro Benutzer</span><span class="sxs-lookup"><span data-stu-id="0e34b-115">Per-User File Management</span></span>](#per-user-file-management)
-   [<span data-ttu-id="0e34b-116">Ordner "Eigene Dokumente" und "Meine Bilder"</span><span class="sxs-lookup"><span data-stu-id="0e34b-116">My Documents and My Pictures Folders</span></span>](#my-documents-and-my-pictures-folders)
-   [<span data-ttu-id="0e34b-117">Verbundene Dateien</span><span class="sxs-lookup"><span data-stu-id="0e34b-117">Connected Files</span></span>](#connected-files)
-   [<span data-ttu-id="0e34b-118">Verschieben, Kopieren, Umbenennen und Löschen von Dateien</span><span class="sxs-lookup"><span data-stu-id="0e34b-118">Moving, Copying, Renaming, and Deleting Files</span></span>](#moving-copying-renaming-and-deleting-files)
    -   [<span data-ttu-id="0e34b-119">Benachrichtigen der Shell</span><span class="sxs-lookup"><span data-stu-id="0e34b-119">Notifying the Shell</span></span>](#notifying-the-shell)
-   [<span data-ttu-id="0e34b-120">Einfaches Beispiel für die Verwaltung von Dateien mit SHFileOperation</span><span class="sxs-lookup"><span data-stu-id="0e34b-120">Simple Example of Managing Files with SHFileOperation</span></span>](#simple-example-of-managing-files-with-shfileoperation)
-   [<span data-ttu-id="0e34b-121">Hinzufügen von Dateien zur Shellliste zuletzt verwendeter Dokumente</span><span class="sxs-lookup"><span data-stu-id="0e34b-121">Adding Files to the Shell's List of Recent Documents</span></span>](#adding-files-to-the-shells-list-of-recent-documents)

## <a name="per-user-file-management"></a><span data-ttu-id="0e34b-122">Per-User Dateiverwaltung</span><span class="sxs-lookup"><span data-stu-id="0e34b-122">Per-User File Management</span></span>

<span data-ttu-id="0e34b-123">Die Windows 2000 Shell ermöglicht die Zuordnung von Dateien zu einem bestimmten Benutzer, sodass die Dateien für andere Benutzer ausgeblendet bleiben.</span><span class="sxs-lookup"><span data-stu-id="0e34b-123">The Windows 2000 Shell allows files to be associated with a particular user so the files remain hidden from other users.</span></span> <span data-ttu-id="0e34b-124">Im Hinblick auf das Dateisystem werden die Dateien im Profilordner des Benutzers gespeichert, in der Regel C: \\ Dokumente und Einstellungen \\ *Benutzername* \\ auf Windows 2000-Systemen.</span><span class="sxs-lookup"><span data-stu-id="0e34b-124">In terms of the file system, the files are stored under the user's profile folder, typically C:\\Documents and Settings\\*Username*\\ on Windows 2000 systems.</span></span> <span data-ttu-id="0e34b-125">Dieses Feature ermöglicht es vielen Personen, denselben Computer zu verwenden und gleichzeitig den Datenschutz ihrer Dateien von anderen Benutzern zu wahren.</span><span class="sxs-lookup"><span data-stu-id="0e34b-125">This feature allows many individuals to use the same computer, while maintaining the privacy of their files from other users.</span></span> <span data-ttu-id="0e34b-126">Für verschiedene Benutzer können unterschiedliche Programme verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="0e34b-126">Different users can have different programs available.</span></span> <span data-ttu-id="0e34b-127">Außerdem bietet es Administratoren und Anwendungen eine einfache Möglichkeit, z.B. Initialisierungs- (.ini) oder Linkdateien (LNK) zu speichern.</span><span class="sxs-lookup"><span data-stu-id="0e34b-127">It also provides a straightforward way for administrators and applications to store such things as initialization (.ini) or link (.lnk) files.</span></span> <span data-ttu-id="0e34b-128">Anwendungen können daher einen anderen Zustand für jeden Benutzer beibehalten und diesen bestimmten Zustand bei Bedarf problemlos wiederherstellen.</span><span class="sxs-lookup"><span data-stu-id="0e34b-128">Applications can thus preserve a different state for each user and easily recover that particular state when needed.</span></span> <span data-ttu-id="0e34b-129">Es gibt auch einen Profilordner zum Speichern von Informationen, die allen Benutzern gemeinsam sind.</span><span class="sxs-lookup"><span data-stu-id="0e34b-129">There is also a profile folder for storing information that is common to all users.</span></span>

<span data-ttu-id="0e34b-130">Da es unpraktisch ist, zu bestimmen, welcher Benutzer angemeldet ist und wo sich seine Dateien befinden, handelt es sich bei den Standardordnern pro Benutzer um spezielle Ordner, die durch eine [**CSIDL**](csidl.md)identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="0e34b-130">Because it is inconvenient to determine which user is logged in and where their files are located, the standard per-user folders are special folders and are identified by a [**CSIDL**](csidl.md).</span></span> <span data-ttu-id="0e34b-131">Die CSIDL für den Ordner Programme pro Benutzer lautet z. B. CSIDL \_ PROGRAMS.</span><span class="sxs-lookup"><span data-stu-id="0e34b-131">For instance, the CSIDL for the per-user Program Files folder is CSIDL\_PROGRAMS.</span></span> <span data-ttu-id="0e34b-132">Wenn Ihre Anwendung [**SHGetFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation) oder [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) mit einer der CSIDLs pro Benutzer aufruft, gibt die Funktion den Zeiger auf eine Elementbezeichnerliste (PIDL) oder einen Pfad zurück, der dem derzeit angemeldeten Benutzer entspricht.</span><span class="sxs-lookup"><span data-stu-id="0e34b-132">If your application calls [**SHGetFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation) or [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) with one of the per-user CSIDLs, the function returns the pointer to an item identifier list (PIDL) or path appropriate to the currently logged-in user.</span></span> <span data-ttu-id="0e34b-133">Wenn Ihre Anwendung den Pfad oder die PIDL des Profilordners abrufen muss, lautet die CSIDL **CSIDL \_ PROFILE.**</span><span class="sxs-lookup"><span data-stu-id="0e34b-133">If your application needs to retrieve the path or PIDL of the profile folder, its CSIDL is **CSIDL\_PROFILE**.</span></span>

## <a name="my-documents-and-my-pictures-folders"></a><span data-ttu-id="0e34b-134">Ordner "Eigene Dokumente" und "Meine Bilder"</span><span class="sxs-lookup"><span data-stu-id="0e34b-134">My Documents and My Pictures Folders</span></span>

<span data-ttu-id="0e34b-135">Eines der Standardsymbole auf dem Desktop ist **Eigene Dokumente**.</span><span class="sxs-lookup"><span data-stu-id="0e34b-135">One of the standard icons found on the desktop is **My Documents**.</span></span> <span data-ttu-id="0e34b-136">Wenn Sie diesen Ordner öffnen, enthält er die Dokumentdateien des aktuellen Benutzers.</span><span class="sxs-lookup"><span data-stu-id="0e34b-136">When you open this folder, it contains the current user's document files.</span></span> <span data-ttu-id="0e34b-137">Die Desktopinstanz von Eigene Dokumente ist ein virtueller Ordner – ein Alias für den Dateisystemspeicherort, der zum physischen Speichern der Benutzerdokumente verwendet wird – direkt unterhalb des Desktops in der Namespacehierarchie.</span><span class="sxs-lookup"><span data-stu-id="0e34b-137">The desktop instance of My Documents is a virtual folder—an alias to the file system location used to physically store the user's documents—located immediately below the desktop in the namespace hierarchy.</span></span>

<span data-ttu-id="0e34b-138">Der Zweck der Ordner "Eigene Dokumente" und "Meine Bilder" besteht darin, Benutzern einen einfachen und sicheren Zugriff auf ihre Dokument- und Bilddateien auf einem System mit mehreren Benutzern zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="0e34b-138">The purpose of the My Documents and My Pictures folders is to provide a straightforward and secure way for users to access their document and picture files on a system that might have multiple users.</span></span> <span data-ttu-id="0e34b-139">Jedem Benutzer werden separate Dateisystemordner für seine Dateien zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="0e34b-139">Each user is assigned separate file system folders for his or her files.</span></span> <span data-ttu-id="0e34b-140">Der Speicherort des Ordners "documents" eines Benutzers im Dateisystem ist beispielsweise in etwa wie folgt: C: \\ Dokumente und Einstellungen \\ *Benutzername* \\ Eigene Dokumente.</span><span class="sxs-lookup"><span data-stu-id="0e34b-140">For example, the location of a user's documents folder in the file system is typically something like C:\\Documents and Settings\\*username*\\My Documents.</span></span> <span data-ttu-id="0e34b-141">Es ist nicht erforderlich, dass Benutzer etwas über den physischen Speicherort ihrer Dateisystemordner wissen.</span><span class="sxs-lookup"><span data-stu-id="0e34b-141">There is no need for users to know anything about the physical location of their file system folders.</span></span> <span data-ttu-id="0e34b-142">Sie greifen einfach über das symbol Eigene Dokumente auf ihre Dateien zu.</span><span class="sxs-lookup"><span data-stu-id="0e34b-142">They simply access their files through the My Documents icon.</span></span>

> [!Note]  
> <span data-ttu-id="0e34b-143">Eigene Dokumente ermöglicht es einem Benutzer, auf seine eigenen Dateien zuzugreifen, jedoch nicht auf die Dateien eines anderen Benutzers.</span><span class="sxs-lookup"><span data-stu-id="0e34b-143">My Documents allows a user to access his or her own files but not those of any other user.</span></span> <span data-ttu-id="0e34b-144">Wenn mehrere Personen denselben Computer verwenden, kann ein Administrator Benutzer aus dem Teil des Dateisystems sperren, in dem die eigentlichen Dateien gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="0e34b-144">If multiple individuals use the same computer, an administrator can lock users out of the part of the file system where the actual files are stored.</span></span> <span data-ttu-id="0e34b-145">Benutzer können daher über den Ordner Eigene Dokumente an ihren eigenen Dokumenten arbeiten, aber nicht an Dokumenten, die anderen Benutzern gehören.</span><span class="sxs-lookup"><span data-stu-id="0e34b-145">Users will thus be able to work on their own documents through the My Documents folder but not on documents that belong to any other users.</span></span>

 

<span data-ttu-id="0e34b-146">Es ist in der Regel nicht erforderlich, dass eine Anwendung weiß, welcher Benutzer angemeldet ist oder wo sich der ordner Eigene Dokumente des Benutzers im Dateisystem befindet.</span><span class="sxs-lookup"><span data-stu-id="0e34b-146">There is usually no need for an application to know which user is logged in or where in the file system that user's My Documents folder is located.</span></span> <span data-ttu-id="0e34b-147">Stattdessen kann Ihre Anwendung die PIDL des Eigene Dokumente Desktopsymbols abrufen, indem sie die [**IShellFolder::P arseDisplayName-Methode**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname) des Desktops aufruft.</span><span class="sxs-lookup"><span data-stu-id="0e34b-147">Instead, your application can retrieve the PIDL of the My Documents desktop icon by calling the desktop's [**IShellFolder::ParseDisplayName**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname) method.</span></span> <span data-ttu-id="0e34b-148">Der Analysename zum Identifizieren des Eigene Dokumente Ordners ist kein Dateipfad, sondern ::{450d8fba-ad25-11d0-98a8-0800361b1103}.</span><span class="sxs-lookup"><span data-stu-id="0e34b-148">The parsing name used to identify the My Documents folder is not a file path but rather ::{450d8fba-ad25-11d0-98a8-0800361b1103}.</span></span> <span data-ttu-id="0e34b-149">Der Ausdruck in Klammern ist die Textform der Eigene Dokumente GUID.</span><span class="sxs-lookup"><span data-stu-id="0e34b-149">The bracketed expression is the text form of the My Documents GUID.</span></span> <span data-ttu-id="0e34b-150">Um beispielsweise die PIDL von Eigene Dokumente abzurufen, sollte Ihre Anwendung diesen Aufruf von **IShellFolder::P arseDisplayName** verwenden.</span><span class="sxs-lookup"><span data-stu-id="0e34b-150">For example, to retrieve the PIDL of My Documents, your application should use this call to **IShellFolder::ParseDisplayName**.</span></span>


```C++
hr = psfDeskTop->ParseDisplayName(NULL, 
                                  NULL, 
                                  L"::{450d8fba-ad25-11d0-98a8-0800361b1103}", 
                                  &chEaten, 
                                  &pidlDocFiles, 
                                  NULL);
```



<span data-ttu-id="0e34b-151">Sobald Ihre Anwendung über die Eigene Dokumente PIDL verfügt, kann sie den Ordner genauso verarbeiten wie einen normalen Dateisystemordner– Aufzählen von Elementen, Analysieren, Binden und Ausführen anderer gültiger Ordnervorgänge.</span><span class="sxs-lookup"><span data-stu-id="0e34b-151">Once your application has the My Documents PIDL, it can handle the folder just as it would a normal file system folder—enumerating items, parsing, binding, and performing any other valid folder operations.</span></span> <span data-ttu-id="0e34b-152">Die Shell ordnet Änderungen in Eigene Dokumente oder ihren Unterordnern automatisch den entsprechenden Dateisystemordnern zu.</span><span class="sxs-lookup"><span data-stu-id="0e34b-152">The Shell automatically maps changes in My Documents or its subfolders to the appropriate file system folders.</span></span>

<span data-ttu-id="0e34b-153">Wenn Ihre Anwendung Zugriff auf den eigentlichen Dateisystemordner benötigt, der die Dokumente des aktuellen Benutzers enthält, übergeben Sie CSIDL \_ PERSONAL an [**SHGetFolderLocation.**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation)</span><span class="sxs-lookup"><span data-stu-id="0e34b-153">If your application needs access to the actual file system folder that contains the current user's documents, pass CSIDL\_PERSONAL to [**SHGetFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation).</span></span> <span data-ttu-id="0e34b-154">Die Funktion gibt die PIDL des Dateisystemordners zurück, der im ordner Eigene Dokumente des aktuellen Benutzers angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="0e34b-154">The function returns the PIDL of the file system folder that is displayed in the current user's My Documents folder.</span></span>

## <a name="connected-files"></a><span data-ttu-id="0e34b-155">Verbundene Dateien</span><span class="sxs-lookup"><span data-stu-id="0e34b-155">Connected Files</span></span>

<span data-ttu-id="0e34b-156">HTML-Dokumente verfügen häufig über eine Reihe von zugeordneten Grafikdateien, eine Stylesheetdatei, mehrere Microsoft JScript-Dateien (kompatibel mit ECMA 262-Sprachspezifikationen) usw.</span><span class="sxs-lookup"><span data-stu-id="0e34b-156">HTML documents often have a number of associated graphics files, a style sheet file, several Microsoft JScript (compatible with ECMA 262 language specification ) files, and so on.</span></span> <span data-ttu-id="0e34b-157">Wenn Sie das primäre HTML-Dokument verschieben oder kopieren, möchten Sie in der Regel auch die zugehörigen Dateien verschieben oder kopieren, um Breaking Links zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="0e34b-157">When you move or copy the primary HTML document, you also usually want to move or copy its associated files to avoid breaking links.</span></span> <span data-ttu-id="0e34b-158">Leider gab es bisher keine einfache Möglichkeit, zu bestimmen, welche Dateien mit einem bestimmten HTML-Dokument verknüpft sind, außer durch Die Analyse ihrer Inhalte.</span><span class="sxs-lookup"><span data-stu-id="0e34b-158">Unfortunately, there has been no easy way until now to determine which files are related to any given HTML document other than by analyzing their contents.</span></span> <span data-ttu-id="0e34b-159">Um dieses Problem zu beheben, bietet Windows 2000 eine einfache Möglichkeit, ein primäres HTML-Dokument mit der zugehörigen Dateigruppe zu *verbinden.*</span><span class="sxs-lookup"><span data-stu-id="0e34b-159">To alleviate this problem, Windows 2000 provides a simple way to *connect* a primary HTML document to its group of associated files.</span></span> <span data-ttu-id="0e34b-160">Wenn die Dateiverbindung aktiviert ist, werden beim Verschieben oder Kopieren des Dokuments alle verbundenen Dateien mit dem Dokument verknüpft.</span><span class="sxs-lookup"><span data-stu-id="0e34b-160">If file connection is enabled, when the document is moved or copied all its connected files go with it.</span></span>

<span data-ttu-id="0e34b-161">Um eine Gruppe verbundener Dateien zu erstellen, muss das primäre Dokument über eine .htm oder .html Dateinamenerweiterung verfügen.</span><span class="sxs-lookup"><span data-stu-id="0e34b-161">To create a group of connected files, the primary document must have an .htm or .html file name extension.</span></span> <span data-ttu-id="0e34b-162">Erstellen Sie einen Unterordner des übergeordneten Ordners des primären Dokuments.</span><span class="sxs-lookup"><span data-stu-id="0e34b-162">Create a subfolder of the primary document's parent folder.</span></span> <span data-ttu-id="0e34b-163">Der Name des Unterordners muss der Name des primären Dokuments sein, abzüglich der .htm oder .html Erweiterung, gefolgt von einer der unten aufgeführten Erweiterungen.</span><span class="sxs-lookup"><span data-stu-id="0e34b-163">The subfolder's name must be the name of the primary document, minus the .htm or .html extension, followed by one of the extensions listed below.</span></span> <span data-ttu-id="0e34b-164">Die am häufigsten verwendeten Erweiterungen sind ".files" oder \_ "files".</span><span class="sxs-lookup"><span data-stu-id="0e34b-164">The most commonly used extensions are ".files" or "\_files".</span></span> <span data-ttu-id="0e34b-165">Wenn das primäre Dokument beispielsweise MyDoc.htm genannt wird, definiert der Unterordner mit dem Namen "MyDoc-Dateien" \_ den Unterordner als Container für die verbundenen Dateien des Dokuments.</span><span class="sxs-lookup"><span data-stu-id="0e34b-165">For instance, if the primary document is named MyDoc.htm, naming the subfolder "MyDoc\_files" defines the subfolder as the container for the document's connected files.</span></span> <span data-ttu-id="0e34b-166">Wenn das primäre Dokument verschoben oder kopiert wird, werden der Unterordner und seine Dateien ebenfalls verschoben oder kopiert.</span><span class="sxs-lookup"><span data-stu-id="0e34b-166">If the primary document is moved or copied, the subfolder and its files are moved or copied as well.</span></span>

<span data-ttu-id="0e34b-167">Für einige Sprachen ist es möglich, eine lokalisierte Entsprechung von \_ "files" zu verwenden, um einen Unterordner für verbundene Dateien zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0e34b-167">For some languages, it is possible to use a localized equivalent of "\_files" to create a subfolder for connected files.</span></span> <span data-ttu-id="0e34b-168">In der folgenden Tabelle sind die gültigen Zeichenfolgen aufgeführt, die an einen Dokumentnamen angefügt werden können, um einen verbundenen Dateiunterordner zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0e34b-168">The following table lists the valid strings that can be appended to a document name to create a connected files subfolder.</span></span> <span data-ttu-id="0e34b-169">Beachten Sie, dass einige dieser Zeichenfolgen als erstes Zeichen "-" anstelle von \_ "" oder "." aufweisen.</span><span class="sxs-lookup"><span data-stu-id="0e34b-169">Note that some of these strings have '-' as their first character rather than '\_' or '.'.</span></span>



:::row:::
   :::column span="":::
      <span data-ttu-id="0e34b-170">\_"archivos"</span><span class="sxs-lookup"><span data-stu-id="0e34b-170">"\_archivos"</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="0e34b-171">\_"arquivos"</span><span class="sxs-lookup"><span data-stu-id="0e34b-171">"\_arquivos"</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="0e34b-172">\_"bestanden"</span><span class="sxs-lookup"><span data-stu-id="0e34b-172">"\_bestanden"</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="0e34b-173">\_"bylos"</span><span class="sxs-lookup"><span data-stu-id="0e34b-173">"\_bylos"</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="0e34b-174">"-Dateien"</span><span class="sxs-lookup"><span data-stu-id="0e34b-174">"-Dateien"</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="0e34b-175">\_"datoteke"</span><span class="sxs-lookup"><span data-stu-id="0e34b-175">"\_datoteke"</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="0e34b-176">\_"dosyalar"</span><span class="sxs-lookup"><span data-stu-id="0e34b-176">"\_dosyalar"</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="0e34b-177">\_"elemei"</span><span class="sxs-lookup"><span data-stu-id="0e34b-177">"\_elemei"</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="0e34b-178">\_"failid"</span><span class="sxs-lookup"><span data-stu-id="0e34b-178">"\_failid"</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="0e34b-179">\_"fails" (Fehler)</span><span class="sxs-lookup"><span data-stu-id="0e34b-179">"\_fails"</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="0e34b-180">" \_ fajlovi"</span><span class="sxs-lookup"><span data-stu-id="0e34b-180">"\_fajlovi"</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="0e34b-181">\_"fichafs"</span><span class="sxs-lookup"><span data-stu-id="0e34b-181">"\_ficheiros"</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="0e34b-182">\_"fichiers"</span><span class="sxs-lookup"><span data-stu-id="0e34b-182">"\_fichiers"</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="0e34b-183">"-filer"</span><span class="sxs-lookup"><span data-stu-id="0e34b-183">"-filer"</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="0e34b-184">".files"</span><span class="sxs-lookup"><span data-stu-id="0e34b-184">".files"</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="0e34b-185">\_"files"</span><span class="sxs-lookup"><span data-stu-id="0e34b-185">"\_files"</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="0e34b-186">\_"file"</span><span class="sxs-lookup"><span data-stu-id="0e34b-186">"\_file"</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="0e34b-187">\_"fitxers"</span><span class="sxs-lookup"><span data-stu-id="0e34b-187">"\_fitxers"</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="0e34b-188">\_"fitxatezweigk"</span><span class="sxs-lookup"><span data-stu-id="0e34b-188">"\_fitxategiak"</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="0e34b-189">\_"pliki"</span><span class="sxs-lookup"><span data-stu-id="0e34b-189">"\_pliki"</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="0e34b-190">\_"soubory"</span><span class="sxs-lookup"><span data-stu-id="0e34b-190">"\_soubory"</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="0e34b-191">" \_ tiedostot"</span><span class="sxs-lookup"><span data-stu-id="0e34b-191">"\_tiedostot"</span></span>
   :::column-end:::
   :::column span="":::
   :::column-end:::
   :::column span="":::
   :::column-end:::
:::row-end:::



 

> [!Note]  
> <span data-ttu-id="0e34b-192">Bei diesem Feature wird die Groß-/Kleinschreibung der Erweiterung beachtet.</span><span class="sxs-lookup"><span data-stu-id="0e34b-192">This feature is sensitive to the case of the extension.</span></span> <span data-ttu-id="0e34b-193">Beispielsweise wird für das oben angegebene Beispiel ein Unterordner mit dem Namen "MyDoc \_ Files" nicht mit MyDoc.htm verbunden.</span><span class="sxs-lookup"><span data-stu-id="0e34b-193">For instance, for the example given above, a subfolder named "MyDoc\_Files" will not be connected to MyDoc.htm.</span></span>

 

<span data-ttu-id="0e34b-194">Ob die Dateiverbindung aktiviert oder deaktiviert ist, wird durch den **REG \_ DWORD-Wert** NoFileFolderConnection des folgenden Registrierungsschlüssels gesteuert.</span><span class="sxs-lookup"><span data-stu-id="0e34b-194">Whether file connection is enabled or disabled is controlled by a **REG\_DWORD** value, NoFileFolderConnection, of the following registry key.</span></span>

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
```

<span data-ttu-id="0e34b-195">Dieser Wert ist normalerweise nicht definiert, und die Dateiverbindung ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="0e34b-195">This value normally is not defined, and file connection is enabled.</span></span> <span data-ttu-id="0e34b-196">Bei Bedarf können Sie die Dateiverbindung deaktivieren, indem Sie diesen Wert zum Schlüssel hinzufügen und auf 1 festlegen.</span><span class="sxs-lookup"><span data-stu-id="0e34b-196">If necessary, you can disable file connection by adding this value to the key and setting it to 1.</span></span> <span data-ttu-id="0e34b-197">Um die Dateiverbindung erneut zu aktivieren, legen Sie NoFileFolderConnection auf 0 (null) fest.</span><span class="sxs-lookup"><span data-stu-id="0e34b-197">To enable file connection again, set NoFileFolderConnection to zero.</span></span>

> [!Note]  
> <span data-ttu-id="0e34b-198">Die Dateiverbindung sollte normalerweise aktiviert werden, da andere Anwendungen davon abhängig sein können.</span><span class="sxs-lookup"><span data-stu-id="0e34b-198">File connection should normally be enabled because other applications might depend on it.</span></span> <span data-ttu-id="0e34b-199">Deaktivieren Sie die Dateiverbindung nur, wenn dies unbedingt erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="0e34b-199">Disable file connection only if absolutely necessary.</span></span>

 

## <a name="moving-copying-renaming-and-deleting-files"></a><span data-ttu-id="0e34b-200">Verschieben, Kopieren, Umbenennen und Löschen von Dateien</span><span class="sxs-lookup"><span data-stu-id="0e34b-200">Moving, Copying, Renaming, and Deleting Files</span></span>

<span data-ttu-id="0e34b-201">Der Namespace ist nicht statisch, und Anwendungen müssen das Dateisystem häufig verwalten, indem sie einen der folgenden Vorgänge ausführen.</span><span class="sxs-lookup"><span data-stu-id="0e34b-201">The namespace is not static, and applications commonly need to manage the file system by performing one of the following operations.</span></span>

-   <span data-ttu-id="0e34b-202">Kopieren eines Objekts in einen anderen Ordner.</span><span class="sxs-lookup"><span data-stu-id="0e34b-202">Copying an object to another folder.</span></span>
-   <span data-ttu-id="0e34b-203">Verschieben eines Objekts in einen anderen Ordner.</span><span class="sxs-lookup"><span data-stu-id="0e34b-203">Moving an object to another folder.</span></span>
-   <span data-ttu-id="0e34b-204">Löschen eines Objekts.</span><span class="sxs-lookup"><span data-stu-id="0e34b-204">Deleting an object.</span></span>
-   <span data-ttu-id="0e34b-205">Umbenennen eines Objekts.</span><span class="sxs-lookup"><span data-stu-id="0e34b-205">Renaming an object.</span></span>

<span data-ttu-id="0e34b-206">Diese Vorgänge werden alle mit [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa)ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0e34b-206">These operations are all performed with [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa).</span></span> <span data-ttu-id="0e34b-207">Diese Funktion verwendet eine oder mehrere Quelldateien und erzeugt entsprechende Zieldateien.</span><span class="sxs-lookup"><span data-stu-id="0e34b-207">This function takes one or more source files and produces corresponding destination files.</span></span> <span data-ttu-id="0e34b-208">Im Fall des Löschvorgangs versucht das System, die gelöschten Dateien in den Papierkorb zu speichern.</span><span class="sxs-lookup"><span data-stu-id="0e34b-208">In the case of the delete operation, the system attempts to put the deleted files into the Recycle Bin.</span></span>

<span data-ttu-id="0e34b-209">It is also possible to move files using the [drag-and-drop](dragdrop.md) functionality.</span><span class="sxs-lookup"><span data-stu-id="0e34b-209">It is also possible to move files using the [drag-and-drop](dragdrop.md) functionality.</span></span>

<span data-ttu-id="0e34b-210">Um die Funktion zu verwenden, müssen Sie die Member einer [**SHFILEOPSTRUCT-Struktur**](/windows/desktop/api/Shellapi/ns-shellapi-shfileopstructa) ausfüllen und an [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa)übergeben.</span><span class="sxs-lookup"><span data-stu-id="0e34b-210">To use the function, you must fill in the members of an [**SHFILEOPSTRUCT**](/windows/desktop/api/Shellapi/ns-shellapi-shfileopstructa) structure and pass it to [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa).</span></span> <span data-ttu-id="0e34b-211">Die Schlüsselmember der -Struktur sind **pFrom** und **pTo.**</span><span class="sxs-lookup"><span data-stu-id="0e34b-211">The key members of the structure are **pFrom** and **pTo**.</span></span>

<span data-ttu-id="0e34b-212">Der **pFrom-Member** ist eine mit **doppelt NULL** endende Zeichenfolge, die einen oder mehrere Quelldateinamen enthält.</span><span class="sxs-lookup"><span data-stu-id="0e34b-212">The **pFrom** member is a double **null**-terminated string that contains one or more source file names.</span></span> <span data-ttu-id="0e34b-213">Diese Namen können entweder vollqualifizierte Pfade oder STANDARD-DOS-Platzhalter wie \* \* sein.</span><span class="sxs-lookup"><span data-stu-id="0e34b-213">These names can be either fully qualified paths or standard DOS wildcards such as \*.\*.</span></span> <span data-ttu-id="0e34b-214">Obwohl dieser Member als null-terminierte Zeichenfolge deklariert ist, wird er als Puffer für mehrere Dateinamen verwendet.</span><span class="sxs-lookup"><span data-stu-id="0e34b-214">Although this member is declared as a **null**-terminated string, it is used as a buffer to hold multiple file names.</span></span> <span data-ttu-id="0e34b-215">Jeder Dateiname muss durch das übliche einzelne **NULL-Zeichen** beendet werden.</span><span class="sxs-lookup"><span data-stu-id="0e34b-215">Each file name must be terminated by the usual single **NULL** character.</span></span> <span data-ttu-id="0e34b-216">Ein zusätzliches **NULL-Zeichen** muss am Ende des endgültigen Namens angefügt werden, um das Ende von **pFrom** anzugeben.</span><span class="sxs-lookup"><span data-stu-id="0e34b-216">An additional **NULL** character must be appended to the end of the final name to indicate the end of **pFrom**.</span></span>

<span data-ttu-id="0e34b-217">Der **pTo-Member** ist eine doppelt **null-terminierte** Zeichenfolge, ähnlich wie **pFrom.**</span><span class="sxs-lookup"><span data-stu-id="0e34b-217">The **pTo** member is a double **null**-terminated string, much like **pFrom**.</span></span> <span data-ttu-id="0e34b-218">Der **pTo-Member** enthält die Namen von einem oder mehreren vollqualifizierten Zielnamen.</span><span class="sxs-lookup"><span data-stu-id="0e34b-218">The **pTo** member contains the names of one or more fully qualified destination names.</span></span> <span data-ttu-id="0e34b-219">Sie werden auf die gleiche Weise wie für **pFrom** in **pTo** gepackt.</span><span class="sxs-lookup"><span data-stu-id="0e34b-219">They are packed into **pTo** in the same way as they are for **pFrom**.</span></span> <span data-ttu-id="0e34b-220">Wenn **pTo** mehrere Namen enthält, müssen Sie auch das **FOF \_ MULTIDESTFILES-Flag** im **fFlags-Member** festlegen.</span><span class="sxs-lookup"><span data-stu-id="0e34b-220">If **pTo** contains multiple names, you must also set the **FOF\_MULTIDESTFILES** flag in the **fFlags** member.</span></span> <span data-ttu-id="0e34b-221">Die Verwendung von **pTo** hängt vom Vorgang ab, wie hier beschrieben.</span><span class="sxs-lookup"><span data-stu-id="0e34b-221">The usage of **pTo** depends on the operation as described here.</span></span>

-   <span data-ttu-id="0e34b-222">Wenn alle Dateien für Kopier- und Verschiebevorgänge in ein einzelnes Verzeichnis verschoben werden, enthält **pTo** den vollqualifizierten Verzeichnisnamen.</span><span class="sxs-lookup"><span data-stu-id="0e34b-222">For copy and move operations, if all the files are going to a single directory, **pTo** contains the fully qualified directory name.</span></span> <span data-ttu-id="0e34b-223">Wenn die Dateien an andere Ziele gelangen, kann **pTo** auch ein vollqualifiziertes Verzeichnis oder einen Dateinamen für jede Quelldatei enthalten.</span><span class="sxs-lookup"><span data-stu-id="0e34b-223">If the files are going to different destinations, **pTo** can also contain one fully qualified directory or file name for each source file.</span></span> <span data-ttu-id="0e34b-224">Wenn kein Verzeichnis vorhanden ist, erstellt das System es.</span><span class="sxs-lookup"><span data-stu-id="0e34b-224">If a directory does not exist, the system creates it.</span></span>
-   <span data-ttu-id="0e34b-225">Für Umbenennungsvorgänge enthält **pTo** einen vollqualifizierten Pfad für jede Quelldatei in **pFrom.**</span><span class="sxs-lookup"><span data-stu-id="0e34b-225">For rename operations, **pTo** contains one fully qualified path for each source file in **pFrom**.</span></span>
-   <span data-ttu-id="0e34b-226">Für Löschvorgänge wird **pTo** nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="0e34b-226">For delete operations, **pTo** is not used.</span></span>

### <a name="notifying-the-shell"></a><span data-ttu-id="0e34b-227">Benachrichtigen der Shell</span><span class="sxs-lookup"><span data-stu-id="0e34b-227">Notifying the Shell</span></span>

<span data-ttu-id="0e34b-228">Benachrichtigen Sie die Shell über die Änderung, nachdem [**Sie SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa) zum Verschieben, Kopieren, Umbenennen oder Löschen von Dateien verwendet oder eine andere Aktion ausgeführt haben, die sich auf den Namespace auswirkt.</span><span class="sxs-lookup"><span data-stu-id="0e34b-228">Notify the Shell of the change after using [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa) to move, copy, rename, or delete files, or after taking any other action that affects the namespace.</span></span> <span data-ttu-id="0e34b-229">Aktionen, die von Benachrichtigungen begleitet werden sollten, umfassen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="0e34b-229">Actions that should be accompanied by notification include the following:</span></span>

-   <span data-ttu-id="0e34b-230">Hinzufügen oder Löschen von Dateien oder Ordnern.</span><span class="sxs-lookup"><span data-stu-id="0e34b-230">Adding or deleting files or folders.</span></span>
-   <span data-ttu-id="0e34b-231">Verschieben, Kopieren oder Umbenennen von Dateien oder Ordnern.</span><span class="sxs-lookup"><span data-stu-id="0e34b-231">Moving, copying, or renaming files or folders.</span></span>
-   <span data-ttu-id="0e34b-232">Ändern einer Dateizuordnung.</span><span class="sxs-lookup"><span data-stu-id="0e34b-232">Changing a file association.</span></span>
-   <span data-ttu-id="0e34b-233">Ändern von Dateiattributen.</span><span class="sxs-lookup"><span data-stu-id="0e34b-233">Changing file attributes.</span></span>
-   <span data-ttu-id="0e34b-234">Hinzufügen oder Entfernen von Laufwerken oder Speichermedien.</span><span class="sxs-lookup"><span data-stu-id="0e34b-234">Adding or removing drives or storage media.</span></span>
-   <span data-ttu-id="0e34b-235">Erstellen oder Deaktivieren eines freigegebenen Ordners.</span><span class="sxs-lookup"><span data-stu-id="0e34b-235">Creating or disabling a shared folder.</span></span>
-   <span data-ttu-id="0e34b-236">Ändern der Systemimageliste.</span><span class="sxs-lookup"><span data-stu-id="0e34b-236">Changing the system image list.</span></span>

<span data-ttu-id="0e34b-237">Eine Anwendung benachrichtigt die Shell, indem [**sie SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) mit den Details der Änderungen aufruft.</span><span class="sxs-lookup"><span data-stu-id="0e34b-237">An application notifies the Shell by calling [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) with the details of what has changed.</span></span> <span data-ttu-id="0e34b-238">Die Shell kann dann ihr Image des Namespace aktualisieren, um den neuen Zustand genau widerzuspiegeln.</span><span class="sxs-lookup"><span data-stu-id="0e34b-238">The Shell can then update its image of the namespace to accurately reflect its new state.</span></span>

## <a name="simple-example-of-managing-files-with-shfileoperation"></a><span data-ttu-id="0e34b-239">Einfaches Beispiel für die Verwaltung von Dateien mit SHFileOperation</span><span class="sxs-lookup"><span data-stu-id="0e34b-239">Simple Example of Managing Files with SHFileOperation</span></span>

<span data-ttu-id="0e34b-240">Die folgende Beispielkonsolenanwendung veranschaulicht die Verwendung von [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa) zum Kopieren von Dateien aus einem Verzeichnis in ein anderes.</span><span class="sxs-lookup"><span data-stu-id="0e34b-240">The following sample console application illustrates the use of [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa) to copy files from one directory to another.</span></span> <span data-ttu-id="0e34b-241">Die Quell- und Zielverzeichnisse C: \\ My \_ Docs und C: \\ My Docs2 sind der Einfachheit \_ halber hart in die Anwendung codiert.</span><span class="sxs-lookup"><span data-stu-id="0e34b-241">The source and destination directories, C:\\My\_Docs and C:\\My\_Docs2, are hard-coded into the application for simplicity.</span></span>


```C++
#include <shlobj.h>
#include <shlwapi.h>
#include <strsafe.h>

int main(void)
{
    IShellFolder *psfDeskTop = NULL;
    IShellFolder *psfDocFiles = NULL;
    LPITEMIDLIST pidlDocFiles = NULL;
    LPITEMIDLIST pidlItems = NULL;
    IEnumIDList *ppenum = NULL;
    SHFILEOPSTRUCT sfo;
    STRRET strDispName;
    TCHAR szParseName[MAX_PATH];
    TCHAR szSourceFiles[256];
    int i;
    int iBufPos = 0;
    ULONG chEaten;
    ULONG celtFetched;
    size_t ParseNameSize = 0;
    HRESULT hr;
    

    szSourceFiles[0] = '\0';
    hr = SHGetDesktopFolder(&psfDeskTop);

    hr = psfDeskTop->ParseDisplayName(NULL, NULL, L"c:\\My_Docs", 
         &chEaten, &pidlDocFiles, NULL);
    hr = psfDeskTop->BindToObject(pidlDocFiles, NULL, IID_IShellFolder, 
         (LPVOID *) &psfDocFiles);
    hr = psfDeskTop->Release();

    hr = psfDocFiles->EnumObjects(NULL,SHCONTF_FOLDERS | SHCONTF_NONFOLDERS, 
         &ppenum);

    while( (hr = ppenum->Next(1,&pidlItems, &celtFetched)) == S_OK 
       && (celtFetched) == 1)
    {
        psfDocFiles->GetDisplayNameOf(pidlItems, SHGDN_FORPARSING, 
            &strDispName);
        StrRetToBuf(&strDispName, pidlItems, szParseName, MAX_PATH);
        
        hr = StringCchLength(szParseName, MAX_PATH, &ParseNameSize);
        
        if (SUCCEEDED(hr))
        {
            for(i=0; i<=ParseNameSize; i++)
            {
                szSourceFiles[iBufPos++] = szParseName[i];
            }
            CoTaskMemFree(pidlItems);
        }
    }
    ppenum->Release();
    
    szSourceFiles[iBufPos] = '\0';

    sfo.hwnd = NULL;
    sfo.wFunc = FO_COPY;
    sfo.pFrom = szSourceFiles;
    sfo.pTo = "c:\\My_Docs2\0";
    sfo.fFlags = FOF_SILENT | FOF_NOCONFIRMATION | FOF_NOCONFIRMMKDIR;

    hr = SHFileOperation(&sfo);
    
    SHChangeNotify(SHCNE_UPDATEDIR, SHCNF_PATH, (LPCVOID) "c:\\My_Docs2", 0);

    CoTaskMemFree(pidlDocFiles);
    psfDocFiles->Release();

    return 0;
}
```



<span data-ttu-id="0e34b-242">Die Anwendung ruft zunächst einen Zeiger auf die [**IShellFolder-Schnittstelle**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) des Desktops ab.</span><span class="sxs-lookup"><span data-stu-id="0e34b-242">The application first retrieves a pointer to the desktop's [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) interface.</span></span> <span data-ttu-id="0e34b-243">Anschließend wird die PIDL des Quellverzeichnisses abgerufen, indem der vollqualifizierte Pfad an [**IShellFolder::P arseDisplayName**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname)übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="0e34b-243">It then retrieves the source directory's PIDL by passing its fully qualified path to [**IShellFolder::ParseDisplayName**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname).</span></span> <span data-ttu-id="0e34b-244">Beachten Sie, dass **IShellFolder::P arseDisplayName** erfordert, dass der Pfad des Verzeichnisses eine Unicode-Zeichenfolge ist.</span><span class="sxs-lookup"><span data-stu-id="0e34b-244">Note that **IShellFolder::ParseDisplayName** requires the directory's path to be a Unicode string.</span></span> <span data-ttu-id="0e34b-245">Die Anwendung bindet dann an das Quellverzeichnis und verwendet die **IShellFolder-Schnittstelle,** um die [**IEnumIDList-Schnittstelle**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist) eines Enumeratorobjekts abzurufen.</span><span class="sxs-lookup"><span data-stu-id="0e34b-245">The application then binds to the source directory and uses its **IShellFolder** interface to retrieve an enumerator object's [**IEnumIDList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist) interface.</span></span>

<span data-ttu-id="0e34b-246">Da jede Datei im Quellverzeichnis aufzählt, wird [**IShellFolder::GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) verwendet, um ihren Namen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="0e34b-246">As each file in the source directory is enumerated, [**IShellFolder::GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) is used to retrieve its name.</span></span> <span data-ttu-id="0e34b-247">Das Flag SWSDN \_ FORPARSING ist festgelegt, wodurch **IShellFolder::GetDisplayNameOf** den vollqualifizierten Pfad der Datei zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="0e34b-247">The SHGDN\_FORPARSING flag is set, which causes **IShellFolder::GetDisplayNameOf** to return the file's fully qualified path.</span></span> <span data-ttu-id="0e34b-248">Die Dateipfade, einschließlich der abschließenden **NULL-Zeichen,** werden zu einem einzelnen Array verkettet, *szSourceFiles.*</span><span class="sxs-lookup"><span data-stu-id="0e34b-248">The file paths, including the terminating **NULL** characters, are concatenated into a single array, *szSourceFiles*.</span></span> <span data-ttu-id="0e34b-249">Ein zweites **NULL-Zeichen** wird an den endgültigen Pfad angefügt, um das Array ordnungsgemäß zu beenden.</span><span class="sxs-lookup"><span data-stu-id="0e34b-249">A second **NULL** character is appended to the final path to terminate the array properly.</span></span>

<span data-ttu-id="0e34b-250">Nach Abschluss der Enumeration weist die Anwendung einer [**SHFILEOPSTRUCT-Struktur**](/windows/desktop/api/Shellapi/ns-shellapi-shfileopstructa) Werte zu.</span><span class="sxs-lookup"><span data-stu-id="0e34b-250">Once the enumeration is complete, the application assigns values to an [**SHFILEOPSTRUCT**](/windows/desktop/api/Shellapi/ns-shellapi-shfileopstructa) structure.</span></span> <span data-ttu-id="0e34b-251">Beachten Sie, dass das Array, das **pTo** zum Angeben des Ziels zugewiesen ist, ebenfalls mit einem doppelten **NULL-Wert** beendet werden muss.</span><span class="sxs-lookup"><span data-stu-id="0e34b-251">Note that the array assigned to **pTo** to specify the destination must also be terminated by a double **NULL**.</span></span> <span data-ttu-id="0e34b-252">In diesem Fall ist sie einfach in der Zeichenfolge enthalten, die **pTo** zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="0e34b-252">In this case, it is simply included in the string that is assigned to **pTo**.</span></span> <span data-ttu-id="0e34b-253">Da es sich um eine Konsolenanwendung handelt, werden die Flags FOF \_ SILENT, FOF \_ NOCONFIRMATION und FOF \_ NOCONFIRMMKDIR so festgelegt, dass alle angezeigten Dialogfelder unterdrückt werden.</span><span class="sxs-lookup"><span data-stu-id="0e34b-253">Because this is a console application, the FOF\_SILENT, FOF\_NOCONFIRMATION, and FOF\_NOCONFIRMMKDIR flags are set to suppress any dialog boxes that might appear.</span></span> <span data-ttu-id="0e34b-254">Nachdem [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa) zurückgegeben wurde, wird [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) aufgerufen, um die Shell über die Änderung zu benachrichtigen.</span><span class="sxs-lookup"><span data-stu-id="0e34b-254">After [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa) returns, [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) is called to notify the Shell of the change.</span></span> <span data-ttu-id="0e34b-255">Anschließend führt die Anwendung die übliche Bereinigung aus und gibt zurück.</span><span class="sxs-lookup"><span data-stu-id="0e34b-255">Then the application performs the usual cleanup and returns.</span></span>

## <a name="adding-files-to-the-shells-list-of-recent-documents"></a><span data-ttu-id="0e34b-256">Hinzufügen von Dateien zur Shellliste zuletzt verwendeter Dokumente</span><span class="sxs-lookup"><span data-stu-id="0e34b-256">Adding Files to the Shell's List of Recent Documents</span></span>

<span data-ttu-id="0e34b-257">Die Shell verwaltet eine Liste der zuletzt hinzugefügten oder geänderten Dokumente für jeden Benutzer.</span><span class="sxs-lookup"><span data-stu-id="0e34b-257">The Shell maintains a list of recently added or modified documents for each user.</span></span> <span data-ttu-id="0e34b-258">Der Benutzer kann eine Liste mit Links zu diesen Dateien anzeigen, indem er im Startmenü auf Dokumente klickt.</span><span class="sxs-lookup"><span data-stu-id="0e34b-258">The user can display a list of links to these files by clicking Documents on the Start menu.</span></span> <span data-ttu-id="0e34b-259">Wie bei Eigene Dokumente verfügt jeder Benutzer über ein Dateisystemverzeichnis, in dem die tatsächlichen Links gespeichert werden können.</span><span class="sxs-lookup"><span data-stu-id="0e34b-259">As with My Documents, each user has a file system directory to hold the actual links.</span></span> <span data-ttu-id="0e34b-260">Um die PIDL des Zuletzt verwendeten Verzeichnisses des aktuellen Benutzers abzurufen, kann Ihre Anwendung [**SHGetFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation) mit CSIDL \_ RECENT aufrufen oder [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) aufrufen, um seinen Pfad abzurufen.</span><span class="sxs-lookup"><span data-stu-id="0e34b-260">To retrieve the PIDL of the current user's Recent directory, your application can call [**SHGetFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation) with CSIDL\_RECENT, or call [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) to retrieve its path.</span></span>

<span data-ttu-id="0e34b-261">Ihre Anwendung kann den Inhalt des Ordners Zuletzt verwendet mithilfe der weiter oben in diesem Dokument beschriebenen Verfahren aufzählen.</span><span class="sxs-lookup"><span data-stu-id="0e34b-261">Your application can enumerate the contents of the Recent folder using the techniques discussed earlier in this document.</span></span> <span data-ttu-id="0e34b-262">Eine Anwendung sollte den Inhalt des Ordners jedoch nicht so ändern, als wäre es ein normaler Dateisystemordner.</span><span class="sxs-lookup"><span data-stu-id="0e34b-262">However, an application should not modify the contents of the folder as if it were a normal file system folder.</span></span> <span data-ttu-id="0e34b-263">In diesem Falle wird die Shell-Liste der letzten Dokumente nicht ordnungsgemäß aktualisiert, und die Änderungen werden nicht im Startmenü widergespiegelt.</span><span class="sxs-lookup"><span data-stu-id="0e34b-263">If it does so, the Shell's list of recent documents will not be updated properly, and the changes will not be reflected in the Start menu.</span></span> <span data-ttu-id="0e34b-264">Um stattdessen einen Dokumentlink zum Ordner Zuletzt verwendet eines Benutzers hinzuzufügen, kann Ihre Anwendung [**SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="0e34b-264">Instead, to add a document link to a user's Recent folder, your application can call [**SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs).</span></span> <span data-ttu-id="0e34b-265">Die Shell fügt einen Link zum entsprechenden Dateisystemordner hinzu und aktualisiert die Liste der zuletzt verwendeten Dokumente und die Startmenü.</span><span class="sxs-lookup"><span data-stu-id="0e34b-265">The Shell will add a link to the appropriate file system folder, as well as updating its list of recent documents and the Start menu.</span></span> <span data-ttu-id="0e34b-266">Sie können diese Funktion auch verwenden, um den Ordner zu löschen.</span><span class="sxs-lookup"><span data-stu-id="0e34b-266">You can also use this function to clear the folder.</span></span>

 

 
