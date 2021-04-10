---
title: Thread-Manager
description: Der Thread-Manager ist die Basiskomponente des TSF-Managers.
ms.assetid: fd43b4c3-80bb-4118-a880-bdea07022c95
keywords:
- Text Services-Framework (TSF), Thread-Manager
- TSF (Text Dienst Framework), Thread-Manager
- Text Dienste, Thread-Manager
- TSF-aktivierte Anwendungen, Thread-Manager
- Thread-Manager
- TSF-Manager
- Ereignisbenachrichtigungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b29596c5c39267181c6a2c301aede3f15ca7297
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039237"
---
# <a name="thread-manager"></a><span data-ttu-id="60395-110">Thread-Manager</span><span class="sxs-lookup"><span data-stu-id="60395-110">Thread Manager</span></span>

<span data-ttu-id="60395-111">Der Thread-Manager ist die Basiskomponente des TSF-Managers.</span><span class="sxs-lookup"><span data-stu-id="60395-111">The thread manager is the base component of the TSF manager.</span></span> <span data-ttu-id="60395-112">Der Thread-Manager führt häufige Aufgaben aus, die sich auf Anwendungen und Text Dienste (Clients) beziehen.</span><span class="sxs-lookup"><span data-stu-id="60395-112">The thread manager performs common tasks related to both applications and text services (clients).</span></span> <span data-ttu-id="60395-113">Zu diesen Tasks gehören u. a. die Aktivierung und Deaktivierung von TSF-Text Diensten, die Erstellung von Dokument-Managern und die Wartung der ordnungsgemäßen Beziehung zwischen Dokumenten und dem Eingabefokus.</span><span class="sxs-lookup"><span data-stu-id="60395-113">These tasks include, but are not limited to, the activation and deactivation of TSF text services, the creation of document managers, and maintenance of the proper relationship between documents and the input focus.</span></span> <span data-ttu-id="60395-114">Der Thread-Manager wird von der [ITfThreadMgr](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgr) -Schnittstelle definiert.</span><span class="sxs-lookup"><span data-stu-id="60395-114">The thread manager is defined by the [ITfThreadMgr](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgr) interface.</span></span>

<span data-ttu-id="60395-115">Die meisten Schnittstellen und Objekte, die vom TSF-Manager bereitgestellt werden, können mithilfe der Methoden abgerufen werden, die die Thread-Manager-Schnittstelle bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="60395-115">The majority of the interfaces and objects provided by the TSF manager can be obtained using the methods that the thread manager interface provides.</span></span>

## <a name="applications"></a><span data-ttu-id="60395-116">Anwendungen</span><span class="sxs-lookup"><span data-stu-id="60395-116">Applications</span></span>

<span data-ttu-id="60395-117">Eine Anwendung erstellt ein Thread-Manager-Objekt durch Aufrufen von [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) mit CLSID \_ tfthreadmgr.</span><span class="sxs-lookup"><span data-stu-id="60395-117">An application creates a thread manager object by calling [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) with CLSID\_TFThreadMgr.</span></span>

## <a name="text-services"></a><span data-ttu-id="60395-118">Text Dienste</span><span class="sxs-lookup"><span data-stu-id="60395-118">Text Services</span></span>

<span data-ttu-id="60395-119">Ein Text Dienst erhält ein Thread-Manager-Objekt in der [itftextinputprocessor:: Aktivierungs](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessor-activate) -Methode von Text Service.</span><span class="sxs-lookup"><span data-stu-id="60395-119">A text service obtains a thread manager object in the text service [ITfTextInputProcessor::Activate](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessor-activate) method.</span></span>

## <a name="event-notifications"></a><span data-ttu-id="60395-120">Ereignisbenachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="60395-120">Event Notifications</span></span>

<span data-ttu-id="60395-121">Der Thread-Manager stellt auch Ereignis Benachrichtigungen für Clients bereit.</span><span class="sxs-lookup"><span data-stu-id="60395-121">The thread manager also provides event notification to clients.</span></span> <span data-ttu-id="60395-122">In TSF werden Ereignis Benachrichtigungen mithilfe einer Ereignis Senke bereitgestellt, bei der es sich um ein COM-Objekt handelt.</span><span class="sxs-lookup"><span data-stu-id="60395-122">In TSF, event notifications are provided by means of an event sink, which is a COM object.</span></span> <span data-ttu-id="60395-123">Zum Empfangen von Benachrichtigungen vom Thread-Manager implementiert ein Client ein [itfthreadmgreventsink](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgreventsink) -Objekt und installiert die Ereignis Senke.</span><span class="sxs-lookup"><span data-stu-id="60395-123">To receive notifications from the thread manager, a client implements an [ITfThreadMgrEventSink](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgreventsink) object and installs the event sink.</span></span> <span data-ttu-id="60395-124">Die Ereignis Senke wird installiert, indem der Thread-Manager nach IID \_ itfsource abgefragt und [itfsource:: AdviseSink](/windows/desktop/api/Msctf/nf-msctf-itfsource-advisesink) mit IID \_ itfthreadmgreventsink aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="60395-124">The event sink is installed by querying the thread manager for IID\_ITfSource and calling [ITfSource::AdviseSink](/windows/desktop/api/Msctf/nf-msctf-itfsource-advisesink) with IID\_ITfThreadMgrEventSink.</span></span>

## <a name="related-topics"></a><span data-ttu-id="60395-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="60395-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="60395-126">ITfThreadMgr</span><span class="sxs-lookup"><span data-stu-id="60395-126">ITfThreadMgr</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgr)
</dt> <dt>

[<span data-ttu-id="60395-127">CoCreateInstance</span><span class="sxs-lookup"><span data-stu-id="60395-127">CoCreateInstance</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> <dt>

[<span data-ttu-id="60395-128">ITF textinputprocessor:: Aktivierung</span><span class="sxs-lookup"><span data-stu-id="60395-128">ITfTextInputProcessor::Activate</span></span>](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessor-activate)
</dt> <dt>

[<span data-ttu-id="60395-129">Itfthreadmgreventsink</span><span class="sxs-lookup"><span data-stu-id="60395-129">ITfThreadMgrEventSink</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgreventsink)
</dt> <dt>

[<span data-ttu-id="60395-130">ITF Source:: AdviseSink</span><span class="sxs-lookup"><span data-stu-id="60395-130">ITfSource::AdviseSink</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfsource-advisesink)
</dt> </dl>

 

 