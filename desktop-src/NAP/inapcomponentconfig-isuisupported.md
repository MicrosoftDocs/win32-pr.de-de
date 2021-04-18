---
title: Inapcomponentconfig isuisupported-Methode (napcommon. h)
description: Gibt an, ob die Komponente eine angepasste Benutzeroberfläche unterstützt.
ms.assetid: 044f8014-f041-4e9c-922a-2691b799ba84
keywords:
- Isuisupported-Methode NAP
- Isuisupported-Methode, NAP, inapcomponentconfig-Schnittstelle
- Inapcomponentconfig-Schnittstelle NAP, isuisupported-Methode
topic_type:
- apiref
api_name:
- INapComponentConfig.IsUISupported
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab7d3f6b87ba5e483b466e6746f0f63d039cb205
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337324"
---
# <a name="inapcomponentconfigisuisupported-method"></a><span data-ttu-id="9ff0f-106">Inapcomponentconfig:: isuisupported-Methode</span><span class="sxs-lookup"><span data-stu-id="9ff0f-106">INapComponentConfig::IsUISupported method</span></span>

> [!Note]  
> <span data-ttu-id="9ff0f-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9ff0f-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="9ff0f-108">Die **isuisupported** -Methode gibt an, ob die Komponente eine angepasste Benutzeroberfläche unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9ff0f-108">The **IsUISupported** method specifies whether the component supports a customized user interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ff0f-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="9ff0f-109">Syntax</span></span>


```C++
HRESULT IsUISupported(
  [out] BOOL *isSupported
) const;
```



## <a name="parameters"></a><span data-ttu-id="9ff0f-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="9ff0f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ff0f-111">*IsSupported* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="9ff0f-111">*isSupported* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9ff0f-112">Ein Zeiger auf einen booleschen Wert, der auf **true** festgelegt ist, wenn die Komponente eine angepasste Benutzeroberfläche unterstützt, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="9ff0f-112">A pointer to a BOOL that is set to **TRUE** if the component supports a customized user interface and **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ff0f-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9ff0f-113">Return value</span></span>

<span data-ttu-id="9ff0f-114">Gibt basierend auf dem Ergebnis dieses Vorgangs einen der folgenden Fehlercodes zurück.</span><span class="sxs-lookup"><span data-stu-id="9ff0f-114">Returns one of the following error codes based on the result of this operation.</span></span>



| <span data-ttu-id="9ff0f-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="9ff0f-115">Return code</span></span>                                                                                     | <span data-ttu-id="9ff0f-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9ff0f-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="9ff0f-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="9ff0f-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="9ff0f-118">Der Vorgang ist erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="9ff0f-118">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="9ff0f-119"><dt>**E \_ Access verweigert**</dt></span><span class="sxs-lookup"><span data-stu-id="9ff0f-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="9ff0f-120">Berechtigungs Fehler, Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="9ff0f-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="9ff0f-121"><dt>**E \_ Outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="9ff0f-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="9ff0f-122">System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="9ff0f-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9ff0f-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9ff0f-123">Remarks</span></span>

<span data-ttu-id="9ff0f-124">Die angepasste Benutzeroberfläche einer Komponente sollte mithilfe von [**inapcomponentconfig:: invokeui**](inapcomponentconfig-invokeui.md)gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="9ff0f-124">A component's customized user interface should be launched using [**INapComponentConfig::InvokeUI**](inapcomponentconfig-invokeui.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9ff0f-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9ff0f-125">Requirements</span></span>



| <span data-ttu-id="9ff0f-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9ff0f-126">Requirement</span></span> | <span data-ttu-id="9ff0f-127">Wert</span><span class="sxs-lookup"><span data-stu-id="9ff0f-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ff0f-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9ff0f-128">Minimum supported client</span></span><br/> | <span data-ttu-id="9ff0f-129">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="9ff0f-129">None supported</span></span><br/>                                                                |
| <span data-ttu-id="9ff0f-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9ff0f-130">Minimum supported server</span></span><br/> | <span data-ttu-id="9ff0f-131">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9ff0f-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="9ff0f-132">Header</span><span class="sxs-lookup"><span data-stu-id="9ff0f-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ff0f-133"><dt>Napcommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ff0f-133"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="9ff0f-134">IDL</span><span class="sxs-lookup"><span data-stu-id="9ff0f-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9ff0f-135"><dt>Napcommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9ff0f-135"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ff0f-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9ff0f-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ff0f-137">**Inapcomponentconfig**</span><span class="sxs-lookup"><span data-stu-id="9ff0f-137">**INapComponentConfig**</span></span>](inapcomponentconfig.md)
</dt> <dt>

[<span data-ttu-id="9ff0f-138">**Inapcomponentconfig:: invokeui**</span><span class="sxs-lookup"><span data-stu-id="9ff0f-138">**INapComponentConfig::InvokeUI**</span></span>](inapcomponentconfig-invokeui.md)
</dt> </dl>

 

 





