---
description: Ruft ein Array von Zeigern auf elementbezeichnerlisten (pidls) für alle ausgewählten Objekte ab. Wird von der shshellfolderview- \_ Nachricht verwendet.
title: SFVM_GETSELECTEDOBJECTS Meldung (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 9639fbb6-d0ef-49b1-b3c5-e6a1dee0b7ad
api_name:
- SFVM_GETSELECTEDOBJECTS
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 056a9bd6bea78ef5093f6654b9935eb90e3759ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868696"
---
# <a name="sfvm_getselectedobjects-message"></a><span data-ttu-id="a7183-104">Sfvm \_ getSelectedObjects-Meldung</span><span class="sxs-lookup"><span data-stu-id="a7183-104">SFVM\_GETSELECTEDOBJECTS message</span></span>

<span data-ttu-id="a7183-105">Ruft ein Array von Zeigern auf elementbezeichnerlisten (pidls) für alle ausgewählten Objekte ab.</span><span class="sxs-lookup"><span data-stu-id="a7183-105">Retrieves an array of pointers to item identifier lists (PIDLs) for all selected objects.</span></span> <span data-ttu-id="a7183-106">Wird von der [**shshellfolderview- \_ Nachricht**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message)verwendet.</span><span class="sxs-lookup"><span data-stu-id="a7183-106">Used by [**SHShellFolderView\_Message**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).</span></span>


```C++
SFVM_GETSELECTEDOBJECTS 

    lParam = (LPARAM*) ppidl;

            
```



## <a name="parameters"></a><span data-ttu-id="a7183-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="a7183-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7183-108">*ppidl* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a7183-108">*ppidl* \[out\]</span></span>
</dt> <dd><span data-ttu-id="a7183-109">Die Adresse eines Arrays von pidls der aktuell ausgewählten Objekte.</span><span class="sxs-lookup"><span data-stu-id="a7183-109">The address of an array of PIDLs of currently selected objects.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7183-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a7183-110">Return value</span></span>

<span data-ttu-id="a7183-111">Gibt die Anzahl der Elemente im Array zurück.</span><span class="sxs-lookup"><span data-stu-id="a7183-111">Returns the number of items in the array.</span></span>

## <a name="remarks"></a><span data-ttu-id="a7183-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a7183-112">Remarks</span></span>

<span data-ttu-id="a7183-113">Wenn Sie fertig sind, sollten Sie für jedes Element des Arrays [**ilfree**](/windows/desktop/api/shlobj_core/nf-shlobj_core-ilfree) abrufen, um den Arbeitsspeicher freizugeben.</span><span class="sxs-lookup"><span data-stu-id="a7183-113">When finished, you should call [**ILFree**](/windows/desktop/api/shlobj_core/nf-shlobj_core-ilfree) on each member of the array to free the memory.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7183-114">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="a7183-114">Requirements</span></span>



| <span data-ttu-id="a7183-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a7183-115">Requirement</span></span> | <span data-ttu-id="a7183-116">Wert</span><span class="sxs-lookup"><span data-stu-id="a7183-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a7183-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a7183-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a7183-118">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a7183-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="a7183-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a7183-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a7183-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a7183-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="a7183-121">Header</span><span class="sxs-lookup"><span data-stu-id="a7183-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="a7183-122"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="a7183-122"><dt>Shlobj.h</dt></span></span> </dl> |



 

 




