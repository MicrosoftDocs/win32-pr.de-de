---
title: Registrierungseinträge für die Bibliotheks Klassifizierung
description: Registrierungseinträge für die Bibliotheks Klassifizierung
ms.assetid: 3ef7d384-503f-4b8f-9f4b-e0ef3c56616b
keywords:
- Windows-Media Player, Bibliothek
- Windows Media Player, Klassifizierungs Registrierungseinträge
- Windows Media Player, Dateinamen Erweiterungen
- Windows Media Player, Registrierung
- Registrierung, Dateinamen Erweiterungen
- Registrierung, Bibliotheks Klassifizierungs Einträge
- Registrierung, Einstellungen für Windows-Media Player
- Registrierungs Einstellungen für die Dateinamenerweiterung
- Bibliothek, Klassifizierungs Registrierungseinträge
- Bibliothek, Registrierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e48ea1aacdd1e4c553a7e83bfdd711ff331c0878
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106342070"
---
# <a name="library-classification-registry-entries"></a><span data-ttu-id="9370f-113">Registrierungseinträge für die Bibliotheks Klassifizierung</span><span class="sxs-lookup"><span data-stu-id="9370f-113">Library Classification Registry Entries</span></span>

<span data-ttu-id="9370f-114">Wenn Windows Media Player auf eine Mediendatei mit einer benutzerdefinierten Dateierweiterung stößt, ist nicht bekannt, ob die Datei als Audiodatei, Video oder ein anderer Typ klassifiziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="9370f-114">When Windows Media Player encounters a media file that has a custom file name extension, it does not know whether the file should be classified as audio, video, or some other type.</span></span> <span data-ttu-id="9370f-115">Standardmäßig platziert Windows Media Player diese Dateien in den anderen Medienbereich der Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="9370f-115">By default, Windows Media Player places such files in the Other Media portion of the library.</span></span>

<span data-ttu-id="9370f-116">Wenn Ihre digitalen Mediendateien ein benutzerdefiniertes Format aufweisen, können Sie Windows Media Player Informationen darüber bereitstellen, wo Ihre Dateien in der Bibliothek des Players angezeigt werden sollen, indem Sie zwei Einträge in der Registrierung auf dem Computer des Benutzers platzieren.</span><span class="sxs-lookup"><span data-stu-id="9370f-116">If your digital media files have a custom format, you can provide Windows Media Player with information about where your files should appear in the Player's library by placing two entries in the registry on the user's computer.</span></span>

<span data-ttu-id="9370f-117">Ein Eintrag wird in den folgenden Unterschlüssel geleitet.</span><span class="sxs-lookup"><span data-stu-id="9370f-117">One entry goes in the following subkey.</span></span>

<span data-ttu-id="9370f-118">**HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ Media Player \\ MLS \\ Extensions**</span><span class="sxs-lookup"><span data-stu-id="9370f-118">**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\MediaPlayer\\MLS\\Extensions**</span></span>

<span data-ttu-id="9370f-119">Der Registrierungs Eintrag weist das folgende Format auf.</span><span class="sxs-lookup"><span data-stu-id="9370f-119">The registry entry has the following format.</span></span>



| <span data-ttu-id="9370f-120">Name</span><span class="sxs-lookup"><span data-stu-id="9370f-120">Name</span></span>                                                  | <span data-ttu-id="9370f-121">Datentyp</span><span class="sxs-lookup"><span data-stu-id="9370f-121">Data type</span></span>   | <span data-ttu-id="9370f-122">Wert</span><span class="sxs-lookup"><span data-stu-id="9370f-122">Value</span></span>                                      |
|-------------------------------------------------------|-------------|--------------------------------------------|
| <span data-ttu-id="9370f-123">Die Dateinamenerweiterung ohne das Punkt Trennzeichen (.)</span><span class="sxs-lookup"><span data-stu-id="9370f-123">The file name extension without the dot (.) separator</span></span> | <span data-ttu-id="9370f-124">**REG- \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="9370f-124">**REG\_SZ**</span></span> | <span data-ttu-id="9370f-125">Eine Zeichenfolge, die einen Bibliotheks Speicherort angibt.</span><span class="sxs-lookup"><span data-stu-id="9370f-125">A string that specifies a library location</span></span> |



 

<span data-ttu-id="9370f-126">Der andere Registrierungs Eintrag ist der folgende Unterschlüssel, den Sie erstellen.</span><span class="sxs-lookup"><span data-stu-id="9370f-126">The other registry entry goes in the following subkey that you create.</span></span>

<span data-ttu-id="9370f-127">**HKEY \_ Klassen Stamm-CustomExtension \_ \\** </span><span class="sxs-lookup"><span data-stu-id="9370f-127">**HKEY\_CLASSES\_ROOT\\** *customExtension*</span></span>

<span data-ttu-id="9370f-128">Dabei ist *CustomExtension* die Dateinamenerweiterung, einschließlich des Punkt Trennzeichens (.).</span><span class="sxs-lookup"><span data-stu-id="9370f-128">where *customExtension* is the file name extension including the dot (.) separator.</span></span>

