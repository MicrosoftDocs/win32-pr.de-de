---
description: Anpassen des Erscheinungs Bilds und Verhaltens eines einzelnen Ordners mit Desktop.ini.
ms.assetid: 0361b7da-bfb3-4880-b982-85d2fe419805
title: Vorgehensweise beim Anpassen von Ordnern mit Desktop.ini
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eaac3e6a96257e63b5e4210da0aa6e6e1db77eaf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104560738"
---
# <a name="how-to-customize-folders-with-desktopini"></a><span data-ttu-id="d3a08-103">Vorgehensweise beim Anpassen von Ordnern mit Desktop.ini</span><span class="sxs-lookup"><span data-stu-id="d3a08-103">How to Customize Folders with Desktop.ini</span></span>

<span data-ttu-id="d3a08-104">Dateisystem Ordner werden häufig mit einem Standard Symbol und einem Satz von Eigenschaften angezeigt, die angeben, ob der Ordner freigegeben ist.</span><span class="sxs-lookup"><span data-stu-id="d3a08-104">File system folders are commonly displayed with a standard icon and set of properties, which specify, for instance, whether the folder is shared.</span></span> <span data-ttu-id="d3a08-105">Sie können die Darstellung und das Verhalten eines einzelnen Ordners anpassen, indem Sie eine Desktop.ini-Datei für diesen Ordner erstellen.</span><span class="sxs-lookup"><span data-stu-id="d3a08-105">You can customize the appearance and behavior of an individual folder by creating a Desktop.ini file for that folder.</span></span>

## <a name="instructions"></a><span data-ttu-id="d3a08-106">Instructions</span><span class="sxs-lookup"><span data-stu-id="d3a08-106">Instructions</span></span>

### <a name="using-desktopini-files"></a><span data-ttu-id="d3a08-107">Verwenden von Desktop.ini Dateien</span><span class="sxs-lookup"><span data-stu-id="d3a08-107">Using Desktop.ini Files</span></span>

<span data-ttu-id="d3a08-108">Ordner werden normalerweise mit dem Symbol "Standardordner" angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d3a08-108">Folders are normally displayed with the standard folder icon.</span></span> <span data-ttu-id="d3a08-109">Die Desktop.ini Datei wird häufig verwendet, um einem Ordner ein benutzerdefiniertes Symbol oder Miniaturbild zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="d3a08-109">A common use of the Desktop.ini file is to assign a custom icon or thumbnail image to a folder.</span></span> <span data-ttu-id="d3a08-110">Sie können auch Desktop.ini verwenden, um einen *Infotipp* zu erstellen, der Informationen zum Ordner anzeigt und einige Aspekte des Ordners des Ordners steuert, z. b. das angeben lokalisierter Namen für den Ordner oder die Elemente im Ordner.</span><span class="sxs-lookup"><span data-stu-id="d3a08-110">You can also use Desktop.ini to create an *infotip* that displays information about the folder and controls some aspects of the folder's behavior, such as specifying localized names for the folder or items in the folder.</span></span>

<span data-ttu-id="d3a08-111">**Verwenden Sie das folgende Verfahren, um den Stil eines Ordners mit Desktop.ini anzupassen:**</span><span class="sxs-lookup"><span data-stu-id="d3a08-111">**Use the following procedure to customize a folder's style with Desktop.ini:**</span></span>

1.  <span data-ttu-id="d3a08-112">Verwenden Sie [**pathmakesystemfolder**](/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakesystemfoldera) , um den Ordner zu einem Systemordner zu machen.</span><span class="sxs-lookup"><span data-stu-id="d3a08-112">Use [**PathMakeSystemFolder**](/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakesystemfoldera) to make the folder a system folder.</span></span> <span data-ttu-id="d3a08-113">Dadurch wird das schreibgeschützte Bit für den Ordner festgelegt, um anzugeben, dass das für Desktop.ini reservierte spezielle Verhalten aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="d3a08-113">This sets the read-only bit on the folder to indicate that the special behavior reserved for Desktop.ini should be enabled.</span></span> <span data-ttu-id="d3a08-114">Sie können einen Ordner auch über die Befehlszeile in einem Ordner erstellen, indem Sie **atzb + s** *FolderName* verwenden.</span><span class="sxs-lookup"><span data-stu-id="d3a08-114">You can also make a folder a system folder from the command line by using **attrib +s** *FolderName*.</span></span>
2.  <span data-ttu-id="d3a08-115">Erstellen Sie eine Desktop.ini-Datei für den Ordner.</span><span class="sxs-lookup"><span data-stu-id="d3a08-115">Create a Desktop.ini file for the folder.</span></span> <span data-ttu-id="d3a08-116">Sie sollten Sie als *ausgeblendet* und *System* markieren, um sicherzustellen, dass Sie für normale Benutzer ausgeblendet ist.</span><span class="sxs-lookup"><span data-stu-id="d3a08-116">You should mark it as *hidden* and *system* to ensure that it is hidden from normal users.</span></span>
3.  <span data-ttu-id="d3a08-117">Stellen Sie sicher, dass die von Ihnen erstellte Desktop.ini Datei im Unicode-Format vorliegt.</span><span class="sxs-lookup"><span data-stu-id="d3a08-117">Make sure the Desktop.ini file that you create is in the Unicode format.</span></span> <span data-ttu-id="d3a08-118">Dies ist erforderlich, um die lokalisierten Zeichen folgen zu speichern, die Benutzern angezeigt werden können.</span><span class="sxs-lookup"><span data-stu-id="d3a08-118">This is necessary to store the localized strings that can be displayed to users.</span></span>

