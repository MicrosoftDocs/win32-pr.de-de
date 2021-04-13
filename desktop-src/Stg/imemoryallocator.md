---
title: Imemoryzuordcator-Klasse
description: Wird von der Arbeitsspeicher Zuweisung für die stgconvertpropertytovariant-Funktion implementiert.
ms.assetid: a0735b62-5ed3-42df-a320-b58c742645a8
keywords:
- Strukturierte Speicherung der imemoryzuordcator-Klasse
- Strukturierte Speicherung der imemoryzuordcator-Klasse, beschrieben
topic_type:
- apiref
api_name:
- IMemoryAllocator
api_location:
- Ole32.lib
- Ole32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 421162fd0ee6228f1dbae03eeb52e5643b0e0b15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391965"
---
# <a name="imemoryallocator-class"></a><span data-ttu-id="b37ac-105">Imemoryzuordcator-Klasse</span><span class="sxs-lookup"><span data-stu-id="b37ac-105">IMemoryAllocator class</span></span>

<span data-ttu-id="b37ac-106">Die **imemoryzuordcator** -Klasse wird von der Speicherzuweisung für die [**stgconvertpropertytovariant**](/windows/desktop/api/propidl/nf-propidl-stgconvertpropertytovariant) -Funktion implementiert.</span><span class="sxs-lookup"><span data-stu-id="b37ac-106">The **IMemoryAllocator** class is implemented by the memory allocator for the [**StgConvertPropertyToVariant**](/windows/desktop/api/propidl/nf-propidl-stgconvertpropertytovariant) function.</span></span>

## <a name="methods"></a><span data-ttu-id="b37ac-107">Methoden</span><span class="sxs-lookup"><span data-stu-id="b37ac-107">Methods</span></span>



| <span data-ttu-id="b37ac-108">Name</span><span class="sxs-lookup"><span data-stu-id="b37ac-108">Name</span></span>                                                     | <span data-ttu-id="b37ac-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b37ac-109">Description</span></span>                                                                                                                                                                                                        |
|----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b37ac-110">**Jugend**</span><span class="sxs-lookup"><span data-stu-id="b37ac-110">**Allocate**</span></span>](imemoryallocator-allocate.md)<br/> | <span data-ttu-id="b37ac-111">Weist Speicher für die [**stgconvertpropertytovariant**](/windows/desktop/api/propidl/nf-propidl-stgconvertpropertytovariant) -Funktion zu, wenn die-Funktion einen **serializedpropertyvalue** -Datentyp in einen **PROPVARIANT** -Datentyp konvertiert.</span><span class="sxs-lookup"><span data-stu-id="b37ac-111">Allocates memory for the [**StgConvertPropertyToVariant**](/windows/desktop/api/propidl/nf-propidl-stgconvertpropertytovariant) function when the function converts a **SERIALIZEDPROPERTYVALUE** data type to a **PROPVARIANT** data type.</span></span><br/> |
| [<span data-ttu-id="b37ac-112">**Kostenlos**</span><span class="sxs-lookup"><span data-stu-id="b37ac-112">**Free**</span></span>](/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-initialize)<br/>        | <span data-ttu-id="b37ac-113">Gibt den von der Zuordnungs [**Methode belegten**](imemoryallocator-allocate.md) Arbeitsspeicher frei.</span><span class="sxs-lookup"><span data-stu-id="b37ac-113">Frees the memory allocated by the [**Allocate**](imemoryallocator-allocate.md) method.</span></span><br/>                                                                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="b37ac-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b37ac-114">Remarks</span></span>

<span data-ttu-id="b37ac-115">Diese Klasse wird nur von der [**stgconvertpropertydevariant**](/windows/desktop/api/propidl/nf-propidl-stgconvertpropertytovariant) -Funktion verwendet.</span><span class="sxs-lookup"><span data-stu-id="b37ac-115">This class is only used by the [**StgConvertPropertyToVariant**](/windows/desktop/api/propidl/nf-propidl-stgconvertpropertytovariant) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="b37ac-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b37ac-116">Requirements</span></span>



| <span data-ttu-id="b37ac-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b37ac-117">Requirement</span></span> | <span data-ttu-id="b37ac-118">Wert</span><span class="sxs-lookup"><span data-stu-id="b37ac-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b37ac-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b37ac-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b37ac-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b37ac-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="b37ac-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b37ac-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b37ac-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b37ac-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="b37ac-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b37ac-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="b37ac-124"><dt>Ole32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b37ac-124"><dt>Ole32.lib</dt></span></span> </dl> |



 

