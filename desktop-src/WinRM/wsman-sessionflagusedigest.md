---
title: WSMAN. sessionflagusedigest-Methode (WSManDisp. h)
description: Gibt den Wert des wsmanflagusedigest-Authentifizierungsflags für die Verwendung im flags-Parameter der WSMAN. kreatesession-Methode zurück.
ms.assetid: dba2448a-4f72-4000-8687-4c1be812fc3b
ms.tgt_platform: multiple
keywords:
- Sessionflagusedigest-Methode Windows-Remoteverwaltung
- Sessionflagusedigest-Methode Windows-Remoteverwaltung, WSMAN-Objekt
- WSMAN-Objekt Windows-Remoteverwaltung, sessionflagusedigest-Methode
topic_type:
- apiref
api_name:
- WSMan.SessionFlagUseDigest
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4018428123443836c4f433f3e82f03a93ee9b766
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040646"
---
# <a name="wsmansessionflagusedigest-method"></a><span data-ttu-id="3d6ca-106">WSMAN. sessionflagusedigest-Methode</span><span class="sxs-lookup"><span data-stu-id="3d6ca-106">WSMan.SessionFlagUseDigest method</span></span>

<span data-ttu-id="3d6ca-107">Die Methode **WSMAN. sessionflagusedigest** gibt den Wert des **wsmanflagusedigest** -Authentifizierungsflags zur Verwendung im *Flags* -Parameter der [**WSMAN. kreatesession**](wsman-createsession.md) -Methode zurück.</span><span class="sxs-lookup"><span data-stu-id="3d6ca-107">The **WSMan.SessionFlagUseDigest** method returns the value of the **WSManFlagUseDigest** authentication flag for use in the *flags* parameter of the [**WSMan.CreateSession**](wsman-createsession.md) method.</span></span> <span data-ttu-id="3d6ca-108">Diese Methode bietet eine effizientere Syntax für die Verwendung der-Konstante, damit Skripts keinen konstanten Wert festlegen müssen.</span><span class="sxs-lookup"><span data-stu-id="3d6ca-108">This method provides a more efficient syntax for using the constant so that scripts are not required to set a constant value.</span></span> <span data-ttu-id="3d6ca-109">Weitere Informationen zum Abrufen dieser Methode finden Sie unter [Sitzungs Konstanten](session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="3d6ca-109">For more information about how to call this method, see [Session Constants](session-constants.md).</span></span>

<span data-ttu-id="3d6ca-110">**Wsmanflagusedigest** ist ein Wert in der **\_ \_ wsmansessionflags** -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="3d6ca-110">**WSManFlagUseDigest** is a value in the **\_\_WSManSessionFlags** enumeration.</span></span> <span data-ttu-id="3d6ca-111">Weitere Informationen finden Sie unter [Authentifizierungs Konstanten](authentication-constants.md).</span><span class="sxs-lookup"><span data-stu-id="3d6ca-111">For more information, see [Authentication Constants](authentication-constants.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="3d6ca-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="3d6ca-112">Syntax</span></span>


```VB
WSMan.SessionFlagUseDigest( _
  ByRef flags _
)
```



## <a name="parameters"></a><span data-ttu-id="3d6ca-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="3d6ca-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d6ca-114">*Flags* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="3d6ca-114">*flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3d6ca-115">Der Wert der Konstante.</span><span class="sxs-lookup"><span data-stu-id="3d6ca-115">The value of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d6ca-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3d6ca-116">Return value</span></span>

<span data-ttu-id="3d6ca-117">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="3d6ca-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3d6ca-118">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3d6ca-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d6ca-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3d6ca-119">Requirements</span></span>



| <span data-ttu-id="3d6ca-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3d6ca-120">Requirement</span></span> | <span data-ttu-id="3d6ca-121">Wert</span><span class="sxs-lookup"><span data-stu-id="3d6ca-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d6ca-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3d6ca-122">Minimum supported client</span></span><br/> | <span data-ttu-id="3d6ca-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3d6ca-123">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="3d6ca-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3d6ca-124">Minimum supported server</span></span><br/> | <span data-ttu-id="3d6ca-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3d6ca-125">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="3d6ca-126">Header</span><span class="sxs-lookup"><span data-stu-id="3d6ca-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="3d6ca-127"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="3d6ca-127"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="3d6ca-128">IDL</span><span class="sxs-lookup"><span data-stu-id="3d6ca-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3d6ca-129"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3d6ca-129"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="3d6ca-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3d6ca-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="3d6ca-131"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="3d6ca-131"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="3d6ca-132">DLL</span><span class="sxs-lookup"><span data-stu-id="3d6ca-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3d6ca-133"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3d6ca-133"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3d6ca-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3d6ca-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d6ca-135">**WSMAN**</span><span class="sxs-lookup"><span data-stu-id="3d6ca-135">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="3d6ca-136">**Sitzung**</span><span class="sxs-lookup"><span data-stu-id="3d6ca-136">**Session**</span></span>](session.md)
</dt> </dl>

 

 





