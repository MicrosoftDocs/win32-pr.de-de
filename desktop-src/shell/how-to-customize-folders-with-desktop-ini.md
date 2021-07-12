---
description: Anpassen der Darstellung und des Verhaltens eines einzelnen Ordners mit Desktop.ini.
ms.assetid: 0361b7da-bfb3-4880-b982-85d2fe419805
title: Anpassen von Ordnern mit Desktop.ini
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a671b169c4b025683cdd220ee3a920b4d592488
ms.sourcegitcommit: 822413efb4a70dd464e5db4d9e8693ef74f8132f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/09/2021
ms.locfileid: "113581748"
---
# <a name="how-to-customize-folders-with-desktopini"></a><span data-ttu-id="9bba0-103">Anpassen von Ordnern mit Desktop.ini</span><span class="sxs-lookup"><span data-stu-id="9bba0-103">How to Customize Folders with Desktop.ini</span></span>

<span data-ttu-id="9bba0-104">Dateisystemordner werden häufig mit einem Standardsymbol und einer Reihe von Eigenschaften angezeigt, die z. B. angeben, ob der Ordner freigegeben ist.</span><span class="sxs-lookup"><span data-stu-id="9bba0-104">File system folders are commonly displayed with a standard icon and set of properties, which specify, for instance, whether the folder is shared.</span></span> <span data-ttu-id="9bba0-105">Sie können die Darstellung und das Verhalten eines einzelnen Ordners anpassen, indem Sie eine Desktop.ini-Datei für diesen Ordner erstellen.</span><span class="sxs-lookup"><span data-stu-id="9bba0-105">You can customize the appearance and behavior of an individual folder by creating a Desktop.ini file for that folder.</span></span>

## <a name="instructions"></a><span data-ttu-id="9bba0-106">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="9bba0-106">Instructions</span></span>

### <a name="using-desktopini-files"></a><span data-ttu-id="9bba0-107">Verwenden von Desktop.ini Dateien</span><span class="sxs-lookup"><span data-stu-id="9bba0-107">Using Desktop.ini Files</span></span>

<span data-ttu-id="9bba0-108">Ordner werden normalerweise mit dem Standardordnersymbol angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9bba0-108">Folders are normally displayed with the standard folder icon.</span></span> <span data-ttu-id="9bba0-109">Eine häufige Verwendung der Desktop.ini Datei besteht darin, einem Ordner ein benutzerdefiniertes Symbol oder miniaturansichtsbild zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="9bba0-109">A common use of the Desktop.ini file is to assign a custom icon or thumbnail image to a folder.</span></span> <span data-ttu-id="9bba0-110">Sie können auch Desktop.ini verwenden, um eine *Infoinfo* zu erstellen, die Informationen zum Ordner anzeigt und einige Aspekte des Ordnerverhaltens steuert, z. B. die Angabe lokalisierter Namen für den Ordner oder Elemente im Ordner.</span><span class="sxs-lookup"><span data-stu-id="9bba0-110">You can also use Desktop.ini to create an *infotip* that displays information about the folder and controls some aspects of the folder's behavior, such as specifying localized names for the folder or items in the folder.</span></span>

<span data-ttu-id="9bba0-111">**Verwenden Sie das folgende Verfahren, um den Stil eines Ordners mit Desktop.ini anzupassen:**</span><span class="sxs-lookup"><span data-stu-id="9bba0-111">**Use the following procedure to customize a folder's style with Desktop.ini:**</span></span>

1.  <span data-ttu-id="9bba0-112">Verwenden Sie [**PathMakeSystemFolder,**](/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakesystemfoldera) um den Ordner zu einem Systemordner zu machen.</span><span class="sxs-lookup"><span data-stu-id="9bba0-112">Use [**PathMakeSystemFolder**](/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakesystemfoldera) to make the folder a system folder.</span></span> <span data-ttu-id="9bba0-113">Dadurch wird das schreibgeschützte Bit im Ordner festgelegt, um anzugeben, dass das für Desktop.ini reservierte spezielle Verhalten aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="9bba0-113">This sets the read-only bit on the folder to indicate that the special behavior reserved for Desktop.ini should be enabled.</span></span> <span data-ttu-id="9bba0-114">Sie können einen Ordner auch über die Befehlszeile zu einem Systemordner machen, indem Sie **attrib +s** *FolderName verwenden.*</span><span class="sxs-lookup"><span data-stu-id="9bba0-114">You can also make a folder a system folder from the command line by using **attrib +s** *FolderName*.</span></span>
2.  <span data-ttu-id="9bba0-115">Erstellen Sie eine Desktop.ini-Datei für den Ordner.</span><span class="sxs-lookup"><span data-stu-id="9bba0-115">Create a Desktop.ini file for the folder.</span></span> <span data-ttu-id="9bba0-116">Sie sollten es als *ausgeblendet* markieren und *als System,* um sicherzustellen, dass es für normale Benutzer ausgeblendet ist.</span><span class="sxs-lookup"><span data-stu-id="9bba0-116">You should mark it as *hidden* and *system* to ensure that it is hidden from normal users.</span></span>
3.  <span data-ttu-id="9bba0-117">Stellen Sie sicher, dass die von Ihnen erstellte Desktop.ini-Datei im Unicode-Format vorliegt.</span><span class="sxs-lookup"><span data-stu-id="9bba0-117">Make sure the Desktop.ini file that you create is in the Unicode format.</span></span> <span data-ttu-id="9bba0-118">Dies ist erforderlich, um die lokalisierten Zeichenfolgen zu speichern, die Benutzern angezeigt werden können.</span><span class="sxs-lookup"><span data-stu-id="9bba0-118">This is necessary to store the localized strings that can be displayed to users.</span></span>

