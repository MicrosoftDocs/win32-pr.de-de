---
description: Die Item-Methode des "errbemubjectset"-Objekts Ruft ein "errbewbject" aus der Auflistung ab.
ms.assetid: da91683c-9895-4110-9f51-c340a0c52aec
ms.tgt_platform: multiple
title: Errbemubjectset. Item-Methode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectSet.Item
- ISWbemObjectSet.Item
- ISWbemObjectSet.Item
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 69267b86a45cc1b95160e1400440b868426b7cae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348881"
---
# <a name="swbemobjectsetitem-method"></a><span data-ttu-id="d4341-103">Errbemubjectset. Item-Methode</span><span class="sxs-lookup"><span data-stu-id="d4341-103">SWbemObjectSet.Item method</span></span>

<span data-ttu-id="d4341-104">Die **Item** -Methode des " [**errbemubjectset**](swbemobjectset.md) "-Objekts Ruft ein " [**errbewbject**](swbemobject.md) " aus der Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="d4341-104">The **Item** method of the [**SWbemObjectSet**](swbemobjectset.md) object gets an [**SWbemObject**](swbemobject.md) from the collection.</span></span>

<span data-ttu-id="d4341-105">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="d4341-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d4341-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="d4341-106">Syntax</span></span>


```VB
objWbemObject = .Item( _
  ByVal strObjectPath _
)
```



## <a name="parameters"></a><span data-ttu-id="d4341-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="d4341-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4341-108">*strobjectpath*</span><span class="sxs-lookup"><span data-stu-id="d4341-108">*strObjectPath*</span></span> 
</dt> <dd>

<span data-ttu-id="d4341-109">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d4341-109">Required.</span></span> <span data-ttu-id="d4341-110">Relativer Pfad des-Objekts, das aus der Auflistung abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="d4341-110">Relative path of the object to retrieve from the collection.</span></span> <span data-ttu-id="d4341-111">Beispiel: Win32 \_ LogicalDisk = "C:"</span><span class="sxs-lookup"><span data-stu-id="d4341-111">Example: Win32\_LogicalDisk="C:"</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4341-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d4341-112">Return value</span></span>

<span data-ttu-id="d4341-113">Wenn der Vorgang erfolgreich ist, gibt das angeforderte [**Swap**](swbemobject.md) -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="d4341-113">If successful, the requested [**SWbemObject**](swbemobject.md) object returns.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d4341-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="d4341-114">Error codes</span></span>

<span data-ttu-id="d4341-115">Nach Abschluss der **Element** Methode kann das **Err** -Objekt einen der folgenden Fehlercodes enthalten.</span><span class="sxs-lookup"><span data-stu-id="d4341-115">Upon completion of the **Item** method, the **Err** object may contain one of the error codes below.</span></span>

<dl> <dt>

<span data-ttu-id="d4341-116">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="d4341-116">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="d4341-117">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="d4341-117">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="d4341-118">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="d4341-118">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="d4341-119">Es wurde ein ungültiger Parameter angegeben.</span><span class="sxs-lookup"><span data-stu-id="d4341-119">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="d4341-120">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="d4341-120">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="d4341-121">Der Arbeitsspeicher reicht nicht aus, um den Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="d4341-121">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="d4341-122">**wbemErrNotFound** -2147749890 (0x80041002 angezeigt)</span><span class="sxs-lookup"><span data-stu-id="d4341-122">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="d4341-123">Das angeforderte Element wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="d4341-123">Requested item was not found.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d4341-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d4341-124">Remarks</span></span>

<span data-ttu-id="d4341-125">Die **Item** -Methode kann viel Prozessorzeit erfordern, da eine komplette Enumeration durch den Anbieter der Elemente des Satzes erforderlich ist, um das Ergebnis zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="d4341-125">The **Item** method can require a lot of processor time because complete enumeration by the provider of the elements of the set is required to return the result.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4341-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d4341-126">Requirements</span></span>



| <span data-ttu-id="d4341-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d4341-127">Requirement</span></span> | <span data-ttu-id="d4341-128">Wert</span><span class="sxs-lookup"><span data-stu-id="d4341-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d4341-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d4341-129">Minimum supported client</span></span><br/> | <span data-ttu-id="d4341-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d4341-130">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d4341-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d4341-131">Minimum supported server</span></span><br/> | <span data-ttu-id="d4341-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d4341-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d4341-133">Header</span><span class="sxs-lookup"><span data-stu-id="d4341-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="d4341-134"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4341-134"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="d4341-135">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="d4341-135">Type library</span></span><br/>             | <dl> <span data-ttu-id="d4341-136"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d4341-136"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d4341-137">DLL</span><span class="sxs-lookup"><span data-stu-id="d4341-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d4341-138"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d4341-138"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="d4341-139">CLSID</span><span class="sxs-lookup"><span data-stu-id="d4341-139">CLSID</span></span><br/>                    | <span data-ttu-id="d4341-140">CLSID- \_ Swap-Objekt Satz</span><span class="sxs-lookup"><span data-stu-id="d4341-140">CLSID\_SWbemObjectSet</span></span><br/>                                                        |
| <span data-ttu-id="d4341-141">IID</span><span class="sxs-lookup"><span data-stu-id="d4341-141">IID</span></span><br/>                      | <span data-ttu-id="d4341-142">IID \_ iswbemubjectset</span><span class="sxs-lookup"><span data-stu-id="d4341-142">IID\_ISWbemObjectSet</span></span><br/>                                                         |



 

 




