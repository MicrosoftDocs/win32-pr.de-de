---
description: Stellt dem System Informationen zu einem Dokument bereit, nachdem der Öffnungsvorgang abgeschlossen wurde.
title: DlpNotifyPostOpenDocument-Funktion (endpointdlp.h)
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
ms.openlocfilehash: 10121e69ddbdc41516e56ec07e87a2f6dd8148cd
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495705"
---
# <a name="dlpnotifypostopendocument-function"></a><span data-ttu-id="c3cf8-103">DlpNotifyPostOpenDocument-Funktion</span><span class="sxs-lookup"><span data-stu-id="c3cf8-103">DlpNotifyPostOpenDocument function</span></span>

<span data-ttu-id="c3cf8-104">Stellt dem System Informationen zu einem Dokument bereit, nachdem ein geöffneter Dokumentvorgang abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="c3cf8-104">Provides the system with information about a document after an open document operation is completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3cf8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c3cf8-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyPostOpenDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus); 
```

## <a name="parameters"></a><span data-ttu-id="c3cf8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c3cf8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3cf8-107">*DocumentInfo* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="c3cf8-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3cf8-108">Ein Zeiger [](endpointdlp-dlp_document_info.md) auf eine PDLP_DOCUMENT_INFO-Struktur, die Informationen über das geöffnete Dokument enthält.</span><span class="sxs-lookup"><span data-stu-id="c3cf8-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document that was opened.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="c3cf8-109">*OpStatus* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="c3cf8-109">*OpStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3cf8-110">Ein Zeiger [](enpointdlp-dlp_postop_status.md) auf eine DLP_POSTOP_STATUS-Struktur, die Statusinformationen zum Vorgang des geöffneten Dokuments enthält.</span><span class="sxs-lookup"><span data-stu-id="c3cf8-110">A pointer to a [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) structure containing status information about the open document operation.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="c3cf8-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c3cf8-111">Return value</span></span>

<span data-ttu-id="c3cf8-112">Gibt void zurück.</span><span class="sxs-lookup"><span data-stu-id="c3cf8-112">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="c3cf8-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c3cf8-113">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="c3cf8-114">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="c3cf8-114">Requirements</span></span>



| <span data-ttu-id="c3cf8-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c3cf8-115">Requirement</span></span>          |    <span data-ttu-id="c3cf8-116">Wert</span><span class="sxs-lookup"><span data-stu-id="c3cf8-116">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c3cf8-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c3cf8-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c3cf8-118">Windows 10, Version 1809 (10.0; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="c3cf8-118">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="c3cf8-119">DLL</span><span class="sxs-lookup"><span data-stu-id="c3cf8-119">DLL</span></span><br/>                      | <span data-ttu-id="c3cf8-120">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="c3cf8-120">EndpointDlp.dll</span></span> |