---
description: Stellt dem System Informationen zu einem Dokument zur Verfügung, nachdem der Vorgang zum Speichern unter abgeschlossen wurde.
title: DlpNotifyPostSaveAsDocument-Funktion (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPostSaveAsDocument
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: 564e7173cbfe72a020f1c7e12a60ceda25fd845c
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495654"
---
# <a name="dlpnotifypostsaveasdocument-function"></a><span data-ttu-id="96ece-103">DlpNotifyPostSaveAsDocument-Funktion</span><span class="sxs-lookup"><span data-stu-id="96ece-103">DlpNotifyPostSaveAsDocument function</span></span>

<span data-ttu-id="96ece-104">Stellt dem System Informationen zu einem Dokument zur Verfügung, nachdem der Vorgang zum Speichern unter abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="96ece-104">Provides the system with information about a document after the save as operation is completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="96ece-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="96ece-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyPostSaveAsDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ LPCWSTR Destination, _In_ const PDLP_POSTOP_STATUS OpStatus); 
```

## <a name="parameters"></a><span data-ttu-id="96ece-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="96ece-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96ece-107">*DocumentInfo* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="96ece-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96ece-108">Ein Zeiger auf [](endpointdlp-dlp_document_info.md) eine PDLP_DOCUMENT_INFO-Struktur, die Informationen über das gespeicherte Dokument enthält.</span><span class="sxs-lookup"><span data-stu-id="96ece-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document that was saved.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="96ece-109">*Ziel* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="96ece-109">*Destination* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96ece-110">Ein **LPCWSTR mit** dem Zielpfad des gespeicherten Dokuments.</span><span class="sxs-lookup"><span data-stu-id="96ece-110">A **LPCWSTR** containing the destination path the document that was saved.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="96ece-111">*OpStatus* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="96ece-111">*OpStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96ece-112">Ein Zeiger auf [](enpointdlp-dlp_postop_status.md) eine DLP_POSTOP_STATUS-Struktur, die Statusinformationen zum Save as-Vorgang enthält.</span><span class="sxs-lookup"><span data-stu-id="96ece-112">A pointer to a [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) structure containing status information about the save as operation.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="96ece-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="96ece-113">Return value</span></span>

<span data-ttu-id="96ece-114">Gibt void zurück.</span><span class="sxs-lookup"><span data-stu-id="96ece-114">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="96ece-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="96ece-115">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="96ece-116">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="96ece-116">Requirements</span></span>



| <span data-ttu-id="96ece-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="96ece-117">Requirement</span></span>          |    <span data-ttu-id="96ece-118">Wert</span><span class="sxs-lookup"><span data-stu-id="96ece-118">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="96ece-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="96ece-119">Minimum supported client</span></span><br/> | <span data-ttu-id="96ece-120">Windows 10, Version 1809 (10.0; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="96ece-120">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="96ece-121">DLL</span><span class="sxs-lookup"><span data-stu-id="96ece-121">DLL</span></span><br/>                      | <span data-ttu-id="96ece-122">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="96ece-122">EndpointDlp.dll</span></span> |