---
description: Stellt dem System Informationen zu einem Dokument zur Verfügung, wenn ein Abbruchziel eingegeben wird.
title: DlpNotifyEnterDropTarget-Funktion (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyEnterDropTarget
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: ec1eee1cee7bbcc38ce3094e3e2f8b650cf3b2a9
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495712"
---
# <a name="dlpnotifyenterdroptarget-function"></a><span data-ttu-id="60edc-103">DlpNotifyEnterDropTarget-Funktion</span><span class="sxs-lookup"><span data-stu-id="60edc-103">DlpNotifyEnterDropTarget function</span></span>

<span data-ttu-id="60edc-104">Stellt dem System Informationen zu einem Dokument zur Verfügung, wenn ein Abbruchziel eingegeben wird.</span><span class="sxs-lookup"><span data-stu-id="60edc-104">Provides the system with information about a document when a drop target is entered.</span></span>

## <a name="syntax"></a><span data-ttu-id="60edc-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="60edc-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyEnterDropTarget(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
```



## <a name="parameters"></a><span data-ttu-id="60edc-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="60edc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60edc-107">*DocumentInfo* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="60edc-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60edc-108">Ein Zeiger auf [](endpointdlp-dlp_document_info.md) eine PDLP_DOCUMENT_INFO-Struktur, die Informationen über das Dokument enthält, das dem Abbruchvorgang zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="60edc-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document associated with the drop operation.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="60edc-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="60edc-109">Return value</span></span>

<span data-ttu-id="60edc-110">Gibt void zurück.</span><span class="sxs-lookup"><span data-stu-id="60edc-110">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="60edc-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="60edc-111">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="60edc-112">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="60edc-112">Requirements</span></span>



| <span data-ttu-id="60edc-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="60edc-113">Requirement</span></span>          |    <span data-ttu-id="60edc-114">Wert</span><span class="sxs-lookup"><span data-stu-id="60edc-114">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="60edc-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="60edc-115">Minimum supported client</span></span><br/> | <span data-ttu-id="60edc-116">Windows 10, Version 1809 (10.0; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="60edc-116">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="60edc-117">DLL</span><span class="sxs-lookup"><span data-stu-id="60edc-117">DLL</span></span><br/>                      | <span data-ttu-id="60edc-118">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="60edc-118">EndpointDlp.dll</span></span> |