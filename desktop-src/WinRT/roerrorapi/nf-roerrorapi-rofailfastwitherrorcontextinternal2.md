---
title: RoFailFastWithErrorContextInternal2-Funktion
description: Löst im aktuellen Prozess eine nicht fort Setz Bare Ausnahme aus und ermöglicht es Ihnen außerdem, zusätzlichen Fehler Kontext einzuschließen, der noch nicht vom Betriebssystem erfasst wurde.
ms.localizationpriority: low
ms.topic: reference
ms.date: 03/13/2020
req.lib: RuntimeObject.lib
req.dll: ComBase.dll
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- ComBase.dll
api_name:
- RoFailFastWithErrorContextInternal2
targetos: Windows
ms.openlocfilehash: 84584c339851ecbf8df5d6dbda2aaa575ca6487b
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/08/2020
ms.locfileid: "106338301"
---
# <a name="rofailfastwitherrorcontextinternal2-function"></a><span data-ttu-id="72f26-103">RoFailFastWithErrorContextInternal2-Funktion</span><span class="sxs-lookup"><span data-stu-id="72f26-103">RoFailFastWithErrorContextInternal2 function</span></span>

<span data-ttu-id="72f26-104">Löst im aktuellen Prozess eine nicht fort Setz Bare Ausnahme aus und ermöglicht es Ihnen außerdem, zusätzlichen Fehler Kontext einzuschließen, der nicht bereits vom Betriebssystem erfasst wurde.</span><span class="sxs-lookup"><span data-stu-id="72f26-104">Raises a non-continuable exception in the current process, and also allows you to include additional error context not already captured by the operating system (OS).</span></span>

## <a name="syntax"></a><span data-ttu-id="72f26-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="72f26-105">Syntax</span></span>

```cpp
void WINAPI RoFailFastWithErrorContextInternal2(
  HRESULT hrError,
  ULONG cStowedExceptions,
  _In_reads_opt_(cStowedExceptions) PSTOWED_EXCEPTION_INFORMATION_V2 aStowedExceptionPointers[]
);
```

## <a name="parameters"></a><span data-ttu-id="72f26-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="72f26-106">Parameters</span></span>

`hrError`

<span data-ttu-id="72f26-107">Typ: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span><span class="sxs-lookup"><span data-stu-id="72f26-107">Type: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span></span>

<span data-ttu-id="72f26-108">Das **HRESULT** , das dem aktuellen Fehler zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="72f26-108">The **HRESULT** associated with the current error.</span></span> <span data-ttu-id="72f26-109">Die Ausnahme wird für jeden Wert von " *hrError*" ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="72f26-109">The exception is raised for any value of *hrError*.</span></span>

`cStowedExceptions`

