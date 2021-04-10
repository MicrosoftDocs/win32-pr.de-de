---
description: Die Methode "Swap. Remove" entfernt das Objekt "pulbemfreshableitem" mit dem angegebenen Index aus dem Aktualisierungs Programm.
ms.assetid: db5ac740-e2b3-4667-b511-d750cb092e0f
ms.tgt_platform: multiple
title: Taubemaktusher. Remove-Methode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefresher.Remove
- ISWbemRefresher.Remove
- ISWbemRefresher.Remove
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 9504b81ce83a91695765e75e74de374437c188d4
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "103961180"
---
# <a name="swbemrefresherremove-method"></a><span data-ttu-id="1b11c-103">Swap. Remove-Methode</span><span class="sxs-lookup"><span data-stu-id="1b11c-103">SWbemRefresher.Remove method</span></span>

<span data-ttu-id="1b11c-104">Die Methode " **Swap. Remove** " entfernt das Objekt " [**pulbemfreshableitem**](swbemrefreshableitem.md) " mit dem angegebenen Index aus dem Aktualisierungs Programm.</span><span class="sxs-lookup"><span data-stu-id="1b11c-104">The **SWbemRefresher.Remove** method removes the [**SWbemRefreshableItem**](swbemrefreshableitem.md) object with the specified index from the refresher.</span></span> <span data-ttu-id="1b11c-105">Das Objekt " **taubemerfrischendes ableitem** " kann entweder ein einzelnes Objekt oder einen Objekt Satz darstellen.</span><span class="sxs-lookup"><span data-stu-id="1b11c-105">The **SWbemRefreshableItem** object can represent either a single object or an object set.</span></span>

<span data-ttu-id="1b11c-106">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="1b11c-106">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="1b11c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="1b11c-107">Syntax</span></span>


```VB
objRefresher = .Remove( _
  ByVal LIndex, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedvalueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="1b11c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="1b11c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b11c-109">*Lindex*</span><span class="sxs-lookup"><span data-stu-id="1b11c-109">*LIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="1b11c-110">Der Index des Elements im " [**Swap**](swbemrefresher.md) -Aktualisierer"-Objekt.</span><span class="sxs-lookup"><span data-stu-id="1b11c-110">Index of the item in the [**SWbemRefresher**](swbemrefresher.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="1b11c-111">*IFlags* \[ optionale\]</span><span class="sxs-lookup"><span data-stu-id="1b11c-111">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1b11c-112">Flags müssen auf T0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="1b11c-112">Flags must be set t0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="1b11c-113">*objwbemnamedvalueset* \[ optionale\]</span><span class="sxs-lookup"><span data-stu-id="1b11c-113">*objWbemNamedvalueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1b11c-114">Null.</span><span class="sxs-lookup"><span data-stu-id="1b11c-114">Null.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b11c-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1b11c-115">Return value</span></span>

<span data-ttu-id="1b11c-116">Diese Methode hat keine Rückgabewerte.</span><span class="sxs-lookup"><span data-stu-id="1b11c-116">This method has no return values.</span></span>

## <a name="remarks"></a><span data-ttu-id="1b11c-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1b11c-117">Remarks</span></span>

<span data-ttu-id="1b11c-118">**Fehlercodes** Wenn das Aktualisierungs Programm kein Element mit dem angegebenen Index enthält, wird **wbemErrNotFound** generiert.</span><span class="sxs-lookup"><span data-stu-id="1b11c-118">**Error codes** If the refresher has no item with the specified index, **wbemErrNotFound** is generated.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b11c-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1b11c-119">Requirements</span></span>



| <span data-ttu-id="1b11c-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1b11c-120">Requirement</span></span> | <span data-ttu-id="1b11c-121">Wert</span><span class="sxs-lookup"><span data-stu-id="1b11c-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1b11c-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1b11c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="1b11c-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1b11c-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1b11c-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1b11c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="1b11c-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1b11c-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1b11c-126">Header</span><span class="sxs-lookup"><span data-stu-id="1b11c-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b11c-127"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="1b11c-127"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="1b11c-128">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="1b11c-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="1b11c-129"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="1b11c-129"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="1b11c-130">DLL</span><span class="sxs-lookup"><span data-stu-id="1b11c-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1b11c-131"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1b11c-131"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="1b11c-132">CLSID</span><span class="sxs-lookup"><span data-stu-id="1b11c-132">CLSID</span></span><br/>                    | <span data-ttu-id="1b11c-133">CLSID- \_ Austauschprogramm</span><span class="sxs-lookup"><span data-stu-id="1b11c-133">CLSID\_SWbemRefresher</span></span><br/>                                                        |
| <span data-ttu-id="1b11c-134">IID</span><span class="sxs-lookup"><span data-stu-id="1b11c-134">IID</span></span><br/>                      | <span data-ttu-id="1b11c-135">IID \_ iswbemfreshsher</span><span class="sxs-lookup"><span data-stu-id="1b11c-135">IID\_ISWbemRefresher</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="1b11c-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1b11c-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b11c-137">**Swap-Aktualisierungs Programm**</span><span class="sxs-lookup"><span data-stu-id="1b11c-137">**SWbemRefresher**</span></span>](swbemrefresher.md)
</dt> </dl>

 

 




