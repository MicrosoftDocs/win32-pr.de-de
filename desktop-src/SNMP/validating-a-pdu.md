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
# <a name="validating-a-pdu"></a>Validieren eines PDU

Wenn die WinSNMP-Anwendung die Funktion [**snmpsendmsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) oder die Funktion [**snmpencodemsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpencodemsg) aufruft, überprüft die Microsoft WinSNMP-Implementierung die Gültigkeit des PDU und der anderen Funktionsparameter.

Der Wert einer PDU-Daten Komponente (oder eines Felds) kann einzeln gültig sein, ist aber möglicherweise in Kombination mit Werten für andere Felder ungültig. Wenn beispielsweise das Feld " **PDU \_ Type** " des PDU-Typs "SNMP \_ PDU \_ Getbulk" oder "SNMP \_ PDU" ist \_ , müssen die Felder " **Fehler \_ Status** " und " **Fehler \_ Index** " gleich 0 (null) sein. Jede andere Wert Kombination stellt ein ungültiges PDU dar.

Die-Implementierung lehnt ungültige PDUs ab und gibt den Fehlerstatus "Snmpapi Failure" zurück \_ . Es wird ein erweiterter Fehlercode festgelegt, der dem ungültigen Snmpapi- \_ PDU entspricht \_ .

 

 




