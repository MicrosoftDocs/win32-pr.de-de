---
description: Die Abort-Methode bricht eine WinHTTP Send-Methode ab.
ms.assetid: 8326feef-8611-4441-b52d-74855e6acfff
title: 'Iwinhttprequest:: Abort-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.Abort
- WinHttpRequest.Abort
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 56290dfc16f9986cb7d7596c098bb53c207efebe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960532"
---
# <a name="iwinhttprequestabort-method"></a><span data-ttu-id="327e7-103">Iwinhttprequest:: Abort-Methode</span><span class="sxs-lookup"><span data-stu-id="327e7-103">IWinHttpRequest::Abort method</span></span>

<span data-ttu-id="327e7-104">Die **Abort** -Methode bricht eine [WinHTTP](about-winhttp.md) [**Send**](iwinhttprequest-send.md) -Methode ab.</span><span class="sxs-lookup"><span data-stu-id="327e7-104">The **Abort** method aborts a [WinHTTP](about-winhttp.md) [**Send**](iwinhttprequest-send.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="327e7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="327e7-105">Syntax</span></span>


```C++
HRESULT Abort();
```



## <a name="parameters"></a><span data-ttu-id="327e7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="327e7-106">Parameters</span></span>

<span data-ttu-id="327e7-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="327e7-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="327e7-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="327e7-108">Return value</span></span>

<span data-ttu-id="327e7-109">Der Rückgabewert ist bei Erfolg **S \_ OK** oder andernfalls ein Fehlerwert.</span><span class="sxs-lookup"><span data-stu-id="327e7-109">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="327e7-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="327e7-110">Remarks</span></span>

<span data-ttu-id="327e7-111">Sie können asynchrone und synchrone [**Sende**](iwinhttprequest-send.md) Methoden abbrechen.</span><span class="sxs-lookup"><span data-stu-id="327e7-111">You can abort both asynchronous and synchronous [**Send**](iwinhttprequest-send.md) methods.</span></span> <span data-ttu-id="327e7-112">Um eine synchrone [**Sende**](iwinhttprequest-send.md) Methode abzubrechen, müssen Sie **Abbruch** innerhalb eines [**iwinhttprequestevents**](iwinhttprequestevents-interface.md) -Ereignisses abrufen.</span><span class="sxs-lookup"><span data-stu-id="327e7-112">To abort a synchronous [**Send**](iwinhttprequest-send.md) method, you must call **Abort** from within an [**IWinHttpRequestEvents**](iwinhttprequestevents-interface.md) event.</span></span>

> [!Note]  
> <span data-ttu-id="327e7-113">Informationen zu Windows XP und Windows 2000 finden Sie im Abschnitt [Lauf Zeitanforderungen](winhttp-start-page.md) auf der WinHTTP-Startseite.</span><span class="sxs-lookup"><span data-stu-id="327e7-113">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHttp start page.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="327e7-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="327e7-114">Requirements</span></span>



| <span data-ttu-id="327e7-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="327e7-115">Requirement</span></span> | <span data-ttu-id="327e7-116">Wert</span><span class="sxs-lookup"><span data-stu-id="327e7-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="327e7-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="327e7-117">Minimum supported client</span></span><br/> | <span data-ttu-id="327e7-118">Windows XP, Windows 2000 Professional mit SP3 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="327e7-118">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="327e7-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="327e7-119">Minimum supported server</span></span><br/> | <span data-ttu-id="327e7-120">Windows Server 2003, Windows 2000-Server mit \[ nur SP3-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="327e7-120">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="327e7-121">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="327e7-121">Redistributable</span></span><br/>          | <span data-ttu-id="327e7-122">WinHTTP 5,0 und Internet Explorer 5,01 oder höher unter Windows XP und Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="327e7-122">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="327e7-123">IDL</span><span class="sxs-lookup"><span data-stu-id="327e7-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="327e7-124"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="327e7-124"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="327e7-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="327e7-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="327e7-126"><dt>WinHTTP. lib</dt></span><span class="sxs-lookup"><span data-stu-id="327e7-126"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="327e7-127">DLL</span><span class="sxs-lookup"><span data-stu-id="327e7-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="327e7-128"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="327e7-128"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="327e7-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="327e7-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="327e7-130">**Iwinhttprequest**</span><span class="sxs-lookup"><span data-stu-id="327e7-130">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="327e7-131">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="327e7-131">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="327e7-132">WinHTTP-Versionen</span><span class="sxs-lookup"><span data-stu-id="327e7-132">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




