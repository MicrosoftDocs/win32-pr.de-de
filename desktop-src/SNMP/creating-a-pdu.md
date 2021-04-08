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
# <a name="creating-a-pdu"></a>Erstellen eines PDU

Zum Erstellen und Initialisieren eines PDU Ruft eine WinSNMP-Anwendung die [**snmpkreatepdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) -Funktion auf. Die Anwendung muss **snmpkreatepdu** aufrufen, bevor Sie die Funktion [**snmpsendmsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) aufruft, um anzufordern, dass die Microsoft WinSNMP-Implementierung ein PDU überträgt. Die Anwendung muss auch [**snmpkreatepdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) aufrufen, bevor die Funktion [**snmpencodemsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpencodemsg) aufgerufen wird, um die Codierung einer SNMP-Nachricht anzufordern.

Die Anwendung muss die Funktion [**snmpfreepdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu) aufrufen, um die Ressourcen freizugeben, die die [**snmpcreatepdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) -Funktion für neue PDUs zuordnet.

 

 




