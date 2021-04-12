---
title: Registrierungs Einstellungen für die Ordner Überwachung
description: Registrierungs Einstellungen für die Ordner Überwachung
ms.assetid: 563aeaec-0759-4b0c-a8e9-a9a2b3092515
keywords:
- Windows Media Player, Registrierungs Einstellungen für die Ordner Überwachung
- Windows Media Player, Registrierungs Einstellungen für die Datei Ordner Überwachung
- Windows Media Player, Registrierung
- Registrierung, Ordner Überwachungs Einstellungen
- Registrierung, Einstellungen für die Überwachung von Datei Ordnern
- Registrierung, Einstellungen für Windows-Media Player
- Registrierungs Einstellungen für die Ordner Überwachung
- Registrierungs Einstellungen für die Datei Ordner Überwachung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 233076d1fc807dd5cdd79e9b4985ef752fba0815
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "104391129"
---
# <a name="folder-monitoring-registry-settings"></a><span data-ttu-id="8f6ee-111">Registrierungs Einstellungen für die Ordner Überwachung</span><span class="sxs-lookup"><span data-stu-id="8f6ee-111">Folder Monitoring Registry Settings</span></span>

<span data-ttu-id="8f6ee-112">Windows Media Player 9 oder höher kann Datei Ordner für neue digitale Mediendateien überwachen.</span><span class="sxs-lookup"><span data-stu-id="8f6ee-112">Windows Media Player 9 Series or later can monitor file folders for new digital media files.</span></span> <span data-ttu-id="8f6ee-113">Wenn der Spieler eine neue Datei in einem überwachten Ordner erkennt, wird die Datei automatisch der Bibliothek hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="8f6ee-113">When the Player detects a new file in a monitored folder, it automatically adds the file to the library.</span></span> <span data-ttu-id="8f6ee-114">Für Windows Media Player 9 bis Windows Media Player 11 können Benutzer die Liste der überwachten Ordner ändern, indem Sie im Dialogfeld **Optionen** auf der Registerkarte Bibliothek auf **Ordner überwachen** klicken.</span><span class="sxs-lookup"><span data-stu-id="8f6ee-114">For Windows Media Player 9 through Windows Media Player 11, users can change the list of monitored folders by clicking **Monitor Folders** on the library tab of the **Options** dialog box.</span></span> <span data-ttu-id="8f6ee-115">Für Windows Media Player 12 kann ein Benutzer die Liste der überwachten Ordner anhand der Anweisungen im Thema [Hinzufügen von Elementen zur Windows Media Player-Bibliothek](https://windows.microsoft.com/windows7/Add-items-to-the-Windows-Media-Player-Library)ändern.</span><span class="sxs-lookup"><span data-stu-id="8f6ee-115">For Windows Media Player 12, a user can change the list of monitored folders by following the instructions in the topic [Add items to the Windows Media Player Library](https://windows.microsoft.com/windows7/Add-items-to-the-Windows-Media-Player-Library).</span></span> <span data-ttu-id="8f6ee-116">Für Windows Media Player 9 bis Windows Media Player 11 können Sie einen zu überwachenden Ordner Programm gesteuert hinzufügen, indem Sie der Registrierung einen Wert hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="8f6ee-116">For Windows Media Player 9 through Windows Media Player 11, you can programmatically add a folder to be monitored by adding a value to the registry.</span></span> <span data-ttu-id="8f6ee-117">Für Windows Media Player 12 können Sie die Registrierung nicht verwenden, um zu überwachende Ordner Programm gesteuert hinzuzufügen oder zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="8f6ee-117">For Windows Media Player 12, you cannot use the registry to programmatically add or remove folders to be monitored.</span></span>

<span data-ttu-id="8f6ee-118">Wenn Sie für Windows Media Player 9 bis Windows Media Player 11 einen Ordner für die Überwachung hinzufügen möchten, müssen Sie zunächst zwei Werte im folgenden Registrierungsschlüssel erstellen oder ändern:</span><span class="sxs-lookup"><span data-stu-id="8f6ee-118">For Windows Media Player 9 through Windows Media Player 11, to add a folder for monitoring you must first create or modify two values in the following registry key:</span></span>

<span data-ttu-id="8f6ee-119">**HKEY \_ Current \_ User \\ Software \\ Microsoft \\ Media Player \\ Preferences\\**</span><span class="sxs-lookup"><span data-stu-id="8f6ee-119">**HKEY\_CURRENT\_USER\\Software\\Microsoft\\MediaPlayer\\Preferences\\**</span></span>

<span data-ttu-id="8f6ee-120">Die neuen Werte müssen wie folgt benannt werden.</span><span class="sxs-lookup"><span data-stu-id="8f6ee-120">The new values must be named as follows.</span></span>



| <span data-ttu-id="8f6ee-121">Name</span><span class="sxs-lookup"><span data-stu-id="8f6ee-121">Name</span></span>                           | <span data-ttu-id="8f6ee-122">type</span><span class="sxs-lookup"><span data-stu-id="8f6ee-122">Type</span></span>           | <span data-ttu-id="8f6ee-123">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8f6ee-123">Description</span></span>                                                                                                                                                                                                                                                                    |
|--------------------------------|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f6ee-124">**Trackfoldersdirectories**</span><span class="sxs-lookup"><span data-stu-id="8f6ee-124">**TrackFoldersDirectories**</span></span>    | <span data-ttu-id="8f6ee-125">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="8f6ee-125">**REG\_DWORD**</span></span> | <span data-ttu-id="8f6ee-126">Ein **DWORD** -Wert, der die Anzahl der zu überwachenden Ordner darstellt.</span><span class="sxs-lookup"><span data-stu-id="8f6ee-126">A **DWORD** value that represents the count of folders to monitor.</span></span> <span data-ttu-id="8f6ee-127">Diese muss mit der Anzahl der \**trackfoldersdirectories \* \* \* X* -Werte identisch sein.</span><span class="sxs-lookup"><span data-stu-id="8f6ee-127">This must match the count of \**TrackFoldersDirectories\*\*\*X* values.</span></span>                                                                                                                                         |
| <span data-ttu-id="8f6ee-128">\**Trackfoldersdirectories \* \* \* X*</span><span class="sxs-lookup"><span data-stu-id="8f6ee-128">\**TrackFoldersDirectories\*\*\*X*</span></span> | <span data-ttu-id="8f6ee-129">**REG- \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="8f6ee-129">**REG\_SZ**</span></span>    | <span data-ttu-id="8f6ee-130">Ein Zeichen folgen Wert, der den Pfad des zu überwachenden Ordners darstellt.</span><span class="sxs-lookup"><span data-stu-id="8f6ee-130">A string value that represents the path of the folder to monitor.</span></span> <span data-ttu-id="8f6ee-131">Für jeden zu überwachenden Ordner ist ein separater Wert erforderlich.</span><span class="sxs-lookup"><span data-stu-id="8f6ee-131">Each folder to monitor requires a separate value.</span></span> <span data-ttu-id="8f6ee-132">Das Suffix *X* ist eine Ganzzahl, die immer bei 0 beginnen sollte und dann um 1 erhöht werden soll.</span><span class="sxs-lookup"><span data-stu-id="8f6ee-132">The suffix *X* is an integer that should always begin at 0 and then increment by 1.</span></span> <span data-ttu-id="8f6ee-133">Windows Media Player überwacht auch die Unterordner des angegebenen Ordners.</span><span class="sxs-lookup"><span data-stu-id="8f6ee-133">Windows Media Player also monitors subfolders of the specified folder.</span></span> |



 

<span data-ttu-id="8f6ee-134">Fügen Sie z. b. den folgenden Wert hinzu, um den ersten zu überwachenden Ordner hinzuzufügen:</span><span class="sxs-lookup"><span data-stu-id="8f6ee-134">For example, to add the first folder to monitor, add the following value:</span></span>


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Preferences]
"TrackFoldersDirectories0" = "c:\MyPath\MyFolder"

