---
description: Stellt dem System Informationen zu einem Dokument bereit, nachdem ein Druckvorgang gestartet wurde.
title: DlpNotifyPostStartPrint-Funktion (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPostOpenDocument
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: 7bc2505b44797edc836ed8ae89e5d9caf3f93f05
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495653"
---
# <a name="dlpnotifypoststartprint-function"></a><span data-ttu-id="a5e07-103">DlpNotifyPostStartPrint-Funktion</span><span class="sxs-lookup"><span data-stu-id="a5e07-103">DlpNotifyPostStartPrint function</span></span>

<span data-ttu-id="a5e07-104">Stellt dem System Informationen zu einem Dokument bereit, nachdem ein Druckvorgang gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="a5e07-104">Provides the system with information about a document after a print operation has started.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5e07-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a5e07-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyPostStartPrint(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_PRINT_INFO PrintInfo);
```

## <a name="parameters"></a><span data-ttu-id="a5e07-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a5e07-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5e07-107">*DocumentInfo* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="a5e07-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5e07-108">Ein Zeiger auf eine [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) Struktur, die Informationen über das Dokument enthält, das dem Druckvorgang zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="a5e07-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document associated with the print operation.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="a5e07-109">*PrintInfo* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="a5e07-109">*PrintInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5e07-110">Ein Zeiger auf eine [DLP_PRINT_INFO](endpointdlp-dlp_print_info.md) Struktur, die Informationen zum Druckvorgang enthält.</span><span class="sxs-lookup"><span data-stu-id="a5e07-110">A pointer to a [DLP_PRINT_INFO](endpointdlp-dlp_print_info.md) structure containing information about the print operation.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="a5e07-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a5e07-111">Return value</span></span>

<span data-ttu-id="a5e07-112">Gibt void zurück.</span><span class="sxs-lookup"><span data-stu-id="a5e07-112">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="a5e07-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a5e07-113">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="a5e07-114">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="a5e07-114">Requirements</span></span>



| <span data-ttu-id="a5e07-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a5e07-115">Requirement</span></span>          |    <span data-ttu-id="a5e07-116">Wert</span><span class="sxs-lookup"><span data-stu-id="a5e07-116">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a5e07-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a5e07-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a5e07-118">Windows 10, Version 1809 (10.0; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="a5e07-118">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="a5e07-119">DLL</span><span class="sxs-lookup"><span data-stu-id="a5e07-119">DLL</span></span><br/>                      | <span data-ttu-id="a5e07-120">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="a5e07-120">EndpointDlp.dll</span></span> |