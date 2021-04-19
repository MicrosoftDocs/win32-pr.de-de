---
description: Stellt dem System Informationen zu einem Dokument zur Verfügung, bevor ein Druckvorgang initiiert wird.
title: DlpNotifyPrePrint-Funktion (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPrePrint
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: eef5e3a19a6b93a49ba8b600be77385a99d3153a
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495566"
---
# <a name="dlpnotifypreprint-function"></a><span data-ttu-id="03155-103">DlpNotifyPrePrint-Funktion</span><span class="sxs-lookup"><span data-stu-id="03155-103">DlpNotifyPrePrint function</span></span>

<span data-ttu-id="03155-104">Stellt dem System Informationen zu einem Dokument zur Verfügung, bevor ein Druckvorgang initiiert wird.</span><span class="sxs-lookup"><span data-stu-id="03155-104">Provides the system with information about a document before a print operation is initiated.</span></span>

## <a name="syntax"></a><span data-ttu-id="03155-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="03155-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyPrePrint(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_PRINT_INFO PrintInfo);
```



## <a name="parameters"></a><span data-ttu-id="03155-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="03155-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03155-107">*DocumentInfo* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="03155-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03155-108">Ein Zeiger auf [](endpointdlp-dlp_document_info.md) eine PDLP_DOCUMENT_INFO-Struktur, die Informationen zum zu druckenden Dokument enthält.</span><span class="sxs-lookup"><span data-stu-id="03155-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document to be printed.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="03155-109">*PrintInfo* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="03155-109">*PrintInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03155-110">Ein Zeiger auf eine [DLP_PRINT_INFO](endpointdlp-dlp_print_info.md) Struktur, die Informationen zum Druckvorgang enthält.</span><span class="sxs-lookup"><span data-stu-id="03155-110">A pointer to a [DLP_PRINT_INFO](endpointdlp-dlp_print_info.md) structure containing information about print operation.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="03155-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="03155-111">Return value</span></span>

<span data-ttu-id="03155-112">Gibt void zurück.</span><span class="sxs-lookup"><span data-stu-id="03155-112">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="03155-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="03155-113">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="03155-114">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="03155-114">Requirements</span></span>



| <span data-ttu-id="03155-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="03155-115">Requirement</span></span>          |    <span data-ttu-id="03155-116">Wert</span><span class="sxs-lookup"><span data-stu-id="03155-116">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="03155-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="03155-117">Minimum supported client</span></span><br/> | <span data-ttu-id="03155-118">Windows 10, Version 1809 (10.0; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="03155-118">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="03155-119">DLL</span><span class="sxs-lookup"><span data-stu-id="03155-119">DLL</span></span><br/>                      | <span data-ttu-id="03155-120">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="03155-120">EndpointDlp.dll</span></span> |