### <a name="creating-a-desktopini-file"></a><span data-ttu-id="9bba0-119">Erstellen einer Desktop.ini-Datei</span><span class="sxs-lookup"><span data-stu-id="9bba0-119">Creating a Desktop.ini File</span></span>

<span data-ttu-id="9bba0-120">Die Desktop.ini-Datei ist eine Textdatei, mit der Sie angeben können, wie ein Dateisystemordner angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="9bba0-120">The Desktop.ini file is a text file that allows you to specify how a file system folder is viewed.</span></span> <span data-ttu-id="9bba0-121">Der \[ . Im Abschnitt ShellClassInfo \] können Sie die Ansicht des Ordners anpassen, indem Sie mehreren Einträgen Werte zuweisen:</span><span class="sxs-lookup"><span data-stu-id="9bba0-121">The \[.ShellClassInfo\] section, allows you to customize the folder's view by assigning values to several entries:</span></span>

| <span data-ttu-id="9bba0-122">Wert</span><span class="sxs-lookup"><span data-stu-id="9bba0-122">Value</span></span>             | <span data-ttu-id="9bba0-123">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9bba0-123">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9bba0-124">**ConfirmFileOp**</span><span class="sxs-lookup"><span data-stu-id="9bba0-124">**ConfirmFileOp**</span></span> | <span data-ttu-id="9bba0-125">Legen Sie diesen Eintrag auf 0 fest, um die Warnung "Sie löschen einen Systemordner" beim Löschen oder Verschieben des Ordners zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="9bba0-125">Set this entry to 0 to avoid a "You Are Deleting a System Folder" warning when deleting or moving the folder.</span></span>                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="9bba0-126">**NoSharing**</span><span class="sxs-lookup"><span data-stu-id="9bba0-126">**NoSharing**</span></span>     | <span data-ttu-id="9bba0-127">Wird unter Windows Vista oder höher nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9bba0-127">Not supported under Windows Vista or later.</span></span> <span data-ttu-id="9bba0-128">Legen Sie diesen Eintrag auf 1 fest, um zu verhindern, dass der Ordner freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="9bba0-128">Set this entry to 1 to prevent the folder from being shared.</span></span>                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="9bba0-129">**IconFile**</span><span class="sxs-lookup"><span data-stu-id="9bba0-129">**IconFile**</span></span>      | <span data-ttu-id="9bba0-130">Wenn Sie ein benutzerdefiniertes Symbol für den Ordner angeben möchten, legen Sie diesen Eintrag auf den Dateinamen des Symbols fest.</span><span class="sxs-lookup"><span data-stu-id="9bba0-130">If you want to specify a custom icon for the folder, set this entry to the icon's file name.</span></span> <span data-ttu-id="9bba0-131">Die ICO-Dateinamenerweiterung wird bevorzugt, aber es ist auch möglich, .bmp Dateien oder .exe und .dll Dateien anzugeben, die Symbole enthalten.</span><span class="sxs-lookup"><span data-stu-id="9bba0-131">The .ico file name extension is preferred, but it is also possible to specify .bmp files, or .exe and .dll files that contain icons.</span></span> <span data-ttu-id="9bba0-132">Wenn Sie einen relativen Pfad verwenden, ist das Symbol für Personen verfügbar, die den Ordner über das Netzwerk anzeigen.</span><span class="sxs-lookup"><span data-stu-id="9bba0-132">If you use a relative path, the icon is available to people who view the folder over the network.</span></span> <span data-ttu-id="9bba0-133">Sie müssen auch den **Eintrag IconIndex** festlegen.</span><span class="sxs-lookup"><span data-stu-id="9bba0-133">You must also set the **IconIndex** entry.</span></span> |
| <span data-ttu-id="9bba0-134">**IconIndex**</span><span class="sxs-lookup"><span data-stu-id="9bba0-134">**IconIndex**</span></span>     | <span data-ttu-id="9bba0-135">Legen Sie diesen Eintrag fest, um den Index für ein benutzerdefiniertes Symbol anzugeben.</span><span class="sxs-lookup"><span data-stu-id="9bba0-135">Set this entry to specify the index for a custom icon.</span></span> <span data-ttu-id="9bba0-136">Wenn die **Datei,** die IconFile zugewiesen ist, nur ein einzelnes Symbol enthält, legen **Sie IconIndex** auf 0 fest.</span><span class="sxs-lookup"><span data-stu-id="9bba0-136">If the file assigned to **IconFile** only contains a single icon, set **IconIndex** to 0.</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="9bba0-137">**InfoTip**</span><span class="sxs-lookup"><span data-stu-id="9bba0-137">**InfoTip**</span></span>       | <span data-ttu-id="9bba0-138">Legen Sie diesen Eintrag auf eine Informationstextzeichenfolge fest.</span><span class="sxs-lookup"><span data-stu-id="9bba0-138">Set this entry to an informational text string.</span></span> <span data-ttu-id="9bba0-139">Sie wird als Infotip angezeigt, wenn der Cursor auf den Ordner zeigt.</span><span class="sxs-lookup"><span data-stu-id="9bba0-139">It is displayed as an infotip when the cursor hovers over the folder.</span></span> <span data-ttu-id="9bba0-140">Wenn der Benutzer auf den Ordner klickt, wird der Informationstext im Informationsblock des Ordners unterhalb der Standardinformationen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9bba0-140">If the user clicks the folder, the information text is displayed in the folder's information block, below the standard information.</span></span>                                                                                                                      |



 

