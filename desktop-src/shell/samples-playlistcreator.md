---
description: Veranschaulicht, wie ein Verb erstellt wird, das für ein ausgewähltes shellelement oder einen ausgewählten Container zum Erstellen einer Wiedergabeliste funktioniert.
title: Wiedergabelistenersteller (Beispiel)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: B35B7A18-2163-4860-BC50-8918056C9F4A
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 5c5e4f6570faff459126a32ea4680d41a3b8302e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980921"
---
# <a name="playlist-creator-sample"></a><span data-ttu-id="d54d7-103">Wiedergabelistenersteller (Beispiel)</span><span class="sxs-lookup"><span data-stu-id="d54d7-103">Playlist Creator Sample</span></span>

<span data-ttu-id="d54d7-104">Veranschaulicht, wie ein Verb erstellt wird, das für ein ausgewähltes shellelement oder einen ausgewählten Container zum Erstellen einer Wiedergabeliste funktioniert.</span><span class="sxs-lookup"><span data-stu-id="d54d7-104">Demonstrates how to create a verb that operates on a selected Shell item or container to create a playlist.</span></span>

<span data-ttu-id="d54d7-105">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="d54d7-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="d54d7-106">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d54d7-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="d54d7-107">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="d54d7-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="d54d7-108">Beispiel zum Aufbau</span><span class="sxs-lookup"><span data-stu-id="d54d7-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="d54d7-109">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="d54d7-109">Running the Sample</span></span>](#running-the-sample)

## <a name="requirements"></a><span data-ttu-id="d54d7-110">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="d54d7-110">Requirements</span></span>



| <span data-ttu-id="d54d7-111">Produkt</span><span class="sxs-lookup"><span data-stu-id="d54d7-111">Product</span></span>                                | <span data-ttu-id="d54d7-112">Minimale Produkt Version</span><span class="sxs-lookup"><span data-stu-id="d54d7-112">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="d54d7-113">Windows</span><span class="sxs-lookup"><span data-stu-id="d54d7-113">Windows</span></span>                                | <span data-ttu-id="d54d7-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d54d7-114">Windows Vista</span></span>           |
| <span data-ttu-id="d54d7-115">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="d54d7-115">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="d54d7-116">7.0</span><span class="sxs-lookup"><span data-stu-id="d54d7-116">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="d54d7-117">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="d54d7-117">Downloading the Sample</span></span>

| <span data-ttu-id="d54d7-118">Standort</span><span class="sxs-lookup"><span data-stu-id="d54d7-118">Location</span></span>      | <span data-ttu-id="d54d7-119">Pfad-URL</span><span class="sxs-lookup"><span data-stu-id="d54d7-119">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d54d7-120">GitHub</span><span class="sxs-lookup"><span data-stu-id="d54d7-120">GitHub</span></span>  | [<span data-ttu-id="d54d7-121">Playlistcreator-Beispiel</span><span class="sxs-lookup"><span data-stu-id="d54d7-121">PlaylistCreator sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/PlaylistCreator) |

## <a name="building-the-sample"></a><span data-ttu-id="d54d7-122">Erstellen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="d54d7-122">Building the Sample</span></span>

<span data-ttu-id="d54d7-123">So erstellen Sie das Beispiel von der Eingabeaufforderung aus:</span><span class="sxs-lookup"><span data-stu-id="d54d7-123">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="d54d7-124">Öffnen Sie das Eingabe Aufforderungs Fenster, und navigieren Sie zum Projektverzeichnis **playlistcreator** .</span><span class="sxs-lookup"><span data-stu-id="d54d7-124">Open the command prompt window and navigate to the **PlaylistCreator** project directory.</span></span>
2.  <span data-ttu-id="d54d7-125">Geben Sie `msbuild PlaylistCreator.sln` ein.</span><span class="sxs-lookup"><span data-stu-id="d54d7-125">Enter `msbuild PlaylistCreator.sln`.</span></span>

<span data-ttu-id="d54d7-126">So erstellen Sie das Beispiel mithilfe Microsoft Visual Studio (bevorzugt):</span><span class="sxs-lookup"><span data-stu-id="d54d7-126">To build the sample using Microsoft Visual Studio (preferred):</span></span>

