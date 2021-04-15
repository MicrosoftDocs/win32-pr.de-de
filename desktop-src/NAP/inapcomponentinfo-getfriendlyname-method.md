---
title: Inapcomponentinfo getfriendlyname-Methode (napcommon. h)
description: Wird vom NAP-System verwendet, um den anzeigen Amen eines Integritäts Clients zu erhalten.
ms.assetid: 28614f06-a250-4f92-abf2-422675efd8a0
keywords:
- Getfriendlyname-Methode NAP
- Getfriendlyname-Methode NAP, inapcomponentinfo-Schnittstelle
- Inapcomponentinfo Interface NAP, getfriendlyname-Methode
topic_type:
- apiref
api_name:
- INapComponentInfo.GetFriendlyName
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3848f8fb8365f91bceb5a44c498578f04a1776b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478915"
---
# <a name="inapcomponentinfogetfriendlyname-method"></a><span data-ttu-id="2d29c-106">Inapcomponentinfo:: getfriendlyname-Methode</span><span class="sxs-lookup"><span data-stu-id="2d29c-106">INapComponentInfo::GetFriendlyName method</span></span>

> [!Note]  
> <span data-ttu-id="2d29c-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2d29c-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="2d29c-108">Die **inapcomponentinfo:: getfriendlyname** -Rückruf Methode wird vom NAP-System verwendet, um den anzeigen Amen eines Integritäts Clients zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="2d29c-108">The **INapComponentInfo::GetFriendlyName** callback method is used by the NAP System to get the friendly name of a health client.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d29c-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="2d29c-109">Syntax</span></span>


```C++
HRESULT GetFriendlyName(
  [out] MessageId *friendlyName
);
```



## <a name="parameters"></a><span data-ttu-id="2d29c-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="2d29c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d29c-111">*FriendlyName* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="2d29c-111">*friendlyName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2d29c-112">Ein Zeiger auf eine [**MessageId**](nap-datatypes.md) , die die Ressourcen-ID des anzeigen Amens enthält.</span><span class="sxs-lookup"><span data-stu-id="2d29c-112">A pointer to a [**MessageId**](nap-datatypes.md) that contains the resource ID of the friendly name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d29c-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2d29c-113">Return value</span></span>

<span data-ttu-id="2d29c-114">Gibt einen dieser Fehlercodes basierend auf dem Ergebnis dieses Vorgangs zurück.</span><span class="sxs-lookup"><span data-stu-id="2d29c-114">Return one of these error codes based on the result of this operation.</span></span>



| <span data-ttu-id="2d29c-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="2d29c-115">Return code</span></span>                                                                                     | <span data-ttu-id="2d29c-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2d29c-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="2d29c-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="2d29c-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="2d29c-118">Der Vorgang ist erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="2d29c-118">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="2d29c-119"><dt>**E \_ Access verweigert**</dt></span><span class="sxs-lookup"><span data-stu-id="2d29c-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="2d29c-120">Berechtigungs Fehler, Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="2d29c-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="2d29c-121"><dt>**E \_ Outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="2d29c-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="2d29c-122">System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="2d29c-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="2d29c-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2d29c-123">Requirements</span></span>



| <span data-ttu-id="2d29c-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2d29c-124">Requirement</span></span> | <span data-ttu-id="2d29c-125">Wert</span><span class="sxs-lookup"><span data-stu-id="2d29c-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d29c-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2d29c-126">Minimum supported client</span></span><br/> | <span data-ttu-id="2d29c-127">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2d29c-127">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="2d29c-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2d29c-128">Minimum supported server</span></span><br/> | <span data-ttu-id="2d29c-129">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2d29c-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="2d29c-130">Header</span><span class="sxs-lookup"><span data-stu-id="2d29c-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="2d29c-131"><dt>Napcommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="2d29c-131"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="2d29c-132">IDL</span><span class="sxs-lookup"><span data-stu-id="2d29c-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2d29c-133"><dt>Napcommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2d29c-133"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d29c-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2d29c-134">See also</span></span>

<dl> <span data-ttu-id="2d29c-135"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="2d29c-135"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="2d29c-136">**Inapcomponentinfo**</span><span class="sxs-lookup"><span data-stu-id="2d29c-136">**INapComponentInfo**</span></span>](inapcomponentinfo.md)
</dt> </dl>

 

 





