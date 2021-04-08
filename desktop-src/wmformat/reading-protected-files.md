---
title: Geschützte Dateien werden gelesen.
description: Geschützte Dateien werden gelesen.
ms.assetid: 24f839f1-ce57-4d06-b1a5-a6bea7b5b7bb
keywords:
- Windows Media-Format-SDK, lesen geschützter Dateien
- Windows Media-Format-SDK, geschützte Dateien
- Advanced Systems Format (ASF), lesen geschützter Dateien
- ASF (Advanced Systems Format), lesen geschützter Dateien
- Advanced Systems Format (ASF), geschützte Dateien
- ASF (Advanced Systems Format), geschützte Dateien
- Advanced Systems Format (ASF), wmstubdrm. lib
- ASF (Advanced Systems Format), wmstubdrm. lib
- Wmstubdrm. lib, lesen geschützter Dateien
- Wmstubdrm. lib, geschützte Dateien
- Digital Rights Management (DRM), wmstubdrm. lib
- DRM (Digital Rights Management), wmstubdrm. lib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4b2110708a28daae1e86ba3dac2ea1f18ad16fc
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723408"
---
# <a name="reading-protected-files"></a><span data-ttu-id="4ee59-115">Geschützte Dateien werden gelesen.</span><span class="sxs-lookup"><span data-stu-id="4ee59-115">Reading Protected Files</span></span>

<span data-ttu-id="4ee59-116">Das Lesen einer DRM-geschützten Datei oder eines Netzwerkstreams umfasst im Wesentlichen den Versuch, die Datei zu öffnen (oder eine Verbindung mit dem Stream herzustellen) und dann alle Ereignisse zu behandeln, die von den DRM-Komponenten gesendet werden können.</span><span class="sxs-lookup"><span data-stu-id="4ee59-116">Reading a DRM-protected file or network stream basically involves attempting to open the file (or connect to the stream) and then handling any events that might be sent from the DRM components.</span></span>

<span data-ttu-id="4ee59-117">Wenn ein Player nicht DRM-aktiviert ist (keine Verknüpfung mit einer gültigen wmstubdrm. lib-Bibliothek), schlägt der [**iwmreader:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) -Befehl fehl, wenn versucht wird, eine geschützte Datei zu öffnen, und gibt den von NS \_ E \_ geschützten \_ Inhalt oder einen zugehörigen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="4ee59-117">If a player is not DRM-enabled (does not link to a valid wmstubdrm.lib library) the [**IWMReader::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) call fails when it tries to open a protected file and returns NS\_E\_PROTECTED\_CONTENT or some related error.</span></span>

<span data-ttu-id="4ee59-118">Wenn eine DRM-fähige Anwendung versucht, eine DRM-geschützte Datei zu öffnen, durchsucht die DRM-Komponente automatisch das lokale System nach einer gültigen Lizenz.</span><span class="sxs-lookup"><span data-stu-id="4ee59-118">When a DRM-enabled application attempts to open a DRM-protected file, the DRM component automatically searches the local system for a valid license.</span></span> <span data-ttu-id="4ee59-119">Wenn ein solcher gefunden wird, entschlüsselt die DRM-Komponente die Datei automatisch auf eine Weise, die für die Anwendung vollständig transparent ist.</span><span class="sxs-lookup"><span data-stu-id="4ee59-119">If one is found, the DRM component automatically decrypts the file in a way that is completely transparent to the application.</span></span> <span data-ttu-id="4ee59-120">Die Aktion, die eine Anwendung für die entschlüsselte Datei ausführen kann, hängt von den in der Lizenz angegebenen rechten ab.</span><span class="sxs-lookup"><span data-stu-id="4ee59-120">The action that an application may perform on the decrypted file depends on the rights specified in the license.</span></span> <span data-ttu-id="4ee59-121">Eine vollständige Beschreibung der möglichen Rechte finden Sie in der Dokumentation zum Windows Media Rights Manager SDK.</span><span class="sxs-lookup"><span data-stu-id="4ee59-121">For a full description of possible rights, see the Windows Media Rights Manager SDK documentation.</span></span>

<span data-ttu-id="4ee59-122">Wenn die Anwendung nicht über eine gültige Lizenz für eine Datei verfügt, empfängt der Spieler eine Status Benachrichtigung von der DRM-Komponente.</span><span class="sxs-lookup"><span data-stu-id="4ee59-122">If the application does not have a valid license for a file, the player receives a status notification from the DRM component.</span></span> <span data-ttu-id="4ee59-123">Die Player Anwendung kann dann den [*Lizenz Erwerbs*](wmformat-glossary.md) Prozess initiieren.</span><span class="sxs-lookup"><span data-stu-id="4ee59-123">The player application can then initiate the [*license acquisition*](wmformat-glossary.md) process.</span></span> <span data-ttu-id="4ee59-124">Nachdem eine gültige Lizenz eingegangen ist, kann auf die Datei zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="4ee59-124">After a valid license has been received, the file can be accessed.</span></span> <span data-ttu-id="4ee59-125">In den folgenden Abschnitten werden die grundlegenden Aufgaben beschrieben, die eine Anwendung bei der Implementierung des Lizenz Erwerbs Vorgangs ausführen muss:</span><span class="sxs-lookup"><span data-stu-id="4ee59-125">The following sections describe the basic tasks that an application must perform in implementing the license acquisition process:</span></span>

-   [<span data-ttu-id="4ee59-126">Angeben der auszuführenden Aktionen</span><span class="sxs-lookup"><span data-stu-id="4ee59-126">Specifying the Actions To Be Performed</span></span>](specifying-the-actions-to-be-performed.md)
-   [<span data-ttu-id="4ee59-127">Behandeln von Lizenz Erwerbs Ereignissen</span><span class="sxs-lookup"><span data-stu-id="4ee59-127">Handling License Acquisition Events</span></span>](handling-license-acquisition-events.md)
-   [<span data-ttu-id="4ee59-128">Individualisieren von DRM-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="4ee59-128">Individualizing DRM Applications</span></span>](individualizing-drm-applications.md)
-   [<span data-ttu-id="4ee59-129">Behandeln von Individualisierungs Ereignissen</span><span class="sxs-lookup"><span data-stu-id="4ee59-129">Handling Individualization Events</span></span>](handling-individualization-events.md)

> [!Note]  
> <span data-ttu-id="4ee59-130">DRM wird von der x64-basierten Version dieses SDK nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4ee59-130">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="4ee59-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4ee59-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4ee59-132">**Features digitaler Rights Management**</span><span class="sxs-lookup"><span data-stu-id="4ee59-132">**Digital Rights Management Features**</span></span>](digital-rights-management-features.md)
</dt> <dt>

[<span data-ttu-id="4ee59-133">**DRM-Attribut Liste**</span><span class="sxs-lookup"><span data-stu-id="4ee59-133">**DRM Attribute List**</span></span>](drm-attribute-list.md)
</dt> <dt>

[<span data-ttu-id="4ee59-134">**DRM-Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="4ee59-134">**DRM Properties**</span></span>](drm-properties.md)
</dt> <dt>

[<span data-ttu-id="4ee59-135">**Aktivieren DRM-Unterstützung**</span><span class="sxs-lookup"><span data-stu-id="4ee59-135">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> </dl>

 

 




