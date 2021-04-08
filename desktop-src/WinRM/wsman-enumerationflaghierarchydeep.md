---
title: WSMAN. enumerationflaghierarchydeep-Methode (WSManDisp. h)
description: Gibt den Wert des Enumerationsflags enumerationflaghierarchydeep zur Verwendung im flags-Parameter von Session. Enumerate zurück.
ms.assetid: b84b82fa-0b2e-418e-850f-6d7a4749fdc1
ms.tgt_platform: multiple
keywords:
- Enumerationflaghierarchydeep-Methode Windows-Remoteverwaltung
- Enumerationflaghierarchydeep-Methode Windows-Remoteverwaltung, WSMAN-Objekt
- WSMAN-Objekt Windows-Remoteverwaltung, enumerationflaghierarchydeep-Methode
topic_type:
- apiref
api_name:
- WSMan.EnumerationFlagHierarchyDeep
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61982c6117d0a91ec253af35657f0cbbf5af12c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957049"
---
# <a name="wsmanenumerationflaghierarchydeep-method"></a><span data-ttu-id="45c88-106">WSMAN. enumerationflaghierarchydeep-Methode</span><span class="sxs-lookup"><span data-stu-id="45c88-106">WSMan.EnumerationFlagHierarchyDeep method</span></span>

<span data-ttu-id="45c88-107">Die **enumerationflaghierarchydeep** -Methode gibt den Wert des **Enumerationsflags enumerationflaghierarchydeep** zur Verwendung im *Flags* -Parameter von [**Session. Enumerate**](session-enumerate.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="45c88-107">The **EnumerationFlagHierarchyDeep** method returns the value of the enumeration flag **EnumerationFlagHierarchyDeep** for use in the *flags* parameter of [**Session.Enumerate**](session-enumerate.md).</span></span> <span data-ttu-id="45c88-108">Diese Methode bietet eine effizientere Syntax für die Verwendung der-Konstante, damit Skripts keinen konstanten Wert festlegen müssen.</span><span class="sxs-lookup"><span data-stu-id="45c88-108">This method provides a more efficient syntax for using the constant so that scripts are not required to set a constant value.</span></span> <span data-ttu-id="45c88-109">Weitere Informationen zum Abrufen dieser Methode finden Sie unter [Sitzungs Konstanten](session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="45c88-109">For more information about how to call this method, see [Session Constants](session-constants.md).</span></span>

<span data-ttu-id="45c88-110">**Enumerationflaghierarchydeep** ist eine Konstante in der **\_ wsmanenumflags** -Enumeration und wird in [**Enumerationskonstanten**](enumeration-constants.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="45c88-110">**EnumerationFlagHierarchyDeep** is a constant in the **\_WSManEnumFlags** enumeration and is described in [**Enumeration Constants**](enumeration-constants.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="45c88-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="45c88-111">Syntax</span></span>


```VB
WSMan.EnumerationFlagHierarchyDeep( _
  ByRef flags _
)
```



## <a name="parameters"></a><span data-ttu-id="45c88-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="45c88-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45c88-113">*Flags* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="45c88-113">*flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="45c88-114">Der Wert der Konstante.</span><span class="sxs-lookup"><span data-stu-id="45c88-114">The value of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45c88-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="45c88-115">Return value</span></span>

<span data-ttu-id="45c88-116">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="45c88-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="45c88-117">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="45c88-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="45c88-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="45c88-118">Requirements</span></span>



| <span data-ttu-id="45c88-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="45c88-119">Requirement</span></span> | <span data-ttu-id="45c88-120">Wert</span><span class="sxs-lookup"><span data-stu-id="45c88-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="45c88-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="45c88-121">Minimum supported client</span></span><br/> | <span data-ttu-id="45c88-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="45c88-122">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="45c88-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="45c88-123">Minimum supported server</span></span><br/> | <span data-ttu-id="45c88-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="45c88-124">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="45c88-125">Header</span><span class="sxs-lookup"><span data-stu-id="45c88-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="45c88-126"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="45c88-126"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="45c88-127">IDL</span><span class="sxs-lookup"><span data-stu-id="45c88-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="45c88-128"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="45c88-128"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="45c88-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="45c88-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="45c88-130"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="45c88-130"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="45c88-131">DLL</span><span class="sxs-lookup"><span data-stu-id="45c88-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="45c88-132"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="45c88-132"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="45c88-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="45c88-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45c88-134">**WSMAN**</span><span class="sxs-lookup"><span data-stu-id="45c88-134">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="45c88-135">**Sitzung**</span><span class="sxs-lookup"><span data-stu-id="45c88-135">**Session**</span></span>](session.md)
</dt> </dl>

 

 





