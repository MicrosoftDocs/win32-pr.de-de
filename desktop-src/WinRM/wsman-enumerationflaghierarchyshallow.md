---
title: WSMAN. enumerationflaghierarchyflache-Methode (WSManDisp. h)
description: Gibt den Wert des Enumerationsflags enumerationflaghierarchyflache zurück, der im flags-Parameter von Session. Enumerate verwendet werden soll.
ms.assetid: 18b564e6-dda1-44b9-b445-26c6183b6af9
ms.tgt_platform: multiple
keywords:
- Enumerationflaghierarchyflache-Methode Windows-Remoteverwaltung
- Enumerationflaghierarchyflache-Methode Windows-Remoteverwaltung, WSMAN-Objekt
- WSMAN-Objekt Windows-Remoteverwaltung, enumerationflaghierarchyflache-Methode
topic_type:
- apiref
api_name:
- WSMan.EnumerationFlagHierarchyShallow
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46b74552fd88ac370ad4a3f8b885a7f61e65a053
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518140"
---
# <a name="wsmanenumerationflaghierarchyshallow-method"></a><span data-ttu-id="f840a-106">WSMAN. enumerationflaghierarchyflache-Methode</span><span class="sxs-lookup"><span data-stu-id="f840a-106">WSMan.EnumerationFlagHierarchyShallow method</span></span>

<span data-ttu-id="f840a-107">Die **enumerationflaghierarchyflache** -Methode gibt den Wert des **Enumerationsflags enumerationflaghierarchyflache** zurück, der im *Flags* -Parameter von [**Session. Enumerate**](session-enumerate.md)verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f840a-107">The **EnumerationFlagHierarchyShallow** method returns the value of the enumeration flag **EnumerationFlagHierarchyShallow** for use in the *flags* parameter of [**Session.Enumerate**](session-enumerate.md).</span></span> <span data-ttu-id="f840a-108">Diese Methode bietet eine effizientere Syntax für die Verwendung der-Konstante, damit Skripts keinen konstanten Wert festlegen müssen.</span><span class="sxs-lookup"><span data-stu-id="f840a-108">This method provides a more efficient syntax for using the constant so that scripts are not required to set a constant value.</span></span> <span data-ttu-id="f840a-109">Weitere Informationen zum Abrufen dieser Methode finden Sie unter [Sitzungs Konstanten](session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="f840a-109">For more information about how to call this method, see [Session Constants](session-constants.md).</span></span>

<span data-ttu-id="f840a-110">**Enumerationflaghierarchyflache** ist eine Konstante in der **\_ wsmanenumflags** -Enumeration und wird in [**Enumerationskonstanten**](enumeration-constants.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="f840a-110">**EnumerationFlagHierarchyShallow** is a constant in the **\_WSManEnumFlags** enumeration and is described in [**Enumeration Constants**](enumeration-constants.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f840a-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="f840a-111">Syntax</span></span>


```VB
WSMan.EnumerationFlagHierarchyShallow( _
  ByRef flags _
)
```



## <a name="parameters"></a><span data-ttu-id="f840a-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="f840a-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f840a-113">*Flags* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f840a-113">*flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f840a-114">Der Wert der Konstante.</span><span class="sxs-lookup"><span data-stu-id="f840a-114">The value of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f840a-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f840a-115">Return value</span></span>

<span data-ttu-id="f840a-116">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="f840a-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f840a-117">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f840a-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="f840a-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f840a-118">Requirements</span></span>



| <span data-ttu-id="f840a-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f840a-119">Requirement</span></span> | <span data-ttu-id="f840a-120">Wert</span><span class="sxs-lookup"><span data-stu-id="f840a-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f840a-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f840a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f840a-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f840a-122">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="f840a-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f840a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f840a-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f840a-124">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="f840a-125">Header</span><span class="sxs-lookup"><span data-stu-id="f840a-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="f840a-126"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f840a-126"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="f840a-127">IDL</span><span class="sxs-lookup"><span data-stu-id="f840a-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f840a-128"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f840a-128"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="f840a-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f840a-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="f840a-130"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f840a-130"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f840a-131">DLL</span><span class="sxs-lookup"><span data-stu-id="f840a-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f840a-132"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f840a-132"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f840a-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f840a-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f840a-134">**WSMAN**</span><span class="sxs-lookup"><span data-stu-id="f840a-134">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="f840a-135">**Sitzung**</span><span class="sxs-lookup"><span data-stu-id="f840a-135">**Session**</span></span>](session.md)
</dt> </dl>

 

 





