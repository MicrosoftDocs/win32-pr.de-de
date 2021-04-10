---
description: Wartet auf das Herunterfahren der angegebenen Engine (Blockierungs aufzurufen).
MS-HAID: vspixengine.IServerConnectionCallback\_WaitForShutdown\_IPixEngine\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Iserverconnectioncallback:: waitforshutdown-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: B70229D5-3C41-4B50-8336-A1271A9EBE81
api_name:
- IServerConnectionCallback.WaitForShutdown
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: d98bd5f398748e6e62a099bcc2be94b5e5f27bc8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125354"
---
# <a name="span-idvspixengineiserverconnectioncallback_waitforshutdown_ipixengine_ptrspaniserverconnectioncallbackwaitforshutdown-method"></a><span data-ttu-id="54a76-103"><span id="vspixengine.iserverconnectioncallback_waitforshutdown_ipixengine_ptr"></span>Iserverconnectioncallback:: waitforshutdown-Methode</span><span class="sxs-lookup"><span data-stu-id="54a76-103"><span id="vspixengine.iserverconnectioncallback_waitforshutdown_ipixengine_ptr"></span>IServerConnectionCallback::WaitForShutdown method</span></span>

<span data-ttu-id="54a76-104">Wartet auf das Herunterfahren der angegebenen Engine (Blockierungs aufzurufen).</span><span class="sxs-lookup"><span data-stu-id="54a76-104">Wait for shutdown of the specified engine (Blocking call).</span></span>

## <a name="syntax"></a><span data-ttu-id="54a76-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="54a76-105">Syntax</span></span>


```C++
HRESULT WaitForShutdown(
   IPixEngine * pEngine
);
```

## <a name="parameters"></a><span data-ttu-id="54a76-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="54a76-106">Parameters</span></span>

<span data-ttu-id="54a76-107">*Pendel* </span><span class="sxs-lookup"><span data-stu-id="54a76-107">*pEngine* </span></span>  
<span data-ttu-id="54a76-108">Die Engine, die heruntergefahren werden soll.</span><span class="sxs-lookup"><span data-stu-id="54a76-108">The engine to shut down.</span></span>

## <a name="return-value"></a><span data-ttu-id="54a76-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="54a76-109">Return value</span></span>

<span data-ttu-id="54a76-110">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="54a76-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="54a76-111">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="54a76-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="54a76-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="54a76-112">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="54a76-113">Header</span><span class="sxs-lookup"><span data-stu-id="54a76-113">Header</span></span></p></td><td><span data-ttu-id="54a76-114">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="54a76-114">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="54a76-115"><span id="see_also"></span>Siehe auch</span><span class="sxs-lookup"><span data-stu-id="54a76-115"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="54a76-116">**Iserverconnectioncallback**</span><span class="sxs-lookup"><span data-stu-id="54a76-116">**IServerConnectionCallback**</span></span>](/windows/desktop/direct3dtools/iserverconnectioncallback)

 

 
