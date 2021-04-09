---
title: Inapenforcementclientconnection getprivatedata-Methode (napforcementclient. h)
description: Wird vom NAPAgent verwendet, um private Daten zu erhalten.
ms.assetid: d38ef523-b645-401f-b3a9-1315ef39931a
keywords:
- Getprivatedata-Methode NAP
- Getprivatedata-Methode NAP, inapenforcementclientconnection-Schnittstelle
- Inapenforcementclientconnection-Schnittstelle NAP, getprivatedata-Methode
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetPrivateData
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6618ff7b25ad57cbb943107e80f299d9b6a68bea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858773"
---
# <a name="inapenforcementclientconnectiongetprivatedata-method"></a><span data-ttu-id="1bd63-106">Inapenforcementclientconnection:: getprivatedata-Methode</span><span class="sxs-lookup"><span data-stu-id="1bd63-106">INapEnforcementClientConnection::GetPrivateData method</span></span>

> [!Note]  
> <span data-ttu-id="1bd63-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="1bd63-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="1bd63-108">Die **inapenforcementclientconnection:: getprivatedata** -Methode wird vom NAPAgent verwendet, um private Daten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="1bd63-108">The **INapEnforcementClientConnection::GetPrivateData** method is used by the NapAgent to get private data.</span></span>

## <a name="syntax"></a><span data-ttu-id="1bd63-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="1bd63-109">Syntax</span></span>


```C++
HRESULT GetPrivateData(
  [out] PrivateData **privateData
);
```



## <a name="parameters"></a><span data-ttu-id="1bd63-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="1bd63-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1bd63-111">*PRIVATEDATA* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="1bd63-111">*privateData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1bd63-112">Ein Zeiger auf einen Zeiger auf ein nicht transparentes datenblob vom Typ [**PRIVATEDATA**](/windows/win32/api/naptypes/ns-naptypes-privatedata) , das nur von NAPAgent interpretiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="1bd63-112">A pointer to a pointer to a [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) opaque data blob that only the NapAgent can interpret.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1bd63-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1bd63-113">Return value</span></span>

<span data-ttu-id="1bd63-114">Es können auch andere com-spezifische Fehlercodes zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="1bd63-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="1bd63-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="1bd63-115">Return code</span></span>                                                                                     | <span data-ttu-id="1bd63-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1bd63-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="1bd63-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1bd63-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="1bd63-118">Vorgang erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="1bd63-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="1bd63-119"><dt>**E \_ Access verweigert**</dt></span><span class="sxs-lookup"><span data-stu-id="1bd63-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="1bd63-120">Berechtigungs Fehler, Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="1bd63-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="1bd63-121"><dt>**E \_ Outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="1bd63-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="1bd63-122">System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="1bd63-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="1bd63-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1bd63-123">Requirements</span></span>



| <span data-ttu-id="1bd63-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1bd63-124">Requirement</span></span> | <span data-ttu-id="1bd63-125">Wert</span><span class="sxs-lookup"><span data-stu-id="1bd63-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1bd63-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1bd63-126">Minimum supported client</span></span><br/> | <span data-ttu-id="1bd63-127">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1bd63-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="1bd63-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1bd63-128">Minimum supported server</span></span><br/> | <span data-ttu-id="1bd63-129">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1bd63-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="1bd63-130">Header</span><span class="sxs-lookup"><span data-stu-id="1bd63-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="1bd63-131"><dt>Napforcementclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="1bd63-131"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="1bd63-132">IDL</span><span class="sxs-lookup"><span data-stu-id="1bd63-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1bd63-133"><dt>Napforcementclient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1bd63-133"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="1bd63-134">DLL</span><span class="sxs-lookup"><span data-stu-id="1bd63-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1bd63-135"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1bd63-135"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="1bd63-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1bd63-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1bd63-137">**Inapenforcementclientconnection**</span><span class="sxs-lookup"><span data-stu-id="1bd63-137">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





