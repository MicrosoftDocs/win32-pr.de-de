---
title: WSMAN. sessionflagenablespnserverport-Methode (WSManDisp. h)
description: Gibt den Wert des Authentifizierungsflags wsmanflagenablespnserverport für die Verwendung im flags-Parameter der WSMAN. kreatesession-Methode zurück.
ms.assetid: a18a87e6-dcee-4e9f-8e8c-262fef36ab1a
ms.tgt_platform: multiple
keywords:
- Sessionflagenablespnserverport-Methode Windows-Remoteverwaltung
- Sessionflagenablespnserverport-Methode Windows-Remoteverwaltung, WSMAN-Objekt
- WSMAN-Objekt Windows-Remoteverwaltung, sessionflagenablespnserverport-Methode
topic_type:
- apiref
api_name:
- WSMan.SessionFlagEnableSPNServerPort
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4153f088079b58b3b0e048f2cd8f38b3524754a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518137"
---
# <a name="wsmansessionflagenablespnserverport-method"></a><span data-ttu-id="dd19c-106">WSMAN. sessionflagenablespnserverport-Methode</span><span class="sxs-lookup"><span data-stu-id="dd19c-106">WSMan.SessionFlagEnableSPNServerPort method</span></span>

<span data-ttu-id="dd19c-107">Die **WSMAN. sessionflagenablespnserverport** -Methode gibt den Wert des Authentifizierungsflags **wsmanflagenablespnserverport** für die Verwendung im *Flags* -Parameter der [**WSMAN. kreatesession**](wsman-createsession.md) -Methode zurück.</span><span class="sxs-lookup"><span data-stu-id="dd19c-107">The **WSMan.SessionFlagEnableSPNServerPort** method returns the value of the authentication flag **WSManFlagEnableSPNServerPort** for use in the *flags* parameter of the [**WSMan.CreateSession**](wsman-createsession.md) method.</span></span> <span data-ttu-id="dd19c-108">Diese Methode bietet eine effizientere Syntax für die Verwendung der-Konstante, damit Skripts keinen konstanten Wert festlegen müssen.</span><span class="sxs-lookup"><span data-stu-id="dd19c-108">This method provides a more efficient syntax for using the constant so that scripts are not required to set a constant value.</span></span> <span data-ttu-id="dd19c-109">Weitere Informationen zum Abrufen dieser Methode finden Sie unter [Sitzungs Konstanten](session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="dd19c-109">For more information about how to call this method, see [Session Constants](session-constants.md).</span></span>

<span data-ttu-id="dd19c-110">**Wsmanflagenablespnserverport** ist eine Konstante in der **\_ \_ wsmansessionflags** -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="dd19c-110">**WSManFlagEnableSPNServerPort** is a constant in the **\_\_WSManSessionFlags** enumeration.</span></span> <span data-ttu-id="dd19c-111">Weitere Informationen finden Sie unter [**andere Sitzungs Konstanten**](other-session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="dd19c-111">For more information, see [**Other Session Constants**](other-session-constants.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="dd19c-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="dd19c-112">Syntax</span></span>


```VB
WSMan.SessionFlagEnableSPNServerPort( _
  ByRef flags _
)
```



## <a name="parameters"></a><span data-ttu-id="dd19c-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="dd19c-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd19c-114">*Flags* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="dd19c-114">*flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dd19c-115">Der Wert der Konstante.</span><span class="sxs-lookup"><span data-stu-id="dd19c-115">The value of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd19c-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dd19c-116">Return value</span></span>

<span data-ttu-id="dd19c-117">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="dd19c-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="dd19c-118">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="dd19c-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd19c-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dd19c-119">Requirements</span></span>



| <span data-ttu-id="dd19c-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dd19c-120">Requirement</span></span> | <span data-ttu-id="dd19c-121">Wert</span><span class="sxs-lookup"><span data-stu-id="dd19c-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd19c-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dd19c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="dd19c-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dd19c-123">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="dd19c-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dd19c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="dd19c-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dd19c-125">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="dd19c-126">Header</span><span class="sxs-lookup"><span data-stu-id="dd19c-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="dd19c-127"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd19c-127"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="dd19c-128">IDL</span><span class="sxs-lookup"><span data-stu-id="dd19c-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="dd19c-129"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="dd19c-129"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="dd19c-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="dd19c-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="dd19c-131"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="dd19c-131"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="dd19c-132">DLL</span><span class="sxs-lookup"><span data-stu-id="dd19c-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dd19c-133"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dd19c-133"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="dd19c-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dd19c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd19c-135">**WSMAN**</span><span class="sxs-lookup"><span data-stu-id="dd19c-135">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="dd19c-136">**Sitzung**</span><span class="sxs-lookup"><span data-stu-id="dd19c-136">**Session**</span></span>](session.md)
</dt> </dl>

 

 





