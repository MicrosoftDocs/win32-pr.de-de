---
title: Verwenden des Kontext Parameters
description: Verwenden des Kontext Parameters
ms.assetid: 50e37c36-0ce1-4abd-bb25-f18bb164fdeb
keywords:
- Windows Media-Format-SDK, Kontext Parameter
- Windows Media-Format-SDK, pvcontext-Parameter
- pvcontext-Parameter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 084d7ac0f58d3f3e19ae6b1d6f990a1867988bcd
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104101242"
---
# <a name="using-the-context-parameter"></a><span data-ttu-id="a47d0-106">Verwenden des Kontext Parameters</span><span class="sxs-lookup"><span data-stu-id="a47d0-106">Using the Context Parameter</span></span>

<span data-ttu-id="a47d0-107">Einige der vom Windows Media Format SDK verwendeten Rückrufe akzeptieren einen Parameter namens *pvcontext*.</span><span class="sxs-lookup"><span data-stu-id="a47d0-107">Some of the callbacks used by the Windows Media Format SDK take a parameter called *pvContext*.</span></span> <span data-ttu-id="a47d0-108">Die aufrufenden Objekte übergeben den Wert, den Sie in der Methode angeben, die mit der asynchronen Aktion begonnen hat.</span><span class="sxs-lookup"><span data-stu-id="a47d0-108">The calling objects pass along the value you specify in the method that began the asynchronous action.</span></span> <span data-ttu-id="a47d0-109">Wenn Sie z. b. [**iwmreader:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open)aufgerufen haben, können Sie einen Wert für *pvcontext* übergeben.</span><span class="sxs-lookup"><span data-stu-id="a47d0-109">For example, when you call [**IWMReader::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open), you can pass a value for *pvContext*.</span></span> <span data-ttu-id="a47d0-110">Wenn die [**iwmstatuscallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) -Methode vom Reader-Objekt aufgerufen wird, um die Anwendung zu benachrichtigen, dass die Datei geöffnet wurde, übergibt Sie den Wert, den Sie in Ihrem Aufruf zum **Öffnen** als *pvcontext* -Parameter von **OnStatus** verwendet haben.</span><span class="sxs-lookup"><span data-stu-id="a47d0-110">When the [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) method is called by the reader object to notify your application that the file has been opened, it will pass whatever value you used in your call to **Open** as the *pvContext* parameter of **OnStatus**.</span></span> <span data-ttu-id="a47d0-111">Dieser Kontext Parameter wird für ihre Verwendung bereitgestellt und kann in beliebiger Weise verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a47d0-111">This context parameter is provided for your use and you can use it in any way you like.</span></span>

<span data-ttu-id="a47d0-112">Der *pvcontext* -Parameter wird am häufigsten verwendet, wenn mehrere Objekte denselben Rückruf gemeinsam verwenden müssen.</span><span class="sxs-lookup"><span data-stu-id="a47d0-112">The *pvContext* parameter is most often used when multiple objects need to share the same callback.</span></span> <span data-ttu-id="a47d0-113">Mehrere-Objekte verwenden z. b. die [**iwmstatuscallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) -Methode.</span><span class="sxs-lookup"><span data-stu-id="a47d0-113">For example, several objects use the [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) method.</span></span> <span data-ttu-id="a47d0-114">Sie können *pvcontext* verwenden, damit die verschiedenen Objekte eine Implementierung von **OnStatus** freigeben können, indem Sie einen anderen Wert für *pvcontext* für den ursprünglichen-Befehl übergeben.</span><span class="sxs-lookup"><span data-stu-id="a47d0-114">You can use *pvContext* to enable the different objects to share one implementation of **OnStatus** by passing a different value for *pvContext* on your original call.</span></span> <span data-ttu-id="a47d0-115">In ihrer Implementierung von **OnStatus** können Sie die Logik zur Verarbeitung von Nachrichten basierend auf dem Wert von *pvcontext* verzweigen.</span><span class="sxs-lookup"><span data-stu-id="a47d0-115">In your implementation of **OnStatus**, you can branch the message handling logic based on the value of *pvContext*.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a47d0-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a47d0-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a47d0-117">**Verwenden der Rückruf Methoden**</span><span class="sxs-lookup"><span data-stu-id="a47d0-117">**Using the Callback Methods**</span></span>](using-the-callback-methods.md)
</dt> </dl>

 

 




