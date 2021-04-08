---
title: WSMAN. sessionflagusekerberos-Methode (WSManDisp. h)
description: Gibt den Wert des wsmanflagusekerberos-Authentifizierungsflags für die Verwendung im flags-Parameter von WSMAN. kreatesession zurück.
ms.assetid: be005312-1e87-4371-9791-709a9be46f7c
ms.tgt_platform: multiple
keywords:
- Sessionflagusekerberos-Methode Windows-Remoteverwaltung
- Sessionflagusekerberos-Methode Windows-Remoteverwaltung, WSMAN-Objekt
- WSMAN-Objekt Windows-Remoteverwaltung, sessionflagusekerberos-Methode
topic_type:
- apiref
api_name:
- WSMan.SessionFlagUseKerberos
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62e7436a5b79480b39c093545a0b579da3d13082
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741617"
---
# <a name="wsmansessionflagusekerberos-method"></a><span data-ttu-id="b0809-106">WSMAN. sessionflagusekerberos-Methode</span><span class="sxs-lookup"><span data-stu-id="b0809-106">WSMan.SessionFlagUseKerberos method</span></span>

<span data-ttu-id="b0809-107">Die Methode **WSMAN. sessionflagusekerberos** gibt den Wert des **wsmanflagusekerberos** -Authentifizierungsflags zur Verwendung im *Flags* -Parameter von [**WSMAN. kreatesession**](wsman-createsession.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="b0809-107">The **WSMan.SessionFlagUseKerberos** method returns the value of the **WSManFlagUseKerberos** authentication flag for use in the *flags* parameter of [**WSMan.CreateSession**](wsman-createsession.md).</span></span> <span data-ttu-id="b0809-108">Diese Methode bietet eine effizientere Syntax für die Verwendung der-Konstante, damit Skripts keinen konstanten Wert festlegen müssen.</span><span class="sxs-lookup"><span data-stu-id="b0809-108">This method provides a more efficient syntax for using the constant so that scripts are not required to set a constant value.</span></span> <span data-ttu-id="b0809-109">Weitere Informationen zum Abrufen dieser Methode finden Sie unter [Sitzungs Konstanten](session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="b0809-109">For more information about how to call this method, see [Session Constants](session-constants.md).</span></span>

<span data-ttu-id="b0809-110">**Wsmanflagusekerberos** ist eine Konstante in der **\_ \_ wsmansessionflags** -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="b0809-110">**WSManFlagUseKerberos** is a constant in the **\_\_WSManSessionFlags** enumeration.</span></span> <span data-ttu-id="b0809-111">Weitere Informationen finden Sie unter [Authentifizierungs Konstanten](authentication-constants.md).</span><span class="sxs-lookup"><span data-stu-id="b0809-111">For more information, see [Authentication Constants](authentication-constants.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b0809-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="b0809-112">Syntax</span></span>


```VB
WSMan.SessionFlagUseKerberos( _
  ByRef flags _
)
```



## <a name="parameters"></a><span data-ttu-id="b0809-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="b0809-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0809-114">*Flags* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="b0809-114">*flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b0809-115">Der Wert der Konstante.</span><span class="sxs-lookup"><span data-stu-id="b0809-115">The value of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0809-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b0809-116">Return value</span></span>

<span data-ttu-id="b0809-117">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="b0809-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b0809-118">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b0809-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0809-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b0809-119">Requirements</span></span>



| <span data-ttu-id="b0809-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b0809-120">Requirement</span></span> | <span data-ttu-id="b0809-121">Wert</span><span class="sxs-lookup"><span data-stu-id="b0809-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0809-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b0809-122">Minimum supported client</span></span><br/> | <span data-ttu-id="b0809-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b0809-123">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="b0809-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b0809-124">Minimum supported server</span></span><br/> | <span data-ttu-id="b0809-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b0809-125">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="b0809-126">Header</span><span class="sxs-lookup"><span data-stu-id="b0809-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="b0809-127"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b0809-127"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="b0809-128">IDL</span><span class="sxs-lookup"><span data-stu-id="b0809-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b0809-129"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b0809-129"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="b0809-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b0809-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="b0809-131"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b0809-131"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b0809-132">DLL</span><span class="sxs-lookup"><span data-stu-id="b0809-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b0809-133"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b0809-133"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b0809-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b0809-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0809-135">**WSMAN**</span><span class="sxs-lookup"><span data-stu-id="b0809-135">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="b0809-136">**Sitzung**</span><span class="sxs-lookup"><span data-stu-id="b0809-136">**Session**</span></span>](session.md)
</dt> </dl>

 

 





