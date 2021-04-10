---
title: Inapsohconstructor getsoh-Methode (napprotocol. h)
description: Ruft das erstellte sohrequest-oder sohresponse-Paket ab.
ms.assetid: 402c72fd-9e23-453a-8c95-57615295e056
keywords:
- Getsoh-Methode NAP
- Getsoh-Methode NAP, inapsohconstructor-Schnittstelle
- Inapsohconstructor Interface NAP, getsoh-Methode
topic_type:
- apiref
api_name:
- INapSoHConstructor.GetSoH
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 066257aadf0ed14816efec06936d4b070087159f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103538"
---
# <a name="inapsohconstructorgetsoh-method"></a><span data-ttu-id="7594d-106">Inapsohconstructor:: getsoh-Methode</span><span class="sxs-lookup"><span data-stu-id="7594d-106">INapSoHConstructor::GetSoH method</span></span>

> [!Note]  
> <span data-ttu-id="7594d-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7594d-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="7594d-108">Die **inapsohconstructor:: getsoh** -Methode ruft das erstellte sohrequest-oder sohresponse-Paket ab.</span><span class="sxs-lookup"><span data-stu-id="7594d-108">The **INapSoHConstructor::GetSoH** method retrieves the constructed SoHRequest or SoHResponse packet.</span></span>

## <a name="syntax"></a><span data-ttu-id="7594d-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="7594d-109">Syntax</span></span>


```C++
HRESULT GetSoH(
  [out] SoH **soh
);
```



## <a name="parameters"></a><span data-ttu-id="7594d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="7594d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7594d-111">*SoH* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="7594d-111">*soh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7594d-112">Ein Zeiger auf einen Zeiger auf das erstellte [**sohrequest**](/windows/win32/api/naptypes/ns-naptypes-soh) -oder **sohresponse** -Paket.</span><span class="sxs-lookup"><span data-stu-id="7594d-112">A pointer to a pointer to the constructed [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) or **SoHResponse** packet.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7594d-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7594d-113">Return value</span></span>

<span data-ttu-id="7594d-114">Es können auch andere com-spezifische Fehlercodes zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="7594d-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="7594d-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="7594d-115">Return code</span></span>                                                                                     | <span data-ttu-id="7594d-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7594d-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="7594d-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7594d-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="7594d-118">Vorgang erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="7594d-118">Operation successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="7594d-119"><dt>**E \_ Access verweigert**</dt></span><span class="sxs-lookup"><span data-stu-id="7594d-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="7594d-120">Berechtigungs Fehler, Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="7594d-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="7594d-121"><dt>**E \_ Outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="7594d-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="7594d-122">System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="7594d-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="7594d-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7594d-123">Requirements</span></span>



| <span data-ttu-id="7594d-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7594d-124">Requirement</span></span> | <span data-ttu-id="7594d-125">Wert</span><span class="sxs-lookup"><span data-stu-id="7594d-125">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="7594d-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7594d-126">Minimum supported client</span></span><br/> | <span data-ttu-id="7594d-127">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7594d-127">Windows Vista \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="7594d-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7594d-128">Minimum supported server</span></span><br/> | <span data-ttu-id="7594d-129">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7594d-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="7594d-130">Header</span><span class="sxs-lookup"><span data-stu-id="7594d-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="7594d-131"><dt>Napprotocol. h</dt></span><span class="sxs-lookup"><span data-stu-id="7594d-131"><dt>NapProtocol.h</dt></span></span> </dl>   |
| <span data-ttu-id="7594d-132">IDL</span><span class="sxs-lookup"><span data-stu-id="7594d-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7594d-133"><dt>Napprotocol. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7594d-133"><dt>NapProtocol.idl</dt></span></span> </dl> |
| <span data-ttu-id="7594d-134">DLL</span><span class="sxs-lookup"><span data-stu-id="7594d-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7594d-135"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7594d-135"><dt>Qutil.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="7594d-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7594d-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7594d-137">**Inapsohconstructor**</span><span class="sxs-lookup"><span data-stu-id="7594d-137">**INapSoHConstructor**</span></span>](inapsohconstructor.md)
</dt> </dl>

 

 





