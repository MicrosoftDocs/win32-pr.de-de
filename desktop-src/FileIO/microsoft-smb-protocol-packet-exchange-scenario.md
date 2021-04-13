---
description: Beispiel für einen Microsoft SMB-Protokoll Paket Austausch zwischen einem Client und einem Server.
ms.assetid: f831d0de-0e38-4141-811c-892a1b5c4037
title: Microsoft SMB Protocol-Paket Austausch Szenario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8a03e2f75b00aa93e629b3e698631c5efde4694
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343189"
---
# <a name="microsoft-smb-protocol-packet-exchange-scenario"></a>Microsoft SMB Protocol-Paket Austausch Szenario

Dieses Thema enthält ein Beispiel für einen Microsoft SMB-Protokoll Paket Austausch zwischen einem Client und einem Server. Die folgenden Schritte sind eine Übersicht über den Prozess:

1.  Der Client und der Server richten eine NetBIOS-Sitzung ein.
2.  Der Client und der Server verhandeln den Microsoft SMB-Protokoll Dialekt.
3.  Der Client meldet sich am Server an.
4.  Der Client stellt eine Verbindung mit einer Freigabe auf dem Server her.
5.  Der Client öffnet eine Datei auf der Freigabe.
6.  Der Client liest aus der Datei.

Zuerst wird eine Vollduplex-TCP-Verbindung vom Client mit dem Server hergestellt. Anschließend erstellt und sendet der Client ein NetBIOS-Sitzungs Anforderungspaket über die TCP-Verbindung. Wenn das Paket ordnungsgemäß formatiert wurde, gibt der Server ein Paket zurück, das eine Meldung enthält, die bestätigt, dass die Sitzung eingerichtet wurde. Danach sendet der Client die ersten Microsoft SMB-Protokoll Pakete an den Server.



|                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Paket 1: SMB- \_ com- \_ Aushandlung**<br/> **Richtung:** Client zu Server<br/> **Beschreibung:** Der Client fordert an, dass der Server den Microsoft SMB-Protokoll Dialekt aushandelt. Eine Liste von Zeichen folgen, die die Dialekte identifizieren, mit denen der Client arbeiten kann, ist im Paket enthalten.<br/>                                                                                                                                                                                                                                                                                                                                   |
| **Paket 2: SMB- \_ com- \_ Aushandlung**<br/> **Richtung:** Server zu Client<br/> **Beschreibung:** Der Server antwortet auf die Anforderung des Clients, um den Microsoft SMB-Protokoll Dialekt zu identifizieren, der in der Sitzung verwendet werden soll. Das zurückgegebene Paket enthält auch eine zufällige 8-Byte-Zeichenfolge, die im nächsten Schritt verwendet wird, um den Client während des Anmeldevorgangs zu authentifizieren.<br/>                                                                                                                                                                                                                                   |
| **Paket 3: Einrichten der SMB- \_ com- \_ Sitzung \_ \_ AndX**<br/> **Richtung:** Client zu Server<br/> **Beschreibung:** Dieses Paket enthält Informationen zu Client Funktionen, sodass dieses Paket auch dann gesendet werden muss, wenn der Server nur die Sicherheit auf Freigabe Ebene implementiert hat.<br/> **Paket 3: Einrichten der SMB- \_ com- \_ Sitzung \_ \_ AndX**<br/> **Richtung:** Server zu Client<br/> **Beschreibung:** Wenn die Anforderung/Antwort vom Server akzeptiert wird, ist eine gültige UID in dem Paket enthalten, das an den Client zurückgegeben wird. Wenn Sie nicht akzeptiert wird, gibt der Server in diesem Paket einen Fehlercode zurück und verweigert den Zugriff.<br/> |
| **Paket 4: SMB \_ com \_ Tree \_ Connect \_ AndX**<br/> **Richtung:** Client zu Server<br/> **Beschreibung:** Der Client fordert den Zugriff auf die Freigabe an. Das Paket enthält den vollständig angegebenen Pfad der Freigabe im UNC-Format.<br/>                                                                                                                                                                                                                                                                                                                                                                                             |
| **Paket 5: SMB \_ com \_ Tree \_ Connect \_ AndX**<br/> **Richtung:** Server zu Client<br/> **Beschreibung:** Wenn der Zugriff auf die Freigabe gewährt wird, gibt der Server die 16-Bit-Struktur-ID (TID) zurück, die der Freigabe in diesem Paket entspricht. Wenn die Freigabe nicht vorhanden ist oder der Benutzer nicht über ausreichende Anmelde Informationen für den Zugriff auf die Freigabe verfügt, gibt der Server in diesem Paket einen Fehlercode zurück und verweigert den Zugriff auf die Freigabe.<br/>                                                                                                                                                                                                 |
| **Paket 6: SMB \_ com \_ Open \_ AndX**<br/> **Richtung:** Client zu Server<br/> **Beschreibung:** Der Client fordert den Server auf, eine Datei auf der Freigabe zu öffnen, auf die im Auftrag des Clients zugegriffen wird. Dieses Paket enthält den Namen der Datei, die geöffnet werden soll.<br/>                                                                                                                                                                                                                                                                                                                                                                   |
| **Paket 7: SMB \_ com \_ Open \_ AndX**<br/> **Richtung:** Server zu Client<br/> **Beschreibung:** Wenn der Zugriff auf die Datei gewährt wird, gibt der Server die Datei-ID der angeforderten Datei zurück. Wenn die Datei nicht vorhanden ist oder der Benutzer nicht über ausreichende Anmelde Informationen für den Zugriff auf die Datei verfügt, gibt der Server in diesem Paket einen Fehlercode zurück und verweigert den Zugriff auf die Datei.<br/>                                                                                                                                                                                                                                                  |
| **Paket 8: SMB \_ com \_ Read \_ AndX**<br/> **Richtung:** Client zu Server<br/> **Beschreibung:** Der Client fordert den Server auf, Daten aus der geöffneten Datei im Namen des Clients zu lesen und diese Daten an den Client zurückzugeben. Die Datei-ID, die vom Client beim Öffnen der Datei abgerufen wird, ist in diesem Paket enthalten, um zu ermitteln, von welcher geöffneten Datei der Serverdaten lesen soll.<br/>                                                                                                                                                                                                                   |
| **Paket 9: SMB \_ com \_ Read \_ AndX**<br/> **Richtung:** Server zu Client<br/> **Beschreibung:** Der Server gibt die angeforderten Datei Daten in diesem Paket zurück. Ein Fehler ist hier unwahrscheinlich, wenn der Zugriff auf den Server, die Freigabe und die Datei gewährt wurde. Dies kann in einigen Situationen vorkommen: z. b. wenn der Zugriff auf eine Freigabe zwischen dem Zeitpunkt, zu dem die Datei geöffnet wird, und dem Zeitpunkt, zu dem Sie gelesen wird, geändert wird.<br/>                                                                                                                                                                                                      |



 

> [!Note]  
> Wenn Sie einen CIFS implementieren, der keine Änderungs Benachrichtigungen unterstützt, kann Windows einen ausstehenden Handle für das Dateisystem nicht aufbewahren, und die SMB-Verbindung kann ohne vorherige Ankündigung Weg gehen.

 

 

 




