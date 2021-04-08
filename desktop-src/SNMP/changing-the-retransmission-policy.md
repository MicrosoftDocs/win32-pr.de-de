---
title: Ändern der Richtlinie für Neuübertragungen
description: Die Microsoft WinSNMP-Implementierung bietet Unterstützung für Neuübertragungs Richtlinien, indem ein Timeout Wert und eine Wiederholungs Anzahl für die WinSNMP-Anwendung in einer-Datenbank gespeichert werden.
ms.assetid: 9ab45adc-12b7-40b1-8fec-40bf04302f64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e9f21fc479517b8844e9c1db75834b5b1c02edc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856188"
---
# <a name="changing-the-retransmission-policy"></a>Ändern der Richtlinie für Neuübertragungen

Die Microsoft WinSNMP-Implementierung bietet Unterstützung für Neuübertragungs Richtlinien, indem ein Timeout Wert und eine Wiederholungs Anzahl für die WinSNMP-Anwendung in einer-Datenbank gespeichert werden. Die-Implementierung speichert Werte für einzelne Ziel Entitäten. Die-Implementierung liefert anfänglich Standardwerte für diese Elemente, aber eine Anwendung kann Werte für einzelne Entitäten hinzufügen oder ändern.

Ein Aufruf der Funktionen [**snmpgettimeout**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgettimeout) und [**snmpgetretry**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetretry) gibt die Werte für Timeout und Wiederholungs Anzahl für eine bestimmte Ziel Entität zurück. Um den Timeout Wert zu ändern, muss eine WinSNMP-Anwendung die [**snmpsettimeout**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsettimeout) -Funktion aufrufen. Um den Wert für die Anzahl der Wiederholungs Versuche zu ändern, muss die Anwendung die [**snmpsetretry**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretry) -Funktion abrufen. Die aktualisierten Einstellungen wirken sich auf neue SNMP-Nachrichten Anforderungen an die Ziel Entität aus.

 

 




