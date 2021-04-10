---
description: Ruft den NPP-Status ab.
ms.assetid: 48682997-f641-4ae5-b5ad-64fd84f07ae3
title: 'IESP:: QueryStatus-Methode (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.QueryStatus
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 3435ed832484042bfeb9229e4b46fa34441cb395
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215473"
---
# <a name="iespquerystatus-method"></a><span data-ttu-id="b9e7e-103">IESP:: QueryStatus-Methode</span><span class="sxs-lookup"><span data-stu-id="b9e7e-103">IESP::QueryStatus method</span></span>

<span data-ttu-id="b9e7e-104">Die **QueryStatus** -Methode ruft den NPP-Status ab.</span><span class="sxs-lookup"><span data-stu-id="b9e7e-104">The **QueryStatus** method retrieves the NPP status.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9e7e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b9e7e-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE QueryStatus(
  [out] NETWORKSTATUS *pNetworkStatus
);
```



## <a name="parameters"></a><span data-ttu-id="b9e7e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b9e7e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9e7e-107">*pnetworkstatus* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="b9e7e-107">*pNetworkStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b9e7e-108">Ein Zeiger auf eine zurückgegebene [Network Status](networkstatus.md) -Struktur, die den aktuellen Zustand (Erfassung, angehalten, angehalten usw.) des NPP angibt.</span><span class="sxs-lookup"><span data-stu-id="b9e7e-108">A pointer to a returned [NETWORKSTATUS](networkstatus.md) structure that indicates the current state (capturing, paused, stopped, and so on) of the NPP.</span></span> <span data-ttu-id="b9e7e-109">Der Benutzer muss den Speicher für die networkstatus-Struktur zuordnen und freigeben.</span><span class="sxs-lookup"><span data-stu-id="b9e7e-109">The user must allocate and free the memory for the NETWORKSTATUS structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9e7e-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b9e7e-110">Return value</span></span>

<span data-ttu-id="b9e7e-111">Wenn die Methode erfolgreich ist, ist der Rückgabewert nmerr \_ Success.</span><span class="sxs-lookup"><span data-stu-id="b9e7e-111">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="b9e7e-112">Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert der folgende Fehlercode:</span><span class="sxs-lookup"><span data-stu-id="b9e7e-112">If the method is unsuccessful, the return value is the following error code:</span></span>



| <span data-ttu-id="b9e7e-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="b9e7e-113">Return code</span></span>                                                                                              | <span data-ttu-id="b9e7e-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b9e7e-114">Description</span></span>                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b9e7e-115"><dt>**Ungültiger nmerr- \_ \_ Parameter**</dt></span><span class="sxs-lookup"><span data-stu-id="b9e7e-115"><dt>**NMERR\_INVALID\_PARAMETER**</dt></span></span> </dl> | <span data-ttu-id="b9e7e-116">Der *pnetworkstatus* -Parameter verweist nicht auf eine gültige [networkstatus](networkstatus.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="b9e7e-116">The *pNetworkStatus* parameter is not pointing to a valid [NETWORKSTATUS](networkstatus.md) structure.</span></span> <span data-ttu-id="b9e7e-117">Weisen Sie für diese Struktur Arbeitsspeicher zu, und nennen Sie **iESP:: QueryStatus** erneut.</span><span class="sxs-lookup"><span data-stu-id="b9e7e-117">Allocate memory for this structure and call **IESP::QueryStatus** again.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b9e7e-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b9e7e-118">Remarks</span></span>

<span data-ttu-id="b9e7e-119">Diese Methode kann jederzeit aufgerufen werden, nachdem " [comatenppinterface](createnppinterface.md) " aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="b9e7e-119">This method can be called at any time after the [CreateNPPInterface](createnppinterface.md) is called.</span></span> <span data-ttu-id="b9e7e-120">Sie können diese Methode abrufen, um zu ermitteln, ob der NPP mit dem Netzwerk verbunden ist, um den Status der aktuellen Erfassung zu ermitteln und zu überprüfen, ob Trigger ausstehend sind.</span><span class="sxs-lookup"><span data-stu-id="b9e7e-120">You can call this method to see if the NPP is connected to the network, to find out the status of the current capture, and to see if any triggers are pending.</span></span>

<span data-ttu-id="b9e7e-121">Bevor Sie diese Methode aufrufen, müssen Sie den für die [networkstatus](networkstatus.md) -Struktur erforderlichen Arbeitsspeicher zuordnen und diesen Speicher freigeben, wenn die Struktur nicht mehr benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="b9e7e-121">Before calling this method, allocate the memory required for the [NETWORKSTATUS](networkstatus.md) structure and free that memory when the structure is no longer required.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9e7e-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b9e7e-122">Requirements</span></span>



| <span data-ttu-id="b9e7e-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b9e7e-123">Requirement</span></span> | <span data-ttu-id="b9e7e-124">Wert</span><span class="sxs-lookup"><span data-stu-id="b9e7e-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9e7e-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b9e7e-125">Minimum supported client</span></span><br/> | <span data-ttu-id="b9e7e-126">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b9e7e-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="b9e7e-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b9e7e-127">Minimum supported server</span></span><br/> | <span data-ttu-id="b9e7e-128">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b9e7e-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="b9e7e-129">Header</span><span class="sxs-lookup"><span data-stu-id="b9e7e-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="b9e7e-130"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="b9e7e-130"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="b9e7e-131">DLL</span><span class="sxs-lookup"><span data-stu-id="b9e7e-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b9e7e-132"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b9e7e-132"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9e7e-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b9e7e-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9e7e-134">IESP</span><span class="sxs-lookup"><span data-stu-id="b9e7e-134">IESP</span></span>](iesp.md)
</dt> <dt>

[<span data-ttu-id="b9e7e-135">"Kreatenppinterface"</span><span class="sxs-lookup"><span data-stu-id="b9e7e-135">CreateNPPInterface</span></span>](createnppinterface.md)
</dt> <dt>

[<span data-ttu-id="b9e7e-136">Vornehmen</span><span class="sxs-lookup"><span data-stu-id="b9e7e-136">NETWORKSTATUS</span></span>](networkstatus.md)
</dt> </dl>

 

 




