---
description: Zusammenfassung der überlappenden Vervollständigungs Anzeige Mechanismen im SPI von Windows Sockets (Winsock).
ms.assetid: 2306b884-7d3a-4002-928e-54537571e5f8
title: Zusammenfassung der Überlapp enden Vervollständigungs Anzeige Mechanismen in der SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c20e78f38e35638f29376cb0807d4eedabbe9164
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129116"
---
# <a name="summary-of-overlapped-completion-indication-mechanisms-in-the-spi"></a><span data-ttu-id="3f9eb-103">Zusammenfassung der Überlapp enden Vervollständigungs Anzeige Mechanismen in der SPI</span><span class="sxs-lookup"><span data-stu-id="3f9eb-103">Summary of Overlapped Completion Indication Mechanisms in the SPI</span></span>

<span data-ttu-id="3f9eb-104">In der folgenden Tabelle wird die Vervollständigungs Semantik für einen überlappenden Socket zusammengefasst, wobei die verschiedenen Kombinationen von *lpoverllapp*, **hevent** und *lpCompletionRoutine* angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="3f9eb-104">The following table summarizes the completion semantics for an overlapped socket, showing the various combination of *lpOverlapped*, **hEvent**, and *lpCompletionRoutine*.</span></span>



| <span data-ttu-id="3f9eb-105">*lpoverlgetauscht*</span><span class="sxs-lookup"><span data-stu-id="3f9eb-105">*lpOverlapped*</span></span> | <span data-ttu-id="3f9eb-106">**hevent**</span><span class="sxs-lookup"><span data-stu-id="3f9eb-106">**hEvent**</span></span>     | <span data-ttu-id="3f9eb-107">*lpCompletionRoutine*</span><span class="sxs-lookup"><span data-stu-id="3f9eb-107">*lpCompletionRoutine*</span></span> | <span data-ttu-id="3f9eb-108">Vervollständigungs Angabe</span><span class="sxs-lookup"><span data-stu-id="3f9eb-108">Completion indication</span></span>                                                                                                                                                                                                        |
|----------------|----------------|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f9eb-109">NULL</span><span class="sxs-lookup"><span data-stu-id="3f9eb-109">NULL</span></span>           | <span data-ttu-id="3f9eb-110">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="3f9eb-110">Not applicable</span></span> | <span data-ttu-id="3f9eb-111">Wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="3f9eb-111">Ignored</span></span>               | <span data-ttu-id="3f9eb-112">Der Vorgang wird synchron abgeschlossen, d. h. er verhält sich wie ein nicht überlappenden Socket.</span><span class="sxs-lookup"><span data-stu-id="3f9eb-112">Operation completes synchronously, that is, it behaves as if it were a nonoverlapped socket.</span></span>                                                                                                                                 |
| <span data-ttu-id="3f9eb-113">nicht NULL</span><span class="sxs-lookup"><span data-stu-id="3f9eb-113">not NULL</span></span>       | <span data-ttu-id="3f9eb-114">NULL</span><span class="sxs-lookup"><span data-stu-id="3f9eb-114">NULL</span></span>           | <span data-ttu-id="3f9eb-115">NULL</span><span class="sxs-lookup"><span data-stu-id="3f9eb-115">NULL</span></span>                  | <span data-ttu-id="3f9eb-116">Der Vorgang wird überlappen abgeschlossen, aber es gibt keinen von Windows Sockets 2 unterstützten Abschlussmechanismus.</span><span class="sxs-lookup"><span data-stu-id="3f9eb-116">Operation completes overlapped, but there is no Windows Sockets 2-supported completion mechanism.</span></span> <span data-ttu-id="3f9eb-117">Der Mechanismus für den Abschluss Port (falls unterstützt) kann in diesem Fall verwendet werden, andernfalls wird keine Vervollständigungs Benachrichtigung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3f9eb-117">The completion port mechanism (if supported) may be used in this case, otherwise there will be no completion notification.</span></span> |
| <span data-ttu-id="3f9eb-118">nicht NULL</span><span class="sxs-lookup"><span data-stu-id="3f9eb-118">not NULL</span></span>       | <span data-ttu-id="3f9eb-119">nicht NULL</span><span class="sxs-lookup"><span data-stu-id="3f9eb-119">not NULL</span></span>       | <span data-ttu-id="3f9eb-120">NULL</span><span class="sxs-lookup"><span data-stu-id="3f9eb-120">NULL</span></span>                  | <span data-ttu-id="3f9eb-121">Der Vorgang wird überlappende Benachrichtigungen durch Signalisieren von Ereignis Objekten abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="3f9eb-121">Operation completes overlapped, notification by signaling event object.</span></span>                                                                                                                                                      |
| <span data-ttu-id="3f9eb-122">nicht NULL</span><span class="sxs-lookup"><span data-stu-id="3f9eb-122">not NULL</span></span>       | <span data-ttu-id="3f9eb-123">Wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="3f9eb-123">Ignored</span></span>        | <span data-ttu-id="3f9eb-124">nicht NULL</span><span class="sxs-lookup"><span data-stu-id="3f9eb-124">not NULL</span></span>              | <span data-ttu-id="3f9eb-125">Der Vorgang wird überlappende Benachrichtigungen durch Planen der Abschluss Routine abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="3f9eb-125">Operation completes overlapped, notification by scheduling completion routine.</span></span>                                                                                                                                               |



 

 

 



