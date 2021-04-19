---
description: Stellt dem System Informationen zu einem Dokument zur Verfügung, bevor ein Save as-Vorgang initiiert wird.
title: DlpNotifyPreSaveAsDocument-Funktion (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPreSaveAsDocument
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: 5226ed63227e2d9dd01155066e2e6e19f77e063f
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495573"
---
# <a name="dlpnotifypresaveasdocument-function"></a><span data-ttu-id="19c8d-103">DlpNotifyPreSaveAsDocument-Funktion</span><span class="sxs-lookup"><span data-stu-id="19c8d-103">DlpNotifyPreSaveAsDocument function</span></span>

<span data-ttu-id="19c8d-104">Stellt dem System Informationen zu einem Dokument zur Verfügung, bevor ein Save as-Vorgang initiiert wird.</span><span class="sxs-lookup"><span data-stu-id="19c8d-104">Provides the system with information about a document before a save as operation is initiated.</span></span>

## <a name="syntax"></a><span data-ttu-id="19c8d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="19c8d-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyPreSaveAsDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ LPCWSTR Destination);
```



## <a name="parameters"></a><span data-ttu-id="19c8d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="19c8d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19c8d-107">*DocumentInfo* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="19c8d-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19c8d-108">Ein Zeiger auf eine [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) Struktur, die Informationen über das zu speichernde Dokument enthält.</span><span class="sxs-lookup"><span data-stu-id="19c8d-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document to be saved.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="19c8d-109">*Ziel* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="19c8d-109">*Destination* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19c8d-110">Ein **LPCWSTR mit** dem Zielpfad des zu speichernden Dokuments.</span><span class="sxs-lookup"><span data-stu-id="19c8d-110">A **LPCWSTR** containing the destination path of the document to be saved.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="19c8d-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="19c8d-111">Return value</span></span>

<span data-ttu-id="19c8d-112">Gibt void zurück.</span><span class="sxs-lookup"><span data-stu-id="19c8d-112">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="19c8d-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="19c8d-113">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="19c8d-114">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="19c8d-114">Requirements</span></span>



| <span data-ttu-id="19c8d-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="19c8d-115">Requirement</span></span>          |    <span data-ttu-id="19c8d-116">Wert</span><span class="sxs-lookup"><span data-stu-id="19c8d-116">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="19c8d-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="19c8d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="19c8d-118">Windows 10, Version 1809 (10.0; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="19c8d-118">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="19c8d-119">DLL</span><span class="sxs-lookup"><span data-stu-id="19c8d-119">DLL</span></span><br/>                      | <span data-ttu-id="19c8d-120">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="19c8d-120">EndpointDlp.dll</span></span> |