---
description: Die QueryStatus-Methode ruft den Status des NPP ab.
ms.assetid: b035d495-a078-4436-9501-0a30fbfa7268
title: 'Idelta-DC:: QueryStatus-Methode (Netmon. h)'
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
ms.openlocfilehash: cff92dfec95555076f9edba5a1b591f0ef905c1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356654"
---
# <a name="idelaydcquerystatus-method"></a><span data-ttu-id="58c03-103">Idelta aydc:: QueryStatus-Methode</span><span class="sxs-lookup"><span data-stu-id="58c03-103">IDelaydC::QueryStatus method</span></span>

<span data-ttu-id="58c03-104">Die **QueryStatus** -Methode ruft den Status des NPP ab.</span><span class="sxs-lookup"><span data-stu-id="58c03-104">The **QueryStatus** method retrieves the status of the NPP.</span></span>

## <a name="syntax"></a><span data-ttu-id="58c03-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="58c03-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE QueryStatus(
  [out] NETWORKSTATUS *pNetworkStatus
);
```



## <a name="parameters"></a><span data-ttu-id="58c03-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="58c03-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58c03-107">*pnetworkstatus* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="58c03-107">*pNetworkStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="58c03-108">Ein Zeiger auf eine zurückgegebene [networkstatus](networkstatus.md) -Struktur, die den aktuellen Zustand (aufzeichnen, angehalten, beendet usw.) des NPP angibt.</span><span class="sxs-lookup"><span data-stu-id="58c03-108">Pointer to a returned [NETWORKSTATUS](networkstatus.md) structure that indicates the current state (capturing, paused, stopped, and so on) of the NPP.</span></span> <span data-ttu-id="58c03-109">Es liegt in ihrer Verantwortung, den der **Network Status** -Struktur zugeordneten Arbeitsspeicher zuzuordnen und freizugeben.</span><span class="sxs-lookup"><span data-stu-id="58c03-109">It is your responsibility to allocate and free the memory associated with the **NETWORKSTATUS** structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58c03-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="58c03-110">Return value</span></span>

<span data-ttu-id="58c03-111">Wenn die Methode erfolgreich ist, ist der Rückgabewert nmerr \_ Success.</span><span class="sxs-lookup"><span data-stu-id="58c03-111">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="58c03-112">Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert der folgende Fehlercode:</span><span class="sxs-lookup"><span data-stu-id="58c03-112">If the method is unsuccessful, the return value is the following error code:</span></span>



| <span data-ttu-id="58c03-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="58c03-113">Return code</span></span>                                                                                              | <span data-ttu-id="58c03-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="58c03-114">Description</span></span>                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="58c03-115"><dt>**Ungültiger nmerr- \_ \_ Parameter**</dt></span><span class="sxs-lookup"><span data-stu-id="58c03-115"><dt>**NMERR\_INVALID\_PARAMETER**</dt></span></span> </dl> | <span data-ttu-id="58c03-116">Der *pnetworkstatus* -Parameter verweist nicht auf eine gültige [networkstatus](networkstatus.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="58c03-116">The *pNetworkStatus* parameter is not pointing to a valid [NETWORKSTATUS](networkstatus.md) structure.</span></span> <span data-ttu-id="58c03-117">Weisen Sie für diese Struktur Arbeitsspeicher zu, und nennen Sie die **idelta-DC:: QueryStatus** -Methode erneut.</span><span class="sxs-lookup"><span data-stu-id="58c03-117">Allocate memory for this structure and call the **IDelaydC::QueryStatus** method again.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="58c03-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="58c03-118">Remarks</span></span>

<span data-ttu-id="58c03-119">Diese Methode kann jederzeit aufgerufen werden, nachdem " [comatenppinterface](createnppinterface.md) " aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="58c03-119">This method can be called at any time after [CreateNPPInterface](createnppinterface.md) is called.</span></span> <span data-ttu-id="58c03-120">Es kann aufgerufen werden, um festzustellen, ob der NPP mit dem Netzwerk verbunden ist, um den Status der aktuellen Erfassung zu ermitteln und um zu ermitteln, ob Trigger ausstehend sind.</span><span class="sxs-lookup"><span data-stu-id="58c03-120">It can be called to see if the NPP is connected to the network, to find out the status of the current capture, and to see if any triggers are pending.</span></span>

<span data-ttu-id="58c03-121">Bevor Sie diese Methode aufrufen, müssen Sie den für die [networkstatus](networkstatus.md) -Struktur benötigten Arbeitsspeicher zuordnen und diesen Arbeitsspeicher freigeben, wenn die Struktur nicht mehr benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="58c03-121">Before calling this method, you must allocate the memory needed for the [NETWORKSTATUS](networkstatus.md) structure and free that memory when the structure is no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="58c03-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="58c03-122">Requirements</span></span>



| <span data-ttu-id="58c03-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="58c03-123">Requirement</span></span> | <span data-ttu-id="58c03-124">Wert</span><span class="sxs-lookup"><span data-stu-id="58c03-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58c03-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="58c03-125">Minimum supported client</span></span><br/> | <span data-ttu-id="58c03-126">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="58c03-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="58c03-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="58c03-127">Minimum supported server</span></span><br/> | <span data-ttu-id="58c03-128">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="58c03-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="58c03-129">Header</span><span class="sxs-lookup"><span data-stu-id="58c03-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="58c03-130"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="58c03-130"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="58c03-131">DLL</span><span class="sxs-lookup"><span data-stu-id="58c03-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="58c03-132"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="58c03-132"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58c03-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="58c03-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58c03-134">Idelta-DC</span><span class="sxs-lookup"><span data-stu-id="58c03-134">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="58c03-135">"Kreatenppinterface"</span><span class="sxs-lookup"><span data-stu-id="58c03-135">CreateNPPInterface</span></span>](createnppinterface.md)
</dt> <dt>

[<span data-ttu-id="58c03-136">Vornehmen</span><span class="sxs-lookup"><span data-stu-id="58c03-136">NETWORKSTATUS</span></span>](networkstatus.md)
</dt> </dl>

 

 




