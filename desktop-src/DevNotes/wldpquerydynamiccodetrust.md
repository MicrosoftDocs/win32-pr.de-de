---
description: Ruft einen Wert ab, der bestimmt, ob der angegebene dynamische Code im Arbeitsspeicher oder auf dem Datenträger mit der Device Guard-Richtlinie vertrauenswürdig ist.
ms.assetid: 9C12894D-98AF-4408-A11A-865E4DA1DA68
title: Wldpquerydynamiccodetrust-Funktion (wldp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WldpQueryDynamicCodeTrust
api_type:
- DllExport
api_location:
- wldp.dll
ms.openlocfilehash: 1b9b3cc30f5a02ae86fd8a30043a9ab417ec1ac7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523467"
---
# <a name="wldpquerydynamiccodetrust-function"></a><span data-ttu-id="45a83-103">Wldpquerydynamiccodetrust-Funktion</span><span class="sxs-lookup"><span data-stu-id="45a83-103">WldpQueryDynamicCodeTrust function</span></span>

<span data-ttu-id="45a83-104">Ruft einen Wert ab, der bestimmt, ob der angegebene dynamische Code im Arbeitsspeicher oder auf dem Datenträger mit der Device Guard-Richtlinie vertrauenswürdig ist.</span><span class="sxs-lookup"><span data-stu-id="45a83-104">Retrieves a value that determines if the specified in-memory or on-disk .NET CRL dynamic code is trusted by Device Guard policy.</span></span>

## <a name="syntax"></a><span data-ttu-id="45a83-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="45a83-105">Syntax</span></span>


```C++
HRESULT WINAPI WldpQueryDynamicCodeTrust(
   _When_(baseImage != NULL, _In_opt_)
    _When_(baseImage == NULL, _In_)
    HANDLE                                                 fileHandle,
   _When_(fileHandle == NULL, _In_reads_bytes_opt_(imageSize))
    _When_(fileHandle != NULL, _In_reads_bytes_(imageSize))
    PVOID  baseImage,
   _In_ ULONG                                                                                                                         ImageSize
);
```



## <a name="parameters"></a><span data-ttu-id="45a83-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="45a83-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45a83-107">*file handle*</span><span class="sxs-lookup"><span data-stu-id="45a83-107">*fileHandle*</span></span> 
</dt> <dd>

<span data-ttu-id="45a83-108">Handle für die zu überprüfende dynamische Codedatei auf dem Datenträger.</span><span class="sxs-lookup"><span data-stu-id="45a83-108">Handle to the on-disk dynamic code file to check.</span></span> <span data-ttu-id="45a83-109">Wenn *File Handle* nicht **null** ist, sollte *baseImage* **null** sein.</span><span class="sxs-lookup"><span data-stu-id="45a83-109">If *fileHandle* is non-**NULL**, *baseImage* should be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="45a83-110">*baseImage*</span><span class="sxs-lookup"><span data-stu-id="45a83-110">*baseImage*</span></span> 
</dt> <dd>

<span data-ttu-id="45a83-111">Zeiger auf die zu Überprüfung der in-Memory-PE-Datei.</span><span class="sxs-lookup"><span data-stu-id="45a83-111">Pointer to the in-memory PE file to check.</span></span> <span data-ttu-id="45a83-112">Wenn *baseImage* nicht **null** ist, sollte *FILEHANDLE* **null** sein.</span><span class="sxs-lookup"><span data-stu-id="45a83-112">If *baseImage* is non-**NULL**, *FileHandle* should be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="45a83-113">*ImageSize*</span><span class="sxs-lookup"><span data-stu-id="45a83-113">*ImageSize*</span></span> 
</dt> <dd>

<span data-ttu-id="45a83-114">Wenn *baseImage* ungleich **null** ist, gibt die Puffergröße an, auf die *baseImage* zeigt.</span><span class="sxs-lookup"><span data-stu-id="45a83-114">When *baseImage* is non-**NULL**, indicates the buffer size that *baseImage* points to.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45a83-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="45a83-115">Return value</span></span>

<span data-ttu-id="45a83-116">Diese Methode gibt bei Erfolg **S \_ OK** zurück oder andernfalls einen Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="45a83-116">This method returns **S\_OK** if successful or a failure code otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="45a83-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="45a83-117">Requirements</span></span>



| <span data-ttu-id="45a83-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="45a83-118">Requirement</span></span> | <span data-ttu-id="45a83-119">Wert</span><span class="sxs-lookup"><span data-stu-id="45a83-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="45a83-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="45a83-120">Minimum supported client</span></span><br/> | <span data-ttu-id="45a83-121">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="45a83-121">Windows 10 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="45a83-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="45a83-122">Minimum supported server</span></span><br/> | <span data-ttu-id="45a83-123">Nur Windows Server 2016 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="45a83-123">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="45a83-124">Header</span><span class="sxs-lookup"><span data-stu-id="45a83-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="45a83-125"><dt>Wldp. h</dt></span><span class="sxs-lookup"><span data-stu-id="45a83-125"><dt>Wldp.h</dt></span></span> </dl>   |
| <span data-ttu-id="45a83-126">DLL</span><span class="sxs-lookup"><span data-stu-id="45a83-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="45a83-127"><dt>Wldp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="45a83-127"><dt>Wldp.dll</dt></span></span> </dl> |



 

 




