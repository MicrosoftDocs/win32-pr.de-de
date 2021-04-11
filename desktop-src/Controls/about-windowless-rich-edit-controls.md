---
title: Informationen zu fensterlosen Bearbeitungs Steuerelementen
description: Ein fensterloses Rich Edit-Steuerelement, das auch als Text Dienste-Objekt bezeichnet wird, ist ein Objekt, das die Funktionalität eines Rich-Edit-Steuer Elements bereitstellt, ohne das Fenster bereitzustellen.
ms.assetid: 880a704d-776a-49d3-be31-0328af408e3b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc1c8bc685dff5f8ddb041011089a84eb2e12008
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103949135"
---
# <a name="about-windowless-rich-edit-controls"></a><span data-ttu-id="e4971-103">Informationen zu fensterlosen Bearbeitungs Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="e4971-103">About Windowless Rich Edit Controls</span></span>

<span data-ttu-id="e4971-104">Ein fensterloses Rich Edit-Steuerelement, das auch als Text Dienste-Objekt bezeichnet wird, ist ein Objekt, das die Funktionalität eines [Rich-Edit-Steuer](rich-edit-controls.md) Elements bereitstellt, ohne das Fenster bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="e4971-104">A windowless rich edit control, also known as a text services object, is an object that provides the functionality of a [rich edit control](rich-edit-controls.md) without providing the window.</span></span> <span data-ttu-id="e4971-105">Um die Funktionalität eines Fensters bereitzustellen, z. b. die Fähigkeit, Nachrichten zu empfangen, und einen Gerätekontext, in dem Sie gezeichnet werden kann, verwenden fensterlose Rich Edit-Steuerelemente ein Schnittstellen Paar: [**itextservices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) und [**itexthost**](/windows/desktop/api/Textserv/nl-textserv-itexthost).</span><span class="sxs-lookup"><span data-stu-id="e4971-105">To provide the functionality of a window, such as the ability to receive messages and a device context into which it can draw, windowless rich edit controls use a pair of interfaces: [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) and [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost).</span></span>

