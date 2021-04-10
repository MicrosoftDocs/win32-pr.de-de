---
title: WSMAN. sessionflagskipcacheck-Methode (WSManDisp. h)
description: Gibt den Wert des wsmanflagskipcacheck-Authentifizierungsflags für die Verwendung im flags-Parameter von WSMAN. kreatesession zurück.
ms.assetid: a67cadb3-c20a-4a58-a13b-5bbd23c547d1
ms.tgt_platform: multiple
keywords:
- Sessionflagskipcacheck-Methode Windows-Remoteverwaltung
- Sessionflagskipcacheck-Methode Windows-Remoteverwaltung, WSMAN-Objekt
- WSMAN-Objekt Windows-Remoteverwaltung, sessionflagskipcacheck-Methode
topic_type:
- apiref
api_name:
- WSMan.SessionFlagSkipCACheck
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e536112b16ad8cbab3cebb2de582a2e0ea8aec0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040116"
---
# <a name="wsmansessionflagskipcacheck-method"></a><span data-ttu-id="32c3b-106">WSMAN. sessionflagskipcacheck-Methode</span><span class="sxs-lookup"><span data-stu-id="32c3b-106">WSMan.SessionFlagSkipCACheck method</span></span>

<span data-ttu-id="32c3b-107">Die **WSMAN. sessionflagskipcacheck** -Methode gibt den Wert des **wsmanflagskipcacheck** -Authentifizierungsflags zur Verwendung im *Flags* -Parameter von [**WSMAN. kreatesession**](wsman-createsession.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="32c3b-107">The **WSMan.SessionFlagSkipCACheck** method returns the value of the **WSManFlagSkipCACheck** authentication flag for use in the *flags* parameter of [**WSMan.CreateSession**](wsman-createsession.md).</span></span> <span data-ttu-id="32c3b-108">Diese Methode bietet eine effizientere Syntax für die Verwendung der-Konstante, damit Skripts keinen konstanten Wert festlegen müssen.</span><span class="sxs-lookup"><span data-stu-id="32c3b-108">This method provides a more efficient syntax for using the constant so that scripts are not required to set a constant value.</span></span> <span data-ttu-id="32c3b-109">Weitere Informationen zum Abrufen dieser Methode und Codebeispiele finden Sie unter [Sitzungs Konstanten](session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="32c3b-109">For more information about how to call this method and code examples, see [Session Constants](session-constants.md).</span></span>

<span data-ttu-id="32c3b-110">**Wsmanflagskipcacheck** ist eine Konstante in der **\_ \_ wsmansessionflags** -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="32c3b-110">**WSManFlagSkipCACheck** is a constant in the **\_\_WSManSessionFlags** enumeration.</span></span> <span data-ttu-id="32c3b-111">Weitere Informationen finden Sie unter [**Authentifizierungs Konstanten**](authentication-constants.md).</span><span class="sxs-lookup"><span data-stu-id="32c3b-111">For more information, see [**Authentication Constants**](authentication-constants.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="32c3b-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="32c3b-112">Syntax</span></span>


```VB
WSMan.SessionFlagSkipCACheck( _
  ByRef flags _
)
```



## <a name="parameters"></a><span data-ttu-id="32c3b-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="32c3b-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32c3b-114">*Flags* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="32c3b-114">*flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="32c3b-115">Der Wert der Konstante.</span><span class="sxs-lookup"><span data-stu-id="32c3b-115">The value of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32c3b-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="32c3b-116">Return value</span></span>

<span data-ttu-id="32c3b-117">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="32c3b-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="32c3b-118">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="32c3b-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="32c3b-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="32c3b-119">Requirements</span></span>



| <span data-ttu-id="32c3b-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="32c3b-120">Requirement</span></span> | <span data-ttu-id="32c3b-121">Wert</span><span class="sxs-lookup"><span data-stu-id="32c3b-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="32c3b-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="32c3b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="32c3b-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="32c3b-123">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="32c3b-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="32c3b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="32c3b-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="32c3b-125">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="32c3b-126">Header</span><span class="sxs-lookup"><span data-stu-id="32c3b-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="32c3b-127"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="32c3b-127"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="32c3b-128">IDL</span><span class="sxs-lookup"><span data-stu-id="32c3b-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="32c3b-129"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="32c3b-129"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="32c3b-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="32c3b-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="32c3b-131"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="32c3b-131"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="32c3b-132">DLL</span><span class="sxs-lookup"><span data-stu-id="32c3b-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="32c3b-133"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="32c3b-133"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="32c3b-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="32c3b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32c3b-135">**WSMAN**</span><span class="sxs-lookup"><span data-stu-id="32c3b-135">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="32c3b-136">**Sitzung**</span><span class="sxs-lookup"><span data-stu-id="32c3b-136">**Session**</span></span>](session.md)
</dt> </dl>

 

 





