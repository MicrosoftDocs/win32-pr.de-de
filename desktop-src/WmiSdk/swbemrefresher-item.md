---
description: Die Methode "Swap. Item" gibt das angegebene "taubemfreshableitem" aus der Auflistung zurück. "Taubemerfrischendes ableitem" aus der Sammlung.
ms.assetid: 8ae3dea5-0582-422e-9cd8-b6d91b41588a
ms.tgt_platform: multiple
title: Taubemaktusher. Item-Methode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefresher.Item
- ISWbemRefresher.Item
- ISWbemRefresher.Item
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: cfdbb592e6358fb1f8c5f3d45bb7e6bb780641c3
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104218990"
---
# <a name="swbemrefresheritem-method"></a><span data-ttu-id="09393-103">Taubemaktusher. Item-Methode</span><span class="sxs-lookup"><span data-stu-id="09393-103">SWbemRefresher.Item method</span></span>

<span data-ttu-id="09393-104">Die Methode " **Swap. Item** " gibt das angegebene " [**taubemfreshableitem**](swbemrefreshableitem.md) " aus der Auflistung zurück.</span><span class="sxs-lookup"><span data-stu-id="09393-104">The **SWbemRefresher.Item** method returns the specified [**SWbemRefreshableItem**](swbemrefreshableitem.md) from the collection.</span></span>

<span data-ttu-id="09393-105">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="09393-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="09393-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="09393-106">Syntax</span></span>


```VB
objItem = .Item( _
  ByVal lIndex _
)
```



## <a name="parameters"></a><span data-ttu-id="09393-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="09393-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09393-108">*Lindex*</span><span class="sxs-lookup"><span data-stu-id="09393-108">*lIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="09393-109">Der Indexwert des Elements in der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="09393-109">Index value of the item in the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09393-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="09393-110">Return value</span></span>

<span data-ttu-id="09393-111">Wenn der-Befehl erfolgreich ausgeführt wurde, wird das angegebene-Objekt von " [**Swap-ableitem**](swbemrefreshableitem.md) " zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="09393-111">If the call is successful, the specified [**SWbemRefreshableItem**](swbemrefreshableitem.md) object is returned.</span></span>

## <a name="error-codes"></a><span data-ttu-id="09393-112">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="09393-112">Error codes</span></span>

<span data-ttu-id="09393-113">Wenn das Aktualisierungs Programm kein Element mit dem angegebenen Index enthält, wird **wbemErrNotFound** generiert.</span><span class="sxs-lookup"><span data-stu-id="09393-113">If the refresher has no item with the specified index, **wbemErrNotFound** is generated.</span></span>

## <a name="requirements"></a><span data-ttu-id="09393-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="09393-114">Requirements</span></span>



| <span data-ttu-id="09393-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="09393-115">Requirement</span></span> | <span data-ttu-id="09393-116">Wert</span><span class="sxs-lookup"><span data-stu-id="09393-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="09393-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="09393-117">Minimum supported client</span></span><br/> | <span data-ttu-id="09393-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="09393-118">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="09393-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="09393-119">Minimum supported server</span></span><br/> | <span data-ttu-id="09393-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="09393-120">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="09393-121">Header</span><span class="sxs-lookup"><span data-stu-id="09393-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="09393-122"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="09393-122"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="09393-123">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="09393-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="09393-124"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="09393-124"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="09393-125">DLL</span><span class="sxs-lookup"><span data-stu-id="09393-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="09393-126"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="09393-126"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="09393-127">CLSID</span><span class="sxs-lookup"><span data-stu-id="09393-127">CLSID</span></span><br/>                    | <span data-ttu-id="09393-128">CLSID- \_ Austauschprogramm</span><span class="sxs-lookup"><span data-stu-id="09393-128">CLSID\_SWbemRefresher</span></span><br/>                                                        |
| <span data-ttu-id="09393-129">IID</span><span class="sxs-lookup"><span data-stu-id="09393-129">IID</span></span><br/>                      | <span data-ttu-id="09393-130">IID \_ iswbemfreshsher</span><span class="sxs-lookup"><span data-stu-id="09393-130">IID\_ISWbemRefresher</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="09393-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="09393-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09393-132">**Swap-Aktualisierungs Programm**</span><span class="sxs-lookup"><span data-stu-id="09393-132">**SWbemRefresher**</span></span>](swbemrefresher.md)
</dt> </dl>

 

 




