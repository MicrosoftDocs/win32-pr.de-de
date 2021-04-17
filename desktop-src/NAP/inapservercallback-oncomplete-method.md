---
title: Inapservercallback OnComplete-Methode (napsystemhealthvalidator. h)
description: Wird von SHVs verwendet, um den Abschluss einer asynchronen Anforderung zu signalisieren.
ms.assetid: 959ee4ac-7c29-4013-a174-24abc6a580c7
keywords:
- OnComplete-Methode, NAP
- OnComplete-Methode, NAP, inapservercallback-Schnittstelle
- Inapservercallback-Schnittstelle NAP, OnComplete-Methode
topic_type:
- apiref
api_name:
- INapServerCallback.OnComplete
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ef846d3d9dc2d6618f0eca9f097d74222606eb4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479344"
---
# <a name="inapservercallbackoncomplete-method"></a><span data-ttu-id="f3a86-106">Inapservercallback:: OnComplete-Methode</span><span class="sxs-lookup"><span data-stu-id="f3a86-106">INapServerCallback::OnComplete method</span></span>

> [!Note]  
> <span data-ttu-id="f3a86-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f3a86-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="f3a86-108">Die **inapservercallback:: OnComplete** -Methode wird von SHVs verwendet, um den Abschluss einer asynchronen Anforderung zu signalisieren.</span><span class="sxs-lookup"><span data-stu-id="f3a86-108">The **INapServerCallback::OnComplete** method is used by SHVs to signal asynchronous request completion.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3a86-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="f3a86-109">Syntax</span></span>


```C++
HRESULT OnComplete(
  [in] INapSystemHealthValidationRequest *request,
  [in] HRESULT                           errorCode
);
```



## <a name="parameters"></a><span data-ttu-id="f3a86-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f3a86-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3a86-111">*Anforderung* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f3a86-111">*request* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3a86-112">Ein Zeiger auf ein [**inapsystemhealthvalidationrequest**](inapsystemhealthvalidationrequest.md) -Objekt, das eine Validierungs Anforderung darstellt.</span><span class="sxs-lookup"><span data-stu-id="f3a86-112">A pointer to an [**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md) object that represents a validation request.</span></span>

</dd> <dt>

<span data-ttu-id="f3a86-113">*errorCode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f3a86-113">*errorCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3a86-114">Ein [**NAP-Fehlercode**](nap-error-constants.md) , der den Grund angibt, warum die Überprüfung nicht ausgeführt werden konnte.</span><span class="sxs-lookup"><span data-stu-id="f3a86-114">A [**NAP error code**](nap-error-constants.md) that indicates the reason why the validation could not be performed.</span></span>

> [!Note]  
> <span data-ttu-id="f3a86-115">In der Regel wird der Rückgabewert der Methode [**inapsystemhealthvalidationrequest:: setsohresponse**](inapsystemhealthvalidationrequest-setsohresponse-method.md) an diesen Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="f3a86-115">Typically, the return value of the [**INapSystemHealthValidationRequest::SetSoHResponse**](inapsystemhealthvalidationrequest-setsohresponse-method.md) method is passed to this parameter.</span></span> <span data-ttu-id="f3a86-116">Wenn **setsohresponse** jedoch aufgrund eines erneuten Verarbeitungs Fehlers nicht aufgerufen werden konnte, wird der Wert, der vom fehlerhaften Befehl zurückgegeben wurde, übermittelt.</span><span class="sxs-lookup"><span data-stu-id="f3a86-116">However, if **SetSoHResponse** could not be called due to a reprocessing failure, the value returned by the failed command is passed.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3a86-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f3a86-117">Return value</span></span>

<span data-ttu-id="f3a86-118">Es können auch andere com-spezifische Fehlercodes zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="f3a86-118">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="f3a86-119">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="f3a86-119">Return code</span></span>                                                                                     | <span data-ttu-id="f3a86-120">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f3a86-120">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="f3a86-121"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f3a86-121"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="f3a86-122">Vorgang erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="f3a86-122">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="f3a86-123"><dt>**E \_ Access verweigert**</dt></span><span class="sxs-lookup"><span data-stu-id="f3a86-123"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="f3a86-124">Berechtigungs Fehler, Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="f3a86-124">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="f3a86-125"><dt>**E \_ Outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="f3a86-125"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="f3a86-126">System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="f3a86-126">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f3a86-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f3a86-127">Remarks</span></span>

<span data-ttu-id="f3a86-128">Validators müssen S OK zurückgeben \_ , wenn die [**sohrequest**](/windows/win32/api/naptypes/ns-naptypes-soh) -Überprüfung abgeschlossen werden konnte, unabhängig davon, ob der **sohrequest** die Integritätsprüfung bestanden hat.</span><span class="sxs-lookup"><span data-stu-id="f3a86-128">Validators must return S\_OK if the [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) validation could be completed, regardless of whether the **SoHRequest** passed the health check.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3a86-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f3a86-129">Requirements</span></span>



| <span data-ttu-id="f3a86-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f3a86-130">Requirement</span></span> | <span data-ttu-id="f3a86-131">Wert</span><span class="sxs-lookup"><span data-stu-id="f3a86-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3a86-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f3a86-132">Minimum supported client</span></span><br/> | <span data-ttu-id="f3a86-133">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="f3a86-133">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="f3a86-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f3a86-134">Minimum supported server</span></span><br/> | <span data-ttu-id="f3a86-135">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f3a86-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f3a86-136">Header</span><span class="sxs-lookup"><span data-stu-id="f3a86-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="f3a86-137"><dt>Napsystemhealthvalidator. h</dt></span><span class="sxs-lookup"><span data-stu-id="f3a86-137"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="f3a86-138">IDL</span><span class="sxs-lookup"><span data-stu-id="f3a86-138">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f3a86-139"><dt>Napsystemhealthvalidator. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f3a86-139"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |
| <span data-ttu-id="f3a86-140">DLL</span><span class="sxs-lookup"><span data-stu-id="f3a86-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f3a86-141"><dt>Qshvhost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f3a86-141"><dt>Qshvhost.dll</dt></span></span> </dl>                 |



## <a name="see-also"></a><span data-ttu-id="f3a86-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f3a86-142">See also</span></span>

<dl> <span data-ttu-id="f3a86-143"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="f3a86-143"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="f3a86-144">**Inapservercallback**</span><span class="sxs-lookup"><span data-stu-id="f3a86-144">**INapServerCallback**</span></span>](inapservercallback.md)
</dt> <dt>

[<span data-ttu-id="f3a86-145">**Inapsystemhealthvalidationrequest**</span><span class="sxs-lookup"><span data-stu-id="f3a86-145">**INapSystemHealthValidationRequest**</span></span>](inapsystemhealthvalidationrequest.md)
</dt> </dl>

 

 





