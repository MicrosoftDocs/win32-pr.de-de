---
title: MPSCAN_TYPE-Enumeration (mpclient. h)
description: Der Typ des ausgeführten Scans.
ms.assetid: 980A80FD-FF02-4338-B7FB-DAA141F65E89
keywords:
- MPSCAN_TYPE-Enumerationsfunktionen der Legacy-Windows-Umgebung
- PMPSCAN_TYPE enumerationszeiger Legacy-Windows-Umgebungs Features
topic_type:
- apiref
api_name:
- MPSCAN_TYPE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9eb89137dc9cfe5b8a4ff1f44a7a101239aa3a22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740136"
---
# <a name="mpscan_type-enumeration"></a><span data-ttu-id="ea4cf-105">Mpscan- \_ Typenumeration</span><span class="sxs-lookup"><span data-stu-id="ea4cf-105">MPSCAN\_TYPE enumeration</span></span>

<span data-ttu-id="ea4cf-106">Der Typ des ausgeführten Scans.</span><span class="sxs-lookup"><span data-stu-id="ea4cf-106">Type of scan performed.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea4cf-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ea4cf-107">Syntax</span></span>


```C++
typedef enum tagMPSCAN_TYPE { 
  MPSCAN_TYPE_UNKNOWN   = 0,
  MPSCAN_TYPE_QUICK     = 1,
  MPSCAN_TYPE_FULL      = 2,
  MPSCAN_TYPE_RESOURCE  = 3,
  MPSCAN_TYPE_MAXVALUE  = 3
} MPSCAN_TYPE, *PMPSCAN_TYPE;
```



## <a name="constants"></a><span data-ttu-id="ea4cf-108">Konstanten</span><span class="sxs-lookup"><span data-stu-id="ea4cf-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="ea4cf-109"><span id="MPSCAN_TYPE_UNKNOWN"></span><span id="mpscan_type_unknown"></span>**mpscan- \_ Typ \_ unbekannt**</span><span class="sxs-lookup"><span data-stu-id="ea4cf-109"><span id="MPSCAN_TYPE_UNKNOWN"></span><span id="mpscan_type_unknown"></span>**MPSCAN\_TYPE\_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="ea4cf-110">Nur interne Verwendung.</span><span class="sxs-lookup"><span data-stu-id="ea4cf-110">Internal use only.</span></span>

</dd> <dt>

<span data-ttu-id="ea4cf-111"><span id="MPSCAN_TYPE_QUICK"></span><span id="mpscan_type_quick"></span>**mpscan- \_ Typ \_ Quick**</span><span class="sxs-lookup"><span data-stu-id="ea4cf-111"><span id="MPSCAN_TYPE_QUICK"></span><span id="mpscan_type_quick"></span>**MPSCAN\_TYPE\_QUICK**</span></span>
</dt> <dd>

<span data-ttu-id="ea4cf-112">Scannt laufende Prozesse und verschiedene ASEP-Punkte im System, wo Schadsoftware normalerweise ausgeblendet wird.</span><span class="sxs-lookup"><span data-stu-id="ea4cf-112">Scans running processes and various ASEP points in the system where malware typically hides.</span></span>

</dd> <dt>

<span data-ttu-id="ea4cf-113"><span id="MPSCAN_TYPE_FULL"></span><span id="mpscan_type_full"></span>**mpscan- \_ Typ \_ voll**</span><span class="sxs-lookup"><span data-stu-id="ea4cf-113"><span id="MPSCAN_TYPE_FULL"></span><span id="mpscan_type_full"></span>**MPSCAN\_TYPE\_FULL**</span></span>
</dt> <dd>

<span data-ttu-id="ea4cf-114">Führt eine schnell Überprüfung durch, gefolgt von der Überprüfung aller Festplattenlaufwerke des Systems.</span><span class="sxs-lookup"><span data-stu-id="ea4cf-114">Performs a quick scan followed by scan of all fixed drives of the system.</span></span>

</dd> <dt>

<span data-ttu-id="ea4cf-115"><span id="MPSCAN_TYPE_RESOURCE"></span><span id="mpscan_type_resource"></span>**mpscan \_ - \_ typressource**</span><span class="sxs-lookup"><span data-stu-id="ea4cf-115"><span id="MPSCAN_TYPE_RESOURCE"></span><span id="mpscan_type_resource"></span>**MPSCAN\_TYPE\_RESOURCE**</span></span>
</dt> <dd>

<span data-ttu-id="ea4cf-116">Scannt bestimmte Ressourcen, z. b. Dateien oder Ordner.</span><span class="sxs-lookup"><span data-stu-id="ea4cf-116">Scans specific resources, such as files or folders.</span></span>

</dd> <dt>

<span data-ttu-id="ea4cf-117"><span id="MPSCAN_TYPE_MAXVALUE"></span><span id="mpscan_type_maxvalue"></span>**mpscan- \_ Typ \_ MaxValue**</span><span class="sxs-lookup"><span data-stu-id="ea4cf-117"><span id="MPSCAN_TYPE_MAXVALUE"></span><span id="mpscan_type_maxvalue"></span>**MPSCAN\_TYPE\_MAXVALUE**</span></span>
</dt> <dd>

<span data-ttu-id="ea4cf-118">Maximal möglicher Wert.</span><span class="sxs-lookup"><span data-stu-id="ea4cf-118">Maximum value possible.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ea4cf-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ea4cf-119">Requirements</span></span>



| <span data-ttu-id="ea4cf-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ea4cf-120">Requirement</span></span> | <span data-ttu-id="ea4cf-121">Wert</span><span class="sxs-lookup"><span data-stu-id="ea4cf-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ea4cf-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ea4cf-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ea4cf-123">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ea4cf-123">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="ea4cf-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ea4cf-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ea4cf-125">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ea4cf-125">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ea4cf-126">Header</span><span class="sxs-lookup"><span data-stu-id="ea4cf-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="ea4cf-127"><dt>Mpclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea4cf-127"><dt>MpClient.h</dt></span></span> </dl> |



 

 





