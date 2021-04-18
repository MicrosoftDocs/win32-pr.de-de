---
description: In diesem Abschnitt wird beschrieben, wie Sie Ereignis Referenzseiten (Erps) planen, entwickeln und testen und wie Sie Sie in einem Experten oder Monitor bereitstellen. Weitere Informationen zu Erps und deren Verwendung mit Netzwerkmonitor finden Sie auf der Seite mit der Ereignis Referenz.
ms.assetid: 78d6e8cf-785e-4d5f-a78d-9ef9da9bc3e0
title: Erstellen von Referenzseiten für Experten und Überwachungs Ereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33c84610c7a1088e994fc852c64a7893f73f7909
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106351660"
---
# <a name="creating-expert-and-monitor-event-reference-pages"></a><span data-ttu-id="2b4b3-104">Erstellen von Referenzseiten für Experten und Überwachungs Ereignisse</span><span class="sxs-lookup"><span data-stu-id="2b4b3-104">Creating Expert and Monitor Event Reference Pages</span></span>

<span data-ttu-id="2b4b3-105">In diesem Abschnitt wird beschrieben, wie Sie Ereignis Referenzseiten (Erps) planen, entwickeln und testen und wie Sie Sie in einem Experten oder Monitor bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="2b4b3-105">This section describes how to plan, develop, and test event reference pages (ERPs) and how to deploy them in an expert or monitor.</span></span> <span data-ttu-id="2b4b3-106">Weitere Informationen zu Erps und deren Verwendung mit Netzwerkmonitor finden Sie auf der [Seite mit der Ereignis Referenz](event-reference-page.md).</span><span class="sxs-lookup"><span data-stu-id="2b4b3-106">For information about ERPs and how to use them with Network Monitor, see [Event Reference Page](event-reference-page.md).</span></span>

<span data-ttu-id="2b4b3-107">Zum Entwickeln eines neuen ERP besteht der erste Schritt darin, die Ereignisse zu bestimmen, die individuelle Erps für Ihren benutzerdefinierten [Experten](experts.md) oder [Monitor](monitors.md)erfordern.</span><span class="sxs-lookup"><span data-stu-id="2b4b3-107">To develop a new ERP, the first step is determining the events that require individual ERPs for your custom [expert](experts.md) or [monitor](monitors.md).</span></span> <span data-ttu-id="2b4b3-108">Sie müssen für jedes Ereignis, das Sie in der Netzwerkmonitor Ereignisanzeige anzeigen möchten, separate Erps erstellen.</span><span class="sxs-lookup"><span data-stu-id="2b4b3-108">You must create separate ERPs for each event you wish to display in the Network Monitor Event Viewer.</span></span> <span data-ttu-id="2b4b3-109">Nehmen Sie beispielsweise Folgendes an:</span><span class="sxs-lookup"><span data-stu-id="2b4b3-109">For example, suppose that:</span></span>

-   <span data-ttu-id="2b4b3-110">Sie entwickeln einen Monitor mit dem Namen "Game Monitor" und "Stock Watcher".</span><span class="sxs-lookup"><span data-stu-id="2b4b3-110">You develop a monitor named Game Monitor and Stock Watcher.</span></span>
-   <span data-ttu-id="2b4b3-111">Der Monitor befindet sich in einer Datei namens Gamemon.dll.</span><span class="sxs-lookup"><span data-stu-id="2b4b3-111">The monitor is located in a file called Gamemon.dll.</span></span>
-   <span data-ttu-id="2b4b3-112">Der Monitor generiert zwei Ereignisse, die ausgeführt werden, und meine Internet Aktien-Soars.</span><span class="sxs-lookup"><span data-stu-id="2b4b3-112">The monitor generates two events, Game Running and My Internet Stock Soars.</span></span>
-   <span data-ttu-id="2b4b3-113">Sie planen, zwei Erps, Gamemon1.htm und Gamemon2.htm zu entwickeln.</span><span class="sxs-lookup"><span data-stu-id="2b4b3-113">You plan to develop two ERPs, Gamemon1.htm and Gamemon2.htm.</span></span>

> [!Note]  
> <span data-ttu-id="2b4b3-114">Es ist nicht erforderlich, dass Sie über eine 1:1-Entsprechung von Erps verfügen, um Ereignisse zu überwachen oder zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="2b4b3-114">It's not necessary to have a one-to-one correspondence of ERPs to monitor or expert events.</span></span>

 

<span data-ttu-id="2b4b3-115">Nachdem Sie eine Liste eindeutiger Erps erstellt haben, führen Sie die folgenden Schritte aus, um die einzelnen ERP-Informationen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="2b4b3-115">After you have established a list of unique ERPs, follow these steps to create each ERP.</span></span>

-   <span data-ttu-id="2b4b3-116">[Schreiben Sie das HTML-Quelldokument](writing-an-event-reference-page.md).</span><span class="sxs-lookup"><span data-stu-id="2b4b3-116">[Write the HTML source document](writing-an-event-reference-page.md).</span></span>
-   <span data-ttu-id="2b4b3-117">Speichern Sie die HTML-Quelldatei, [und benennen](naming-an-event-reference-page.md) Sie Sie als eine HTM-Datei.</span><span class="sxs-lookup"><span data-stu-id="2b4b3-117">[Save and name](naming-an-event-reference-page.md) the HTML source file as an .htm file.</span></span>
-   <span data-ttu-id="2b4b3-118">[Testen Sie das ERP](testing-an-event-reference-page.md) mit dem abgeschlossenen Experten oder Monitor.</span><span class="sxs-lookup"><span data-stu-id="2b4b3-118">[Test the ERP](testing-an-event-reference-page.md) with the completed expert or monitor.</span></span>

 

 



