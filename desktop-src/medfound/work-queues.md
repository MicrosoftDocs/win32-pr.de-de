---
description: In Microsoft Media Foundation ist eine Arbeits Warteschlange eine effiziente Möglichkeit, um asynchrone Vorgänge in einem anderen Thread auszuführen.
ms.assetid: f886d096-b1f5-42e4-8888-501b58bffd50
title: Arbeits Warteschlangen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15b1e5e8a0a3776f718f645550813bf008b38aee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216264"
---
# <a name="work-queues"></a><span data-ttu-id="e9260-103">Arbeits Warteschlangen</span><span class="sxs-lookup"><span data-stu-id="e9260-103">Work Queues</span></span>

<span data-ttu-id="e9260-104">In Microsoft Media Foundation ist eine Arbeits Warteschlange eine effiziente Möglichkeit, um asynchrone Vorgänge in einem anderen Thread auszuführen.</span><span class="sxs-lookup"><span data-stu-id="e9260-104">In Microsoft Media Foundation, a work queue is an efficient way to perform asynchronous operations on another thread.</span></span>

<span data-ttu-id="e9260-105">In diesem Abschnitt werden die folgenden Themen behandelt:</span><span class="sxs-lookup"><span data-stu-id="e9260-105">This section contains the following topics.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e9260-106">Thema</span><span class="sxs-lookup"><span data-stu-id="e9260-106">Topic</span></span></th>
<th><span data-ttu-id="e9260-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e9260-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e9260-108"><a href="using-work-queues.md">Verwenden von Arbeits Warteschlangen</a></span><span class="sxs-lookup"><span data-stu-id="e9260-108"><a href="using-work-queues.md">Using Work Queues</a></span></span></td>
<td><span data-ttu-id="e9260-109">Beschreibt, wie eine Anwendung oder Komponente mithilfe von Arbeits Warteschlangen asynchrone Vorgänge ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="e9260-109">Describes how an application or component can use work queues to perform asynchronous operations.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e9260-110"><a href="writing-an-asynchronous-method.md">Schreiben einer asynchronen Methode</a></span><span class="sxs-lookup"><span data-stu-id="e9260-110"><a href="writing-an-asynchronous-method.md">Writing an Asynchronous Method</a></span></span></td>
<td><span data-ttu-id="e9260-111">Beschreibt, wie eine asynchrone Methode geschrieben wird, die auf das Begin/End-Muster folgt, das in <a href="asynchronous-callback-methods.md">asynchronen Rückruf Methoden</a>beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="e9260-111">Describes how to write an asynchronous method that follows the Begin/End pattern described in <a href="asynchronous-callback-methods.md">Asynchronous Callback Methods</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e9260-112"><a href="custom-asynchronous-result-objects.md">Benutzerdefinierte asynchrone Ergebnis Objekte</a></span><span class="sxs-lookup"><span data-stu-id="e9260-112"><a href="custom-asynchronous-result-objects.md">Custom Asynchronous Result Objects</a></span></span></td>
<td><span data-ttu-id="e9260-113">Beschreibt, wie eine benutzerdefinierte Implementierung der <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult"><strong>imfasynkresult</strong></a> -Schnittstelle erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="e9260-113">Describes how to create a custom implementation of the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult"><strong>IMFAsyncResult</strong></a> interface.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="e9260-114">Die meisten Anwendungen sollten die von <a href="/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult"><strong>MF | ateasynkresult</strong></a>bereitgestellte Aktien Implementierung verwenden.</span><span class="sxs-lookup"><span data-stu-id="e9260-114">Most applications should use the stock implementation provided by <a href="/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult"><strong>MFCreateAsyncResult</strong></a>.</span></span> <span data-ttu-id="e9260-115">Dieses Thema ist für Anwendungen mit erweiterten Anforderungen vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="e9260-115">This topic is for applications with advanced requirements.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e9260-116"><a href="media-foundation-work-queue-and-threading-improvements.md">Arbeits Warteschlangen und Threading</a></span><span class="sxs-lookup"><span data-stu-id="e9260-116"><a href="media-foundation-work-queue-and-threading-improvements.md">Work Queue and Threading Improvements</a></span></span></td>
<td><span data-ttu-id="e9260-117">Beschreibt Verbesserungen in Windows 8 für Arbeits Warteschlangen und Threading in der Media Foundation Plattform.</span><span class="sxs-lookup"><span data-stu-id="e9260-117">Describes improvements in Windows 8 for work queues and threading in the Media Foundation platform.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="e9260-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e9260-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e9260-119">Media Foundation Plattform-APIs</span><span class="sxs-lookup"><span data-stu-id="e9260-119">Media Foundation Platform APIs</span></span>](media-foundation-platform-apis.md)
</dt> </dl>

 

 




