---
description: Gibt Informationen zu einem Dokument an, das einem Endpunkt-DLP-Vorgang zugeordnet ist.
title: DLP_DOCUMENT_INFO -Struktur (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DLP_DOCUMENT_INFO
api_type:
- COM
api_location:
- endpointdlp.h
ms.openlocfilehash: d588b627a4d5a88162cb0af67df1b5bf4fd943f1
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495782"
---
# <a name="dlp_document_info-structure"></a><span data-ttu-id="18df6-103">DLP_DOCUMENT_INFO Struktur</span><span class="sxs-lookup"><span data-stu-id="18df6-103">DLP_DOCUMENT_INFO structure</span></span>

<span data-ttu-id="18df6-104">Gibt Informationen zu einem Dokument an, das einem Endpunkt-DLP-Vorgang zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="18df6-104">Specifies information about a document that is associated with an endpoint DLP operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="18df6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="18df6-105">Syntax</span></span>


```C++
typedef struct _DLP_DOCUMENT_INFO {

    DWORD Version;    
    LPCWSTR PersistentFileName;
    LPCWSTR LocalFileName;

}DLP_DOCUMENT_INFO, *PDLP_DOCUMENT_INFO;
```


## <a name="members"></a><span data-ttu-id="18df6-106">Members</span><span class="sxs-lookup"><span data-stu-id="18df6-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="18df6-107">*Version* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="18df6-107">*Version* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18df6-108">Ein DWORD, das die API-Version an gibt.</span><span class="sxs-lookup"><span data-stu-id="18df6-108">A DWORD specifying the API version.</span></span> <span data-ttu-id="18df6-109">Dieser Wert sollte immer **DLP_DOCUMENT_INFO_V_LATEST.**</span><span class="sxs-lookup"><span data-stu-id="18df6-109">This value should always be **DLP_DOCUMENT_INFO_V_LATEST**.</span></span> <span data-ttu-id="18df6-110">Diese Konstante wird in der Auflistung der Endpointdlp.h-Beispielheaderdatei im Artikel [Endpoint data loss prevention definiert.](endpointdlp-endpoint-data-loss-prevention.md)</span><span class="sxs-lookup"><span data-stu-id="18df6-110">This constant is defined in the endpointdlp.h sample header file listing in the article [Endpoint data loss prevention](endpointdlp-endpoint-data-loss-prevention.md).</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="18df6-111">*PersistentFileName* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="18df6-111">*PersistentFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18df6-112">Ein LPCWSTR, der den ursprünglichen Pfad des Dokuments an gibt.</span><span class="sxs-lookup"><span data-stu-id="18df6-112">A LPCWSTR specifying the original path of the document.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="18df6-113">*LocalFileName* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="18df6-113">*LocalFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18df6-114">Ein LPCWSTR, der den Pfad zur tatsächlichen Hintergrunddatei des Dokuments an gibt.</span><span class="sxs-lookup"><span data-stu-id="18df6-114">A LPCWSTR specifying the path to the real backing file of the document.</span></span>

</dd> </dl>



## <a name="remarks"></a><span data-ttu-id="18df6-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="18df6-115">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="18df6-116">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="18df6-116">Requirements</span></span>



| <span data-ttu-id="18df6-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="18df6-117">Requirement</span></span>          |    <span data-ttu-id="18df6-118">Wert</span><span class="sxs-lookup"><span data-stu-id="18df6-118">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="18df6-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="18df6-119">Minimum supported client</span></span><br/> | <span data-ttu-id="18df6-120">Windows 10, Version 1809 (10.0; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="18df6-120">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |

