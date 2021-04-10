---
title: ResourceLocator. clearselectors-Methode (WSManDisp. h)
description: Entfernt alle Selektoren aus einem ResourceLocator-Objekt.
ms.assetid: 759880e6-5026-45de-b7e1-a4f5a16c32a0
ms.tgt_platform: multiple
keywords:
- Clearselectors-Methode Windows-Remoteverwaltung
- Clearselectors-Methode Windows-Remoteverwaltung, ResourceLocator-Objekt
- ResourceLocator-Objekt Windows-Remoteverwaltung, clearselectors-Methode
topic_type:
- apiref
api_name:
- ResourceLocator.ClearSelectors
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd5dbf1322a5e0c36a1383581e2822fbd00a00e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105627"
---
# <a name="resourcelocatorclearselectors-method"></a><span data-ttu-id="0cdb2-106">ResourceLocator. clearselectors-Methode</span><span class="sxs-lookup"><span data-stu-id="0cdb2-106">ResourceLocator.ClearSelectors method</span></span>

<span data-ttu-id="0cdb2-107">Entfernt alle [*Selektoren*](windows-remote-management-glossary.md) aus einem [**ResourceLocator**](resourcelocator.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="0cdb2-107">Removes all of the [*selectors*](windows-remote-management-glossary.md) from a [**ResourceLocator**](resourcelocator.md) object.</span></span> <span data-ttu-id="0cdb2-108">Sie können ein [**ResourceLocator**](resourcelocator.md) -Objekt bereitstellen, anstatt einen Ressourcen-URI in [**Sitzungs**](session.md) Objekt Vorgängen wie " [**Session. Get**](session-get.md)", " [**Session. Put**](session-put.md)" oder " [**Session. Enumerate**](session-enumerate.md)" anzugeben.</span><span class="sxs-lookup"><span data-stu-id="0cdb2-108">You can provide a [**ResourceLocator**](resourcelocator.md) object instead of specifying a resource URI in [**Session**](session.md) object operations such as [**Session.Get**](session-get.md), [**Session.Put**](session-put.md), or [**Session.Enumerate**](session-enumerate.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="0cdb2-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="0cdb2-109">Syntax</span></span>


```VB
ResourceLocator.ClearSelectors()
```



## <a name="parameters"></a><span data-ttu-id="0cdb2-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="0cdb2-110">Parameters</span></span>

<span data-ttu-id="0cdb2-111">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="0cdb2-111">This method has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="0cdb2-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0cdb2-112">Remarks</span></span>

<span data-ttu-id="0cdb2-113">**Iwsmanresourcelocator:: clearselectors** ist die entsprechende C++-Methode.</span><span class="sxs-lookup"><span data-stu-id="0cdb2-113">**IWSManResourceLocator::ClearSelectors** is the corresponding C++ method.</span></span>

## <a name="requirements"></a><span data-ttu-id="0cdb2-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0cdb2-114">Requirements</span></span>



| <span data-ttu-id="0cdb2-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0cdb2-115">Requirement</span></span> | <span data-ttu-id="0cdb2-116">Wert</span><span class="sxs-lookup"><span data-stu-id="0cdb2-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0cdb2-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0cdb2-117">Minimum supported client</span></span><br/> | <span data-ttu-id="0cdb2-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0cdb2-118">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="0cdb2-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0cdb2-119">Minimum supported server</span></span><br/> | <span data-ttu-id="0cdb2-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0cdb2-120">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="0cdb2-121">Header</span><span class="sxs-lookup"><span data-stu-id="0cdb2-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="0cdb2-122"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="0cdb2-122"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="0cdb2-123">IDL</span><span class="sxs-lookup"><span data-stu-id="0cdb2-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0cdb2-124"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0cdb2-124"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="0cdb2-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0cdb2-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="0cdb2-126"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="0cdb2-126"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="0cdb2-127">DLL</span><span class="sxs-lookup"><span data-stu-id="0cdb2-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0cdb2-128"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0cdb2-128"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0cdb2-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0cdb2-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0cdb2-130">**ResourceLocator**</span><span class="sxs-lookup"><span data-stu-id="0cdb2-130">**ResourceLocator**</span></span>](resourcelocator.md)
</dt> </dl>

 

 





