---
title: Einfache SNMP-Syntax Werte (SNMP. h)
description: Die einfachen SNMP-Syntax Werte werden verwendet, um einen SNMP-Variablentyp anzugeben.
ms.assetid: 42b681e5-721d-4d41-bc1a-c9f0005cde87
topic_type:
- apiref
api_name:
- ASN_INTEGER
- ASN_BITS
- ASN_OCTETSTRING
- ASN_NULL
- ASN_OBJECTIDENTIFIER
- ASN_INTEGER32
api_location:
- Snmp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cee6a40b4f63b7ce701b8232b310b2f73bac42d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104373"
---
# <a name="snmp-simple-syntax-values"></a><span data-ttu-id="5df64-103">Einfache SNMP-Syntax Werte</span><span class="sxs-lookup"><span data-stu-id="5df64-103">SNMP Simple Syntax Values</span></span>

<span data-ttu-id="5df64-104">\[SNMP ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="5df64-104">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="5df64-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="5df64-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="5df64-106">Verwenden Sie stattdessen [Windows-Remoteverwaltung](/windows/desktop/WinRM/portal), bei dem es sich um die Microsoft-Implementierung von WS-man handelt.\]</span><span class="sxs-lookup"><span data-stu-id="5df64-106">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="5df64-107">Die einfachen SNMP-Syntax Werte werden verwendet, um einen SNMP-Variablentyp anzugeben.</span><span class="sxs-lookup"><span data-stu-id="5df64-107">The SNMP Simple Syntax Values are used to indicate an SNMP variable type.</span></span>



| <span data-ttu-id="5df64-108">Konstante</span><span class="sxs-lookup"><span data-stu-id="5df64-108">Constant</span></span>                                                                                                                                                                           | <span data-ttu-id="5df64-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5df64-109">Description</span></span>                                                           |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------|
| <span id="ASN_INTEGER"></span><span id="asn_integer"></span><dl> <span data-ttu-id="5df64-110"><dt>**ASN- \_ Ganzzahl**</dt></span><span class="sxs-lookup"><span data-stu-id="5df64-110"><dt>**ASN\_INTEGER**</dt></span></span> </dl>                            | <span data-ttu-id="5df64-111">Gibt eine 32-Bit-Ganzzahl mit Vorzeichen an.</span><span class="sxs-lookup"><span data-stu-id="5df64-111">Indicates a 32-bit signed integer variable.</span></span><br/>                |
| <span id="ASN_BITS"></span><span id="asn_bits"></span><dl> <span data-ttu-id="5df64-112"><dt>**ASN- \_ Bits**</dt></span><span class="sxs-lookup"><span data-stu-id="5df64-112"><dt>**ASN\_BITS**</dt></span></span> </dl>                                     | <span data-ttu-id="5df64-113">Gibt eine Variable an, die eine Enumeration benannter Bits ist.</span><span class="sxs-lookup"><span data-stu-id="5df64-113">Indicates a variable that is an enumeration of named bits.</span></span><br/> |
| <span id="ASN_OCTETSTRING"></span><span id="asn_octetstring"></span><dl> <span data-ttu-id="5df64-114"><dt>**ASN \_ octetstring**</dt></span><span class="sxs-lookup"><span data-stu-id="5df64-114"><dt>**ASN\_OCTETSTRING**</dt></span></span> </dl>                | <span data-ttu-id="5df64-115">Gibt eine Oktett-Zeichen folgen Variable an.</span><span class="sxs-lookup"><span data-stu-id="5df64-115">Indicates an octet string variable.</span></span><br/>                        |
| <span id="ASN_NULL"></span><span id="asn_null"></span><dl> <span data-ttu-id="5df64-116"><dt>**ASN \_ null**</dt></span><span class="sxs-lookup"><span data-stu-id="5df64-116"><dt>**ASN\_NULL**</dt></span></span> </dl>                                     | <span data-ttu-id="5df64-117">Gibt einen **null** -Wert an.</span><span class="sxs-lookup"><span data-stu-id="5df64-117">Indicates a **NULL** value.</span></span><br/>                                |
| <span id="ASN_OBJECTIDENTIFIER"></span><span id="asn_objectidentifier"></span><dl> <span data-ttu-id="5df64-118"><dt>**ASN- \_ objectidentifier**</dt></span><span class="sxs-lookup"><span data-stu-id="5df64-118"><dt>**ASN\_OBJECTIDENTIFIER**</dt></span></span> </dl> | <span data-ttu-id="5df64-119">Gibt eine objektbezeichnervariable an.</span><span class="sxs-lookup"><span data-stu-id="5df64-119">Indicates an object identifier variable.</span></span><br/>                   |
| <span id="ASN_INTEGER32"></span><span id="asn_integer32"></span><dl> <span data-ttu-id="5df64-120"><dt>**ASN \_ INTEGER32**</dt></span><span class="sxs-lookup"><span data-stu-id="5df64-120"><dt>**ASN\_INTEGER32**</dt></span></span> </dl>                      | <span data-ttu-id="5df64-121">Gibt einen 32-Bit-Ganzzahl mit Vorzeichen an.</span><span class="sxs-lookup"><span data-stu-id="5df64-121">Indicates a 32-bit signed integer value.</span></span><br/>                   |



## <a name="requirements"></a><span data-ttu-id="5df64-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5df64-122">Requirements</span></span>



| <span data-ttu-id="5df64-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5df64-123">Requirement</span></span> | <span data-ttu-id="5df64-124">Wert</span><span class="sxs-lookup"><span data-stu-id="5df64-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="5df64-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5df64-125">Minimum supported client</span></span><br/> | <span data-ttu-id="5df64-126">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5df64-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="5df64-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5df64-127">Minimum supported server</span></span><br/> | <span data-ttu-id="5df64-128">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5df64-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="5df64-129">Header</span><span class="sxs-lookup"><span data-stu-id="5df64-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="5df64-130"><dt>SNMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="5df64-130"><dt>Snmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5df64-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5df64-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5df64-132">Simple Network Management-Protokoll (SNMP) – Übersicht</span><span class="sxs-lookup"><span data-stu-id="5df64-132">Simple Network Management Protocol (SNMP) Overview</span></span>](simple-network-management-protocol-snmp-.md)
</dt> <dt>

[<span data-ttu-id="5df64-133">SNMP-Referenz</span><span class="sxs-lookup"><span data-stu-id="5df64-133">SNMP Reference</span></span>](snmp-reference.md)
</dt> <dt>

[<span data-ttu-id="5df64-134">SNMP-Konstanten</span><span class="sxs-lookup"><span data-stu-id="5df64-134">SNMP Constants</span></span>](snmp-constants.md)
</dt> </dl>

 

