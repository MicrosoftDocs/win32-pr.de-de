---
title: Inapcomponentinfo GetVersion-Methode (napcommon. h)
description: Wird vom NAP-System verwendet, um die Version eines Integritäts Clients zu erhalten.
ms.assetid: aabd13d9-d2ad-4554-a9f6-7845e6775ccd
keywords:
- GetVersion-Methode NAP
- GetVersion-Methode NAP, inapcomponentinfo-Schnittstelle
- Inapcomponentinfo Interface NAP, GetVersion-Methode
topic_type:
- apiref
api_name:
- INapComponentInfo.GetVersion
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa1d62c22acf778430bfc2f9dc0e969887c7b306
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519180"
---
# <a name="inapcomponentinfogetversion-method"></a><span data-ttu-id="b02af-106">Inapcomponentinfo:: GetVersion-Methode</span><span class="sxs-lookup"><span data-stu-id="b02af-106">INapComponentInfo::GetVersion method</span></span>

> [!Note]  
> <span data-ttu-id="b02af-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b02af-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="b02af-108">Die **inapcomponentinfo:: GetVersion** -Rückruf Methode wird vom NAP-System verwendet, um die Version eines Integritäts Clients zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="b02af-108">The **INapComponentInfo::GetVersion** callback method is used by the NAP System to get the version of a health client.</span></span>

## <a name="syntax"></a><span data-ttu-id="b02af-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="b02af-109">Syntax</span></span>


```C++
HRESULT GetVersion(
  [out] MessageId *version
);
```



## <a name="parameters"></a><span data-ttu-id="b02af-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="b02af-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b02af-111">*Version* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="b02af-111">*version* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b02af-112">Ein Zeiger auf eine [**MessageId**](nap-datatypes.md) , die die Ressourcen-ID der Version enthält.</span><span class="sxs-lookup"><span data-stu-id="b02af-112">A pointer to a [**MessageId**](nap-datatypes.md) that contains the resource ID of the version.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b02af-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b02af-113">Return value</span></span>

<span data-ttu-id="b02af-114">Gibt einen dieser Fehlercodes basierend auf dem Ergebnis dieses Vorgangs zurück.</span><span class="sxs-lookup"><span data-stu-id="b02af-114">Return one of these error codes based on the result of this operation.</span></span>



| <span data-ttu-id="b02af-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="b02af-115">Return code</span></span>                                                                                     | <span data-ttu-id="b02af-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b02af-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="b02af-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b02af-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="b02af-118">Der Vorgang ist erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="b02af-118">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="b02af-119"><dt>**E \_ Access verweigert**</dt></span><span class="sxs-lookup"><span data-stu-id="b02af-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="b02af-120">Berechtigungs Fehler, Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="b02af-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="b02af-121"><dt>**E \_ Outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="b02af-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="b02af-122">System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="b02af-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="b02af-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b02af-123">Requirements</span></span>



| <span data-ttu-id="b02af-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b02af-124">Requirement</span></span> | <span data-ttu-id="b02af-125">Wert</span><span class="sxs-lookup"><span data-stu-id="b02af-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b02af-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b02af-126">Minimum supported client</span></span><br/> | <span data-ttu-id="b02af-127">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b02af-127">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="b02af-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b02af-128">Minimum supported server</span></span><br/> | <span data-ttu-id="b02af-129">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b02af-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="b02af-130">Header</span><span class="sxs-lookup"><span data-stu-id="b02af-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="b02af-131"><dt>Napcommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="b02af-131"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="b02af-132">IDL</span><span class="sxs-lookup"><span data-stu-id="b02af-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b02af-133"><dt>Napcommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b02af-133"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b02af-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b02af-134">See also</span></span>

<dl> <span data-ttu-id="b02af-135"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="b02af-135"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="b02af-136">**Inapcomponentinfo**</span><span class="sxs-lookup"><span data-stu-id="b02af-136">**INapComponentInfo**</span></span>](inapcomponentinfo.md)
</dt> </dl>

 

 





