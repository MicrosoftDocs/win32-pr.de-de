---
description: Auflisten von Geräten und Filtern
ms.assetid: 334bba2a-7477-4115-9ce0-d4495c1fc290
title: Auflisten von Geräten und Filtern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e69997a4af4f3160f0b338bc9c595adea83a5354
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860408"
---
# <a name="enumerating-devices-and-filters"></a><span data-ttu-id="db626-103">Auflisten von Geräten und Filtern</span><span class="sxs-lookup"><span data-stu-id="db626-103">Enumerating Devices and Filters</span></span>

<span data-ttu-id="db626-104">Manchmal muss eine Anwendung einen bestimmten Filter im System des Benutzers suchen.</span><span class="sxs-lookup"><span data-stu-id="db626-104">Sometimes an application needs to locate a particular filter on the user's system.</span></span> <span data-ttu-id="db626-105">Beispielsweise wird in einer Video Erfassungs Anwendung möglicherweise eine Liste der verfügbaren Erfassungsgeräte angezeigt.</span><span class="sxs-lookup"><span data-stu-id="db626-105">For example, a video capture application might display a list of available capture devices.</span></span> <span data-ttu-id="db626-106">Da DirectShow eine komponentenbasierte Architektur verwendet, können Sie zur Entwurfszeit nicht wissen, welche Filter auf dem System des Benutzers installiert werden.</span><span class="sxs-lookup"><span data-stu-id="db626-106">Because DirectShow uses a component-based architecture, you cannot know at design time which filters are installed on the user's system.</span></span> <span data-ttu-id="db626-107">Dies gilt insbesondere für Filter, die Hardware Geräte darstellen.</span><span class="sxs-lookup"><span data-stu-id="db626-107">This is particularly true for filters that represent hardware devices.</span></span> <span data-ttu-id="db626-108">DirectShow bietet zwei Komponenten, die registrierte Filter finden:</span><span class="sxs-lookup"><span data-stu-id="db626-108">DirectShow provides two components that locate registered filters:</span></span>

-   <span data-ttu-id="db626-109">Der [Enumerator für System Geräte](system-device-enumerator.md) findet Filter nach ihrer Kategorie.</span><span class="sxs-lookup"><span data-stu-id="db626-109">The [System Device Enumerator](system-device-enumerator.md) finds filters by their category.</span></span>
-   <span data-ttu-id="db626-110">Der [Filter Mapper](filter-mapper.md) findet Filter gemäß den Suchkriterien, die von der Anwendung bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="db626-110">The [Filter Mapper](filter-mapper.md) finds filters according to search criteria supplied by the application.</span></span>

<span data-ttu-id="db626-111">Die in diesem Abschnitt erläuterten Enumeratoren befolgen das Standardformular, das von com-enumerationsschnittstellen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="db626-111">The enumerators discussed in this section follow the standard form used by COM enumeration interfaces.</span></span> <span data-ttu-id="db626-112">Weitere Informationen finden Sie im Thema "IEnumXXXX" im Microsoft Platform Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="db626-112">For more information, see the "IEnumXXXX" topic in the Microsoft Platform Software Development Kit (SDK).</span></span>

<span data-ttu-id="db626-113">Dieser Abschnitt enthält die folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="db626-113">This section contains the following topics:</span></span>

-   [<span data-ttu-id="db626-114">Verwenden des Enumerators für System Geräte</span><span class="sxs-lookup"><span data-stu-id="db626-114">Using the System Device Enumerator</span></span>](using-the-system-device-enumerator.md)
-   [<span data-ttu-id="db626-115">Verwenden des Filter Mappers</span><span class="sxs-lookup"><span data-stu-id="db626-115">Using the Filter Mapper</span></span>](using-the-filter-mapper.md)

## <a name="related-topics"></a><span data-ttu-id="db626-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="db626-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="db626-117">Grundlegende DirectShow-Aufgaben</span><span class="sxs-lookup"><span data-stu-id="db626-117">Basic DirectShow Tasks</span></span>](basic-directshow-tasks.md)
</dt> </dl>

 

 



