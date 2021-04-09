---
title: MPRESOLVED_REASON-Enumeration (mpclient. h)
description: Mögliche Gründe für das Auflösen eines Fehlers bei der Behebung.
ms.assetid: 29E875D7-97DA-4129-AB71-B261CD0E682A
keywords:
- MPRESOLVED_REASON-Enumerationsfunktionen der Legacy-Windows-Umgebung
- PMPRESOLVED_REASON enumerationszeiger Legacy-Windows-Umgebungs Features
topic_type:
- apiref
api_name:
- MPRESOLVED_REASON
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab31fc8b734852ccdf15278f535d916228b43976
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040773"
---
# <a name="mpresolved_reason-enumeration"></a><span data-ttu-id="c1838-105">Mpregelöste \_ reason-Enumeration</span><span class="sxs-lookup"><span data-stu-id="c1838-105">MPRESOLVED\_REASON enumeration</span></span>

<span data-ttu-id="c1838-106">Mögliche Gründe für das Auflösen eines Fehlers bei der Behebung.</span><span class="sxs-lookup"><span data-stu-id="c1838-106">Possible reasons for a remediation failure being resolved.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1838-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c1838-107">Syntax</span></span>


```C++
typedef enum tagMPRESOLVED_REASON { 
  MPRESOLVED_REASON_UNKNOWN    = 0,
  MPRESOLVED_REASON_FULL_SCAN  = 1,
  MPRESOLVED_REASON_TIMED_OUT  = 2
} MPRESOLVED_REASON, *PMPRESOLVED_REASON;
```



## <a name="constants"></a><span data-ttu-id="c1838-108">Konstanten</span><span class="sxs-lookup"><span data-stu-id="c1838-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="c1838-109"><span id="MPRESOLVED_REASON_UNKNOWN"></span><span id="mpresolved_reason_unknown"></span>**mpregelösten \_ Grund \_ unbekannt**</span><span class="sxs-lookup"><span data-stu-id="c1838-109"><span id="MPRESOLVED_REASON_UNKNOWN"></span><span id="mpresolved_reason_unknown"></span>**MPRESOLVED\_REASON\_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="c1838-110">In einem Fehlerzustand.</span><span class="sxs-lookup"><span data-stu-id="c1838-110">In an error state.</span></span>

</dd> <dt>

<span data-ttu-id="c1838-111"><span id="MPRESOLVED_REASON_FULL_SCAN"></span><span id="mpresolved_reason_full_scan"></span>**mpregelöste \_ Grund für \_ vollständige \_ Überprüfung**</span><span class="sxs-lookup"><span data-stu-id="c1838-111"><span id="MPRESOLVED_REASON_FULL_SCAN"></span><span id="mpresolved_reason_full_scan"></span>**MPRESOLVED\_REASON\_FULL\_SCAN**</span></span>
</dt> <dd>

<span data-ttu-id="c1838-112">Es wurde eine vollständige Überprüfung durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="c1838-112">A full scan was performed.</span></span>

</dd> <dt>

<span data-ttu-id="c1838-113"><span id="MPRESOLVED_REASON_TIMED_OUT"></span><span id="mpresolved_reason_timed_out"></span>**mpregelösten \_ Grund Zeitüberschreitung \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c1838-113"><span id="MPRESOLVED_REASON_TIMED_OUT"></span><span id="mpresolved_reason_timed_out"></span>**MPRESOLVED\_REASON\_TIMED\_OUT**</span></span>
</dt> <dd>

<span data-ttu-id="c1838-114">Genügend Zeit vergangen.</span><span class="sxs-lookup"><span data-stu-id="c1838-114">Enough time has passed.</span></span> <span data-ttu-id="c1838-115">Der Standardwert ist eine Woche.</span><span class="sxs-lookup"><span data-stu-id="c1838-115">The default is one week.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c1838-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c1838-116">Requirements</span></span>



| <span data-ttu-id="c1838-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c1838-117">Requirement</span></span> | <span data-ttu-id="c1838-118">Wert</span><span class="sxs-lookup"><span data-stu-id="c1838-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c1838-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c1838-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c1838-120">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c1838-120">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="c1838-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c1838-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c1838-122">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c1838-122">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c1838-123">Header</span><span class="sxs-lookup"><span data-stu-id="c1838-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1838-124"><dt>Mpclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="c1838-124"><dt>MpClient.h</dt></span></span> </dl> |



 

 





