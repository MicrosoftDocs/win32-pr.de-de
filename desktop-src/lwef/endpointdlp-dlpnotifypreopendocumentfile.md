---
description: Stellt dem System Informationen zu einer Dokumentdatei zur Verfügung, bevor ein Geöffnet-Vorgang initiiert wird.
title: DlpNotifyPreOpenDocumentFile-Funktion (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPreOpenDocumentFile
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: 12caf5230d8affce195a63da155ed6b6ca409b72
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495630"
---
# <a name="dlpnotifypreopendocumentfile-function"></a><span data-ttu-id="6433f-103">DlpNotifyPreOpenDocumentFile-Funktion</span><span class="sxs-lookup"><span data-stu-id="6433f-103">DlpNotifyPreOpenDocumentFile function</span></span>

<span data-ttu-id="6433f-104">Stellt dem System Informationen zu einer Dokumentdatei zur Verfügung, bevor ein Geöffnet-Vorgang initiiert wird.</span><span class="sxs-lookup"><span data-stu-id="6433f-104">Provides the system with information about a document file before an open operation is initiated.</span></span>

## <a name="syntax"></a><span data-ttu-id="6433f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6433f-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyPreOpenDocumentFile(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
```



## <a name="parameters"></a><span data-ttu-id="6433f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6433f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6433f-107">*DocumentInfo* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="6433f-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6433f-108">Ein Zeiger auf eine [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) Struktur, die Informationen über das zu öffnende Dokument enthält.</span><span class="sxs-lookup"><span data-stu-id="6433f-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document to be opened.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="6433f-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6433f-109">Return value</span></span>

<span data-ttu-id="6433f-110">Gibt void zurück.</span><span class="sxs-lookup"><span data-stu-id="6433f-110">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="6433f-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6433f-111">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="6433f-112">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="6433f-112">Requirements</span></span>



| <span data-ttu-id="6433f-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6433f-113">Requirement</span></span>          |    <span data-ttu-id="6433f-114">Wert</span><span class="sxs-lookup"><span data-stu-id="6433f-114">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6433f-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6433f-115">Minimum supported client</span></span><br/> | <span data-ttu-id="6433f-116">Windows 10, Version 1809 (10.0; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="6433f-116">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="6433f-117">DLL</span><span class="sxs-lookup"><span data-stu-id="6433f-117">DLL</span></span><br/>                      | <span data-ttu-id="6433f-118">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="6433f-118">EndpointDlp.dll</span></span> |