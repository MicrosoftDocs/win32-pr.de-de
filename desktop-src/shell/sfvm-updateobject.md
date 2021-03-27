---
description: Aktualisiert ein Objekt durch Übergabe eines Zeigers auf ein Array von zwei Zeigern auf Element Bezeichner Listen (pidls). Wird von der shshellfolderview- \_ Nachricht verwendet.
title: SFVM_UPDATEOBJECT Meldung (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 3bd68ace-3ccf-446c-8cf9-52f42444674e
api_name:
- SFVM_UPDATEOBJECT
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 4367551cdf2d48a06c633329ad850c3f7c2e0976
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218581"
---
# <a name="sfvm_updateobject-message"></a><span data-ttu-id="59a05-104">Sfvm- \_ UpdateObject-Nachricht</span><span class="sxs-lookup"><span data-stu-id="59a05-104">SFVM\_UPDATEOBJECT message</span></span>

<span data-ttu-id="59a05-105">Aktualisiert ein Objekt durch Übergabe eines Zeigers auf ein Array von zwei Zeigern auf Element Bezeichner Listen (pidls).</span><span class="sxs-lookup"><span data-stu-id="59a05-105">Updates an object by passing a pointer to an array of two pointers to item identifier lists (PIDLs).</span></span> <span data-ttu-id="59a05-106">Wird von der [**shshellfolderview- \_ Nachricht**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message)verwendet.</span><span class="sxs-lookup"><span data-stu-id="59a05-106">Used by [**SHShellFolderView\_Message**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).</span></span>


```C++

                SFVM_UPDATEOBJECT 

    lParam = (LPARAM*) ppidl;

            
```



## <a name="parameters"></a><span data-ttu-id="59a05-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="59a05-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59a05-108">*ppidl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="59a05-108">*ppidl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59a05-109">Die Adresse eines Arrays mit zwei pidls.</span><span class="sxs-lookup"><span data-stu-id="59a05-109">The address of an array of two PIDLs.</span></span> <span data-ttu-id="59a05-110">Die erste PIDL ist die alte PIDL.</span><span class="sxs-lookup"><span data-stu-id="59a05-110">The first PIDL is the old PIDL.</span></span> <span data-ttu-id="59a05-111">Die zweite ist eine Kopie der alten PIDL mit aktualisierten Informationen.</span><span class="sxs-lookup"><span data-stu-id="59a05-111">The second one is a copy of the old PIDL with updated information.</span></span> <span data-ttu-id="59a05-112">Die Kontrolle über die Lebensdauer des Kopiervorgangs gehört der Ansicht nach erfolgreichem Abschluss dieses Aufrufens an.</span><span class="sxs-lookup"><span data-stu-id="59a05-112">Control over the copy's lifetime belongs to the view after successful completion of this call.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59a05-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="59a05-113">Return value</span></span>

<span data-ttu-id="59a05-114">Gibt die ListView-ID des aktualisierten Objekts zurück, wenn das Update erfolgreich war. Andernfalls wird-1 zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="59a05-114">Returns the listview ID of the updated object if the update was successful; otherwise, it returns -1.</span></span>

## <a name="remarks"></a><span data-ttu-id="59a05-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="59a05-115">Remarks</span></span>

<span data-ttu-id="59a05-116">Wenn das Update nicht erfolgreich war, muss der Aufrufer den Arbeitsspeicher freigeben.</span><span class="sxs-lookup"><span data-stu-id="59a05-116">If the update was unsuccessful, the caller must free the memory.</span></span>

## <a name="requirements"></a><span data-ttu-id="59a05-117">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="59a05-117">Requirements</span></span>



| <span data-ttu-id="59a05-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="59a05-118">Requirement</span></span> | <span data-ttu-id="59a05-119">Wert</span><span class="sxs-lookup"><span data-stu-id="59a05-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="59a05-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="59a05-120">Minimum supported client</span></span><br/> | <span data-ttu-id="59a05-121">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="59a05-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="59a05-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="59a05-122">Minimum supported server</span></span><br/> | <span data-ttu-id="59a05-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="59a05-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="59a05-124">Header</span><span class="sxs-lookup"><span data-stu-id="59a05-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="59a05-125"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="59a05-125"><dt>Shlobj.h</dt></span></span> </dl> |



 

 




