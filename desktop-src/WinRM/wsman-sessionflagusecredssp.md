---
title: WSMAN. sessionflagusecredssp-Methode (WSManDisp. h)
description: Gibt den Wert des wsmanflagusecredssp-Authentifizierungsflags für die Verwendung im flags-Parameter der WSMAN. kreatesession-Methode zurück.
ms.assetid: bb167445-91d6-4e06-a976-bf869320784a
ms.tgt_platform: multiple
keywords:
- Sessionflagusecredssp-Methode Windows-Remoteverwaltung
- Sessionflagusecredssp-Methode Windows-Remoteverwaltung, WSMAN-Objekt
- WSMAN-Objekt Windows-Remoteverwaltung, sessionflagusecredssp-Methode
topic_type:
- apiref
api_name:
- WSMan.SessionFlagUseCredSsp
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed5dfbaba3e705f100cdd373e194174f4654a7d8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476863"
---
# <a name="wsmansessionflagusecredssp-method"></a><span data-ttu-id="68858-106">WSMAN. sessionflagusecredssp-Methode</span><span class="sxs-lookup"><span data-stu-id="68858-106">WSMan.SessionFlagUseCredSsp method</span></span>

<span data-ttu-id="68858-107">Gibt den Wert des **wsmanflagusecredssp** -Authentifizierungsflags für die Verwendung im *Flags* -Parameter der [**WSMAN. kreatesession**](wsman-createsession.md) -Methode zurück.</span><span class="sxs-lookup"><span data-stu-id="68858-107">Returns the value of the **WSManFlagUseCredSsp** authentication flag for use in the *flags* parameter of the [**WSMan.CreateSession**](wsman-createsession.md) method.</span></span> <span data-ttu-id="68858-108">Diese Methode bietet eine effizientere Syntax für die Verwendung der-Konstante, damit Skripts keinen konstanten Wert festlegen müssen.</span><span class="sxs-lookup"><span data-stu-id="68858-108">This method provides a more efficient syntax for using the constant so that scripts are not required to set a constant value.</span></span> <span data-ttu-id="68858-109">Weitere Informationen zum Abrufen dieser Methode finden Sie unter [Sitzungs Konstanten](session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="68858-109">For more information about how to call this method, see [Session Constants](session-constants.md).</span></span>

<span data-ttu-id="68858-110">**Wsmanflagusecredssp** ist eine Konstante in der **\_ \_ wsmansessionflags** -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="68858-110">**WSManFlagUseCredSsp** is a constant in the **\_\_WSManSessionFlags** enumeration.</span></span> <span data-ttu-id="68858-111">Weitere Informationen finden Sie unter [Authentifizierungs Konstanten](authentication-constants.md).</span><span class="sxs-lookup"><span data-stu-id="68858-111">For more information, see [Authentication Constants](authentication-constants.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="68858-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="68858-112">Syntax</span></span>


```VB
WSMan.SessionFlagUseCredSsp( _
  ByRef flags _
)
```



## <a name="parameters"></a><span data-ttu-id="68858-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="68858-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68858-114">*Flags* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="68858-114">*flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="68858-115">Der Wert der Konstante.</span><span class="sxs-lookup"><span data-stu-id="68858-115">The value of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68858-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="68858-116">Return value</span></span>

<span data-ttu-id="68858-117">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="68858-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="68858-118">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="68858-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="68858-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="68858-119">Requirements</span></span>



| <span data-ttu-id="68858-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="68858-120">Requirement</span></span> | <span data-ttu-id="68858-121">Wert</span><span class="sxs-lookup"><span data-stu-id="68858-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="68858-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="68858-122">Minimum supported client</span></span><br/> | <span data-ttu-id="68858-123">Windows 7</span><span class="sxs-lookup"><span data-stu-id="68858-123">Windows 7</span></span><br/>                                                                                                        |
| <span data-ttu-id="68858-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="68858-124">Minimum supported server</span></span><br/> | <span data-ttu-id="68858-125">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="68858-125">Windows Server 2008 R2</span></span><br/>                                                                                           |
| <span data-ttu-id="68858-126">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="68858-126">Redistributable</span></span><br/>          | <span data-ttu-id="68858-127">Windows Management Framework unter Windows Server 2008 mit SP2, Windows Vista mit SP1 und Windows Vista mit SP2</span><span class="sxs-lookup"><span data-stu-id="68858-127">Windows Management Framework on Windows Server 2008 with SP2, Windows Vista with SP1, and Windows Vista with SP2</span></span><br/> |
| <span data-ttu-id="68858-128">Header</span><span class="sxs-lookup"><span data-stu-id="68858-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="68858-129"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="68858-129"><dt>WSManDisp.h</dt></span></span> </dl>                                      |
| <span data-ttu-id="68858-130">IDL</span><span class="sxs-lookup"><span data-stu-id="68858-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="68858-131"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="68858-131"><dt>WSManDisp.idl</dt></span></span> </dl>                                    |
| <span data-ttu-id="68858-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="68858-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="68858-133"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="68858-133"><dt>WSManDisp.tlb</dt></span></span> </dl>                                    |
| <span data-ttu-id="68858-134">DLL</span><span class="sxs-lookup"><span data-stu-id="68858-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="68858-135"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68858-135"><dt>WSMAuto.dll</dt></span></span> </dl>                                      |



## <a name="see-also"></a><span data-ttu-id="68858-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="68858-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68858-137">**WSMAN**</span><span class="sxs-lookup"><span data-stu-id="68858-137">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="68858-138">**Sitzung**</span><span class="sxs-lookup"><span data-stu-id="68858-138">**Session**</span></span>](session.md)
</dt> </dl>

 

 





