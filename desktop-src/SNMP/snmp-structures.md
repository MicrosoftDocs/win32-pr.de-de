---
title: SNMP-Strukturen
description: In der folgenden Tabelle sind die-Strukturen aufgelistet, die mit SNMP verwendet werden.
ms.assetid: b6dacc85-893d-4825-93df-729333b491b3
keywords:
- SNMP-Strukturen SNMP
- Strukturen SNMP, SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f254dfebeb3d468add8871d4b6f28f268341e9ea
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390891"
---
# <a name="snmp-structures"></a><span data-ttu-id="6ac42-105">SNMP-Strukturen</span><span class="sxs-lookup"><span data-stu-id="6ac42-105">SNMP Structures</span></span>

<span data-ttu-id="6ac42-106">\[SNMP ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="6ac42-106">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="6ac42-107">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="6ac42-107">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="6ac42-108">Verwenden Sie stattdessen [Windows-Remoteverwaltung](/windows/desktop/WinRM/portal), bei dem es sich um die Microsoft-Implementierung von WS-man handelt.\]</span><span class="sxs-lookup"><span data-stu-id="6ac42-108">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="6ac42-109">In der folgenden Tabelle sind die-Strukturen aufgelistet, die mit SNMP verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6ac42-109">The following table lists structures that are used with SNMP.</span></span>



| <span data-ttu-id="6ac42-110">SNMP-Struktur</span><span class="sxs-lookup"><span data-stu-id="6ac42-110">SNMP Structure</span></span>                                         | <span data-ttu-id="6ac42-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6ac42-111">Description</span></span>                                                                                             |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6ac42-112">**Asnany**</span><span class="sxs-lookup"><span data-stu-id="6ac42-112">**AsnAny**</span></span>](/windows/desktop/api/Snmp/ns-snmp-asnany)                           | <span data-ttu-id="6ac42-113">Beschreibt den Typ und den Wert einer angegebenen SNMP-Variablen.</span><span class="sxs-lookup"><span data-stu-id="6ac42-113">Describes the type and value of a specified SNMP variable.</span></span>                                              |
| <span data-ttu-id="6ac42-114">[**AsnCounter64**](/previous-versions/windows/desktop/legacy/aa377953(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6ac42-114">[**AsnCounter64**](/previous-versions/windows/desktop/legacy/aa377953(v=vs.85))</span></span>               | <span data-ttu-id="6ac42-115">Enthält einen 64-Bit-Leistungs Bewert, der durch zwei Werte angegeben wird, die die nieder wertigen und höherwertigen Bits beschreiben.</span><span class="sxs-lookup"><span data-stu-id="6ac42-115">Contains a 64-bit counter that is specified by two values describing its low-order and high-order bits.</span></span> |
| [<span data-ttu-id="6ac42-116">**Asnobjectidentifier**</span><span class="sxs-lookup"><span data-stu-id="6ac42-116">**AsnObjectIdentifier**</span></span>](/windows/desktop/api/Snmp/ns-snmp-asnobjectidentifier) | <span data-ttu-id="6ac42-117">Beschreibt einen Objekt Bezeichner (OID).</span><span class="sxs-lookup"><span data-stu-id="6ac42-117">Describes an object identifier (OID).</span></span>                                                                   |
| [<span data-ttu-id="6ac42-118">**Asnoctetstring**</span><span class="sxs-lookup"><span data-stu-id="6ac42-118">**AsnOctetString**</span></span>](/windows/desktop/api/Snmp/ns-snmp-asnoctetstring)           | <span data-ttu-id="6ac42-119">Stellt eine Zeichenfolge von Oktetten dar, normalerweise in Byte Werten.</span><span class="sxs-lookup"><span data-stu-id="6ac42-119">Represents a string of octets, usually in byte values.</span></span>                                                  |
| [<span data-ttu-id="6ac42-120">**Snmpvarbind**</span><span class="sxs-lookup"><span data-stu-id="6ac42-120">**SnmpVarBind**</span></span>](/windows/desktop/api/Snmp/ns-snmp-snmpvarbind)                 | <span data-ttu-id="6ac42-121">Beschreibt eine SNMP-Variablen Bindung.</span><span class="sxs-lookup"><span data-stu-id="6ac42-121">Describes an SNMP variable binding.</span></span>                                                                     |
| [<span data-ttu-id="6ac42-122">**Snmpvarbindlist**</span><span class="sxs-lookup"><span data-stu-id="6ac42-122">**SnmpVarBindList**</span></span>](/windows/desktop/api/Snmp/ns-snmp-snmpvarbindlist)         | <span data-ttu-id="6ac42-123">Enthält eine Liste von SNMP-Variablen Bindungen.</span><span class="sxs-lookup"><span data-stu-id="6ac42-123">Contains a list of SNMP variable bindings.</span></span>                                                              |



 

 

 