---
title: Entwickeln des Plug-Ins für einen Typ-1-Online Shop
description: Entwickeln des Plug-Ins für einen Typ-1-Online Shop
ms.assetid: 5d38a41f-9859-452b-953f-3449c2b0ce06
keywords:
- Windows Media Player Online Stores, Plug-ins
- Online Stores, Plug-ins
- Typ 1 Online Stores, Plug-ins
- Windows Media Player Online Stores, Aufbau von Plug-ins
- Online Stores, Aufbau von Plug-ins
- Geben Sie 1 Online Stores ein, und entwickeln Sie Plug-ins.
- Windows Media Player Online Stores, iwmpcontentpartner-Schnittstelle
- Online Stores, iwmpcontentpartner-Schnittstelle
- Typ 1 Online Stores, iwmpcontentpartner-Schnittstelle
- Plug-ins, Windows Media Player Online Stores
- Plug-ins, Online Stores
- Plug-ins, Typ 1 Online Stores
- Plug-ins, iwmpcontentpartner-Schnittstelle
- Plug-ins, Gebäude
- Windows Media Player-Plug-ins, geben Sie 1 Online Stores ein.
- Windows Media Player-Plug-ins, Online Stores
- Windows Media Player-Plug-ins, Windows Media Player Online Stores
- Windows Media Player-Plug-ins, iwmpcontentpartner-Schnittstelle
- Windows Media Player-Plug-ins, Gebäude
- Iwmpcontentpartner
- Entwickeln von Plug-ins, eingeben von 1 Online Stores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36272e3497eebc7b5362d793a0ee265d2c3166fc
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "106339044"
---
# <a name="building-the-plug-in-for-a-type-1-online-store"></a><span data-ttu-id="5dc31-124">Entwickeln des Plug-Ins für einen Typ-1-Online Shop</span><span class="sxs-lookup"><span data-stu-id="5dc31-124">Building the Plug-in for a Type 1 Online Store</span></span>

<span data-ttu-id="5dc31-125">Ein Onlinespeicher vom Typ 1 muss ein Plug-in bereitstellen, das die [**iwmpcontentpartner**](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner) -Schnittstelle implementiert.</span><span class="sxs-lookup"><span data-stu-id="5dc31-125">A type 1 online store must provide a plug-in that implements the [**IWMPContentPartner**](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner) interface.</span></span> <span data-ttu-id="5dc31-126">Das Plug-in wird in einem separaten Prozess von Windows Media Player ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5dc31-126">The plug-in runs in a separate process from Windows Media Player.</span></span>

<span data-ttu-id="5dc31-127">Die Schritte zum Erstellen eines Plug-ins, das außerhalb des Prozesses ausgeführt wird, lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="5dc31-127">The steps for creating a plug-in that runs out-of-process are as follows:</span></span>

1.  <span data-ttu-id="5dc31-128">Schreiben Sie Ihr Plug-in so, als wäre es ein Prozess interner com-Server.</span><span class="sxs-lookup"><span data-stu-id="5dc31-128">Write your plug-in as if it were an in-process COM server.</span></span>
2.  <span data-ttu-id="5dc31-129">Erstellen Sie einen **dllersatz** -Registrierungs Eintrag auf dem Computer des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="5dc31-129">Create a **DllSurrogate** registry entry on the user's computer.</span></span> <span data-ttu-id="5dc31-130">Der **dllersatz** -Eintrag informiert die com-Laufzeit darüber, dass das Plug-in in einer Instanz des standardmäßigen dll-Ersatz Zeichens (dllhost.exe) erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5dc31-130">The **DllSurrogate** entry informs the COM runtime that your plug-in should be created in an instance of the default DLL surrogate, dllhost.exe.</span></span>

<span data-ttu-id="5dc31-131">Ausführliche Informationen zum Registrieren des Plug-Ins finden Sie unter [Registrierungsschlüssel und Einträge für den Online Store vom Typ 1](registry-keys-and-entries-for-a-type-1-online-store.md).</span><span class="sxs-lookup"><span data-stu-id="5dc31-131">For detailed information about registering your plug-in, see [Registry Keys and Entries for a Type 1 Online Store](registry-keys-and-entries-for-a-type-1-online-store.md).</span></span>

<span data-ttu-id="5dc31-132">Sie müssen keinen Proxy-oder Stubcode für Ihr Plug-in erstellen.</span><span class="sxs-lookup"><span data-stu-id="5dc31-132">You do not need to create any proxy or stub code for your plug-in.</span></span> <span data-ttu-id="5dc31-133">Alle Marshallingunterstützung wird von Windows Media Player bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="5dc31-133">All of the marshaling support is provided by Windows Media Player.</span></span>

<span data-ttu-id="5dc31-134">Mit dem Assistenten für Online Shop-Plug-Ins können Sie schnell ein Plug-in erstellen, das als Ausgangspunkt fungiert.</span><span class="sxs-lookup"><span data-stu-id="5dc31-134">You can use the online store plug-in wizard to quickly create a plug-in that serves as a starting point.</span></span> <span data-ttu-id="5dc31-135">Weitere Informationen finden Sie unter [Installieren des Plug-in-Assistenten für den Online Shop](installing-the-online-store-plug-in-wizard.md).</span><span class="sxs-lookup"><span data-stu-id="5dc31-135">For more information, see [Installing the Online Store Plug-in Wizard](installing-the-online-store-plug-in-wizard.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5dc31-136">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5dc31-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5dc31-137">**Programmier Handbuch für den Typ 1 Online Stores**</span><span class="sxs-lookup"><span data-stu-id="5dc31-137">**Programming Guide for Type 1 Online Stores**</span></span>](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




