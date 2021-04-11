---
description: In diesem Abschnitt wird die Verwendung von Umgebungslichtsensor-Daten behandelt und erläutert, wie Benutzeroberflächen Features und Programminhalte für viele Beleuchtungsbedingungen optimiert werden können.
ms.assetid: c84075b2-ae41-4915-a0f6-3a9c017ae0b8
title: Erstellen Light-Aware Benutzeroberflächen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a4b6d404e366cb898114fe61729ab1ad722feb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960253"
---
# <a name="creating-light-aware-user-interfaces"></a><span data-ttu-id="cc60c-103">Erstellen Light-Aware Benutzeroberflächen</span><span class="sxs-lookup"><span data-stu-id="cc60c-103">Creating Light-Aware User Interfaces</span></span>

<span data-ttu-id="cc60c-104">In diesem Abschnitt wird die Verwendung von Umgebungslichtsensor-Daten behandelt und erläutert, wie Benutzeroberflächen Features und Programminhalte für viele Beleuchtungsbedingungen optimiert werden können.</span><span class="sxs-lookup"><span data-stu-id="cc60c-104">This section covers the use of ambient light sensor data, and how user interface features and program content can be optimized for many lighting conditions.</span></span>

<span data-ttu-id="cc60c-105">Umgebungslichtsensoren machen Daten verfügbar, mit denen verschiedene Aspekte der Beleuchtungsbedingungen bestimmt werden können, in denen sich der Sensor befindet.</span><span class="sxs-lookup"><span data-stu-id="cc60c-105">Ambient light sensors expose data that can be used to determine various aspects of the lighting conditions where the sensor is located.</span></span> <span data-ttu-id="cc60c-106">Umgebungslichtsensoren können die Gesamthelligkeit einer Umgebung (Beleuchtung) und andere Aspekte der umgebenden Beleuchtung, wie z. b. die Chromaticity-oder Farbtemperatur, verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="cc60c-106">Ambient light sensors can expose the overall brightness of an environment (illuminance) and other aspects of the surrounding light, such as chromaticity or color temperature.</span></span>

<span data-ttu-id="cc60c-107">Computer können auf verschiedene Arten nützlicher sein, wenn das System auf Beleuchtungsbedingungen reagiert.</span><span class="sxs-lookup"><span data-stu-id="cc60c-107">Computers can be more useful in several ways when the system is responsive to lighting conditions.</span></span> <span data-ttu-id="cc60c-108">Dazu gehört das Steuern der Helligkeit der Computer Anzeige (ein neues, vollständig unterstütztes Feature in Windows 7), das automatische Anpassen der Beleuchtungs Ebene von beleuchteten Tastaturen und sogar der Helligkeitssteuerung für andere Leuchten (z. b. Schaltflächen Beleuchtung, Aktivitäts Beleuchtung usw.).</span><span class="sxs-lookup"><span data-stu-id="cc60c-108">These include controlling the brightness of the computer display (a new, fully supported feature in Windows 7), automatically adjusting the lighting level of illuminated keyboards, and even brightness control for other lights (such as button illumination, activity lights, and so on).</span></span>

<span data-ttu-id="cc60c-109">Endbenutzer Programme können auch von Lichtsensoren profitieren.</span><span class="sxs-lookup"><span data-stu-id="cc60c-109">End-user programs can also benefit from light sensors.</span></span> <span data-ttu-id="cc60c-110">Programme können ein Design anwenden, das für eine bestimmte Beleuchtungs Bedingung geeignet ist, z. b. ein bestimmtes Outdoor-Design und ein spezielles Design.</span><span class="sxs-lookup"><span data-stu-id="cc60c-110">Programs can apply a theme that is appropriate for a particular lighting condition, such as a specific outdoor theme and indoor theme.</span></span> <span data-ttu-id="cc60c-111">Der wichtigste Aspekt der Lichtsensor Integration in Programme sind Optimierungen der Lesbarkeit und Lesbarkeit auf der Grundlage von Beleuchtungsbedingungen.</span><span class="sxs-lookup"><span data-stu-id="cc60c-111">Perhaps the most important aspect of light sensor integration with programs is readability and legibility optimizations that are based on lighting conditions.</span></span>

<span data-ttu-id="cc60c-112">Die Sensor-API ermöglicht es Ihnen, solche Programme zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="cc60c-112">The Sensor API enables you to create such programs.</span></span> <span data-ttu-id="cc60c-113">Stellen Sie sich folgendes Szenario vor:</span><span class="sxs-lookup"><span data-stu-id="cc60c-113">Consider the following scenario.</span></span>

## <a name="scenario-using-your-laptop-to-navigate-to-a-restaurant"></a><span data-ttu-id="cc60c-114">Szenario: Navigieren zu einem Restaurant mithilfe Ihres Laptops</span><span class="sxs-lookup"><span data-stu-id="cc60c-114">Scenario: Using your Laptop to Navigate to a Restaurant</span></span>

