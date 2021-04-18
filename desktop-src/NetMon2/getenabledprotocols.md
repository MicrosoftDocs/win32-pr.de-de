---
description: Die getenabledprotokolls-Funktion gibt eine Tabelle aller Protokolle zurück, die als aktiviert markiert sind.
ms.assetid: 11feac64-c770-47b2-a740-fc372e97b8ed
title: Getenabledprotokolls-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetEnabledProtocols
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 284d6c87bf5a3b26d6c3f379a710966be21006d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344041"
---
# <a name="getenabledprotocols-function"></a><span data-ttu-id="95475-103">Getenabledprotokolls-Funktion</span><span class="sxs-lookup"><span data-stu-id="95475-103">GetEnabledProtocols function</span></span>

<span data-ttu-id="95475-104">Die **getenabledprotokolls** -Funktion gibt eine Tabelle aller Protokolle zurück, die als aktiviert markiert sind.</span><span class="sxs-lookup"><span data-stu-id="95475-104">The **GetEnabledProtocols** function returns a table of all protocols that are marked Enabled.</span></span>

## <a name="syntax"></a><span data-ttu-id="95475-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="95475-105">Syntax</span></span>


```C++
LPPROTOCOLTABLE WINAPI GetEnabledProtocols(
  _In_ HCAPTURE hCapture
);
```



## <a name="parameters"></a><span data-ttu-id="95475-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="95475-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95475-107">*hcapture* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="95475-107">*hCapture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95475-108">Handle für die Erfassung.</span><span class="sxs-lookup"><span data-stu-id="95475-108">Handle to the capture.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95475-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="95475-109">Return value</span></span>

<span data-ttu-id="95475-110">Wenn die Funktion erfolgreich ist, ist der Rückgabewert ein Zeiger auf eine [protocoltable](protocoltable.md) -Struktur, die alle aktivierten Protokolle in der Erfassung auflistet.</span><span class="sxs-lookup"><span data-stu-id="95475-110">If the function is successful, the return value is a pointer to a [PROTOCOLTABLE](protocoltable.md) structure that lists all the enabled protocols in the capture.</span></span>

<span data-ttu-id="95475-111">Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert **null**.</span><span class="sxs-lookup"><span data-stu-id="95475-111">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="95475-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="95475-112">Remarks</span></span>

<span data-ttu-id="95475-113">[*Experten*](e.md) und [*Parser*](p.md) können die **getenabledprotokolls** -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="95475-113">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetEnabledProtocols** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="95475-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="95475-114">Requirements</span></span>



| <span data-ttu-id="95475-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="95475-115">Requirement</span></span> | <span data-ttu-id="95475-116">Wert</span><span class="sxs-lookup"><span data-stu-id="95475-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="95475-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="95475-117">Minimum supported client</span></span><br/> | <span data-ttu-id="95475-118">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="95475-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="95475-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="95475-119">Minimum supported server</span></span><br/> | <span data-ttu-id="95475-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="95475-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="95475-121">Header</span><span class="sxs-lookup"><span data-stu-id="95475-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="95475-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="95475-122"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="95475-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="95475-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="95475-124"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="95475-124"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="95475-125">DLL</span><span class="sxs-lookup"><span data-stu-id="95475-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="95475-126"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="95475-126"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95475-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="95475-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95475-128">Protocoltable</span><span class="sxs-lookup"><span data-stu-id="95475-128">PROTOCOLTABLE</span></span>](protocoltable.md)
</dt> </dl>

 

 




