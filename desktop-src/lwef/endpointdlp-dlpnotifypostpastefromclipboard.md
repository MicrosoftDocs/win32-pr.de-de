---
description: Stellt dem System Informationen zu einem Dokument zur Verfügung, nachdem ein Einfügevorgang aus der Zwischenablage abgeschlossen wurde.
title: DlpNotifyPostPasteFromClipboard-Funktion (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPostPasteFromClipboard
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: 69a5afbc41350092ebd4d433d2f4d7259ece82cf
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495662"
---
# <a name="dlpnotifypostpastefromclipboard-function"></a><span data-ttu-id="3e4d7-103">DlpNotifyPostPasteFromClipboard-Funktion</span><span class="sxs-lookup"><span data-stu-id="3e4d7-103">DlpNotifyPostPasteFromClipboard function</span></span>

<span data-ttu-id="3e4d7-104">Stellt dem System Informationen zu einem Dokument zur Verfügung, nachdem ein Einfügevorgang aus der Zwischenablage abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="3e4d7-104">Provides the system with information about a document after a paste from clipboard operation is completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e4d7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3e4d7-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyPostPasteFromClipboard(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus);
```



## <a name="parameters"></a><span data-ttu-id="3e4d7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3e4d7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e4d7-107">*DocumentInfo* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="3e4d7-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e4d7-108">Ein Zeiger auf [](endpointdlp-dlp_document_info.md) eine PDLP_DOCUMENT_INFO-Struktur, die Informationen über das Dokument enthält, in das der Inhalt kopiert wurde.</span><span class="sxs-lookup"><span data-stu-id="3e4d7-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document into which content was copied.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="3e4d7-109">*OpStatus* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="3e4d7-109">*OpStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e4d7-110">Ein Zeiger auf [](enpointdlp-dlp_postop_status.md) eine DLP_POSTOP_STATUS-Struktur, die Statusinformationen zum Einfügen aus der Zwischenablage enthält.</span><span class="sxs-lookup"><span data-stu-id="3e4d7-110">A pointer to a [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) structure containing status information about the paste from clipboard operation.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="3e4d7-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3e4d7-111">Return value</span></span>

<span data-ttu-id="3e4d7-112">Gibt void zurück.</span><span class="sxs-lookup"><span data-stu-id="3e4d7-112">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="3e4d7-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3e4d7-113">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="3e4d7-114">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="3e4d7-114">Requirements</span></span>



| <span data-ttu-id="3e4d7-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3e4d7-115">Requirement</span></span>          |    <span data-ttu-id="3e4d7-116">Wert</span><span class="sxs-lookup"><span data-stu-id="3e4d7-116">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3e4d7-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3e4d7-117">Minimum supported client</span></span><br/> | <span data-ttu-id="3e4d7-118">Windows 10, Version 1809 (10.0; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="3e4d7-118">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="3e4d7-119">DLL</span><span class="sxs-lookup"><span data-stu-id="3e4d7-119">DLL</span></span><br/>                      | <span data-ttu-id="3e4d7-120">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="3e4d7-120">EndpointDlp.dll</span></span> |