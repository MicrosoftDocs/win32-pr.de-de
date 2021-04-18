---
title: BITS_FILE_PROPERTY_ID-Enumeration (deliveryoptimization. h)
description: Die BITS_FILE_PROPERTY_ID-Enumeration gibt Werte an, die ID-Werte definieren, die den backgroundcopyfile-Eigenschaften entsprechen.
ms.assetid: 47EFD160-7CA8-48E6-A18E-38D85F7C6E47
keywords:
- BITS_FILE_PROPERTY_ID-Enumeration
- BITS_FILE_PROPERTY_ID-Enumeration
topic_type:
- apiref
api_name:
- BITS_FILE_PROPERTY_ID
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1b6c6b8a4de359e8313e3127080f2cc17ae6478c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340324"
---
# <a name="bits_file_property_id-enumeration"></a><span data-ttu-id="c3310-105">BITS_FILE_PROPERTY_ID-Enumeration</span><span class="sxs-lookup"><span data-stu-id="c3310-105">BITS_FILE_PROPERTY_ID enumeration</span></span>

<span data-ttu-id="c3310-106">Die **BITS_FILE_PROPERTY_ID** -Enumeration gibt Werte an, die ID-Werte definieren, die den **backgroundcopyfile** -Eigenschaften entsprechen.</span><span class="sxs-lookup"><span data-stu-id="c3310-106">The **BITS_FILE_PROPERTY_ID** enumeration specifies values that define ID values corresponding to **BackgroundCopyFile** properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3310-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c3310-107">Syntax</span></span>


```C++
typedef enum _BITS_FILE_PROPERTY_ID { 
  BITS_FILE_PROPERTY_ID_HTTP_RESPONSE_HEADERS  = 1
} BITS_FILE_PROPERTY_ID;
```



## <a name="constants"></a><span data-ttu-id="c3310-108">Konstanten</span><span class="sxs-lookup"><span data-stu-id="c3310-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="c3310-109"><span id="BITS_FILE_PROPERTY_ID_HTTP_RESPONSE_HEADERS"></span><span id="bits_file_property_id_http_response_headers"></span>**BITS_FILE_PROPERTY_ID_HTTP_RESPONSE_HEADERS**</span><span class="sxs-lookup"><span data-stu-id="c3310-109"><span id="BITS_FILE_PROPERTY_ID_HTTP_RESPONSE_HEADERS"></span><span id="bits_file_property_id_http_response_headers"></span>**BITS_FILE_PROPERTY_ID_HTTP_RESPONSE_HEADERS**</span></span>
</dt> <dd>

<span data-ttu-id="c3310-110">Der vollständige Satz von HTTP-Antwort Headern aus dem letzten http-Antwortpaket des Servers.</span><span class="sxs-lookup"><span data-stu-id="c3310-110">The full set of HTTP response headers from the server's last HTTP response packet.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c3310-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c3310-111">Requirements</span></span>



| <span data-ttu-id="c3310-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c3310-112">Requirement</span></span> | <span data-ttu-id="c3310-113">Wert</span><span class="sxs-lookup"><span data-stu-id="c3310-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3310-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c3310-114">Minimum supported client</span></span><br/> | <span data-ttu-id="c3310-115">Windows 10, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c3310-115">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="c3310-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c3310-116">Minimum supported server</span></span><br/> | <span data-ttu-id="c3310-117">Windows Server, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c3310-117">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="c3310-118">Header</span><span class="sxs-lookup"><span data-stu-id="c3310-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="c3310-119"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="c3310-119"><dt>Deliveryoptimization.h</dt></span></span> </dl> |



 

 





