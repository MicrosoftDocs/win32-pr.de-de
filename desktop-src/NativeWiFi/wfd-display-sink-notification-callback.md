---
description: Definiert die Rückruffunktion&\# 8212, die Sie in Ihrer APP implementieren&\# 8212;, die für die wfdstartdisplaysink-Funktion angegeben wurde.
ms.assetid: 0D4C00FD-4ED6-4F0F-BB72-0A1FCC05DB37
title: WFD_DISPLAY_SINK_NOTIFICATION_CALLBACK Callback-Funktion (WF-Sink. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFD_DISPLAY_SINK_NOTIFICATION_CALLBACK
api_type:
- UserDefined
api_location:
- wfdsink.h
ms.openlocfilehash: c576f88a5b7f97484647c4c06f44522a5c3c379f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353439"
---
# <a name="wfd_display_sink_notification_callback-callback-function"></a><span data-ttu-id="09033-103">WFD \_ - \_ \_ Benachrichtigungs \_ Rückruf-Rückruffunktion</span><span class="sxs-lookup"><span data-stu-id="09033-103">WFD\_DISPLAY\_SINK\_NOTIFICATION\_CALLBACK callback function</span></span>

<span data-ttu-id="09033-104">Die **WFD \_ - \_ \_ Benachrichtigungs \_ Rückruffunktion zeigt** die Rückruffunktion an – die Sie in Ihrer APP implementieren –, die für die [**wfdstartdisplaysink**](wfdstartdisplaysink.md) -Funktion angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="09033-104">The **WFD\_DISPLAY\_SINK\_NOTIFICATION\_CALLBACK** function defines the callback function—which you implement in your app—that was specified to the [**WFDStartDisplaySink**](wfdstartdisplaysink.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="09033-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="09033-105">Syntax</span></span>


```C++
DWORD CALLBACK WFD_DISPLAY_SINK_NOTIFICATION_CALLBACK(
  _In_opt_          PVOID                                 pvContext,
  _In_        const PWFD_DISPLAY_SINK_NOTIFICATION        pNotification,
  _Inout_opt_       PWFD_DISPLAY_SINK_NOTIFICATION_RESULT pNotificationResult
);
```



## <a name="parameters"></a><span data-ttu-id="09033-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="09033-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09033-107">*pvcontext* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="09033-107">*pvContext* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="09033-108">Ein optionaler Kontext Zeiger, der an die Rückruffunktion übermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="09033-108">An optional context pointer passed to the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="09033-109">*pnotification* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="09033-109">*pNotification* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09033-110">Ein Zeiger auf eine Struktur, die Daten über die Anzeige Senke Benachrichtigung enthält.</span><span class="sxs-lookup"><span data-stu-id="09033-110">A pointer to a struct containing data about the display sink notification.</span></span>

</dd> <dt>

<span data-ttu-id="09033-111">*pnotificationresult* \[ in, out, optional\]</span><span class="sxs-lookup"><span data-stu-id="09033-111">*pNotificationResult* \[in, out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="09033-112">Ein Zeiger auf eine Struktur mit Daten, die von Ihrer APP optional festgelegt werden können, um das Ergebnis der Verarbeitung der Benachrichtigung über die Anzeige Senke anzugeben.</span><span class="sxs-lookup"><span data-stu-id="09033-112">A pointer to a struct containing data that your app can optionally set to indicate the result of processing the display sink notification.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="09033-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="09033-113">Requirements</span></span>



| <span data-ttu-id="09033-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="09033-114">Requirement</span></span> | <span data-ttu-id="09033-115">Wert</span><span class="sxs-lookup"><span data-stu-id="09033-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="09033-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="09033-116">Minimum supported client</span></span><br/> | <span data-ttu-id="09033-117">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="09033-117">Windows 8.1 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="09033-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="09033-118">Minimum supported server</span></span><br/> | <span data-ttu-id="09033-119">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="09033-119">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="09033-120">Header</span><span class="sxs-lookup"><span data-stu-id="09033-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="09033-121"><dt>WF-Senke. h</dt></span><span class="sxs-lookup"><span data-stu-id="09033-121"><dt>Wfdsink.h</dt></span></span> </dl> |



 

 




