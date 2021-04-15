---
title: Inapserverinfo getfailurecategorymappings-Methode (napservermanagement. h)
description: Ruft die Zuordnungen der Fehlerkategorien für einen angegebenen SHA-oder SHV-Knoten ab.
ms.assetid: 89b89003-40b3-4763-aec8-01cd0c307649
keywords:
- Getfailurecategorymappings-Methode NAP
- Getfailurecategorymappings-Methode NAP, inapserverinfo-Schnittstelle
- Inapserverinfo-Schnittstelle NAP, getfailurecategorymappings-Methode
topic_type:
- apiref
api_name:
- INapServerInfo.GetFailureCategoryMappings
api_location:
- qsvrmgmt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7ba830dd8a35a2c60b14c4feec14846125223e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479341"
---
# <a name="inapserverinfogetfailurecategorymappings-method"></a><span data-ttu-id="93d03-106">Inapserverinfo:: getfailurecategorymappings-Methode</span><span class="sxs-lookup"><span data-stu-id="93d03-106">INapServerInfo::GetFailureCategoryMappings method</span></span>

> [!Note]  
> <span data-ttu-id="93d03-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="93d03-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="93d03-108">Die **inapserverinfo:: getfailurecategorymappings** -Methode ruft die Zuordnungen der Fehlerkategorien für einen angegebenen SHA oder SHV ab.</span><span class="sxs-lookup"><span data-stu-id="93d03-108">The **INapServerInfo::GetFailureCategoryMappings** method retrieves the failure category mappings for a specified SHA or SHV.</span></span>

## <a name="syntax"></a><span data-ttu-id="93d03-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="93d03-109">Syntax</span></span>


```C++
HRESULT GetFailureCategoryMappings(
  [in]  SystemHealthEntityId   id,
  [out] FailureCategoryMapping *mapping
);
```



## <a name="parameters"></a><span data-ttu-id="93d03-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="93d03-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93d03-111">*ID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="93d03-111">*id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93d03-112">Eine [**systemhealthentityid**](nap-type-constants.md) , die den eindeutigen Bezeichner von SHA oder SHV enthält.</span><span class="sxs-lookup"><span data-stu-id="93d03-112">A [**SystemHealthEntityId**](nap-type-constants.md) that contains the unique identifier of the SHA or the SHV.</span></span>

</dd> <dt>

<span data-ttu-id="93d03-113">*Zuordnung* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="93d03-113">*mapping* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="93d03-114">Ein Zeiger auf ein [**failurecategorymapping**](/windows/win32/api/naptypes/ns-naptypes-failurecategorymapping) , das die Mapping-Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="93d03-114">A pointer to a [**FailureCategoryMapping**](/windows/win32/api/naptypes/ns-naptypes-failurecategorymapping) that contains the mapping data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93d03-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="93d03-115">Return value</span></span>

<span data-ttu-id="93d03-116">Es können auch andere com-spezifische Fehlercodes zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="93d03-116">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="93d03-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="93d03-117">Return code</span></span>                                                                                     | <span data-ttu-id="93d03-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="93d03-118">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="93d03-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="93d03-119"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="93d03-120">Vorgang erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="93d03-120">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="93d03-121"><dt>**E \_ Access verweigert**</dt></span><span class="sxs-lookup"><span data-stu-id="93d03-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="93d03-122">Berechtigungs Fehler, Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="93d03-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="93d03-123"><dt>**E \_ Outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="93d03-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="93d03-124">System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="93d03-124">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="93d03-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="93d03-125">Requirements</span></span>



| <span data-ttu-id="93d03-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="93d03-126">Requirement</span></span> | <span data-ttu-id="93d03-127">Wert</span><span class="sxs-lookup"><span data-stu-id="93d03-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93d03-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="93d03-128">Minimum supported client</span></span><br/> | <span data-ttu-id="93d03-129">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="93d03-129">None supported</span></span><br/>                                                                          |
| <span data-ttu-id="93d03-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="93d03-130">Minimum supported server</span></span><br/> | <span data-ttu-id="93d03-131">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="93d03-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="93d03-132">Header</span><span class="sxs-lookup"><span data-stu-id="93d03-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="93d03-133"><dt>Napservermanagement. h</dt></span><span class="sxs-lookup"><span data-stu-id="93d03-133"><dt>NapServerManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="93d03-134">IDL</span><span class="sxs-lookup"><span data-stu-id="93d03-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="93d03-135"><dt>Napservermanagement. idl</dt></span><span class="sxs-lookup"><span data-stu-id="93d03-135"><dt>NapServerManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="93d03-136">DLL</span><span class="sxs-lookup"><span data-stu-id="93d03-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="93d03-137"><dt>Qsvrmgmt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="93d03-137"><dt>Qsvrmgmt.dll</dt></span></span> </dl>            |



## <a name="see-also"></a><span data-ttu-id="93d03-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="93d03-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93d03-139">**Inapserverinfo**</span><span class="sxs-lookup"><span data-stu-id="93d03-139">**INapServerInfo**</span></span>](inapserverinfo.md)
</dt> </dl>

 

 





