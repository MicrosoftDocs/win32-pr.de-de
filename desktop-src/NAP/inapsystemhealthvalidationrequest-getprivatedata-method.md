---
title: Inapsystemhealthvalidationrequest getprivatedata-Methode (napsystemhealthvalidator. h)
description: Ermöglicht dem napserver das Abrufen von Zustandsinformationen.
ms.assetid: f85026ca-852b-4eb1-9a8c-7e03cd1765f2
keywords:
- Getprivatedata-Methode NAP
- Getprivatedata-Methode NAP, inapsystemhealthvalidationrequest-Schnittstelle
- Inapsystemhealthvalidationrequest-Schnittstelle NAP, getprivatedata-Methode
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest.GetPrivateData
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d78cceba42cd503ef8a875ece8f4ed196eaeff8c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743345"
---
# <a name="inapsystemhealthvalidationrequestgetprivatedata-method"></a><span data-ttu-id="4cb1e-106">Inapsystemhealthvalidationrequest:: getprivatedata-Methode</span><span class="sxs-lookup"><span data-stu-id="4cb1e-106">INapSystemHealthValidationRequest::GetPrivateData method</span></span>

> [!Note]  
> <span data-ttu-id="4cb1e-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="4cb1e-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="4cb1e-108">Die **inapsystemhealthvalidationrequest:: getprivatedata** -Methode ermöglicht dem napserver das Abrufen von Zustandsinformationen.</span><span class="sxs-lookup"><span data-stu-id="4cb1e-108">The **INapSystemHealthValidationRequest::GetPrivateData** method allows the NapServer to retrieve state information.</span></span>

## <a name="syntax"></a><span data-ttu-id="4cb1e-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="4cb1e-109">Syntax</span></span>


```C++
HRESULT GetPrivateData(
  [out] PrivateData **privateData
);
```



## <a name="parameters"></a><span data-ttu-id="4cb1e-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="4cb1e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4cb1e-111">*PRIVATEDATA* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="4cb1e-111">*privateData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4cb1e-112">Ein Zeiger auf einen Zeiger auf einen nicht transparenten Daten-BLOB mit [**PRIVATEDATA**](/windows/win32/api/naptypes/ns-naptypes-privatedata) , der Zustandsinformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="4cb1e-112">A pointer to a pointer to [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) opaque data blob that contains state information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4cb1e-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4cb1e-113">Return value</span></span>

<span data-ttu-id="4cb1e-114">Es können auch andere com-spezifische Fehlercodes zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="4cb1e-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="4cb1e-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="4cb1e-115">Return code</span></span>                                                                                     | <span data-ttu-id="4cb1e-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4cb1e-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="4cb1e-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="4cb1e-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="4cb1e-118">Vorgang erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="4cb1e-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="4cb1e-119"><dt>**E \_ Access verweigert**</dt></span><span class="sxs-lookup"><span data-stu-id="4cb1e-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="4cb1e-120">Berechtigungs Fehler, Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="4cb1e-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="4cb1e-121"><dt>**E \_ Outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="4cb1e-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="4cb1e-122">System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="4cb1e-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4cb1e-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4cb1e-123">Remarks</span></span>

<span data-ttu-id="4cb1e-124">Nur der napserver kann das datenblob interpretieren.</span><span class="sxs-lookup"><span data-stu-id="4cb1e-124">Only the NapServer can interpret the data blob.</span></span>

## <a name="requirements"></a><span data-ttu-id="4cb1e-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4cb1e-125">Requirements</span></span>



| <span data-ttu-id="4cb1e-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4cb1e-126">Requirement</span></span> | <span data-ttu-id="4cb1e-127">Wert</span><span class="sxs-lookup"><span data-stu-id="4cb1e-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4cb1e-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4cb1e-128">Minimum supported client</span></span><br/> | <span data-ttu-id="4cb1e-129">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="4cb1e-129">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="4cb1e-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4cb1e-130">Minimum supported server</span></span><br/> | <span data-ttu-id="4cb1e-131">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4cb1e-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4cb1e-132">Header</span><span class="sxs-lookup"><span data-stu-id="4cb1e-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="4cb1e-133"><dt>Napsystemhealthvalidator. h</dt></span><span class="sxs-lookup"><span data-stu-id="4cb1e-133"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="4cb1e-134">IDL</span><span class="sxs-lookup"><span data-stu-id="4cb1e-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4cb1e-135"><dt>Napsystemhealthvalidator. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4cb1e-135"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |
| <span data-ttu-id="4cb1e-136">DLL</span><span class="sxs-lookup"><span data-stu-id="4cb1e-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4cb1e-137"><dt>Qshvhost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4cb1e-137"><dt>Qshvhost.dll</dt></span></span> </dl>                 |



## <a name="see-also"></a><span data-ttu-id="4cb1e-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4cb1e-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cb1e-139">**Inapsystemhealthvalidationrequest**</span><span class="sxs-lookup"><span data-stu-id="4cb1e-139">**INapSystemHealthValidationRequest**</span></span>](inapsystemhealthvalidationrequest.md)
</dt> </dl>

 

 





