---
title: Erstellen einer PDU
description: Zum Erstellen und Initialisieren einer PDU ruft eine WinSNMP-Anwendung die SnmpCreatePdu-Funktion auf.
ms.assetid: 7f02a2c6-19bc-456f-bf04-3297d19000f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ef0598c08c27d988825b3f0db3d8172362e9e6daf2ed4dbad049e2808b01034
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009598"
---
# <a name="creating-a-pdu"></a>Erstellen einer PDU

Zum Erstellen und Initialisieren einer PDU ruft eine WinSNMP-Anwendung die [**SnmpCreatePdu-Funktion**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) auf. Die Anwendung muss **SnmpCreatePdu** aufrufen, bevor sie die [**SnmpSendMsg-Funktion aufruft,**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) um anzufordern, dass die Microsoft WinSNMP-Implementierung eine PDU überträgt. Die Anwendung muss auch [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) aufrufen, bevor sie die [**SnmpEncodeMsg-Funktion**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpencodemsg) aufruft, um die Codierung einer SNMP-Nachricht anzufordern.

Die Anwendung muss die [**SnmpFreePdu-Funktion**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu) aufrufen, um die Ressourcen freizugeben, die die [**SnmpCreatePdu-Funktion**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) für neue PDUs zuordnet.

 

 




