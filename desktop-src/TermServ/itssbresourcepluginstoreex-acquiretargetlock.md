---
title: Itssbresourcepluginstoreex acquiretargetlock-Methode
description: Sperrt ein Ziel.
ms.assetid: 76707f1d-1f13-4d81-8954-2acf05cda2cd
ms.tgt_platform: multiple
keywords:
- Acquiretargetlock-Methode Remotedesktopdienste
- Acquiretargetlock-Methode Remotedesktopdienste, itssbresourcepluginstoreex-Schnittstelle
- Itssbresourcepluginstoreex-Schnittstelle Remotedesktopdienste, acquiretargetlock-Methode
topic_type:
- apiref
api_name:
- ITsSbResourcePluginStoreEx.AcquireTargetLock
api_location:
- SbTsV.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c18be0a544ebcea2d2cecb40dcea3a08e4bd35b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103155"
---
# <a name="itssbresourcepluginstoreexacquiretargetlock-method"></a><span data-ttu-id="aec88-106">Itssbresourcepluginstoreex:: acquiretargetlock-Methode</span><span class="sxs-lookup"><span data-stu-id="aec88-106">ITsSbResourcePluginStoreEx::AcquireTargetLock method</span></span>

<span data-ttu-id="aec88-107">Sperrt ein Ziel.</span><span class="sxs-lookup"><span data-stu-id="aec88-107">Locks a target.</span></span>

## <a name="syntax"></a><span data-ttu-id="aec88-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="aec88-108">Syntax</span></span>


```C++
HRESULT AcquireTargetLock(
  [in]  BSTR     targetName,
  [in]  DWORD    dwTimeout,
  [out] IUnknown **ppContext
);
```



## <a name="parameters"></a><span data-ttu-id="aec88-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="aec88-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aec88-110">*TargetName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aec88-110">*targetName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aec88-111">Der Name des zu Sperr enden Ziels.</span><span class="sxs-lookup"><span data-stu-id="aec88-111">The name of the target to lock.</span></span>

</dd> <dt>

<span data-ttu-id="aec88-112">*dwtimeout* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aec88-112">*dwTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aec88-113">Das Timeout für den Vorgang in Millisekunden.</span><span class="sxs-lookup"><span data-stu-id="aec88-113">The timeout for the operation, in milliseconds.</span></span>

</dd> <dt>

<span data-ttu-id="aec88-114">*ppcontext* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="aec88-114">*ppContext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="aec88-115">Gibt einen Zeiger auf den Kontext der Sperre zurück.</span><span class="sxs-lookup"><span data-stu-id="aec88-115">Returns a pointer to the context of the lock.</span></span> <span data-ttu-id="aec88-116">Um die Sperre freizugeben, geben Sie diesen Zeiger auf die [**releasetargetlock**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-releasetargetlock) -Methode an.</span><span class="sxs-lookup"><span data-stu-id="aec88-116">To release the lock, supply this pointer to the [**ReleaseTargetLock**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-releasetargetlock) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aec88-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="aec88-117">Return value</span></span>

<span data-ttu-id="aec88-118">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="aec88-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="aec88-119">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="aec88-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="aec88-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="aec88-120">Remarks</span></span>

<span data-ttu-id="aec88-121">Nachdem die Sperre eingerichtet wurde, wird davon ausgegangen, dass der aufrufende Thread exklusiven Zugriff auf das Zielobjekt hat und daher kein anderer Thread (innerhalb desselben Computers) ihn aktualisieren kann.</span><span class="sxs-lookup"><span data-stu-id="aec88-121">After the lock is acquired, the calling thread is assumed to have exclusive access to the target object and therefore no other thread (within the same machine) can update it.</span></span> <span data-ttu-id="aec88-122">Daher muss der aufrufende Thread die [**releasetargetlock**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-releasetargetlock) -Methode aufrufen, sobald die erforderlichen Updates für das Zielobjekt vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="aec88-122">Therefore the calling thread must call the [**ReleaseTargetLock**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-releasetargetlock) method as soon as it has made the necessary updates to the target object.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="aec88-123">Diese Sperre verhindert nicht vollständig, dass Zielobjekte extern geändert werden, wenn mehr als ein Verbindungs Broker in der Bereitstellung vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="aec88-123">this lock does not completely prevent target objects from being modified externally if more than one Connection Broker exists in the deployment.</span></span> <span data-ttu-id="aec88-124">Der aufrufende Thread muss darauf vorbereitet sein, einen Fehler ordnungsgemäß zu behandeln und das Ziel Update zu wiederholen.</span><span class="sxs-lookup"><span data-stu-id="aec88-124">The calling thread must be prepared to handle a failure gracefully and retry the target update.</span></span>

 

<span data-ttu-id="aec88-125">Diese Methode ist unter Windows Server 2012 R2 mit installiertem [KB3091411](https://support.microsoft.com/kb/3091411) in der [**itssbresourcepluginstoreex**](itssbresourcepluginstoreex.md) -Schnittstelle verfügbar.</span><span class="sxs-lookup"><span data-stu-id="aec88-125">This method is available on Windows Server 2012 R2 with [KB3091411](https://support.microsoft.com/kb/3091411) installed in the [**ITsSbResourcePluginStoreEx**](itssbresourcepluginstoreex.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="aec88-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aec88-126">Requirements</span></span>



| <span data-ttu-id="aec88-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="aec88-127">Requirement</span></span> | <span data-ttu-id="aec88-128">Wert</span><span class="sxs-lookup"><span data-stu-id="aec88-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="aec88-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="aec88-129">Minimum supported client</span></span><br/> | <span data-ttu-id="aec88-130">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="aec88-130">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="aec88-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="aec88-131">Minimum supported server</span></span><br/> | <span data-ttu-id="aec88-132">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="aec88-132">Windows Server 2012 R2</span></span><br/>                                                             |
| <span data-ttu-id="aec88-133">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="aec88-133">End of server support</span></span><br/>    | <span data-ttu-id="aec88-134">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="aec88-134">Windows Server 2012 R2</span></span><br/>                                                             |
| <span data-ttu-id="aec88-135">IDL</span><span class="sxs-lookup"><span data-stu-id="aec88-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="aec88-136"><dt>Sbtsv. idl</dt></span><span class="sxs-lookup"><span data-stu-id="aec88-136"><dt>SbTsV.idl</dt></span></span> </dl>          |
| <span data-ttu-id="aec88-137">IID</span><span class="sxs-lookup"><span data-stu-id="aec88-137">IID</span></span><br/>                      | <span data-ttu-id="aec88-138">IID \_ itssbresourcepluginstoreex ist als 80b83ffd-625d-11e5-bea1-a0481c7e9064 definiert</span><span class="sxs-lookup"><span data-stu-id="aec88-138">IID\_ITsSbResourcePluginStoreEx is defined as 80b83ffd-625d-11e5-bea1-a0481c7e9064</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="aec88-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aec88-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aec88-140">**Itssbresourcepluginstoreex**</span><span class="sxs-lookup"><span data-stu-id="aec88-140">**ITsSbResourcePluginStoreEx**</span></span>](itssbresourcepluginstoreex.md)
</dt> </dl>

 

 





