---
title: Inapcomponentinfo GetLocalizedString-Methode (napcommon. h)
description: Wird vom NAP-System verwendet, um lokalisierte Zeichen folgen zu erhalten.
ms.assetid: ad5be180-6329-4c91-b4d1-871a4d83c323
keywords:
- GetLocalizedString-Methode NAP
- GetLocalizedString-Methode NAP, inapcomponentinfo-Schnittstelle
- Inapcomponentinfo-Schnittstelle NAP, GetLocalizedString-Methode
topic_type:
- apiref
api_name:
- INapComponentInfo.GetLocalizedString
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 781e4e8c93f58039c72a98f40a529243e5722d23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957232"
---
# <a name="inapcomponentinfogetlocalizedstring-method"></a><span data-ttu-id="03b9d-106">Inapcomponentinfo:: GetLocalizedString-Methode</span><span class="sxs-lookup"><span data-stu-id="03b9d-106">INapComponentInfo::GetLocalizedString method</span></span>

> [!Note]  
> <span data-ttu-id="03b9d-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="03b9d-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="03b9d-108">Die **inapcomponentinfo:: GetLocalizedString** -Rückruf Methode wird vom NAP-System verwendet, um lokalisierte Zeichen folgen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="03b9d-108">The **INapComponentInfo::GetLocalizedString** callback method is used by the NAP System to get localized strings.</span></span>

## <a name="syntax"></a><span data-ttu-id="03b9d-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="03b9d-109">Syntax</span></span>


```C++
HRESULT GetLocalizedString(
  [in]  MessageId     msgId,
  [out] CountedString **string
);
```



## <a name="parameters"></a><span data-ttu-id="03b9d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="03b9d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03b9d-111">*msgid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="03b9d-111">*msgId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03b9d-112">Eine [**MessageId**](nap-datatypes.md) , die die Ressourcen-ID der zu lokalisieren Zeichenfolge enthält.</span><span class="sxs-lookup"><span data-stu-id="03b9d-112">A [**MessageId**](nap-datatypes.md) that contains the resource ID of the string to localize.</span></span>

</dd> <dt>

<span data-ttu-id="03b9d-113">*Zeichenfolge* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="03b9d-113">*string* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="03b9d-114">Ein Zeiger auf einen Zeiger auf eine [**zählzeichenfolge**](/windows/win32/api/naptypes/ns-naptypes-countedstring) , die die lokalisierte Version der Nachricht enthält.</span><span class="sxs-lookup"><span data-stu-id="03b9d-114">A pointer to a pointer to a [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) that contains the localized version of the message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03b9d-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="03b9d-115">Return value</span></span>

<span data-ttu-id="03b9d-116">Gibt einen dieser Fehlercodes basierend auf dem Ergebnis dieses Vorgangs zurück.</span><span class="sxs-lookup"><span data-stu-id="03b9d-116">Return one of these error codes based on the result of this operation.</span></span>



| <span data-ttu-id="03b9d-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="03b9d-117">Return code</span></span>                                                                                     | <span data-ttu-id="03b9d-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="03b9d-118">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="03b9d-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="03b9d-119"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="03b9d-120">Der Vorgang ist erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="03b9d-120">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="03b9d-121"><dt>**E \_ Access verweigert**</dt></span><span class="sxs-lookup"><span data-stu-id="03b9d-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="03b9d-122">Berechtigungs Fehler, Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="03b9d-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="03b9d-123"><dt>**E \_ Outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="03b9d-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="03b9d-124">System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="03b9d-124">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="03b9d-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="03b9d-125">Remarks</span></span>

<span data-ttu-id="03b9d-126">Zeichen folgen sollten entsprechend der Sprach-ID des aufrufenden Threads lokalisiert werden.</span><span class="sxs-lookup"><span data-stu-id="03b9d-126">Strings should be localized according to the calling thread's language-id.</span></span>

## <a name="requirements"></a><span data-ttu-id="03b9d-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="03b9d-127">Requirements</span></span>



| <span data-ttu-id="03b9d-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="03b9d-128">Requirement</span></span> | <span data-ttu-id="03b9d-129">Wert</span><span class="sxs-lookup"><span data-stu-id="03b9d-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="03b9d-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="03b9d-130">Minimum supported client</span></span><br/> | <span data-ttu-id="03b9d-131">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="03b9d-131">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="03b9d-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="03b9d-132">Minimum supported server</span></span><br/> | <span data-ttu-id="03b9d-133">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="03b9d-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="03b9d-134">Header</span><span class="sxs-lookup"><span data-stu-id="03b9d-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="03b9d-135"><dt>Napcommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="03b9d-135"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="03b9d-136">IDL</span><span class="sxs-lookup"><span data-stu-id="03b9d-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="03b9d-137"><dt>Napcommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="03b9d-137"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03b9d-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="03b9d-138">See also</span></span>

<dl> <span data-ttu-id="03b9d-139"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="03b9d-139"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="03b9d-140">**Inapcomponentinfo**</span><span class="sxs-lookup"><span data-stu-id="03b9d-140">**INapComponentInfo**</span></span>](inapcomponentinfo.md)
</dt> </dl>

 

 





