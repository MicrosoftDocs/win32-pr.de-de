---
title: SNMP-Anwendungs Syntax Werte (SNMP. h)
description: Die SNMP-Anwendungs Syntax Werte werden von Verwaltungs Anwendungen verwendet, die die Microsoft SNMP-Verwaltungs-API verwenden.
ms.assetid: fa269f97-f9d3-49f4-b29b-8c4d71f075d0
topic_type:
- apiref
api_name:
- ASN_IPADDRESS
- ASN_COUNTER32
- ASN_GAUGE32
- ASN_TIMETICKS
- ASN_OPAQUE
- ASN_COUNTER64
- ASN_UINTEGER32
- ASN_RFC2578_UNSIGNED32
api_location:
- Snmp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d79ab6535c97fe4124aa1cb3f7ca11ce3eb02582
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103423"
---
# <a name="snmp-application-syntax-values"></a><span data-ttu-id="66232-103">SNMP-Anwendungs Syntax Werte</span><span class="sxs-lookup"><span data-stu-id="66232-103">SNMP Application Syntax Values</span></span>

<span data-ttu-id="66232-104">\[SNMP ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="66232-104">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="66232-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="66232-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="66232-106">Verwenden Sie stattdessen [Windows-Remoteverwaltung](/windows/desktop/WinRM/portal), bei dem es sich um die Microsoft-Implementierung von WS-man handelt.\]</span><span class="sxs-lookup"><span data-stu-id="66232-106">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="66232-107">Die SNMP-Anwendungs Syntax Werte werden von Verwaltungs Anwendungen verwendet, die die Microsoft SNMP-Verwaltungs-API verwenden.</span><span class="sxs-lookup"><span data-stu-id="66232-107">The SNMP Application Syntax Values are used by management applications that employ the Microsoft SNMP Management API.</span></span>



