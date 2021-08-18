---
title: Verwalten der Neuübertragungsrichtlinie
description: Die WinSNMP-Anwendung kann anfordern, dass die Microsoft WinSNMP-Implementierung die Neuübertragungsrichtlinie der Anwendung ausführen soll. Wenn die Implementierung die Neuübertragung verwaltet, verwendet sie den Time out-Zeitraum und die Wiederholungsanzahlwerte in der Datenbank.
ms.assetid: 1f1a9589-3566-4d90-ac4d-7acf69f34676
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63737f8cb4a0fcdb8c6e3824d07cbc7c592c1f7e9813e8751197fcd1d64ad786
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009428"
---
# <a name="managing-the-retransmission-policy"></a>Verwalten der Neuübertragungsrichtlinie

Die WinSNMP-Anwendung kann anfordern, dass die Microsoft WinSNMP-Implementierung die Neuübertragungsrichtlinie der Anwendung ausführen soll. Wenn die Implementierung die Neuübertragung verwaltet, verwendet sie den Time out-Zeitraum und die Wiederholungsanzahlwerte in der Datenbank.

Die Implementierung identifiziert den Standardmäßigen Neuübertragungsmodus in einem Rückgabewert der [**SnmpStartup-Funktion**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup) während der Initialisierung. Der Modus kann einer der folgenden Werte sein.



| Wert        | Bedeutung                                                                      |
|--------------|------------------------------------------------------------------------------|
| SNMPAPI \_ ON  | Die Implementierung wird die Neuübertragungsrichtlinie der Anwendung ausführen.     |
| SNMPAPI \_ OFF | Die Implementierung wird die Neuübertragungsrichtlinie der Anwendung nicht ausführen. |



 

Eine WinSNMP-Anwendung kann jederzeit den aktuellen Neuübertragungsmodus für die Implementierung abrufen, indem die [**SnmpGetRetransmitMode-Funktion aufgerufen**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetretransmitmode) wird. Die WinSNMP-API stellt andere [Datenbankfunktionen bereit,](winsnmp-functions.md) die die Verwaltung der Neuübertragungsrichtlinie vereinfachen.

Während der Programmausführung kann die WinSNMP-Anwendung die Ausführung der Richtlinie jederzeit anpassen, indem sie einen der folgenden Schritte ausführen:

-   Fordern Sie an, dass die Implementierung die Neuübertragungsrichtlinie startet oder stoppt, indem Sie die [**SnmpSetRetransmitMode-Funktion**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode) aufrufen. Weitere Informationen finden Sie unter [Aktivieren und Deaktivieren von Neuübertragungen.](turning-retransmission-on-and-off.md)
-   Ändern Sie den Time out-Zeitraum und die Wiederholungsanzahlwerte in der Datenbank der Implementierung. Weitere Informationen finden Sie unter [Ändern der Neuübertragungsrichtlinie.](changing-the-retransmission-policy.md)
-   Rufen Sie [**die SnmpCancelMsg-Funktion**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg) auf, um den Neuübertragungszyklus abzubricht und interne Datenstrukturen frei zu geben, die einer einzelnen SNMP-Nachrichtenanforderung zugeordnet sind. Weitere Informationen finden Sie unter [Abbrechen der Neuübertragung](canceling-retransmission.md).

Die Anwendung kann ihre eigene Neuübertragungsrichtlinie ausführen. In diesem Fall kann die Ausführung auf den Werten in der Datenbank basieren.

 

 




