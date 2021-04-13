---
title: Validieren eines PDU
description: Wenn die WinSNMP-Anwendung die Funktion snmpsendmsg oder die Funktion snmpencodemsg aufruft, überprüft die Microsoft WinSNMP-Implementierung die Gültigkeit des PDU und der anderen Funktionsparameter.
ms.assetid: 0f5754ff-3688-465b-a1ad-bf7d89d7dbd8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9d3fe0f9831f285b51b3060517d2037a8ec05f8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388587"
---
# <a name="validating-a-pdu"></a><span data-ttu-id="38581-103">Validieren eines PDU</span><span class="sxs-lookup"><span data-stu-id="38581-103">Validating a PDU</span></span>

<span data-ttu-id="38581-104">Wenn die WinSNMP-Anwendung die Funktion [**snmpsendmsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) oder die Funktion [**snmpencodemsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpencodemsg) aufruft, überprüft die Microsoft WinSNMP-Implementierung die Gültigkeit des PDU und der anderen Funktionsparameter.</span><span class="sxs-lookup"><span data-stu-id="38581-104">When the WinSNMP application calls the [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) function or the [**SnmpEncodeMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpencodemsg) function, the Microsoft WinSNMP implementation verifies the validity of the PDU and the other function parameters.</span></span>

<span data-ttu-id="38581-105">Der Wert einer PDU-Daten Komponente (oder eines Felds) kann einzeln gültig sein, ist aber möglicherweise in Kombination mit Werten für andere Felder ungültig.</span><span class="sxs-lookup"><span data-stu-id="38581-105">The value of one PDU data component (or field) can be valid individually, but it may be invalid in combination with values for other fields.</span></span> <span data-ttu-id="38581-106">Wenn beispielsweise das Feld " **PDU \_ Type** " des PDU-Typs "SNMP \_ PDU \_ Getbulk" oder "SNMP \_ PDU" ist \_ , müssen die Felder " **Fehler \_ Status** " und " **Fehler \_ Index** " gleich 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="38581-106">For example, unless the **PDU\_type** field of the PDU is SNMP\_PDU\_GETBULK or SNMP\_PDU\_RESPONSE, both the **error\_status** and **error\_index** fields must be equal to zero.</span></span> <span data-ttu-id="38581-107">Jede andere Wert Kombination stellt ein ungültiges PDU dar.</span><span class="sxs-lookup"><span data-stu-id="38581-107">Any other value combination constitutes an invalid PDU.</span></span>

<span data-ttu-id="38581-108">Die-Implementierung lehnt ungültige PDUs ab und gibt den Fehlerstatus "Snmpapi Failure" zurück \_ .</span><span class="sxs-lookup"><span data-stu-id="38581-108">The implementation rejects invalid PDUs and returns the error status SNMPAPI\_FAILURE.</span></span> <span data-ttu-id="38581-109">Es wird ein erweiterter Fehlercode festgelegt, der dem ungültigen Snmpapi- \_ PDU entspricht \_ .</span><span class="sxs-lookup"><span data-stu-id="38581-109">It sets an extended error code equal to SNMPAPI\_PDU\_INVALID.</span></span>

 

 




