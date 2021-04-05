---
title: SNMPv1 Trap-Typen (SNMP. h)
description: Die SNMPv1 Trap-Typen beschreiben einen vordefinierten Satz generischer Trap-Typen, die so formatiert sind, dass Sie dem SNMPv1 Trap-PDU-Standard entsprechen.
ms.assetid: 3a652b8f-2ae1-4f8c-b0d6-388bc9171427
topic_type:
- apiref
api_name:
- SNMP_GENERICTRAP_COLDSTART
- SNMP_GENERICTRAP_WARMSTART
- SNMP_GENERICTRAP_LINKDOWN
- SNMP_GENERICTRAP_LINKUP
- SNMP_GENERICTRAP_AUTHFAILURE
- SNMP_GENERICTRAP_EGPNEIGHLOSS
- SNMP_GENERICTRAP_ENTERSPECIFIC
api_location:
- Snmp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1091bc6af4fa4b1ddfadbaf35e3e69250ded6dcb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859271"
---
# <a name="snmpv1-trap-types"></a><span data-ttu-id="04ff0-103">SNMPv1 Trap-Typen</span><span class="sxs-lookup"><span data-stu-id="04ff0-103">SNMPv1 Trap Types</span></span>

<span data-ttu-id="04ff0-104">\[SNMP ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="04ff0-104">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="04ff0-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="04ff0-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="04ff0-106">Verwenden Sie stattdessen [Windows-Remoteverwaltung](/windows/desktop/WinRM/portal), bei dem es sich um die Microsoft-Implementierung von WS-man handelt.\]</span><span class="sxs-lookup"><span data-stu-id="04ff0-106">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="04ff0-107">Die SNMPv1 Trap-Typen beschreiben einen vordefinierten Satz generischer Trap-Typen, die so formatiert sind, dass Sie dem SNMPv1 Trap-PDU-Standard entsprechen.</span><span class="sxs-lookup"><span data-stu-id="04ff0-107">The SNMPv1 trap types describe a predefined set of generic trap types that are formatted to comply with the SNMPv1 trap PDU standard.</span></span>



