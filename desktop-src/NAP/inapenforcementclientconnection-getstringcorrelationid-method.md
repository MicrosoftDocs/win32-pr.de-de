---
title: Inapenforcementclientconnection getstringcorrelationid-Methode (napforcementclient. h)
description: Ruft die Zeichen folgen Version der ID ab, die verwendet wird, um Anforderungen und Antworten zu korrelieren.
ms.assetid: d744fa4e-5e30-429e-810d-7326047bb3f8
keywords:
- Getstringcorrelationid-Methode NAP
- Getstringcorrelationid-Methode NAP, inapenforcementclientconnection-Schnittstelle
- Inapenforcementclientconnection-Schnittstelle NAP, getstringcorrelationid-Methode
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetStringCorrelationId
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6a01ca16bffb627f4ca5be38ef547980951c0ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517579"
---
# <a name="inapenforcementclientconnectiongetstringcorrelationid-method"></a><span data-ttu-id="f435d-106">Inapenforcementclientconnection:: getstringcorrelationid-Methode</span><span class="sxs-lookup"><span data-stu-id="f435d-106">INapEnforcementClientConnection::GetStringCorrelationId method</span></span>

> [!Note]  
> <span data-ttu-id="f435d-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f435d-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="f435d-108">Die **inapenforcementclientconnection:: getstringcorrelationid** -Methode ruft die Zeichen folgen Version der ID ab, die verwendet wird, um Anforderungen und Antworten zu korrelieren.</span><span class="sxs-lookup"><span data-stu-id="f435d-108">The **INapEnforcementClientConnection::GetStringCorrelationId** method gets the string version of the ID used to correlate requests and responses.</span></span>

## <a name="syntax"></a><span data-ttu-id="f435d-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="f435d-109">Syntax</span></span>


```C++
HRESULT GetStringCorrelationId(
  [out] CountedString **correlationId
);
```



## <a name="parameters"></a><span data-ttu-id="f435d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f435d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f435d-111">*correlationId* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f435d-111">*correlationId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f435d-112">Ein Zeiger auf eine [**zählstring**](/windows/win32/api/naptypes/ns-naptypes-countedstring) -Struktur, die die Zeichen folgen Version der [**correlationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid)der Verbindung enthält.</span><span class="sxs-lookup"><span data-stu-id="f435d-112">A pointer to a [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) structure that contains the string version of the connection's [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f435d-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f435d-113">Return value</span></span>

<span data-ttu-id="f435d-114">Es können auch andere com-spezifische Fehlercodes zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="f435d-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="f435d-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="f435d-115">Return code</span></span>                                                                                     | <span data-ttu-id="f435d-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f435d-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="f435d-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f435d-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="f435d-118">Vorgang erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="f435d-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="f435d-119"><dt>**E \_ Access verweigert**</dt></span><span class="sxs-lookup"><span data-stu-id="f435d-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="f435d-120">Berechtigungs Fehler, Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="f435d-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="f435d-121"><dt>**E \_ Outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="f435d-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="f435d-122">System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="f435d-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="f435d-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f435d-123">Requirements</span></span>



| <span data-ttu-id="f435d-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f435d-124">Requirement</span></span> | <span data-ttu-id="f435d-125">Wert</span><span class="sxs-lookup"><span data-stu-id="f435d-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f435d-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f435d-126">Minimum supported client</span></span><br/> | <span data-ttu-id="f435d-127">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f435d-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="f435d-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f435d-128">Minimum supported server</span></span><br/> | <span data-ttu-id="f435d-129">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f435d-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f435d-130">Header</span><span class="sxs-lookup"><span data-stu-id="f435d-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="f435d-131"><dt>Napforcementclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="f435d-131"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="f435d-132">IDL</span><span class="sxs-lookup"><span data-stu-id="f435d-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f435d-133"><dt>Napforcementclient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f435d-133"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="f435d-134">DLL</span><span class="sxs-lookup"><span data-stu-id="f435d-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f435d-135"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f435d-135"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="f435d-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f435d-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f435d-137">**Inapenforcementclientconnection**</span><span class="sxs-lookup"><span data-stu-id="f435d-137">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





