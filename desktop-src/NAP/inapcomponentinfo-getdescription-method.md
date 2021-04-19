---
title: Inapcomponentinfo GetDescription-Methode (napcommon. h)
description: Wird vom NAP-System verwendet, um die Beschreibung eines Integritäts Clients zu erhalten.
ms.assetid: f8d1d5ea-0de6-426d-90eb-b035b5bd0bfd
keywords:
- GetDescription-Methode NAP
- GetDescription-Methode NAP, inapcomponentinfo-Schnittstelle
- Inapcomponentinfo-Schnittstelle NAP, GetDescription-Methode
topic_type:
- apiref
api_name:
- INapComponentInfo.GetDescription
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 499aee6f7805925cc68c08b580db7b1b72763165
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341778"
---
# <a name="inapcomponentinfogetdescription-method"></a><span data-ttu-id="db536-106">Inapcomponentinfo:: GetDescription-Methode</span><span class="sxs-lookup"><span data-stu-id="db536-106">INapComponentInfo::GetDescription method</span></span>

> [!Note]  
> <span data-ttu-id="db536-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="db536-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="db536-108">Die **inapcomponentinfo:: GetDescription** -Rückruf Methode wird vom NAP-System verwendet, um die Beschreibung eines Integritäts Clients zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="db536-108">The **INapComponentInfo::GetDescription** callback method is used by the NAP System to get the description of a health client.</span></span>

## <a name="syntax"></a><span data-ttu-id="db536-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="db536-109">Syntax</span></span>


```C++
HRESULT GetDescription(
  [out] MessageId *description
);
```



## <a name="parameters"></a><span data-ttu-id="db536-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="db536-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db536-111">*Beschreibung* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="db536-111">*description* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="db536-112">Ein Zeiger auf eine [**MessageId**](nap-datatypes.md) , die die Ressourcen-ID der Beschreibung enthält.</span><span class="sxs-lookup"><span data-stu-id="db536-112">A pointer to a [**MessageId**](nap-datatypes.md) that contains the resource ID of the description.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db536-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="db536-113">Return value</span></span>

<span data-ttu-id="db536-114">Gibt einen dieser Fehlercodes basierend auf dem Ergebnis dieses Vorgangs zurück.</span><span class="sxs-lookup"><span data-stu-id="db536-114">Return one of these error codes based on the result of this operation.</span></span>



| <span data-ttu-id="db536-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="db536-115">Return code</span></span>                                                                                     | <span data-ttu-id="db536-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="db536-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="db536-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="db536-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="db536-118">Der Vorgang ist erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="db536-118">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="db536-119"><dt>**E \_ Access verweigert**</dt></span><span class="sxs-lookup"><span data-stu-id="db536-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="db536-120">Berechtigungs Fehler, Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="db536-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="db536-121"><dt>**E \_ Outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="db536-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="db536-122">System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="db536-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="db536-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="db536-123">Requirements</span></span>



| <span data-ttu-id="db536-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="db536-124">Requirement</span></span> | <span data-ttu-id="db536-125">Wert</span><span class="sxs-lookup"><span data-stu-id="db536-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="db536-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="db536-126">Minimum supported client</span></span><br/> | <span data-ttu-id="db536-127">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="db536-127">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="db536-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="db536-128">Minimum supported server</span></span><br/> | <span data-ttu-id="db536-129">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="db536-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="db536-130">Header</span><span class="sxs-lookup"><span data-stu-id="db536-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="db536-131"><dt>Napcommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="db536-131"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="db536-132">IDL</span><span class="sxs-lookup"><span data-stu-id="db536-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="db536-133"><dt>Napcommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="db536-133"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db536-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="db536-134">See also</span></span>

<dl> <span data-ttu-id="db536-135"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="db536-135"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="db536-136">**Inapcomponentinfo**</span><span class="sxs-lookup"><span data-stu-id="db536-136">**INapComponentInfo**</span></span>](inapcomponentinfo.md)
</dt> </dl>

 

 





