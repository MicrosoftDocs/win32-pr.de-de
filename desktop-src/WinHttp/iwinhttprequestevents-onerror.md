---
description: Tritt auf, wenn in der Anwendung ein Laufzeitfehler auftritt.
ms.assetid: d99400a4-3661-4162-bfd6-8c2a27e0f328
title: 'Iwinhttprequestevents:: OnError-Ereignis'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8582deec90eb6bfc2985460f3127d5c7ee9c01b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960691"
---
# <a name="iwinhttprequesteventsonerror-event"></a><span data-ttu-id="2bd23-103">Iwinhttprequestevents:: OnError-Ereignis</span><span class="sxs-lookup"><span data-stu-id="2bd23-103">IWinHttpRequestEvents::OnError event</span></span>

<span data-ttu-id="2bd23-104">Das **OnError** -Ereignis tritt auf, wenn ein Laufzeitfehler in der Anwendung vorliegt.</span><span class="sxs-lookup"><span data-stu-id="2bd23-104">The **OnError** event occurs when there is a run-time error in the application.</span></span>

## <a name="syntax"></a><span data-ttu-id="2bd23-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2bd23-105">Syntax</span></span>


```C++
void OnError(
  [in] long ErrorNumber,
  [in] BSTR ErrorDescription
);
```



## <a name="parameters"></a><span data-ttu-id="2bd23-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2bd23-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2bd23-107">*Errornumber* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2bd23-107">*ErrorNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2bd23-108">Empfängt den numerischen Wert des Fehlers.</span><span class="sxs-lookup"><span data-stu-id="2bd23-108">Receives the numerical value of the error.</span></span> <span data-ttu-id="2bd23-109">Die unteren 16 Bits dieser Fehlernummer entsprechen einem der in [**Fehlermeldungen**](error-messages.md)aufgeführten Fehler.</span><span class="sxs-lookup"><span data-stu-id="2bd23-109">The lower 16 bits of this error number corresponds to one of the errors listed in [**Error Messages**](error-messages.md).</span></span>

</dd> <dt>

<span data-ttu-id="2bd23-110">*ErrorDescription* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2bd23-110">*ErrorDescription* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2bd23-111">Gibt eine kurze Beschreibung des aufgetretenen Fehlers an.</span><span class="sxs-lookup"><span data-stu-id="2bd23-111">Specifies a short description of the error which occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2bd23-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2bd23-112">Return value</span></span>

<span data-ttu-id="2bd23-113">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="2bd23-113">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2bd23-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2bd23-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="2bd23-115">Informationen zu Windows XP und Windows 2000 finden Sie im Abschnitt [Lauf Zeitanforderungen](winhttp-start-page.md) auf der WinHTTP-Start Seite.</span><span class="sxs-lookup"><span data-stu-id="2bd23-115">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2bd23-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2bd23-116">Requirements</span></span>



| <span data-ttu-id="2bd23-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2bd23-117">Requirement</span></span> | <span data-ttu-id="2bd23-118">Wert</span><span class="sxs-lookup"><span data-stu-id="2bd23-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="2bd23-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2bd23-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2bd23-120">Windows XP, Windows 2000 Professional mit SP3 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2bd23-120">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="2bd23-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2bd23-121">Minimum supported server</span></span><br/> | <span data-ttu-id="2bd23-122">Windows Server 2003, Windows 2000-Server mit \[ nur SP3-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2bd23-122">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="2bd23-123">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="2bd23-123">Redistributable</span></span><br/>          | <span data-ttu-id="2bd23-124">WinHTTP 5,0 und Internet Explorer 5,01 oder höher unter Windows XP und Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="2bd23-124">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="2bd23-125">IDL</span><span class="sxs-lookup"><span data-stu-id="2bd23-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2bd23-126"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2bd23-126"><dt>HttpRequest.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2bd23-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2bd23-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2bd23-128">**Iwinhttprequestevents**</span><span class="sxs-lookup"><span data-stu-id="2bd23-128">**IWinHttpRequestEvents**</span></span>](iwinhttprequestevents-interface.md)
</dt> <dt>

[<span data-ttu-id="2bd23-129">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="2bd23-129">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="2bd23-130">WinHTTP-Versionen</span><span class="sxs-lookup"><span data-stu-id="2bd23-130">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




