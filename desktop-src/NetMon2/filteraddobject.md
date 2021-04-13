---
description: Die Funktion FilterAddObject fügt einem Anzeige Filter ein einzelnes Objekt hinzu.
ms.assetid: 796216f4-a407-4a8c-98b3-8c3761d91913
title: FilterAddObject-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FilterAddObject
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 7fc6c41a675bfe560c060e271e4f9f48f88cd58c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484331"
---
# <a name="filteraddobject-function"></a><span data-ttu-id="fd235-103">FilterAddObject-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd235-103">FilterAddObject function</span></span>

<span data-ttu-id="fd235-104">Die Funktion **FilterAddObject** fügt einem [*Anzeige Filter*](d.md)ein einzelnes Objekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="fd235-104">The **FilterAddObject** function adds a single object to a [*display filter*](d.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="fd235-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fd235-105">Syntax</span></span>


```C++
DWORD WINAPI FilterAddObject(
  _In_  HFILTER        hFilter,
  _Out_ LPFILTEROBJECT lpFilterObject
);
```



## <a name="parameters"></a><span data-ttu-id="fd235-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fd235-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd235-107">*hfilter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fd235-107">*hFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd235-108">Handle für den Anzeige Filter.</span><span class="sxs-lookup"><span data-stu-id="fd235-108">Handle to the display filter.</span></span>

</dd> <dt>

<span data-ttu-id="fd235-109">*lpfilterobject* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="fd235-109">*lpFilterObject* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fd235-110">Ein Zeiger auf eine [filterobject](filterobject.md) -Struktur, die das Objekt definiert, das dem Filter hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="fd235-110">Pointer to a [FILTEROBJECT](filterobject.md) structure that defines the object to be added to the filter.</span></span> <span data-ttu-id="fd235-111">Jedes Objekt kann ein Operator, ein Wert oder eine Eigenschaft sein.</span><span class="sxs-lookup"><span data-stu-id="fd235-111">Each object can be an operator, value, or property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd235-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fd235-112">Return value</span></span>

<span data-ttu-id="fd235-113">Wenn die Funktion erfolgreich ist, ist der Rückgabewert nmerr \_ Success.</span><span class="sxs-lookup"><span data-stu-id="fd235-113">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="fd235-114">Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="fd235-114">If the function is unsuccessful, the return value is an error code.</span></span>



| <span data-ttu-id="fd235-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="fd235-115">Return code</span></span>                                                                                              | <span data-ttu-id="fd235-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fd235-116">Description</span></span>                                                                  |
|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="fd235-117"><dt>**Ungültiger nmerr- \_ \_ Parameter**</dt></span><span class="sxs-lookup"><span data-stu-id="fd235-117"><dt>**NMERR\_INVALID\_PARAMETER**</dt></span></span> </dl> | <span data-ttu-id="fd235-118">Der *hfilter* -Parameter weist einen ungültigen Wert auf.</span><span class="sxs-lookup"><span data-stu-id="fd235-118">The *hFilter* parameter has an invalid value.</span></span><br/>                     |
| <dl> <span data-ttu-id="fd235-119"><dt>**nicht genügend Arbeits \_ \_ Speicher für nmerr \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fd235-119"><dt>**NMERR\_OUT\_OF\_MEMORY**</dt></span></span> </dl>    | <span data-ttu-id="fd235-120">Netzwerkmonitor verfügt nicht über genügend Arbeitsspeicher, um das Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="fd235-120">Network Monitor does not have enough memory to create the object.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="fd235-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fd235-121">Remarks</span></span>

<span data-ttu-id="fd235-122">[*Experten*](e.md) und [*Parser*](p.md) können die Funktion **FilterAddObject** aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="fd235-122">[*Experts*](e.md) and [*parsers*](p.md) can call the **FilterAddObject** function.</span></span>

<span data-ttu-id="fd235-123">Die **FilterAddObject** -Funktion wird jedes Mal aufgerufen, wenn dem Anzeige Filter ein Filter Objekt hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="fd235-123">The **FilterAddObject** function is called each time a filter object is added to the display filter.</span></span> <span data-ttu-id="fd235-124">Der Anzeige Filter ist ein postfix Stapel von Objekten, bei denen es sich um einen Operator, einen Wert oder eine Eigenschaft handeln kann.</span><span class="sxs-lookup"><span data-stu-id="fd235-124">The display filter is a postfix stack of objects that can be an operator, value, or property.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd235-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fd235-125">Requirements</span></span>



| <span data-ttu-id="fd235-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fd235-126">Requirement</span></span> | <span data-ttu-id="fd235-127">Wert</span><span class="sxs-lookup"><span data-stu-id="fd235-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="fd235-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fd235-128">Minimum supported client</span></span><br/> | <span data-ttu-id="fd235-129">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fd235-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="fd235-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fd235-130">Minimum supported server</span></span><br/> | <span data-ttu-id="fd235-131">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fd235-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="fd235-132">Header</span><span class="sxs-lookup"><span data-stu-id="fd235-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd235-133"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd235-133"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="fd235-134">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="fd235-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="fd235-135"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fd235-135"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="fd235-136">DLL</span><span class="sxs-lookup"><span data-stu-id="fd235-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fd235-137"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fd235-137"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd235-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fd235-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd235-139">Filter Object</span><span class="sxs-lookup"><span data-stu-id="fd235-139">FILTEROBJECT</span></span>](filterobject.md)
</dt> </dl>

 

 




