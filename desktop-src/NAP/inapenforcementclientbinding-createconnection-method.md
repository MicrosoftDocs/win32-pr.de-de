---
title: Inapenforcementclientbinding-Methode "fiateconnetction" (napforcementclient. h)
description: Wird von enforcern zum Erstellen von Verbindungs Objekten verwendet.
ms.assetid: 4d31928f-1a10-4168-a53c-256cbbf3e5c9
keywords:
- Methode "deeconnetction" für NAP
- Anateconnetction-Methode NAP, inapenforcementclientbinding-Schnittstelle
- Inapenforcementclientbinding-Schnittstelle NAP, Methode "kreateconnetction"
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding.CreateConnection
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bf530b9fefd0e5b361f4f86ef2421712c750be9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040404"
---
# <a name="inapenforcementclientbindingcreateconnection-method"></a><span data-ttu-id="1d9e3-106">Inapenforcementclientbinding:: kreateconnetction-Methode</span><span class="sxs-lookup"><span data-stu-id="1d9e3-106">INapEnforcementClientBinding::CreateConnection method</span></span>

> [!Note]  
> <span data-ttu-id="1d9e3-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="1d9e3-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="1d9e3-108">Die **inapenforcementclientbinding:: kreateconnetction** -Factorymethode wird von enforcern zum Erstellen von Verbindungs Objekten verwendet.</span><span class="sxs-lookup"><span data-stu-id="1d9e3-108">The **INapEnforcementClientBinding::CreateConnection** factory method is used by enforcers to create connection objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d9e3-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="1d9e3-109">Syntax</span></span>


```C++
HRESULT CreateConnection(
  [out] INapEnforcementClientConnection **connection
);
```



## <a name="parameters"></a><span data-ttu-id="1d9e3-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="1d9e3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d9e3-111">*Verbindung* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="1d9e3-111">*connection* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1d9e3-112">Ein com-Zeiger auf eine neue [**inapenforcementclientconnection**](inapenforcementclientconnection.md) -Schnittstelle, die vom NAP-System zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="1d9e3-112">A COM pointer to a new [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) interface returned by the NAP system.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d9e3-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1d9e3-113">Return value</span></span>

<span data-ttu-id="1d9e3-114">Es können auch andere com-spezifische Fehlercodes zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="1d9e3-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="1d9e3-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="1d9e3-115">Return code</span></span>                                                                                     | <span data-ttu-id="1d9e3-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1d9e3-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="1d9e3-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1d9e3-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="1d9e3-118">Der Vorgang ist erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="1d9e3-118">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="1d9e3-119"><dt>**E \_ Access verweigert**</dt></span><span class="sxs-lookup"><span data-stu-id="1d9e3-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="1d9e3-120">Berechtigungs Fehler, Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="1d9e3-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="1d9e3-121"><dt>**E \_ Outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="1d9e3-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="1d9e3-122">System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="1d9e3-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1d9e3-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1d9e3-123">Remarks</span></span>

<span data-ttu-id="1d9e3-124">Der Erzwingungs Client muss die [**inapenforcementclientbinding:: Initialize**](inapenforcementclientbinding-initialize-method.md) -Methode aufrufen, bevor diese oder eine andere Methode der [**inapenforcementclientbinding**](inapenforcementclientbinding.md) -Schnittstelle aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="1d9e3-124">The enforcement client must call the [**INapEnforcementClientBinding::Initialize**](inapenforcementclientbinding-initialize-method.md) method before calling this or any other method of the [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d9e3-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1d9e3-125">Requirements</span></span>



| <span data-ttu-id="1d9e3-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1d9e3-126">Requirement</span></span> | <span data-ttu-id="1d9e3-127">Wert</span><span class="sxs-lookup"><span data-stu-id="1d9e3-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d9e3-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1d9e3-128">Minimum supported client</span></span><br/> | <span data-ttu-id="1d9e3-129">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1d9e3-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="1d9e3-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1d9e3-130">Minimum supported server</span></span><br/> | <span data-ttu-id="1d9e3-131">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1d9e3-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="1d9e3-132">Header</span><span class="sxs-lookup"><span data-stu-id="1d9e3-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="1d9e3-133"><dt>Napforcementclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="1d9e3-133"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="1d9e3-134">IDL</span><span class="sxs-lookup"><span data-stu-id="1d9e3-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1d9e3-135"><dt>Napforcementclient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1d9e3-135"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="1d9e3-136">DLL</span><span class="sxs-lookup"><span data-stu-id="1d9e3-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1d9e3-137"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1d9e3-137"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="1d9e3-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1d9e3-138">See also</span></span>

<dl> <span data-ttu-id="1d9e3-139"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="1d9e3-139"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="1d9e3-140">**Inapenforcementclientbinding**</span><span class="sxs-lookup"><span data-stu-id="1d9e3-140">**INapEnforcementClientBinding**</span></span>](inapenforcementclientbinding.md)
</dt> <dt>

[<span data-ttu-id="1d9e3-141">**Inapenforcementclientconnection**</span><span class="sxs-lookup"><span data-stu-id="1d9e3-141">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





