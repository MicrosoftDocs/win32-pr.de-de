---
title: WSMAN. sessionflagskipcncheck-Methode (WSManDisp. h)
description: Gibt den Wert des wsmanflagskipcncheck-Authentifizierungsflags für die Verwendung im flags-Parameter von WSMAN. kreatesession zurück.
ms.assetid: 44884a9d-ec5f-4822-945d-2681d214a902
ms.tgt_platform: multiple
keywords:
- Sessionflagskipcncheck-Methode Windows-Remoteverwaltung
- Sessionflagskipcncheck-Methode Windows-Remoteverwaltung, WSMAN-Objekt
- WSMAN-Objekt Windows-Remoteverwaltung, sessionflagskipcncheck-Methode
topic_type:
- apiref
api_name:
- WSMan.SessionFlagSkipCNCheck
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c98981ac166ea7b1b76f1ab322db6c48679a4bf4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956744"
---
# <a name="wsmansessionflagskipcncheck-method"></a><span data-ttu-id="13cde-106">WSMAN. sessionflagskipcncheck-Methode</span><span class="sxs-lookup"><span data-stu-id="13cde-106">WSMan.SessionFlagSkipCNCheck method</span></span>

<span data-ttu-id="13cde-107">Die **WSMAN. sessionflagskipcncheck** -Methode gibt den Wert des **wsmanflagskipcncheck** -Authentifizierungsflags zur Verwendung im *Flags* -Parameter von [**WSMAN. kreatesession**](wsman-createsession.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="13cde-107">The **WSMan.SessionFlagSkipCNCheck** method returns the value of the **WSManFlagSkipCNCheck** authentication flag for use in the *flags* parameter of [**WSMan.CreateSession**](wsman-createsession.md).</span></span> <span data-ttu-id="13cde-108">Diese Methode bietet eine effizientere Syntax für die Verwendung der-Konstante, damit Skripts keinen konstanten Wert festlegen müssen.</span><span class="sxs-lookup"><span data-stu-id="13cde-108">This method provides a more efficient syntax for using the constant so that scripts are not required to set a constant value.</span></span> <span data-ttu-id="13cde-109">Weitere Informationen zum Abrufen dieser Methode finden Sie unter [Sitzungs Konstanten](session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="13cde-109">For more information about how to call this method, see [Session Constants](session-constants.md).</span></span>

<span data-ttu-id="13cde-110">**Wsmanflagskipcncheck** ist eine Konstante in der **\_ \_ wsmansessionflags** -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="13cde-110">**WSManFlagSkipCNCheck** is a constant in the **\_\_WSManSessionFlags** enumeration.</span></span> <span data-ttu-id="13cde-111">Weitere Informationen finden Sie unter [**Authentifizierungs Konstanten**](authentication-constants.md).</span><span class="sxs-lookup"><span data-stu-id="13cde-111">For more information, see [**Authentication Constants**](authentication-constants.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="13cde-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="13cde-112">Syntax</span></span>


```VB
WSMan.SessionFlagSkipCNCheck( _
  ByRef flags _
)
```



## <a name="parameters"></a><span data-ttu-id="13cde-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="13cde-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13cde-114">*Flags* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="13cde-114">*flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="13cde-115">Der Wert der Konstante.</span><span class="sxs-lookup"><span data-stu-id="13cde-115">The value of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13cde-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="13cde-116">Return value</span></span>

<span data-ttu-id="13cde-117">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="13cde-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="13cde-118">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="13cde-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="13cde-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="13cde-119">Requirements</span></span>



| <span data-ttu-id="13cde-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="13cde-120">Requirement</span></span> | <span data-ttu-id="13cde-121">Wert</span><span class="sxs-lookup"><span data-stu-id="13cde-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="13cde-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="13cde-122">Minimum supported client</span></span><br/> | <span data-ttu-id="13cde-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="13cde-123">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="13cde-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="13cde-124">Minimum supported server</span></span><br/> | <span data-ttu-id="13cde-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="13cde-125">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="13cde-126">Header</span><span class="sxs-lookup"><span data-stu-id="13cde-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="13cde-127"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="13cde-127"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="13cde-128">IDL</span><span class="sxs-lookup"><span data-stu-id="13cde-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="13cde-129"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="13cde-129"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="13cde-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="13cde-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="13cde-131"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="13cde-131"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="13cde-132">DLL</span><span class="sxs-lookup"><span data-stu-id="13cde-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="13cde-133"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="13cde-133"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="13cde-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="13cde-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13cde-135">**WSMAN**</span><span class="sxs-lookup"><span data-stu-id="13cde-135">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="13cde-136">**Sitzung**</span><span class="sxs-lookup"><span data-stu-id="13cde-136">**Session**</span></span>](session.md)
</dt> </dl>

 

 





