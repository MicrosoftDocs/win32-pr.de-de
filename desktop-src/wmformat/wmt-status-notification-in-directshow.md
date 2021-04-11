---
title: Ereignis Benachrichtigung WMT_STATUS in DirectShow
description: WMT- \_ Status Ereignis Benachrichtigung in DirectShow
ms.assetid: 6b777c7e-2777-445b-88de-a9a28be6da9c
keywords:
- Windows Media-Format-SDK, Ereignis Benachrichtigungen WMT_STATUS in DirectShow
- Windows Media-Format-SDK, Ereignis Benachrichtigungen
- Windows Media-Format-SDK, DirectShow
- Advanced Systems Format (ASF), WMT_STATUS Ereignis Benachrichtigungen in DirectShow
- ASF (Advanced Systems Format), WMT_STATUS Ereignis Benachrichtigungen in DirectShow
- Advanced Systems Format (ASF), Ereignis Benachrichtigungen
- ASF (Advanced Systems Format), Ereignis Benachrichtigungen
- Advanced Systems Format (ASF), DirectShow
- ASF (Advanced Systems Format), DirectShow
- DirectShow, Ereignis Benachrichtigungen
- DirectShow, WMT_STATUS Ereignis Benachrichtigungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e12c953b2c9b1509ad1b3adc2831d2276fcd474
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104209270"
---
# <a name="wmt_status-event-notification-in-directshow"></a><span data-ttu-id="55379-114">WMT- \_ Status Ereignis Benachrichtigung in DirectShow</span><span class="sxs-lookup"><span data-stu-id="55379-114">WMT\_STATUS Event Notification in DirectShow</span></span>

<span data-ttu-id="55379-115">Sowohl der ASF-Reader als auch der ASF-Writer leiten [**WMT- \_ Status**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) Ereignisse an Anwendungen weiter.</span><span class="sxs-lookup"><span data-stu-id="55379-115">Both the ASF Reader and the ASF Writer forward [**WMT\_STATUS**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) events to applications.</span></span> <span data-ttu-id="55379-116">Der Writer leitet alle derartigen Ereignisse weiter, und der Reader leitet nur die Ereignisse weiter, die sich auf den DRM-Lizenzerwerb beziehen.</span><span class="sxs-lookup"><span data-stu-id="55379-116">The writer forwards all such events, and the reader forwards only those that pertain to DRM license acquisition.</span></span> <span data-ttu-id="55379-117">Um diese Ereignis Benachrichtigungen in Ihrer Anwendung zu erhalten, fügen Sie einen Fall für das **EC \_ WMT- \_ Ereignis** in ihrer Ereignis Behandlungs Funktion hinzu.</span><span class="sxs-lookup"><span data-stu-id="55379-117">To receive these event notifications in your application, add a case for the **EC\_WMT\_EVENT** in your event-handling function.</span></span> <span data-ttu-id="55379-118">Der *lParam1* -Parameter, der dem Ereignis zugeordnet ist, enthält den **WMT- \_ Status** Code (der **WMT- \_ Fehler** sein kann), und lParam2 enthält die [**am \_ WMT- \_ Ereignis \_ Daten**](/previous-versions/windows/desktop/api/evcode/ns-evcode-am_wmt_event_data) , die das **HRESULT** enthalten.</span><span class="sxs-lookup"><span data-stu-id="55379-118">The *lParam1* parameter associated with the event contains the **WMT\_STATUS** code (which can be **WMT\_ERROR**) and lParam2 contains an [**AM\_WMT\_EVENT\_DATA**](/previous-versions/windows/desktop/api/evcode/ns-evcode-am_wmt_event_data) that includes the **HRESULT**.</span></span>

 

 