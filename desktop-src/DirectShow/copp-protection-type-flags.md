---
description: Die folgenden Konstanten werden mit dem Certified Output Protection Protocol (COPP) für bestimmte Mechanismen zum Schutz von-Mechanismen verwendet.
ms.assetid: a3cd63d8-22a5-473c-83c2-3499f3d32671
title: COPP-Schutztyp Flags (DXVA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COPP_ProtectionType_Unknown
- COPP_ProtectionType_None
- COPP_ProtectionType_HDCP
- COPP_ProtectionType_ACP
- COPP_ProtectionType_CGMSA
- COPP_ProtectionType_Mask
- COPP_ProtectionType_Reserved
api_type:
- HeaderDef
api_location:
- dxva.h
ms.openlocfilehash: 57e9ccc9420659ac09c19f2bbb7a18db519c07bc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365421"
---
# <a name="copp-protection-type-flags"></a><span data-ttu-id="e8727-103">COPP-Schutztyp Flags</span><span class="sxs-lookup"><span data-stu-id="e8727-103">COPP Protection Type Flags</span></span>

<span data-ttu-id="e8727-104">Die folgenden Konstanten werden mit dem Certified Output Protection Protocol (COPP) für bestimmte Mechanismen zum Schutz von-Mechanismen verwendet.</span><span class="sxs-lookup"><span data-stu-id="e8727-104">The follow constants are used with Certified Output Protection Protocol (COPP) to specific output protection mechanisms.</span></span>



| <span data-ttu-id="e8727-105">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="e8727-105">Constant/value</span></span>                                                                                                                                                                                                                                                                                                             | <span data-ttu-id="e8727-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e8727-106">Description</span></span>                                                     |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------|
| <span id="COPP_ProtectionType_Unknown"></span><span id="copp_protectiontype_unknown"></span><span id="COPP_PROTECTIONTYPE_UNKNOWN"></span><dl> <span data-ttu-id="e8727-107"><dt>**COPP \_ Schutztyp \_ unbekannt**</dt> <dt>0x80000000</dt></span><span class="sxs-lookup"><span data-stu-id="e8727-107"><dt>**COPP\_ProtectionType\_Unknown**</dt> <dt>0x80000000</dt></span></span> </dl>     | <span data-ttu-id="e8727-108">Unbekannter Schutzmechanismus.</span><span class="sxs-lookup"><span data-stu-id="e8727-108">Unknown protection mechanism.</span></span><br/>                        |
| <span id="COPP_ProtectionType_None"></span><span id="copp_protectiontype_none"></span><span id="COPP_PROTECTIONTYPE_NONE"></span><dl> <span data-ttu-id="e8727-109"><dt>**COPP \_ Schutztyp \_ None**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="e8727-109"><dt>**COPP\_ProtectionType\_None**</dt> <dt>0x00000000</dt></span></span> </dl>                 | <span data-ttu-id="e8727-110">Keine Schutzmechanismen.</span><span class="sxs-lookup"><span data-stu-id="e8727-110">No protection mechanisms.</span></span><br/>                            |
| <span id="COPP_ProtectionType_HDCP"></span><span id="copp_protectiontype_hdcp"></span><span id="COPP_PROTECTIONTYPE_HDCP"></span><dl> <span data-ttu-id="e8727-111"><dt>**COPP \_ Schutztyp \_ HDCP**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="e8727-111"><dt>**COPP\_ProtectionType\_HDCP**</dt> <dt>0x00000001</dt></span></span> </dl>                 | <span data-ttu-id="e8727-112">High-Bandwidth Digital Content Protection (HDCP).</span><span class="sxs-lookup"><span data-stu-id="e8727-112">High-Bandwidth Digital Content Protection (HDCP).</span></span><br/>    |
| <span id="COPP_ProtectionType_ACP"></span><span id="copp_protectiontype_acp"></span><span id="COPP_PROTECTIONTYPE_ACP"></span><dl> <span data-ttu-id="e8727-113"><dt>**COPP \_ Schutztyp \_ ACP**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="e8727-113"><dt>**COPP\_ProtectionType\_ACP**</dt> <dt>0x00000002</dt></span></span> </dl>                     | <span data-ttu-id="e8727-114">Der Schutz von analogen Kopien (ACP).</span><span class="sxs-lookup"><span data-stu-id="e8727-114">Analog Copy Protection (ACP).</span></span><br/>                        |
| <span id="COPP_ProtectionType_CGMSA"></span><span id="copp_protectiontype_cgmsa"></span><span id="COPP_PROTECTIONTYPE_CGMSA"></span><dl> <span data-ttu-id="e8727-115"><dt>**COPP \_ Schutztype \_ cgmsa**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="e8727-115"><dt>**COPP\_ProtectionType\_CGMSA**</dt> <dt>0x00000004</dt></span></span> </dl>             | <span data-ttu-id="e8727-116">Copy Generation Management System Analog (CGMS-A).</span><span class="sxs-lookup"><span data-stu-id="e8727-116">Copy Generation Management System   Analog (CGMS-A).</span></span><br/> |
| <span id="COPP_ProtectionType_Mask"></span><span id="copp_protectiontype_mask"></span><span id="COPP_PROTECTIONTYPE_MASK"></span><dl> <span data-ttu-id="e8727-117"><dt>**COPP \_ Schutztyp \_ Maske**</dt> <dt>0x80000007</dt></span><span class="sxs-lookup"><span data-stu-id="e8727-117"><dt>**COPP\_ProtectionType\_Mask**</dt> <dt>0x80000007</dt></span></span> </dl>                 | <span data-ttu-id="e8727-118">Bitmaske, um gültige Flags zu isolieren.</span><span class="sxs-lookup"><span data-stu-id="e8727-118">Bitmask to isolate valid flags.</span></span><br/>                      |
| <span id="COPP_ProtectionType_Reserved"></span><span id="copp_protectiontype_reserved"></span><span id="COPP_PROTECTIONTYPE_RESERVED"></span><dl> <span data-ttu-id="e8727-119"><dt>**COPP \_ Schutztyp \_ reserviert**</dt> <dt>0x7ffffff8</dt></span><span class="sxs-lookup"><span data-stu-id="e8727-119"><dt>**COPP\_ProtectionType\_Reserved**</dt> <dt>0x7FFFFFF8</dt></span></span> </dl> | <span data-ttu-id="e8727-120">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="e8727-120">Reserved.</span></span> <span data-ttu-id="e8727-121">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="e8727-121">Must be zero.</span></span><br/>                              |



## <a name="remarks"></a><span data-ttu-id="e8727-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e8727-122">Remarks</span></span>

<span data-ttu-id="e8727-123">Einige Methoden geben ein einzelnes Flag von diesem Enumerationstyp zurück, und einige Methoden geben ein bitweises **or** von einem oder mehreren Flags zurück.</span><span class="sxs-lookup"><span data-stu-id="e8727-123">Some methods return a single flag from this enumeration type, and some methods return a bitwise **OR** of one or more flags.</span></span>

<span data-ttu-id="e8727-124">Diese Flags werden in den folgenden COPP-Abfragen und-Befehlen verwendet.</span><span class="sxs-lookup"><span data-stu-id="e8727-124">These flags are used in the following COPP queries and commands.</span></span>

-   <span data-ttu-id="e8727-125">Globale Schutz Ebene</span><span class="sxs-lookup"><span data-stu-id="e8727-125">Global Protection Level</span></span>
-   <span data-ttu-id="e8727-126">Lokale Schutz Ebene</span><span class="sxs-lookup"><span data-stu-id="e8727-126">Local Protection Level</span></span>
-   <span data-ttu-id="e8727-127">Schutztyp</span><span class="sxs-lookup"><span data-stu-id="e8727-127">Protection Type</span></span>
-   <span data-ttu-id="e8727-128">Schutz Ebene festlegen</span><span class="sxs-lookup"><span data-stu-id="e8727-128">Set Protection Level</span></span>

## <a name="requirements"></a><span data-ttu-id="e8727-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e8727-129">Requirements</span></span>



| <span data-ttu-id="e8727-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e8727-130">Requirement</span></span> | <span data-ttu-id="e8727-131">Wert</span><span class="sxs-lookup"><span data-stu-id="e8727-131">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="e8727-132">Header</span><span class="sxs-lookup"><span data-stu-id="e8727-132">Header</span></span><br/> | <dl> <span data-ttu-id="e8727-133"><dt>DXVA. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8727-133"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8727-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e8727-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8727-135">Konstanten und GUIDs</span><span class="sxs-lookup"><span data-stu-id="e8727-135">Constants and GUIDs</span></span>](constants-and-guids.md)
</dt> <dt>

[<span data-ttu-id="e8727-136">Verwenden des Certified Output Protection-Protokolls (COPP)</span><span class="sxs-lookup"><span data-stu-id="e8727-136">Using Certified Output Protection Protocol (COPP)</span></span>](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 




