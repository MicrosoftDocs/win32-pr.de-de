---
description: Ruft ein Objekt Handle für das angegebene Objekt ab, das dem angegebenen Prozess zugeordnet ist.
ms.assetid: c7b371c3-02c0-4137-ad9d-dd07a74fe2a5
title: Obfindlenker forobject-Funktion (ntosp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObFindHandleForObject
api_type:
- LibDef
api_location:
- Ntoskrnl.lib
- Ntoskrnl.dll
ms.openlocfilehash: 7ba87d05d4264f3bb160bae16053a338e38e2145
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860788"
---
# <a name="obfindhandleforobject-function"></a><span data-ttu-id="b8448-103">Obfindlenker forobject-Funktion</span><span class="sxs-lookup"><span data-stu-id="b8448-103">ObFindHandleForObject function</span></span>

<span data-ttu-id="b8448-104">\[Diese Funktion ist veraltet und kann in zukünftigen Versionen von Windows geändert werden oder nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="b8448-104">\[This function is obsolete and may be altered or unavailable in future versions of Windows.</span></span> <span data-ttu-id="b8448-105">Vermeiden Sie die Verwendung dieser Funktion.\]</span><span class="sxs-lookup"><span data-stu-id="b8448-105">Avoid using this function.\]</span></span>

<span data-ttu-id="b8448-106">Ruft ein Objekt Handle für das angegebene Objekt ab, das dem angegebenen Prozess zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="b8448-106">Retrieves an object handle for the specified object associated with the specified process.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8448-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b8448-107">Syntax</span></span>


```C++
BOOLEAN WINAPI ObFindHandleForObject(
  _In_     PEPROCESS Process,
  _In_     PVOID     Object,
  _In_opt_ PVOID     Reserved1,
  _In_opt_ PVOID     Reserved2,
  _Out_    PHANDLE   Handle
);
```



## <a name="parameters"></a><span data-ttu-id="b8448-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b8448-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8448-109">*Prozess* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b8448-109">*Process* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8448-110">Der Prozess.</span><span class="sxs-lookup"><span data-stu-id="b8448-110">The process.</span></span> <span data-ttu-id="b8448-111">Dieses Handle wird von der **iogetcurrentprocess** -oder der **psgetcurrentprocess** -Funktion zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b8448-111">This handle is returned by the **IoGetCurrentProcess** or **PsGetCurrentProcess** function.</span></span>

</dd> <dt>

<span data-ttu-id="b8448-112">*Objekt* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b8448-112">*Object* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8448-113">Ein Zeiger auf das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="b8448-113">A pointer to the object.</span></span>

</dd> <dt>

<span data-ttu-id="b8448-114">*"Reserved1"* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="b8448-114">*Reserved1* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b8448-115">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="b8448-115">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="b8448-116">*"Reserved2"* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="b8448-116">*Reserved2* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b8448-117">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="b8448-117">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="b8448-118">*Handle* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="b8448-118">*Handle* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b8448-119">Das Objekt handle.</span><span class="sxs-lookup"><span data-stu-id="b8448-119">The object handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8448-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b8448-120">Return value</span></span>

<span data-ttu-id="b8448-121">Die Funktion gibt **true** zurück, wenn eine Entsprechung gefunden wird, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="b8448-121">The function returns **TRUE** if a match is found and **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8448-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b8448-122">Remarks</span></span>

<span data-ttu-id="b8448-123">Diese Funktion ist in Ntoskrnl.exe verfügbar und kann nur aus dem Kernel Modus aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="b8448-123">This function is available in Ntoskrnl.exe and can be called only from kernel mode.</span></span> <span data-ttu-id="b8448-124">Die entsprechende Import Bibliothek ist über das Windows-Treiberkit (WDK) verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b8448-124">The corresponding import library is available through the Windows Driver Kit (WDK).</span></span>

## <a name="requirements"></a><span data-ttu-id="b8448-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b8448-125">Requirements</span></span>



| <span data-ttu-id="b8448-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b8448-126">Requirement</span></span> | <span data-ttu-id="b8448-127">Wert</span><span class="sxs-lookup"><span data-stu-id="b8448-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b8448-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b8448-128">Minimum supported client</span></span><br/> | <span data-ttu-id="b8448-129">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b8448-129">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="b8448-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b8448-130">Minimum supported server</span></span><br/> | <span data-ttu-id="b8448-131">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b8448-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b8448-132">Header</span><span class="sxs-lookup"><span data-stu-id="b8448-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8448-133"><dt>Nzu SP. h</dt></span><span class="sxs-lookup"><span data-stu-id="b8448-133"><dt>Ntosp.h</dt></span></span> </dl>      |
| <span data-ttu-id="b8448-134">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b8448-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="b8448-135"><dt>Nzu-nl. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b8448-135"><dt>Ntoskrnl.lib</dt></span></span> </dl> |



 

 




