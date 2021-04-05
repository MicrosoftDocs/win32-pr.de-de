---
description: Die Clone-Methode des Swap-namedvalueset-Objekts gibt ein neues-Objekt zurück, das ein Klon der aktuellen Auflistung ist.
ms.assetid: 0e7fab2e-8175-45e5-aa70-1109502e2b3f
ms.tgt_platform: multiple
title: Swap-namedvalueset. Clone-Methode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemNamedValueSet.Clone
- ISWbemNamedValueSet.Clone
- ISWbemNamedValueSet.Clone
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 17678d36a553c84c008f606c647d7ff1fa9dfadc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103756973"
---
# <a name="swbemnamedvaluesetclone-method"></a><span data-ttu-id="86082-103">Swap-namedvalueset. Clone-Methode</span><span class="sxs-lookup"><span data-stu-id="86082-103">SWbemNamedValueSet.Clone method</span></span>

<span data-ttu-id="86082-104">Die **Clone** -Methode des [**Swap-namedvalueset**](swbemnamedvalueset.md) -Objekts gibt ein neues-Objekt zurück, das ein Klon der aktuellen Auflistung ist.</span><span class="sxs-lookup"><span data-stu-id="86082-104">The **Clone** method of the [**SWbemNamedValueSet**](swbemnamedvalueset.md) object returns a new object that is a clone of the current collection.</span></span>

<span data-ttu-id="86082-105">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="86082-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="86082-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="86082-106">Syntax</span></span>


```VB
objwbemNamedValueSet = .Clone( _
)
```



## <a name="parameters"></a><span data-ttu-id="86082-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="86082-107">Parameters</span></span>

<span data-ttu-id="86082-108">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="86082-108">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="86082-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="86082-109">Return value</span></span>

<span data-ttu-id="86082-110">Bei erfolgreicher Ausführung gibt ein neues Objekt vom [**metadatennamedvalueset**](swbemnamedvalueset.md) zurück.</span><span class="sxs-lookup"><span data-stu-id="86082-110">If successful, a new [**SWbemNamedValueSet**](swbemnamedvalueset.md) object returns.</span></span>

## <a name="error-codes"></a><span data-ttu-id="86082-111">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="86082-111">Error codes</span></span>

<span data-ttu-id="86082-112">Nach Abschluss der **Klon** Methode kann das **Err** -Objekt einen der folgenden Fehlercodes enthalten.</span><span class="sxs-lookup"><span data-stu-id="86082-112">Upon completion of the **Clone** method, the **Err** object may contain one of the error codes below.</span></span>

<dl> <dt>

<span data-ttu-id="86082-113">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="86082-113">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="86082-114">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="86082-114">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="86082-115">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="86082-115">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="86082-116">Nicht genügend Arbeitsspeicher zum Klonen des Objekts.</span><span class="sxs-lookup"><span data-stu-id="86082-116">Not enough memory to clone the object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="86082-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="86082-117">Remarks</span></span>

<span data-ttu-id="86082-118">Verwenden Sie diese Methode, um eine Sammlung von " [**Swap namedvalueset**](swbemnamedvalueset.md) " zu duplizieren.</span><span class="sxs-lookup"><span data-stu-id="86082-118">Use this method to duplicate an [**SWbemNamedValueSet**](swbemnamedvalueset.md) collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="86082-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="86082-119">Requirements</span></span>



| <span data-ttu-id="86082-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="86082-120">Requirement</span></span> | <span data-ttu-id="86082-121">Wert</span><span class="sxs-lookup"><span data-stu-id="86082-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="86082-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="86082-122">Minimum supported client</span></span><br/> | <span data-ttu-id="86082-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="86082-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="86082-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="86082-124">Minimum supported server</span></span><br/> | <span data-ttu-id="86082-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="86082-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="86082-126">Header</span><span class="sxs-lookup"><span data-stu-id="86082-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="86082-127"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="86082-127"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="86082-128">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="86082-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="86082-129"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="86082-129"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="86082-130">DLL</span><span class="sxs-lookup"><span data-stu-id="86082-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="86082-131"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="86082-131"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="86082-132">CLSID</span><span class="sxs-lookup"><span data-stu-id="86082-132">CLSID</span></span><br/>                    | <span data-ttu-id="86082-133">CLSID- \_ Swap-namedvalueset</span><span class="sxs-lookup"><span data-stu-id="86082-133">CLSID\_SWbemNamedValueSet</span></span><br/>                                                    |
| <span data-ttu-id="86082-134">IID</span><span class="sxs-lookup"><span data-stu-id="86082-134">IID</span></span><br/>                      | <span data-ttu-id="86082-135">IID \_ iswbemnamedvalueset</span><span class="sxs-lookup"><span data-stu-id="86082-135">IID\_ISWbemNamedValueSet</span></span><br/>                                                     |



## <a name="see-also"></a><span data-ttu-id="86082-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="86082-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86082-137">**Austausch Elementname**</span><span class="sxs-lookup"><span data-stu-id="86082-137">**SWbemNamedValueSet**</span></span>](swbemnamedvalueset.md)
</dt> </dl>

 

 




