---
title: Hinzufügen des contentdistributor-Attributs
description: Hinzufügen des contentdistributor-Attributs
ms.assetid: b4ba5c9b-f28f-4275-bd39-c0ad1080d122
keywords:
- Windows Media Player Online Stores, Hinzufügen des contentdistributor-Attributs
- Online Stores, Hinzufügen des contentdistributor-Attributs
- Typ 1 Online Stores, Hinzufügen des contentdistributor-Attributs
- Typ 2 Online Stores, Hinzufügen des contentdistributor-Attributs
- Windows Media Player Online Stores, contentdistributor-Attribut
- Online Stores, contentdistributor-Attribut
- Typ 1 Online Stores, contentdistributor-Attribut
- Typ 2 Online Stores, contentdistributor-Attribut
- Hinzufügen von contentdistributor-Attributen
- Contentdistributor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1636c002affbcf1235283a22f7eb060c75f24a81
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310091"
---
# <a name="adding-the-contentdistributor-attribute"></a><span data-ttu-id="dd723-113">Hinzufügen des contentdistributor-Attributs</span><span class="sxs-lookup"><span data-stu-id="dd723-113">Adding the ContentDistributor Attribute</span></span>

<span data-ttu-id="dd723-114">Wenn der Benutzer versucht, Online Store-Inhalte wiederzugeben oder den Inhalt auf eine CD oder ein Gerät zu kopieren, ruft Windows Media Player bestimmte Methoden in Ihrem com-Objekt auf.</span><span class="sxs-lookup"><span data-stu-id="dd723-114">When the user attempts to play online store content or to copy the content to a CD or device, Windows Media Player calls certain methods in your COM object.</span></span> <span data-ttu-id="dd723-115">Zu diesem Zweck benötigt der Player eine Möglichkeit, ihre Inhalte von anderen Online Store-Anbietern zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="dd723-115">To do this, the Player needs a way to differentiate your content from that of other online store providers.</span></span> <span data-ttu-id="dd723-116">Indem Sie den Namen Ihres Online Store-Schlüssels als Wert für den **contentdistributor** (einen Alias für das Windows Media Format SDK-Attribut mit dem Namen **WM/contentdistributor**) zu Ihrem Windows Media-basierten Inhalt hinzufügen, stellen Sie sicher, dass der Player den dem Dienst zugeordneten Inhalt identifizieren kann.</span><span class="sxs-lookup"><span data-stu-id="dd723-116">By adding your online store key name as the value for the **ContentDistributor** (which is an alias for the Windows Media Format SDK attribute named **WM/ContentDistributor**) attribute to your Windows Media-based content, you ensure that the Player can identify the content associated with your service.</span></span>

<span data-ttu-id="dd723-117">Durch das Hinzufügen eines Werts für **contentdistributor** wird auch sichergestellt, dass Windows Media Player einen Knoten in der Bibliothek für von Ihnen bereitgestellte Inhalte erstellt.</span><span class="sxs-lookup"><span data-stu-id="dd723-117">Adding a value for **ContentDistributor** also ensures that Windows Media Player will create a node in the library for content you provide.</span></span> <span data-ttu-id="dd723-118">Siehe [Bibliotheks Integration](library-integration.md).</span><span class="sxs-lookup"><span data-stu-id="dd723-118">See [Library Integration](library-integration.md).</span></span>

<span data-ttu-id="dd723-119">Sie können diesen Wert auf zwei Arten angeben:</span><span class="sxs-lookup"><span data-stu-id="dd723-119">You can specify this value two ways:</span></span>

-   <span data-ttu-id="dd723-120">Verwenden Sie das Windows Media Player-Objektmodell.</span><span class="sxs-lookup"><span data-stu-id="dd723-120">Use the Windows Media Player object model.</span></span> <span data-ttu-id="dd723-121">Wenn Sie dies tun, fügt Windows Media Player den von Ihnen angegebenen Wert der Bibliotheks Datenbank hinzu.</span><span class="sxs-lookup"><span data-stu-id="dd723-121">When you do this, Windows Media Player adds the value you specify to the library database.</span></span> <span data-ttu-id="dd723-122">Schließlich schreibt der Spieler auch den Attribut Wert in die digitale Mediendatei.</span><span class="sxs-lookup"><span data-stu-id="dd723-122">Eventually, the Player will also write the attribute value to the digital media file.</span></span>
-   <span data-ttu-id="dd723-123">Verwenden Sie das SDK für den Windows Media-Format, um das **WM/contentdistributor-** Attribut Programm gesteuert hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="dd723-123">Use the Windows Media Format SDK to programmatically add the **WM/ContentDistributor** attribute.</span></span> <span data-ttu-id="dd723-124">Wenn Sie dies tun, liest Windows Media Player den Attribut Wert und fügt ihn der-Datenbank hinzu, wenn die digitale Mediendatei der Bibliothek hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="dd723-124">When you do this, Windows Media Player reads the attribute value and adds it to the database when the digital media file is added to the library.</span></span>

