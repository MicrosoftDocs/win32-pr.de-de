---
title: SNMP-Variablen Typen und PDU-Anforderungs Typen
description: Die Definitionen für einige SNMP-Variablen Typen und PDU-Anforderungs Typen wurden geändert. Die Datei SNMP. h ordnet alte Typen den entsprechenden neuen Typen zu.
ms.assetid: 2d87aeee-6fcb-4837-b091-6a9def8a9acb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d656add1b177b50e24b30a11d9fe008dcdfdf9bc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728953"
---
# <a name="snmp-variable-types-and-request-pdu-types"></a><span data-ttu-id="ae624-104">SNMP-Variablen Typen und PDU-Anforderungs Typen</span><span class="sxs-lookup"><span data-stu-id="ae624-104">SNMP Variable Types and Request PDU Types</span></span>

<span data-ttu-id="ae624-105">\[SNMP ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="ae624-105">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="ae624-106">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="ae624-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="ae624-107">Verwenden Sie stattdessen [Windows-Remoteverwaltung](/windows/desktop/WinRM/portal), bei dem es sich um die Microsoft-Implementierung von WS-man handelt.\]</span><span class="sxs-lookup"><span data-stu-id="ae624-107">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="ae624-108">Die Definitionen für einige SNMP-Variablen Typen und PDU-Anforderungs Typen wurden geändert.</span><span class="sxs-lookup"><span data-stu-id="ae624-108">The definitions for some SNMP variable types and request PDU types have changed.</span></span> <span data-ttu-id="ae624-109">Die Datei SNMP. h ordnet alte Typen den entsprechenden neuen Typen zu.</span><span class="sxs-lookup"><span data-stu-id="ae624-109">The Snmp.h file maps old types to the corresponding new types.</span></span>

## <a name="modified-snmp-variable-types"></a><span data-ttu-id="ae624-110">Geänderte SNMP-Variablen Typen</span><span class="sxs-lookup"><span data-stu-id="ae624-110">Modified SNMP Variable Types</span></span>

<span data-ttu-id="ae624-111">Sie sollten die neuen SNMP-Variablen Typen verwenden, die in der folgenden Tabelle aufgeführt sind, wenn Sie Manager-Anwendungen entwickeln, die die Microsoft SNMP-Verwaltungs-API verwenden.</span><span class="sxs-lookup"><span data-stu-id="ae624-111">You should use the new SNMP variable types listed in the following table when you develop manager applications that use the Microsoft SNMP Management API.</span></span> <span data-ttu-id="ae624-112">In der Tabelle werden die alten SNMP-Variablen Typen mit den entsprechenden neuen Variablen Typen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="ae624-112">The table lists the old SNMP variable types with the corresponding new variable types.</span></span>

| <span data-ttu-id="ae624-113">Alter Variablentyp</span><span class="sxs-lookup"><span data-stu-id="ae624-113">Old variable type</span></span>        | <span data-ttu-id="ae624-114">Neuer Variablentyp</span><span class="sxs-lookup"><span data-stu-id="ae624-114">New variable type</span></span> |
|--------------------------|-------------------|
| <span data-ttu-id="ae624-115">ASN \_ RFC1155 \_ IPAddress</span><span class="sxs-lookup"><span data-stu-id="ae624-115">ASN\_RFC1155\_IPADDRESS</span></span>  | <span data-ttu-id="ae624-116">ASN- \_ IPAddress</span><span class="sxs-lookup"><span data-stu-id="ae624-116">ASN\_IPADDRESS</span></span>    |
| <span data-ttu-id="ae624-117">ASN \_ RFC1155- \_ Counter</span><span class="sxs-lookup"><span data-stu-id="ae624-117">ASN\_RFC1155\_COUNTER</span></span>    | <span data-ttu-id="ae624-118">ASN \_ COUNTER32</span><span class="sxs-lookup"><span data-stu-id="ae624-118">ASN\_COUNTER32</span></span>    |
| <span data-ttu-id="ae624-119">ASN \_ RFC1155 \_ Messgerät</span><span class="sxs-lookup"><span data-stu-id="ae624-119">ASN\_RFC1155\_GAUGE</span></span>      | <span data-ttu-id="ae624-120">ASN \_ GAUGE32</span><span class="sxs-lookup"><span data-stu-id="ae624-120">ASN\_GAUGE32</span></span>      |
| <span data-ttu-id="ae624-121">ASN \_ RFC1155 \_ TimeTicks</span><span class="sxs-lookup"><span data-stu-id="ae624-121">ASN\_RFC1155\_TIMETICKS</span></span>  | <span data-ttu-id="ae624-122">ASN- \_ TimeTicks</span><span class="sxs-lookup"><span data-stu-id="ae624-122">ASN\_TIMETICKS</span></span>    |
| <span data-ttu-id="ae624-123">ASN \_ RFC1155 nicht transparent \_</span><span class="sxs-lookup"><span data-stu-id="ae624-123">ASN\_RFC1155\_OPAQUE</span></span>     | <span data-ttu-id="ae624-124">ASN \_ nicht transparent</span><span class="sxs-lookup"><span data-stu-id="ae624-124">ASN\_OPAQUE</span></span>       |
| <span data-ttu-id="ae624-125">ASN \_ RFC1213 \_ dispstring</span><span class="sxs-lookup"><span data-stu-id="ae624-125">ASN\_RFC1213\_DISPSTRING</span></span> | <span data-ttu-id="ae624-126">ASN \_ octetstring</span><span class="sxs-lookup"><span data-stu-id="ae624-126">ASN\_OCTETSTRING</span></span>  |



 

## <a name="modified-snmp-pdu-request-types"></a><span data-ttu-id="ae624-127">Geänderte SNMP-PDU-Anforderungs Typen</span><span class="sxs-lookup"><span data-stu-id="ae624-127">Modified SNMP PDU Request Types</span></span>

<span data-ttu-id="ae624-128">Sie sollten die neuen SNMP-PDU-Typen verwenden, die in der folgenden Tabelle aufgeführt sind, wenn Sie Manager-Anwendungen entwickeln, die die Microsoft SNMP-Verwaltungs-API verwenden.</span><span class="sxs-lookup"><span data-stu-id="ae624-128">You should use the new SNMP PDU types listed in the following table when you develop manager applications that use the Microsoft SNMP Management API.</span></span> <span data-ttu-id="ae624-129">In der Tabelle sind die alten SNMP-PDU-Typen mit den entsprechenden neuen PDU-Typen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="ae624-129">The table lists the old SNMP PDU types with the corresponding new PDU types.</span></span>

| <span data-ttu-id="ae624-130">Alter PDU-Typ</span><span class="sxs-lookup"><span data-stu-id="ae624-130">Old PDU type</span></span>                 | <span data-ttu-id="ae624-131">Neuer PDU-Typ</span><span class="sxs-lookup"><span data-stu-id="ae624-131">New PDU type</span></span>        |
|------------------------------|---------------------|
| <span data-ttu-id="ae624-132">ASN \_ RFC1157 \_ GetRequest</span><span class="sxs-lookup"><span data-stu-id="ae624-132">ASN\_RFC1157\_GETREQUEST</span></span>     | <span data-ttu-id="ae624-133">SNMP \_ PDU \_ Get</span><span class="sxs-lookup"><span data-stu-id="ae624-133">SNMP\_PDU\_GET</span></span>      |
| <span data-ttu-id="ae624-134">ASN \_ RFC1157 \_ getnextrequest</span><span class="sxs-lookup"><span data-stu-id="ae624-134">ASN\_RFC1157\_GETNEXTREQUEST</span></span> | <span data-ttu-id="ae624-135">SNMP \_ PDU \_ GetNext</span><span class="sxs-lookup"><span data-stu-id="ae624-135">SNMP\_PDU\_GETNEXT</span></span>  |
| <span data-ttu-id="ae624-136">ASN \_ RFC1157 \_ GetResponse</span><span class="sxs-lookup"><span data-stu-id="ae624-136">ASN\_RFC1157\_GETRESPONSE</span></span>    | <span data-ttu-id="ae624-137">SNMP- \_ PDU- \_ Antwort</span><span class="sxs-lookup"><span data-stu-id="ae624-137">SNMP\_PDU\_RESPONSE</span></span> |
| <span data-ttu-id="ae624-138">ASN \_ RFC1157 \_ abtrequest</span><span class="sxs-lookup"><span data-stu-id="ae624-138">ASN\_RFC1157\_SETREQUEST</span></span>     | <span data-ttu-id="ae624-139">SNMP- \_ PDU- \_ Satz</span><span class="sxs-lookup"><span data-stu-id="ae624-139">SNMP\_PDU\_SET</span></span>      |
| <span data-ttu-id="ae624-140">ASN \_ RFC1157 \_ Trap</span><span class="sxs-lookup"><span data-stu-id="ae624-140">ASN\_RFC1157\_TRAP</span></span>           | <span data-ttu-id="ae624-141">SNMP \_ PDU \_ V1TRAP</span><span class="sxs-lookup"><span data-stu-id="ae624-141">SNMP\_PDU\_V1TRAP</span></span>   |



 

 

 