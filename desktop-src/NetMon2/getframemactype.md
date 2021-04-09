---
description: Die getframemactype-Funktion gibt den Mac-Typ des Frames zurück.
ms.assetid: 8d3da770-1392-4638-a267-32c2dae289b0
title: Getframemactype-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameMacType
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: b85accc64a6e29424e3f65d070bafcf29bb3ec0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958717"
---
# <a name="getframemactype-function"></a><span data-ttu-id="7d01f-103">Getframemactype-Funktion</span><span class="sxs-lookup"><span data-stu-id="7d01f-103">GetFrameMacType function</span></span>

<span data-ttu-id="7d01f-104">Die **getframemactype** -Funktion gibt den Mac-Typ des Frames zurück.</span><span class="sxs-lookup"><span data-stu-id="7d01f-104">The **GetFrameMacType** function returns the MAC type of the frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d01f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7d01f-105">Syntax</span></span>


```C++
DWORD WINAPI GetFrameMacType(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a><span data-ttu-id="7d01f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7d01f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d01f-107">*hframe* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7d01f-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7d01f-108">Handle für den Frame.</span><span class="sxs-lookup"><span data-stu-id="7d01f-108">Handle to the frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d01f-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7d01f-109">Return value</span></span>

<span data-ttu-id="7d01f-110">Die-Funktion gibt den Mac-Typ des Frames zurück, der einen der folgenden Werte aufweisen kann.</span><span class="sxs-lookup"><span data-stu-id="7d01f-110">The function returns the MAC type of the frame, which can have one of the following values.</span></span>

-   <span data-ttu-id="7d01f-111">Unbekannter Mac- \_ Typ. \_</span><span class="sxs-lookup"><span data-stu-id="7d01f-111">MAC\_TYPE\_UNKNOWN</span></span>
-   <span data-ttu-id="7d01f-112">Mac- \_ Typ \_ Ethernet</span><span class="sxs-lookup"><span data-stu-id="7d01f-112">MAC\_TYPE\_ETHERNET</span></span>
-   <span data-ttu-id="7d01f-113">Mac- \_ Typ \_ TokenRing</span><span class="sxs-lookup"><span data-stu-id="7d01f-113">MAC\_TYPE\_TOKENRING</span></span>
-   <span data-ttu-id="7d01f-114">Mac- \_ Typ " \_ f"</span><span class="sxs-lookup"><span data-stu-id="7d01f-114">MAC\_TYPE\_FDDI</span></span>

## <a name="remarks"></a><span data-ttu-id="7d01f-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7d01f-115">Remarks</span></span>

<span data-ttu-id="7d01f-116">[*Experten*](e.md) und [*Parser*](p.md) können die **getframemactype** -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="7d01f-116">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetFrameMacType** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d01f-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7d01f-117">Requirements</span></span>



| <span data-ttu-id="7d01f-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7d01f-118">Requirement</span></span> | <span data-ttu-id="7d01f-119">Wert</span><span class="sxs-lookup"><span data-stu-id="7d01f-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7d01f-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7d01f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="7d01f-121">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7d01f-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="7d01f-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7d01f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="7d01f-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7d01f-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="7d01f-124">Header</span><span class="sxs-lookup"><span data-stu-id="7d01f-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="7d01f-125"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="7d01f-125"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="7d01f-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7d01f-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="7d01f-127"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7d01f-127"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="7d01f-128">DLL</span><span class="sxs-lookup"><span data-stu-id="7d01f-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7d01f-129"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7d01f-129"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




