---
title: Übersetzen von Nachrichtenanforderungen
description: In diesem Thema wird der Prozess der Übersetzung von SNMPv1-Anforderungen in SNMPv2-Anforderungen beschrieben.
ms.assetid: 7671ae36-99b1-47b1-930a-f376021d56a2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1775d59a8de0bd0473570f3028018a1a25cad2ebd4ee004025ad11a38e37e69c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119885890"
---
# <a name="translating-message-requests"></a>Übersetzen von Nachrichtenanforderungen

In diesem Thema wird der Prozess der Übersetzung von SNMPv1-Anforderungen in SNMPv2-Anforderungen beschrieben.

Wenn eine WinSNMP-Anwendung Funktionen anfordert, die unter dem SNMP Version 2C-Framework (SNMPv2C) verfügbar sind, die Zielentität jedoch nur das SNMP Version 1-Framework (SNMPv1) unterstützt, versucht die Microsoft WinSNMP-Implementierung, die Anforderung in das SNMPv1-Format zu übersetzen. Hierzu verwendet die Implementierung die in RFC 1908 definierten Verfahren"Koexistenz zwischen Version 1 und Version 2 des Internet-Standard Network Management Framework". Wenn die Übersetzung nicht möglich ist, schlägt die [**SnmpSendMsg-Funktion**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) mit dem erweiterten Fehlercode SNMPAPI \_ OPERATION INVALID \_ fehl.

 

 




