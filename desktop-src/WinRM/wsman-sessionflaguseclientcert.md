---
title: WSMAN. sessionflaguseclientcertificate-Methode (WSManDisp. h)
description: Gibt den Wert des wsmanflaguseclientcertificate-Authentifizierungsflags für die Verwendung im flags-Parameter der WSMAN. kreatesession-Methode zurück.
ms.assetid: b0ec4dbb-3a98-45e8-8f6b-74b858d6c3fc
ms.tgt_platform: multiple
keywords:
- Sessionflaguseclientcertificate-Methode Windows-Remoteverwaltung
- Sessionflaguseclientcertificate-Methode Windows-Remoteverwaltung, WSMAN-Objekt
- WSMAN-Objekt Windows-Remoteverwaltung, sessionflaguseclientcertificate-Methode
topic_type:
- apiref
api_name:
- WSMan.SessionFlagUseClientCertificate
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbbcbc1a920cbd7ce2b58e29c52fc08245b8aa35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340358"
---
# <a name="wsmansessionflaguseclientcertificate-method"></a><span data-ttu-id="f9dca-106">WSMAN. sessionflaguseclientcertificate-Methode</span><span class="sxs-lookup"><span data-stu-id="f9dca-106">WSMan.SessionFlagUseClientCertificate method</span></span>

<span data-ttu-id="f9dca-107">Die Methode **WSMAN. sessionflaguseclientcertificate** gibt den Wert des **wsmanflaguseclientcertificate** -Authentifizierungsflags zur Verwendung im *Flags* -Parameter der [**WSMAN. kreatesession**](wsman-createsession.md) -Methode zurück.</span><span class="sxs-lookup"><span data-stu-id="f9dca-107">The **WSMan.SessionFlagUseClientCertificate** method returns the value of the **WSManFlagUseClientCertificate** authentication flag for use in the *flags* parameter of the [**WSMan.CreateSession**](wsman-createsession.md) method.</span></span> <span data-ttu-id="f9dca-108">Diese Methode bietet eine effizientere Syntax für die Verwendung der-Konstante, damit Skripts keinen konstanten Wert festlegen müssen.</span><span class="sxs-lookup"><span data-stu-id="f9dca-108">This method provides a more efficient syntax for using the constant so that scripts are not required to set a constant value.</span></span> <span data-ttu-id="f9dca-109">Weitere Informationen zum Abrufen dieser Methode finden Sie unter [Sitzungs Konstanten](session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="f9dca-109">For more information about how to call this method, see [Session Constants](session-constants.md).</span></span>

<span data-ttu-id="f9dca-110">**Wsmanflaguseclientcertificate** ist eine Konstante in der **\_ \_ wsmanauthenticationflags** -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="f9dca-110">**WSManFlagUseClientCertificate** is a constant in the **\_\_WSManAuthenticationFlags** enumeration.</span></span> <span data-ttu-id="f9dca-111">Weitere Informationen finden Sie unter [Authentifizierungs Konstanten](authentication-constants.md).</span><span class="sxs-lookup"><span data-stu-id="f9dca-111">For more information, see [Authentication Constants](authentication-constants.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f9dca-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="f9dca-112">Syntax</span></span>


```VB
WSMan.SessionFlagUseClientCertificate( _
  ByRef flags _
)
```



## <a name="parameters"></a><span data-ttu-id="f9dca-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="f9dca-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9dca-114">*Flags* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f9dca-114">*flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f9dca-115">Der Wert der Konstante.</span><span class="sxs-lookup"><span data-stu-id="f9dca-115">The value of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9dca-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f9dca-116">Return value</span></span>

<span data-ttu-id="f9dca-117">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="f9dca-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f9dca-118">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f9dca-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9dca-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f9dca-119">Requirements</span></span>



| <span data-ttu-id="f9dca-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f9dca-120">Requirement</span></span> | <span data-ttu-id="f9dca-121">Wert</span><span class="sxs-lookup"><span data-stu-id="f9dca-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9dca-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f9dca-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f9dca-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f9dca-123">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="f9dca-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f9dca-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f9dca-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f9dca-125">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="f9dca-126">Header</span><span class="sxs-lookup"><span data-stu-id="f9dca-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9dca-127"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f9dca-127"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="f9dca-128">IDL</span><span class="sxs-lookup"><span data-stu-id="f9dca-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f9dca-129"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f9dca-129"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="f9dca-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f9dca-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="f9dca-131"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f9dca-131"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f9dca-132">DLL</span><span class="sxs-lookup"><span data-stu-id="f9dca-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f9dca-133"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f9dca-133"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f9dca-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f9dca-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9dca-135">**WSMAN**</span><span class="sxs-lookup"><span data-stu-id="f9dca-135">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="f9dca-136">**Sitzung**</span><span class="sxs-lookup"><span data-stu-id="f9dca-136">**Session**</span></span>](session.md)
</dt> </dl>

 

 





