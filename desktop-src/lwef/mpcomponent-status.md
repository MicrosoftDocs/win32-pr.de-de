---
title: MPCOMPONENT_STATUS Struktur (mpclient. h)
description: Informationen zum Komponenten Status.
ms.assetid: 0E589E52-A204-425C-880B-CF13C16893F3
keywords:
- MPCOMPONENT_STATUS Struktur Funktionen der Legacy-Windows-Umgebung
- PMPCOMPONENT_STATUS Struktur Zeiger Legacy-Windows-Umgebungs Features
topic_type:
- apiref
api_name:
- MPCOMPONENT_STATUS
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2923136d2599440bc6ccfe863af9795f7d7ff96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741024"
---
# <a name="mpcomponent_status-structure"></a><span data-ttu-id="03421-105">Mpcomponent- \_ Status Struktur</span><span class="sxs-lookup"><span data-stu-id="03421-105">MPCOMPONENT\_STATUS structure</span></span>

<span data-ttu-id="03421-106">Informationen zum Komponenten Status.</span><span class="sxs-lookup"><span data-stu-id="03421-106">Component status information.</span></span>

## <a name="syntax"></a><span data-ttu-id="03421-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="03421-107">Syntax</span></span>


```C++
typedef struct tagMPCOMPONENT_STATUS {
  BOOL    fEnable;
  HRESULT hResult;
} MPCOMPONENT_STATUS, *PMPCOMPONENT_STATUS;
```



## <a name="members"></a><span data-ttu-id="03421-108">Member</span><span class="sxs-lookup"><span data-stu-id="03421-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="03421-109">**fenckbar**</span><span class="sxs-lookup"><span data-stu-id="03421-109">**fEnable**</span></span>
</dt> <dd>

<span data-ttu-id="03421-110">Typ: **bool**</span><span class="sxs-lookup"><span data-stu-id="03421-110">Type: **BOOL**</span></span>

</dd> <dd>

<span data-ttu-id="03421-111">Der Status der Komponente.</span><span class="sxs-lookup"><span data-stu-id="03421-111">Status for the component.</span></span>

</dd> <dt>

<span data-ttu-id="03421-112">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="03421-112">**hResult**</span></span>
</dt> <dd>

<span data-ttu-id="03421-113">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="03421-113">Type: **HRESULT**</span></span>

</dd> <dd>

<span data-ttu-id="03421-114">Der Status "erfolgreich" oder "Fehlercode".</span><span class="sxs-lookup"><span data-stu-id="03421-114">Success or failure code associated with the status.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="03421-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="03421-115">Requirements</span></span>



| <span data-ttu-id="03421-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="03421-116">Requirement</span></span> | <span data-ttu-id="03421-117">Wert</span><span class="sxs-lookup"><span data-stu-id="03421-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="03421-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="03421-118">Minimum supported client</span></span><br/> | <span data-ttu-id="03421-119">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="03421-119">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="03421-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="03421-120">Minimum supported server</span></span><br/> | <span data-ttu-id="03421-121">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="03421-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="03421-122">Header</span><span class="sxs-lookup"><span data-stu-id="03421-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="03421-123"><dt>Mpclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="03421-123"><dt>MpClient.h</dt></span></span> </dl> |



 

 





