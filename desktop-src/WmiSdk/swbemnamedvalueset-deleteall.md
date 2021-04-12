---
description: Die DeleteAll-Methode des "pulbemnamedvalueset"-Objekts entfernt alle benannten Werte aus der Auflistung und entleert Sie somit.
ms.assetid: db5d2e68-028e-4902-ad42-0b46e1a96bcb
ms.tgt_platform: multiple
title: Taubemnamedvalueset. DeleteAll-Methode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemNamedValueSet.DeleteAll
- ISWbemNamedValueSet.DeleteAll
- ISWbemNamedValueSet.DeleteAll
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 9df7b08dddf4cf9f1a687a262721452c0780267a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216516"
---
# <a name="swbemnamedvaluesetdeleteall-method"></a><span data-ttu-id="1aba7-103">Taubemnamedvalueset. DeleteAll-Methode</span><span class="sxs-lookup"><span data-stu-id="1aba7-103">SWbemNamedValueSet.DeleteAll method</span></span>

<span data-ttu-id="1aba7-104">Die **DeleteAll** -Methode des " [**pulbemnamedvalueset**](swbemnamedvalueset.md) "-Objekts entfernt alle benannten Werte aus der Auflistung und entleert Sie somit.</span><span class="sxs-lookup"><span data-stu-id="1aba7-104">The **DeleteAll** method of the [**SWbemNamedValueSet**](swbemnamedvalueset.md) object removes all named values from the collection, thus emptying it.</span></span>

## <a name="syntax"></a><span data-ttu-id="1aba7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1aba7-105">Syntax</span></span>


```VB
SWbemNamedValueSet.DeleteAll()
```



## <a name="parameters"></a><span data-ttu-id="1aba7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1aba7-106">Parameters</span></span>

<span data-ttu-id="1aba7-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="1aba7-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1aba7-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1aba7-108">Return value</span></span>

<span data-ttu-id="1aba7-109">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="1aba7-109">This method does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="1aba7-110">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="1aba7-110">Error codes</span></span>

<span data-ttu-id="1aba7-111">Nach Abschluss der **DeleteAll** -Methode kann das **Err** -Objekt den folgenden Fehlercode enthalten.</span><span class="sxs-lookup"><span data-stu-id="1aba7-111">Upon completion of the **DeleteAll** method, the **Err** object may contain the error code below.</span></span>

<dl> <dt>

<span data-ttu-id="1aba7-112">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="1aba7-112">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="1aba7-113">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="1aba7-113">Unspecified error.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1aba7-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1aba7-114">Requirements</span></span>



| <span data-ttu-id="1aba7-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1aba7-115">Requirement</span></span> | <span data-ttu-id="1aba7-116">Wert</span><span class="sxs-lookup"><span data-stu-id="1aba7-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1aba7-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1aba7-117">Minimum supported client</span></span><br/> | <span data-ttu-id="1aba7-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1aba7-118">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1aba7-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1aba7-119">Minimum supported server</span></span><br/> | <span data-ttu-id="1aba7-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1aba7-120">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1aba7-121">Header</span><span class="sxs-lookup"><span data-stu-id="1aba7-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="1aba7-122"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="1aba7-122"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="1aba7-123">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="1aba7-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="1aba7-124"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="1aba7-124"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="1aba7-125">DLL</span><span class="sxs-lookup"><span data-stu-id="1aba7-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1aba7-126"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1aba7-126"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="1aba7-127">CLSID</span><span class="sxs-lookup"><span data-stu-id="1aba7-127">CLSID</span></span><br/>                    | <span data-ttu-id="1aba7-128">CLSID- \_ Swap-namedvalueset</span><span class="sxs-lookup"><span data-stu-id="1aba7-128">CLSID\_SWbemNamedValueSet</span></span><br/>                                                    |
| <span data-ttu-id="1aba7-129">IID</span><span class="sxs-lookup"><span data-stu-id="1aba7-129">IID</span></span><br/>                      | <span data-ttu-id="1aba7-130">IID \_ iswbemnamedvalueset</span><span class="sxs-lookup"><span data-stu-id="1aba7-130">IID\_ISWbemNamedValueSet</span></span><br/>                                                     |



## <a name="see-also"></a><span data-ttu-id="1aba7-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1aba7-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1aba7-132">**Austausch Elementname**</span><span class="sxs-lookup"><span data-stu-id="1aba7-132">**SWbemNamedValueSet**</span></span>](swbemnamedvalueset.md)
</dt> <dt>

[<span data-ttu-id="1aba7-133">**Swap Name User. Remove**</span><span class="sxs-lookup"><span data-stu-id="1aba7-133">**SWbemNamedValueSet.Remove**</span></span>](swbemnamedvalueset-remove.md)
</dt> </dl>

 

 




