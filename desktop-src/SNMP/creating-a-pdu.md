---
title: Erstellen eines PDU
description: Zum Erstellen und Initialisieren eines PDU Ruft eine WinSNMP-Anwendung die snmpkreatepdu-Funktion auf.
ms.assetid: 7f02a2c6-19bc-456f-bf04-3297d19000f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1aba7a4ca42e2a5d63169d2521410773ca018c4f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856187"
---
# <a name="creating-a-pdu"></a><span data-ttu-id="500f1-103">Erstellen eines PDU</span><span class="sxs-lookup"><span data-stu-id="500f1-103">Creating a PDU</span></span>

<span data-ttu-id="500f1-104">Zum Erstellen und Initialisieren eines PDU Ruft eine WinSNMP-Anwendung die [**snmpkreatepdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) -Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="500f1-104">To create and initialize a PDU a WinSNMP application calls the [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) function.</span></span> <span data-ttu-id="500f1-105">Die Anwendung muss **snmpkreatepdu** aufrufen, bevor Sie die Funktion [**snmpsendmsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) aufruft, um anzufordern, dass die Microsoft WinSNMP-Implementierung ein PDU überträgt.</span><span class="sxs-lookup"><span data-stu-id="500f1-105">The application must call **SnmpCreatePdu** before it calls the [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) function to request that the Microsoft WinSNMP implementation transmit a PDU.</span></span> <span data-ttu-id="500f1-106">Die Anwendung muss auch [**snmpkreatepdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) aufrufen, bevor die Funktion [**snmpencodemsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpencodemsg) aufgerufen wird, um die Codierung einer SNMP-Nachricht anzufordern.</span><span class="sxs-lookup"><span data-stu-id="500f1-106">The application must also call [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) before it calls the [**SnmpEncodeMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpencodemsg) function to request encoding of an SNMP message.</span></span>

<span data-ttu-id="500f1-107">Die Anwendung muss die Funktion [**snmpfreepdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu) aufrufen, um die Ressourcen freizugeben, die die [**snmpcreatepdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) -Funktion für neue PDUs zuordnet.</span><span class="sxs-lookup"><span data-stu-id="500f1-107">The application must call the [**SnmpFreePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu) function to release the resources that the [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) function allocates for new PDUs.</span></span>

 

 




