---
description: Die Item-Methode des-Objekts von "taubemqualifierset" gibt ein benanntes "Swap"-Objekt aus der Auflistung zurück. Dies ist die Standardmethode dieses Objekts.
ms.assetid: 5ed3a336-c06f-446d-85d4-243daddc82a5
ms.tgt_platform: multiple
title: Taubemqualifierset. Item-Methode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemQualifierSet.Item
- ISWbemQualifierSet.Item
- ISWbemQualifierSet.Item
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 9c89ff554b049e6730a64ebf7e5f017fc8a5652f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868572"
---
# <a name="swbemqualifiersetitem-method"></a><span data-ttu-id="c4afa-104">Taubemqualifierset. Item-Methode</span><span class="sxs-lookup"><span data-stu-id="c4afa-104">SWbemQualifierSet.Item method</span></span>

<span data-ttu-id="c4afa-105">Die **Item** -Methode des-Objekts von " [**taubemqualifierset**](swbemqualifierset.md) " gibt ein benanntes " [**Swap**](swbemqualifier.md) "-Objekt aus der Auflistung zurück.</span><span class="sxs-lookup"><span data-stu-id="c4afa-105">The **Item** method of the [**SWbemQualifierSet**](swbemqualifierset.md) object returns a named [**SWbemQualifier**](swbemqualifier.md) object from the collection.</span></span> <span data-ttu-id="c4afa-106">Dies ist die Standardmethode dieses Objekts.</span><span class="sxs-lookup"><span data-stu-id="c4afa-106">This is the default method of this object.</span></span>

<span data-ttu-id="c4afa-107">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="c4afa-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="c4afa-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c4afa-108">Syntax</span></span>


```VB
objQualifier = .Item( _
  ByVal strName, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="c4afa-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="c4afa-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4afa-110">" *Name* \[ " in\]</span><span class="sxs-lookup"><span data-stu-id="c4afa-110">*strName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4afa-111">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c4afa-111">Required.</span></span> <span data-ttu-id="c4afa-112">Der Name des abzurufenden Qualifizierers.</span><span class="sxs-lookup"><span data-stu-id="c4afa-112">Name of the qualifier to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="c4afa-113">*IFlags* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="c4afa-113">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c4afa-114">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="c4afa-114">Reserved.</span></span> <span data-ttu-id="c4afa-115">Der Standardwert ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="c4afa-115">The default value is 0 (zero).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4afa-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c4afa-116">Return value</span></span>

<span data-ttu-id="c4afa-117">Wenn der Vorgang erfolgreich ist, wird das angeforderte [**Austausch qualifizierungsobjekt**](swbemqualifier.md) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c4afa-117">If successful, the requested [**SWbemQualifier**](swbemqualifier.md) object is returned.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c4afa-118">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="c4afa-118">Error codes</span></span>

<span data-ttu-id="c4afa-119">Nach Abschluss der **Element** Methode kann das **Err** -Objekt einen der Fehlercodes in der folgenden Liste enthalten.</span><span class="sxs-lookup"><span data-stu-id="c4afa-119">After completion of the **Item** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="c4afa-120">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="c4afa-120">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="c4afa-121">Der *IFlags* -Parameter war ungültig.</span><span class="sxs-lookup"><span data-stu-id="c4afa-121">The *iFlags* parameter was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="c4afa-122">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="c4afa-122">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="c4afa-123">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="c4afa-123">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="c4afa-124">**wbemErrNotFound** -2147749890 (0x80041002 angezeigt)</span><span class="sxs-lookup"><span data-stu-id="c4afa-124">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="c4afa-125">Der angegebene Qualifizierer ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="c4afa-125">Specified qualifier does not exist.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c4afa-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c4afa-126">Requirements</span></span>



| <span data-ttu-id="c4afa-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c4afa-127">Requirement</span></span> | <span data-ttu-id="c4afa-128">Wert</span><span class="sxs-lookup"><span data-stu-id="c4afa-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c4afa-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c4afa-129">Minimum supported client</span></span><br/> | <span data-ttu-id="c4afa-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c4afa-130">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c4afa-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c4afa-131">Minimum supported server</span></span><br/> | <span data-ttu-id="c4afa-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c4afa-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c4afa-133">Header</span><span class="sxs-lookup"><span data-stu-id="c4afa-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="c4afa-134"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c4afa-134"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="c4afa-135">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="c4afa-135">Type library</span></span><br/>             | <dl> <span data-ttu-id="c4afa-136"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c4afa-136"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c4afa-137">DLL</span><span class="sxs-lookup"><span data-stu-id="c4afa-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c4afa-138"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c4afa-138"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="c4afa-139">CLSID</span><span class="sxs-lookup"><span data-stu-id="c4afa-139">CLSID</span></span><br/>                    | <span data-ttu-id="c4afa-140">CLSID- \_ Swap-Gruppe</span><span class="sxs-lookup"><span data-stu-id="c4afa-140">CLSID\_SWbemQualifierSet</span></span><br/>                                                     |
| <span data-ttu-id="c4afa-141">IID</span><span class="sxs-lookup"><span data-stu-id="c4afa-141">IID</span></span><br/>                      | <span data-ttu-id="c4afa-142">IID \_ iswbemqualifierset</span><span class="sxs-lookup"><span data-stu-id="c4afa-142">IID\_ISWbemQualifierSet</span></span><br/>                                                      |



## <a name="see-also"></a><span data-ttu-id="c4afa-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c4afa-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4afa-144">**Swap-qualifierset**</span><span class="sxs-lookup"><span data-stu-id="c4afa-144">**SWbemQualifierSet**</span></span>](swbemqualifierset.md)
</dt> <dt>

[<span data-ttu-id="c4afa-145">**Austausch Qualifizierer**</span><span class="sxs-lookup"><span data-stu-id="c4afa-145">**SWbemQualifier**</span></span>](swbemqualifier.md)
</dt> </dl>

 

 




