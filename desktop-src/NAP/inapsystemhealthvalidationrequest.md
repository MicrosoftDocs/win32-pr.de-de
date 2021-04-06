---
title: Inapsystemhealthvalidationrequest-Schnittstelle (napsystemhealthvalidator. h)
description: Werden zur Unterstützung von Systemintegritäts-Validierungs Steuerelementen verwendet, die vom Anwendungsentwickler definiert werden.
ms.assetid: faa91ff5-49f5-4aec-81d7-02ec59274f23
keywords:
- Inapsystemhealthvalidationrequest-Schnittstelle NAP
- Inapsystemhealthvalidationrequest-Schnittstelle NAP, beschrieben
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf09f93e00401251a3d0e2296323edeb84ad6007
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743536"
---
# <a name="inapsystemhealthvalidationrequest-interface"></a><span data-ttu-id="e1858-105">Inapsystemhealthvalidationrequest-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="e1858-105">INapSystemHealthValidationRequest interface</span></span>

> [!Note]  
> <span data-ttu-id="e1858-106">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e1858-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="e1858-107">Die **inapsystemhealthvalidationrequest** -Schnittstelle stellt Methoden bereit, die zur Unterstützung von Systemintegritäts-Validierungs Steuerelementen verwendet werden, die vom Anwendungsentwickler definiert werden.</span><span class="sxs-lookup"><span data-stu-id="e1858-107">The **INapSystemHealthValidationRequest** interface provides methods that are used to support system health validators which are defined by the application developer.</span></span>

> [!Note]  
> <span data-ttu-id="e1858-108">[**INapSystemHealthValidationRequest2**](inapsystemhealthvalidationrequest2.md) erbt alle Methoden dieser Schnittstelle und sollte stattdessen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e1858-108">[**INapSystemHealthValidationRequest2**](inapsystemhealthvalidationrequest2.md) inherits all the methods of this interface and should be used instead.</span></span>

 

## <a name="members"></a><span data-ttu-id="e1858-109">Member</span><span class="sxs-lookup"><span data-stu-id="e1858-109">Members</span></span>

<span data-ttu-id="e1858-110">Die **inapsystemhealthvalidationrequest** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="e1858-110">The **INapSystemHealthValidationRequest** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="e1858-111">**Inapsystemhealthvalidationrequest** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="e1858-111">**INapSystemHealthValidationRequest** also has these types of members:</span></span>

