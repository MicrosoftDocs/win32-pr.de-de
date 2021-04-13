---
title: MPTHREAT_TYPE-Enumeration (mpclient. h)
description: Mögliche Bedrohungs Typen.
ms.assetid: 56061F12-AA89-4203-BED4-99613E24002A
keywords:
- MPTHREAT_TYPE-Enumerationsfunktionen der Legacy-Windows-Umgebung
- PMPTHREAT_TYPE enumerationszeiger Legacy-Windows-Umgebungs Features
topic_type:
- apiref
api_name:
- MPTHREAT_TYPE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ed823b100c91f259252d7cad71e554099caf6a2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391786"
---
# <a name="mpthreat_type-enumeration"></a><span data-ttu-id="d7569-105">Mpthreat \_ Type-Enumeration</span><span class="sxs-lookup"><span data-stu-id="d7569-105">MPTHREAT\_TYPE enumeration</span></span>

<span data-ttu-id="d7569-106">Mögliche Bedrohungs Typen.</span><span class="sxs-lookup"><span data-stu-id="d7569-106">Possible threat types.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7569-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d7569-107">Syntax</span></span>


```C++
typedef enum tagMPTHREAT_TYPE { 
  MPTHREAT_TYPE_KNOWNBAD   = 0,
  MPTHREAT_TYPE_BEHAVIOR   = 1,
  MPTHREAT_TYPE_UNKNOWN    = 2,
  MPTHREAT_TYPE_KNOWNGOOD  = 3,
  MPTHREAT_TYPE_NIS        = 4,
  MPTHREAT_TYPE_MAXVALUE   = 4
} MPTHREAT_TYPE, *PMPTHREAT_TYPE;
```



## <a name="constants"></a><span data-ttu-id="d7569-108">Konstanten</span><span class="sxs-lookup"><span data-stu-id="d7569-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="d7569-109"><span id="MPTHREAT_TYPE_KNOWNBAD"></span><span id="mpthreat_type_knownbad"></span>**mpthreat- \_ Typ \_ knownbad**</span><span class="sxs-lookup"><span data-stu-id="d7569-109"><span id="MPTHREAT_TYPE_KNOWNBAD"></span><span id="mpthreat_type_knownbad"></span>**MPTHREAT\_TYPE\_KNOWNBAD**</span></span>
</dt> <dd>

<span data-ttu-id="d7569-110">Bekannte ungültige Bedrohung durch Signatur erkannt.</span><span class="sxs-lookup"><span data-stu-id="d7569-110">Known bad threat detected via signature.</span></span>

</dd> <dt>

<span data-ttu-id="d7569-111"><span id="MPTHREAT_TYPE_BEHAVIOR"></span><span id="mpthreat_type_behavior"></span>**mpthreat \_ - \_ typverhalten**</span><span class="sxs-lookup"><span data-stu-id="d7569-111"><span id="MPTHREAT_TYPE_BEHAVIOR"></span><span id="mpthreat_type_behavior"></span>**MPTHREAT\_TYPE\_BEHAVIOR**</span></span>
</dt> <dd>

<span data-ttu-id="d7569-112">Verdächtige Bedrohung durch Verhaltens Überwachung erkannt.</span><span class="sxs-lookup"><span data-stu-id="d7569-112">Suspicious threat detected via behavior monitoring.</span></span>

</dd> <dt>

<span data-ttu-id="d7569-113"><span id="MPTHREAT_TYPE_UNKNOWN"></span><span id="mpthreat_type_unknown"></span>**mpthreat- \_ Typ \_ unbekannt**</span><span class="sxs-lookup"><span data-stu-id="d7569-113"><span id="MPTHREAT_TYPE_UNKNOWN"></span><span id="mpthreat_type_unknown"></span>**MPTHREAT\_TYPE\_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="d7569-114">Unbekannte Bedrohungen (nicht klassifiziert).</span><span class="sxs-lookup"><span data-stu-id="d7569-114">Unknown threats (unclassified).</span></span>

</dd> <dt>

<span data-ttu-id="d7569-115"><span id="MPTHREAT_TYPE_KNOWNGOOD"></span><span id="mpthreat_type_knowngood"></span>**mpthreat- \_ Typ \_ knowngood**</span><span class="sxs-lookup"><span data-stu-id="d7569-115"><span id="MPTHREAT_TYPE_KNOWNGOOD"></span><span id="mpthreat_type_knowngood"></span>**MPTHREAT\_TYPE\_KNOWNGOOD**</span></span>
</dt> <dd>

<span data-ttu-id="d7569-116">Bekannte gute Bedrohung.</span><span class="sxs-lookup"><span data-stu-id="d7569-116">Known good threat.</span></span>

</dd> <dt>

<span data-ttu-id="d7569-117"><span id="MPTHREAT_TYPE_NIS"></span><span id="mpthreat_type_nis"></span>**mpthreat- \_ Typ \_ NIS**</span><span class="sxs-lookup"><span data-stu-id="d7569-117"><span id="MPTHREAT_TYPE_NIS"></span><span id="mpthreat_type_nis"></span>**MPTHREAT\_TYPE\_NIS**</span></span>
</dt> <dd>

<span data-ttu-id="d7569-118">NIS-Bedrohungserkennung.</span><span class="sxs-lookup"><span data-stu-id="d7569-118">NIS threat detection.</span></span>

</dd> <dt>

<span data-ttu-id="d7569-119"><span id="MPTHREAT_TYPE_MAXVALUE"></span><span id="mpthreat_type_maxvalue"></span>**mpthreat- \_ Typ \_ MaxValue**</span><span class="sxs-lookup"><span data-stu-id="d7569-119"><span id="MPTHREAT_TYPE_MAXVALUE"></span><span id="mpthreat_type_maxvalue"></span>**MPTHREAT\_TYPE\_MAXVALUE**</span></span>
</dt> <dd>

<span data-ttu-id="d7569-120">Maximal möglicher Wert.</span><span class="sxs-lookup"><span data-stu-id="d7569-120">Maximum value possible.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d7569-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d7569-121">Requirements</span></span>



| <span data-ttu-id="d7569-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d7569-122">Requirement</span></span> | <span data-ttu-id="d7569-123">Wert</span><span class="sxs-lookup"><span data-stu-id="d7569-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d7569-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d7569-124">Minimum supported client</span></span><br/> | <span data-ttu-id="d7569-125">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d7569-125">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="d7569-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d7569-126">Minimum supported server</span></span><br/> | <span data-ttu-id="d7569-127">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d7569-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d7569-128">Header</span><span class="sxs-lookup"><span data-stu-id="d7569-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7569-129"><dt>Mpclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7569-129"><dt>MpClient.h</dt></span></span> </dl> |



 

 





