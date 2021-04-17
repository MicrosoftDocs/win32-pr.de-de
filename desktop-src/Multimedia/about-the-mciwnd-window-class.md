---
title: Informationen zur mciwnd-Fenster Klasse
description: Informationen zur mciwnd-Fenster Klasse
ms.assetid: 7dde7346-5853-4c8f-8788-bf74d01ece83
keywords:
- Mciwnd-Fenster Klasse, Informationen zu
- Mciwndcreate-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e459a0e7d93543af126287a776b64130595ad11
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388352"
---
# <a name="about-the-mciwnd-window-class"></a><span data-ttu-id="5989c-105">Informationen zur mciwnd-Fenster Klasse</span><span class="sxs-lookup"><span data-stu-id="5989c-105">About the MCIWnd Window Class</span></span>

<span data-ttu-id="5989c-106">Die mciwnd-Fenster Klasse ist einfach zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="5989c-106">The MCIWnd Window class is easy to use.</span></span> <span data-ttu-id="5989c-107">Durch die Verwendung einer einzelnen Funktion kann [**mciwndcreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) Ihre Anwendung ein Steuerelement erstellen, das jedes Gerät wieder gibt, das die Media Control Interface (MCI) verwendet.</span><span class="sxs-lookup"><span data-stu-id="5989c-107">By using a single function, [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) your application can create a control that plays any device that uses the media control interface (MCI).</span></span> <span data-ttu-id="5989c-108">Zu diesen Geräten gehören CD-Audiodaten, Waveform-Audiodaten, MIDI und Videogeräte.</span><span class="sxs-lookup"><span data-stu-id="5989c-108">These devices include CD audio, waveform-audio, MIDI, and video devices.</span></span>

<span data-ttu-id="5989c-109">Die Automatisierung der Wiedergabe ist auch schnell und einfach.</span><span class="sxs-lookup"><span data-stu-id="5989c-109">Automating playback is also quick and easy.</span></span> <span data-ttu-id="5989c-110">Wenn Sie nur eine Funktion und zwei Makros verwenden, kann eine Anwendung ein mciwnd-Fenster mit dem entsprechenden Medien Gerät erstellen, das Gerät wiedergeben und sowohl das Gerät als auch das Fenster schließen, wenn die Wiedergabe des Inhalts beendet ist.</span><span class="sxs-lookup"><span data-stu-id="5989c-110">Using only one function and two macros, an application can create an MCIWnd window with the appropriate media device, play the device, and close both the device and the window when the content has finished playing.</span></span>

> [!Note]  
> <span data-ttu-id="5989c-111">Einige Geräte spielen Inhalt, der in Dateien gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="5989c-111">Some devices play content that is stored in files.</span></span> <span data-ttu-id="5989c-112">Andere Geräte, z. b. CD-Audiogeräte, geben Inhalte wieder, die auf einem anderen Medium gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="5989c-112">Other devices, such as CD audio devices, play content that is stored in another medium.</span></span> <span data-ttu-id="5989c-113">Aus Gründen der Übersichtlichkeit bezieht sich diese Übersicht auf beide Umstände als "Wiedergabe des Geräts".</span><span class="sxs-lookup"><span data-stu-id="5989c-113">For purposes of clarity, this overview refers to both circumstances as "playing the device."</span></span>

 

 

 




