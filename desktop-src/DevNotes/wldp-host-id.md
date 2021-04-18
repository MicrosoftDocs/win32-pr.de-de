---
description: Identifiziert den Hosttyp des wldp-Aufrufers.
ms.assetid: E8E603CC-9CB2-4C3B-9F06-9B06C7B5D752
title: WLDP_HOST_ID-Enumeration (wldp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WLDP_HOST_ID
api_type:
- HeaderDef
api_location:
- wldp.h
ms.openlocfilehash: 8914f93ff5936451b71b855473a09cb1d06584b4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104522923"
---
# <a name="wldp_host_id-enumeration"></a><span data-ttu-id="d9c83-103">Wldp- \_ Host- \_ ID-Enumeration</span><span class="sxs-lookup"><span data-stu-id="d9c83-103">WLDP\_HOST\_ID enumeration</span></span>

<span data-ttu-id="d9c83-104">Identifiziert den Hosttyp des wldp-Aufrufers.</span><span class="sxs-lookup"><span data-stu-id="d9c83-104">Identifies the host type of the WLDP caller.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9c83-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d9c83-105">Syntax</span></span>


```C++
typedef enum _WLDP_HOST_ID { 
   WLDP_HOST_ID_UNKNOWN     = 0,
   WLDP_HOST_ID_GLOBAL      = 1,
  WLDP_HOST_ID_VBA          = 2,
   WLDP_HOST_ID_WSH         = 3,
   WLDP_HOST_ID_POWERSHELL  = 4,
   WLDP_HOST_ID_IE          = 5,
   WLDP_HOST_ID_MSI         = 6,
   WLDP_HOST_ID_MAX         = 7
} WLDP_HOST_ID, *PWLDP_HOST_ID;
```



## <a name="constants"></a><span data-ttu-id="d9c83-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="d9c83-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="d9c83-107"><span id="_WLDP_HOST_ID_UNKNOWN_"></span><span id="_wldp_host_id_unknown_"></span>**Wldp \_ Host- \_ ID \_ unbekannt**</span><span class="sxs-lookup"><span data-stu-id="d9c83-107"><span id="_WLDP_HOST_ID_UNKNOWN_"></span><span id="_wldp_host_id_unknown_"></span> **WLDP\_HOST\_ID\_UNKNOWN**</span></span> 
</dt> <dd>

<span data-ttu-id="d9c83-108">Der Hosttyp ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="d9c83-108">The host type is unknown.</span></span>

</dd> <dt>

<span data-ttu-id="d9c83-109"><span id="_WLDP_HOST_ID_GLOBAL"></span><span id="_wldp_host_id_global"></span>**Wldp \_ Host- \_ ID \_ Global**</span><span class="sxs-lookup"><span data-stu-id="d9c83-109"><span id="_WLDP_HOST_ID_GLOBAL"></span><span id="_wldp_host_id_global"></span> **WLDP\_HOST\_ID\_GLOBAL**</span></span>
</dt> <dd>

<span data-ttu-id="d9c83-110">Der Hosttyp ist eine globale Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="d9c83-110">The host type is global policy.</span></span>

</dd> <dt>

<span data-ttu-id="d9c83-111"><span id="WLDP_HOST_ID_VBA"></span><span id="wldp_host_id_vba"></span>**wldp- \_ Host- \_ ID \_ VBA**</span><span class="sxs-lookup"><span data-stu-id="d9c83-111"><span id="WLDP_HOST_ID_VBA"></span><span id="wldp_host_id_vba"></span>**WLDP\_HOST\_ID\_VBA**</span></span>
</dt> <dd>

<span data-ttu-id="d9c83-112">Der Hosttyp ist "VBScript".</span><span class="sxs-lookup"><span data-stu-id="d9c83-112">The host type is VBScript.</span></span>

</dd> <dt>

<span data-ttu-id="d9c83-113"><span id="_WLDP_HOST_ID_WSH"></span><span id="_wldp_host_id_wsh"></span>**Wldp \_ Host- \_ ID \_ WSH**</span><span class="sxs-lookup"><span data-stu-id="d9c83-113"><span id="_WLDP_HOST_ID_WSH"></span><span id="_wldp_host_id_wsh"></span> **WLDP\_HOST\_ID\_WSH**</span></span>
</dt> <dd>

<span data-ttu-id="d9c83-114">Der Hosttyp ist "Windows Script Host".</span><span class="sxs-lookup"><span data-stu-id="d9c83-114">The host type is Windows Script Host.</span></span>

</dd> <dt>

<span data-ttu-id="d9c83-115"><span id="_WLDP_HOST_ID_POWERSHELL"></span><span id="_wldp_host_id_powershell"></span>**Wldp \_ Host- \_ ID \_ PowerShell**</span><span class="sxs-lookup"><span data-stu-id="d9c83-115"><span id="_WLDP_HOST_ID_POWERSHELL"></span><span id="_wldp_host_id_powershell"></span> **WLDP\_HOST\_ID\_POWERSHELL**</span></span>
</dt> <dd>

<span data-ttu-id="d9c83-116">Der Hosttyp ist Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d9c83-116">The host type is Windows Powershell.</span></span>

</dd> <dt>

<span data-ttu-id="d9c83-117"><span id="_WLDP_HOST_ID_IE"></span><span id="_wldp_host_id_ie"></span>**Wldp \_ Host- \_ ID \_ IE**</span><span class="sxs-lookup"><span data-stu-id="d9c83-117"><span id="_WLDP_HOST_ID_IE"></span><span id="_wldp_host_id_ie"></span> **WLDP\_HOST\_ID\_IE**</span></span>
</dt> <dd>

<span data-ttu-id="d9c83-118">Der Hosttyp ist "Internet Explorer".</span><span class="sxs-lookup"><span data-stu-id="d9c83-118">The host type is Internet Explorer.</span></span>

</dd> <dt>

<span data-ttu-id="d9c83-119"><span id="_WLDP_HOST_ID_MSI"></span><span id="_wldp_host_id_msi"></span>**Wldp \_ Host- \_ ID- \_ MSI**</span><span class="sxs-lookup"><span data-stu-id="d9c83-119"><span id="_WLDP_HOST_ID_MSI"></span><span id="_wldp_host_id_msi"></span> **WLDP\_HOST\_ID\_MSI**</span></span>
</dt> <dd>

<span data-ttu-id="d9c83-120">Der Hosttyp ist der Microsoft Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="d9c83-120">The host type is the Microsoft Windows Installer.</span></span>

</dd> <dt>

<span data-ttu-id="d9c83-121"><span id="_WLDP_HOST_ID_MAX__"></span><span id="_wldp_host_id_max__"></span>**Wldp \_ Host- \_ ID \_ Max**</span><span class="sxs-lookup"><span data-stu-id="d9c83-121"><span id="_WLDP_HOST_ID_MAX__"></span><span id="_wldp_host_id_max__"></span> **WLDP\_HOST\_ID\_MAX**</span></span> 
</dt> <dd>

<span data-ttu-id="d9c83-122">Der maximale Enumerationswert.</span><span class="sxs-lookup"><span data-stu-id="d9c83-122">The maximum enumeration value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d9c83-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d9c83-123">Requirements</span></span>



| <span data-ttu-id="d9c83-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d9c83-124">Requirement</span></span> | <span data-ttu-id="d9c83-125">Wert</span><span class="sxs-lookup"><span data-stu-id="d9c83-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="d9c83-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d9c83-126">Minimum supported client</span></span><br/> | <span data-ttu-id="d9c83-127">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d9c83-127">Windows 8 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d9c83-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d9c83-128">Minimum supported server</span></span><br/> | <span data-ttu-id="d9c83-129">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d9c83-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="d9c83-130">Header</span><span class="sxs-lookup"><span data-stu-id="d9c83-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="d9c83-131"><dt>Wldp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d9c83-131"><dt>Wldp.h</dt></span></span> </dl> |



 

 




