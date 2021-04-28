---
description: 'IRTC::QueryStatus-Methode: Die QueryStatus-Methode ruft den Status des NPP ab.'
ms.assetid: 4517eb34-087a-491c-97b5-cbe9190fa7a2
title: IRTC::QueryStatus-Methode (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.QueryStatus
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 6dd8c18d19df7d577ad219742520630f00122a41
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110608"
---
# <a name="irtcquerystatus-method"></a><span data-ttu-id="d3ebe-103">IRTC::QueryStatus-Methode</span><span class="sxs-lookup"><span data-stu-id="d3ebe-103">IRTC::QueryStatus method</span></span>

<span data-ttu-id="d3ebe-104">Die **QueryStatus-Methode** ruft den Status des NPP ab.</span><span class="sxs-lookup"><span data-stu-id="d3ebe-104">The **QueryStatus** method retrieves the status of the NPP.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3ebe-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d3ebe-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE QueryStatus(
  [out] NETWORKSTATUS *pNetworkStatus
);
```



## <a name="parameters"></a><span data-ttu-id="d3ebe-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d3ebe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3ebe-107">*pNetworkStatus* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d3ebe-107">*pNetworkStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d3ebe-108">Zeiger auf eine zurückgegebene [NETWORKSTATUS-Struktur,](networkstatus.md) die den aktuellen Zustand (Erfassen, Anhalten, Beendet usw.) des NPP angibt.</span><span class="sxs-lookup"><span data-stu-id="d3ebe-108">Pointer to a returned [NETWORKSTATUS](networkstatus.md) structure that indicates the current state (capturing, paused, stopped, and so on) of the NPP.</span></span> <span data-ttu-id="d3ebe-109">Es liegt in der Verantwortung der Anwendung, den Arbeitsspeicher für die **NETWORKSTATUS-Struktur** zuzuordnen und freizugeben.</span><span class="sxs-lookup"><span data-stu-id="d3ebe-109">It is the application's responsibility to allocate and free the memory for the **NETWORKSTATUS** structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3ebe-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d3ebe-110">Return value</span></span>

<span data-ttu-id="d3ebe-111">Wenn die Methode erfolgreich ist, lautet der Rückgabewert NMERR \_ SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="d3ebe-111">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="d3ebe-112">Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert der folgende Fehlercode:</span><span class="sxs-lookup"><span data-stu-id="d3ebe-112">If the method is unsuccessful, the return value is the following error code:</span></span>



| <span data-ttu-id="d3ebe-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="d3ebe-113">Return code</span></span>                                                                                              | <span data-ttu-id="d3ebe-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d3ebe-114">Description</span></span>                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d3ebe-115"><dt>**NMERR \_ – UNGÜLTIGER \_ PARAMETER**</dt></span><span class="sxs-lookup"><span data-stu-id="d3ebe-115"><dt>**NMERR\_INVALID\_PARAMETER**</dt></span></span> </dl> | <span data-ttu-id="d3ebe-116">Der *pNetworkStatus-Parameter* verweist nicht auf eine gültige [NETWORKSTATUS-Struktur.](networkstatus.md)</span><span class="sxs-lookup"><span data-stu-id="d3ebe-116">The *pNetworkStatus* parameter is not pointing to a valid [NETWORKSTATUS](networkstatus.md) structure.</span></span> <span data-ttu-id="d3ebe-117">Belegen Sie Arbeitsspeicher für diese Struktur, und rufen Sie **IRTC::QueryStatus** erneut auf.</span><span class="sxs-lookup"><span data-stu-id="d3ebe-117">Allocate memory for this structure and call **IRTC::QueryStatus** again.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d3ebe-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d3ebe-118">Remarks</span></span>

<span data-ttu-id="d3ebe-119">Diese Methode kann jederzeit aufgerufen werden, nachdem die [CreateNPPInterface-Methode](createnppinterface.md) aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="d3ebe-119">This method can be called at any time after the [CreateNPPInterface](createnppinterface.md) method is called.</span></span> <span data-ttu-id="d3ebe-120">Sie können diese Methode aufrufen, um festzustellen, ob das NPP mit dem Netzwerk verbunden ist, um den Status der aktuellen Erfassung zu ermitteln und um festzustellen, ob Trigger ausstehend sind.</span><span class="sxs-lookup"><span data-stu-id="d3ebe-120">You can call this method to see if the NPP is connected to the network, to find out the status of the current capture, and to see if any triggers are pending.</span></span> <span data-ttu-id="d3ebe-121">Vor dem Aufrufen dieser Methode müssen Sie jedoch den für die [NETWORKSTATUS-Struktur](networkstatus.md) benötigten Arbeitsspeicher zuordnen und diesen Arbeitsspeicher freigeben, wenn die Struktur nicht mehr benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="d3ebe-121">Before calling this method, however, you must allocate the memory needed for the [NETWORKSTATUS](networkstatus.md) structure and free that memory when the structure is no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3ebe-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d3ebe-122">Requirements</span></span>



| <span data-ttu-id="d3ebe-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d3ebe-123">Requirement</span></span> | <span data-ttu-id="d3ebe-124">Wert</span><span class="sxs-lookup"><span data-stu-id="d3ebe-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3ebe-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d3ebe-125">Minimum supported client</span></span><br/> | <span data-ttu-id="d3ebe-126">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d3ebe-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="d3ebe-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d3ebe-127">Minimum supported server</span></span><br/> | <span data-ttu-id="d3ebe-128">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d3ebe-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="d3ebe-129">Header</span><span class="sxs-lookup"><span data-stu-id="d3ebe-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3ebe-130"><dt>Netmon.h</dt></span><span class="sxs-lookup"><span data-stu-id="d3ebe-130"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="d3ebe-131">DLL</span><span class="sxs-lookup"><span data-stu-id="d3ebe-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d3ebe-132"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d3ebe-132"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3ebe-133">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d3ebe-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3ebe-134">IRTC</span><span class="sxs-lookup"><span data-stu-id="d3ebe-134">IRTC</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="d3ebe-135">CreateNPPInterface</span><span class="sxs-lookup"><span data-stu-id="d3ebe-135">CreateNPPInterface</span></span>](createnppinterface.md)
</dt> <dt>

[<span data-ttu-id="d3ebe-136">Networkstatus</span><span class="sxs-lookup"><span data-stu-id="d3ebe-136">NETWORKSTATUS</span></span>](networkstatus.md)
</dt> </dl>

 

 




