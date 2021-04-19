---
description: Die cmspthread-Klasse implementiert den MSPs-Arbeits Thread.
ms.assetid: 9dc2373a-cdcf-4e60-95fa-56cb68bda15b
title: Cmspthread
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17a12b71668e81688b5de7f41e188a51b88944d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369013"
---
# <a name="cmspthread"></a><span data-ttu-id="e7372-103">Cmspthread</span><span class="sxs-lookup"><span data-stu-id="e7372-103">CMSPThread</span></span>

<span data-ttu-id="e7372-104">Die **cmspthread** -Klasse implementiert den MSP-Arbeits Thread.</span><span class="sxs-lookup"><span data-stu-id="e7372-104">The **CMSPThread** class implements the MSP's worker thread.</span></span> <span data-ttu-id="e7372-105">Die Basisklassen verwenden diesen Arbeits Thread für eine Reihe von Zwecken.</span><span class="sxs-lookup"><span data-stu-id="e7372-105">The base classes use this worker thread for a number of purposes.</span></span> <span data-ttu-id="e7372-106">Ein generischer und schlanker Arbeits Element Mechanismus wird bereitgestellt, damit der abgeleitete MSP diesen Thread für seine eigenen synchronen oder asynchronen Arbeitsaufgaben verwenden kann, was Sie möglicherweise tun.</span><span class="sxs-lookup"><span data-stu-id="e7372-106">A generic and lightweight work item mechanism is provided to allow the derived MSP to use this thread for its own synchronous or asynchronous work items, whatever they may be.</span></span> <span data-ttu-id="e7372-107">Der Thread pumpt auch Nachrichten und unterstützt die Verarbeitung von APCs (obwohl APCs nicht in den Basisklassen verwendet werden).</span><span class="sxs-lookup"><span data-stu-id="e7372-107">The thread also pumps messages and supports handling of APCs (although APCs are not used in the base classes).</span></span>

<span data-ttu-id="e7372-108">Wenn mehrere like-Adressen vorhanden sind (d. h., wenn dieselbe MSP-Implementierung aus derselben DLL mehrmals instanziiert wird), stellt die Thread Klasse die Skalierbarkeit sicher, indem automatisch ein einzelner Thread für alle Adressen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e7372-108">When multiple like addresses are present (that is, when the same MSP implementation from the same DLL is instantiated multiple times), the thread class ensures scalability by automatically using a single thread for all the addresses.</span></span> <span data-ttu-id="e7372-109">Die Schnittstelle zur Thread Klasse besteht darin, dass die MSP-Implementierung die Thread Klasse als privaten Thread vorstellen kann und die anderen Adressen, die Sie möglicherweise freigeben, nicht wichtig sind.</span><span class="sxs-lookup"><span data-stu-id="e7372-109">The interface to the thread class is such that the MSP implementation can think of the thread class as a private thread and need not care about the other addresses that may be sharing it.</span></span>

<span data-ttu-id="e7372-110">Definiert in "mspthrd. h".</span><span class="sxs-lookup"><span data-stu-id="e7372-110">Defined in MSPthrd.h.</span></span>

 

 



