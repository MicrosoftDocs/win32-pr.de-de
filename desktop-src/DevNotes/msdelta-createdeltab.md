---
description: Erstellt ein Delta zwischen Quelle und Ziel (bereitgestellt als Puffer) und gibt das Ausgabe Delta als in Msdelta zugewiesener Puffer zurück.
title: CreateDeltaB-Funktion
ms.topic: reference
ms.date: 12/03/2020
ms.keywords: CreateDeltaB
req.header: msdelta.h
req.dll: msdelta.dll
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateDeltaB
api_type:
- DllExport
api_location:
- msdelta.dll
ms.openlocfilehash: a2142f26499514c24967e5334d782c2dee559cd9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357526"
---
# <a name="createdeltab-function"></a><span data-ttu-id="46461-103">CreateDeltaB-Funktion</span><span class="sxs-lookup"><span data-stu-id="46461-103">CreateDeltaB function</span></span>

<span data-ttu-id="46461-104">Erstellt ein Delta zwischen Quelle und Ziel (bereitgestellt als Puffer) und gibt das Ausgabe Delta als in Msdelta zugewiesener Puffer zurück.</span><span class="sxs-lookup"><span data-stu-id="46461-104">Creates a delta between the source and target (provided as buffers) and returns the output delta as an MSDelta-allocated buffer.</span></span>

> [!NOTE]
> <span data-ttu-id="46461-105">Sie müssen [Delta Free](msdelta-deltafree.md) anrufen, um den Ausgabepuffer freizugeben, nachdem diese Funktion abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="46461-105">You must call [DeltaFree](msdelta-deltafree.md) to free the output buffer after this function has completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="46461-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="46461-106">Syntax</span></span>

```cpp
BOOL  WINAPI  CreateDeltaB(
           DELTA_FILE_TYPE  FileTypeSet,
           DELTA_FLAG_TYPE  SetFlags,
           DELTA_FLAG_TYPE  ResetFlags,
           DELTA_INPUT      Source,
           DELTA_INPUT      Target,
           DELTA_INPUT      SourceOptions,
           DELTA_INPUT      TargetOptions,
           DELTA_INPUT      GlobalOptions,
    const  FILETIME        *lpTargetFileTime,
           ALG_ID           HashAlgId,
           LPDELTA_OUTPUT   lpDelta
    );
```

## <a name="parameters"></a><span data-ttu-id="46461-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="46461-107">Parameters</span></span>

<span data-ttu-id="46461-108">*Filetypeset*</span><span class="sxs-lookup"><span data-stu-id="46461-108">*FileTypeSet*</span></span>

