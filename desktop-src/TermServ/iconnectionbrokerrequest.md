---
title: Iconnectionbrokerrequest-Schnittstelle (cbclient. h)
description: Stellt die Methoden bereit, die zum Abrufen der Ergebnisse der asynchronen iconnectionbrokerclient gettargetinfo-Methode erforderlich sind.
ms.assetid: 20F42FDC-7026-468E-9B8D-25DFFBE229C1
ms.tgt_platform: multiple
keywords:
- Iconnectionbrokerrequest-Schnittstelle Remotedesktopdienste
- Iconnectionbrokerrequest-Schnittstelle Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- IConnectionBrokerRequest
api_location:
- Cbclient.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb95427aee37053b6979cb1a12ce7b5d1942c2fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743664"
---
# <a name="iconnectionbrokerrequest-interface"></a><span data-ttu-id="176f5-105">Iconnectionbrokerrequest-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="176f5-105">IConnectionBrokerRequest interface</span></span>

<span data-ttu-id="176f5-106">Stellt die Methoden bereit, die zum Abrufen der Ergebnisse der asynchronen [**iconnectionbrokerclient:: gettargetinfo**](iconnectionbrokerclient-gettargetinfo.md) -Methode erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="176f5-106">Provides the methods needed to obtain the results of the asynchronous [**IConnectionBrokerClient::GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md) method.</span></span>

<span data-ttu-id="176f5-107">Diese Schnittstelle wird vom System implementiert.</span><span class="sxs-lookup"><span data-stu-id="176f5-107">This interface is implemented by the system.</span></span> <span data-ttu-id="176f5-108">Eine Instanz dieser Schnittstelle wird dem Aufrufer mit der [**iconnectionbrokerclient:: gettargetinfo**](iconnectionbrokerclient-gettargetinfo.md) -Methode bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="176f5-108">An instance of this interface is provided to the caller with the [**IConnectionBrokerClient::GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md) method.</span></span>

## <a name="members"></a><span data-ttu-id="176f5-109">Member</span><span class="sxs-lookup"><span data-stu-id="176f5-109">Members</span></span>

<span data-ttu-id="176f5-110">Die **iconnectionbrokerrequest** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="176f5-110">The **IConnectionBrokerRequest** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="176f5-111">**Iconnectionbrokerrequest** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="176f5-111">**IConnectionBrokerRequest** also has these types of members:</span></span>

-   [<span data-ttu-id="176f5-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="176f5-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="176f5-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="176f5-113">Methods</span></span>

<span data-ttu-id="176f5-114">Die **iconnectionbrokerrequest** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="176f5-114">The **IConnectionBrokerRequest** interface has these methods.</span></span>



| <span data-ttu-id="176f5-115">Methode</span><span class="sxs-lookup"><span data-stu-id="176f5-115">Method</span></span>                                                      | <span data-ttu-id="176f5-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="176f5-116">Description</span></span>                                                           |
|:------------------------------------------------------------|:----------------------------------------------------------------------|
| [<span data-ttu-id="176f5-117">**Check Status**</span><span class="sxs-lookup"><span data-stu-id="176f5-117">**CheckStatus**</span></span>](iconnectionbrokerrequest-checkstatus.md) | <span data-ttu-id="176f5-118">Wird aufgerufen, um den Status einer asynchronen Anforderung zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="176f5-118">Called to determine the status of an asynchronous request.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="176f5-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="176f5-119">Requirements</span></span>



| <span data-ttu-id="176f5-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="176f5-120">Requirement</span></span> | <span data-ttu-id="176f5-121">Wert</span><span class="sxs-lookup"><span data-stu-id="176f5-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="176f5-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="176f5-122">Minimum supported client</span></span><br/> | <span data-ttu-id="176f5-123">Windows 8</span><span class="sxs-lookup"><span data-stu-id="176f5-123">Windows 8</span></span><br/>                                                                        |
| <span data-ttu-id="176f5-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="176f5-124">Minimum supported server</span></span><br/> | <span data-ttu-id="176f5-125">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="176f5-125">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="176f5-126">Header</span><span class="sxs-lookup"><span data-stu-id="176f5-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="176f5-127"><dt>Cbclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="176f5-127"><dt>Cbclient.h</dt></span></span> </dl>       |
| <span data-ttu-id="176f5-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="176f5-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="176f5-129"><dt>Cbclient. lib</dt></span><span class="sxs-lookup"><span data-stu-id="176f5-129"><dt>Cbclient.lib</dt></span></span> </dl>     |
| <span data-ttu-id="176f5-130">DLL</span><span class="sxs-lookup"><span data-stu-id="176f5-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="176f5-131"><dt>Cbclient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="176f5-131"><dt>Cbclient.dll</dt></span></span> </dl>     |
| <span data-ttu-id="176f5-132">IID</span><span class="sxs-lookup"><span data-stu-id="176f5-132">IID</span></span><br/>                      | <span data-ttu-id="176f5-133">IID \_ iconnectionbrokerrequest ist als 25114427-ED5D-46a6-AF53-C62D33A4108E definiert.</span><span class="sxs-lookup"><span data-stu-id="176f5-133">IID\_IConnectionBrokerRequest is defined as 25114427-ED5D-46A6-AF53-C62D33A4108E</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="176f5-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="176f5-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="176f5-135">**Iconnectionbrokerclient:: gettargetinfo**</span><span class="sxs-lookup"><span data-stu-id="176f5-135">**IConnectionBrokerClient::GetTargetInfo**</span></span>](iconnectionbrokerclient-gettargetinfo.md)
</dt> </dl>

 

