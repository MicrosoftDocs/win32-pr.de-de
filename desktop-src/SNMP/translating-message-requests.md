---
title: Übersetzen von Nachrichten Anforderungen
description: In diesem Thema wird beschrieben, wie Sie SNMPv1-Anforderungen in SNMPv2-Anforderungen übersetzen.
ms.assetid: 7671ae36-99b1-47b1-930a-f376021d56a2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa2a67ecb78b16f818ea50158faf827e19d4eba5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515579"
---
# <a name="translating-message-requests"></a>Übersetzen von Nachrichten Anforderungen

In diesem Thema wird beschrieben, wie Sie SNMPv1-Anforderungen in SNMPv2-Anforderungen übersetzen.

Wenn eine WinSNMP-Anwendung Funktionen anfordert, die unter der SNMP-Version 2C Framework (SNMPv2C) verfügbar sind, aber die Ziel Entität nur das SNMP-Framework Version 1 (SNMPv1) unterstützt, versucht die Microsoft WinSNMP-Implementierung, die Anforderung in das SNMPv1-Format zu übersetzen. Zu diesem Zweck verwendet die-Implementierung die Prozeduren, die in RFC 1908, "Koexistenz zwischen Version 1 und Version 2 der Internet-Standard Network Management Framework" definiert sind. Wenn die Übersetzung nicht möglich ist, schlägt die [**snmpsendmsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) -Funktion mit dem erweiterten Fehlercode "Snmpapi"- \_ Vorgang \_ ungültig.

 

 




