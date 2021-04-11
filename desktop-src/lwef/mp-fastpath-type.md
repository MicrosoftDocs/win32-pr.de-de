---
title: MP_FASTPATH_TYPE-Enumeration (mpclient. h)
description: FastPath-Typ.
ms.assetid: BD72228F-DCC0-435E-A408-BD7FB02E55E1
keywords:
- MP_FASTPATH_TYPE-Enumerationsfunktionen der Legacy-Windows-Umgebung
- PMP_FASTPATH_TYPE enumerationszeiger Legacy-Windows-Umgebungs Features
topic_type:
- apiref
api_name:
- MP_FASTPATH_TYPE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e89db79c54b166a833369ff52e47473463e0a2b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105777"
---
# <a name="mp_fastpath_type-enumeration"></a><span data-ttu-id="45b14-105">MP- \_ FastPath- \_ Typenumeration</span><span class="sxs-lookup"><span data-stu-id="45b14-105">MP\_FASTPATH\_TYPE enumeration</span></span>

<span data-ttu-id="45b14-106">FastPath-Typ.</span><span class="sxs-lookup"><span data-stu-id="45b14-106">FastPath type.</span></span>

## <a name="syntax"></a><span data-ttu-id="45b14-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="45b14-107">Syntax</span></span>


```C++
typedef enum tagMP_FASTPATH_TYPE { 
  MP_FASTPATH_UNKNOWN   = 0,
  MP_FASTPATH_VDM       = 1,
  MP_FASTPATH_DISABLED  = 2
} MP_FASTPATH_TYPE, *PMP_FASTPATH_TYPE;
```



## <a name="constants"></a><span data-ttu-id="45b14-108">Konstanten</span><span class="sxs-lookup"><span data-stu-id="45b14-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="45b14-109"><span id="MP_FASTPATH_UNKNOWN"></span><span id="mp_fastpath_unknown"></span>**MP- \_ FastPath \_ unbekannt**</span><span class="sxs-lookup"><span data-stu-id="45b14-109"><span id="MP_FASTPATH_UNKNOWN"></span><span id="mp_fastpath_unknown"></span>**MP\_FASTPATH\_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="45b14-110">Unbekannt</span><span class="sxs-lookup"><span data-stu-id="45b14-110">Unknown.</span></span>

</dd> <dt>

<span data-ttu-id="45b14-111"><span id="MP_FASTPATH_VDM"></span><span id="mp_fastpath_vdm"></span>**MP \_ FastPath \_ VDM**</span><span class="sxs-lookup"><span data-stu-id="45b14-111"><span id="MP_FASTPATH_VDM"></span><span id="mp_fastpath_vdm"></span>**MP\_FASTPATH\_VDM**</span></span>
</dt> <dd>

<span data-ttu-id="45b14-112">VDM-Update.</span><span class="sxs-lookup"><span data-stu-id="45b14-112">VDM update.</span></span>

</dd> <dt>

<span data-ttu-id="45b14-113"><span id="MP_FASTPATH_DISABLED"></span><span id="mp_fastpath_disabled"></span>**MP- \_ FastPath \_ deaktiviert**</span><span class="sxs-lookup"><span data-stu-id="45b14-113"><span id="MP_FASTPATH_DISABLED"></span><span id="mp_fastpath_disabled"></span>**MP\_FASTPATH\_DISABLED**</span></span>
</dt> <dd>

<span data-ttu-id="45b14-114">Benachrichtigung zur Deaktivierung der Signatur.</span><span class="sxs-lookup"><span data-stu-id="45b14-114">Signature disable notification.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="45b14-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="45b14-115">Requirements</span></span>



| <span data-ttu-id="45b14-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="45b14-116">Requirement</span></span> | <span data-ttu-id="45b14-117">Wert</span><span class="sxs-lookup"><span data-stu-id="45b14-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="45b14-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="45b14-118">Minimum supported client</span></span><br/> | <span data-ttu-id="45b14-119">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="45b14-119">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="45b14-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="45b14-120">Minimum supported server</span></span><br/> | <span data-ttu-id="45b14-121">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="45b14-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="45b14-122">Header</span><span class="sxs-lookup"><span data-stu-id="45b14-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="45b14-123"><dt>Mpclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="45b14-123"><dt>MpClient.h</dt></span></span> </dl> |



 

 





