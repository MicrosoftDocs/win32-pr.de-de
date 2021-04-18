---
description: Bereitstellen für schnellere Kommunikation
ms.assetid: 9099f9df-b620-4623-826e-c541202ebc4a
title: Bereitstellen für schnellere Kommunikation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2594a7dbd34813013257350e2deb9d93db6bae5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345636"
---
# <a name="deploying-for-faster-communication"></a><span data-ttu-id="f26fa-103">Bereitstellen für schnellere Kommunikation</span><span class="sxs-lookup"><span data-stu-id="f26fa-103">Deploying for Faster Communication</span></span>

<span data-ttu-id="f26fa-104">Die Leistung ist ein wichtiger Aspekt bei der Bereitstellung einer COM+-Anwendung, und der Speicherort der Komponente ist der Schlüssel zum erzielen der besten Leistung einer gut entworfenen Anwendung.</span><span class="sxs-lookup"><span data-stu-id="f26fa-104">Performance is a key consideration when deploying a COM+ application, and component location is the key to getting the best performance from a well-designed application.</span></span>

<span data-ttu-id="f26fa-105">Es war in der Zwischenzeit mit skalierbaren Anwendungsarchitekturen, dass die Leistung durch einfaches Verschieben der primären Komponenten der Anwendung auf schnellere Hardware gelöst werden konnte.</span><span class="sxs-lookup"><span data-stu-id="f26fa-105">It was once widely held that with scalable application architectures, performance could be addressed by simply moving primary components of the application to faster hardware.</span></span> <span data-ttu-id="f26fa-106">Dies hat sich als nicht wahr erwiesen.</span><span class="sxs-lookup"><span data-stu-id="f26fa-106">This has proven not to be true.</span></span> <span data-ttu-id="f26fa-107">Leistungsprobleme treten nicht aus der Leistung einzelner Komponenten, sondern von den Verknüpfungen, die Komponenten verbinden, auf.</span><span class="sxs-lookup"><span data-stu-id="f26fa-107">Performance problems arise not from individual component performance but from the links connecting components.</span></span>

<span data-ttu-id="f26fa-108">Der primäre Faktor für den Erfolg ist die Position.</span><span class="sxs-lookup"><span data-stu-id="f26fa-108">The primary factor for success is location.</span></span> <span data-ttu-id="f26fa-109">Near oder physischer Standort, Zeit, Kapazität und Zweck sind unterschiedliche Aspekte des Standorts, die für die Bereitstellung einer COM+-Anwendung gelten, die sich alle auf die Leistung auswirken.</span><span class="sxs-lookup"><span data-stu-id="f26fa-109">Proximity or physical location, time, capacity, and purpose are distinct aspects of location that apply to the deployment of a COM+ application, all of which affect performance.</span></span>

<span data-ttu-id="f26fa-110">Die beste Leistung ist, wenn die Anwendungskomponenten und-Ressourcen entworfen und bereitgestellt werden, um die Anforderungen zu erfüllen, die von der Arbeitsauslastung der Anwendung auf diese angewendet werden</span><span class="sxs-lookup"><span data-stu-id="f26fa-110">The best performance comes when the application components and resources are designed and deployed to match the demands placed upon them by the application workload.</span></span>

<span data-ttu-id="f26fa-111">Im Allgemeinen sollten Sie Komponenten bereitstellen, um prozessübergreifende und besonders Computer übergreifende Kommunikation zwischen Komponenten zu minimieren.</span><span class="sxs-lookup"><span data-stu-id="f26fa-111">In general, you should deploy components to minimize cross-process, and especially cross-computer, communication between components.</span></span> <span data-ttu-id="f26fa-112">Wenn ihr Anwendungs Entwurf effizient ist, werden Klassen innerhalb einer Komponente nach Verwendung und Funktion gruppiert, um die Kommunikation innerhalb von Komponenten zu maximieren.</span><span class="sxs-lookup"><span data-stu-id="f26fa-112">If your application design is efficient, classes within a component are grouped by use and function to maximize communications within components.</span></span> <span data-ttu-id="f26fa-113">Beim Bereitstellen von Komponenten müssen Sie sicherstellen, dass sich die Komponenten logisch befinden, um die Beziehungen zwischen den Komponenten zu nutzen und die Menge an Messaging zwischen den Komponenten zu verringern.</span><span class="sxs-lookup"><span data-stu-id="f26fa-113">In deploying components, you need to ensure that the components are logically located to make use of the relationships between the components and to reduce the amount of messaging between components.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f26fa-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f26fa-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f26fa-115">Entwerfen für die Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="f26fa-115">Designing for Deployment</span></span>](designing-for-deployment.md)
</dt> </dl>

 

 



