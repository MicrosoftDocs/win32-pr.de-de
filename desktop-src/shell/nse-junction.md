---
description: Der Stamm einer Namespace Erweiterung wird normalerweise von Windows Explorer als Ordner in den Struktur-und Ordner Sichten angezeigt.
title: Angeben des Speicher Orts der Namespace Erweiterung
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2c1fdd5d-b359-4d5c-a20e-0622f3a1cb1d
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 7617c7361c5f2ae76331c5f1b59eb845f6806395
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866160"
---
# <a name="specifying-a-namespace-extensions-location"></a><span data-ttu-id="0e301-103">Angeben des Speicher Orts der Namespace Erweiterung</span><span class="sxs-lookup"><span data-stu-id="0e301-103">Specifying a Namespace Extension's Location</span></span>

<span data-ttu-id="0e301-104">Der Stamm einer Namespace Erweiterung wird normalerweise von Windows Explorer als Ordner in den Struktur-und Ordner Sichten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0e301-104">The root of a namespace extension is normally displayed by Windows Explorer as a folder in both tree and folder views.</span></span> <span data-ttu-id="0e301-105">Damit Windows Explorer die Dateien und Unterordner der Erweiterung anzeigt, müssen Sie angeben, wo sich der Stamm Ordner in der Shellnamespace Hierarchie befindet.</span><span class="sxs-lookup"><span data-stu-id="0e301-105">For Windows Explorer to display your extension's files and subfolders, you must specify where the root folder is located in the Shell namespace hierarchy.</span></span> <span data-ttu-id="0e301-106">Dieser Speicherort wird als Verknüpfungs *Punkt* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="0e301-106">This location is referred to as a *junction point*.</span></span>