> [!Note]  
> <span data-ttu-id="d54d7-127">Dieses Beispiel kann auch mit der Visual C++ Express Edition verwendet werden, wenn das vollständige Visual Studio nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="d54d7-127">This sample can also be used with the Visual C++ Express Edition if the full Visual Studio is not available.</span></span>

 

1.  <span data-ttu-id="d54d7-128">Öffnen Sie Windows-Explorer, und navigieren Sie zum Projektverzeichnis **playlistcreator** .</span><span class="sxs-lookup"><span data-stu-id="d54d7-128">Open Windows Explorer and navigate to the **PlaylistCreator** project directory.</span></span>
2.  <span data-ttu-id="d54d7-129">Doppelklicken Sie auf das Symbol für die Datei playlistcreator. sln, um das Projekt in Visual Studio zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="d54d7-129">Double-click the icon for the PlaylistCreator.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="d54d7-130">Wählen Sie im Menü **Erstellen** die Option Projekt Mappe **Erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="d54d7-130">From the **Build** menu, select **Build Solution**.</span></span>
    > [!Note]  
    > <span data-ttu-id="d54d7-131">Wenn Sie 64-Bit mithilfe der Visual C++ Express Edition kompilieren, müssen Sie den für die Windows SDK bereitgestellten x64-Cross-Compiler verwenden.</span><span class="sxs-lookup"><span data-stu-id="d54d7-131">If you are compiling 64-bit using the Visual C++ Express Edition, you must to use the x64 cross-compiler supplied with the Windows SDK.</span></span>

     

## <a name="running-the-sample"></a><span data-ttu-id="d54d7-132">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="d54d7-132">Running the Sample</span></span>

1.  <span data-ttu-id="d54d7-133">Navigieren Sie mithilfe der Eingabeaufforderung oder Windows-Explorer zu dem Verzeichnis, das die neue ausführbare Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="d54d7-133">Navigate to the directory that contains the new executable, using the command prompt or Windows Explorer.</span></span>
2.  <span data-ttu-id="d54d7-134">Geben Sie in der Befehlszeile ein `PlaylistCreator.exe` .</span><span class="sxs-lookup"><span data-stu-id="d54d7-134">At the command line, enter `PlaylistCreator.exe`.</span></span> <span data-ttu-id="d54d7-135">Alternativ können Sie in Windows-Explorer auf das Symbol für PlaylistCreator.exe doppelklicken.</span><span class="sxs-lookup"><span data-stu-id="d54d7-135">Alternatively, from Windows Explorer double-click the icon for PlaylistCreator.exe.</span></span>
3.  <span data-ttu-id="d54d7-136">Klicken Sie mit der rechten Maustaste auf eine beliebige Musikdatei oder einen Ordner mit Musikdateien im Windows-Explorer, um eine Wiedergabeliste für das Kontextmenü zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d54d7-136">Right-click any music file or folder containing music files in Windows Explorer to create a playlist to bring up the context menu</span></span>
4.  <span data-ttu-id="d54d7-137">Sie können eine. M3U-oder WPL-Wiedergabeliste erstellen.</span><span class="sxs-lookup"><span data-stu-id="d54d7-137">You can create a .m3u or .wpl playlist.</span></span> <span data-ttu-id="d54d7-138">Wiedergabelisten werden im `%userprofile%\Music\Playlists` Ordner erstellt.</span><span class="sxs-lookup"><span data-stu-id="d54d7-138">Playlists are created in the `%userprofile%\Music\Playlists` folder.</span></span>
    > [!Note]  
    > <span data-ttu-id="d54d7-139">Neue Verben im Kontextmenü finden Sie im Ordner " **Musik** ", Musik Stapel, Stapeln in der **Musikbibliothek** und Sammlungen von Musikdateien.</span><span class="sxs-lookup"><span data-stu-id="d54d7-139">New verbs in the context menu can be found in the **Music** folder, music stacks, stacks in the **Music Library**, and collections of music files.</span></span>

     

 

 



