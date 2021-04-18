---
description: Die deleteextractedfiles-Funktion löscht die Dateien, die von der Extract-Funktion extrahiert wurden.
ms.assetid: 253e6267-d4be-46d6-bad2-2eb20bbc7e33
title: Deleteextractedfiles-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeleteExtractedFiles
api_type:
- DllExport
api_location:
- Cabinet.dll
ms.openlocfilehash: 4ab032864e59d8e7379fe347d241874d9336e431
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358064"
---
# <a name="deleteextractedfiles-function"></a><span data-ttu-id="ed4c1-103">Deleteextractedfiles-Funktion</span><span class="sxs-lookup"><span data-stu-id="ed4c1-103">DeleteExtractedFiles function</span></span>

<span data-ttu-id="ed4c1-104">\[Diese Funktion wird nicht mehr unterstützt, sodass Ihr Verhalten nicht garantiert werden kann.\]</span><span class="sxs-lookup"><span data-stu-id="ed4c1-104">\[This function is no longer supported, so its behavior cannot be guaranteed.\]</span></span>

<span data-ttu-id="ed4c1-105">Die **deleteextractedfiles** -Funktion löscht die Dateien, die von der [**extract**](extract.md) -Funktion extrahiert wurden.</span><span class="sxs-lookup"><span data-stu-id="ed4c1-105">The **DeleteExtractedFiles** function deletes the files that were extracted by the [**Extract**](extract.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed4c1-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="ed4c1-106">Syntax</span></span>


```C++
VOID WINAPI DeleteExtractedFiles(
   PSESSION ps
);
```



## <a name="parameters"></a><span data-ttu-id="ed4c1-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="ed4c1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed4c1-108">*Psel*</span><span class="sxs-lookup"><span data-stu-id="ed4c1-108">*ps*</span></span> 
</dt> <dd>

<span data-ttu-id="ed4c1-109">Ein Zeiger auf eine [**Sitzungs**](session.md) Struktur, die Informationen über die aktuelle Sitzung enthält.</span><span class="sxs-lookup"><span data-stu-id="ed4c1-109">A pointer to a [**SESSION**](session.md) structure that contains information about the current session.</span></span>

<span data-ttu-id="ed4c1-110">Diese Funktion gibt den Arbeitsspeicher im **pfilelist** -Member dieser Struktur frei und legt **pfilelist** auf **null** fest.</span><span class="sxs-lookup"><span data-stu-id="ed4c1-110">This function frees the memory in the **pFileList** member of this structure and sets **pFileList** to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed4c1-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ed4c1-111">Return value</span></span>

<span data-ttu-id="ed4c1-112">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="ed4c1-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed4c1-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ed4c1-113">Remarks</span></span>

<span data-ttu-id="ed4c1-114">Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="ed4c1-114">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed4c1-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ed4c1-115">Requirements</span></span>



| <span data-ttu-id="ed4c1-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ed4c1-116">Requirement</span></span> | <span data-ttu-id="ed4c1-117">Wert</span><span class="sxs-lookup"><span data-stu-id="ed4c1-117">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ed4c1-118">DLL</span><span class="sxs-lookup"><span data-stu-id="ed4c1-118">DLL</span></span><br/> | <dl> <span data-ttu-id="ed4c1-119"><dt>Cabinet.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ed4c1-119"><dt>Cabinet.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed4c1-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ed4c1-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed4c1-121">**Extrahieren**</span><span class="sxs-lookup"><span data-stu-id="ed4c1-121">**Extract**</span></span>](extract.md)
</dt> <dt>

[<span data-ttu-id="ed4c1-122">**Sitzung**</span><span class="sxs-lookup"><span data-stu-id="ed4c1-122">**SESSION**</span></span>](session.md)
</dt> </dl>

 

 