| <span data-ttu-id="04ff0-108">Konstante</span><span class="sxs-lookup"><span data-stu-id="04ff0-108">Constant</span></span>                                                                                                                                                                                                          | <span data-ttu-id="04ff0-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="04ff0-109">Description</span></span>                                                                                                                                                                              |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SNMP_GENERICTRAP_COLDSTART"></span><span id="snmp_generictrap_coldstart"></span><dl> <span data-ttu-id="04ff0-110"><dt>**SNMP- \_ generictrap ( \_ coldStart)**</dt></span><span class="sxs-lookup"><span data-stu-id="04ff0-110"><dt>**SNMP\_GENERICTRAP\_COLDSTART**</dt></span></span> </dl>             | <span data-ttu-id="04ff0-111">Gibt einen Kaltstart-Trap an.</span><span class="sxs-lookup"><span data-stu-id="04ff0-111">Indicates a cold start trap.</span></span> <span data-ttu-id="04ff0-112">Der Agent initialisiert Protokoll Entitäten im verwalteten Modus.</span><span class="sxs-lookup"><span data-stu-id="04ff0-112">The agent is initializing protocol entities on the managed mode.</span></span> <span data-ttu-id="04ff0-113">Sie kann Objekte in der Ansicht ändern.</span><span class="sxs-lookup"><span data-stu-id="04ff0-113">It may alter objects in its view.</span></span><br/>                                               |
| <span id="SNMP_GENERICTRAP_WARMSTART"></span><span id="snmp_generictrap_warmstart"></span><dl> <span data-ttu-id="04ff0-114"><dt>**SNMP- \_ generictrap- \_ Warmstart**</dt></span><span class="sxs-lookup"><span data-stu-id="04ff0-114"><dt>**SNMP\_GENERICTRAP\_WARMSTART**</dt></span></span> </dl>             | <span data-ttu-id="04ff0-115">Gibt einen warmen Start Trap an.</span><span class="sxs-lookup"><span data-stu-id="04ff0-115">Indicates a warm start trap.</span></span> <span data-ttu-id="04ff0-116">Der Agent wird erneut initialisiert, die Objekte in der Ansicht werden jedoch nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="04ff0-116">The agent is reinitializing itself but it will not alter objects in its view.</span></span><br/>                                                                    |
| <span id="SNMP_GENERICTRAP_LINKDOWN"></span><span id="snmp_generictrap_linkdown"></span><dl> <span data-ttu-id="04ff0-117"><dt>**SNMP- \_ generictrap- \_ Link**</dt></span><span class="sxs-lookup"><span data-stu-id="04ff0-117"><dt>**SNMP\_GENERICTRAP\_LINKDOWN**</dt></span></span> </dl>                | <span data-ttu-id="04ff0-118">Gibt einen linkdown-Trap an.</span><span class="sxs-lookup"><span data-stu-id="04ff0-118">Indicates a link-down trap.</span></span> <span data-ttu-id="04ff0-119">Eine angefügte Schnittstelle hat sich von oben in den Zustand "nach unten" geändert.</span><span class="sxs-lookup"><span data-stu-id="04ff0-119">An attached interface has changed from the up state to the down state.</span></span> <span data-ttu-id="04ff0-120">Die erste Variable in der Variablen Bindungs Liste identifiziert die-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="04ff0-120">The first variable in the variable bindings list identifies the interface.</span></span><br/> |
| <span id="SNMP_GENERICTRAP_LINKUP"></span><span id="snmp_generictrap_linkup"></span><dl> <span data-ttu-id="04ff0-121"><dt>**SNMP- \_ generictrap- \_ Verknüpfung**</dt></span><span class="sxs-lookup"><span data-stu-id="04ff0-121"><dt>**SNMP\_GENERICTRAP\_LINKUP**</dt></span></span> </dl>                      | <span data-ttu-id="04ff0-122">Gibt einen Verbindungs Trap an.</span><span class="sxs-lookup"><span data-stu-id="04ff0-122">Indicates a link-up trap.</span></span> <span data-ttu-id="04ff0-123">Eine angefügte Schnittstelle hat sich von unten nach oben geändert.</span><span class="sxs-lookup"><span data-stu-id="04ff0-123">An attached interface has changed from the down start to the up state.</span></span> <span data-ttu-id="04ff0-124">Die erste Variable in der Variablen Bindungs Liste identifiziert die-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="04ff0-124">The first variable in the variable bindings list identifies the interface.</span></span><br/>   |
| <span id="SNMP_GENERICTRAP_AUTHFAILURE"></span><span id="snmp_generictrap_authfailure"></span><dl> <span data-ttu-id="04ff0-125"><dt>**SNMP- \_ generictrap- \_ authfailure**</dt></span><span class="sxs-lookup"><span data-stu-id="04ff0-125"><dt>**SNMP\_GENERICTRAP\_AUTHFAILURE**</dt></span></span> </dl>       | <span data-ttu-id="04ff0-126">Gibt einen Authentifizierungsfehler Trap an.</span><span class="sxs-lookup"><span data-stu-id="04ff0-126">Indicates an authentication failure trap.</span></span> <span data-ttu-id="04ff0-127">Eine SNMP-Entität hat eine SNMP-Nachricht gesendet, hat aber fälschlicherweise behauptet, zu einer bekannten Community zu gehören.</span><span class="sxs-lookup"><span data-stu-id="04ff0-127">An SNMP entity has sent an SNMP message, but it has falsely claimed to belong to a known community.</span></span><br/>                                 |
| <span id="SNMP_GENERICTRAP_EGPNEIGHLOSS"></span><span id="snmp_generictrap_egpneighloss"></span><dl> <span data-ttu-id="04ff0-128"><dt>**SNMP- \_ generictrap- \_ egpnachbarloss**</dt></span><span class="sxs-lookup"><span data-stu-id="04ff0-128"><dt>**SNMP\_GENERICTRAP\_EGPNEIGHLOSS**</dt></span></span> </dl>    | <span data-ttu-id="04ff0-129">Gibt den Verlust eines EGP-Nachbar Verlusts an.</span><span class="sxs-lookup"><span data-stu-id="04ff0-129">Indicates an EGP neighbor loss trap.</span></span> <span data-ttu-id="04ff0-130">Ein EGP-Peer hat sich in den Zustand "nach unten" geändert.</span><span class="sxs-lookup"><span data-stu-id="04ff0-130">An EGP peer has changed to the down state.</span></span> <span data-ttu-id="04ff0-131">Die erste Variable in der Variablen Bindungs Liste identifiziert die IP-Adresse des EGP-Peers.</span><span class="sxs-lookup"><span data-stu-id="04ff0-131">The first variable in the variable bindings list identifies the IP address of the EGP peer.</span></span><br/>   |
| <span id="SNMP_GENERICTRAP_ENTERSPECIFIC"></span><span id="snmp_generictrap_enterspecific"></span><dl> <span data-ttu-id="04ff0-132"><dt>**SNMP- \_ generictrap Enterprise- \_ spezifisch**</dt></span><span class="sxs-lookup"><span data-stu-id="04ff0-132"><dt>**SNMP\_GENERICTRAP\_ENTERSPECIFIC**</dt></span></span> </dl> | <span data-ttu-id="04ff0-133">Gibt einen unternehmensspezifischen Trap an.</span><span class="sxs-lookup"><span data-stu-id="04ff0-133">Indicates an enterprise-specific trap.</span></span> <span data-ttu-id="04ff0-134">Ein außergewöhnliches Ereignis ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="04ff0-134">An extraordinary event has occurred.</span></span> <span data-ttu-id="04ff0-135">Er wird im Parameter " *specifictrap* " mit einem unternehmensspezifischen Wert identifiziert.</span><span class="sxs-lookup"><span data-stu-id="04ff0-135">It is identified in the *specificTrap* parameter with an enterprise-specific value.</span></span><br/>               |



