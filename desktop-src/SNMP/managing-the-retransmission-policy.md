---
title: Verwalten der Richtlinie für Neuübertragungen
description: Die WinSNMP-Anwendung kann anfordern, dass die Microsoft WinSNMP-Implementierung die Richtlinie zur erneuten Übertragung der Anwendung ausführt. Wenn die Implementierung die erneute Übertragung verwaltet, werden die Timeout-und Wiederholungs Zählerwerte in der Datenbank verwendet.
ms.assetid: 1f1a9589-3566-4d90-ac4d-7acf69f34676
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f2e47d983f8da62ccb8ffbe9c20b35c71bfbb70
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037292"
---
# <a name="managing-the-retransmission-policy"></a>Verwalten der Richtlinie für Neuübertragungen

Die WinSNMP-Anwendung kann anfordern, dass die Microsoft WinSNMP-Implementierung die Richtlinie zur erneuten Übertragung der Anwendung ausführt. Wenn die Implementierung die erneute Übertragung verwaltet, werden die Timeout-und Wiederholungs Zählerwerte in der Datenbank verwendet.

Die-Implementierung identifiziert den Standardmodus für Neuübertragungen in einem Rückgabewert der [**SnmpStartup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup) -Funktion während der Initialisierung. Der Modus kann einen der folgenden Werte aufweisen.



| Wert        | Bedeutung                                                                      |
|--------------|------------------------------------------------------------------------------|
| Snmpapi \_ auf  | Die Implementierung führt die Neuübertragungs Richtlinie der Anwendung aus.     |
| Snmpapi \_ deaktiviert | Die-Implementierung führt nicht die Neuübertragungs Richtlinie der Anwendung aus. |



 

Eine WinSNMP-Anwendung kann jederzeit den aktuellen Neuübertragungs Modus für die Implementierung abrufen, indem die [**snmpgetretransmitmode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetretransmitmode) -Funktion aufgerufen wird. Die WinSNMP-API bietet andere [Datenbankfunktionen](winsnmp-functions.md) , die die Verwaltung der Richtlinie zur erneuten Übertragung vereinfachen.

Die WinSNMP-Anwendung kann während der Ausführung eines Programms jederzeit die Ausführung der Richtlinie anpassen, indem Sie einen der folgenden Schritte ausführen:

-   Fordern Sie an, dass die Implementierung die Neuübertragungs Richtlinie startet oder beendet, indem Sie die [**snmpstretransmitmode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode) -Funktion aufrufen. Weitere Informationen finden Sie unter [aktivieren und Deaktivieren der erneuten Übertragung](turning-retransmission-on-and-off.md).
-   Ändern Sie den Timeout Zeitraum und die Anzahl der Wiederholungswerte in der Datenbank der Implementierung. Weitere Informationen finden Sie unter [Ändern der Richtlinie für Neuübertragungen](changing-the-retransmission-policy.md).
-   Rufen Sie die [**snmpcancelmsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg) -Funktion auf, um den Neuübertragungs Zyklen abzubrechen und interne Datenstrukturen freizugeben, die einer einzelnen SNMP-Nachrichten Anforderung zugeordnet sind. Weitere Informationen finden Sie unter [Abbrechen der erneuten Übertragung](canceling-retransmission.md).

Die Anwendung kann Ihre eigene Neuübertragungs Richtlinie ausführen. In diesem Fall basiert die Ausführung möglicherweise auf den Werten in der Datenbank.

 

 




