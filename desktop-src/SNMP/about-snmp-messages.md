---
title: Informationen zu SNMP-Nachrichten
description: Das Simple Network Management-Protokoll verwendet Nachrichten zum kommunizieren und Austauschen von Informationen zwischen Remote-SNMP-Entitäten.
ms.assetid: 9ba4b854-fc02-40c1-a92f-7c102c900e95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a0426bf44d976ddf9e2eafe2093dcea94956cb4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388115"
---
# <a name="about-snmp-messages"></a><span data-ttu-id="1c271-103">Informationen zu SNMP-Nachrichten</span><span class="sxs-lookup"><span data-stu-id="1c271-103">About SNMP Messages</span></span>

<span data-ttu-id="1c271-104">Das Simple Network Management-Protokoll verwendet Nachrichten zum kommunizieren und Austauschen von Informationen zwischen Remote-SNMP-Entitäten.</span><span class="sxs-lookup"><span data-stu-id="1c271-104">The Simple Network Management Protocol uses messages to communicate and exchange information between remote SNMP entities.</span></span> <span data-ttu-id="1c271-105">SNMP-Nachrichten enthalten Protokolldaten Einheiten (PDUs) sowie zusätzliche Nachrichten Header Elemente, die durch die relevante RFC definiert werden.</span><span class="sxs-lookup"><span data-stu-id="1c271-105">SNMP messages contain protocol data units (PDUs) plus additional message header elements defined by the relevant RFC.</span></span> <span data-ttu-id="1c271-106">Bei einem PDU handelt es sich um ein Datenpaket, das SNMP-Daten Komponenten (oder Felder) enthält.</span><span class="sxs-lookup"><span data-stu-id="1c271-106">A PDU is a data packet that contains SNMP data components (or fields).</span></span>

<span data-ttu-id="1c271-107">Das Format einer SNMP-Nachricht ist für SNMPv1 und SNMPv2C identisch.</span><span class="sxs-lookup"><span data-stu-id="1c271-107">The format of an SNMP message is the same for both SNMPv1 and SNMPv2C.</span></span> <span data-ttu-id="1c271-108">SNMPv2C unterstützt jedoch zusätzliche PDU-Typen.</span><span class="sxs-lookup"><span data-stu-id="1c271-108">However, SNMPv2C supports additional PDU types.</span></span> <span data-ttu-id="1c271-109">Beispielsweise wird der [SNMP \_ PDU \_ Getbulk](snmp-variable-types-and-request-pdu-types.md) -Anforderungstyp unterstützt, mit dem eine Anwendung große Datenblöcke aus Ziel Entitäten effizient abrufen kann.</span><span class="sxs-lookup"><span data-stu-id="1c271-109">For example, it supports the [SNMP\_PDU\_GETBULK](snmp-variable-types-and-request-pdu-types.md) request type, which enables an application to efficiently retrieve large blocks of data from target entities.</span></span>

 

 




