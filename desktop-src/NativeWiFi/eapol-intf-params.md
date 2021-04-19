---
description: Enthält EAPOL-Konfigurationsparameter.
ms.assetid: 4157a643-86f2-4f6f-8517-6207b11ea9a1
title: EAPOL_INTF_PARAMS Struktur (wzcsapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EAPOL_INTF_PARAMS
api_type:
- HeaderDef
api_location:
- wzcsapi.h
ms.openlocfilehash: dd9e0664fe41b471162beccd31bf2c22fbfa1640
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350290"
---
# <a name="eapol_intf_params-structure"></a><span data-ttu-id="ae42b-103">EAPOL \_ INTF-Parameter \_ Struktur</span><span class="sxs-lookup"><span data-stu-id="ae42b-103">EAPOL\_INTF\_PARAMS structure</span></span>

<span data-ttu-id="ae42b-104">\[**EAPOL \_ INTF \_** -Parameter werden ab Windows Vista und Windows Server 2008 nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ae42b-104">\[**EAPOL\_INTF\_PARAMS** is no longer supported as of Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="ae42b-105">Verwenden Sie stattdessen die [native WiFi-API](native-wifi-reference.md), die eine ähnliche Funktionalität bietet.</span><span class="sxs-lookup"><span data-stu-id="ae42b-105">Instead, use the [Native Wifi API](native-wifi-reference.md), which provides similar functionality.</span></span> <span data-ttu-id="ae42b-106">Weitere Informationen finden Sie unter Informationen zur [nativen WiFi-API](about-the-native-wifi-api.md).\]</span><span class="sxs-lookup"><span data-stu-id="ae42b-106">For more information, see [About the Native Wifi API](about-the-native-wifi-api.md).\]</span></span>

<span data-ttu-id="ae42b-107">Enthält EAPOL-Konfigurationsparameter.</span><span class="sxs-lookup"><span data-stu-id="ae42b-107">Contains EAPOL configuration parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae42b-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="ae42b-108">Syntax</span></span>


```C++
typedef struct _EAPOL_INTF_PARAMS {
  DWORD dwVersion;
  DWORD dwReserved2;
  DWORD dwEapFlags;
  DWORD dwEapType;
  DWORD dwSizeOfSSID;
  BYTE  bSSID[MAX_NETWORK_NAME_LENGTH];
} EAPOL_INTF_PARAMS, *PEAPOL_INTF_PARAMS;
```



## <a name="members"></a><span data-ttu-id="ae42b-109">Member</span><span class="sxs-lookup"><span data-stu-id="ae42b-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="ae42b-110">**dwVersion**</span><span class="sxs-lookup"><span data-stu-id="ae42b-110">**dwVersion**</span></span>
</dt> <dd>

<span data-ttu-id="ae42b-111">Die Version des Aufrufers.</span><span class="sxs-lookup"><span data-stu-id="ae42b-111">Version of the caller.</span></span> <span data-ttu-id="ae42b-112">Standard ist "0".</span><span class="sxs-lookup"><span data-stu-id="ae42b-112">Default is 0.</span></span>

</dd> <dt>

<span data-ttu-id="ae42b-113">**dwReserved2**</span><span class="sxs-lookup"><span data-stu-id="ae42b-113">**dwReserved2**</span></span>
</dt> <dd>

<span data-ttu-id="ae42b-114">Für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="ae42b-114">Reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="ae42b-115">**dbewaffnung-Flags**</span><span class="sxs-lookup"><span data-stu-id="ae42b-115">**dwEapFlags**</span></span>
</dt> <dd>

<span data-ttu-id="ae42b-116">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="ae42b-116">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="ae42b-117">**dbewaffnete-Typ**</span><span class="sxs-lookup"><span data-stu-id="ae42b-117">**dwEapType**</span></span>
</dt> <dd>

<span data-ttu-id="ae42b-118">Der zu verwendende EAP-Erweiterungstyp.</span><span class="sxs-lookup"><span data-stu-id="ae42b-118">The EAP extension type to be used.</span></span> <span data-ttu-id="ae42b-119">Legen Sie auf 0x00000013 für EAP-TLS und 0x00000026 für PEAP fest.</span><span class="sxs-lookup"><span data-stu-id="ae42b-119">Set to 0x00000013 for EAP-TLS and 0x00000026 for PEAP.</span></span>

</dd> <dt>

<span data-ttu-id="ae42b-120">**dwsizeofssid**</span><span class="sxs-lookup"><span data-stu-id="ae42b-120">**dwSizeOfSSID**</span></span>
</dt> <dd>

<span data-ttu-id="ae42b-121">Größe des Netzwerk Bezeichners.</span><span class="sxs-lookup"><span data-stu-id="ae42b-121">Size of network identifier.</span></span>

</dd> <dt>

<span data-ttu-id="ae42b-122">**bSSID**</span><span class="sxs-lookup"><span data-stu-id="ae42b-122">**bSSID**</span></span>
</dt> <dd>

<span data-ttu-id="ae42b-123">Netzwerk Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="ae42b-123">Network identifier.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ae42b-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ae42b-124">Remarks</span></span>

<span data-ttu-id="ae42b-125">Die Header Datei "wzcsapi. h" ist im Windows SDK nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ae42b-125">The header file wzcsapi.h is not available in the Windows SDK.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae42b-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ae42b-126">Requirements</span></span>



| <span data-ttu-id="ae42b-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ae42b-127">Requirement</span></span> | <span data-ttu-id="ae42b-128">Wert</span><span class="sxs-lookup"><span data-stu-id="ae42b-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ae42b-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ae42b-129">Minimum supported client</span></span><br/> | <span data-ttu-id="ae42b-130">Nur Windows XP mit SP2 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ae42b-130">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="ae42b-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ae42b-131">Minimum supported server</span></span><br/> | <span data-ttu-id="ae42b-132">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ae42b-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="ae42b-133">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="ae42b-133">End of client support</span></span><br/>    | <span data-ttu-id="ae42b-134">Windows XP mit SP3</span><span class="sxs-lookup"><span data-stu-id="ae42b-134">Windows XP with SP3</span></span><br/>                                                       |
| <span data-ttu-id="ae42b-135">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="ae42b-135">End of server support</span></span><br/>    | <span data-ttu-id="ae42b-136">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ae42b-136">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="ae42b-137">Header</span><span class="sxs-lookup"><span data-stu-id="ae42b-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="ae42b-138"><dt>Wzcsapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="ae42b-138"><dt>Wzcsapi.h</dt></span></span> </dl> |



 

 




