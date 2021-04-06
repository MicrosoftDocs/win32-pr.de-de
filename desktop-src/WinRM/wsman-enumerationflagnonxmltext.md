---
title: WSMAN. enumerationflagnonxmltext-Methode (WSManDisp. h)
description: Gibt den Wert der Enumerationskonstante wsmanflagnonxmltext zurück, der im flags-Parameter der Session. Enumerate-Methode verwendet werden soll.
ms.assetid: 5e062e73-f833-4090-ba5a-48ca374724e7
ms.tgt_platform: multiple
keywords:
- Enumerationflagnonxmltext-Methode Windows-Remoteverwaltung
- Enumerationflagnonxmltext-Methode Windows-Remoteverwaltung, WSMAN-Objekt
- WSMAN-Objekt Windows-Remoteverwaltung, enumerationflagnonxmltext-Methode
topic_type:
- apiref
api_name:
- WSMan.EnumerationFlagNonXmlText
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26a9547f85a07702dc3735129842e5bc286ee9b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742360"
---
# <a name="wsmanenumerationflagnonxmltext-method"></a><span data-ttu-id="8bff5-106">WSMAN. enumerationflagnonxmltext-Methode</span><span class="sxs-lookup"><span data-stu-id="8bff5-106">WSMan.EnumerationFlagNonXmlText method</span></span>

<span data-ttu-id="8bff5-107">**WSMAN. enumerationflagnonxmltext** gibt den Wert der Enumerationskonstante **wsmanflagnonxmltext** zur Verwendung im *Flags* -Parameter der [**Session. Enumerate**](session-enumerate.md) -Methode zurück.</span><span class="sxs-lookup"><span data-stu-id="8bff5-107">The **WSMan.EnumerationFlagNonXmlText** returns the value of the enumeration constant **WSManFlagNonXmlText** for use in the *flags* parameter of the [**Session.Enumerate**](session-enumerate.md) method.</span></span> <span data-ttu-id="8bff5-108">Diese Methode bietet eine effizientere Syntax für die Verwendung der-Konstante, damit Skripts keinen konstanten Wert festlegen müssen.</span><span class="sxs-lookup"><span data-stu-id="8bff5-108">This method provides a more efficient syntax for using the constant so that scripts are not required to set a constant value.</span></span> <span data-ttu-id="8bff5-109">Weitere Informationen zum Abrufen dieser Methode finden Sie unter [Sitzungs Konstanten](session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="8bff5-109">For more information about how to call this method, see [Session Constants](session-constants.md).</span></span>

<span data-ttu-id="8bff5-110">**Wsmanflagnonxmltext** ist eine Konstante in der **\_ \_ wsmanenumflags** -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="8bff5-110">**WSManFlagNonXmlText** is a constant in the **\_\_WSManEnumFlags** enumeration.</span></span> <span data-ttu-id="8bff5-111">Weitere Informationen finden Sie unter [**Enumerationskonstanten**](enumeration-constants.md).</span><span class="sxs-lookup"><span data-stu-id="8bff5-111">For more information, see [**Enumeration Constants**](enumeration-constants.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="8bff5-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="8bff5-112">Syntax</span></span>


```VB
WSMan.EnumerationFlagNonXmlText( _
  ByRef flags _
)
```



## <a name="parameters"></a><span data-ttu-id="8bff5-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="8bff5-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8bff5-114">*Flags* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="8bff5-114">*flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8bff5-115">Der Wert der Konstante.</span><span class="sxs-lookup"><span data-stu-id="8bff5-115">The value of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8bff5-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8bff5-116">Return value</span></span>

<span data-ttu-id="8bff5-117">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="8bff5-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8bff5-118">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8bff5-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="8bff5-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8bff5-119">Requirements</span></span>



| <span data-ttu-id="8bff5-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8bff5-120">Requirement</span></span> | <span data-ttu-id="8bff5-121">Wert</span><span class="sxs-lookup"><span data-stu-id="8bff5-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8bff5-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8bff5-122">Minimum supported client</span></span><br/> | <span data-ttu-id="8bff5-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8bff5-123">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="8bff5-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8bff5-124">Minimum supported server</span></span><br/> | <span data-ttu-id="8bff5-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8bff5-125">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="8bff5-126">Header</span><span class="sxs-lookup"><span data-stu-id="8bff5-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="8bff5-127"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="8bff5-127"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="8bff5-128">IDL</span><span class="sxs-lookup"><span data-stu-id="8bff5-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8bff5-129"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8bff5-129"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="8bff5-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8bff5-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="8bff5-131"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="8bff5-131"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="8bff5-132">DLL</span><span class="sxs-lookup"><span data-stu-id="8bff5-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8bff5-133"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8bff5-133"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8bff5-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8bff5-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8bff5-135">**WSMAN**</span><span class="sxs-lookup"><span data-stu-id="8bff5-135">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="8bff5-136">**Iwsmanex**</span><span class="sxs-lookup"><span data-stu-id="8bff5-136">**IWSManEx**</span></span>](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanex)
</dt> <dt>

[<span data-ttu-id="8bff5-137">**IWSManSession**</span><span class="sxs-lookup"><span data-stu-id="8bff5-137">**IWSManSession**</span></span>](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession)
</dt> </dl>

 

 





