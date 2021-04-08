---
title: Verwenden des OnStatus-Rückrufs
description: Verwenden des OnStatus-Rückrufs
ms.assetid: 598e2d13-709b-42a3-ae06-b8c7d208ca9e
keywords:
- Windows Media-Format-SDK, OnStatus-Rückruf Methode
- Windows Media-Format-SDK, iwmstatus Callback-Schnittstelle
- OnStatus-Rückruf Methode, Informationen zu
- Iwmstatus Callback
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56e96b8d7fd75fd8a1d97a56c8b09304c51d0238
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "103948412"
---
# <a name="using-the-onstatus-callback"></a><span data-ttu-id="dd40f-107">Verwenden des OnStatus-Rückrufs</span><span class="sxs-lookup"><span data-stu-id="dd40f-107">Using the OnStatus Callback</span></span>

<span data-ttu-id="dd40f-108">Die [**iwmstatuscallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) -Rückruf Methode wird von mehreren Objekten im Windows Media-Format-SDK aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="dd40f-108">The [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) callback method is called by several objects in the Windows Media Format SDK.</span></span> <span data-ttu-id="dd40f-109">**OnStatus** empfängt Nachrichten, die Änderungen am Status von SDK-Vorgängen darstellen.</span><span class="sxs-lookup"><span data-stu-id="dd40f-109">**OnStatus** receives messages that represent changes in the status of SDK operations.</span></span>

<span data-ttu-id="dd40f-110">Um die **OnStatus** -Rückruf Methode verwenden zu können, müssen Sie eine Klasse in der Anwendung implementieren, die von der [**iwmstatuscallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) -Schnittstelle erbt.</span><span class="sxs-lookup"><span data-stu-id="dd40f-110">To use the **OnStatus** callback method, you must implement a class in your application that inherits from the [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) interface.</span></span> <span data-ttu-id="dd40f-111">Fügen Sie Code für Ihre Version von **OnStatus** in der-Klasse ein.</span><span class="sxs-lookup"><span data-stu-id="dd40f-111">Include code for your version of **OnStatus** in the class.</span></span> <span data-ttu-id="dd40f-112">Einige Beispiele für **OnStatus** -Implementierungen finden Sie in den Beispielen, die in diesem SDK enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="dd40f-112">Several examples of **OnStatus** implementations can be found in the samples included with this SDK.</span></span> <span data-ttu-id="dd40f-113">Weitere Informationen zu den Beispielen finden Sie unter [Beispielanwendungen](sample-applications.md).</span><span class="sxs-lookup"><span data-stu-id="dd40f-113">For more information about the samples, see [Sample Applications](sample-applications.md).</span></span>

<span data-ttu-id="dd40f-114">Sie müssen die Implementierung des Status Rückrufs verschiedenen Objekten des Windows Media Format SDK zuordnen.</span><span class="sxs-lookup"><span data-stu-id="dd40f-114">You must associate your implementation of the status callback with various objects of the Windows Media Format SDK.</span></span> <span data-ttu-id="dd40f-115">Jedes-Objekt verfügt über eine andere Möglichkeit, diese Zuordnung vorzunehmen.</span><span class="sxs-lookup"><span data-stu-id="dd40f-115">Each object has a different way of making this association.</span></span> <span data-ttu-id="dd40f-116">Eine Liste der Methoden, die bestimmte Objekte zuordnen, finden Sie auf der Referenzseite zu **iwmstatus Callback** .</span><span class="sxs-lookup"><span data-stu-id="dd40f-116">For a list of the methods that associate specific objects, see the **IWMStatusCallback** reference page.</span></span>

<span data-ttu-id="dd40f-117">Die Statusmeldungen, die von **OnStatus** empfangen werden können, werden im [**WMT- \_ statusenumerationstyp**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) definiert.</span><span class="sxs-lookup"><span data-stu-id="dd40f-117">The status messages that can be received by **OnStatus** are defined in the [**WMT\_STATUS**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) enumeration type.</span></span>

<span data-ttu-id="dd40f-118">Sie können auswählen, welche Nachrichten abgefangen und welche ignoriert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="dd40f-118">You can choose which messages to trap and which to ignore.</span></span> <span data-ttu-id="dd40f-119">Allerdings ist die Reaktion auf einige Statusmeldungen für bestimmte Features erforderlich.</span><span class="sxs-lookup"><span data-stu-id="dd40f-119">However, responding to some status messages is required for certain features.</span></span> <span data-ttu-id="dd40f-120">Bei Verwendung des asynchronen Readers öffnet die [**iwmreader:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) -Methode z. b. eine Datei asynchron.</span><span class="sxs-lookup"><span data-stu-id="dd40f-120">For example, when using the asynchronous reader, the [**IWMReader::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) method opens a file asynchronously.</span></span> <span data-ttu-id="dd40f-121">Die einzige Möglichkeit, um zu erkennen, wann die Datei geöffnet wurde, ist das Abfangen der geöffneten MWT- \_ Nachricht.</span><span class="sxs-lookup"><span data-stu-id="dd40f-121">The only way to tell when the file has been opened is to trap the MWT\_OPENED message.</span></span> <span data-ttu-id="dd40f-122">In der Regel sind die Nachrichten, auf die Sie Antworten, eine Benachrichtigung über den Abschluss von asynchronen Tasks.</span><span class="sxs-lookup"><span data-stu-id="dd40f-122">Typically, the messages you respond to are notifications of the completion of asynchronous tasks.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dd40f-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="dd40f-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dd40f-124">**Verwenden der Rückruf Methoden**</span><span class="sxs-lookup"><span data-stu-id="dd40f-124">**Using the Callback Methods**</span></span>](using-the-callback-methods.md)
</dt> </dl>

 

 




