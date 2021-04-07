---
title: Öffnen und Schließen von Mischungs Geräten
description: Öffnen und Schließen von Mischungs Geräten
ms.assetid: b1943308-3778-485e-80f3-6d80cb583e00
keywords:
- Multimedia-Audiodatei, Öffnen von Mixer-Geräten
- Audiodatei, Öffnen von Mixer-Geräten
- Audiomixer, öffnen
- Mixer, öffnen
- Multimedia-Audiodaten, schließen von Mischungs Geräten
- Audiodatei, schließen von Mischungs Geräten
- Audiomixer, schließen
- Mixer, schließen
- Öffnen von Mischgerät Geräten
- Schließen von Mischungs Geräten
- Geräte Bezeichner im Vergleich zu Geräte Handles
- audiomischern, Geräte Bezeichner und Geräte Handles
- Mischern, Geräte Bezeichner und Geräte Handles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea2be7fcc0563508aabfd957109d62c7dbfe1c1a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038838"
---
# <a name="opening-and-closing-mixer-devices"></a><span data-ttu-id="373d1-116">Öffnen und Schließen von Mischungs Geräten</span><span class="sxs-lookup"><span data-stu-id="373d1-116">Opening and Closing Mixer Devices</span></span>

<span data-ttu-id="373d1-117">Wenn Sie ein Mischgerät verwenden möchten, können Sie es entweder einfach verwenden, oder Sie können das Gerät explizit öffnen, bevor Sie es verwenden.</span><span class="sxs-lookup"><span data-stu-id="373d1-117">When you want to use a mixer device, you can either simply begin using it or you can explicitly open the device before using it.</span></span> <span data-ttu-id="373d1-118">Das explizite Öffnen eines Mischgerät bietet zwei wesentliche Vorteile:</span><span class="sxs-lookup"><span data-stu-id="373d1-118">Explicitly opening a mixer device offers two main benefits:</span></span>

-   <span data-ttu-id="373d1-119">Dadurch wird sichergestellt, dass dieses Mischungs Gerät weiterhin vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="373d1-119">It guarantees the continued existence of that mixer device.</span></span>
-   <span data-ttu-id="373d1-120">Es ermöglicht Ihnen das Empfangen von Benachrichtigungen über audiozeilen und das Steuern von Änderungen.</span><span class="sxs-lookup"><span data-stu-id="373d1-120">It lets you receive notification of audio line and control changes.</span></span>

<span data-ttu-id="373d1-121">Sie können die [**mixeropen**](/windows/win32/api/mmeapi/nf-mmeapi-mixeropen) -Funktion verwenden, um ein Mischgerät explizit zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="373d1-121">You can use the [**mixerOpen**](/windows/win32/api/mmeapi/nf-mmeapi-mixeropen) function to explicitly open a mixer device.</span></span> <span data-ttu-id="373d1-122">Diese Funktion übernimmt als Parameter einen Geräte Bezeichner, einen Zeiger auf einen Speicherort und andere Werte, die für die einzelnen Gerätetypen eindeutig sind.</span><span class="sxs-lookup"><span data-stu-id="373d1-122">This function takes as parameters a device identifier, a pointer to a memory location, and other values unique to each type of device.</span></span> <span data-ttu-id="373d1-123">Der Speicherort wird mit einem Geräte handle gefüllt.</span><span class="sxs-lookup"><span data-stu-id="373d1-123">The memory location is filled with a device handle.</span></span> <span data-ttu-id="373d1-124">Verwenden Sie dieses Geräte handle, um das Open-Mixer-Gerät zu identifizieren, wenn andere audiomischfunktionen aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="373d1-124">Use this device handle to identify the open mixer device when calling other audio mixer functions.</span></span> <span data-ttu-id="373d1-125">Solange ein Handle eines Mixer-Geräts vorhanden ist, ist das Gerät weiterhin im System vorhanden.</span><span class="sxs-lookup"><span data-stu-id="373d1-125">As long as a handle of a mixer device exists, the device continues to exist in the system.</span></span> <span data-ttu-id="373d1-126">Wenn eine Konfigurationsänderung für das Mischgerät erfolgt und es nicht explizit geöffnet wurde, kann die Anwendung plötzlich nicht mehr darauf zugreifen.</span><span class="sxs-lookup"><span data-stu-id="373d1-126">If a configuration change occurs to the mixer device and it hasn't been explicitly opened, your application might suddenly be unable to access it.</span></span>

> [!Note]  
> <span data-ttu-id="373d1-127">Der Unterschied zwischen Geräte bezeichatoren und Geräte Handles ist wichtig.</span><span class="sxs-lookup"><span data-stu-id="373d1-127">The difference between device identifiers and device handles is important.</span></span> <span data-ttu-id="373d1-128">Geräte Handles werden zurückgegeben, wenn Sie einen Gerätetreiber mithilfe von **mixeropen** öffnen.</span><span class="sxs-lookup"><span data-stu-id="373d1-128">Device handles are returned when you open a device driver by using **mixerOpen**.</span></span> <span data-ttu-id="373d1-129">Geräte Bezeichner werden implizit von der Anzahl von Geräten, die in einem System vorhanden sind, bestimmt. Diese Zahl wird mithilfe der Funktion [**mixergetnumentvs**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetnumdevs) abgerufen.</span><span class="sxs-lookup"><span data-stu-id="373d1-129">Device identifiers are determined implicitly from the number of devices present in a system; this number is obtained by using the [**mixerGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetnumdevs) function.</span></span>

 

<span data-ttu-id="373d1-130">Sie können die [**mixerclose**](/windows/win32/api/mmeapi/nf-mmeapi-mixerclose) -Funktion verwenden, um ein Mischgerät zu schließen.</span><span class="sxs-lookup"><span data-stu-id="373d1-130">You can use the [**mixerClose**](/windows/win32/api/mmeapi/nf-mmeapi-mixerclose) function to close a mixer device.</span></span> <span data-ttu-id="373d1-131">Sie sollten das Gerät schließen, nachdem Sie es verwendet haben.</span><span class="sxs-lookup"><span data-stu-id="373d1-131">You should close the device after you finish using it.</span></span>

 

 