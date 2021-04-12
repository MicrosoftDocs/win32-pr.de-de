---
title: Animations Parameter für Client Bereich
description: Das clientbereichsanimations-Flag gibt an, ob der Benutzer Animationen in Benutzeroberflächen Elementen deaktivieren möchte.
ms.assetid: 4a3ec9da-d5ae-4cd9-8222-f02143895ce4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c62e25fdb08022d53cbe9e818a0a1089988cd6a6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104209346"
---
# <a name="client-area-animation-parameter"></a><span data-ttu-id="b5f0f-103">Animations Parameter für Client Bereich</span><span class="sxs-lookup"><span data-stu-id="b5f0f-103">Client area animation parameter</span></span>

<span data-ttu-id="b5f0f-104">Der Animations Parameter für den Client Bereich gibt an, ob der Benutzer Animationen in Benutzeroberflächen Elementen deaktivieren möchte.</span><span class="sxs-lookup"><span data-stu-id="b5f0f-104">The client area animation parameter indicates whether the user wants to disable animations in UI elements.</span></span> <span data-ttu-id="b5f0f-105">Anzeigen von Features wie blinken, blinken, Flimmern und Verschieben von Inhalten kann bei Benutzern mit Foto sensibler Epilepsie zu Angriffen führen.</span><span class="sxs-lookup"><span data-stu-id="b5f0f-105">Display features such as flashing, blinking, flickering, and moving content can cause seizures in users with photo-sensitive epilepsy.</span></span> <span data-ttu-id="b5f0f-106">Mit diesem Parameter können Sie all diese Animationen aktivieren oder deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="b5f0f-106">This parameter enables you to enable or disable all such animations.</span></span>

<span data-ttu-id="b5f0f-107">Anwendungen verwenden die **SPI-Flags \_ getclientareaanimation** und **SPI \_ setclientareaanimation** mit der [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) -Funktion, um Client Bereichs Animationen ein-oder auszuschalten.</span><span class="sxs-lookup"><span data-stu-id="b5f0f-107">Applications use the **SPI\_GETCLIENTAREAANIMATION** and **SPI\_SETCLIENTAREAANIMATION** flags with the [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) function to turn client area animations on or off.</span></span>

 

 