---
description: Übergibt Ressourcen asynchron an die-Engine, z. b. Zeichen folgen für Fehlermeldungen.
MS-HAID: vspixengine.IPixEngine7\_InitEngineAsync\_ResourcePair\_arr\_UINT\_IVersionCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPixEngine7:: initengineasync-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 10138B39-88D2-4586-BD51-C618722EFFA0
api_name:
- IPixEngine7.InitEngineAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 21d98a207b0194f281abc2800cd63f9be7de5073
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482630"
---
# <a name="span-idvspixengineipixengine7_initengineasync_resourcepair_arr_uint_iversioncallback_ptr_dword_dwordspanipixengine7initengineasync-method"></a><span data-ttu-id="8e85f-103"><span id="vspixengine.ipixengine7_initengineasync_resourcepair_arr_uint_iversioncallback_ptr_dword_dword"></span>IPixEngine7:: initengineasync-Methode</span><span class="sxs-lookup"><span data-stu-id="8e85f-103"><span id="vspixengine.ipixengine7_initengineasync_resourcepair_arr_uint_iversioncallback_ptr_dword_dword"></span>IPixEngine7::InitEngineAsync method</span></span>

<span data-ttu-id="8e85f-104">Übergibt Ressourcen asynchron an die-Engine, z. b. Zeichen folgen für Fehlermeldungen.</span><span class="sxs-lookup"><span data-stu-id="8e85f-104">Asynchronously passes resources to the engine, such as strings for error messages.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e85f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8e85f-105">Syntax</span></span>


```C++
HRESULT InitEngineAsync(
   ResourcePair []   count1_resources,
   UINT              count,
   IVersionCallback* versionCallback,
   DWORD             requestCookie,
   DWORD             progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="8e85f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8e85f-106">Parameters</span></span>

<span data-ttu-id="8e85f-107">*count1- \_ Ressourcen* </span><span class="sxs-lookup"><span data-stu-id="8e85f-107">*count1\_resources* </span></span>  
<span data-ttu-id="8e85f-108">Ein Array von Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="8e85f-108">An array of resources.</span></span>

<span data-ttu-id="8e85f-109">*Countdown* </span><span class="sxs-lookup"><span data-stu-id="8e85f-109">*count* </span></span>  
<span data-ttu-id="8e85f-110">Die Anzahl der Ressourcen in count1- \_ Ressourcen</span><span class="sxs-lookup"><span data-stu-id="8e85f-110">The number of resources in count1\_resources</span></span>

<span data-ttu-id="8e85f-111">*versioncallback* </span><span class="sxs-lookup"><span data-stu-id="8e85f-111">*versionCallback* </span></span>  
<span data-ttu-id="8e85f-112">Die Adresse des Rückrufs, der zum Benachrichtigen des Hosts der Ergebnisse verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8e85f-112">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="8e85f-113">*requestcookie* </span><span class="sxs-lookup"><span data-stu-id="8e85f-113">*requestCookie* </span></span>  
<span data-ttu-id="8e85f-114">Ein Cookie, das die Anforderung eindeutig identifiziert, und kann verwendet werden, um zu signalisieren, dass es abgebrochen werden soll.</span><span class="sxs-lookup"><span data-stu-id="8e85f-114">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="8e85f-115">*progressintervalmsekunden* </span><span class="sxs-lookup"><span data-stu-id="8e85f-115">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="8e85f-116">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="8e85f-116">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="8e85f-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8e85f-117">Return value</span></span>

<span data-ttu-id="8e85f-118">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="8e85f-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8e85f-119">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8e85f-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e85f-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8e85f-120">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="8e85f-121">Header</span><span class="sxs-lookup"><span data-stu-id="8e85f-121">Header</span></span></p></td><td><span data-ttu-id="8e85f-122">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="8e85f-122">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="8e85f-123"><span id="see_also"></span>Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8e85f-123"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="8e85f-124">**IPixEngine7**</span><span class="sxs-lookup"><span data-stu-id="8e85f-124">**IPixEngine7**</span></span>](/windows/desktop/direct3dtools/ipixengine7)

 

 
