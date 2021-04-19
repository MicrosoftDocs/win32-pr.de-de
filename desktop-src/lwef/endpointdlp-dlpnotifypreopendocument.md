---
description: Stellt dem System Informationen zu einem Dokument bereit, bevor ein Öffnungsvorgang initiiert wird.
title: DlpNotifyPreOpenDocument-Funktion (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPreOpenDocument
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: 557554ad55a3a520fa95fcf53c8044881eed8b21
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495637"
---
# <a name="dlpnotifypreopendocument-function"></a><span data-ttu-id="21bff-103">DlpNotifyPreOpenDocument-Funktion</span><span class="sxs-lookup"><span data-stu-id="21bff-103">DlpNotifyPreOpenDocument function</span></span>

<span data-ttu-id="21bff-104">Stellt dem System Informationen zu einem Dokument bereit, bevor ein geöffneter Vorgang initiiert wird.</span><span class="sxs-lookup"><span data-stu-id="21bff-104">Provides the system with information about a document before an open operation is initiated.</span></span>

## <a name="syntax"></a><span data-ttu-id="21bff-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="21bff-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyPreOpenDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
```



## <a name="parameters"></a><span data-ttu-id="21bff-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="21bff-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21bff-107">*DocumentInfo* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="21bff-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21bff-108">Ein Zeiger [](endpointdlp-dlp_document_info.md) auf eine PDLP_DOCUMENT_INFO-Struktur, die Informationen über das zu öffnende Dokument enthält.</span><span class="sxs-lookup"><span data-stu-id="21bff-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document to be opened.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="21bff-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="21bff-109">Return value</span></span>

<span data-ttu-id="21bff-110">Gibt void zurück.</span><span class="sxs-lookup"><span data-stu-id="21bff-110">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="21bff-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="21bff-111">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="21bff-112">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="21bff-112">Requirements</span></span>



| <span data-ttu-id="21bff-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="21bff-113">Requirement</span></span>          |    <span data-ttu-id="21bff-114">Wert</span><span class="sxs-lookup"><span data-stu-id="21bff-114">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="21bff-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="21bff-115">Minimum supported client</span></span><br/> | <span data-ttu-id="21bff-116">Windows 10, Version 1809 (10.0; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="21bff-116">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="21bff-117">DLL</span><span class="sxs-lookup"><span data-stu-id="21bff-117">DLL</span></span><br/>                      | <span data-ttu-id="21bff-118">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="21bff-118">EndpointDlp.dll</span></span> |