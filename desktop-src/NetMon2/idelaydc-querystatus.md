---
description: 'IDelaydC::QueryStatus-Methode: Die QueryStatus-Methode ruft den Status des NPP ab.'
ms.assetid: b035d495-a078-4436-9501-0a30fbfa7268
title: IDelaydC::QueryStatus-Methode (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.QueryStatus
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 13d1e34b57302d263b81ed64df0b136dc01177b2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118458"
---
# <a name="idelaydcquerystatus-method"></a><span data-ttu-id="6b1b3-103">IDelaydC::QueryStatus-Methode</span><span class="sxs-lookup"><span data-stu-id="6b1b3-103">IDelaydC::QueryStatus method</span></span>

<span data-ttu-id="6b1b3-104">Die **QueryStatus-Methode** ruft den Status des NPP ab.</span><span class="sxs-lookup"><span data-stu-id="6b1b3-104">The **QueryStatus** method retrieves the status of the NPP.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b1b3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6b1b3-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE QueryStatus(
  [out] NETWORKSTATUS *pNetworkStatus
);
```



## <a name="parameters"></a><span data-ttu-id="6b1b3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6b1b3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b1b3-107">*pNetworkStatus* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="6b1b3-107">*pNetworkStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6b1b3-108">Zeiger auf eine zurückgegebene [NETWORKSTATUS-Struktur,](networkstatus.md) die den aktuellen Zustand des NPP angibt (Erfassen, Anhalten, Beendeten und so weiter).</span><span class="sxs-lookup"><span data-stu-id="6b1b3-108">Pointer to a returned [NETWORKSTATUS](networkstatus.md) structure that indicates the current state (capturing, paused, stopped, and so on) of the NPP.</span></span> <span data-ttu-id="6b1b3-109">Es liegt in Ihrer Verantwortung, den der **NETWORKSTATUS-Struktur** zugeordneten Arbeitsspeicher zu reservieren und frei zu geben.</span><span class="sxs-lookup"><span data-stu-id="6b1b3-109">It is your responsibility to allocate and free the memory associated with the **NETWORKSTATUS** structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b1b3-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6b1b3-110">Return value</span></span>

<span data-ttu-id="6b1b3-111">Wenn die Methode erfolgreich ist, ist der Rückgabewert NMERR \_ SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="6b1b3-111">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="6b1b3-112">Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert der folgende Fehlercode:</span><span class="sxs-lookup"><span data-stu-id="6b1b3-112">If the method is unsuccessful, the return value is the following error code:</span></span>



| <span data-ttu-id="6b1b3-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="6b1b3-113">Return code</span></span>                                                                                              | <span data-ttu-id="6b1b3-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6b1b3-114">Description</span></span>                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6b1b3-115"><dt>**NMERR \_ INVALID \_ PARAMETER**</dt></span><span class="sxs-lookup"><span data-stu-id="6b1b3-115"><dt>**NMERR\_INVALID\_PARAMETER**</dt></span></span> </dl> | <span data-ttu-id="6b1b3-116">Der *pNetworkStatus-Parameter* zeigt nicht auf eine gültige [NETWORKSTATUS-Struktur.](networkstatus.md)</span><span class="sxs-lookup"><span data-stu-id="6b1b3-116">The *pNetworkStatus* parameter is not pointing to a valid [NETWORKSTATUS](networkstatus.md) structure.</span></span> <span data-ttu-id="6b1b3-117">Ordnen Sie Arbeitsspeicher für diese Struktur zu, und rufen Sie **erneut die IDelaydC::QueryStatus-Methode** auf.</span><span class="sxs-lookup"><span data-stu-id="6b1b3-117">Allocate memory for this structure and call the **IDelaydC::QueryStatus** method again.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6b1b3-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6b1b3-118">Remarks</span></span>

<span data-ttu-id="6b1b3-119">Diese Methode kann jederzeit aufgerufen werden, nachdem [CreateNPPInterface](createnppinterface.md) aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="6b1b3-119">This method can be called at any time after [CreateNPPInterface](createnppinterface.md) is called.</span></span> <span data-ttu-id="6b1b3-120">Sie kann aufgerufen werden, um zu überprüfen, ob die NPP mit dem Netzwerk verbunden ist, um den Status der aktuellen Erfassung zu finden und um zu überprüfen, ob Trigger ausstehen.</span><span class="sxs-lookup"><span data-stu-id="6b1b3-120">It can be called to see if the NPP is connected to the network, to find out the status of the current capture, and to see if any triggers are pending.</span></span>

<span data-ttu-id="6b1b3-121">Bevor Sie diese Methode aufrufen, müssen Sie den für die [NETWORKSTATUS-Struktur](networkstatus.md) erforderlichen Arbeitsspeicher zuordnen und den Arbeitsspeicher frei geben, wenn die Struktur nicht mehr benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="6b1b3-121">Before calling this method, you must allocate the memory needed for the [NETWORKSTATUS](networkstatus.md) structure and free that memory when the structure is no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b1b3-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6b1b3-122">Requirements</span></span>



| <span data-ttu-id="6b1b3-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6b1b3-123">Requirement</span></span> | <span data-ttu-id="6b1b3-124">Wert</span><span class="sxs-lookup"><span data-stu-id="6b1b3-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b1b3-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6b1b3-125">Minimum supported client</span></span><br/> | <span data-ttu-id="6b1b3-126">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6b1b3-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="6b1b3-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6b1b3-127">Minimum supported server</span></span><br/> | <span data-ttu-id="6b1b3-128">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6b1b3-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="6b1b3-129">Header</span><span class="sxs-lookup"><span data-stu-id="6b1b3-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b1b3-130"><dt>Netmon.h</dt></span><span class="sxs-lookup"><span data-stu-id="6b1b3-130"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="6b1b3-131">DLL</span><span class="sxs-lookup"><span data-stu-id="6b1b3-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6b1b3-132"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6b1b3-132"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b1b3-133">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="6b1b3-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b1b3-134">IDelaydC</span><span class="sxs-lookup"><span data-stu-id="6b1b3-134">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="6b1b3-135">CreateNPPInterface</span><span class="sxs-lookup"><span data-stu-id="6b1b3-135">CreateNPPInterface</span></span>](createnppinterface.md)
</dt> <dt>

[<span data-ttu-id="6b1b3-136">Networkstatus</span><span class="sxs-lookup"><span data-stu-id="6b1b3-136">NETWORKSTATUS</span></span>](networkstatus.md)
</dt> </dl>

 

 




