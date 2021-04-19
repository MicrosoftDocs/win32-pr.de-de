---
description: Gibt den angegebenen Speicherblock frei.
title: DeltaFree-Funktion
ms.topic: reference
ms.date: 12/03/2020
ms.keywords: DeltaFree
req.header: msdelta.h
req.dll: msdelta.dll
topic_type:
- APIRef
- kbSyntax
api_name:
- DeltaFree
api_type:
- DllExport
api_location:
- msdelta.dll
ms.openlocfilehash: 15885cfa3e879ed6a1e85b2f9553af92d436ca71
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370119"
---
# <a name="deltafree-function"></a><span data-ttu-id="6e183-103">DeltaFree-Funktion</span><span class="sxs-lookup"><span data-stu-id="6e183-103">DeltaFree function</span></span>

<span data-ttu-id="6e183-104">Gibt den angegebenen Speicherblock frei.</span><span class="sxs-lookup"><span data-stu-id="6e183-104">Frees the specified memory block.</span></span> <span data-ttu-id="6e183-105">Sie müssen diese Funktion nach erfolgreichen Aufrufen von " [anatedeltab](msdelta-createdeltab.md) " und " [applydeltab](msdelta-applydeltab.md) " aufrufen, um den von Msdelta zugewiesenen Speicherpuffer freizugeben.</span><span class="sxs-lookup"><span data-stu-id="6e183-105">You must call this function after successful calls to [CreateDeltaB](msdelta-createdeltab.md) and [ApplyDeltaB](msdelta-applydeltab.md) to free the MSDelta-allocated memory buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e183-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="6e183-106">Syntax</span></span>

```cpp
BOOL  WINAPI  DeltaFree(
    LPVOID  lpMemory
    );
```

## <a name="parameters"></a><span data-ttu-id="6e183-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="6e183-107">Parameters</span></span>

<span data-ttu-id="6e183-108">*lpmemory*</span><span class="sxs-lookup"><span data-stu-id="6e183-108">*lpMemory*</span></span>

<span data-ttu-id="6e183-109">in Der Speicherblock, der freigegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="6e183-109">[in] Memory block to be freed.</span></span>

## <a name="return-value"></a><span data-ttu-id="6e183-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6e183-110">Return value</span></span>

<span data-ttu-id="6e183-111">Diese Funktion gibt **true** zurück, wenn Sie erfolgreich ist. Andernfalls wird **false** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6e183-111">This function returns **TRUE** if it succeeds; otherwise, it returns **FALSE**.</span></span> <span data-ttu-id="6e183-112">Wenn die Funktion " **false**" zurückgibt, können Sie " [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) " aufrufen, um den entsprechenden Win32-Systemfehler Code zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="6e183-112">When the function returns **FALSE**, you can call [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) to get the corresponding Win32 system error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e183-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6e183-113">Requirements</span></span>

| <span data-ttu-id="6e183-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6e183-114">Requirement</span></span> | <span data-ttu-id="6e183-115">Wert</span><span class="sxs-lookup"><span data-stu-id="6e183-115">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6e183-116">Header</span><span class="sxs-lookup"><span data-stu-id="6e183-116">Header</span></span> | <span data-ttu-id="6e183-117">Msdelta. h</span><span class="sxs-lookup"><span data-stu-id="6e183-117">msdelta.h</span></span> |
| <span data-ttu-id="6e183-118">DLL</span><span class="sxs-lookup"><span data-stu-id="6e183-118">DLL</span></span> | <span data-ttu-id="6e183-119">msdelta.dll</span><span class="sxs-lookup"><span data-stu-id="6e183-119">msdelta.dll</span></span> |
| <span data-ttu-id="6e183-120">Unicode</span><span class="sxs-lookup"><span data-stu-id="6e183-120">Unicode</span></span> | <span data-ttu-id="6e183-121">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="6e183-121">Not applicable</span></span> |

## <a name="see-also"></a><span data-ttu-id="6e183-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6e183-122">See also</span></span>

[<span data-ttu-id="6e183-123">Msdelta</span><span class="sxs-lookup"><span data-stu-id="6e183-123">MSDelta</span></span>](msdelta.md)

[<span data-ttu-id="6e183-124">"Kreatedeltab"</span><span class="sxs-lookup"><span data-stu-id="6e183-124">CreateDeltaB</span></span>](msdelta-createdeltab.md)

[<span data-ttu-id="6e183-125">ApplyDelta Tab</span><span class="sxs-lookup"><span data-stu-id="6e183-125">ApplyDeltaB</span></span>](msdelta-applydeltab.md)
