---
title: DRM-Grundlagen
description: DRM-Grundlagen
ms.assetid: f36da29d-5f9d-441d-8061-eb50331a8e7a
keywords:
- Windows Media-Format-SDK, DRM-Grundlagen
- Digital Rights Management (DRM), Informationen zu
- DRM (Digital Rights Management), Informationen zu
- Digital Rights Management (DRM), schützen von Inhalten
- DRM (Digital Rights Management), schützen von Inhalten
- Digital Rights Management (DRM), Verpacken von Inhalten
- DRM (Digital Rights Management), Verpacken von Inhalten
- Digital Rights Management (DRM), lesen geschützter Inhalte
- DRM (Digital Rights Management), lesen geschützter Inhalte
- Schützen von Inhalten
- Verpacken von Inhalten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c210fceb69174147dcb36a3e97b5591c2654a566
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388744"
---
# <a name="drm-basics"></a><span data-ttu-id="4bb8f-114">DRM-Grundlagen</span><span class="sxs-lookup"><span data-stu-id="4bb8f-114">DRM Basics</span></span>

<span data-ttu-id="4bb8f-115">Die Windows Media DRM-Technologien sind aus der Sicht des Windows Media-Formats SDK recht einfach.</span><span class="sxs-lookup"><span data-stu-id="4bb8f-115">The Windows Media DRM technologies are fairly simple from the perspective of the Windows Media Format SDK.</span></span> <span data-ttu-id="4bb8f-116">Komponenten des SDK können verwendet werden, um Inhalte zu schützen und geschützte Inhalte wiederzugeben.</span><span class="sxs-lookup"><span data-stu-id="4bb8f-116">Components of the SDK can be used to protect content and to play protected content.</span></span>

## <a name="protecting-content"></a><span data-ttu-id="4bb8f-117">Schützen von Inhalt</span><span class="sxs-lookup"><span data-stu-id="4bb8f-117">Protecting Content</span></span>

<span data-ttu-id="4bb8f-118">Der Schutz von Inhalten (auch als Paketinhalt bezeichnet) umfasst das Verschlüsseln des Daten Abschnitts der Datei und das einschließen einiger Informationen in den Dateiheader, mit denen der Inhalt von den Playern entschlüsselt werden kann.</span><span class="sxs-lookup"><span data-stu-id="4bb8f-118">Protecting content (also called packaging content) involves encrypting the data section of the file and including some information in the file header that enables players to decrypt the content.</span></span>

<span data-ttu-id="4bb8f-119">Um den Inhalt zu verschlüsseln, benötigen Sie einen Schlüssel, der als Ausgangswert für die Verschlüsselungsalgorithmen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4bb8f-119">To encrypt the content, you need a key, which is a value used to seed the encryption algorithms.</span></span> <span data-ttu-id="4bb8f-120">Ein Schlüssel besteht aus zwei Teilen: einem schlüsselseed (oder einem privaten Schlüssel) und einem Schlüssel Bezeichner (oder einem öffentlichen Schlüssel).</span><span class="sxs-lookup"><span data-stu-id="4bb8f-120">A key is made up of two pieces: a key seed (or private key), and a key identifier (or public key).</span></span> <span data-ttu-id="4bb8f-121">Der Schlüssel Startwert ist der geheime Wert, mit dem Sie Inhalte codieren.</span><span class="sxs-lookup"><span data-stu-id="4bb8f-121">The key seed is the secret value with which you encode content.</span></span> <span data-ttu-id="4bb8f-122">Der Schlüssel Bezeichner ist ein öffentlicher Wert, der im Header einer geschützten Datei enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="4bb8f-122">The key identifier is a public value that is included in the header of a protected file.</span></span>

<span data-ttu-id="4bb8f-123">Wenn eine Datei geschützt ist, kann Sie nicht ohne Lizenz entschlüsselt werden.</span><span class="sxs-lookup"><span data-stu-id="4bb8f-123">When a file is protected, it cannot be decrypted without a license.</span></span> <span data-ttu-id="4bb8f-124">Eine Lizenz umfasst Informationen, mit denen die Nutzungsbedingungen für den geschützten Inhalt angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="4bb8f-124">A license includes information that specifies the terms of use for the protected content.</span></span> <span data-ttu-id="4bb8f-125">Die Lizenzbedingungen werden vom Inhalts Besitzer entschieden und können an verschiedene Anforderungen angepasst werden.</span><span class="sxs-lookup"><span data-stu-id="4bb8f-125">The terms of a license are decided by the content owner and can be customized to meet a variety of needs.</span></span> <span data-ttu-id="4bb8f-126">Ein Teil des paketpaketpakets besteht darin, die URL einer Webseite einzuschließen, auf der Benutzer eine Lizenz für den Zugriff auf den Inhalt erwerben können.</span><span class="sxs-lookup"><span data-stu-id="4bb8f-126">Part of the process of packaging a file is to include the URL of a Web page where users can acquire a license to access the content.</span></span>

## <a name="reading-protected-content"></a><span data-ttu-id="4bb8f-127">Lesen geschützter Inhalte</span><span class="sxs-lookup"><span data-stu-id="4bb8f-127">Reading Protected Content</span></span>

<span data-ttu-id="4bb8f-128">Um geschützte Inhalte zu lesen, muss sich eine Lizenz für den Inhalt auf dem Client Computer befinden.</span><span class="sxs-lookup"><span data-stu-id="4bb8f-128">To read protected content, a license for the content must reside on the client computer.</span></span> <span data-ttu-id="4bb8f-129">Einige Lizenz Einschränkungen werden intern von den DRM-Komponenten des Windows Media SDK-SDKs geprüft, während andere von Ihrer Anwendung erzwungen werden müssen.</span><span class="sxs-lookup"><span data-stu-id="4bb8f-129">Some license restrictions are checked internally by the DRM components of the Windows Media Format SDK, while others must be enforced by your application.</span></span>

<span data-ttu-id="4bb8f-130">Mithilfe der Objekte des SDK für den Windows Media-Format können Sie den Benutzer beim Erwerb von Lizenzen für Inhalte und beim Ausführen anderer Verwaltungsaufgaben unterstützen, z. b. beim Aktualisieren von DRM-Komponenten und Sichern von Lizenzen.</span><span class="sxs-lookup"><span data-stu-id="4bb8f-130">You can use the objects of the Windows Media Format SDK to assist the user in acquiring licenses for content and to perform other administrative tasks, such as updating DRM components and backing up licenses.</span></span>

> [!Note]  
> <span data-ttu-id="4bb8f-131">DRM wird von der x64-basierten Version dieses SDK nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4bb8f-131">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="4bb8f-132">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4bb8f-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4bb8f-133">**Features digitaler Rights Management**</span><span class="sxs-lookup"><span data-stu-id="4bb8f-133">**Digital Rights Management Features**</span></span>](digital-rights-management-features.md)
</dt> <dt>

[<span data-ttu-id="4bb8f-134">**Aktivieren DRM-Unterstützung**</span><span class="sxs-lookup"><span data-stu-id="4bb8f-134">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> </dl>

 

 




