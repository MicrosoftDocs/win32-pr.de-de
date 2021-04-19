---
description: Diese API ist nur für die interne Verwendung vorgesehen und sollte nicht in Ihrem Code verwendet werden.
ms.assetid: 836A7515-8C22-4032-9E99-F89B32C21685
title: Apisetqueryapisetpresence-Funktion (apiquery. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ApiSetQueryApiSetPresence
api_type:
- DllExport
api_location:
- api-ms-win-core-apiquery-l1-1-0.dll
- ntdll.dll
ms.openlocfilehash: 738a69b0d08f7e619dbd64229d0c13b2ae7dfaca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364260"
---
# <a name="apisetqueryapisetpresence-function"></a><span data-ttu-id="d6a63-103">Apisetqueryapisetpresence-Funktion</span><span class="sxs-lookup"><span data-stu-id="d6a63-103">ApiSetQueryApiSetPresence function</span></span>

<span data-ttu-id="d6a63-104">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="d6a63-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="d6a63-105">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="d6a63-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="d6a63-106">Diese API ist nur für die interne Verwendung vorgesehen und sollte nicht in Ihrem Code verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d6a63-106">This API is intended for internal use only and should not be used in your code.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6a63-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d6a63-107">Syntax</span></span>


```C++
BOOL WINAPI ApiSetQueryApiSetPresence(
  _In_  PCUNICODE_STRING Namespace,
  _Out_ PBOOLEAN         Present
);
```



## <a name="parameters"></a><span data-ttu-id="d6a63-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d6a63-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6a63-109">*Namespace* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d6a63-109">*Namespace* \[in\]</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="d6a63-110">*Vorhanden* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="d6a63-110">*Present* \[out\]</span></span>
<span data-ttu-id="d6a63-111"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="d6a63-111"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="d6a63-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d6a63-112">Requirements</span></span>



| <span data-ttu-id="d6a63-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d6a63-113">Requirement</span></span> | <span data-ttu-id="d6a63-114">Wert</span><span class="sxs-lookup"><span data-stu-id="d6a63-114">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6a63-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d6a63-115">Minimum supported client</span></span><br/> | <span data-ttu-id="d6a63-116">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d6a63-116">Windows 10 \[desktop apps only\]</span></span><br/>                                                                                                                                                           |
| <span data-ttu-id="d6a63-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d6a63-117">Minimum supported server</span></span><br/> | <span data-ttu-id="d6a63-118">Nur Windows Server 2016 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d6a63-118">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                                                                                                                  |
| <span data-ttu-id="d6a63-119">Header</span><span class="sxs-lookup"><span data-stu-id="d6a63-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="d6a63-120"><dt>Apiquery. h</dt></span><span class="sxs-lookup"><span data-stu-id="d6a63-120"><dt>Apiquery.h</dt></span></span> </dl>                                                                                                                 |
| <span data-ttu-id="d6a63-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d6a63-121">Library</span></span><br/>                  | <dl> <span data-ttu-id="d6a63-122"><dt>API-MS-WIN-Core-apiquery-L1. lib; </dt> <dt>API-MS-WIN-Core-apiquery-L1-1 -0. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d6a63-122"><dt>Api-ms-win-core-apiquery-l1.lib; </dt> <dt>Api-ms-win-core-apiquery-l1-1-0.lib</dt></span></span> </dl> |
| <span data-ttu-id="d6a63-123">DLL</span><span class="sxs-lookup"><span data-stu-id="d6a63-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d6a63-124"><dt>Api-ms-win-core-apiquery-l1-1-0.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d6a63-124"><dt>Api-ms-win-core-apiquery-l1-1-0.dll</dt></span></span> </dl>                                                                                        |



 

 




