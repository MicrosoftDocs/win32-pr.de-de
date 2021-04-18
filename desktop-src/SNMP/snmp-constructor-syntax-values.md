---
title: SNMP-Konstruktorsyntax Werte (SNMP. h)
description: In den SNMP-Konstruktorsyntax Werten werden Typen beschrieben, die mit dem Codierungsstandard der abstrakten Syntax Notation One (ASN. 1) kompatibel sind.
ms.assetid: 8e3b6e00-51cf-4e39-a68e-dcf8fbe8ab3b
topic_type:
- apiref
api_name:
- ASN_SEQUENCE
- ASN_SEQUENCEOF
api_location:
- Snmp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a484e58d7a92a3c75408db3160362d84e7891b76
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103422"
---
# <a name="snmp-constructor-syntax-values"></a><span data-ttu-id="80f8e-103">Werte der SNMP-Konstruktorsyntax</span><span class="sxs-lookup"><span data-stu-id="80f8e-103">SNMP Constructor Syntax Values</span></span>

<span data-ttu-id="80f8e-104">\[SNMP ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="80f8e-104">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="80f8e-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="80f8e-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="80f8e-106">Verwenden Sie stattdessen [Windows-Remoteverwaltung](/windows/desktop/WinRM/portal), bei dem es sich um die Microsoft-Implementierung von WS-man handelt.\]</span><span class="sxs-lookup"><span data-stu-id="80f8e-106">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="80f8e-107">In den SNMP-Konstruktorsyntax Werten werden Typen beschrieben, die mit dem Codierungsstandard der abstrakten Syntax Notation One (ASN. 1) kompatibel sind.</span><span class="sxs-lookup"><span data-stu-id="80f8e-107">The SNMP Constructor Syntax Values describe types that are compliant with the Abstract Syntax Notation One (ASN.1) encoding standard.</span></span>



| <span data-ttu-id="80f8e-108">Konstante</span><span class="sxs-lookup"><span data-stu-id="80f8e-108">Constant</span></span>                                                                                                                                                         | <span data-ttu-id="80f8e-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="80f8e-109">Description</span></span>                                               |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------|
| <span id="ASN_SEQUENCE"></span><span id="asn_sequence"></span><dl> <span data-ttu-id="80f8e-110"><dt>**ASN- \_ Sequenz**</dt></span><span class="sxs-lookup"><span data-stu-id="80f8e-110"><dt>**ASN\_SEQUENCE**</dt></span></span> </dl>       | <span data-ttu-id="80f8e-111">Gibt an, dass die Nachricht eine ASN-Sequenz ist.</span><span class="sxs-lookup"><span data-stu-id="80f8e-111">Indicates that the message is an ASN sequence.</span></span><br/> |
| <span id="ASN_SEQUENCEOF"></span><span id="asn_sequenceof"></span><dl> <span data-ttu-id="80f8e-112"><dt>**ASN- \_ sequenceof**</dt></span><span class="sxs-lookup"><span data-stu-id="80f8e-112"><dt>**ASN\_SEQUENCEOF**</dt></span></span> </dl> | <span data-ttu-id="80f8e-113">Siehe ASN \_ Sequence.</span><span class="sxs-lookup"><span data-stu-id="80f8e-113">See ASN\_SEQUENCE.</span></span><br/>                             |



## <a name="requirements"></a><span data-ttu-id="80f8e-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="80f8e-114">Requirements</span></span>



| <span data-ttu-id="80f8e-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="80f8e-115">Requirement</span></span> | <span data-ttu-id="80f8e-116">Wert</span><span class="sxs-lookup"><span data-stu-id="80f8e-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="80f8e-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="80f8e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="80f8e-118">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="80f8e-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="80f8e-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="80f8e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="80f8e-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="80f8e-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="80f8e-121">Header</span><span class="sxs-lookup"><span data-stu-id="80f8e-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="80f8e-122"><dt>SNMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="80f8e-122"><dt>Snmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80f8e-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="80f8e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80f8e-124">Simple Network Management-Protokoll (SNMP) – Übersicht</span><span class="sxs-lookup"><span data-stu-id="80f8e-124">Simple Network Management Protocol (SNMP) Overview</span></span>](simple-network-management-protocol-snmp-.md)
</dt> <dt>

[<span data-ttu-id="80f8e-125">SNMP-Referenz</span><span class="sxs-lookup"><span data-stu-id="80f8e-125">SNMP Reference</span></span>](snmp-reference.md)
</dt> <dt>

[<span data-ttu-id="80f8e-126">SNMP-Konstanten</span><span class="sxs-lookup"><span data-stu-id="80f8e-126">SNMP Constants</span></span>](snmp-constants.md)
</dt> </dl>

 