<span data-ttu-id="e4971-106">Um ein fensterloses Bearbeitungs Steuerelement zu erstellen, rufen Sie [**die Funktion "**](/windows/desktop/api/Textserv/nf-textserv-createtextservices) -Funktion" mit einem Zeiger auf die Implementierung der [**itexthost**](/windows/desktop/api/Textserv/nl-textserv-itexthost) -Schnittstelle auf.</span><span class="sxs-lookup"><span data-stu-id="e4971-106">To create a windowless rich edit control, call the [**CreateTextServices**](/windows/desktop/api/Textserv/nf-textserv-createtextservices) function with a pointer to your implementation of the [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost) interface.</span></span> <span data-ttu-id="e4971-107">" **Kreatetextservices** " gibt einen [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Zeiger zurück, den Sie Abfragen können, um einen Zeiger auf die [**itextservices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) -Implementierung des fensterlosen Steuer Elements abzurufen.</span><span class="sxs-lookup"><span data-stu-id="e4971-107">**CreateTextServices** returns an [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pointer that you can query to retrieve a pointer to the [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) implementation of the windowless control.</span></span>

<span data-ttu-id="e4971-108">Msftedit.dll exportiert eine Schnittstellen-ID (IID) namens **IID \_ itextservices** , die Sie verwenden können, um den [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Zeiger für die [**itextservices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) -Schnittstelle abzufragen.</span><span class="sxs-lookup"><span data-stu-id="e4971-108">Msftedit.dll exports an interface identifier (IID) called **IID\_ITextServices** that you can use to query the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pointer for the [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) interface.</span></span> <span data-ttu-id="e4971-109">Im folgenden Beispiel wird gezeigt, wie **IID \_ itextservices** abgerufen und zum Abrufen der **itextservices** -Schnittstelle verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e4971-109">The following example shows how to retrieve **IID\_ITextServices** and use it to get the **ITextServices** interface.</span></span>


```
    .
    .
    .
    HRESULT hr;
    IUnknown* pUnk = NULL;
    ITextServices* pTextServices =  NULL;
    
    // Create an instance of the application-defined object that implements the 
    // ITextHost interface.
    TextHost* pTextHost = new TextHost();
    if (pTextHost == NULL) 
        goto errorHandler;

    // Create an instance of the text services object.
    hr = CreateTextServices(NULL, pTextHost, &pUnk);
    if (FAILED(hr))
        goto errorHandler;
        
    // Retrieve the IID_ITextServices interface identifier from 
    // Msftedit.dll. The hmodRichEdit parameter is a handle to the 
    // Msftedit.dll module retrieved by a previous call to the 
    // GetModuleHandle function.
    IID* pIID_ITS = (IID*) (VOID*) GetProcAddress(hmodRichEdit, 
        "IID_ITextServices");
               
    // Retrieve the ITextServices interface.    
    hr = pUnk->QueryInterface(*pIID_ITS, (void **)&pTextServices);
    if (FAILED(hr))
        goto errorHandler;
     .
     . 
     .   
     
```



<span data-ttu-id="e4971-110">Msftedit.dll exportiert außerdem eine Schnittstellen-ID (IID) namens **IID \_ itexthost** , die auf ähnliche Weise verwendet werden kann, um die [**itexthost**](/windows/desktop/api/Textserv/nl-textserv-itexthost) -Schnittstelle abzufragen.</span><span class="sxs-lookup"><span data-stu-id="e4971-110">Msftedit.dll also exports an interface identifier (IID) called **IID\_ITextHost** that can be used in a similar manner to query for the [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost) interface.</span></span>

<span data-ttu-id="e4971-111">Die [**itexthost**](/windows/desktop/api/Textserv/nl-textserv-itexthost) -Schnittstelle verfügt über Methoden, die vom fensterlosen Steuerelement aufgerufen werden, um Informationen zu Ihrem Fenster abzurufen.</span><span class="sxs-lookup"><span data-stu-id="e4971-111">The [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost) interface has methods that the windowless control calls to retrieve information about your window.</span></span> <span data-ttu-id="e4971-112">Beispielsweise ruft das Text Services-Objekt die [**txgetdc**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txgetdc) -Methode auf, um einen Gerätekontext abzurufen, in den er gezeichnet werden kann.</span><span class="sxs-lookup"><span data-stu-id="e4971-112">For example, the text services object calls the [**TxGetDC**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txgetdc) method to retrieve a device context into which it can draw.</span></span> <span data-ttu-id="e4971-113">Das fensterlose Steuerelement ruft die [**txnotify**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txnotify) -Methode auf, um Benachrichtigungen (z. b. die Rich-Edit-Benachrichtigungs Meldungen) an den texthost zu senden.</span><span class="sxs-lookup"><span data-stu-id="e4971-113">The windowless control calls the [**TxNotify**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txnotify) method to send notifications, such as the rich edit notification messages, to the text host.</span></span> <span data-ttu-id="e4971-114">Das Text Services-Objekt ruft andere **itexthost** -Methoden auf, um den texthost zum Ausführen anderer Fenster bezogener Dienste aufzufordern.</span><span class="sxs-lookup"><span data-stu-id="e4971-114">The text services object calls other **ITextHost** methods to request the text host to perform other window-related services.</span></span> <span data-ttu-id="e4971-115">Beispielsweise fordert die [**txinvalidatup**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txinvalidaterect) -Methode den texthost zum Hinzufügen eines Rechtecks zum Aktualisierungs Bereich des Fensters auf.</span><span class="sxs-lookup"><span data-stu-id="e4971-115">For example, the [**TxInvalidateRect**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txinvalidaterect) method requests the text host to add a rectangle to the window's update region.</span></span>

<span data-ttu-id="e4971-116">Ein Standardmäßiges Bearbeitungs Steuerelement verfügt über eine Fenster Prozedur, mit der Systemmeldungen und Nachrichten von der Anwendung verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="e4971-116">A standard rich edit control has a window procedure that processes system messages and messages from your application.</span></span> <span data-ttu-id="e4971-117">Sie können das Fenster Handle des Steuer Elements verwenden, um IT-Nachrichten zum Durchführen von Textbearbeitung und anderen Vorgängen zu senden.</span><span class="sxs-lookup"><span data-stu-id="e4971-117">You can use the control's window handle to send it messages for performing text editing and other operations.</span></span> <span data-ttu-id="e4971-118">Ein fensterloses Steuerelement für die Bearbeitung von Fenstern hat jedoch keine Fenster Prozedur zum empfangen und Verarbeiten von Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="e4971-118">But a windowless rich edit control has no window procedure to receive and process messages.</span></span> <span data-ttu-id="e4971-119">Stattdessen wird eine [**itextservices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) -Schnittstelle bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="e4971-119">Instead, it provides an [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) interface.</span></span> <span data-ttu-id="e4971-120">Zum Senden von Nachrichten an ein fensterloses Rich-Edit-Steuerelement wird die [**txsendmessage**](/windows/desktop/api/Textserv/nf-textserv-itextservices-txsendmessage) -Methode aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="e4971-120">To send messages to a windowless rich edit control, call the [**TxSendMessage**](/windows/desktop/api/Textserv/nf-textserv-itextservices-txsendmessage) method.</span></span> <span data-ttu-id="e4971-121">Mit dieser Methode können Sie jede der Rich Edit-Nachrichten senden oder andere Nachrichten übergeben, die sich auf das Steuerelement auswirken, z. b. Systemmeldungen für Maus-oder Tastatureingaben.</span><span class="sxs-lookup"><span data-stu-id="e4971-121">You can use this method to send any of the rich edit messages or to pass on other messages that affect the control, such as system messages for mouse or keyboard input.</span></span>

<span data-ttu-id="e4971-122">Sie können das Objekt "Text Dienste" auch als Teil eines [com-aggregierten Objekts](/windows/desktop/com/aggregation)erstellen.</span><span class="sxs-lookup"><span data-stu-id="e4971-122">You can also create the text services object as part of a [COM-aggregated object](/windows/desktop/com/aggregation).</span></span> <span data-ttu-id="e4971-123">Dies vereinfacht das Aggregieren des Text Services-Objekts mit einem COM-Objekt (Windows less Component Object Model).</span><span class="sxs-lookup"><span data-stu-id="e4971-123">This makes it easy to aggregate the text services object with a windowless Component Object Model (COM) object.</span></span>

 

 