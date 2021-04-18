---
title: Anzeigen oder Ändern des Musik Signals (veraltet)
description: Anzeigen oder Ändern des Musik Signals (veraltet)
ms.assetid: 47150951-2ab5-4cbe-ae57-4ebd23943f1d
keywords:
- Windows Media-Format-SDK, Microsoft Secure-Audiopfad (SAP)
- Digital Rights Management (DRM), Microsoft Secure-Audiopfad (SAP)
- DRM (Digital Rights Management), Microsoft Secure-Audiopfad (SAP)
- Windows Media-Format-SDK, sicherer Audiopfad (SAP)
- Digital Rights Management (DRM), sicherer Audiopfad (SAP)
- DRM (Digital Rights Management), sicherer Audiopfad (SAP)
- Windows Media-Format-SDK, anzeigen oder Ändern von Musik Signalen
- Digital Rights Management (DRM), anzeigen oder Ändern von Musik Signalen
- DRM (Digital Rights Management), anzeigen oder Ändern von Musik Signalen
- Microsoft Secure-Audiopfad (SAP), anzeigen oder Ändern von Musik Signalen
- Sicherer Audiopfad (SAP), anzeigen oder Ändern von Musik Signalen
- SAP (sicherer Audiopfad), anzeigen oder Ändern von Musik Signalen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 673038c9769301d2820cd73e4a090b5e4770fc4a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338617"
---
# <a name="viewing-or-modifying-the-music-signal-deprecated"></a><span data-ttu-id="6642e-115">Anzeigen oder Ändern des Musik Signals (veraltet)</span><span class="sxs-lookup"><span data-stu-id="6642e-115">Viewing or Modifying the Music Signal (deprecated)</span></span>

<span data-ttu-id="6642e-116">Diese Seite dokumentiert eine Funktion, die in zukünftigen Versionen von Windows mit einer anderen technischen Lösung unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="6642e-116">This page documents a feature that will be supported with a different technical solution in future versions of Windows.</span></span>

<span data-ttu-id="6642e-117">Im Microsoft Secure audiopath (SAP)-Modell können Anwendungen geschützte Musik in keiner Weise ändern.</span><span class="sxs-lookup"><span data-stu-id="6642e-117">In the Microsoft Secure Audio Path (SAP) model, applications cannot modify protected music in any way.</span></span> <span data-ttu-id="6642e-118">Wenn eine Anwendung z. b. versucht, ein Musiksignal abzufangen, klingt das Signal wie zufälliges Rauschen.</span><span class="sxs-lookup"><span data-stu-id="6642e-118">For example, when an application attempts to intercept a music signal, the signal sounds like random noise.</span></span> <span data-ttu-id="6642e-119">Folglich können Anwendungen, die in der Regel Signale ändern (z. b. ein Equalizer), den Sound der Musik nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="6642e-119">As a result, applications that normally modify signals (such as an equalizer) cannot change the sound of the music.</span></span>

<span data-ttu-id="6642e-120">Bei einigen Anwendungen wird lediglich ein Musiksignal angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6642e-120">Some applications merely view a music signal.</span></span> <span data-ttu-id="6642e-121">Beispielsweise zeigen einige Anwendungen blinkende Beleuchtung rechtzeitig mit dem Musiksignal an, aber ändern Sie Sie nicht.</span><span class="sxs-lookup"><span data-stu-id="6642e-121">For example, some applications display flashing lights in time with the music signal, but do not modify it.</span></span> <span data-ttu-id="6642e-122">Um Anwendungen, die Signale anzeigen, zu unterstützen, wird ein kleiner Teil der Musik entschlüsselt und als Klartext mit dem verschlüsselten Inhalt übermittelt.</span><span class="sxs-lookup"><span data-stu-id="6642e-122">To accommodate applications that view signals, a small part of the music is decrypted and passed in clear form with the encrypted content.</span></span> <span data-ttu-id="6642e-123">Das resultierende Signal ist sehr schlecht (schlimmer als die Telefonqualität), kann aber für Anwendungen, die Signale anzeigen, ausreichen.</span><span class="sxs-lookup"><span data-stu-id="6642e-123">The resulting signal is very poor (worse than telephone quality) but can suffice for applications that view signals.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6642e-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6642e-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6642e-125">**Microsoft Secure-Audiopfad**</span><span class="sxs-lookup"><span data-stu-id="6642e-125">**Microsoft Secure Audio Path**</span></span>](microsoft-secure-audio-path--deprecated.md)
</dt> </dl>

 

 




