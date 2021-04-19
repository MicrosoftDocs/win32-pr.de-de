---
description: Stellt dem System Informationen zu einem Dokument zur Verfügung, nachdem ein Druckvorgang abgeschlossen wurde.
title: DlpNotifyPostPrint-Funktion (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPostPrint
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: b1206aa4e358e0763c10a0d9b5028acae25f5683
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495661"
---
# <a name="dlpnotifypostprint-function"></a><span data-ttu-id="fe5c7-103">DlpNotifyPostPrint-Funktion</span><span class="sxs-lookup"><span data-stu-id="fe5c7-103">DlpNotifyPostPrint function</span></span>

<span data-ttu-id="fe5c7-104">Stellt dem System Informationen zu einem Dokument zur Verfügung, nachdem ein Druckvorgang abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="fe5c7-104">Provides the system with information about a document after a print operation has completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe5c7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fe5c7-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyPostPrint(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_PRINT_INFO PrintInfo, _In_ const PDLP_POSTOP_STATUS OpStatus);
```

## <a name="parameters"></a><span data-ttu-id="fe5c7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fe5c7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe5c7-107">*DocumentInfo* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="fe5c7-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe5c7-108">Ein Zeiger auf [](endpointdlp-dlp_document_info.md) eine PDLP_DOCUMENT_INFO-Struktur, die Informationen über das dokument enthält, das dem Druckvorgang zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="fe5c7-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document associated with the print operation.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="fe5c7-109">*PrintInfo* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="fe5c7-109">*PrintInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe5c7-110">Ein Zeiger auf eine [DLP_PRINT_INFO](endpointdlp-dlp_print_info.md) Struktur, die Informationen zum Druckvorgang enthält.</span><span class="sxs-lookup"><span data-stu-id="fe5c7-110">A pointer to a [DLP_PRINT_INFO](endpointdlp-dlp_print_info.md) structure containing information about the print operation.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="fe5c7-111">*OpStatus* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="fe5c7-111">*OpStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe5c7-112">Ein Zeiger auf [](enpointdlp-dlp_postop_status.md) eine DLP_POSTOP_STATUS-Struktur, die Statusinformationen zum Druckvorgang enthält.</span><span class="sxs-lookup"><span data-stu-id="fe5c7-112">A pointer to a [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) structure containing status information about the print operation.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="fe5c7-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fe5c7-113">Return value</span></span>

<span data-ttu-id="fe5c7-114">Gibt void zurück.</span><span class="sxs-lookup"><span data-stu-id="fe5c7-114">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe5c7-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fe5c7-115">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="fe5c7-116">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="fe5c7-116">Requirements</span></span>



| <span data-ttu-id="fe5c7-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fe5c7-117">Requirement</span></span>          |    <span data-ttu-id="fe5c7-118">Wert</span><span class="sxs-lookup"><span data-stu-id="fe5c7-118">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fe5c7-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fe5c7-119">Minimum supported client</span></span><br/> | <span data-ttu-id="fe5c7-120">Windows 10, Version 1809 (10.0; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="fe5c7-120">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="fe5c7-121">DLL</span><span class="sxs-lookup"><span data-stu-id="fe5c7-121">DLL</span></span><br/>                      | <span data-ttu-id="fe5c7-122">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="fe5c7-122">EndpointDlp.dll</span></span> |