| <span data-ttu-id="66232-108">Konstante</span><span class="sxs-lookup"><span data-stu-id="66232-108">Constant</span></span>                                                                                                                                                                                  | <span data-ttu-id="66232-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="66232-109">Description</span></span>                                                                                                                      |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------|
| <span id="ASN_IPADDRESS"></span><span id="asn_ipaddress"></span><dl> <span data-ttu-id="66232-110"><dt>**ASN- \_ IPAddress**</dt></span><span class="sxs-lookup"><span data-stu-id="66232-110"><dt>**ASN\_IPADDRESS**</dt></span></span> </dl>                             | <span data-ttu-id="66232-111">Gibt eine IP-Adress Variable an.</span><span class="sxs-lookup"><span data-stu-id="66232-111">Indicates an IP address variable.</span></span><br/>                                                                                     |
| <span id="ASN_COUNTER32"></span><span id="asn_counter32"></span><dl> <span data-ttu-id="66232-112"><dt>**ASN \_ COUNTER32**</dt></span><span class="sxs-lookup"><span data-stu-id="66232-112"><dt>**ASN\_COUNTER32**</dt></span></span> </dl>                             | <span data-ttu-id="66232-113">Gibt eine Counter-Variable an.</span><span class="sxs-lookup"><span data-stu-id="66232-113">Indicates a counter variable.</span></span><br/>                                                                                         |
| <span id="ASN_GAUGE32"></span><span id="asn_gauge32"></span><dl> <span data-ttu-id="66232-114"><dt>**ASN \_ GAUGE32**</dt></span><span class="sxs-lookup"><span data-stu-id="66232-114"><dt>**ASN\_GAUGE32**</dt></span></span> </dl>                                   | <span data-ttu-id="66232-115">Gibt eine Messgeräte Variable an.</span><span class="sxs-lookup"><span data-stu-id="66232-115">Indicates a gauge variable.</span></span> <span data-ttu-id="66232-116">Diese Variable beschreibt einen Unsigned32-Typ in Übereinstimmung mit RFC 1902.</span><span class="sxs-lookup"><span data-stu-id="66232-116">This variable describes an Unsigned32 type in conformance with RFC 1902.</span></span><br/>                  |
| <span id="ASN_TIMETICKS"></span><span id="asn_timeticks"></span><dl> <span data-ttu-id="66232-117"><dt>**ASN- \_ TimeTicks**</dt></span><span class="sxs-lookup"><span data-stu-id="66232-117"><dt>**ASN\_TIMETICKS**</dt></span></span> </dl>                             | <span data-ttu-id="66232-118">Gibt eine TimeTicks-Variable an.</span><span class="sxs-lookup"><span data-stu-id="66232-118">Indicates a timeticks variable.</span></span><br/>                                                                                       |
| <span id="ASN_OPAQUE"></span><span id="asn_opaque"></span><dl> <span data-ttu-id="66232-119"><dt>**ASN \_ nicht transparent**</dt></span><span class="sxs-lookup"><span data-stu-id="66232-119"><dt>**ASN\_OPAQUE**</dt></span></span> </dl>                                      | <span data-ttu-id="66232-120">Gibt eine nicht transparente Variable an.</span><span class="sxs-lookup"><span data-stu-id="66232-120">Indicates an opaque variable.</span></span><br/>                                                                                         |
| <span id="ASN_COUNTER64"></span><span id="asn_counter64"></span><dl> <span data-ttu-id="66232-121"><dt>**ASN \_ COUNTER64**</dt></span><span class="sxs-lookup"><span data-stu-id="66232-121"><dt>**ASN\_COUNTER64**</dt></span></span> </dl>                             | <span data-ttu-id="66232-122">Gibt eine-Counter-Variable an, die zunimmt, bis Sie den maximalen Wert erreicht (2 ^ 64)-1.</span><span class="sxs-lookup"><span data-stu-id="66232-122">Indicates a counter variable that increases until it reaches a maximum value of (2^64) - 1.</span></span><br/>                           |
| <span id="ASN_UINTEGER32"></span><span id="asn_uinteger32"></span><dl> <span data-ttu-id="66232-123"><dt>**ASN \_ UINTEGER32**</dt></span><span class="sxs-lookup"><span data-stu-id="66232-123"><dt>**ASN\_UINTEGER32**</dt></span></span> </dl>                          | <span data-ttu-id="66232-124">Gibt eine 32-Bit-Ganzzahl ohne Vorzeichen an.</span><span class="sxs-lookup"><span data-stu-id="66232-124">Indicates a 32-bit unsigned integer variable.</span></span> <span data-ttu-id="66232-125">Diese Variable beschreibt einen UInteger32-Typ in Übereinstimmung mit RFC 1442.</span><span class="sxs-lookup"><span data-stu-id="66232-125">This variable describes a UInteger32 type in conformance with RFC 1442.</span></span><br/> |
| <span id="ASN_RFC2578_UNSIGNED32"></span><span id="asn_rfc2578_unsigned32"></span><dl> <span data-ttu-id="66232-126"><dt>**ASN \_ RFC2578 \_ UNSIGNED32**</dt></span><span class="sxs-lookup"><span data-stu-id="66232-126"><dt>**ASN\_RFC2578\_UNSIGNED32**</dt></span></span> </dl> | <span data-ttu-id="66232-127">Siehe ASN \_ GAUGE32.</span><span class="sxs-lookup"><span data-stu-id="66232-127">See ASN\_GAUGE32.</span></span><br/>                                                                                                     |



## <a name="requirements"></a><span data-ttu-id="66232-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="66232-128">Requirements</span></span>



| <span data-ttu-id="66232-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="66232-129">Requirement</span></span> | <span data-ttu-id="66232-130">Wert</span><span class="sxs-lookup"><span data-stu-id="66232-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="66232-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="66232-131">Minimum supported client</span></span><br/> | <span data-ttu-id="66232-132">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="66232-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="66232-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="66232-133">Minimum supported server</span></span><br/> | <span data-ttu-id="66232-134">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="66232-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="66232-135">Header</span><span class="sxs-lookup"><span data-stu-id="66232-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="66232-136"><dt>SNMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="66232-136"><dt>Snmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66232-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="66232-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66232-138">Simple Network Management-Protokoll (SNMP) – Übersicht</span><span class="sxs-lookup"><span data-stu-id="66232-138">Simple Network Management Protocol (SNMP) Overview</span></span>](simple-network-management-protocol-snmp-.md)
</dt> <dt>

[<span data-ttu-id="66232-139">SNMP-Referenz</span><span class="sxs-lookup"><span data-stu-id="66232-139">SNMP Reference</span></span>](snmp-reference.md)
</dt> <dt>

[<span data-ttu-id="66232-140">SNMP-Konstanten</span><span class="sxs-lookup"><span data-stu-id="66232-140">SNMP Constants</span></span>](snmp-constants.md)
</dt> </dl>

 

