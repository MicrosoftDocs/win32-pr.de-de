---
title: ResourceLocator. clearoptions-Methode (WSManDisp. h)
description: Entfernt alle Optionen aus dem ResourceLocator-Objekt.
ms.assetid: 1b4d7f15-c56f-4b0d-9614-8376012abca7
ms.tgt_platform: multiple
keywords:
- Clearoptions-Methode Windows-Remoteverwaltung
- Clearoptions-Methode Windows-Remoteverwaltung, ResourceLocator-Objekt
- ResourceLocator-Objekt Windows-Remoteverwaltung, clearoptions-Methode
topic_type:
- apiref
api_name:
- ResourceLocator.ClearOptions
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fda4be766b65756a9bcf8de02a4417fd15a3e7f2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858716"
---
# <a name="resourcelocatorclearoptions-method"></a><span data-ttu-id="72f1f-106">ResourceLocator. clearoptions-Methode</span><span class="sxs-lookup"><span data-stu-id="72f1f-106">ResourceLocator.ClearOptions method</span></span>

<span data-ttu-id="72f1f-107">Entfernt alle [*Optionen*](windows-remote-management-glossary.md) aus dem [**ResourceLocator**](resourcelocator.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="72f1f-107">Removes any [*options*](windows-remote-management-glossary.md) from the [**ResourceLocator**](resourcelocator.md) object.</span></span> <span data-ttu-id="72f1f-108">Sie können ein [**ResourceLocator**](resourcelocator.md) -Objekt bereitstellen, anstatt einen Ressourcen-URI in [**Sitzungs**](session.md) Objekt Vorgängen wie " [**Session. Get**](session-get.md)", " [**Session. Put**](session-put.md)" oder " [**Session. Enumerate**](session-enumerate.md)" anzugeben.</span><span class="sxs-lookup"><span data-stu-id="72f1f-108">You can provide a [**ResourceLocator**](resourcelocator.md) object instead of specifying a resource URI in [**Session**](session.md) object operations such as [**Session.Get**](session-get.md), [**Session.Put**](session-put.md), or [**Session.Enumerate**](session-enumerate.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="72f1f-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="72f1f-109">Syntax</span></span>


```VB
ResourceLocator.ClearOptions()
```



## <a name="parameters"></a><span data-ttu-id="72f1f-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="72f1f-110">Parameters</span></span>

<span data-ttu-id="72f1f-111">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="72f1f-111">This method has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="72f1f-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="72f1f-112">Remarks</span></span>

<span data-ttu-id="72f1f-113">**Iwsmanresourcelocator:: clearoptions** ist die entsprechende C++-Methode.</span><span class="sxs-lookup"><span data-stu-id="72f1f-113">**IWSManResourceLocator::ClearOptions** is the corresponding C++ method.</span></span>

## <a name="requirements"></a><span data-ttu-id="72f1f-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="72f1f-114">Requirements</span></span>



| <span data-ttu-id="72f1f-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="72f1f-115">Requirement</span></span> | <span data-ttu-id="72f1f-116">Wert</span><span class="sxs-lookup"><span data-stu-id="72f1f-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="72f1f-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="72f1f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="72f1f-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="72f1f-118">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="72f1f-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="72f1f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="72f1f-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="72f1f-120">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="72f1f-121">Header</span><span class="sxs-lookup"><span data-stu-id="72f1f-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="72f1f-122"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="72f1f-122"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="72f1f-123">IDL</span><span class="sxs-lookup"><span data-stu-id="72f1f-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="72f1f-124"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="72f1f-124"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="72f1f-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="72f1f-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="72f1f-126"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="72f1f-126"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="72f1f-127">DLL</span><span class="sxs-lookup"><span data-stu-id="72f1f-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="72f1f-128"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="72f1f-128"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="72f1f-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="72f1f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72f1f-130">**ResourceLocator**</span><span class="sxs-lookup"><span data-stu-id="72f1f-130">**ResourceLocator**</span></span>](resourcelocator.md)
</dt> </dl>

 

 





