---
title: Übersetzen von Traps von SNMPv1 in SNMPv2C
description: Wenn die Microsoft WinSNMP-Implementierung Traps von einer Entität empfängt, die unter dem SNMPv1-Framework ausgeführt wird, übersetzt sie die Traps in das SNMPv2C-Format.
ms.assetid: 472f67ba-05d5-46f7-a2f1-1cef6182574e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f70ddbdfb779f6b06f8ed26490c6fabd2421ae96f0006b4af5b7f1ab18f7d5d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119885860"
---
# <a name="translating-traps-from-snmpv1-to-snmpv2c"></a>Übersetzen von Traps von SNMPv1 in SNMPv2C

Wenn die Microsoft WinSNMP-Implementierung Traps von einer Entität empfängt, die unter dem SNMPv1-Framework ausgeführt wird, übersetzt sie die Traps in das SNMPv2C-Format. Wenn [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) eine Trap übermittelt, liegt sie daher immer im SNMPv2C-Format vor. RFC 1908, "Koexistenz zwischen Version 1 und Version 2 des Netzwerkverwaltungsframework nach Internetstandard", gibt die Regeln für die Übersetzung von SNMPv1 in das SNMPv2C-Trapformat an.

Eine WinSNMP-Anwendung kann den letzten Variablenbindungseintrag in einer Variablenbindungsliste überprüfen, um zu ermitteln, ob der Eintrag ein Trap ist, der aus SNMPv1 in das SNMPv2C-Format übersetzt wird. Wenn ja, ist die letzte Variablenbindung immer gleich dem Wert "snmpTrapEnterpriseOID.0".

Weitere Informationen finden Sie unter [Verwalten von Traps und Benachrichtigungen.](managing-traps-and-notifications.md)

 

 




