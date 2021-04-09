---
description: Interoperabilität mit Legacy-audioapis
ms.assetid: 34939f6d-a6e4-4f7a-afa3-b1fed52b471f
title: Interoperabilität mit Legacy-audioapis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a6b9a80b55695ffcfd3ac54e871f00ea27744d8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958505"
---
# <a name="interoperability-with-legacy-audio-apis"></a><span data-ttu-id="76b00-103">Interoperabilität mit Legacy-audioapis</span><span class="sxs-lookup"><span data-stu-id="76b00-103">Interoperability with Legacy Audio APIs</span></span>

<span data-ttu-id="76b00-104">Viele vorhandene Anwendungen verwenden ältere Audio-APIs, wie z. b. DirectSound, DirectShow und die Multimedia-Funktionen von Windows.</span><span class="sxs-lookup"><span data-stu-id="76b00-104">Many existing applications use legacy audio APIs such as DirectSound, DirectShow, and the Windows multimedia functions.</span></span> <span data-ttu-id="76b00-105">Mit nur geringfügigen Änderungen können diese Anwendungen erweitert werden, um [Geräte Rollen](device-roles.md), [Sitzungs-volumesteuerelemente](session-volume-controls.md)und andere Features der Kerncode-APIs in Windows Vista zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="76b00-105">With only minor modifications, these applications can be augmented to make use of [device roles](device-roles.md), [session volume controls](session-volume-controls.md), and other features of the core audio APIs in Windows Vista.</span></span>

<span data-ttu-id="76b00-106">Wie im [benutzermodusaudiokomponenten](user-mode-audio-components.md)erläutert, dienen die kernaudioapis als Grundlage für die Erstellung von audioapis auf höherer Ebene.</span><span class="sxs-lookup"><span data-stu-id="76b00-106">As discussed in [User-Mode Audio Components](user-mode-audio-components.md), the core audio APIs serve as the foundation on which higher-level audio APIs are built.</span></span> <span data-ttu-id="76b00-107">In Windows Vista sind audioendpunktgeräte, die von den kernaudio-APIs implementiert werden, auf audioendpunktgeräten, auf die über Legacy-Audio-APIs wie DirectSound [](audio-endpoint-devices.md) und Windows Media **waveoutxxx** -und **waveinixxx** -Funktionen zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="76b00-107">In Windows Vista, the audio devices that applications access through legacy audio APIs such as DirectSound and the Windows media **waveOutXxx** and **waveInXxx** functions are, in fact, [audio endpoint devices](audio-endpoint-devices.md) that are implemented by the core audio APIs.</span></span> <span data-ttu-id="76b00-108">Aufgrund der inhärenten Einschränkungen in den Schnittstellen von Legacy-audioapis kann eine Anwendung über diese Schnittstellen auf einige Funktionen von audioendpunktgeräten zugreifen.</span><span class="sxs-lookup"><span data-stu-id="76b00-108">Because of inherent limitations in the interfaces of legacy audio APIs, an application can access some but not all of the capabilities of audio endpoint devices through these interfaces.</span></span> <span data-ttu-id="76b00-109">In den folgenden Abschnitten werden Techniken zum Erweitern vorhandener Anwendungen beschrieben, indem direkt über die Kerncode-APIs auf zusätzliche Funktionen von audioendpunktgeräten zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="76b00-109">The following sections describe techniques for enhancing existing applications by accessing additional capabilities of audio endpoint devices directly through the core audio APIs.</span></span> <span data-ttu-id="76b00-110">Diese Verbesserungen erfordern in der Regel nur geringfügige Änderungen am vorhandenen Anwendungscode.</span><span class="sxs-lookup"><span data-stu-id="76b00-110">These enhancements typically require only minor changes to the existing application code.</span></span>

<span data-ttu-id="76b00-111">In den folgenden Abschnitten wird beschrieben, wie Features der kernaudioapis in vorhandene Anwendungen integriert werden, die Legacy-audioapis verwenden:</span><span class="sxs-lookup"><span data-stu-id="76b00-111">The following sections describe how to incorporate features of the core audio APIs into existing applications that use legacy audio APIs:</span></span>

-   [<span data-ttu-id="76b00-112">Geräte Rollen für DirectSound-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="76b00-112">Device Roles for DirectSound Applications</span></span>](device-roles-for-directsound-applications.md)
-   [<span data-ttu-id="76b00-113">Geräte Rollen für DirectShow-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="76b00-113">Device Roles for DirectShow Applications</span></span>](device-roles-for-directshow-applications.md)
-   [<span data-ttu-id="76b00-114">Geräte Rollen für ältere Windows-Multimediaanwendungen</span><span class="sxs-lookup"><span data-stu-id="76b00-114">Device Roles for Legacy Windows Multimedia Applications</span></span>](device-roles-for-legacy-windows-multimedia-applications.md)
-   [<span data-ttu-id="76b00-115">Audioereignisse für Legacy-Audioanwendungen</span><span class="sxs-lookup"><span data-stu-id="76b00-115">Audio Events for Legacy Audio Applications</span></span>](audio-events-for-legacy-audio-applications.md)
-   [<span data-ttu-id="76b00-116">Benachrichtigungs Sounds für Legacy-Audioanwendungen</span><span class="sxs-lookup"><span data-stu-id="76b00-116">Notification Sounds for Legacy Audio Applications</span></span>](notification-sounds-for-legacy-audio-applications.md)

## <a name="related-topics"></a><span data-ttu-id="76b00-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="76b00-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="76b00-118">Geräte Rollen</span><span class="sxs-lookup"><span data-stu-id="76b00-118">Device Roles</span></span>](device-roles.md)
</dt> </dl>

 

 



