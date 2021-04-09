---
title: Trap-Formate
description: Das Format von Trap-PDUs unterscheidet sich von dem anderer PDUs. Das Format von SNMPv1 Traps und SNMPv2C Traps ist ebenfalls unterschiedlich.
ms.assetid: 2d2b4520-28b7-4a2e-8dee-456e17d9d6f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e87adc3222808fcc7e81904ade07c09afa13bc6d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036617"
---
# <a name="trap-formats"></a><span data-ttu-id="292c4-104">Trap-Formate</span><span class="sxs-lookup"><span data-stu-id="292c4-104">Trap Formats</span></span>

<span data-ttu-id="292c4-105">Das Format von Trap-PDUs unterscheidet sich von dem anderer PDUs.</span><span class="sxs-lookup"><span data-stu-id="292c4-105">The format of trap PDUs is different than that of other PDUs.</span></span> <span data-ttu-id="292c4-106">Das Format von SNMPv1 Traps und SNMPv2C Traps ist ebenfalls unterschiedlich.</span><span class="sxs-lookup"><span data-stu-id="292c4-106">The format of SNMPv1 traps and SNMPv2C traps is also different.</span></span>

<span data-ttu-id="292c4-107">Im SNMPv2C Framework ist das PDU-Trap-Format eine Variablen Bindungs Liste von *n* Variablen Bindungs Einträgen, die folgendermaßen organisiert sind:</span><span class="sxs-lookup"><span data-stu-id="292c4-107">Under the SNMPv2C framework, the PDU trap format is a variable binding list of *n* variable binding entries organized in the following manner:</span></span>

-   <span data-ttu-id="292c4-108">Der erste Variablen Bindungs Eintrag enthält einen Zeitstempel.</span><span class="sxs-lookup"><span data-stu-id="292c4-108">The first variable binding entry contains a time-stamp.</span></span>
-   <span data-ttu-id="292c4-109">Der zweite Variablen Bindungs Eintrag ist ein Objekt Bezeichner, der den Trap identifiziert.</span><span class="sxs-lookup"><span data-stu-id="292c4-109">The second variable binding entry is an object identifier that identifies the trap.</span></span>
-   <span data-ttu-id="292c4-110">Die dritten bis *n* Variablen Bindungs Einträge enthalten ggf. zusätzliche Informationen, die mit dem Trap verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="292c4-110">The third through *n* variable binding entries, if present, contain additional information associated with the trap.</span></span>

<span data-ttu-id="292c4-111">Im SNMPv1 Framework lautet das PDU-Trap Format wie folgt.</span><span class="sxs-lookup"><span data-stu-id="292c4-111">Under the SNMPv1 framework, the PDU trap format is as follows.</span></span>

| <span data-ttu-id="292c4-112">Feld</span><span class="sxs-lookup"><span data-stu-id="292c4-112">Field</span></span>                      | <span data-ttu-id="292c4-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="292c4-113">Description</span></span>                                                      |
|----------------------------|------------------------------------------------------------------|
| <span data-ttu-id="292c4-114">Enterprise</span><span class="sxs-lookup"><span data-stu-id="292c4-114">enterprise</span></span>                 | <span data-ttu-id="292c4-115">Identifiziert den Typ des Geräts, das den Trap generiert hat.</span><span class="sxs-lookup"><span data-stu-id="292c4-115">Identifies the type of device that generated the trap.</span></span>           |
| <span data-ttu-id="292c4-116">Agent-addr</span><span class="sxs-lookup"><span data-stu-id="292c4-116">agent-addr</span></span>                 | <span data-ttu-id="292c4-117">Gibt die IP-Adresse des Geräts an, von dem der Trap generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="292c4-117">Identifies the IP address of the device that generated the trap.</span></span> |
| <span data-ttu-id="292c4-118">generischer Trap/spezifischer Trap</span><span class="sxs-lookup"><span data-stu-id="292c4-118">generic-trap/specific-trap</span></span> | <span data-ttu-id="292c4-119">Identifiziert einen vordefinierten Trap-Typ.</span><span class="sxs-lookup"><span data-stu-id="292c4-119">Identifies a predefined trap type.</span></span>                               |
| <span data-ttu-id="292c4-120">Zeitstempel</span><span class="sxs-lookup"><span data-stu-id="292c4-120">time-stamp</span></span>                 | <span data-ttu-id="292c4-121">Gibt an, wann der Trap generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="292c4-121">Identifies when the trap was generated.</span></span>                          |
| <span data-ttu-id="292c4-122">Variablen Bindungen</span><span class="sxs-lookup"><span data-stu-id="292c4-122">variable-bindings</span></span>          | <span data-ttu-id="292c4-123">Enthält zusätzliche Informationen, die mit dem Trap verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="292c4-123">Contains additional information associated with the trap.</span></span>        |



 

<span data-ttu-id="292c4-124">Die [**snmprecvmsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) -Funktion gibt immer eine Nachricht im SNMPv2C-Format zurück.</span><span class="sxs-lookup"><span data-stu-id="292c4-124">The [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) function always returns a message in the SNMPv2C format.</span></span> <span data-ttu-id="292c4-125">Wenn die Nachricht den Vorgangstyp **SNMP \_ PDU \_ Trap** enthält, kann die Anwendung die Variablen Bindungs Einträge der Nachricht lesen und die dem Trap zugeordneten Informationen abrufen.</span><span class="sxs-lookup"><span data-stu-id="292c4-125">If the message contains the operation type **SNMP\_PDU\_TRAP**, the application can read the variable binding entries of the message and retrieve the information associated with the trap.</span></span>

 

 