<span data-ttu-id="dd723-125">Wenn Sie das COM-Objekt des Online Stores erstellen, muss der Datei Attribut Wert, den Sie für **contentdistributor** festlegen, und der Wert, der der Konstanten kszcontentdistributorid in yourproject. h zugewiesen ist, exakt übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="dd723-125">When creating your online store COM object, the file attribute value you set for **ContentDistributor** and the value assigned to the constant kszContentDistributorID in YourProject.h must match exactly.</span></span> <span data-ttu-id="dd723-126">Denken Sie daran, dass Sie diesen Konstanten Wert für das COM-Objekt angegeben haben, als Sie das Projekt mit dem Projekt-Assistenten erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="dd723-126">Recall that you specified this constant value for your COM object when you created the project by using the project wizard.</span></span> <span data-ttu-id="dd723-127">Sie können diesen Wert manuell ändern.</span><span class="sxs-lookup"><span data-stu-id="dd723-127">You can change this value manually.</span></span> <span data-ttu-id="dd723-128">Achten Sie einfach darauf, eine Zeichenfolge zu verwenden, die ihren Dienst eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="dd723-128">Just be sure to use a string that uniquely identifies your service.</span></span>

## <a name="using-the-windows-media-player-object-model"></a><span data-ttu-id="dd723-129">Verwenden des Windows Media Player-Objektmodells</span><span class="sxs-lookup"><span data-stu-id="dd723-129">Using the Windows Media Player Object Model</span></span>

