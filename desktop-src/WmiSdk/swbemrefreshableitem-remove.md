---
description: Die Methode "pulbemfreshableitem. Remove" entfernt das Objekt "pulbemfreshableitem" aus dem übergeordneten "pulbemaktusher"-Objekt. Das Objekt "Swap. metadatenableitem" aus dem übergeordneten "Swap"-Objekt.
ms.assetid: 8d3f5e22-c343-4191-a20a-6bca2ec9b01a
ms.tgt_platform: multiple
title: Taubemaktuableitem. Remove-Methode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefreshableItem.Remove
- ISWbemRefreshableItem.Remove
- ISWbemRefreshableItem.Remove
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 028bff202108481ce498be02c6014141313f27cc
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106354906"
---
# <a name="swbemrefreshableitemremove-method"></a><span data-ttu-id="4a4ea-103">Taubemaktuableitem. Remove-Methode</span><span class="sxs-lookup"><span data-stu-id="4a4ea-103">SWbemRefreshableItem.Remove method</span></span>

<span data-ttu-id="4a4ea-104">Die Methode " **pulbemfreshableitem. Remove** " entfernt das Objekt " [**pulbemfreshableitem**](swbemrefreshableitem.md) " aus dem übergeordneten " [**pulbemaktusher**](swbemrefresher.md) "-Objekt.</span><span class="sxs-lookup"><span data-stu-id="4a4ea-104">The **SWbemRefreshableItem.Remove** method removes the [**SWbemRefreshableItem**](swbemrefreshableitem.md) object from the parent [**SWbemRefresher**](swbemrefresher.md) object.</span></span>

<span data-ttu-id="4a4ea-105">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="4a4ea-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="4a4ea-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="4a4ea-106">Syntax</span></span>


```VB
SWbemRefreshableItem.Remove( _
  [ ByVal lFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="4a4ea-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="4a4ea-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a4ea-108">*lFlags* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="4a4ea-108">*lFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4a4ea-109">Dieser Parameter muss auf 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="4a4ea-109">This parameter must be set to 0 (zero).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a4ea-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4a4ea-110">Return value</span></span>

<span data-ttu-id="4a4ea-111">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="4a4ea-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a4ea-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4a4ea-112">Remarks</span></span>

<span data-ttu-id="4a4ea-113">**Fehler Codes** Wenn das Aktualisierungs Programm kein Element mit dem angegebenen Index enthält, wird **wbemErrNotFound** generiert.</span><span class="sxs-lookup"><span data-stu-id="4a4ea-113">**Error Codes** If the refresher has no item with the specified index, **wbemErrNotFound** is generated.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a4ea-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4a4ea-114">Requirements</span></span>



| <span data-ttu-id="4a4ea-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4a4ea-115">Requirement</span></span> | <span data-ttu-id="4a4ea-116">Wert</span><span class="sxs-lookup"><span data-stu-id="4a4ea-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4a4ea-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4a4ea-117">Minimum supported client</span></span><br/> | <span data-ttu-id="4a4ea-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4a4ea-118">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4a4ea-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4a4ea-119">Minimum supported server</span></span><br/> | <span data-ttu-id="4a4ea-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4a4ea-120">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4a4ea-121">Header</span><span class="sxs-lookup"><span data-stu-id="4a4ea-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a4ea-122"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a4ea-122"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="4a4ea-123">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="4a4ea-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="4a4ea-124"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="4a4ea-124"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="4a4ea-125">DLL</span><span class="sxs-lookup"><span data-stu-id="4a4ea-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4a4ea-126"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4a4ea-126"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="4a4ea-127">CLSID</span><span class="sxs-lookup"><span data-stu-id="4a4ea-127">CLSID</span></span><br/>                    | <span data-ttu-id="4a4ea-128">CLSID, \_ Swap-ableitem</span><span class="sxs-lookup"><span data-stu-id="4a4ea-128">CLSID\_SWbemRefreshableItem</span></span><br/>                                                  |
| <span data-ttu-id="4a4ea-129">IID</span><span class="sxs-lookup"><span data-stu-id="4a4ea-129">IID</span></span><br/>                      | <span data-ttu-id="4a4ea-130">IID \_ iswbemerfrischendes ableitem</span><span class="sxs-lookup"><span data-stu-id="4a4ea-130">IID\_ISWbemRefreshableItem</span></span><br/>                                                   |



## <a name="see-also"></a><span data-ttu-id="4a4ea-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4a4ea-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a4ea-132">**Swap-aktuableitem**</span><span class="sxs-lookup"><span data-stu-id="4a4ea-132">**SWbemRefreshableItem**</span></span>](swbemrefreshableitem.md)
</dt> <dt>

[<span data-ttu-id="4a4ea-133">**Swap-Aktualisierungs Programm**</span><span class="sxs-lookup"><span data-stu-id="4a4ea-133">**SWbemRefresher**</span></span>](swbemrefresher.md)
</dt> </dl>

 

 




