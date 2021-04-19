---
description: Tritt auf, wenn die Antwortdaten empfangen werden.
ms.assetid: 7245725b-40dd-4282-b681-f0b2c191db94
title: 'Iwinhttprequestevents:: onresponserstart-Ereignis'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a299c535dd854bff07f2c24989096f7b9e49fc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360643"
---
# <a name="iwinhttprequesteventsonresponsestart-event"></a><span data-ttu-id="b56d8-103">Iwinhttprequestevents:: onresponserstart-Ereignis</span><span class="sxs-lookup"><span data-stu-id="b56d8-103">IWinHttpRequestEvents::OnResponseStart event</span></span>

<span data-ttu-id="b56d8-104">Das **onresponanstart** -Ereignis tritt auf, wenn die Antwortdaten empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="b56d8-104">The **OnResponseStart** event occurs when the response data starts to be received.</span></span>

## <a name="syntax"></a><span data-ttu-id="b56d8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b56d8-105">Syntax</span></span>


```C++
void OnResponseStart(
  [in] long Status,
  [in] BSTR ContentType
);
```



## <a name="parameters"></a><span data-ttu-id="b56d8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b56d8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b56d8-107">*Status* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b56d8-107">*Status* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b56d8-108">Empfängt den Standardstatus Code, der mit den Antwortdaten zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="b56d8-108">Receives the standard status code returned with the response data.</span></span> <span data-ttu-id="b56d8-109">Status Codes werden in [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt)definiert.</span><span class="sxs-lookup"><span data-stu-id="b56d8-109">Status codes are defined in [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span></span>

</dd> <dt>

<span data-ttu-id="b56d8-110">*ContentType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b56d8-110">*ContentType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b56d8-111">Gibt den Typ des empfangenen Inhalts an, z. b. "Text/HTML" oder "image/gif".</span><span class="sxs-lookup"><span data-stu-id="b56d8-111">Specifies the type of content received, such as "text/html" or "image/gif".</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b56d8-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b56d8-112">Return value</span></span>

<span data-ttu-id="b56d8-113">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="b56d8-113">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b56d8-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b56d8-114">Remarks</span></span>

<span data-ttu-id="b56d8-115">Damit dieses Ereignis auftritt, verwenden Sie [**Open**](iwinhttprequest-open.md) , um eine HTTP-Verbindung im asynchronen Modus zu senden, und senden Sie mit [**Send**](iwinhttprequest-send.md) eine Daten Anforderung an einen Internet Server.</span><span class="sxs-lookup"><span data-stu-id="b56d8-115">For this event to occur, use [**Open**](iwinhttprequest-open.md) to send an HTTP connection in asynchronous mode and use [**Send**](iwinhttprequest-send.md) to send a data request to an Internet server.</span></span>

<span data-ttu-id="b56d8-116">Dies ist das erste WinHTTP-Ereignis, das nach dem [**senden**](iwinhttprequest-send.md)auftritt.</span><span class="sxs-lookup"><span data-stu-id="b56d8-116">This is the first WinHTTP event to occur after the [**Send**](iwinhttprequest-send.md).</span></span>

> [!Note]  
> <span data-ttu-id="b56d8-117">Informationen zu Windows XP und Windows 2000 finden Sie im Abschnitt [Lauf Zeitanforderungen](winhttp-start-page.md) auf der WinHTTP-Start Seite.</span><span class="sxs-lookup"><span data-stu-id="b56d8-117">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b56d8-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b56d8-118">Requirements</span></span>



| <span data-ttu-id="b56d8-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b56d8-119">Requirement</span></span> | <span data-ttu-id="b56d8-120">Wert</span><span class="sxs-lookup"><span data-stu-id="b56d8-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="b56d8-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b56d8-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b56d8-122">Windows XP, Windows 2000 Professional mit SP3 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b56d8-122">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="b56d8-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b56d8-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b56d8-124">Windows Server 2003, Windows 2000-Server mit \[ nur SP3-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b56d8-124">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="b56d8-125">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="b56d8-125">Redistributable</span></span><br/>          | <span data-ttu-id="b56d8-126">WinHTTP 5,0 und Internet Explorer 5,01 oder höher unter Windows XP und Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="b56d8-126">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="b56d8-127">IDL</span><span class="sxs-lookup"><span data-stu-id="b56d8-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b56d8-128"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b56d8-128"><dt>HttpRequest.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b56d8-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b56d8-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b56d8-130">**Iwinhttprequestevents**</span><span class="sxs-lookup"><span data-stu-id="b56d8-130">**IWinHttpRequestEvents**</span></span>](iwinhttprequestevents-interface.md)
</dt> <dt>

[<span data-ttu-id="b56d8-131">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="b56d8-131">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="b56d8-132">WinHTTP-Versionen</span><span class="sxs-lookup"><span data-stu-id="b56d8-132">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




