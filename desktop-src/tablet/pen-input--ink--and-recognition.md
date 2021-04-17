---
description: Ein interessantes neues Feature von Tablet PC ist das Stift Eingabe System.
ms.assetid: 8432617a-5ae7-44cb-a5f7-f3b2d8885846
title: Stift Eingabe, frei Hand Eingabe und-Erkennung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a46d865e40d1779edaa2607b1754c45659609b5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104558705"
---
# <a name="pen-input-ink-and-recognition"></a><span data-ttu-id="35592-103">Stift Eingabe, frei Hand Eingabe und-Erkennung</span><span class="sxs-lookup"><span data-stu-id="35592-103">Pen Input, Ink, and Recognition</span></span>

<span data-ttu-id="35592-104">Ein interessantes neues Feature von Tablet PC ist das Stift Eingabe System.</span><span class="sxs-lookup"><span data-stu-id="35592-104">One interesting new feature of Tablet PC is the pen input system.</span></span> <span data-ttu-id="35592-105">Alle Tablet PC-Computer verfügen unter dem Bildschirm über einen Digitalisierer, der Stift Eingaben akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="35592-105">All Tablet PC computers have a digitizer beneath the screen that accepts pen input.</span></span> <span data-ttu-id="35592-106">Dieser neue Eingabe Mechanismus erfordert, dass Sie sich Gedanken über das Erstellen von Anwendungen speziell für Tablet PC machen müssen.</span><span class="sxs-lookup"><span data-stu-id="35592-106">This new input mechanism requires you to think about how to build applications specifically for Tablet PC.</span></span> <span data-ttu-id="35592-107">Die Tablet PC Platform-API (Application Programming Interface) hilft Ihnen dabei, dies zu tun.</span><span class="sxs-lookup"><span data-stu-id="35592-107">The Tablet PC platform application programming interface (API) helps you do this.</span></span>

## <a name="collection-data-management-and-recognition"></a><span data-ttu-id="35592-108">Erfassung, Datenverwaltung und Erkennung</span><span class="sxs-lookup"><span data-stu-id="35592-108">Collection, Data Management, and Recognition</span></span>

<span data-ttu-id="35592-109">Die Tablet PC-Plattform kann in drei verschiedene Bereiche unterteilt werden:</span><span class="sxs-lookup"><span data-stu-id="35592-109">The Tablet PC platform can be divided into three distinct areas:</span></span>

-   <span data-ttu-id="35592-110">Ink-Auflistung (Objekte, die verwendet werden, um frei Hand Eingaben vom Digitalisierer zu erfassen).</span><span class="sxs-lookup"><span data-stu-id="35592-110">Ink collection (objects that are used to collect ink from the digitizer).</span></span>
-   <span data-ttu-id="35592-111">Frei Hand Datenverwaltung (Objekte, die zum Verwalten der gesammelten frei Hand Eingaben verwendet werden).</span><span class="sxs-lookup"><span data-stu-id="35592-111">Ink data management (objects that are used to manage the collected ink).</span></span>
-   <span data-ttu-id="35592-112">Frei Handerkennung (-Objekte, die zum Konvertieren der gesammelten frei Hand Eingaben in andere Datentypen verwendet werden, z. b. Text).</span><span class="sxs-lookup"><span data-stu-id="35592-112">Ink recognition (objects that are used to convert the collected ink into other types of data, such as text).</span></span>

<span data-ttu-id="35592-113">Die folgende Abbildung zeigt, wie die frei Hand Sammlungs-API (Pen API), die frei Hand Datenverwaltung-API (Ink-API) und die frei Hand Erkennungs-API (Erkennungs-API) auf der Tablet PC-Plattform zusammenarbeiten.</span><span class="sxs-lookup"><span data-stu-id="35592-113">The following image shows, at a high level, how the Ink Collection API (Pen API), Ink Data Management API (Ink API), and Ink Recognition API (Recognition API) work together in the Tablet PC platform.</span></span>

![illustraton zeigt, wie die Stift-API, die frei Hand-API und die Erkennungs-API zusammenarbeiten](images/aabc298b-fd64-435b-87bc-eb7cd11524e8.jpg)

<span data-ttu-id="35592-115">Die Tablet PC Platform-API ist sowohl in verwalteten APIs als auch in einer COM-Bibliothek verfügbar.</span><span class="sxs-lookup"><span data-stu-id="35592-115">The Tablet PC platform API is available in Managed APIs as well as a COM library.</span></span> <span data-ttu-id="35592-116">In den folgenden Themen werden die Objekte in der API beschrieben und veranschaulicht, wie Anwendungen diese Objekte verwenden:</span><span class="sxs-lookup"><span data-stu-id="35592-116">The following topics describe the objects in the API and illustrate how applications use these objects:</span></span>

-   [<span data-ttu-id="35592-117">Ink-Auflistung</span><span class="sxs-lookup"><span data-stu-id="35592-117">Ink Collection</span></span>](ink-collection.md)
-   [<span data-ttu-id="35592-118">Frei Hand Daten</span><span class="sxs-lookup"><span data-stu-id="35592-118">Ink Data</span></span>](ink-data.md)
-   [<span data-ttu-id="35592-119">Frei Handerkennung</span><span class="sxs-lookup"><span data-stu-id="35592-119">Ink Recognition</span></span>](ink-recognition.md)
-   [<span data-ttu-id="35592-120">Ink-Analyse</span><span class="sxs-lookup"><span data-stu-id="35592-120">Ink Analysis</span></span>](ink-analysis.md)
-   [<span data-ttu-id="35592-121">Handschrifterkennung in Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="35592-121">Handwriting Recognition in Windows Server 2008 R2</span></span>](handwriting-recognition-in-windows-server-2008-r2.md)

 

 