-   [<span data-ttu-id="e1858-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="e1858-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="e1858-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="e1858-113">Methods</span></span>

<span data-ttu-id="e1858-114">Die **inapsystemhealthvalidationrequest** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="e1858-114">The **INapSystemHealthValidationRequest** interface has these methods.</span></span>



| <span data-ttu-id="e1858-115">Methode</span><span class="sxs-lookup"><span data-stu-id="e1858-115">Method</span></span>                                                                                                                               | <span data-ttu-id="e1858-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e1858-116">Description</span></span>                                                                                                           |
|:-------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e1858-117">**Inapsystemhealthvalidationrequest:: getcorrelationid**</span><span class="sxs-lookup"><span data-stu-id="e1858-117">**INapSystemHealthValidationRequest::GetCorrelationId**</span></span>](inapsystemhealthvalidationrequest-getcorrelationid-method.md)             | <span data-ttu-id="e1858-118">Wird von Validierungs Steuerelemente verwendet, um die Korrelations-ID abzurufen.</span><span class="sxs-lookup"><span data-stu-id="e1858-118">Used by validators to retrieve the correlation ID.</span></span> <span data-ttu-id="e1858-119">Das Validierungs Steuerelement muss diese Informationen dann protokollieren.</span><span class="sxs-lookup"><span data-stu-id="e1858-119">The validator must then log this information.</span></span><br/>           |
| [<span data-ttu-id="e1858-120">**Inapsystemhealthvalidationrequest:: GetMachineName**</span><span class="sxs-lookup"><span data-stu-id="e1858-120">**INapSystemHealthValidationRequest::GetMachineName**</span></span>](inapsystemhealthvalidationrequest-getmachinename-method.md)                 | <span data-ttu-id="e1858-121">Wird von Validierungs Steuerelemente verwendet, um den Computernamen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="e1858-121">Used by validators to retrieve the machine name.</span></span> <span data-ttu-id="e1858-122">Das Validierungs Steuerelement muss diese Informationen dann protokollieren.</span><span class="sxs-lookup"><span data-stu-id="e1858-122">The validator must then log this information.</span></span><br/>             |
| [<span data-ttu-id="e1858-123">**Inapsystemhealthvalidationrequest:: getprivatedata**</span><span class="sxs-lookup"><span data-stu-id="e1858-123">**INapSystemHealthValidationRequest::GetPrivateData**</span></span>](inapsystemhealthvalidationrequest-getprivatedata-method.md)                 | <span data-ttu-id="e1858-124">Ermöglicht dem napserver das Abrufen von Zustandsinformationen.</span><span class="sxs-lookup"><span data-stu-id="e1858-124">Allows the NapServer to retrieve state information.</span></span><br/>                                                        |
| [<span data-ttu-id="e1858-125">**Inapsystemhealthvalidationrequest:: getsohrequest**</span><span class="sxs-lookup"><span data-stu-id="e1858-125">**INapSystemHealthValidationRequest::GetSoHRequest**</span></span>](inapsystemhealthvalidationrequest-getsohrequest-method.md)                   | <span data-ttu-id="e1858-126">Ermöglicht Validierungs Steuerelementen das Abrufen und Validieren der sohrequest-Informationen.</span><span class="sxs-lookup"><span data-stu-id="e1858-126">Allows Validators to retrieve and validate the SoHRequest information.</span></span><br/>                                     |
| [<span data-ttu-id="e1858-127">**Inapsystemhealthvalidationrequest:: getsohresponse**</span><span class="sxs-lookup"><span data-stu-id="e1858-127">**INapSystemHealthValidationRequest::GetSoHResponse**</span></span>](inapsystemhealthvalidationrequest-getsohresponse-method.md)                 | <span data-ttu-id="e1858-128">Ruft das sohresponse-Objekt ab.</span><span class="sxs-lookup"><span data-stu-id="e1858-128">Gets the SoHResponse object.</span></span><br/>                                                                               |
| [<span data-ttu-id="e1858-129">**Inapsystemhealthvalidationrequest:: getstringcorrelationid**</span><span class="sxs-lookup"><span data-stu-id="e1858-129">**INapSystemHealthValidationRequest::GetStringCorrelationId**</span></span>](inapsystemhealthvalidationrequest-getstringcorrelationid-method.md) | <span data-ttu-id="e1858-130">Wird von Validierungs Steuerelemente zum Abrufen eines eindeutigen Exchange-Bezeichners verwendet.</span><span class="sxs-lookup"><span data-stu-id="e1858-130">Used by validators to retrieve a unique exchange identifier.</span></span> <span data-ttu-id="e1858-131">Das Validierungs Steuerelement muss diese Informationen dann protokollieren.</span><span class="sxs-lookup"><span data-stu-id="e1858-131">The validator must then log this information.</span></span><br/> |
| [<span data-ttu-id="e1858-132">**Inapsystemhealthvalidationrequest:: setprivatedata**</span><span class="sxs-lookup"><span data-stu-id="e1858-132">**INapSystemHealthValidationRequest::SetPrivateData**</span></span>](inapsystemhealthvalidationrequest-setprivatedata-method.md)                 | <span data-ttu-id="e1858-133">Ermöglicht dem napserver das Speichern von Zustandsinformationen.</span><span class="sxs-lookup"><span data-stu-id="e1858-133">Allows the NapServer to store state information.</span></span><br/>                                                           |
| [<span data-ttu-id="e1858-134">**Inapsystemhealthvalidationrequest:: setsohresponse**</span><span class="sxs-lookup"><span data-stu-id="e1858-134">**INapSystemHealthValidationRequest::SetSoHResponse**</span></span>](inapsystemhealthvalidationrequest-setsohresponse-method.md)                 | <span data-ttu-id="e1858-135">Ermöglicht Validierungs Steuerelementen das Festlegen der sohresponse.</span><span class="sxs-lookup"><span data-stu-id="e1858-135">Allows validators to set the SoHResponse.</span></span><br/>                                                                  |



 

## <a name="requirements"></a><span data-ttu-id="e1858-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e1858-136">Requirements</span></span>



| <span data-ttu-id="e1858-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e1858-137">Requirement</span></span> | <span data-ttu-id="e1858-138">Wert</span><span class="sxs-lookup"><span data-stu-id="e1858-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1858-139">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e1858-139">Minimum supported client</span></span><br/> | <span data-ttu-id="e1858-140">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="e1858-140">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="e1858-141">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e1858-141">Minimum supported server</span></span><br/> | <span data-ttu-id="e1858-142">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e1858-142">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e1858-143">Header</span><span class="sxs-lookup"><span data-stu-id="e1858-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="e1858-144"><dt>Napsystemhealthvalidator. h</dt></span><span class="sxs-lookup"><span data-stu-id="e1858-144"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="e1858-145">IDL</span><span class="sxs-lookup"><span data-stu-id="e1858-145">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e1858-146"><dt>Napsystemhealthvalidator. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e1858-146"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |
| <span data-ttu-id="e1858-147">DLL</span><span class="sxs-lookup"><span data-stu-id="e1858-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e1858-148"><dt>Qshvhost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e1858-148"><dt>Qshvhost.dll</dt></span></span> </dl>                 |



## <a name="see-also"></a><span data-ttu-id="e1858-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e1858-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1858-150">NAP-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="e1858-150">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="e1858-151">NAP-Referenz</span><span class="sxs-lookup"><span data-stu-id="e1858-151">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

