---
title: WSMAN. SessionFlagUTF8-Methode (WSManDisp. h)
description: Gibt den Wert des WSManFlagUTF8-Authentifizierungsflags für die Verwendung im flags-Parameter von WSMAN. kreatesession zurück.
ms.assetid: a79e292a-364b-4bf3-ae66-6a15ad51524f
ms.tgt_platform: multiple
keywords:
- SessionFlagUTF8-Methode Windows-Remoteverwaltung
- SessionFlagUTF8-Methode Windows-Remoteverwaltung, WSMAN-Objekt
- WSMAN-Objekt Windows-Remoteverwaltung, SessionFlagUTF8-Methode
topic_type:
- apiref
api_name:
- WSMan.SessionFlagUTF8
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 985763131c2f3d4227f1a24af612ea3141237832
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743216"
---
# <a name="wsmansessionflagutf8-method"></a><span data-ttu-id="68190-106">WSMAN. SessionFlagUTF8-Methode</span><span class="sxs-lookup"><span data-stu-id="68190-106">WSMan.SessionFlagUTF8 method</span></span>

<span data-ttu-id="68190-107">Die Methode **WSMAN. SessionFlagUTF8** gibt den Wert des **WSManFlagUTF8** -Authentifizierungsflags zur Verwendung im *Flags* -Parameter von [**WSMAN. kreatesession**](wsman-createsession.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="68190-107">The **WSMan.SessionFlagUTF8** method returns the value of the **WSManFlagUTF8** authentication flag for use in the *flags* parameter of [**WSMan.CreateSession**](wsman-createsession.md).</span></span> <span data-ttu-id="68190-108">Diese Methode bietet eine effizientere Syntax für die Verwendung der-Konstante, damit Skripts keinen konstanten Wert festlegen müssen.</span><span class="sxs-lookup"><span data-stu-id="68190-108">This method provides a more efficient syntax for using the constant so that scripts are not required to set a constant value.</span></span> <span data-ttu-id="68190-109">Weitere Informationen zum Abrufen dieser Methode finden Sie unter [Sitzungs Konstanten](session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="68190-109">For more information about how to call this method, see [Session Constants](session-constants.md).</span></span>

<span data-ttu-id="68190-110">**WSManFlagUTF8** ist eine Konstante in der **\_ \_ wsmansessionflags** -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="68190-110">**WSManFlagUTF8** is a constant in the **\_\_WSManSessionFlags** enumeration.</span></span> <span data-ttu-id="68190-111">Weitere Informationen finden Sie unter [andere Sitzungs Konstanten](other-session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="68190-111">For more information, see [Other Session Constants](other-session-constants.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="68190-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="68190-112">Syntax</span></span>


```VB
WSMan.SessionFlagUTF8( _
  ByRef flags _
)
```



## <a name="parameters"></a><span data-ttu-id="68190-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="68190-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68190-114">*Flags* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="68190-114">*flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="68190-115">Der Wert der Konstante.</span><span class="sxs-lookup"><span data-stu-id="68190-115">The value of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68190-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="68190-116">Return value</span></span>

<span data-ttu-id="68190-117">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="68190-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="68190-118">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="68190-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="68190-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="68190-119">Requirements</span></span>



| <span data-ttu-id="68190-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="68190-120">Requirement</span></span> | <span data-ttu-id="68190-121">Wert</span><span class="sxs-lookup"><span data-stu-id="68190-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="68190-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="68190-122">Minimum supported client</span></span><br/> | <span data-ttu-id="68190-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="68190-123">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="68190-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="68190-124">Minimum supported server</span></span><br/> | <span data-ttu-id="68190-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="68190-125">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="68190-126">Header</span><span class="sxs-lookup"><span data-stu-id="68190-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="68190-127"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="68190-127"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="68190-128">IDL</span><span class="sxs-lookup"><span data-stu-id="68190-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="68190-129"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="68190-129"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="68190-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="68190-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="68190-131"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="68190-131"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="68190-132">DLL</span><span class="sxs-lookup"><span data-stu-id="68190-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="68190-133"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68190-133"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="68190-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="68190-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68190-135">**WSMAN**</span><span class="sxs-lookup"><span data-stu-id="68190-135">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="68190-136">**Sitzung**</span><span class="sxs-lookup"><span data-stu-id="68190-136">**Session**</span></span>](session.md)
</dt> </dl>

 

 





