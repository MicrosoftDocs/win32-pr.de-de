---
title: Inapcomponentconfig invokeui-Methode (napcommon. h)
description: Hiermit wird eine angepasste Benutzeroberfläche für eine Komponente der System Integritätsprüfung (System Health Prüfungs, SHV) gestartet
ms.assetid: da2a5e3e-bc17-4984-bdbe-b72e9e710a9d
keywords:
- Invokeui-Methode NAP
- Invokeui-Methode NAP, inapcomponentconfig-Schnittstelle
- Inapcomponentconfig-Schnittstelle NAP, invokeui-Methode
topic_type:
- apiref
api_name:
- INapComponentConfig.InvokeUI
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2dd86d683365286fc2130c1ac9edf21ff075d61a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949674"
---
# <a name="inapcomponentconfiginvokeui-method"></a><span data-ttu-id="c2ebe-106">Inapcomponentconfig:: invokeui-Methode</span><span class="sxs-lookup"><span data-stu-id="c2ebe-106">INapComponentConfig::InvokeUI method</span></span>

> [!Note]  
> <span data-ttu-id="c2ebe-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c2ebe-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="c2ebe-108">Die **invokeui** -Methode gestartet eine angepasste Benutzeroberfläche für eine Komponente der System Integritätsprüfung (System Health Prüfungs, SHV).</span><span class="sxs-lookup"><span data-stu-id="c2ebe-108">The **InvokeUI** method launches a customized user interface for a system health validator (SHV) component.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2ebe-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="c2ebe-109">Syntax</span></span>


```C++
HRESULT InvokeUI(
  [in] HWND hwndParent
) const;
```



## <a name="parameters"></a><span data-ttu-id="c2ebe-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="c2ebe-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2ebe-111">*hwndParent* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c2ebe-111">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2ebe-112">Ein Handle für das übergeordnete Fenster oder Besitzer Fenster.</span><span class="sxs-lookup"><span data-stu-id="c2ebe-112">A handle to the parent or owner window.</span></span> <span data-ttu-id="c2ebe-113">Ein gültiges Fenster Handle muss angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c2ebe-113">A valid window handle must be supplied.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2ebe-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c2ebe-114">Return value</span></span>

<span data-ttu-id="c2ebe-115">Gibt basierend auf dem Ergebnis dieses Vorgangs einen der folgenden Fehlercodes zurück.</span><span class="sxs-lookup"><span data-stu-id="c2ebe-115">Returns one of the following error codes based on the result of this operation.</span></span>



| <span data-ttu-id="c2ebe-116">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="c2ebe-116">Return code</span></span>                                                                                     | <span data-ttu-id="c2ebe-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c2ebe-117">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="c2ebe-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c2ebe-118"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="c2ebe-119">Der Vorgang ist erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="c2ebe-119">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="c2ebe-120"><dt>**E \_ Access verweigert**</dt></span><span class="sxs-lookup"><span data-stu-id="c2ebe-120"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="c2ebe-121">Berechtigungs Fehler, Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="c2ebe-121">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="c2ebe-122"><dt>**E \_ Outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="c2ebe-122"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="c2ebe-123">System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="c2ebe-123">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="c2ebe-124"><dt>**E \_ notimpl**</dt></span><span class="sxs-lookup"><span data-stu-id="c2ebe-124"><dt>**E\_NOTIMPL**</dt></span></span> </dl>       | <span data-ttu-id="c2ebe-125">Der SHV unterstützt keine angepasste Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="c2ebe-125">The SHV does not support a customized UI.</span></span><br/>               |



 

## <a name="remarks"></a><span data-ttu-id="c2ebe-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c2ebe-126">Remarks</span></span>

<span data-ttu-id="c2ebe-127">Dieser Methodenaufrufe sollte blockieren, bis die SHV-Benutzeroberfläche beendet wird.</span><span class="sxs-lookup"><span data-stu-id="c2ebe-127">This method call should block until the SHV user interface exits.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2ebe-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c2ebe-128">Requirements</span></span>



| <span data-ttu-id="c2ebe-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c2ebe-129">Requirement</span></span> | <span data-ttu-id="c2ebe-130">Wert</span><span class="sxs-lookup"><span data-stu-id="c2ebe-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2ebe-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c2ebe-131">Minimum supported client</span></span><br/> | <span data-ttu-id="c2ebe-132">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="c2ebe-132">None supported</span></span><br/>                                                                |
| <span data-ttu-id="c2ebe-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c2ebe-133">Minimum supported server</span></span><br/> | <span data-ttu-id="c2ebe-134">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c2ebe-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="c2ebe-135">Header</span><span class="sxs-lookup"><span data-stu-id="c2ebe-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2ebe-136"><dt>Napcommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2ebe-136"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="c2ebe-137">IDL</span><span class="sxs-lookup"><span data-stu-id="c2ebe-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c2ebe-138"><dt>Napcommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c2ebe-138"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2ebe-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c2ebe-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2ebe-140">**Inapcomponentconfig**</span><span class="sxs-lookup"><span data-stu-id="c2ebe-140">**INapComponentConfig**</span></span>](inapcomponentconfig.md)
</dt> <dt>

[<span data-ttu-id="c2ebe-141">**Inapcomponentconfig:: isuisupported**</span><span class="sxs-lookup"><span data-stu-id="c2ebe-141">**INapComponentConfig::IsUISupported**</span></span>](inapcomponentconfig-isuisupported.md)
</dt> </dl>

 

 





