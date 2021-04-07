---
description: Gibt die Member der nmcolumnvariant-Struktur an.
ms.assetid: 29363341-f4d3-43c3-a523-45402174cb74
title: Nmcolumntype-Enumeration (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NMCOLUMNTYPE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 3c88d001ce3ccf1ebfe1e28855ae9df9fca5d327
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760123"
---
# <a name="nmcolumntype-enumeration"></a><span data-ttu-id="a1667-103">Nmcolumntype-Enumeration</span><span class="sxs-lookup"><span data-stu-id="a1667-103">NMCOLUMNTYPE enumeration</span></span>

<span data-ttu-id="a1667-104">Die **nmcolumntype** -Enumeration gibt die Member der [**nmcolumnvariant**](nmcolumnvariant.md) -Struktur an.</span><span class="sxs-lookup"><span data-stu-id="a1667-104">The **NMCOLUMNTYPE** enumeration specifies the members of the [**NMCOLUMNVARIANT**](nmcolumnvariant.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1667-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a1667-105">Syntax</span></span>


```C++
typedef enum  { 
  NMCOLUMNTYPE_UINT8      = 0,
  NMCOLUMNTYPE_SINT8,
  NMCOLUMNTYPE_UINT16,
  NMCOLUMNTYPE_SINT16,
  NMCOLUMNTYPE_UINT32,
  NMCOLUMNTYPE_SINT32,
  NMCOLUMNTYPE_FLOAT64,
  NMCOLUMNTYPE_FRAME,
  NMCOLUMNTYPE_YESNO,
  NMCOLUMNTYPE_ONOFF,
  NMCOLUMNTYPE_TRUEFALSE,
  NMCOLUMNTYPE_MACADDR,
  NMCOLUMNTYPE_IPXADDR,
  NMCOLUMNTYPE_IPADDR,
  NMCOLUMNTYPE_VARTIME,
  NMCOLUMNTYPE_STRING
} NMCOLUMNTYPE;
```



## <a name="constants"></a><span data-ttu-id="a1667-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="a1667-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="a1667-107"><span id="NMCOLUMNTYPE_UINT8"></span><span id="nmcolumntype_uint8"></span>**Nmcolumntype \_ Uint8**</span><span class="sxs-lookup"><span data-stu-id="a1667-107"><span id="NMCOLUMNTYPE_UINT8"></span><span id="nmcolumntype_uint8"></span>**NMCOLUMNTYPE\_UINT8**</span></span>
</dt> <dd>

<span data-ttu-id="a1667-108">8-Bit-Ganzzahl ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="a1667-108">8-bit unsigned integer.</span></span>

</dd> <dt>

<span data-ttu-id="a1667-109"><span id="NMCOLUMNTYPE_SINT8"></span><span id="nmcolumntype_sint8"></span>**Nmcolumntype \_ SINT8**</span><span class="sxs-lookup"><span data-stu-id="a1667-109"><span id="NMCOLUMNTYPE_SINT8"></span><span id="nmcolumntype_sint8"></span>**NMCOLUMNTYPE\_SINT8**</span></span>
</dt> <dd>

<span data-ttu-id="a1667-110">8-Bit-Ganzzahl mit Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="a1667-110">8-bit signed integer.</span></span>

</dd> <dt>

<span data-ttu-id="a1667-111"><span id="NMCOLUMNTYPE_UINT16"></span><span id="nmcolumntype_uint16"></span>**Nmcolumntype \_ UInt16**</span><span class="sxs-lookup"><span data-stu-id="a1667-111"><span id="NMCOLUMNTYPE_UINT16"></span><span id="nmcolumntype_uint16"></span>**NMCOLUMNTYPE\_UINT16**</span></span>
</dt> <dd>

<span data-ttu-id="a1667-112">16-Bit-Ganzzahl ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="a1667-112">16-bit unsigned integer.</span></span>

</dd> <dt>

<span data-ttu-id="a1667-113"><span id="NMCOLUMNTYPE_SINT16"></span><span id="nmcolumntype_sint16"></span>**Nmcolumntype \_ SINT16**</span><span class="sxs-lookup"><span data-stu-id="a1667-113"><span id="NMCOLUMNTYPE_SINT16"></span><span id="nmcolumntype_sint16"></span>**NMCOLUMNTYPE\_SINT16**</span></span>
</dt> <dd>

<span data-ttu-id="a1667-114">16-Bit-Ganzzahl mit Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="a1667-114">16-bit signed integer.</span></span>

</dd> <dt>

<span data-ttu-id="a1667-115"><span id="NMCOLUMNTYPE_UINT32"></span><span id="nmcolumntype_uint32"></span>**Nmcolumntype \_ UInt32**</span><span class="sxs-lookup"><span data-stu-id="a1667-115"><span id="NMCOLUMNTYPE_UINT32"></span><span id="nmcolumntype_uint32"></span>**NMCOLUMNTYPE\_UINT32**</span></span>
</dt> <dd>

<span data-ttu-id="a1667-116">32-Bit-Ganzzahl ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="a1667-116">32-bit unsigned integer.</span></span>

</dd> <dt>

<span data-ttu-id="a1667-117"><span id="NMCOLUMNTYPE_SINT32"></span><span id="nmcolumntype_sint32"></span>**Nmcolumntype \_ SINT32**</span><span class="sxs-lookup"><span data-stu-id="a1667-117"><span id="NMCOLUMNTYPE_SINT32"></span><span id="nmcolumntype_sint32"></span>**NMCOLUMNTYPE\_SINT32**</span></span>
</dt> <dd>

<span data-ttu-id="a1667-118">Ganze 32-Bit-Zahl mit Vorzeichen:</span><span class="sxs-lookup"><span data-stu-id="a1667-118">32-bit signed integer.</span></span>

</dd> <dt>

<span data-ttu-id="a1667-119"><span id="NMCOLUMNTYPE_FLOAT64"></span><span id="nmcolumntype_float64"></span>**Nmcolumntype \_ float64**</span><span class="sxs-lookup"><span data-stu-id="a1667-119"><span id="NMCOLUMNTYPE_FLOAT64"></span><span id="nmcolumntype_float64"></span>**NMCOLUMNTYPE\_FLOAT64**</span></span>
</dt> <dd>

<span data-ttu-id="a1667-120">64-Bit Float.</span><span class="sxs-lookup"><span data-stu-id="a1667-120">64-bit float.</span></span>

</dd> <dt>

<span data-ttu-id="a1667-121"><span id="NMCOLUMNTYPE_FRAME"></span><span id="nmcolumntype_frame"></span>**nmcolumntype- \_ Frame**</span><span class="sxs-lookup"><span data-stu-id="a1667-121"><span id="NMCOLUMNTYPE_FRAME"></span><span id="nmcolumntype_frame"></span>**NMCOLUMNTYPE\_FRAME**</span></span>
</dt> <dd>

<span data-ttu-id="a1667-122">Frame Nummer.</span><span class="sxs-lookup"><span data-stu-id="a1667-122">Frame number.</span></span>

</dd> <dt>

<span data-ttu-id="a1667-123"><span id="NMCOLUMNTYPE_YESNO"></span><span id="nmcolumntype_yesno"></span>**nmcolumntype \_ YesNo**</span><span class="sxs-lookup"><span data-stu-id="a1667-123"><span id="NMCOLUMNTYPE_YESNO"></span><span id="nmcolumntype_yesno"></span>**NMCOLUMNTYPE\_YESNO**</span></span>
</dt> <dd>

<span data-ttu-id="a1667-124">"Yes" oder "No".</span><span class="sxs-lookup"><span data-stu-id="a1667-124">"Yes" or "No".</span></span>

</dd> <dt>

<span data-ttu-id="a1667-125"><span id="NMCOLUMNTYPE_ONOFF"></span><span id="nmcolumntype_onoff"></span>**nmcolumntype \_ onoff**</span><span class="sxs-lookup"><span data-stu-id="a1667-125"><span id="NMCOLUMNTYPE_ONOFF"></span><span id="nmcolumntype_onoff"></span>**NMCOLUMNTYPE\_ONOFF**</span></span>
</dt> <dd>

<span data-ttu-id="a1667-126">"On" oder "Off"</span><span class="sxs-lookup"><span data-stu-id="a1667-126">"On" or "Off"</span></span>

</dd> <dt>

<span data-ttu-id="a1667-127"><span id="NMCOLUMNTYPE_TRUEFALSE"></span><span id="nmcolumntype_truefalse"></span>**nmcolumntype \_ truefalse**</span><span class="sxs-lookup"><span data-stu-id="a1667-127"><span id="NMCOLUMNTYPE_TRUEFALSE"></span><span id="nmcolumntype_truefalse"></span>**NMCOLUMNTYPE\_TRUEFALSE**</span></span>
</dt> <dd>

<span data-ttu-id="a1667-128">"True" oder "false".</span><span class="sxs-lookup"><span data-stu-id="a1667-128">"True" or "False".</span></span>

</dd> <dt>

<span data-ttu-id="a1667-129"><span id="NMCOLUMNTYPE_MACADDR"></span><span id="nmcolumntype_macaddr"></span>**nmcolumntype \_ MACADDR**</span><span class="sxs-lookup"><span data-stu-id="a1667-129"><span id="NMCOLUMNTYPE_MACADDR"></span><span id="nmcolumntype_macaddr"></span>**NMCOLUMNTYPE\_MACADDR**</span></span>
</dt> <dd>

<span data-ttu-id="a1667-130">MAC-Adresse</span><span class="sxs-lookup"><span data-stu-id="a1667-130">MAC address.</span></span>

</dd> <dt>

<span data-ttu-id="a1667-131"><span id="NMCOLUMNTYPE_IPXADDR"></span><span id="nmcolumntype_ipxaddr"></span>**nmcolumntype \_ ipxaddr**</span><span class="sxs-lookup"><span data-stu-id="a1667-131"><span id="NMCOLUMNTYPE_IPXADDR"></span><span id="nmcolumntype_ipxaddr"></span>**NMCOLUMNTYPE\_IPXADDR**</span></span>
</dt> <dd>

<span data-ttu-id="a1667-132">IPX-Adresse</span><span class="sxs-lookup"><span data-stu-id="a1667-132">IPX address.</span></span>

</dd> <dt>

<span data-ttu-id="a1667-133"><span id="NMCOLUMNTYPE_IPADDR"></span><span id="nmcolumntype_ipaddr"></span>**nmcolumntype \_ ipaddr**</span><span class="sxs-lookup"><span data-stu-id="a1667-133"><span id="NMCOLUMNTYPE_IPADDR"></span><span id="nmcolumntype_ipaddr"></span>**NMCOLUMNTYPE\_IPADDR**</span></span>
</dt> <dd>

<span data-ttu-id="a1667-134">IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="a1667-134">IP address.</span></span>

</dd> <dt>

<span data-ttu-id="a1667-135"><span id="NMCOLUMNTYPE_VARTIME"></span><span id="nmcolumntype_vartime"></span>**nmcolumntype \_ vartime**</span><span class="sxs-lookup"><span data-stu-id="a1667-135"><span id="NMCOLUMNTYPE_VARTIME"></span><span id="nmcolumntype_vartime"></span>**NMCOLUMNTYPE\_VARTIME**</span></span>
</dt> <dd>

<span data-ttu-id="a1667-136">Variant-Zeit.</span><span class="sxs-lookup"><span data-stu-id="a1667-136">Variant time.</span></span>

</dd> <dt>

<span data-ttu-id="a1667-137"><span id="NMCOLUMNTYPE_STRING"></span><span id="nmcolumntype_string"></span>**nmcolumntype- \_ Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a1667-137"><span id="NMCOLUMNTYPE_STRING"></span><span id="nmcolumntype_string"></span>**NMCOLUMNTYPE\_STRING**</span></span>
</dt> <dd>

<span data-ttu-id="a1667-138">Zeiger auf eine Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="a1667-138">Pointer to a string.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a1667-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a1667-139">Requirements</span></span>



| <span data-ttu-id="a1667-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a1667-140">Requirement</span></span> | <span data-ttu-id="a1667-141">Wert</span><span class="sxs-lookup"><span data-stu-id="a1667-141">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a1667-142">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a1667-142">Minimum supported client</span></span><br/> | <span data-ttu-id="a1667-143">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a1667-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="a1667-144">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a1667-144">Minimum supported server</span></span><br/> | <span data-ttu-id="a1667-145">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a1667-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="a1667-146">Header</span><span class="sxs-lookup"><span data-stu-id="a1667-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="a1667-147"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="a1667-147"><dt>Netmon.h</dt></span></span> </dl> |



 

 




