---
title: Übereinstimmende Antworten und Anforderungs-PDUs
description: Die Reihenfolge, in der die WinSNMP-Anwendung SNMP-Antworten empfängt, entspricht möglicherweise nicht der Reihenfolge, in der die Anwendung SNMP-Vorgangs Anforderungen übermittelt.
ms.assetid: cd09cc4b-2ef6-4d2f-8f0f-b83d8df8599a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a75a05f4a450ac1712d7cdd01a3c0e79dfddeb2d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947893"
---
# <a name="matching-response-and-request-pdus"></a><span data-ttu-id="6ecf4-103">Übereinstimmende Antworten und Anforderungs-PDUs</span><span class="sxs-lookup"><span data-stu-id="6ecf4-103">Matching Response and Request PDUs</span></span>

<span data-ttu-id="6ecf4-104">Die Reihenfolge, in der die WinSNMP-Anwendung SNMP-Antworten empfängt, entspricht möglicherweise nicht der Reihenfolge, in der die Anwendung SNMP-Vorgangs Anforderungen übermittelt.</span><span class="sxs-lookup"><span data-stu-id="6ecf4-104">The order in which the WinSNMP application receives SNMP responses may not match the order in which the application submits SNMP operation requests.</span></span> <span data-ttu-id="6ecf4-105">Damit die Antwort mit der Anforderung abgeglichen wird, muss die Anwendung das Feld Anforderungs- **ID (Anforderungs- \_ ID**) der Antwort verwenden.</span><span class="sxs-lookup"><span data-stu-id="6ecf4-105">To match the response with the request, the application must use the request identifier field (the **request\_id**) of the response.</span></span>

<span data-ttu-id="6ecf4-106">Das Feld **Anforderungs- \_ ID** ist ein eindeutiger numerischer Wert, der das PDU identifiziert.</span><span class="sxs-lookup"><span data-stu-id="6ecf4-106">The **request\_id** field is a unique numeric value that identifies the PDU.</span></span> <span data-ttu-id="6ecf4-107">Anwendungen können Anforderungs Bezeichner zuweisen, indem Sie die [**snmpcreatepdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) -Funktion oder die [**snmpsetpdudata**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="6ecf4-107">Applications can assign request identifiers by calling the [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) function or the [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) function.</span></span> <span data-ttu-id="6ecf4-108">Rufen Sie die [**snmpgetpdudata**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata) -Funktion auf, um eine PDU- **Anforderungs- \_ ID** abzurufen.</span><span class="sxs-lookup"><span data-stu-id="6ecf4-108">Call the [**SnmpGetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata) function to retrieve a PDU's **request\_id**.</span></span>

 

 