<span data-ttu-id="cc60c-115">Angenommen, Sie möchten Ihren Computer verwenden, um zu einem neuen Restaurant zu navigieren.</span><span class="sxs-lookup"><span data-stu-id="cc60c-115">Suppose you want to use your computer to help you navigate to a new restaurant.</span></span> <span data-ttu-id="cc60c-116">Beginnen Sie in Ihrem Haus, und suchen Sie nach der Adresse des Restaurants und der Planung der Route.</span><span class="sxs-lookup"><span data-stu-id="cc60c-116">You start out in your house, looking up the address of the restaurant and planning your route.</span></span> <span data-ttu-id="cc60c-117">Der folgende Screenshot zeigt, wie Ihre Benutzeroberfläche von Ihrem Navigationsprogramm optimiert werden kann, um ausführliche Informationen in den Bereichen der Innenbeleuchtung anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="cc60c-117">The following screen shot shows how your navigation program could optimize its UI to show detailed information in indoor lighting conditions.</span></span>

![Benutzeroberfläche, die für die Innenbeleuchtung konzipiert ist](images/nav-normal.png)

<span data-ttu-id="cc60c-119">Wenn Sie zu Ihrem Auto wechseln, stoßen Sie auf direktes Sonnenlicht. Dadurch wird der Bildschirm des Laptops schwer lesbar.</span><span class="sxs-lookup"><span data-stu-id="cc60c-119">When you go outside to your car, you encounter direct sunlight, which makes the laptop's screen difficult to read.</span></span> <span data-ttu-id="cc60c-120">Der folgende Screenshot zeigt, wie Ihr Programm die Benutzeroberfläche ändern kann, um die Lesbarkeit/Lesbarkeit in direktem Licht zu maximieren.</span><span class="sxs-lookup"><span data-stu-id="cc60c-120">The following screen shot shows how your program could alter its UI to maximize legibility/readability in direct light.</span></span> <span data-ttu-id="cc60c-121">In dieser Ansicht wurde ein Großteil des Details ausgelassen und der Kontrast maximiert.</span><span class="sxs-lookup"><span data-stu-id="cc60c-121">In this view, much of the detail has been omitted and contrast is maximized.</span></span>

![die Benutzeroberfläche für direkte Beleuchtungsbedingungen.](images/nav-contrast.png)

<span data-ttu-id="cc60c-123">Wenn Sie sich näher mit dem Restaurant auskennen, kommt es vor, und es wird nicht mehr angezeigt.</span><span class="sxs-lookup"><span data-stu-id="cc60c-123">As you get closer to the restaurant, evening approaches and it gets dark outside.</span></span> <span data-ttu-id="cc60c-124">Im folgenden Screenshot wurde die Benutzeroberfläche für das Navigationsprogramm für die Anzeige mit geringem Licht optimiert.</span><span class="sxs-lookup"><span data-stu-id="cc60c-124">In the following screen shot, the UI for the navigation program has been optimized for low-light viewing.</span></span> <span data-ttu-id="cc60c-125">Durch die Verwendung von dunkleren Farben insgesamt ist die Benutzeroberfläche auf dem dunklen Fahrzeug leicht zu betrachten.</span><span class="sxs-lookup"><span data-stu-id="cc60c-125">By using darker colors overall, this UI is easy to glance at in the dark car.</span></span>

![die Benutzeroberfläche, die für die Ansicht mit geringem Licht konzipiert](images/nav-lowlight.png)

<span data-ttu-id="cc60c-127">Im restlichen Teil dieses Abschnitts werden einige Dinge erläutert, die Sie tun können, um Ihre Programme für verschiedene Beleuchtungsbedingungen zu optimieren, und wie Sie die Sensor-API verwenden können, um die helle Benutzeroberfläche zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="cc60c-127">In the remainder of this section, you will explore some things that you can do to optimize your programs for various lighting conditions and how you can use the Sensor API to help enable light-aware UI.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="cc60c-128">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="cc60c-128">In This Section</span></span>

-   [<span data-ttu-id="cc60c-129">Grundlagen der Light-Aware Benutzeroberflächen</span><span class="sxs-lookup"><span data-stu-id="cc60c-129">Fundamentals of Light-Aware User Interfaces</span></span>](fundamentals-of-light-aware-user-interfaces.md)
-   [<span data-ttu-id="cc60c-130">Beispiele für Light-Aware Benutzeroberflächen</span><span class="sxs-lookup"><span data-stu-id="cc60c-130">Examples of Light-Aware User Interfaces</span></span>](examples-of-light-aware-user-interfaces.md)
-   [<span data-ttu-id="cc60c-131">Optimieren der Benutzer Leistung</span><span class="sxs-lookup"><span data-stu-id="cc60c-131">Optimizing the User Experience</span></span>](optimizing-the-user-experience.md)
-   [<span data-ttu-id="cc60c-132">Verstehen und Interpretieren von Lux-Werten</span><span class="sxs-lookup"><span data-stu-id="cc60c-132">Understanding and Interpreting Lux Values</span></span>](understanding-and-interpreting-lux-values.md)
-   [<span data-ttu-id="cc60c-133">Verwenden von Licht Sensor Daten</span><span class="sxs-lookup"><span data-stu-id="cc60c-133">Using Light Sensor Data</span></span>](handling-data-from-multiple-light-sensors.md)

 

 