### <a name="creating-a-desktopini-file"></a><span data-ttu-id="d3a08-119">Erstellen einer Desktop.ini Datei</span><span class="sxs-lookup"><span data-stu-id="d3a08-119">Creating a Desktop.ini File</span></span>

<span data-ttu-id="d3a08-120">Die Desktop.ini-Datei ist eine Textdatei, mit der Sie angeben können, wie ein Dateisystem Ordner angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="d3a08-120">The Desktop.ini file is a text file that allows you to specify how a file system folder is viewed.</span></span> <span data-ttu-id="d3a08-121">Die \[ . Der Abschnitt "shellclassinfo" \] ermöglicht das Anpassen der Ordneransicht durch Zuweisen von Werten zu mehreren Einträgen:</span><span class="sxs-lookup"><span data-stu-id="d3a08-121">The \[.ShellClassInfo\] section, allows you to customize the folder's view by assigning values to several entries:</span></span>

|                   |                                                                                                                                                                                                                                                                                                                                                                                |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3a08-122">**Eingabe**</span><span class="sxs-lookup"><span data-stu-id="d3a08-122">**Entry**</span></span>         | <span data-ttu-id="d3a08-123">**Wert**</span><span class="sxs-lookup"><span data-stu-id="d3a08-123">**Value**</span></span>                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="d3a08-124">**Confirmfileop**</span><span class="sxs-lookup"><span data-stu-id="d3a08-124">**ConfirmFileOp**</span></span> | <span data-ttu-id="d3a08-125">Legen Sie diesen Eintrag auf 0 fest, um beim Löschen oder Verschieben des Ordners die Warnung "Sie können einen System Ordner löschen" zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="d3a08-125">Set this entry to 0 to avoid a "You Are Deleting a System Folder" warning when deleting or moving the folder.</span></span>                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="d3a08-126">**Nosharing**</span><span class="sxs-lookup"><span data-stu-id="d3a08-126">**NoSharing**</span></span>     | <span data-ttu-id="d3a08-127">Wird unter Windows Vista oder höher nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d3a08-127">Not supported under Windows Vista or later.</span></span> <span data-ttu-id="d3a08-128">Legen Sie diesen Eintrag auf 1 fest, um zu verhindern, dass der Ordner freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d3a08-128">Set this entry to 1 to prevent the folder from being shared.</span></span>                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="d3a08-129">**IconFile**</span><span class="sxs-lookup"><span data-stu-id="d3a08-129">**IconFile**</span></span>      | <span data-ttu-id="d3a08-130">Wenn Sie ein benutzerdefiniertes Symbol für den Ordner angeben möchten, legen Sie diesen Eintrag auf den Dateinamen des Symbols fest.</span><span class="sxs-lookup"><span data-stu-id="d3a08-130">If you want to specify a custom icon for the folder, set this entry to the icon's file name.</span></span> <span data-ttu-id="d3a08-131">Die Dateinamenerweiterung. ico wird bevorzugt, aber es ist auch möglich, BMP-Dateien, exe-und dll-Dateien anzugeben, die Symbole enthalten.</span><span class="sxs-lookup"><span data-stu-id="d3a08-131">The .ico file name extension is preferred, but it is also possible to specify .bmp files, or .exe and .dll files that contain icons.</span></span> <span data-ttu-id="d3a08-132">Wenn Sie einen relativen Pfad verwenden, steht das Symbol den Personen zur Verfügung, die den Ordner über das Netzwerk anzeigen.</span><span class="sxs-lookup"><span data-stu-id="d3a08-132">If you use a relative path, the icon is available to people who view the folder over the network.</span></span> <span data-ttu-id="d3a08-133">Sie müssen auch den Eintrag **IconIndex** festlegen.</span><span class="sxs-lookup"><span data-stu-id="d3a08-133">You must also set the **IconIndex** entry.</span></span> |
| <span data-ttu-id="d3a08-134">**IconIndex**</span><span class="sxs-lookup"><span data-stu-id="d3a08-134">**IconIndex**</span></span>     | <span data-ttu-id="d3a08-135">Legen Sie diesen Eintrag fest, um den Index für ein benutzerdefiniertes Symbol anzugeben.</span><span class="sxs-lookup"><span data-stu-id="d3a08-135">Set this entry to specify the index for a custom icon.</span></span> <span data-ttu-id="d3a08-136">Wenn die **IconFile** zugewiesene Datei nur ein einzelnes Symbol enthält, legen Sie **IconIndex** auf 0 fest.</span><span class="sxs-lookup"><span data-stu-id="d3a08-136">If the file assigned to **IconFile** only contains a single icon, set **IconIndex** to 0.</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="d3a08-137">**InfoTip**</span><span class="sxs-lookup"><span data-stu-id="d3a08-137">**InfoTip**</span></span>       | <span data-ttu-id="d3a08-138">Legen Sie diesen Eintrag auf eine Informationstext Zeichenfolge fest.</span><span class="sxs-lookup"><span data-stu-id="d3a08-138">Set this entry to an informational text string.</span></span> <span data-ttu-id="d3a08-139">Sie wird als InfoTipp angezeigt, wenn der Cursor auf den Ordner zeigt.</span><span class="sxs-lookup"><span data-stu-id="d3a08-139">It is displayed as an infotip when the cursor hovers over the folder.</span></span> <span data-ttu-id="d3a08-140">Wenn der Benutzer auf den Ordner klickt, wird der Informationstext im Informationsblock des Ordners unter den Standardinformationen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d3a08-140">If the user clicks the folder, the information text is displayed in the folder's information block, below the standard information.</span></span>                                                                                                                      |



 

