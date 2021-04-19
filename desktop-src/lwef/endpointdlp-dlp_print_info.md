---
description: Gibt Informationen zu einem Dokument an, das einem Endpunkt-DLP-Druckvorgang zugeordnet ist.
title: DLP_PRINT_INFO -Struktur (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DLP_PRINT_INFO
api_type:
- COM
api_location:
- endpointdlp.h
ms.openlocfilehash: 37bde9f62de07083aac6a3d2fb367b021caf3732
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495781"
---
# <a name="dlp_print_info-structure"></a><span data-ttu-id="62afc-103">DLP_PRINT_INFO-Struktur</span><span class="sxs-lookup"><span data-stu-id="62afc-103">DLP_PRINT_INFO structure</span></span>

<span data-ttu-id="62afc-104">Gibt Informationen zu einem Dokument an, das einem Endpunkt-DLP-Druckvorgang zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="62afc-104">Specifies information about a document that is associated with an endpoint DLP print operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="62afc-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="62afc-105">Syntax</span></span>


```C++
typedef struct _DLP_PRINT_INFO {
    DWORD Version;
    LPCWSTR PrinterName;
    LPCWSTR JobName;
    LPCWSTR OutputFileName;
    
}DLP_PRINT_INFO, *PDLP_PRINT_INFO;
```


## <a name="members"></a><span data-ttu-id="62afc-106">Members</span><span class="sxs-lookup"><span data-stu-id="62afc-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="62afc-107">*Version* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="62afc-107">*Version* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62afc-108">Ein DWORD, das die API-Version an gibt.</span><span class="sxs-lookup"><span data-stu-id="62afc-108">A DWORD specifying the API version.</span></span> <span data-ttu-id="62afc-109">Dieser Wert sollte immer **DLP_PRINT_INFO_V_LATEST.**</span><span class="sxs-lookup"><span data-stu-id="62afc-109">This value should always be **DLP_PRINT_INFO_V_LATEST**.</span></span> <span data-ttu-id="62afc-110">Diese Konstante wird in der Auflistung der Endpointdlp.h-Beispielheaderdatei im Artikel [Endpoint data loss prevention definiert.](endpointdlp-endpoint-data-loss-prevention.md)</span><span class="sxs-lookup"><span data-stu-id="62afc-110">This constant is defined in the endpointdlp.h sample header file listing in the article [Endpoint data loss prevention](endpointdlp-endpoint-data-loss-prevention.md).</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="62afc-111">*PrinterName* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="62afc-111">*PrinterName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62afc-112">Ein LPCWSTR, der den Zieldrucker identifiziert.</span><span class="sxs-lookup"><span data-stu-id="62afc-112">A LPCWSTR identifying the destination printer.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="62afc-113">*JobName* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="62afc-113">*JobName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62afc-114">Ein LPCWSTR, der den Namen des Druckauftrags an gibt.</span><span class="sxs-lookup"><span data-stu-id="62afc-114">A LPCWSTR specifying print job name.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="62afc-115">*OutputFileName* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="62afc-115">*OutputFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62afc-116">Ein LPCWSTR, der beim Drucken in eine Datei den Pfad zur Ausgabedatei an gibt.</span><span class="sxs-lookup"><span data-stu-id="62afc-116">A LPCWSTR specifying the path to the output file, when printing to a file.</span></span>

</dd> </dl>



## <a name="remarks"></a><span data-ttu-id="62afc-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="62afc-117">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="62afc-118">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="62afc-118">Requirements</span></span>



| <span data-ttu-id="62afc-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="62afc-119">Requirement</span></span>          |    <span data-ttu-id="62afc-120">Wert</span><span class="sxs-lookup"><span data-stu-id="62afc-120">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="62afc-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="62afc-121">Minimum supported client</span></span><br/> | <span data-ttu-id="62afc-122">Windows 10, Version 1809 (10.0; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="62afc-122">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |

