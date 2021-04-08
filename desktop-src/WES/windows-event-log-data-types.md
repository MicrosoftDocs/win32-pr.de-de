---
title: Windows-Ereignisprotokoll-Datentypen (winevt. h)
description: 'Das Windows-Ereignisprotokoll definiert die folgenden Datentypen:'
ms.assetid: 1aad25fe-7503-4ef8-a40a-63457bd9a007
keywords:
- EVT_HANDLE
- PEVT_HANDLE
- EVT_OBJECT_ARRAY_PROPERTY_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71a93794d8cc3a254fe182c439698324dccdfc20
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741385"
---
# <a name="windows-event-log-data-types"></a><span data-ttu-id="44ca2-106">Windows-Ereignisprotokoll Datentypen</span><span class="sxs-lookup"><span data-stu-id="44ca2-106">Windows Event Log Data Types</span></span>

<span data-ttu-id="44ca2-107">Das Windows-Ereignisprotokoll definiert die folgenden Datentypen:</span><span class="sxs-lookup"><span data-stu-id="44ca2-107">Windows Event Log defines the following data types:</span></span>


```C++
typedef HANDLE EVT_HANDLE;
typedef HANDLE* PEVT_HANDLE;
typedef HANDLE EVT_OBJECT_ARRAY_PROPERTY_HANDLE;
```



<dl> <dt>

<span data-ttu-id="44ca2-108">**EVT- \_ handle**</span><span class="sxs-lookup"><span data-stu-id="44ca2-108">**EVT\_HANDLE**</span></span>
</dt> <dd>

<span data-ttu-id="44ca2-109">Ein Handle für ein Windows-Ereignisprotokoll Objekt.</span><span class="sxs-lookup"><span data-stu-id="44ca2-109">A handle to a Windows Event Log object.</span></span>

</dd> <dt>

<span data-ttu-id="44ca2-110">**Peer- \_ handle**</span><span class="sxs-lookup"><span data-stu-id="44ca2-110">**PEVT\_HANDLE**</span></span>
</dt> <dd>

<span data-ttu-id="44ca2-111">Ein Zeiger auf das Handle eines Windows-Ereignisprotokoll Objekts.</span><span class="sxs-lookup"><span data-stu-id="44ca2-111">A pointer to the handle of a Windows Event Log object.</span></span>

</dd> <dt>

<span data-ttu-id="44ca2-112">**EVT- \_ Objekt \_ array- \_ Eigenschaften \_ handle**</span><span class="sxs-lookup"><span data-stu-id="44ca2-112">**EVT\_OBJECT\_ARRAY\_PROPERTY\_HANDLE**</span></span>
</dt> <dd>

<span data-ttu-id="44ca2-113">Ein Handle für ein Array von Windows-Ereignisprotokoll Objekten.</span><span class="sxs-lookup"><span data-stu-id="44ca2-113">A handle to an array of Windows Event Log objects.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="44ca2-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="44ca2-114">Requirements</span></span>



| <span data-ttu-id="44ca2-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="44ca2-115">Requirement</span></span> | <span data-ttu-id="44ca2-116">Wert</span><span class="sxs-lookup"><span data-stu-id="44ca2-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="44ca2-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="44ca2-117">Minimum supported client</span></span><br/> | <span data-ttu-id="44ca2-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="44ca2-118">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="44ca2-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="44ca2-119">Minimum supported server</span></span><br/> | <span data-ttu-id="44ca2-120">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="44ca2-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="44ca2-121">Header</span><span class="sxs-lookup"><span data-stu-id="44ca2-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="44ca2-122"><dt>Winevt. h</dt></span><span class="sxs-lookup"><span data-stu-id="44ca2-122"><dt>WinEvt.h</dt></span></span> </dl> |



 

 





