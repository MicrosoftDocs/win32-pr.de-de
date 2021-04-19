---
description: Verwendet das Delta und die Quelle (als Puffer bereitgestellt), um eine neue Kopie der Zieldaten zu erstellen. Die Ausgabedaten werden in einem von Msdelta zugewiesenen Puffer zurückgegeben.
title: ApplyDeltaB-Funktion
ms.topic: reference
ms.date: 12/03/2020
ms.keywords: ApplyDeltaB
req.header: msdelta.h
req.dll: msdelta.dll
topic_type:
- APIRef
- kbSyntax
api_name:
- ApplyDeltaB
api_type:
- DllExport
api_location:
- msdelta.dll
ms.openlocfilehash: 368788ba894064aa8ac3f8c9711f987a32f306af
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359723"
---
# <a name="applydeltab-function"></a><span data-ttu-id="d56c8-104">ApplyDeltaB-Funktion</span><span class="sxs-lookup"><span data-stu-id="d56c8-104">ApplyDeltaB function</span></span>

<span data-ttu-id="d56c8-105">Verwendet das Delta und die Quelle (als Puffer bereitgestellt), um eine neue Kopie der Zieldaten zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d56c8-105">Uses the delta and source (provided as buffers) to create a new copy of the target data.</span></span> <span data-ttu-id="d56c8-106">Die Ausgabedaten werden in einem von Msdelta zugewiesenen Puffer zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d56c8-106">The output data is returned in an MSDelta-allocated buffer.</span></span>

> [!NOTE]
> <span data-ttu-id="d56c8-107">Sie müssen [Delta Free](msdelta-deltafree.md) anrufen, um den Ausgabepuffer freizugeben, nachdem diese Funktion abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="d56c8-107">You must call [DeltaFree](msdelta-deltafree.md) to free the output buffer after this function has completed.</span></span>

> [!NOTE]
> <span data-ttu-id="d56c8-108">Wenn das angegebene Delta mithilfe von [PatchAPI](patchapi.md)erstellt wurde und das [DELTA_APPLY_FLAG_ALLOW_PA19](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags) -Flag festgelegt ist, ruft Msdelta PatchAPI auf, um das Delta anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="d56c8-108">If the specified delta was created using [PatchAPI](patchapi.md), and the [DELTA_APPLY_FLAG_ALLOW_PA19](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags) flag is set, MSDelta will call PatchAPI to apply the delta.</span></span>

## <a name="syntax"></a><span data-ttu-id="d56c8-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="d56c8-109">Syntax</span></span>

```cpp
BOOL  WINAPI  ApplyDeltaB(
    DELTA_FLAG_TYPE  ApplyFlags,
    DELTA_INPUT      Source,
    DELTA_INPUT      Delta,
    LPDELTA_OUTPUT   lpTarget
   );
```

## <a name="parameters"></a><span data-ttu-id="d56c8-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="d56c8-110">Parameters</span></span>

<span data-ttu-id="d56c8-111">*Applyflags*</span><span class="sxs-lookup"><span data-stu-id="d56c8-111">*ApplyFlags*</span></span>

<span data-ttu-id="d56c8-112">in Entweder [DELTA_FLAG_NONE](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags) oder [DELTA_APPLY_FLAG_ALLOW_PA19](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags).</span><span class="sxs-lookup"><span data-stu-id="d56c8-112">[in] Either [DELTA_FLAG_NONE](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags) or [DELTA_APPLY_FLAG_ALLOW_PA19](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags).</span></span>

<span data-ttu-id="d56c8-113">*Quelle*</span><span class="sxs-lookup"><span data-stu-id="d56c8-113">*Source*</span></span>

<span data-ttu-id="d56c8-114">in Eine [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) -Struktur mit einem Zeiger auf den Puffer, der die Quelldaten enthält.</span><span class="sxs-lookup"><span data-stu-id="d56c8-114">[in] A [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) structure containing a pointer to the buffer containing the source data.</span></span>

<span data-ttu-id="d56c8-115">*Delta*</span><span class="sxs-lookup"><span data-stu-id="d56c8-115">*Delta*</span></span>

<span data-ttu-id="d56c8-116">in Eine [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) -Struktur mit einem Zeiger auf den Puffer, der die Delta Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="d56c8-116">[in] A [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) structure containing a pointer to the buffer containing the delta data.</span></span>

<span data-ttu-id="d56c8-117">*lptarget*</span><span class="sxs-lookup"><span data-stu-id="d56c8-117">*lpTarget*</span></span>

<span data-ttu-id="d56c8-118">vorgenommen Ein Zeiger auf die [DELTA_OUTPUT](/previous-versions/bb417345(v=msdn.10)#delta-output-structure) Struktur, in der das Ziel geschrieben werden soll.</span><span class="sxs-lookup"><span data-stu-id="d56c8-118">[out] Pointer to the [DELTA_OUTPUT](/previous-versions/bb417345(v=msdn.10)#delta-output-structure) structure where the target is to be written.</span></span>

## <a name="return-value"></a><span data-ttu-id="d56c8-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d56c8-119">Return value</span></span>

<span data-ttu-id="d56c8-120">Diese Funktion gibt **true** zurück, wenn Sie erfolgreich ist. Andernfalls wird **false** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d56c8-120">This function returns **TRUE** if it succeeds; otherwise, it returns **FALSE**.</span></span> <span data-ttu-id="d56c8-121">Wenn die Funktion " **false**" zurückgibt, können Sie " [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) " aufrufen, um den entsprechenden Win32-Systemfehler Code zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="d56c8-121">When the function returns **FALSE**, you can call [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) to get the corresponding Win32 system error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="d56c8-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d56c8-122">Requirements</span></span>

| <span data-ttu-id="d56c8-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d56c8-123">Requirement</span></span> | <span data-ttu-id="d56c8-124">Wert</span><span class="sxs-lookup"><span data-stu-id="d56c8-124">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d56c8-125">Header</span><span class="sxs-lookup"><span data-stu-id="d56c8-125">Header</span></span> | <span data-ttu-id="d56c8-126">Msdelta. h</span><span class="sxs-lookup"><span data-stu-id="d56c8-126">msdelta.h</span></span> |
| <span data-ttu-id="d56c8-127">DLL</span><span class="sxs-lookup"><span data-stu-id="d56c8-127">DLL</span></span> | <span data-ttu-id="d56c8-128">msdelta.dll</span><span class="sxs-lookup"><span data-stu-id="d56c8-128">msdelta.dll</span></span> |
| <span data-ttu-id="d56c8-129">Unicode</span><span class="sxs-lookup"><span data-stu-id="d56c8-129">Unicode</span></span> | <span data-ttu-id="d56c8-130">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="d56c8-130">Not applicable</span></span> |

## <a name="see-also"></a><span data-ttu-id="d56c8-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d56c8-131">See also</span></span>

[<span data-ttu-id="d56c8-132">Msdelta</span><span class="sxs-lookup"><span data-stu-id="d56c8-132">MSDelta</span></span>](msdelta.md)

[<span data-ttu-id="d56c8-133">Delta frei</span><span class="sxs-lookup"><span data-stu-id="d56c8-133">DeltaFree</span></span>](msdelta-deltafree.md)
