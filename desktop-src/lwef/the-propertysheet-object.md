---
title: Das PropertySheet-Objekt
description: Das PropertySheet-Objekt
ms.assetid: 9d15d198-a4fe-4c05-a7be-0807a179cd9c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90ae4ded2625440ba34170df605b60287f105800
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100675"
---
# <a name="the-propertysheet-object"></a><span data-ttu-id="0f4eb-103">Das PropertySheet-Objekt</span><span class="sxs-lookup"><span data-stu-id="0f4eb-103">The PropertySheet Object</span></span>

<span data-ttu-id="0f4eb-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="0f4eb-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="0f4eb-105">Das [**PropertySheet**](https://www.bing.com/search?q=**PropertySheet**) -Objekt bietet verschiedene Eigenschaften, die Sie verwenden können, wenn Sie das Zeichen relativ zum Microsoft-Agent-Eigenschaften Blatt (auch als Fenster für erweiterte Zeichen Optionen bezeichnet) bearbeiten möchten.</span><span class="sxs-lookup"><span data-stu-id="0f4eb-105">The [**PropertySheet**](https://www.bing.com/search?q=**PropertySheet**) object provides several properties you can use if you want to manipulate the character relative to the Microsoft Agent property sheet (also known as the Advanced Character Options window).</span></span>

-   [<span data-ttu-id="0f4eb-106">**Höhe**</span><span class="sxs-lookup"><span data-stu-id="0f4eb-106">**Height**</span></span>](height-property-pso.md)
-   [<span data-ttu-id="0f4eb-107">**Linken**</span><span class="sxs-lookup"><span data-stu-id="0f4eb-107">**Left**</span></span>](left-property-pso.md)
-   [<span data-ttu-id="0f4eb-108">**Seite**</span><span class="sxs-lookup"><span data-stu-id="0f4eb-108">**Page**</span></span>](page-property.md)
-   [<span data-ttu-id="0f4eb-109">**Nach oben**</span><span class="sxs-lookup"><span data-stu-id="0f4eb-109">**Top**</span></span>](top-property-pso.md)
-   [<span data-ttu-id="0f4eb-110">**Sichtbar**</span><span class="sxs-lookup"><span data-stu-id="0f4eb-110">**Visible**</span></span>](visible-property.md)
-   [<span data-ttu-id="0f4eb-111">**Breite**</span><span class="sxs-lookup"><span data-stu-id="0f4eb-111">**Width**</span></span>](width-property-pso.md)

<span data-ttu-id="0f4eb-112">Wenn Sie die Eigenschaften [**height**](height-property-pso.md), [**left**](left-property-pso.md), [**Top**](top-property-pso.md)und [**Width**](width-property-pso.md) Abfragen, bevor das Eigenschaften Blatt angezeigt wird, geben die Werte als NULL (0) zurück.</span><span class="sxs-lookup"><span data-stu-id="0f4eb-112">If you query [**Height**](height-property-pso.md), [**Left**](left-property-pso.md), [**Top**](top-property-pso.md), and [**Width**](width-property-pso.md) properties before the property sheet has ever been shown, their values return as zero (0).</span></span> <span data-ttu-id="0f4eb-113">Wenn diese Eigenschaften angezeigt werden, geben Sie die letzte Position und Größe des Fensters zurück (relativ zur aktuellen Bildschirmauflösung).</span><span class="sxs-lookup"><span data-stu-id="0f4eb-113">Once shown, these properties return the last position and size of the window (relative to your current screen resolution).</span></span>

 

 