## <a name="requirements"></a><span data-ttu-id="04ff0-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="04ff0-136">Requirements</span></span>



| <span data-ttu-id="04ff0-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="04ff0-137">Requirement</span></span> | <span data-ttu-id="04ff0-138">Wert</span><span class="sxs-lookup"><span data-stu-id="04ff0-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="04ff0-139">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="04ff0-139">Minimum supported client</span></span><br/> | <span data-ttu-id="04ff0-140">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="04ff0-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="04ff0-141">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="04ff0-141">Minimum supported server</span></span><br/> | <span data-ttu-id="04ff0-142">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="04ff0-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="04ff0-143">Header</span><span class="sxs-lookup"><span data-stu-id="04ff0-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="04ff0-144"><dt>SNMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="04ff0-144"><dt>Snmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04ff0-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="04ff0-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04ff0-146">Simple Network Management-Protokoll (SNMP) – Übersicht</span><span class="sxs-lookup"><span data-stu-id="04ff0-146">Simple Network Management Protocol (SNMP) Overview</span></span>](simple-network-management-protocol-snmp-.md)
</dt> <dt>

[<span data-ttu-id="04ff0-147">SNMP-Referenz</span><span class="sxs-lookup"><span data-stu-id="04ff0-147">SNMP Reference</span></span>](snmp-reference.md)
</dt> <dt>

[<span data-ttu-id="04ff0-148">SNMP-Konstanten</span><span class="sxs-lookup"><span data-stu-id="04ff0-148">SNMP Constants</span></span>](snmp-constants.md)
</dt> </dl>

 

