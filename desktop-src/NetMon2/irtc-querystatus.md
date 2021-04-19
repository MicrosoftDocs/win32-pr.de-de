---
description: Die QueryStatus-Methode ruft den Status des NPP ab.
ms.assetid: 4517eb34-087a-491c-97b5-cbe9190fa7a2
title: 'Untc:: QueryStatus-Methode (Netmon. h)'
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
ms.openlocfilehash: e05120353cd39db661cf1b4309353034c184cd66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354636"
---
# <a name="irtcquerystatus-method"></a><span data-ttu-id="2654c-103">Untc:: QueryStatus-Methode</span><span class="sxs-lookup"><span data-stu-id="2654c-103">IRTC::QueryStatus method</span></span>

<span data-ttu-id="2654c-104">Die **QueryStatus** -Methode ruft den Status des NPP ab.</span><span class="sxs-lookup"><span data-stu-id="2654c-104">The **QueryStatus** method retrieves the status of the NPP.</span></span>

## <a name="syntax"></a><span data-ttu-id="2654c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2654c-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE QueryStatus(
  [out] NETWORKSTATUS *pNetworkStatus
);
```



## <a name="parameters"></a><span data-ttu-id="2654c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2654c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2654c-107">*pnetworkstatus* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="2654c-107">*pNetworkStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2654c-108">Ein Zeiger auf eine zurückgegebene [networkstatus](networkstatus.md) -Struktur, die den aktuellen Zustand (aufzeichnen, angehalten, beendet usw.) des NPP angibt.</span><span class="sxs-lookup"><span data-stu-id="2654c-108">Pointer to a returned [NETWORKSTATUS](networkstatus.md) structure that indicates the current state (capturing, paused, stopped, and so on) of the NPP.</span></span> <span data-ttu-id="2654c-109">Es ist Aufgabe der Anwendung, den Arbeitsspeicher für die **networkstatus** -Struktur zuzuordnen und freizugeben.</span><span class="sxs-lookup"><span data-stu-id="2654c-109">It is the application's responsibility to allocate and free the memory for the **NETWORKSTATUS** structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2654c-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2654c-110">Return value</span></span>

<span data-ttu-id="2654c-111">Wenn die Methode erfolgreich ist, ist der Rückgabewert nmerr \_ Success.</span><span class="sxs-lookup"><span data-stu-id="2654c-111">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="2654c-112">Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert der folgende Fehlercode:</span><span class="sxs-lookup"><span data-stu-id="2654c-112">If the method is unsuccessful, the return value is the following error code:</span></span>



| <span data-ttu-id="2654c-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="2654c-113">Return code</span></span>                                                                                              | <span data-ttu-id="2654c-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2654c-114">Description</span></span>                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2654c-115"><dt>**Ungültiger nmerr- \_ \_ Parameter**</dt></span><span class="sxs-lookup"><span data-stu-id="2654c-115"><dt>**NMERR\_INVALID\_PARAMETER**</dt></span></span> </dl> | <span data-ttu-id="2654c-116">Der *pnetworkstatus* -Parameter verweist nicht auf eine gültige [networkstatus](networkstatus.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="2654c-116">The *pNetworkStatus* parameter is not pointing to a valid [NETWORKSTATUS](networkstatus.md) structure.</span></span> <span data-ttu-id="2654c-117">Weisen Sie der Struktur Arbeitsspeicher zu, und wiederholen Sie den Befehl " **untc:: QueryStatus** "</span><span class="sxs-lookup"><span data-stu-id="2654c-117">Allocate memory for this structure and call **IRTC::QueryStatus** again.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2654c-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2654c-118">Remarks</span></span>

<span data-ttu-id="2654c-119">Diese Methode kann jederzeit aufgerufen werden, nachdem die Methode " [comatenppinterface](createnppinterface.md) " aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="2654c-119">This method can be called at any time after the [CreateNPPInterface](createnppinterface.md) method is called.</span></span> <span data-ttu-id="2654c-120">Sie können diese Methode abrufen, um zu ermitteln, ob der NPP mit dem Netzwerk verbunden ist, um den Status der aktuellen Erfassung zu ermitteln und zu überprüfen, ob Trigger ausstehend sind.</span><span class="sxs-lookup"><span data-stu-id="2654c-120">You can call this method to see if the NPP is connected to the network, to find out the status of the current capture, and to see if any triggers are pending.</span></span> <span data-ttu-id="2654c-121">Vor dem Aufrufen dieser Methode müssen Sie jedoch den Arbeitsspeicher zuordnen, der für die [networkstatus](networkstatus.md) -Struktur benötigt wird, und diesen Arbeitsspeicher freigeben, wenn die Struktur nicht mehr benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="2654c-121">Before calling this method, however, you must allocate the memory needed for the [NETWORKSTATUS](networkstatus.md) structure and free that memory when the structure is no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="2654c-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2654c-122">Requirements</span></span>



| <span data-ttu-id="2654c-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2654c-123">Requirement</span></span> | <span data-ttu-id="2654c-124">Wert</span><span class="sxs-lookup"><span data-stu-id="2654c-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2654c-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2654c-125">Minimum supported client</span></span><br/> | <span data-ttu-id="2654c-126">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2654c-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="2654c-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2654c-127">Minimum supported server</span></span><br/> | <span data-ttu-id="2654c-128">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2654c-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="2654c-129">Header</span><span class="sxs-lookup"><span data-stu-id="2654c-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="2654c-130"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="2654c-130"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="2654c-131">DLL</span><span class="sxs-lookup"><span data-stu-id="2654c-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2654c-132"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2654c-132"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2654c-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2654c-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2654c-134">"Iran"</span><span class="sxs-lookup"><span data-stu-id="2654c-134">IRTC</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="2654c-135">"Kreatenppinterface"</span><span class="sxs-lookup"><span data-stu-id="2654c-135">CreateNPPInterface</span></span>](createnppinterface.md)
</dt> <dt>

[<span data-ttu-id="2654c-136">Vornehmen</span><span class="sxs-lookup"><span data-stu-id="2654c-136">NETWORKSTATUS</span></span>](networkstatus.md)
</dt> </dl>

 

 