-   [<span data-ttu-id="0e301-107">Verwenden von virtuellen Ordnern als Verknüpfungs Punkte</span><span class="sxs-lookup"><span data-stu-id="0e301-107">Using Virtual Folders as Junction Points</span></span>](#using-virtual-folders-as-junction-points)
-   [<span data-ttu-id="0e301-108">Verwenden von Datei System Ordnern als Verknüpfungs Punkte</span><span class="sxs-lookup"><span data-stu-id="0e301-108">Using File System Folders as Junction Points</span></span>](#using-file-system-folders-as-junction-points)
-   [<span data-ttu-id="0e301-109">Öffnen einer Ansicht einer Namespace Erweiterung</span><span class="sxs-lookup"><span data-stu-id="0e301-109">Opening a View of a Namespace Extension</span></span>](#opening-a-view-of-a-namespace-extension)

## <a name="using-virtual-folders-as-junction-points"></a><span data-ttu-id="0e301-110">Verwenden von virtuellen Ordnern als Verknüpfungs Punkte</span><span class="sxs-lookup"><span data-stu-id="0e301-110">Using Virtual Folders as Junction Points</span></span>

<span data-ttu-id="0e301-111">Die einfachste Möglichkeit, den Verknüpfungs Punkt einer Erweiterung zu definieren, besteht darin, den Stamm Ordner zu einem Unterordner eines virtuellen System Ordners zu machen.</span><span class="sxs-lookup"><span data-stu-id="0e301-111">The simplest way to define an extension's junction point is to make the root folder a subfolder of a system virtual folder.</span></span> <span data-ttu-id="0e301-112">Diese Art von Verbindungspunkt wird als virtueller Verknüpfungs *Punkt* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="0e301-112">This type of junction point is referred to as a *virtual junction point*.</span></span> <span data-ttu-id="0e301-113">Die Ordner " **Desktop** " und " **Arbeitsplatz** " sind die typischen Orte für virtuelle Verknüpfungs Punkte, Sie können aber auch einen virtuellen Verknüpfungs Punkt auf einem Remote Computer oder unter den Ordnern " **meine Netzwerk Orte**", " **Internet Explorer**" und " **Systemsteuerung** " definieren.</span><span class="sxs-lookup"><span data-stu-id="0e301-113">The **Desktop** and **My Computer** folders are the typical locations for virtual junction points, but you can also define a virtual junction point on a remote computer or under the **My Network Places**, **Internet Explorer**, and **Control Panel** folders.</span></span>

<span data-ttu-id="0e301-114">Wenn Sie einen virtuellen Verknüpfungs Punkt definieren möchten, erstellen Sie einen Unterschlüssel des Schlüssels, der den entsprechenden virtuellen Ordner darstellt, und benennen Sie ihn mit der Zeichenfolge Form der Klassen-ID (CLSID) ihrer Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="0e301-114">To define a virtual junction point, create a subkey of the key that represents the appropriate virtual folder and name it with the string form of your extension's class identifier (CLSID).</span></span> <span data-ttu-id="0e301-115">Die registrierte CLSID würde wie folgt aussehen.</span><span class="sxs-lookup"><span data-stu-id="0e301-115">The registered CLSID would appear as follows.</span></span>

```
HKEY_LOCAL_MACHINE or HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  Virtual Folder Name
                     NameSpace
                        {Extension CLSID}
                           (Default) = Junction Point Name
```

<span data-ttu-id="0e301-116">Der *Name des virtuellen Ordners* ist einer der Unterschlüssel in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="0e301-116">*Virtual Folder Name* is one of the subkeys in the following table.</span></span>



| <span data-ttu-id="0e301-117">Standort</span><span class="sxs-lookup"><span data-stu-id="0e301-117">Location</span></span>          | <span data-ttu-id="0e301-118">Name des virtuellen Ordners</span><span class="sxs-lookup"><span data-stu-id="0e301-118">Virtual Folder Name</span></span>                        |
|-------------------|--------------------------------------------|
| <span data-ttu-id="0e301-119">Systemsteuerung</span><span class="sxs-lookup"><span data-stu-id="0e301-119">Control Panel</span></span>     | <span data-ttu-id="0e301-120">**Steuerung**</span><span class="sxs-lookup"><span data-stu-id="0e301-120">**ControlPanel**</span></span>                           |
| <span data-ttu-id="0e301-121">Desktop</span><span class="sxs-lookup"><span data-stu-id="0e301-121">Desktop</span></span>           | <span data-ttu-id="0e301-122">**Desktop**</span><span class="sxs-lookup"><span data-stu-id="0e301-122">**Desktop**</span></span>                                |
| <span data-ttu-id="0e301-123">Gesamtes Netzwerk</span><span class="sxs-lookup"><span data-stu-id="0e301-123">Entire Network</span></span>    | <span data-ttu-id="0e301-124">**Network Neighborhood** \\ **Entirenetwork**</span><span class="sxs-lookup"><span data-stu-id="0e301-124">**NetworkNeighborhood**\\**EntireNetwork**</span></span> |
| <span data-ttu-id="0e301-125">Arbeitsplatz</span><span class="sxs-lookup"><span data-stu-id="0e301-125">My Computer</span></span>       | <span data-ttu-id="0e301-126">**MyComputer**</span><span class="sxs-lookup"><span data-stu-id="0e301-126">**MyComputer**</span></span>                             |
| <span data-ttu-id="0e301-127">Meine Netzwerk Orte</span><span class="sxs-lookup"><span data-stu-id="0e301-127">My Network Places</span></span> | <span data-ttu-id="0e301-128">**Network Neighborhood**</span><span class="sxs-lookup"><span data-stu-id="0e301-128">**NetworkNeighborhood**</span></span>                    |
| <span data-ttu-id="0e301-129">Remote Computer</span><span class="sxs-lookup"><span data-stu-id="0e301-129">Remote Computer</span></span>   | <span data-ttu-id="0e301-130">**Remote Computer**</span><span class="sxs-lookup"><span data-stu-id="0e301-130">**RemoteComputer**</span></span>                         |
| <span data-ttu-id="0e301-131">Benutzer Dateien</span><span class="sxs-lookup"><span data-stu-id="0e301-131">Users Files</span></span>       | <span data-ttu-id="0e301-132">**Usersfiles**</span><span class="sxs-lookup"><span data-stu-id="0e301-132">**UsersFiles**</span></span>                             |



 

<span data-ttu-id="0e301-133">Remote Erweiterungen müssen mit [**iremotecomputer**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iremotecomputer)initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="0e301-133">Remote extensions must be initialized with [**IRemoteComputer**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iremotecomputer).</span></span>

## <a name="using-file-system-folders-as-junction-points"></a><span data-ttu-id="0e301-134">Verwenden von Datei System Ordnern als Verknüpfungs Punkte</span><span class="sxs-lookup"><span data-stu-id="0e301-134">Using File System Folders as Junction Points</span></span>

<span data-ttu-id="0e301-135">Es gibt zwei Möglichkeiten, Dateisystem Ordner als Verknüpfungs Punkte zu definieren.</span><span class="sxs-lookup"><span data-stu-id="0e301-135">There are two ways to define file system folders as junction points.</span></span> <span data-ttu-id="0e301-136">Der einfachste Ansatz besteht darin, einen Ordner am entsprechenden Speicherort zu erstellen und einen Zeitraum an den Namen des Ordners anzufügen, gefolgt von der Zeichen folgen Form der CLSID der Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="0e301-136">The simplest approach is to create a folder in the appropriate location and append a period to the folder's name, followed by the string form of the CLSID of your extension.</span></span> <span data-ttu-id="0e301-137">Nur der Ordnername wird in Windows-Explorer angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0e301-137">Only the folder name will be visible in Windows Explorer.</span></span> <span data-ttu-id="0e301-138">Im folgenden Beispiel wird ein Verknüpfungs Punkt mit dem anzeigen Amen "MyFolder" erstellt.</span><span class="sxs-lookup"><span data-stu-id="0e301-138">The following example creates a junction point with a display name of MyFolder.</span></span>


```
MyFolder.{Extension CLSID}
```



<span data-ttu-id="0e301-139">Alternativ können Sie einen Ordner mit konventionell Namen als Verknüpfungs Punkt definieren, indem Sie folgende Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="0e301-139">Alternatively, you can define a conventionally named folder as a junction point by:</span></span>

-   <span data-ttu-id="0e301-140">Festlegen, dass der Ordner schreibgeschützt ist.</span><span class="sxs-lookup"><span data-stu-id="0e301-140">Making the folder read-only.</span></span>
-   <span data-ttu-id="0e301-141">Erstellen Sie den Ordner durch Aufrufen von [**pathmakesystemfolder**](/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakesystemfoldera)zu einem Systemordner.</span><span class="sxs-lookup"><span data-stu-id="0e301-141">Making the folder a system folder by calling [**PathMakeSystemFolder**](/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakesystemfoldera).</span></span>
-   <span data-ttu-id="0e301-142">Platzieren einer ausgeblendeten Desktop.ini Datei in dem Ordner, der die CLSID der Erweiterung enthält.</span><span class="sxs-lookup"><span data-stu-id="0e301-142">Placing a hidden Desktop.ini file in the folder that includes the extension's CLSID.</span></span>

<span data-ttu-id="0e301-143">Desktop.ini ist eine Standard Textdatei, die einem beliebigen Ordner hinzugefügt werden kann, um bestimmte Aspekte des Ordner Verhaltens anzupassen.</span><span class="sxs-lookup"><span data-stu-id="0e301-143">Desktop.ini is a standard text file that can be added to any folder to customize certain aspects of the folder's behavior.</span></span> <span data-ttu-id="0e301-144">Eine allgemeine Erläuterung zur Verwendung dieser Datei finden Sie unter Anpassen von [Ordnern mit Desktop.ini](how-to-customize-folders-with-desktop-ini.md).</span><span class="sxs-lookup"><span data-stu-id="0e301-144">For a general discussion of how to use this file, see [How to Customize Folders with Desktop.ini](how-to-customize-folders-with-desktop-ini.md).</span></span> <span data-ttu-id="0e301-145">Zum Definieren eines Ordners als Verknüpfungs Punkt wird der \[ . Der shellclassinfo \] -Abschnitt des Desktop.ini muss die CLSID der Erweiterung wie folgt enthalten:</span><span class="sxs-lookup"><span data-stu-id="0e301-145">To define a folder as a junction point, the \[.ShellClassInfo\] section of Desktop.ini must contain the extension's CLSID as follows:</span></span>


```
[.ShellClassInfo]
CLSID={Extension CLSID}
```



## <a name="opening-a-view-of-a-namespace-extension"></a><span data-ttu-id="0e301-146">Öffnen einer Ansicht einer Namespace Erweiterung</span><span class="sxs-lookup"><span data-stu-id="0e301-146">Opening a View of a Namespace Extension</span></span>

<span data-ttu-id="0e301-147">Wenn ein Benutzer einen Verknüpfungs Punkt durchsucht, erstellt Windows-Explorer automatisch eine Ansicht des Stamm Ordners.</span><span class="sxs-lookup"><span data-stu-id="0e301-147">When a user browses into a junction point, Windows Explorer automatically creates a view of the root folder.</span></span> <span data-ttu-id="0e301-148">Sie können auch eine Ansicht erstellen, indem Sie Explorer.exe explizit mit der CLSID der Erweiterung als Argument starten.</span><span class="sxs-lookup"><span data-stu-id="0e301-148">You can also create a view by explicitly launching Explorer.exe with the extension's CLSID as an argument.</span></span> <span data-ttu-id="0e301-149">Beispielsweise können Sie diese Vorgehensweise verwenden, um eine Ansicht einer Erweiterung über ein Kontextmenü oder eine Verknüpfung zu starten.</span><span class="sxs-lookup"><span data-stu-id="0e301-149">You can, for instance, use this approach to launch a view of an extension from a shortcut menu or shortcut.</span></span> <span data-ttu-id="0e301-150">Wenn Sie z. b. eine Ansicht von MyExtension starten möchten, die eine Strukturansicht enthält, können Sie die folgende Befehls Zeichenfolge verwenden.</span><span class="sxs-lookup"><span data-stu-id="0e301-150">For example, to launch a view of MyExtension that includes a tree view, you can use the following command string.</span></span>


```
%SystemRoot%\Explorer.exe /e,::{MyExtension CLSID}
```



<span data-ttu-id="0e301-151">Eine Alternative Befehls Zeichenfolge kann verwendet werden, um eine Ansicht eines Objekts innerhalb der Erweiterung zu starten.</span><span class="sxs-lookup"><span data-stu-id="0e301-151">An alternative command string can be used to launch a view of an object within the extension.</span></span> <span data-ttu-id="0e301-152">Diese Funktion wäre beispielsweise nützlich für eine Erweiterung, die eine Ordneransicht verwendet, damit Benutzer den Inhalt einer Reihe von komprimierten Dateien anzeigen können.</span><span class="sxs-lookup"><span data-stu-id="0e301-152">This feature would be useful, for instance, for an extension that uses a folder view to allow users to view the contents of one of a number of compressed files.</span></span>


```
%SystemRoot%\Explorer.exe /e,::{MyExtension CLSID},objectname
```



<span data-ttu-id="0e301-153">Der *objectName* -Parameter ist der Name des Objekts, das angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0e301-153">The *objectname* parameter is the name of the object that is to be viewed.</span></span> <span data-ttu-id="0e301-154">Windows-Explorer konvertiert den Namen in die entsprechende PIDL und übergibt die PIDL an die [**ipersistfolder:: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder-initialize) -Methode des neuen Ordner Objekts.</span><span class="sxs-lookup"><span data-stu-id="0e301-154">Windows Explorer converts the name to its corresponding PIDL and passes the PIDL to the new folder object's [**IPersistFolder::Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder-initialize) method.</span></span>

> [!Note]  
> <span data-ttu-id="0e301-155">Der CLSID-Zeichenfolge muss ein paar von Doppelpunkten vorangestellt werden (::) Andernfalls schlägt der Befehl fehl.</span><span class="sxs-lookup"><span data-stu-id="0e301-155">The CLSID string must be preceded by a pair of colons (::) or the command will fail.</span></span> <span data-ttu-id="0e301-156">Der Schrägstrich-e (/e)-Flag, der in den beiden zuvor gezeigten Beispiel Befehlszeilen verwendet wird, weist Windows-Explorer an, eine Strukturansicht anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="0e301-156">The slash-e (/e) flag used in the two sample command lines shown previously instructs Windows Explorer to display a tree view.</span></span> <span data-ttu-id="0e301-157">Das Flag muss von den beiden Doppelpunkten durch ein Komma getrennt werden.</span><span class="sxs-lookup"><span data-stu-id="0e301-157">The flag must be separated from the two colons by a comma.</span></span> <span data-ttu-id="0e301-158">Wenn Sie keine Strukturansicht verwenden möchten, lassen Sie das/e-Flag und das Komma aus.</span><span class="sxs-lookup"><span data-stu-id="0e301-158">If you do not want a tree view, omit the /e flag and the comma.</span></span>

 

 

 