```



<span data-ttu-id="8f6ee-135">Erstellen Sie dann den Wert Anzahl:</span><span class="sxs-lookup"><span data-stu-id="8f6ee-135">Then, create the count value:</span></span>


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Preferences]
"TrackFoldersDirectories" = dword:00000001

```



<span data-ttu-id="8f6ee-136">Um einen zweiten Ordner zur Überwachung hinzuzufügen, fügen Sie den folgenden Wert hinzu:</span><span class="sxs-lookup"><span data-stu-id="8f6ee-136">To add a second folder to monitor, add the following value:</span></span>


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Preferences]
"TrackFoldersDirectories1" = "c:\MyPath\MyFolder2"

```



<span data-ttu-id="8f6ee-137">Erhöhen Sie anschließend den Wert für die Anzahl:</span><span class="sxs-lookup"><span data-stu-id="8f6ee-137">Then, increment the count value:</span></span>


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Preferences]
"TrackFoldersDirectories" = dword:00000002

```



## <a name="related-topics"></a><span data-ttu-id="8f6ee-138">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8f6ee-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8f6ee-139">**Registrierungs Einstellungen**</span><span class="sxs-lookup"><span data-stu-id="8f6ee-139">**Registry Settings**</span></span>](registry-settings.md)
</dt> </dl>

 

 