<span data-ttu-id="72f26-110">Typ: **[ulong](../../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="72f26-110">Type: **[ULONG](../../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="72f26-111">Die Anzahl der Elemente im " *astowedexceptionpointer* "-Array.</span><span class="sxs-lookup"><span data-stu-id="72f26-111">The number of elements in the *aStowedExceptionPointers* array.</span></span>

`aStowedExceptionPointers`

<span data-ttu-id="72f26-112">Typ: **[PSTOWED_EXCEPTION_INFORMATION_V2](../../wer/stowed-exception-information-v2.md)\[\]**</span><span class="sxs-lookup"><span data-stu-id="72f26-112">Type: **[PSTOWED_EXCEPTION_INFORMATION_V2](../../wer/stowed-exception-information-v2.md)\[\]**</span></span>

<span data-ttu-id="72f26-113">Ein Array von Zeigern auf [**STOWED_EXCEPTION_INFORMATION_V2**](../../wer/stowed-exception-information-v2.md) Strukturen.</span><span class="sxs-lookup"><span data-stu-id="72f26-113">An array of pointers to [**STOWED_EXCEPTION_INFORMATION_V2**](../../wer/stowed-exception-information-v2.md) structures.</span></span> <span data-ttu-id="72f26-114">Jede Struktur enthält Informationen, in denen eine verstaute Ausnahme beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="72f26-114">Each structure contains info describing a stowed exception.</span></span> <span data-ttu-id="72f26-115">Die Informationen in diesen Strukturen werden dann an Windows-Fehlerberichterstattung (wer) zusammen mit den Informationen über die gestaut-Ausnahme gesendet, die von der Plattform aufgezeichnet wurden.</span><span class="sxs-lookup"><span data-stu-id="72f26-115">The info in these structures is then submitted to Windows Error Reporting (WER) along with the stowed exception information that was captured by the platform.</span></span>

## <a name="return-value"></a><span data-ttu-id="72f26-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="72f26-116">Return value</span></span>

<span data-ttu-id="72f26-117">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="72f26-117">This function doesn't return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="72f26-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="72f26-118">Remarks</span></span>

<span data-ttu-id="72f26-119">**RoFailFastWithErrorContextInternal2** ist nicht mit einer Import Bibliothek und einer Header Datei verknüpft.</span><span class="sxs-lookup"><span data-stu-id="72f26-119">**RoFailFastWithErrorContextInternal2** isn't associated with an import library nor a header file.</span></span> <span data-ttu-id="72f26-120">Sie können ihn zuerst mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryw) -Funktion (Laden `ComBase.dll` ) und dann durch Aufrufen der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen, um die Adresse von **RoFailFastWithErrorContextInternal2** abzurufen.</span><span class="sxs-lookup"><span data-stu-id="72f26-120">You can call it by first using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryw) function (to load `ComBase.dll`), and then by calling the [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) function to retrieve the address of **RoFailFastWithErrorContextInternal2**.</span></span>

<span data-ttu-id="72f26-121">Weitere Informationen finden Sie unter [rofailfastwitherrorcontext-Funktion](/windows/win32/api/roerrorapi/nf-roerrorapi-rofailfastwitherrorcontext).</span><span class="sxs-lookup"><span data-stu-id="72f26-121">For more info, see [RoFailFastWithErrorContext function](/windows/win32/api/roerrorapi/nf-roerrorapi-rofailfastwitherrorcontext).</span></span>

## <a name="requirements"></a><span data-ttu-id="72f26-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="72f26-122">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="72f26-123">**Zielplattform**</span><span class="sxs-lookup"><span data-stu-id="72f26-123">**Target Platform**</span></span> | <span data-ttu-id="72f26-124">Windows</span><span class="sxs-lookup"><span data-stu-id="72f26-124">Windows</span></span> |
| <span data-ttu-id="72f26-125">**Header**</span><span class="sxs-lookup"><span data-stu-id="72f26-125">**Header**</span></span> | <span data-ttu-id="72f26-126">–</span><span class="sxs-lookup"><span data-stu-id="72f26-126">N/A</span></span> |
| <span data-ttu-id="72f26-127">**Bibliothek**</span><span class="sxs-lookup"><span data-stu-id="72f26-127">**Library**</span></span> | <span data-ttu-id="72f26-128">–</span><span class="sxs-lookup"><span data-stu-id="72f26-128">N/A</span></span> |
| <span data-ttu-id="72f26-129">**DLL**</span><span class="sxs-lookup"><span data-stu-id="72f26-129">**DLL**</span></span> | <span data-ttu-id="72f26-130">ComBase.dll</span><span class="sxs-lookup"><span data-stu-id="72f26-130">ComBase.dll</span></span> |

## <a name="see-also"></a><span data-ttu-id="72f26-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="72f26-131">See also</span></span>

* [<span data-ttu-id="72f26-132">Rofailfastwitherrorcontext-Funktion</span><span class="sxs-lookup"><span data-stu-id="72f26-132">RoFailFastWithErrorContext function</span></span>](/windows/win32/api/roerrorapi/nf-roerrorapi-rofailfastwitherrorcontext)