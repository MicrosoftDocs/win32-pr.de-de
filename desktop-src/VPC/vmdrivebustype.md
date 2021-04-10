---
title: Vmdrivebustype-Enumeration (vpccominterfaces. h)
description: Gibt den Bustyp an.
ms.assetid: 7e0926f3-8218-49c9-8d3a-27214c111a77
keywords:
- Vmdrivebustype-Enumeration virtueller PC
topic_type:
- apiref
api_name:
- VMDriveBusType
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c53b8da4b9c7a6943f083eec62a144dcfb5bd68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104265"
---
# <a name="vmdrivebustype-enumeration"></a><span data-ttu-id="201db-104">Vmdrivebustype-Enumeration</span><span class="sxs-lookup"><span data-stu-id="201db-104">VMDriveBusType enumeration</span></span>

<span data-ttu-id="201db-105">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="201db-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="201db-106">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="201db-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="201db-107">Gibt den Bustyp an.</span><span class="sxs-lookup"><span data-stu-id="201db-107">Specifies the type of bus.</span></span>

## <a name="syntax"></a><span data-ttu-id="201db-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="201db-108">Syntax</span></span>


```C++
typedef enum  { 
  vmDriveBusType_Invalid  = -1,
  vmDriveBusType_IDE      = 0,
  vmDriveBusType_SCSI     = 1
} VMDriveBusType;
```



## <a name="constants"></a><span data-ttu-id="201db-109">Konstanten</span><span class="sxs-lookup"><span data-stu-id="201db-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="201db-110"><span id="vmDriveBusType_Invalid"></span><span id="vmdrivebustype_invalid"></span><span id="VMDRIVEBUSTYPE_INVALID"></span>**vmdrivebustype \_ ungültig**</span><span class="sxs-lookup"><span data-stu-id="201db-110"><span id="vmDriveBusType_Invalid"></span><span id="vmdrivebustype_invalid"></span><span id="VMDRIVEBUSTYPE_INVALID"></span>**vmDriveBusType\_Invalid**</span></span>
</dt> <dd>

<span data-ttu-id="201db-111">Kein Bustyp.</span><span class="sxs-lookup"><span data-stu-id="201db-111">No bus type.</span></span>

</dd> <dt>

<span data-ttu-id="201db-112"><span id="vmDriveBusType_IDE"></span><span id="vmdrivebustype_ide"></span><span id="VMDRIVEBUSTYPE_IDE"></span>**vmdrivebustype- \_ IDE**</span><span class="sxs-lookup"><span data-stu-id="201db-112"><span id="vmDriveBusType_IDE"></span><span id="vmdrivebustype_ide"></span><span id="VMDRIVEBUSTYPE_IDE"></span>**vmDriveBusType\_IDE**</span></span>
</dt> <dd>

<span data-ttu-id="201db-113">IDE-Bustyp.</span><span class="sxs-lookup"><span data-stu-id="201db-113">IDE bus type.</span></span>

</dd> <dt>

<span data-ttu-id="201db-114"><span id="vmDriveBusType_SCSI"></span><span id="vmdrivebustype_scsi"></span><span id="VMDRIVEBUSTYPE_SCSI"></span>**vmdrivebustype \_ SCSI**</span><span class="sxs-lookup"><span data-stu-id="201db-114"><span id="vmDriveBusType_SCSI"></span><span id="vmdrivebustype_scsi"></span><span id="VMDRIVEBUSTYPE_SCSI"></span>**vmDriveBusType\_SCSI**</span></span>
</dt> <dd>

<span data-ttu-id="201db-115">Der SCSI-Bustyp.</span><span class="sxs-lookup"><span data-stu-id="201db-115">SCSI bus type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="201db-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="201db-116">Requirements</span></span>



| <span data-ttu-id="201db-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="201db-117">Requirement</span></span> | <span data-ttu-id="201db-118">Wert</span><span class="sxs-lookup"><span data-stu-id="201db-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="201db-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="201db-119">Minimum supported client</span></span><br/> | <span data-ttu-id="201db-120">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="201db-120">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="201db-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="201db-121">Minimum supported server</span></span><br/> | <span data-ttu-id="201db-122">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="201db-122">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="201db-123">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="201db-123">End of client support</span></span><br/>    | <span data-ttu-id="201db-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="201db-124">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="201db-125">Produkt</span><span class="sxs-lookup"><span data-stu-id="201db-125">Product</span></span><br/>                  | <span data-ttu-id="201db-126">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="201db-126">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="201db-127">Header</span><span class="sxs-lookup"><span data-stu-id="201db-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="201db-128"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="201db-128"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



 

