---
title: DRM-Schutz und Inhalts Lizenz Verteilung
description: DRM-Schutz und Inhalts Lizenz Verteilung
ms.assetid: 147fef8c-7298-450d-a1a9-345c03c49bec
keywords:
- Windows Media-Format-SDK, DRM-Inhalts Schutz
- Windows Media-Format-SDK, DRM-Lizenzen
- Advanced Systems Format (ASF), DRM-Inhalts Schutz
- ASF (Advanced Systems Format), DRM-Inhalts Schutz
- Advanced Systems Format (ASF), DRM-Lizenz Verteilung
- ASF (Advanced Systems Format), DRM-Lizenz Verteilung
- Digital Rights Management (DRM), Inhalts Schutz
- DRM (Digital Rights Management), Inhalts Schutz
- Digital Rights Management (DRM), Lizenz Verteilung
- DRM (Digital Rights Management), Lizenz Verteilung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25af13947828885d70f3e0fd9fe8bf035eb8c5e5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311453"
---
# <a name="drm-protection-and-content-license-distribution"></a><span data-ttu-id="c97c8-113">DRM-Schutz und Inhalts Lizenz Verteilung</span><span class="sxs-lookup"><span data-stu-id="c97c8-113">DRM Protection and Content License Distribution</span></span>

<span data-ttu-id="c97c8-114">Auf der Erstellungs Seite beinhaltet Digital Rights Management Technologie zwei Hauptprozesse: (1) der Schutz des Inhalts und (2) die Bereitstellung von Lizenzen für den Inhalt.</span><span class="sxs-lookup"><span data-stu-id="c97c8-114">On the creation side, digital rights management technology involves two main processes: (1) protecting the content and (2) providing licenses for the content.</span></span> <span data-ttu-id="c97c8-115">Der Schutz einer Datei umfasst im Wesentlichen das Verschlüsseln des Inhalts und das Einschließen einer URL in den Dateiheader, die angibt, wo eine Lizenz für den Inhalt abgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="c97c8-115">Protecting a file basically involves encrypting the content, and including a URL in the file header that specifies where a license for the content may be obtained.</span></span> <span data-ttu-id="c97c8-116">Wenn Sie Dateien mit schützen und die Dateien dann an andere Computer oder Geräte verteilen möchten, können Sie das Windows Media-Format-SDK oder das Windows Media Rights Manager SDK verwenden, um die Datei zu schützen.</span><span class="sxs-lookup"><span data-stu-id="c97c8-116">If you want to protect files with and then distribute the files to other computers or devices, you can use either the Windows Media Format SDK or the Windows Media Rights Manager SDK to protect the file.</span></span> <span data-ttu-id="c97c8-117">Bei Live-DRM-Szenarien müssen Sie das Windows Media-Format-SDK verwenden, um den Inhalt zu schützen, während er codiert wird.</span><span class="sxs-lookup"><span data-stu-id="c97c8-117">For live-DRM scenarios, you must use the Windows Media Format SDK to protect the content as it is being encoded.</span></span>

<span data-ttu-id="c97c8-118">Zum Erstellen und Ausstellen von Lizenzen für geschützte Inhalte können Sie eine eigene benutzerdefinierte Lösung mithilfe der Objekte des Windows Media Rights Manager SDK erstellen, oder Sie können einen Dienst verwenden, der von einem Drittanbieter ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c97c8-118">To create and issue licenses for protected content, you can create your own custom solution using the objects of the Windows Media Rights Manager SDK, or you can use a service run by a third party.</span></span>

<span data-ttu-id="c97c8-119">Unabhängig davon, welche Methode Sie verwenden, enthalten die geschützten Dateien, die Sie erstellen, im DRM-Header Objekt eine URL, die Client Anwendungen mitteilt, wo eine Lizenz für den Inhalt abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="c97c8-119">Whichever method you use, the protected files that you create will contain, in the DRM header object, a URL that tells client applications where to obtain a license for the content.</span></span>

> [!Note]  
> <span data-ttu-id="c97c8-120">Das Windows Media-Format-SDK bietet keine Unterstützung für das Erstellen oder Ausstellen von Lizenzen.</span><span class="sxs-lookup"><span data-stu-id="c97c8-120">The Windows Media Format SDK does not provide support for creating or issuing licenses.</span></span>

 

<span data-ttu-id="c97c8-121">Auf der Wiedergabe Seite muss eine DRM-fähige Anwendung in der Lage sein, Lizenzen für geschützte Inhalte zu erhalten, den Inhalt mit dem in der Lizenz enthaltenen Schlüssel zu entschlüsseln und die Lizenzbeschränkungen zu erzwingen, z. b. wie oft eine Datei abgespielt werden kann oder ob die Datei auf ein anderes Gerät kopiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="c97c8-121">On the playback side, a DRM-enabled application must be able to obtain licenses for protected content, to decrypt that content using the key contained in the license, and to enforce the license restrictions, such as the number of times a file may be played, or whether the file can be copied to another device.</span></span> <span data-ttu-id="c97c8-122">Das Windows Media-Format SDK bietet alle erforderlichen Unterstützung zum Erstellen einer vollständig aktivierten DRM-Wiedergabe Anwendung.</span><span class="sxs-lookup"><span data-stu-id="c97c8-122">The Windows Media Format SDK provides all the support required to create a fully enabled DRM playback application.</span></span>

> [!Note]  
> <span data-ttu-id="c97c8-123">DRM wird von der x64-basierten Version dieses SDK nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c97c8-123">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="c97c8-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c97c8-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c97c8-125">**Features digitaler Rights Management**</span><span class="sxs-lookup"><span data-stu-id="c97c8-125">**Digital Rights Management Features**</span></span>](digital-rights-management-features.md)
</dt> <dt>

[<span data-ttu-id="c97c8-126">**Aktivieren DRM-Unterstützung**</span><span class="sxs-lookup"><span data-stu-id="c97c8-126">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> </dl>

 

 




