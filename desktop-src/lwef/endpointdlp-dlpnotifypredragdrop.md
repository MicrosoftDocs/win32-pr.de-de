---
description: Stellt dem System Informationen zu einem Dokument zur Verfügung, bevor ein Drag &amp; Drop-Vorgang initiiert wird.
title: DlpNotifyPreDragDrop-Funktion (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPreDragDrop
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: d88a28c0dff4b13cf1c1848eeb8623c3acd1c024
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495638"
---
# <a name="dlpnotifypredragdrop-function"></a><span data-ttu-id="b26b6-103">DlpNotifyPreDragDrop-Funktion</span><span class="sxs-lookup"><span data-stu-id="b26b6-103">DlpNotifyPreDragDrop function</span></span>

<span data-ttu-id="b26b6-104">Stellt dem System Informationen zu einem Dokument zur Verfügung, bevor ein Drag &amp; Drop-Vorgang initiiert wird.</span><span class="sxs-lookup"><span data-stu-id="b26b6-104">Provides the system with information about a document before a drag drop operation is initiated.</span></span>

## <a name="syntax"></a><span data-ttu-id="b26b6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b26b6-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyPreDragDrop(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
```



## <a name="parameters"></a><span data-ttu-id="b26b6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b26b6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b26b6-107">*DocumentInfo* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="b26b6-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b26b6-108">Ein Zeiger auf [](endpointdlp-dlp_document_info.md) eine PDLP_DOCUMENT_INFO-Struktur, die Informationen über das Dokument enthält, das dem Drag &amp; Drop-Vorgang zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="b26b6-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document associated with the drag drop operation.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="b26b6-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b26b6-109">Return value</span></span>

<span data-ttu-id="b26b6-110">Gibt void zurück.</span><span class="sxs-lookup"><span data-stu-id="b26b6-110">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="b26b6-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b26b6-111">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="b26b6-112">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="b26b6-112">Requirements</span></span>



| <span data-ttu-id="b26b6-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b26b6-113">Requirement</span></span>          |    <span data-ttu-id="b26b6-114">Wert</span><span class="sxs-lookup"><span data-stu-id="b26b6-114">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b26b6-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b26b6-115">Minimum supported client</span></span><br/> | <span data-ttu-id="b26b6-116">Windows 10, Version 1809 (10.0; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="b26b6-116">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="b26b6-117">DLL</span><span class="sxs-lookup"><span data-stu-id="b26b6-117">DLL</span></span><br/>                      | <span data-ttu-id="b26b6-118">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="b26b6-118">EndpointDlp.dll</span></span> |