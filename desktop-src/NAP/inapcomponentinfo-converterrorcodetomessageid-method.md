---
title: Inapcomponentinfo converterrorcodetomess ageid-Methode (napcommon. h)
description: Wird vom NAP-System verwendet, um anzufordern, dass der Integritäts Client einen HRESULT-Fehlercode in eine Nachrichten-ID konvertiert.
ms.assetid: 760dd039-5b9c-4227-9939-ad6ea23f5b81
keywords:
- Converterrorcodetomess ageid-Methode NAP
- Converterrorcodetomess ageid-Methode NAP, inapcomponentinfo-Schnittstelle
- Inapcomponentinfo-Schnittstelle NAP, converterrorcodetomess ageid-Methode
topic_type:
- apiref
api_name:
- INapComponentInfo.ConvertErrorCodeToMessageId
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7ed8eee06ed6bd553ffcce68e76e375dd706238
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478918"
---
# <a name="inapcomponentinfoconverterrorcodetomessageid-method"></a><span data-ttu-id="6ae18-106">Inapcomponentinfo:: converterrorcodetomess ageid-Methode</span><span class="sxs-lookup"><span data-stu-id="6ae18-106">INapComponentInfo::ConvertErrorCodeToMessageId method</span></span>

> [!Note]  
> <span data-ttu-id="6ae18-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6ae18-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="6ae18-108">Die **inapcomponentinfo:: converterrorcodetomesageid** -Rückruf Methode wird vom NAP-System verwendet, um anzufordern, dass der Integritäts Client einen HRESULT-Fehlercode in eine Nachrichten-ID konvertiert.</span><span class="sxs-lookup"><span data-stu-id="6ae18-108">The **INapComponentInfo::ConvertErrorCodeToMessageId** callback method is used by the NAP System to request the health client convert an HRESULT error code into a message ID.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ae18-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="6ae18-109">Syntax</span></span>


```C++
HRESULT ConvertErrorCodeToMessageId(
  [in]  HRESULT   errorCode,
  [out] MessageId *msgId
);
```



## <a name="parameters"></a><span data-ttu-id="6ae18-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="6ae18-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ae18-111">*errorCode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6ae18-111">*errorCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ae18-112">Der [**Fehlercode**](nap-error-constants.md) aus dem NAP-System, der in eine **MessageId** konvertiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="6ae18-112">The [**error code**](nap-error-constants.md) from the NAP System that is to be converted into a **MessageId**.</span></span>

</dd> <dt>

<span data-ttu-id="6ae18-113">*msgid* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="6ae18-113">*msgId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6ae18-114">Ein Zeiger auf eine [**MessageId**](nap-datatypes.md) , die die Ressourcen-ID der entsprechenden lokalisierten Zeichenfolge enthält.</span><span class="sxs-lookup"><span data-stu-id="6ae18-114">A pointer to a [**MessageId**](nap-datatypes.md) that contains the resource ID of the corresponding localized string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ae18-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6ae18-115">Return value</span></span>

<span data-ttu-id="6ae18-116">Gibt einen dieser Fehlercodes basierend auf dem Ergebnis dieses Vorgangs zurück.</span><span class="sxs-lookup"><span data-stu-id="6ae18-116">Return one of these error codes based on the result of this operation.</span></span>



| <span data-ttu-id="6ae18-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="6ae18-117">Return code</span></span>                                                                                     | <span data-ttu-id="6ae18-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6ae18-118">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="6ae18-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6ae18-119"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="6ae18-120">Der Vorgang ist erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="6ae18-120">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="6ae18-121"><dt>**E \_ Access verweigert**</dt></span><span class="sxs-lookup"><span data-stu-id="6ae18-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="6ae18-122">Berechtigungs Fehler, Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="6ae18-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="6ae18-123"><dt>**E \_ Outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="6ae18-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="6ae18-124">System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="6ae18-124">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6ae18-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6ae18-125">Remarks</span></span>

<span data-ttu-id="6ae18-126">Die zurückgegebene **MessageId** wird vom NAP-System verwendet, um eine lokalisierte Zeichenfolge abzurufen.</span><span class="sxs-lookup"><span data-stu-id="6ae18-126">The returned **MessageId** is used by the NAP System to retrieve a localized string.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ae18-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6ae18-127">Requirements</span></span>



| <span data-ttu-id="6ae18-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6ae18-128">Requirement</span></span> | <span data-ttu-id="6ae18-129">Wert</span><span class="sxs-lookup"><span data-stu-id="6ae18-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ae18-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6ae18-130">Minimum supported client</span></span><br/> | <span data-ttu-id="6ae18-131">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6ae18-131">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="6ae18-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6ae18-132">Minimum supported server</span></span><br/> | <span data-ttu-id="6ae18-133">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6ae18-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="6ae18-134">Header</span><span class="sxs-lookup"><span data-stu-id="6ae18-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ae18-135"><dt>Napcommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ae18-135"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="6ae18-136">IDL</span><span class="sxs-lookup"><span data-stu-id="6ae18-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6ae18-137"><dt>Napcommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6ae18-137"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ae18-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6ae18-138">See also</span></span>

<dl> <span data-ttu-id="6ae18-139"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="6ae18-139"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="6ae18-140">**Inapcomponentinfo**</span><span class="sxs-lookup"><span data-stu-id="6ae18-140">**INapComponentInfo**</span></span>](inapcomponentinfo.md)
</dt> </dl>

 

 





