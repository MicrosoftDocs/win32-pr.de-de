---
description: Sucht die nächste Instanz der Eigenschaft, die durch den hproperty-Parameter angegeben wird.
ms.assetid: f77cb92b-5936-4349-bf66-643c16e9e0df
title: Findpropertyinstancerestart-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FindPropertyInstanceRestart
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: d1e731bb00b28bb62862dd18fbd6031fa973fe38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346489"
---
# <a name="findpropertyinstancerestart-function"></a><span data-ttu-id="7faac-103">Findpropertyinstancerestart-Funktion</span><span class="sxs-lookup"><span data-stu-id="7faac-103">FindPropertyInstanceRestart function</span></span>

<span data-ttu-id="7faac-104">Die **findpropertyinstancerestart** -Funktion sucht die nächste Instanz der Eigenschaft, die durch den *hproperty* -Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="7faac-104">The **FindPropertyInstanceRestart** function finds the next instance of the property specified by the *hProperty* parameter.</span></span>

## <a name="syntax"></a><span data-ttu-id="7faac-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7faac-105">Syntax</span></span>


```C++
LPPROPERTYINST WINAPI FindPropertyInstanceRestart(
  _In_ HFRAME         hFrame,
  _In_ HPROPERTY      hProperty,
  _In_ LPPROPERTYINST *lpRestartKey,
  _In_ BOOL           DirForward
);
```



## <a name="parameters"></a><span data-ttu-id="7faac-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7faac-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7faac-107">*hframe* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7faac-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7faac-108">Ein Handle für den Frame.</span><span class="sxs-lookup"><span data-stu-id="7faac-108">A handle to the frame.</span></span> <span data-ttu-id="7faac-109">Das Frame Handle kann durch einen Aufrufen der [GetFrame](getframe.md) -Funktion abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="7faac-109">The frame handle can be retrieved by a call to the [GetFrame](getframe.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="7faac-110">*hproperty* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7faac-110">*hProperty* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7faac-111">Ein Handle für die zu suchende Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="7faac-111">A handle to the property to find.</span></span> <span data-ttu-id="7faac-112">Das Eigenschafts Handle kann durch einen Aufrufen der [GetProperty](getproperty.md) -Funktion abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="7faac-112">The property handle can be retrieved by a call to the [GetProperty](getproperty.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="7faac-113">*lprestartkey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7faac-113">*lpRestartKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7faac-114">Ein Zeiger auf die Eigenschaften Instanz, die als Ausgangspunkt für die Suche verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7faac-114">A pointer to the property instance used as the starting point of the search.</span></span> <span data-ttu-id="7faac-115">Wenn der *lprestartkey* -Parameter auf **null** festgelegt ist, beginnt die Suche am Anfang des Frames oder am Ende des Frames, abhängig vom Wert des *dirforward* -Parameters.</span><span class="sxs-lookup"><span data-stu-id="7faac-115">If the *lpRestartKey* parameter is set to **NULL**, the search begins at beginning of the frame, or the end of the frame, depending on the value of the *DirForward* parameter.</span></span>

<span data-ttu-id="7faac-116">Wenn *lprestartkey* auf **null** zeigt, beginnt die Suche am Anfang des Frames, wenn *dirforward* den Wert **true** hat, oder am Ende des Frames, wenn der-Parameter **false** ist.</span><span class="sxs-lookup"><span data-stu-id="7faac-116">If *lpRestartKey* points to **NULL**, the search begins at the beginning of the frame if *DirForward* is **TRUE** or the at end of the frame if the parameter is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="7faac-117">*Dirforward* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7faac-117">*DirForward* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7faac-118">Ein Indikator der Suchrichtung.</span><span class="sxs-lookup"><span data-stu-id="7faac-118">An indicator of the search direction.</span></span> <span data-ttu-id="7faac-119">Wenn der Wert **true** ist, wechselt die Suche von der aktuellen Position bis zum Ende des Frames.</span><span class="sxs-lookup"><span data-stu-id="7faac-119">If the value is **TRUE**, the search moves from the current location to the end of the frame.</span></span> <span data-ttu-id="7faac-120">Wenn der Wert **false** ist, wird die Suche von der aktuellen Position bis zum Anfang des Frames verschoben.</span><span class="sxs-lookup"><span data-stu-id="7faac-120">If the value is **FALSE**, the search moves from the current location to the beginning of the frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7faac-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7faac-121">Return value</span></span>

<span data-ttu-id="7faac-122">Wenn die Funktion erfolgreich ist, ist der Rückgabewert das nächste gültige **lppropertyinst**.</span><span class="sxs-lookup"><span data-stu-id="7faac-122">If the function is successful, the return value is the next valid **LPPROPERTYINST**.</span></span>

<span data-ttu-id="7faac-123">Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert **null**.</span><span class="sxs-lookup"><span data-stu-id="7faac-123">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="7faac-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7faac-124">Remarks</span></span>

<span data-ttu-id="7faac-125">[*Experten*](e.md) und [*Parser*](p.md) können die **findpropertyinstancerestart** -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="7faac-125">[*Experts*](e.md) and [*parsers*](p.md) can call the **FindPropertyInstanceRestart** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="7faac-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7faac-126">Requirements</span></span>



| <span data-ttu-id="7faac-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7faac-127">Requirement</span></span> | <span data-ttu-id="7faac-128">Wert</span><span class="sxs-lookup"><span data-stu-id="7faac-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7faac-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7faac-129">Minimum supported client</span></span><br/> | <span data-ttu-id="7faac-130">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7faac-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="7faac-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7faac-131">Minimum supported server</span></span><br/> | <span data-ttu-id="7faac-132">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7faac-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="7faac-133">Header</span><span class="sxs-lookup"><span data-stu-id="7faac-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="7faac-134"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="7faac-134"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="7faac-135">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7faac-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="7faac-136"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7faac-136"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="7faac-137">DLL</span><span class="sxs-lookup"><span data-stu-id="7faac-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7faac-138"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7faac-138"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7faac-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7faac-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7faac-140">GetFrame</span><span class="sxs-lookup"><span data-stu-id="7faac-140">GetFrame</span></span>](getframe.md)
</dt> <dt>

[<span data-ttu-id="7faac-141">GetProperty</span><span class="sxs-lookup"><span data-stu-id="7faac-141">GetProperty</span></span>](getproperty.md)
</dt> </dl>

 

 