<span data-ttu-id="dd723-130">Um einen Wert für **contentdistributor** mithilfe des Windows Media Player-Objektmodells anzugeben, verwenden Sie die [Media. setiteminfo](media-setiteminfo.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="dd723-130">To specify a value for **ContentDistributor** using the Windows Media Player object model, use the [Media.setItemInfo](media-setiteminfo.md) method.</span></span> <span data-ttu-id="dd723-131">Der folgende Beispielcode gibt den Wert "Proseware" für **contentdistributor** für das aktuell wiedergegebene Medien Element an:</span><span class="sxs-lookup"><span data-stu-id="dd723-131">The following example code specifies the value "Proseware" for **ContentDistributor** for the currently playing media item:</span></span>


```C++
// Retrieve the current media item.
var theMedia = Player.currentMedia;

//Test whether the media item was retrieved.
if(theMedia)
{
    // Set the ContentDistributor value.
    theMedia.setItemInfo("ContentDistributor", "Proseware");
}
```



## <a name="using-the-windows-media-format-sdk"></a><span data-ttu-id="dd723-132">Verwenden des SDK für den Windows Media-Format</span><span class="sxs-lookup"><span data-stu-id="dd723-132">Using the Windows Media Format SDK</span></span>

<span data-ttu-id="dd723-133">Das Windows Media Player SDK umfasst eine C++-Beispieldatei mit dem Namen setcontentdistributor. cpp, die veranschaulicht, wie das Windows Media Format 9-Reihe-SDK zum Hinzufügen des **WM/contentdistributor-** Attributs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="dd723-133">The Windows Media Player SDK includes a sample C++ file, named SetContentDistributor.cpp, which demonstrates how to use the Windows Media Format 9 Series SDK to add the **WM/ContentDistributor** attribute.</span></span> <span data-ttu-id="dd723-134">Sie finden diese Beispieldatei im Ordner "Metadata", in dem Sie das SDK installiert haben.</span><span class="sxs-lookup"><span data-stu-id="dd723-134">You can locate this sample file in the folder named Metadata where you installed the SDK.</span></span> <span data-ttu-id="dd723-135">Um diesen Code zu verwenden, müssen Sie die folgenden Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="dd723-135">To use this code you must follow these steps:</span></span>

1.  <span data-ttu-id="dd723-136">Installieren Sie das Windows Media Format 9-Reihe-SDK, und konfigurieren Sie die Runtime, wie in der Dokumentation beschrieben.</span><span class="sxs-lookup"><span data-stu-id="dd723-136">Install the Windows Media Format 9 Series SDK and configure the runtime as described in the documentation.</span></span>
2.  <span data-ttu-id="dd723-137">Erstellen Sie ein neues leeres C++-Projekt in Visual Studio, und fügen Sie dem Projekt die Beispieldatei mit dem Namen setcontentdistributor. cpp hinzu.</span><span class="sxs-lookup"><span data-stu-id="dd723-137">Create a new empty C++ project in Visual Studio and add the sample file named SetContentDistributor.cpp to the project.</span></span>
3.  <span data-ttu-id="dd723-138">Fügen Sie der Liste der Dateipfade den Pfad der SDK-lib-Ordner des Windows Media-Formats der Serie 9 hinzu.</span><span class="sxs-lookup"><span data-stu-id="dd723-138">Add the path to the Windows Media Format 9 Series SDK Lib folders to your list of file paths.</span></span> <span data-ttu-id="dd723-139">Wählen Sie im Menü **Extras** den Befehl **Optionen**.</span><span class="sxs-lookup"><span data-stu-id="dd723-139">From the **Tools** menu, choose **Options**.</span></span>
4.  <span data-ttu-id="dd723-140">Klicken Sie im Dialogfeld **Optionen** auf **Projekte**, und klicken Sie dann auf **VC + +-Verzeichnisse**.</span><span class="sxs-lookup"><span data-stu-id="dd723-140">In the **Options** dialog box, click **Projects**, and then click **VC++ Directories**.</span></span>
5.  <span data-ttu-id="dd723-141">Klicken Sie im Dropdown-Listenfeld **Verzeichnisse anzeigen für** auf **Bibliotheksdateien**.</span><span class="sxs-lookup"><span data-stu-id="dd723-141">In the **Show Directories for** drop-down list box, click **Library files**.</span></span>
6.  <span data-ttu-id="dd723-142">Verwenden Sie die Schaltflächen, um die Pfade zu den Listenfeldern hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="dd723-142">Use the buttons to add the paths to the list boxes.</span></span>
7.  <span data-ttu-id="dd723-143">Öffnen Sie das Dialogfeld Eigenschaften Seiten für das Projekt.</span><span class="sxs-lookup"><span data-stu-id="dd723-143">Open the property pages dialog box for your project.</span></span> <span data-ttu-id="dd723-144">Wählen Sie **Konfigurations Eigenschaften** und dann **Linker** aus, und geben Sie dann **Input** ein.</span><span class="sxs-lookup"><span data-stu-id="dd723-144">Choose **Configuration Properties**, then **Linker**, and then **Input**.</span></span> <span data-ttu-id="dd723-145">Geben Sie im Textfeld **Zusätzliche Abhängigkeiten** "Wmvcore. lib" ein.</span><span class="sxs-lookup"><span data-stu-id="dd723-145">Type "wmvcore.lib" in the **Additional Dependencies** text box.</span></span>

<span data-ttu-id="dd723-146">Der Beispielcode erstellt ein Befehlszeilenprogramm.</span><span class="sxs-lookup"><span data-stu-id="dd723-146">The sample code creates a command-line program.</span></span> <span data-ttu-id="dd723-147">Die Argumente, die Sie beim Ausführen des Programms angeben, geben den Pfad zu der zu ändernden digitalen Mediendatei und eine Zeichenfolge für den Wert des **contentdistributor** -Attributs an.</span><span class="sxs-lookup"><span data-stu-id="dd723-147">The arguments you provide when running the program specify the path to the digital media file to modify and a string for the **ContentDistributor** attribute value.</span></span> <span data-ttu-id="dd723-148">Der Code verwendet **iwmheaderinfo:: setAttribute** , um der von Ihnen angegebenen Datei das-Attribut hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="dd723-148">The code uses **IWMHeaderInfo::SetAttribute** to add the attribute to the file you specified.</span></span> <span data-ttu-id="dd723-149">Sie können dieses Beispiel unverändert verwenden oder als Ausgangspunkt für Ihr eigenes Programm verwenden.</span><span class="sxs-lookup"><span data-stu-id="dd723-149">You can use this sample as is or use it as a starting point for your own program.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dd723-150">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="dd723-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dd723-151">**Informationen, die von Typ 1 und Typ 2 Online Stores gemeinsam sind**</span><span class="sxs-lookup"><span data-stu-id="dd723-151">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> </dl>

 

 




