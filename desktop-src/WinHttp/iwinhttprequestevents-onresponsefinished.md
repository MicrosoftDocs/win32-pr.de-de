---
description: Tritt auf, wenn die Antwortdaten fertig sind.
ms.assetid: 0df2031e-826f-436e-a689-201fa8b5c38f
title: 'Iwinhttprequestevents:: onresponabbeendete-Ereignis'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19d3a596e23028cec0401a21a1ee866ef6e51d9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353570"
---
# <a name="iwinhttprequesteventsonresponsefinished-event"></a><span data-ttu-id="fd7b2-103">Iwinhttprequestevents:: onresponabbeendete-Ereignis</span><span class="sxs-lookup"><span data-stu-id="fd7b2-103">IWinHttpRequestEvents::OnResponseFinished event</span></span>

<span data-ttu-id="fd7b2-104">Das **onresponabcomplete** -Ereignis tritt auf, wenn die Antwortdaten vollständig sind.</span><span class="sxs-lookup"><span data-stu-id="fd7b2-104">The **OnResponseFinished** event occurs when the response data is complete.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd7b2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fd7b2-105">Syntax</span></span>


```C++
void OnResponseFinished();
```



## <a name="parameters"></a><span data-ttu-id="fd7b2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fd7b2-106">Parameters</span></span>

<span data-ttu-id="fd7b2-107">Dieses Ereignis weist keine Parameter auf.</span><span class="sxs-lookup"><span data-stu-id="fd7b2-107">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fd7b2-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fd7b2-108">Return value</span></span>

<span data-ttu-id="fd7b2-109">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="fd7b2-109">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd7b2-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fd7b2-110">Remarks</span></span>

<span data-ttu-id="fd7b2-111">Dieses Ereignis signalisiert, dass alle Antwortdaten, die sich auf die letzte Anforderung beziehen, empfangen wurden.</span><span class="sxs-lookup"><span data-stu-id="fd7b2-111">This event signals that all of the response data that pertains to the most recent request has been received.</span></span> <span data-ttu-id="fd7b2-112">" [**Onresponondataavailable**](iwinhttprequestevents-onresponsedataavailable.md) " tritt bis zur nächsten Anforderung nicht wieder auf.</span><span class="sxs-lookup"><span data-stu-id="fd7b2-112">[**OnResponseDataAvailable**](iwinhttprequestevents-onresponsedataavailable.md) does not occur again until the next request.</span></span>

> [!Note]  
> <span data-ttu-id="fd7b2-113">Informationen zu Windows XP und Windows 2000 finden Sie im Abschnitt [Lauf Zeitanforderungen](winhttp-start-page.md) auf der WinHTTP-Start Seite.</span><span class="sxs-lookup"><span data-stu-id="fd7b2-113">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="fd7b2-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fd7b2-114">Requirements</span></span>



| <span data-ttu-id="fd7b2-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fd7b2-115">Requirement</span></span> | <span data-ttu-id="fd7b2-116">Wert</span><span class="sxs-lookup"><span data-stu-id="fd7b2-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd7b2-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fd7b2-117">Minimum supported client</span></span><br/> | <span data-ttu-id="fd7b2-118">Windows XP, Windows 2000 Professional mit SP3 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fd7b2-118">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="fd7b2-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fd7b2-119">Minimum supported server</span></span><br/> | <span data-ttu-id="fd7b2-120">Windows Server 2003, Windows 2000-Server mit \[ nur SP3-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fd7b2-120">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="fd7b2-121">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="fd7b2-121">Redistributable</span></span><br/>          | <span data-ttu-id="fd7b2-122">WinHTTP 5,0 und Internet Explorer 5,01 oder höher unter Windows XP und Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="fd7b2-122">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="fd7b2-123">IDL</span><span class="sxs-lookup"><span data-stu-id="fd7b2-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="fd7b2-124"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="fd7b2-124"><dt>HttpRequest.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd7b2-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fd7b2-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd7b2-126">**Iwinhttprequestevents**</span><span class="sxs-lookup"><span data-stu-id="fd7b2-126">**IWinHttpRequestEvents**</span></span>](iwinhttprequestevents-interface.md)
</dt> <dt>

[<span data-ttu-id="fd7b2-127">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="fd7b2-127">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="fd7b2-128">WinHTTP-Versionen</span><span class="sxs-lookup"><span data-stu-id="fd7b2-128">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