<span data-ttu-id="9bba0-141">Die folgenden Abbildungen enthalten den ordner Musik mit einer benutzerdefinierten Desktop.ini-Datei.</span><span class="sxs-lookup"><span data-stu-id="9bba0-141">The following illustrations are of the Music folder with a custom Desktop.ini file.</span></span> <span data-ttu-id="9bba0-142">Der Ordner jetzt:</span><span class="sxs-lookup"><span data-stu-id="9bba0-142">The folder now:</span></span>

-   <span data-ttu-id="9bba0-143">Verfügt über ein benutzerdefiniertes Symbol.</span><span class="sxs-lookup"><span data-stu-id="9bba0-143">Has a custom icon.</span></span>
-   <span data-ttu-id="9bba0-144">Die Warnung "Sie löschen einen Systemordner" wird nicht angezeigt, wenn der Ordner verschoben oder gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="9bba0-144">Does not display a "You Are Deleting a System Folder" warning if the folder is moved or deleted.</span></span>
-   <span data-ttu-id="9bba0-145">Keine gemeinsame Nutzung möglich.</span><span class="sxs-lookup"><span data-stu-id="9bba0-145">Cannot be shared.</span></span>
-   <span data-ttu-id="9bba0-146">Zeigt Informationstext an, wenn der Cursor auf den Ordner zeigt.</span><span class="sxs-lookup"><span data-stu-id="9bba0-146">Displays informational text when the cursor hovers over the folder.</span></span>

<span data-ttu-id="9bba0-147">Die Ordneroptionen in den folgenden Abbildungen sind so festgelegt, dass ausgeblendete Dateien angezeigt werden, damit Desktop.ini sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="9bba0-147">The folder options in the following illustrations are set to show hidden files so that Desktop.ini is visible.</span></span> <span data-ttu-id="9bba0-148">Der Ordner sieht wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="9bba0-148">The folder looks like this:</span></span>

![Screenshot des Ordners mit benutzerdefiniertem Symbol](images/webview4.jpg)

<span data-ttu-id="9bba0-150">Wenn der Cursor auf den Ordner zeigt, wird die Infotip angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9bba0-150">When the cursor hovers over the folder, the infotip is displayed.</span></span>

![Screenshot des Ordners mit infotip](images/webview6.jpg)

<span data-ttu-id="9bba0-152">Das benutzerdefinierte Symbol ersetzt das Ordnersymbol überall dort, wo der Ordnername angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="9bba0-152">The custom icon replaces the folder icon everywhere the folder name appears.</span></span>

![Screenshot des benutzerdefinierten Symbols zum Ersetzen des Ordnersymbols](images/webview5.jpg)

<span data-ttu-id="9bba0-154">Die folgende desktop.ini Datei wurde verwendet, um den Ordner Musik anzupassen, wie in den vorherigen Abbildungen dargestellt.</span><span class="sxs-lookup"><span data-stu-id="9bba0-154">The following desktop.ini file was used to customize the Music folder, as seen in the preceding illustrations.</span></span>


```
[.ShellClassInfo]
ConfirmFileOp=0
NoSharing=1
IconFile=Folder.ico
IconIndex=0
InfoTip=Some sensible information.
```



 

 



