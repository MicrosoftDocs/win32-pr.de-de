---
description: Stellt dem System Informationen zu einem Dokument bereit, nachdem ein Drag &amp; Drop-Vorgang abgeschlossen wurde.
title: DlpNotifyPostDragDrop-Funktion (endpointdlp.h)
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
ms.openlocfilehash: 468255cee3c3fef44e44dd033b541e317db3d268
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495706"
---
# <a name="dlpnotifypostdragdrop-function"></a><span data-ttu-id="c9b4f-103">DlpNotifyPostDragDrop-Funktion</span><span class="sxs-lookup"><span data-stu-id="c9b4f-103">DlpNotifyPostDragDrop function</span></span>

<span data-ttu-id="c9b4f-104">Stellt dem System Informationen zu einem Dokument bereit, nachdem ein Drag &amp; Drop-Vorgang abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="c9b4f-104">Provides the system with information about a document after a drag drop operation is completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9b4f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c9b4f-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyPostDragDrop(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus);
```



## <a name="parameters"></a><span data-ttu-id="c9b4f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c9b4f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9b4f-107">*DocumentInfo* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="c9b4f-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9b4f-108">Ein Zeiger [](endpointdlp-dlp_document_info.md) auf eine PDLP_DOCUMENT_INFO-Struktur, die Informationen über das Dokument enthält, das dem Drag &amp; Drop-Vorgang zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="c9b4f-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document associated with the drag drop operation.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="c9b4f-109">*OpStatus* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="c9b4f-109">*OpStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9b4f-110">Ein Zeiger [](enpointdlp-dlp_postop_status.md) auf eine DLP_POSTOP_STATUS-Struktur, die Statusinformationen zum Drag &amp; Drop enthält.</span><span class="sxs-lookup"><span data-stu-id="c9b4f-110">A pointer to a [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) structure containing status information about the drag drop.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="c9b4f-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c9b4f-111">Return value</span></span>

<span data-ttu-id="c9b4f-112">Gibt void zurück.</span><span class="sxs-lookup"><span data-stu-id="c9b4f-112">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9b4f-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c9b4f-113">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="c9b4f-114">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="c9b4f-114">Requirements</span></span>



| <span data-ttu-id="c9b4f-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c9b4f-115">Requirement</span></span>          |    <span data-ttu-id="c9b4f-116">Wert</span><span class="sxs-lookup"><span data-stu-id="c9b4f-116">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c9b4f-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c9b4f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c9b4f-118">Windows 10, Version 1809 (10.0; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="c9b4f-118">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="c9b4f-119">DLL</span><span class="sxs-lookup"><span data-stu-id="c9b4f-119">DLL</span></span><br/>                      | <span data-ttu-id="c9b4f-120">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="c9b4f-120">EndpointDlp.dll</span></span> |