<span data-ttu-id="46461-109">in Der [DELTA_FILE_TYPE](/previous-versions/bb417345(v=msdn.10)#file-type-sets) -Wert, der den Dateityp angibt, der für den Erstellungs Prozess verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="46461-109">[in] The [DELTA_FILE_TYPE](/previous-versions/bb417345(v=msdn.10)#file-type-sets) value that indicates the file type set to be used for the create process.</span></span>

<span data-ttu-id="46461-110">*SetFlags*</span><span class="sxs-lookup"><span data-stu-id="46461-110">*SetFlags*</span></span>

<span data-ttu-id="46461-111">in Mindestens ein [DELTA_FLAG_TYPE](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags) -Wert, der die Flags angibt, die während des Erstellungs Prozesses verwendet werden sollen, zusätzlich zu den Standardflags.</span><span class="sxs-lookup"><span data-stu-id="46461-111">[in] One or more [DELTA_FLAG_TYPE](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags) values that specify the flags to be used during the create process, in addition to the default flags.</span></span>

<span data-ttu-id="46461-112">*Resetflags*</span><span class="sxs-lookup"><span data-stu-id="46461-112">*ResetFlags*</span></span>

<span data-ttu-id="46461-113">in Mindestens ein [DELTA_FLAG_TYPE](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags) -Wert, der die Standardflags angibt, die während des Erstellungs Vorgangs zurückgesetzt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="46461-113">[in] One or more [DELTA_FLAG_TYPE](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags) values that specify the default flags to be reset during the create process.</span></span>

<span data-ttu-id="46461-114">*Quelle*</span><span class="sxs-lookup"><span data-stu-id="46461-114">*Source*</span></span>

<span data-ttu-id="46461-115">in Eine [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) -Struktur mit einem Zeiger auf den Puffer, der die Quelldaten enthält.</span><span class="sxs-lookup"><span data-stu-id="46461-115">[in] A [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) structure containing a pointer to the buffer containing the source data.</span></span>

<span data-ttu-id="46461-116">*Target*</span><span class="sxs-lookup"><span data-stu-id="46461-116">*Target*</span></span>

<span data-ttu-id="46461-117">in Eine [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) -Struktur mit einem Zeiger auf den Puffer, der die Zieldaten enthält.</span><span class="sxs-lookup"><span data-stu-id="46461-117">[in] A [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) structure containing a pointer to the buffer containing the target data.</span></span>

<span data-ttu-id="46461-118">*Sourceoptions*</span><span class="sxs-lookup"><span data-stu-id="46461-118">*SourceOptions*</span></span>

<span data-ttu-id="46461-119">[in]: Reserviert</span><span class="sxs-lookup"><span data-stu-id="46461-119">[in] Reserved.</span></span> <span data-ttu-id="46461-120">Übergeben Sie eine [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) -Struktur, bei der *editable* auf **false** festgelegt ist, *lpstart* auf **null** und *usize* auf 0 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="46461-120">Pass a [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) structure with *Editable* set to **FALSE**, *lpStart* set to **NULL** and *uSize* set to 0.</span></span>

<span data-ttu-id="46461-121">*Targetoptions*</span><span class="sxs-lookup"><span data-stu-id="46461-121">*TargetOptions*</span></span>

<span data-ttu-id="46461-122">[in]: Reserviert</span><span class="sxs-lookup"><span data-stu-id="46461-122">[in] Reserved.</span></span> <span data-ttu-id="46461-123">Übergeben Sie eine [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) -Struktur, bei der *editable* auf **false** festgelegt ist, *lpstart* auf **null** und *usize* auf 0 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="46461-123">Pass a [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) structure with *Editable* set to **FALSE**, *lpStart* set to **NULL** and *uSize* set to 0.</span></span>

<span data-ttu-id="46461-124">*GlobalOptions*</span><span class="sxs-lookup"><span data-stu-id="46461-124">*GlobalOptions*</span></span>

<span data-ttu-id="46461-125">[in]: Reserviert</span><span class="sxs-lookup"><span data-stu-id="46461-125">[in] Reserved.</span></span> <span data-ttu-id="46461-126">Übergeben Sie eine [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) -Struktur, wobei *lpstart* auf **null** und *usize* auf 0 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="46461-126">Pass a [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) structure with *lpStart* set to **NULL** and *uSize* set to 0.</span></span>

<span data-ttu-id="46461-127">*lptargetfiletime*</span><span class="sxs-lookup"><span data-stu-id="46461-127">*lpTargetFileTime*</span></span>

<span data-ttu-id="46461-128">in Der Zeitstempel, der für die Zieldatei festgelegt ist, nachdem Delta angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="46461-128">[in] The time stamp set on the target file after delta apply.</span></span> <span data-ttu-id="46461-129">Wenn der Wert **null** ist, wird der Ziel Zeitstempel die aktuelle Zeit während des Erstellungs Prozesses sein.</span><span class="sxs-lookup"><span data-stu-id="46461-129">If **NULL**, the target timestamp will be the current time during the create process.</span></span>

<span data-ttu-id="46461-130">*HashAlgId*</span><span class="sxs-lookup"><span data-stu-id="46461-130">*HashAlgId*</span></span>

<span data-ttu-id="46461-131">in ALG_ID des Algorithmus, der zum Generieren der Ziel Signatur verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="46461-131">[in] ALG_ID of the algorithm to be used to generate the target signature.</span></span> <span data-ttu-id="46461-132">Einige besondere Werte sind:</span><span class="sxs-lookup"><span data-stu-id="46461-132">Some special values are:</span></span>

- <span data-ttu-id="46461-133">0 = keine Signatur</span><span class="sxs-lookup"><span data-stu-id="46461-133">0 = No signature</span></span>
- <span data-ttu-id="46461-134">32 = 32-Bit CRC in msdelta.dll definiert</span><span class="sxs-lookup"><span data-stu-id="46461-134">32 = 32-bit CRC defined in msdelta.dll</span></span>

<span data-ttu-id="46461-135">*lpdelta*</span><span class="sxs-lookup"><span data-stu-id="46461-135">*lpDelta*</span></span>

<span data-ttu-id="46461-136">vorgenommen Ein Zeiger auf die [DELTA_OUTPUT](/previous-versions/bb417345(v=msdn.10)#delta-output-structure) Struktur, in die das Delta geschrieben werden soll.</span><span class="sxs-lookup"><span data-stu-id="46461-136">[out] Pointer to the [DELTA_OUTPUT](/previous-versions/bb417345(v=msdn.10)#delta-output-structure) structure where the delta is to be written.</span></span>

## <a name="return-value"></a><span data-ttu-id="46461-137">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="46461-137">Return value</span></span>

<span data-ttu-id="46461-138">Diese Funktion gibt **true** zurück, wenn Sie erfolgreich ist. Andernfalls wird **false** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="46461-138">This function returns **TRUE** if it succeeds; otherwise, it returns **FALSE**.</span></span> <span data-ttu-id="46461-139">Wenn die Funktion " **false**" zurückgibt, können Sie " [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) " aufrufen, um den entsprechenden Win32-Systemfehler Code zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="46461-139">When the function returns **FALSE**, you can call [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) to get the corresponding Win32 system error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="46461-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="46461-140">Requirements</span></span>

| <span data-ttu-id="46461-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="46461-141">Requirement</span></span> | <span data-ttu-id="46461-142">Wert</span><span class="sxs-lookup"><span data-stu-id="46461-142">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="46461-143">Header</span><span class="sxs-lookup"><span data-stu-id="46461-143">Header</span></span> | <span data-ttu-id="46461-144">Msdelta. h</span><span class="sxs-lookup"><span data-stu-id="46461-144">msdelta.h</span></span> |
| <span data-ttu-id="46461-145">DLL</span><span class="sxs-lookup"><span data-stu-id="46461-145">DLL</span></span> | <span data-ttu-id="46461-146">msdelta.dll</span><span class="sxs-lookup"><span data-stu-id="46461-146">msdelta.dll</span></span> |
| <span data-ttu-id="46461-147">Unicode</span><span class="sxs-lookup"><span data-stu-id="46461-147">Unicode</span></span> | <span data-ttu-id="46461-148">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="46461-148">Not applicable</span></span> |

## <a name="see-also"></a><span data-ttu-id="46461-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="46461-149">See also</span></span>

[<span data-ttu-id="46461-150">Msdelta</span><span class="sxs-lookup"><span data-stu-id="46461-150">MSDelta</span></span>](msdelta.md)

[<span data-ttu-id="46461-151">Delta frei</span><span class="sxs-lookup"><span data-stu-id="46461-151">DeltaFree</span></span>](msdelta-deltafree.md)
