---
description: Stellt dem System Informationen zu einem Dokument zur Verfügung, wenn ein Abbruchziel beendet wird.
title: DlpNotifyLeaveDropTarget-Funktion (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyLeaveDropTarget
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: 2f96ea9a825ca930631fe94dd1a3d632019dd9c1
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495717"
---
# <a name="dlpnotifyleavedroptarget-function"></a><span data-ttu-id="dc386-103">DlpNotifyLeaveDropTarget-Funktion</span><span class="sxs-lookup"><span data-stu-id="dc386-103">DlpNotifyLeaveDropTarget function</span></span>

<span data-ttu-id="dc386-104">Stellt dem System Informationen zu einem Dokument zur Verfügung, wenn ein Abbruchziel beendet wird.</span><span class="sxs-lookup"><span data-stu-id="dc386-104">Provides the system with information about a document when a drop target is exited.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc386-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="dc386-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyLeaveDropTarget(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus);
```



## <a name="parameters"></a><span data-ttu-id="dc386-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="dc386-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc386-107">*DocumentInfo* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="dc386-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc386-108">Ein Zeiger auf eine [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) Struktur, die Informationen über das Dokument enthält, das dem Abbruchvorgang zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="dc386-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document associated with the drop operation.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="dc386-109">*OpStatus* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="dc386-109">*OpStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc386-110">Ein Zeiger auf eine [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) Struktur, die Statusinformationen zum Beendigungsvorgang des Abbruchziels enthält.</span><span class="sxs-lookup"><span data-stu-id="dc386-110">A pointer to a [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) structure containing status information about the drop target exit operation.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="dc386-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dc386-111">Return value</span></span>

<span data-ttu-id="dc386-112">Gibt void zurück.</span><span class="sxs-lookup"><span data-stu-id="dc386-112">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="dc386-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dc386-113">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="dc386-114">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="dc386-114">Requirements</span></span>



| <span data-ttu-id="dc386-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dc386-115">Requirement</span></span>          |    <span data-ttu-id="dc386-116">Wert</span><span class="sxs-lookup"><span data-stu-id="dc386-116">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dc386-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dc386-117">Minimum supported client</span></span><br/> | <span data-ttu-id="dc386-118">Windows 10, Version 1809 (10.0; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="dc386-118">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="dc386-119">DLL</span><span class="sxs-lookup"><span data-stu-id="dc386-119">DLL</span></span><br/>                      | <span data-ttu-id="dc386-120">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="dc386-120">EndpointDlp.dll</span></span> |