<span data-ttu-id="9370f-129">Der Registrierungs Eintrag weist das folgende Format auf.</span><span class="sxs-lookup"><span data-stu-id="9370f-129">The registry entry has the following format.</span></span>



| <span data-ttu-id="9370f-130">Name</span><span class="sxs-lookup"><span data-stu-id="9370f-130">Name</span></span>          | <span data-ttu-id="9370f-131">Datentyp</span><span class="sxs-lookup"><span data-stu-id="9370f-131">Data type</span></span>   | <span data-ttu-id="9370f-132">Wert</span><span class="sxs-lookup"><span data-stu-id="9370f-132">Value</span></span>                                      |
|---------------|-------------|--------------------------------------------|
| <span data-ttu-id="9370f-133">Wahrnehmungstyp</span><span class="sxs-lookup"><span data-stu-id="9370f-133">PerceivedType</span></span> | <span data-ttu-id="9370f-134">**REG- \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="9370f-134">**REG\_SZ**</span></span> | <span data-ttu-id="9370f-135">Eine Zeichenfolge, die einen Bibliotheks Speicherort angibt.</span><span class="sxs-lookup"><span data-stu-id="9370f-135">A string that specifies a library location</span></span> |



 

<span data-ttu-id="9370f-136">Beide Registrierungseinträge müssen denselben Wert aufweisen.</span><span class="sxs-lookup"><span data-stu-id="9370f-136">Both registry entries must have the same value.</span></span> <span data-ttu-id="9370f-137">Mögliche Werte sind in der folgenden Tabelle angegeben.</span><span class="sxs-lookup"><span data-stu-id="9370f-137">Possible values are given in the following table.</span></span>



| <span data-ttu-id="9370f-138">Wert</span><span class="sxs-lookup"><span data-stu-id="9370f-138">Value</span></span> | <span data-ttu-id="9370f-139">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9370f-139">Description</span></span>                                                                      |
|-------|----------------------------------------------------------------------------------|
| <span data-ttu-id="9370f-140">Audio</span><span class="sxs-lookup"><span data-stu-id="9370f-140">audio</span></span> | <span data-ttu-id="9370f-141">Dateien, die über die benutzerdefinierte Erweiterung verfügen, werden im Musik Teil der Bibliothek angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9370f-141">Files that have the custom extension appear in the music portion of the library.</span></span> |
| <span data-ttu-id="9370f-142">video</span><span class="sxs-lookup"><span data-stu-id="9370f-142">video</span></span> | <span data-ttu-id="9370f-143">Dateien, die über die benutzerdefinierte Erweiterung verfügen, werden im Video Teil der Bibliothek angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9370f-143">Files that have the custom extension appear in the video portion of the library.</span></span> |



 

<span data-ttu-id="9370f-144">Die folgenden Registrierungseinträge geben z. b. an, dass Dateien mit der Dateinamenerweiterung ". xyz" im Musik Teil der Bibliothek angezeigt werden:</span><span class="sxs-lookup"><span data-stu-id="9370f-144">For example, the following registry entries specify that files having the file name extension .xyz will appear in the music portion of the library:</span></span>


```C++

HKEY_LOCAL_MACHINE\Software\Microsoft\MediaPlayer\MLS\Extensions
    xyz     REG_SZ     audio

HKEY_CLASSES_ROOT\.xyz
    PerceivedType     REG_SZ     audio

```



<span data-ttu-id="9370f-145">Beachten Sie, dass jeder Code, der versucht, in die Registrierung auf dem Computer des Benutzers zu schreiben, in die HKEY-Unterstruktur des lokalen Computers schreiben kann, \_ \_ Wenn der aktuelle Benutzer über Administratorrechte verfügt.</span><span class="sxs-lookup"><span data-stu-id="9370f-145">Note that any code that attempts to write to the registry on the user's computer can write to the HKEY\_LOCAL\_MACHINE subtree only if the current user has administrative privileges.</span></span>

<span data-ttu-id="9370f-146">Registrierungseinträge für die Bibliotheks Klassifizierung werden von den folgenden Versionen von Windows Media Player unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9370f-146">Library classification registry entries are supported by the following versions of Windows Media Player.</span></span>

-   <span data-ttu-id="9370f-147">Windows Media Player 9-Serie mit Hotfix 823275</span><span class="sxs-lookup"><span data-stu-id="9370f-147">Windows Media Player 9 Series with hotfix 823275</span></span>
-   <span data-ttu-id="9370f-148">Windows Media Player 10 und höher</span><span class="sxs-lookup"><span data-stu-id="9370f-148">Windows Media Player 10 and later</span></span>

## <a name="related-topics"></a><span data-ttu-id="9370f-149">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9370f-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9370f-150">**Registrierungs Einstellungen für die Dateinamenerweiterung**</span><span class="sxs-lookup"><span data-stu-id="9370f-150">**File Name Extension Registry Settings**</span></span>](file-name-extension-registry-settings.md)
</dt> </dl>

 

 




