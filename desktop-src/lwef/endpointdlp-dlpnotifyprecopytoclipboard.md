---
description: Stellt dem System Informationen zu einem Dokument zur Verfügung, bevor ein Kopiervorgang in die Zwischenablage initiiert wird.
title: DlpNotifyPreCopyToClipboard-Funktion (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPreCopyToClipboard
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: b8e835e58d19570b9459d91ad131bbc0f38f378a
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495645"
---
# <a name="dlpnotifyprecopytoclipboard-function"></a><span data-ttu-id="56c8b-103">DlpNotifyPreCopyToClipboard-Funktion</span><span class="sxs-lookup"><span data-stu-id="56c8b-103">DlpNotifyPreCopyToClipboard function</span></span>

<span data-ttu-id="56c8b-104">Stellt dem System Informationen zu einem Dokument zur Verfügung, bevor ein Kopiervorgang in die Zwischenablage initiiert wird.</span><span class="sxs-lookup"><span data-stu-id="56c8b-104">Provides the system with information about a document before a copy to clipboard operation is initiated.</span></span>

## <a name="syntax"></a><span data-ttu-id="56c8b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="56c8b-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyPreCopyToClipboard(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
```



## <a name="parameters"></a><span data-ttu-id="56c8b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="56c8b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56c8b-107">*DocumentInfo* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="56c8b-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="56c8b-108">Ein Zeiger auf [](endpointdlp-dlp_document_info.md) eine PDLP_DOCUMENT_INFO-Struktur, die Informationen über das Dokument enthält, aus dem Inhalt kopiert wird.</span><span class="sxs-lookup"><span data-stu-id="56c8b-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document from which content is being copied.</span></span>

</dd> </dl>




## <a name="return-value"></a><span data-ttu-id="56c8b-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="56c8b-109">Return value</span></span>

<span data-ttu-id="56c8b-110">Gibt void zurück.</span><span class="sxs-lookup"><span data-stu-id="56c8b-110">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="56c8b-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="56c8b-111">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="56c8b-112">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="56c8b-112">Requirements</span></span>



| <span data-ttu-id="56c8b-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="56c8b-113">Requirement</span></span>          |    <span data-ttu-id="56c8b-114">Wert</span><span class="sxs-lookup"><span data-stu-id="56c8b-114">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="56c8b-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="56c8b-115">Minimum supported client</span></span><br/> | <span data-ttu-id="56c8b-116">Windows 10, Version 1809 (10.0; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="56c8b-116">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="56c8b-117">DLL</span><span class="sxs-lookup"><span data-stu-id="56c8b-117">DLL</span></span><br/>                      | <span data-ttu-id="56c8b-118">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="56c8b-118">EndpointDlp.dll</span></span> |