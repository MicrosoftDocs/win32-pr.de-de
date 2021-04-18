---
description: Die findpropertyinstance-Funktion sucht die erste Instanz der Eigenschaft, die durch den hproperty-Parameter angegeben wird.
ms.assetid: e994503d-2f32-4fa2-bba9-ff66c9d558dc
title: Findpropertyinstance-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FindPropertyInstance
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 21f94a3e4a1eb9619b39cff534a778235980a278
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344662"
---
# <a name="findpropertyinstance-function"></a><span data-ttu-id="24d03-103">Findpropertyinstance-Funktion</span><span class="sxs-lookup"><span data-stu-id="24d03-103">FindPropertyInstance function</span></span>

<span data-ttu-id="24d03-104">Die **findpropertyinstance** -Funktion sucht die erste Instanz der Eigenschaft, die durch den *hproperty* -Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="24d03-104">The **FindPropertyInstance** function finds the first instance of the property specified by the *hProperty* parameter.</span></span>

## <a name="syntax"></a><span data-ttu-id="24d03-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="24d03-105">Syntax</span></span>


```C++
LPPROPERTYINST WINAPI FindPropertyInstance(
  _In_ HFRAME    hFrame,
  _In_ HPROPERTY hProperty
);
```



## <a name="parameters"></a><span data-ttu-id="24d03-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="24d03-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24d03-107">*hframe* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="24d03-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24d03-108">Handle für den Frame.</span><span class="sxs-lookup"><span data-stu-id="24d03-108">Handle to the frame.</span></span> <span data-ttu-id="24d03-109">Das Frame Handle kann durch einen Aufrufen der [GetFrame](getframe.md) -Funktion abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="24d03-109">The frame handle can be retrieved by a call to the [GetFrame](getframe.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="24d03-110">*hproperty* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="24d03-110">*hProperty* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24d03-111">Handle für die Eigenschaft, die Sie suchen möchten.</span><span class="sxs-lookup"><span data-stu-id="24d03-111">Handle to the property you want to find.</span></span> <span data-ttu-id="24d03-112">Das Eigenschafts Handle kann durch einen Aufrufen der [GetProperty](getproperty.md) -Funktion abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="24d03-112">The property handle can be retrieved by a call to the [GetProperty](getproperty.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24d03-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="24d03-113">Return value</span></span>

<span data-ttu-id="24d03-114">Wenn die Funktion erfolgreich ist (d. h., wenn die-Eigenschaft gefunden wird), ist der Rückgabewert ein Zeiger auf die erste Instanz der-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="24d03-114">If the function is successful (that is, if the property is found), the return value is a pointer to the first instance of the property.</span></span>

<span data-ttu-id="24d03-115">Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert **null**.</span><span class="sxs-lookup"><span data-stu-id="24d03-115">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="24d03-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="24d03-116">Remarks</span></span>

<span data-ttu-id="24d03-117">Rufen Sie zum Abrufen der nächsten Instanz der Eigenschaft [findpropertyinstancerestart](findpropertyinstancerestart.md)auf.</span><span class="sxs-lookup"><span data-stu-id="24d03-117">To retrieve the next instance of the property, call [FindPropertyInstanceRestart](findpropertyinstancerestart.md).</span></span>

<span data-ttu-id="24d03-118">[*Experten*](e.md) und [*Parser*](p.md)können die **findpropertyinstance** -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="24d03-118">[*Experts*](e.md) and [*parsers*](p.md)can call the **FindPropertyInstance** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="24d03-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="24d03-119">Requirements</span></span>



| <span data-ttu-id="24d03-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="24d03-120">Requirement</span></span> | <span data-ttu-id="24d03-121">Wert</span><span class="sxs-lookup"><span data-stu-id="24d03-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="24d03-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="24d03-122">Minimum supported client</span></span><br/> | <span data-ttu-id="24d03-123">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="24d03-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="24d03-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="24d03-124">Minimum supported server</span></span><br/> | <span data-ttu-id="24d03-125">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="24d03-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="24d03-126">Header</span><span class="sxs-lookup"><span data-stu-id="24d03-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="24d03-127"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="24d03-127"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="24d03-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="24d03-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="24d03-129"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="24d03-129"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="24d03-130">DLL</span><span class="sxs-lookup"><span data-stu-id="24d03-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="24d03-131"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="24d03-131"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24d03-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="24d03-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24d03-133">Findpropertyinstancerestart</span><span class="sxs-lookup"><span data-stu-id="24d03-133">FindPropertyInstanceRestart</span></span>](findpropertyinstancerestart.md)
</dt> </dl>

 

 




