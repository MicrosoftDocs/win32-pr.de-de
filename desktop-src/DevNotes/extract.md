---
description: Die Extract-Funktion extrahiert Dateien aus einer CAB-Datei.
ms.assetid: c6a79d81-7adf-4b8e-a1ef-fec868f7fdbf
title: Extract-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Extract
api_type:
- DllExport
api_location:
- Cabinet.dll
ms.openlocfilehash: 2e1096cdb7909f49fbcac7c32891210b25637c90
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359658"
---
# <a name="extract-function"></a><span data-ttu-id="a019f-103">Extract-Funktion</span><span class="sxs-lookup"><span data-stu-id="a019f-103">Extract function</span></span>

<span data-ttu-id="a019f-104">\[Diese Funktion wird nicht mehr unterstützt, sodass Ihr Verhalten nicht garantiert werden kann.\]</span><span class="sxs-lookup"><span data-stu-id="a019f-104">\[This function is no longer supported, so its behavior cannot be guaranteed.\]</span></span>

<span data-ttu-id="a019f-105">Die **extract** -Funktion extrahiert Dateien aus einer CAB-Datei.</span><span class="sxs-lookup"><span data-stu-id="a019f-105">The **Extract** function extracts files from a cabinet.</span></span>

## <a name="syntax"></a><span data-ttu-id="a019f-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="a019f-106">Syntax</span></span>


```C++
HRESULT Extract(
   PSESSION ps,
   LPCSTR   lpCabName
);
```



## <a name="parameters"></a><span data-ttu-id="a019f-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="a019f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a019f-108">*Psel*</span><span class="sxs-lookup"><span data-stu-id="a019f-108">*ps*</span></span> 
</dt> <dd>

<span data-ttu-id="a019f-109">Ein Zeiger auf eine [**Sitzungs**](session.md) Struktur, die Informationen über die aktuelle Sitzung enthält.</span><span class="sxs-lookup"><span data-stu-id="a019f-109">Pointer to a [**SESSION**](session.md) structure that contains information about the current session.</span></span>

</dd> <dt>

<span data-ttu-id="a019f-110">*lpcabname*</span><span class="sxs-lookup"><span data-stu-id="a019f-110">*lpCabName*</span></span> 
</dt> <dd>

<span data-ttu-id="a019f-111">Ein Zeiger auf den Namen der CAB-Datei, aus der Dateien extrahiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a019f-111">Pointer to the name of the cabinet from which files are to be extracted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a019f-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a019f-112">Return value</span></span>

<span data-ttu-id="a019f-113">Wenn die Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück; andernfalls wird ein Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a019f-113">If the function succeeds, it returns **S\_OK**; otherwise, it returns an error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a019f-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a019f-114">Remarks</span></span>

<span data-ttu-id="a019f-115">Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="a019f-115">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="a019f-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a019f-116">Requirements</span></span>



| <span data-ttu-id="a019f-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a019f-117">Requirement</span></span> | <span data-ttu-id="a019f-118">Wert</span><span class="sxs-lookup"><span data-stu-id="a019f-118">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a019f-119">DLL</span><span class="sxs-lookup"><span data-stu-id="a019f-119">DLL</span></span><br/> | <dl> <span data-ttu-id="a019f-120"><dt>Cabinet.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a019f-120"><dt>Cabinet.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a019f-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a019f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a019f-122">**Deleteextractedfiles**</span><span class="sxs-lookup"><span data-stu-id="a019f-122">**DeleteExtractedFiles**</span></span>](deleteextractedfiles.md)
</dt> <dt>

[<span data-ttu-id="a019f-123">**ERF**</span><span class="sxs-lookup"><span data-stu-id="a019f-123">**ERF**</span></span>](/windows/win32/api/fdi_fci_types/ns-fdi_fci_types-erf)
</dt> <dt>

[<span data-ttu-id="a019f-124">**Sitzung**</span><span class="sxs-lookup"><span data-stu-id="a019f-124">**SESSION**</span></span>](session.md)
</dt> </dl>

 

 
