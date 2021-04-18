---
description: Die Item-Methode des Objekts "Swap-methodset" gibt ein benanntes "taubemmethod"-Objekt aus der Auflistung zurück.
ms.assetid: 4c1bbecc-b38b-4869-9c8c-b9321536b23e
ms.tgt_platform: multiple
title: Swap. Item-Methode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemMethodSet.Item
- ISWbemMethodSet.Item
- ISWbemMethodSet.Item
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 89d20dc652189abe3354f5d1b51c03279d3f74c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347313"
---
# <a name="swbemmethodsetitem-method"></a><span data-ttu-id="54f07-103">Taubemmethodset. Item-Methode</span><span class="sxs-lookup"><span data-stu-id="54f07-103">SWbemMethodSet.Item method</span></span>

<span data-ttu-id="54f07-104">Die **Item** -Methode des Objekts " [**Swap-methodset**](swbemmethodset.md) " gibt ein benanntes " [**taubemmethod**](swbemmethod.md) "-Objekt aus der Auflistung zurück.</span><span class="sxs-lookup"><span data-stu-id="54f07-104">The **Item** method of the [**SWbemMethodSet**](swbemmethodset.md) object returns a named [**SWbemMethod**](swbemmethod.md) object from the collection.</span></span>

<span data-ttu-id="54f07-105">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="54f07-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="54f07-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="54f07-106">Syntax</span></span>


```VB
objMethod = .Item( _
  ByVal strName, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="54f07-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="54f07-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54f07-108">" *Name* \[ " in\]</span><span class="sxs-lookup"><span data-stu-id="54f07-108">*strName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54f07-109">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="54f07-109">Required.</span></span> <span data-ttu-id="54f07-110">Der Name der abzurufenden Methode.</span><span class="sxs-lookup"><span data-stu-id="54f07-110">Name of the method to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="54f07-111">*IFlags* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="54f07-111">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="54f07-112">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="54f07-112">Reserved.</span></span> <span data-ttu-id="54f07-113">Der Standardwert ist 0.</span><span class="sxs-lookup"><span data-stu-id="54f07-113">The default value is 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54f07-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="54f07-114">Return value</span></span>

<span data-ttu-id="54f07-115">Bei erfolgreicher Ausführung gibt das angeforderte " [**Swap Method**](swbemmethod.md) "-Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="54f07-115">If successful, the requested [**SWbemMethod**](swbemmethod.md) object returns.</span></span>

## <a name="error-codes"></a><span data-ttu-id="54f07-116">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="54f07-116">Error codes</span></span>

<span data-ttu-id="54f07-117">Nach Abschluss der **Element** Methode kann das **Err** -Objekt einen der Fehlercodes in der folgenden Liste enthalten.</span><span class="sxs-lookup"><span data-stu-id="54f07-117">Upon completion of the **Item** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="54f07-118">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="54f07-118">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="54f07-119">Der *IFlags* -Parameter war ungültig.</span><span class="sxs-lookup"><span data-stu-id="54f07-119">The *iFlags* parameter was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="54f07-120">**wbemErrFailed** -2147749894</span><span class="sxs-lookup"><span data-stu-id="54f07-120">**wbemErrFailed** - 2147749894</span></span>
</dt> <dd>

<span data-ttu-id="54f07-121">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="54f07-121">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="54f07-122">**wbemErrNotFound** -2147749890 (0x80041002 angezeigt)</span><span class="sxs-lookup"><span data-stu-id="54f07-122">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="54f07-123">Die angegebene Methode ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="54f07-123">The specified method does not exist.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="54f07-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="54f07-124">Requirements</span></span>



| <span data-ttu-id="54f07-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="54f07-125">Requirement</span></span> | <span data-ttu-id="54f07-126">Wert</span><span class="sxs-lookup"><span data-stu-id="54f07-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="54f07-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="54f07-127">Minimum supported client</span></span><br/> | <span data-ttu-id="54f07-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="54f07-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="54f07-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="54f07-129">Minimum supported server</span></span><br/> | <span data-ttu-id="54f07-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="54f07-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="54f07-131">Header</span><span class="sxs-lookup"><span data-stu-id="54f07-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="54f07-132"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="54f07-132"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="54f07-133">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="54f07-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="54f07-134"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="54f07-134"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="54f07-135">DLL</span><span class="sxs-lookup"><span data-stu-id="54f07-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="54f07-136"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="54f07-136"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="54f07-137">CLSID</span><span class="sxs-lookup"><span data-stu-id="54f07-137">CLSID</span></span><br/>                    | <span data-ttu-id="54f07-138">CLSID- \_ Swap-Methode</span><span class="sxs-lookup"><span data-stu-id="54f07-138">CLSID\_SWbemMethodSet</span></span><br/>                                                        |
| <span data-ttu-id="54f07-139">IID</span><span class="sxs-lookup"><span data-stu-id="54f07-139">IID</span></span><br/>                      | <span data-ttu-id="54f07-140">IID \_ iswbemmethodset</span><span class="sxs-lookup"><span data-stu-id="54f07-140">IID\_ISWbemMethodSet</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="54f07-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="54f07-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54f07-142">**Swap-methodset**</span><span class="sxs-lookup"><span data-stu-id="54f07-142">**SWbemMethodSet**</span></span>](swbemmethodset.md)
</dt> <dt>

[<span data-ttu-id="54f07-143">**Swap-Methode**</span><span class="sxs-lookup"><span data-stu-id="54f07-143">**SWbemMethod**</span></span>](swbemmethod.md)
</dt> </dl>

 

 