<span data-ttu-id="d3a08-141">Die folgenden Abbildungen sind der Ordner "Music" mit einer benutzerdefinierten Desktop.ini Datei.</span><span class="sxs-lookup"><span data-stu-id="d3a08-141">The following illustrations are of the Music folder with a custom Desktop.ini file.</span></span> <span data-ttu-id="d3a08-142">Jetzt der Ordner:</span><span class="sxs-lookup"><span data-stu-id="d3a08-142">The folder now:</span></span>

-   <span data-ttu-id="d3a08-143">Verfügt über ein benutzerdefiniertes Symbol.</span><span class="sxs-lookup"><span data-stu-id="d3a08-143">Has a custom icon.</span></span>
-   <span data-ttu-id="d3a08-144">Wenn der Ordner verschoben oder gelöscht wird, wird von keine Warnung angezeigt, dass ein System Ordner gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="d3a08-144">Does not display a "You Are Deleting a System Folder" warning if the folder is moved or deleted.</span></span>
-   <span data-ttu-id="d3a08-145">Keine gemeinsame Nutzung möglich.</span><span class="sxs-lookup"><span data-stu-id="d3a08-145">Cannot be shared.</span></span>
-   <span data-ttu-id="d3a08-146">Zeigt Informationstext an, wenn der Cursor auf den Ordner zeigt.</span><span class="sxs-lookup"><span data-stu-id="d3a08-146">Displays informational text when the cursor hovers over the folder.</span></span>

<span data-ttu-id="d3a08-147">Die Ordneroptionen in den folgenden Abbildungen sind so festgelegt, dass ausgeblendete Dateien angezeigt werden, damit Desktop.ini sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="d3a08-147">The folder options in the following illustrations are set to show hidden files so that Desktop.ini is visible.</span></span> <span data-ttu-id="d3a08-148">Der Ordner sieht wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="d3a08-148">The folder looks like this:</span></span>

![Screenshot des Ordners mit benutzerdefiniertem Symbol](images/webview4.jpg)

<span data-ttu-id="d3a08-150">Wenn der Cursor über den Ordner bewegt wird, wird der InfoTipp angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d3a08-150">When the cursor hovers over the folder, the infotip is displayed.</span></span>

![Screenshot des Ordners mit einem InfoTipp](images/webview6.jpg)

<span data-ttu-id="d3a08-152">Das benutzerdefinierte Symbol ersetzt das Ordnersymbol, wo der Ordnername angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="d3a08-152">The custom icon replaces the folder icon everywhere the folder name appears.</span></span>

![Screenshot des benutzerdefinierten Symbols zum Ersetzen des Ordner Symbols](images/webview5.jpg)

<span data-ttu-id="d3a08-154">Die folgende desktop.ini Datei wurde verwendet, um den Musik Ordner anzupassen, wie in den vorherigen Abbildungen gezeigt.</span><span class="sxs-lookup"><span data-stu-id="d3a08-154">The following desktop.ini file was used to customize the Music folder, as seen in the preceding illustrations.</span></span>


```
[.ShellClassInfo]
ConfirmFileOp=0
NoSharing=1
IconFile=Folder.ico
IconIndex=0
InfoTip=Some sensible information.
```



 

 



