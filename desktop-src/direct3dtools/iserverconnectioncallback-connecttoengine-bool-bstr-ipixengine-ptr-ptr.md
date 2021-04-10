---
description: Stellen Sie eine Verbindung mit einer anderen Instanz einer Remote-Engine auf dem lokalen Computer her.
MS-HAID: vspixengine.IServerConnectionCallback\_ConnectToEngine\_BOOL\_BSTR\_IPixEngine\_ptr\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Iserverconnectioncallback:: connectbackengine-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 56D67449-EA8B-4AD0-94D7-B3CDB7F0ABC8
api_name:
- IServerConnectionCallback.ConnectToEngine
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 1506075066767cba95c7fec768fa27e858bd6a10
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125359"
---
# <a name="span-idvspixengineiserverconnectioncallback_connecttoengine_bool_bstr_ipixengine_ptr_ptrspaniserverconnectioncallbackconnecttoengine-method"></a><span data-ttu-id="3f1de-103"><span id="vspixengine.iserverconnectioncallback_connecttoengine_bool_bstr_ipixengine_ptr_ptr"></span>Iserverconnectioncallback:: connectbackengine-Methode</span><span class="sxs-lookup"><span data-stu-id="3f1de-103"><span id="vspixengine.iserverconnectioncallback_connecttoengine_bool_bstr_ipixengine_ptr_ptr"></span>IServerConnectionCallback::ConnectToEngine method</span></span>

<span data-ttu-id="3f1de-104">Stellen Sie eine Verbindung mit einer anderen Instanz einer Remote-Engine auf dem lokalen Computer her.</span><span class="sxs-lookup"><span data-stu-id="3f1de-104">Connect to another instance of a remote engine on the local machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f1de-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3f1de-105">Syntax</span></span>


```C++
HRESULT ConnectToEngine(
   BOOL          bLegacyConnection,
   BSTR          runAddress,
   IPixEngine ** ppEngineCreated
);
```

## <a name="parameters"></a><span data-ttu-id="3f1de-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3f1de-106">Parameters</span></span>

<span data-ttu-id="3f1de-107">*blegacyconnection* </span><span class="sxs-lookup"><span data-stu-id="3f1de-107">*bLegacyConnection* </span></span>  
<span data-ttu-id="3f1de-108">true, wenn die Engine Legacy verwendet; andernfalls false.</span><span class="sxs-lookup"><span data-stu-id="3f1de-108">true if the engine uses is legacy, otherwise false.</span></span>

<span data-ttu-id="3f1de-109">*runaddress* </span><span class="sxs-lookup"><span data-stu-id="3f1de-109">*runAddress* </span></span>  
<span data-ttu-id="3f1de-110">Eine com-Zeichenfolge, die den Namen des lokalen Computers enthält.</span><span class="sxs-lookup"><span data-stu-id="3f1de-110">A COM string containing the name of the local machine.</span></span>

<span data-ttu-id="3f1de-111">*ppenginecreated* </span><span class="sxs-lookup"><span data-stu-id="3f1de-111">*ppEngineCreated* </span></span>  
<span data-ttu-id="3f1de-112">Bei der Rückgabe die Adresse der Engine-Instanz.</span><span class="sxs-lookup"><span data-stu-id="3f1de-112">On return, the address of the engine instance.</span></span>

## <a name="return-value"></a><span data-ttu-id="3f1de-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3f1de-113">Return value</span></span>

<span data-ttu-id="3f1de-114">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="3f1de-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3f1de-115">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3f1de-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f1de-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3f1de-116">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="3f1de-117">Header</span><span class="sxs-lookup"><span data-stu-id="3f1de-117">Header</span></span></p></td><td><span data-ttu-id="3f1de-118">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="3f1de-118">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="3f1de-119"><span id="see_also"></span>Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3f1de-119"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="3f1de-120">**Iserverconnectioncallback**</span><span class="sxs-lookup"><span data-stu-id="3f1de-120">**IServerConnectionCallback**</span></span>](/windows/desktop/direct3dtools/iserverconnectioncallback)

 

 
