---
title: MP_SIGNATURE_TYPE-Enumeration (mpclient. h)
description: Mögliche Signatur Typen.
ms.assetid: 44B195A8-866D-4B87-9576-54E00658F9B3
keywords:
- MP_SIGNATURE_TYPE-Enumerationsfunktionen der Legacy-Windows-Umgebung
- PMP_SIGNATURE_TYPE enumerationszeiger Legacy-Windows-Umgebungs Features
topic_type:
- apiref
api_name:
- MP_SIGNATURE_TYPE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b99f7140706e9a6d3fa32e7eb346ef6478f3f26
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476503"
---
# <a name="mp_signature_type-enumeration"></a><span data-ttu-id="ef19d-105">MP- \_ Signatur \_ Typen-Enumeration</span><span class="sxs-lookup"><span data-stu-id="ef19d-105">MP\_SIGNATURE\_TYPE enumeration</span></span>

<span data-ttu-id="ef19d-106">Mögliche Signatur Typen.</span><span class="sxs-lookup"><span data-stu-id="ef19d-106">Possible signature types.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef19d-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ef19d-107">Syntax</span></span>


```C++
typedef enum tagMP_SIGNATURE_TYPE { 
  MP_SIGNATURE_ANTIMALWARE     = 0,
  MP_SIGNATURE_ANTIVIRUS       = 1,
  MP_SIGNATURE_ANTISPYWARE     = 2,
  MP_SIGNATURE_NIS             = 3,
  MP_SIGNATURE_TYPES_MAXVALUE  = 3
} MP_SIGNATURE_TYPE, *PMP_SIGNATURE_TYPE;
```



## <a name="constants"></a><span data-ttu-id="ef19d-108">Konstanten</span><span class="sxs-lookup"><span data-stu-id="ef19d-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="ef19d-109"><span id="MP_SIGNATURE_ANTIMALWARE"></span><span id="mp_signature_antimalware"></span>**MP- \_ Signatur- \_ Antischadsoftware**</span><span class="sxs-lookup"><span data-stu-id="ef19d-109"><span id="MP_SIGNATURE_ANTIMALWARE"></span><span id="mp_signature_antimalware"></span>**MP\_SIGNATURE\_ANTIMALWARE**</span></span>
</dt> <dd>

<span data-ttu-id="ef19d-110">Sowohl Antivirus-als auch antispywaresignaturen.</span><span class="sxs-lookup"><span data-stu-id="ef19d-110">Both antivirus and antispyware signatures.</span></span>

</dd> <dt>

<span data-ttu-id="ef19d-111"><span id="MP_SIGNATURE_ANTIVIRUS"></span><span id="mp_signature_antivirus"></span>**MP- \_ Signatur \_ Antivirus**</span><span class="sxs-lookup"><span data-stu-id="ef19d-111"><span id="MP_SIGNATURE_ANTIVIRUS"></span><span id="mp_signature_antivirus"></span>**MP\_SIGNATURE\_ANTIVIRUS**</span></span>
</dt> <dd>

<span data-ttu-id="ef19d-112">Nur Antivirensignaturen.</span><span class="sxs-lookup"><span data-stu-id="ef19d-112">Only antivirus signatures.</span></span>

</dd> <dt>

<span data-ttu-id="ef19d-113"><span id="MP_SIGNATURE_ANTISPYWARE"></span><span id="mp_signature_antispyware"></span>**MP- \_ Signatur- \_ AntiSpyware**</span><span class="sxs-lookup"><span data-stu-id="ef19d-113"><span id="MP_SIGNATURE_ANTISPYWARE"></span><span id="mp_signature_antispyware"></span>**MP\_SIGNATURE\_ANTISPYWARE**</span></span>
</dt> <dd>

<span data-ttu-id="ef19d-114">Nur antispywaresignaturen.</span><span class="sxs-lookup"><span data-stu-id="ef19d-114">Only antispyware signatures.</span></span>

</dd> <dt>

<span data-ttu-id="ef19d-115"><span id="MP_SIGNATURE_NIS"></span><span id="mp_signature_nis"></span>**MP- \_ Signatur \_ NIS**</span><span class="sxs-lookup"><span data-stu-id="ef19d-115"><span id="MP_SIGNATURE_NIS"></span><span id="mp_signature_nis"></span>**MP\_SIGNATURE\_NIS**</span></span>
</dt> <dd>

<span data-ttu-id="ef19d-116">NIS-Signaturen.</span><span class="sxs-lookup"><span data-stu-id="ef19d-116">NIS signatures.</span></span>

</dd> <dt>

<span data-ttu-id="ef19d-117"><span id="MP_SIGNATURE_TYPES_MAXVALUE"></span><span id="mp_signature_types_maxvalue"></span>**MP- \_ Signatur \_ Typen \_ MaxValue**</span><span class="sxs-lookup"><span data-stu-id="ef19d-117"><span id="MP_SIGNATURE_TYPES_MAXVALUE"></span><span id="mp_signature_types_maxvalue"></span>**MP\_SIGNATURE\_TYPES\_MAXVALUE**</span></span>
<span data-ttu-id="ef19d-118"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="ef19d-118"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="ef19d-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ef19d-119">Requirements</span></span>



| <span data-ttu-id="ef19d-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ef19d-120">Requirement</span></span> | <span data-ttu-id="ef19d-121">Wert</span><span class="sxs-lookup"><span data-stu-id="ef19d-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ef19d-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ef19d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ef19d-123">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ef19d-123">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="ef19d-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ef19d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ef19d-125">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ef19d-125">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ef19d-126">Header</span><span class="sxs-lookup"><span data-stu-id="ef19d-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef19d-127"><dt>Mpclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef19d-127"><dt>MpClient.h</dt></span></span> </dl> |



 

 





