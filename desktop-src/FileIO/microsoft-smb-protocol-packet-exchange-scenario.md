---
description: Beispiel für einen Microsoft SMB-Protokoll-Paketaustausch zwischen einem Client und einem Server.
ms.assetid: f831d0de-0e38-4141-811c-892a1b5c4037
title: Szenario mit Microsoft SMB-Protokollpaketaustausch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47415c6d49f6c1f7b924719d4d012277c03956c1af0d948b3ef66049c1203641
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048050"
---
# <a name="microsoft-smb-protocol-packet-exchange-scenario"></a>Szenario mit Microsoft SMB-Protokollpaketaustausch

Dieses Thema enthält ein Beispiel für einen Microsoft SMB-Protokoll-Paketaustausch zwischen einem Client und einem Server. Die folgenden Schritte sind eine Übersicht über den Prozess:

1.  Client und Server richten eine NetBIOS-Sitzung ein.
2.  Client und Server handeln den Dialekt des Microsoft SMB-Protokolls aus.
3.  Der Client meldet sich beim Server an.
4.  Der Client stellt eine Verbindung mit einer Freigabe auf dem Server herstellen.
5.  Der Client öffnet eine Datei auf der Freigabe.
6.  Der Client liest aus der Datei.

Zunächst wird eine Vollduplex-TCP-Verbindung vom Client mit dem Server hergestellt. Anschließend erstellt und sendet der Client ein NetBIOS-Sitzungsanforderungspaket über die TCP-Verbindung. Wenn das Paket ordnungsgemäß formatiert wurde, gibt der Server ein Paket zurück, das eine Meldung enthält, die angibt, dass die Sitzung eingerichtet wurde. Danach sendet der Client die ersten Microsoft SMB-Protokollpakete an den Server.



|                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Paket 1: SMB \_ COM \_ NEGOTIATE**<br/> **Richtung:** Client zu Server<br/> **Beschreibung:** Der Client fordert an, dass der Server den Dialekt des Microsoft SMB-Protokolls aushandelt. Eine Liste von Zeichenfolgen, die die Dialekte identifizieren, mit denen der Client arbeiten kann, ist im Paket enthalten.<br/>                                                                                                                                                                                                                                                                                                                                   |
| **Paket 2: SMB \_ COM \_ NEGOTIATE**<br/> **Richtung:** Server zu Client<br/> **Beschreibung:** Der Server antwortet auf die Clientanforderung, um den Dialekt des Microsoft SMB-Protokolls zu identifizieren, der in der Sitzung verwendet werden soll. Das zurückgegebene Paket enthält auch eine zufällige 8-Byte-Zeichenfolge, die im nächsten Schritt verwendet wird, um den Client während des Anmeldevorgangs zu authentifizieren.<br/>                                                                                                                                                                                                                                   |
| **Paket 3: SMB \_ COM \_ SESSION SETUP \_ \_ ANDX**<br/> **Richtung:** Client zu Server<br/> **Beschreibung:** Dieses Paket enthält Informationen zu Clientfunktionen, sodass dieses Paket gesendet werden muss, auch wenn der Server nur Sicherheit auf Freigabeebene implementiert hat.<br/> **Paket 3: SMB \_ COM \_ SESSION SETUP \_ \_ ANDX**<br/> **Richtung:** Server zu Client<br/> **Beschreibung:** Wenn die Herausforderung/Antwort vom Server akzeptiert wird, wird eine gültige UID in das Paket eingeschlossen, das an den Client zurückgegeben wird. Wenn dies nicht akzeptiert wird, gibt der Server einen Fehlercode in diesem Paket zurück und verweigert den Zugriff.<br/> |
| **Paket 4: SMB \_ COM \_ TREE CONNECT \_ \_ ANDX**<br/> **Richtung:** Client zu Server<br/> **Beschreibung:** Der Client fordert Zugriff auf die Freigabe an. Das Paket enthält den vollständig angegebenen Pfad der Freigabe im UNC-Format.<br/>                                                                                                                                                                                                                                                                                                                                                                                             |
| **Paket 5: SMB \_ COM \_ TREE CONNECT \_ \_ ANDX**<br/> **Richtung:** Server zu Client<br/> **Beschreibung:** Wenn Zugriff auf die Freigabe gewährt wird, gibt der Server die 16-Bit-Struktur-ID (TID) zurück, die der Freigabe in diesem Paket entspricht. Wenn die Freigabe nicht vorhanden ist oder der Benutzer nicht über unzureichende Anmeldeinformationen für den Zugriff auf die Freigabe verfügt, gibt der Server einen Fehlercode in diesem Paket zurück und verweigert den Zugriff auf die Freigabe.<br/>                                                                                                                                                                                                 |
| **Paket 6: SMB \_ COM \_ OPEN \_ ANDX**<br/> **Richtung:** Client zu Server<br/> **Beschreibung:** Der Client fordert den Server auf, im Namen des Clients eine Datei auf der Freigabe zu öffnen, auf die zugegriffen wird. Dieses Paket enthält den Namen der zu öffnenden Datei.<br/>                                                                                                                                                                                                                                                                                                                                                                   |
| **Paket 7: SMB \_ COM \_ OPEN \_ ANDX**<br/> **Richtung:** Server zu Client<br/> **Beschreibung:** Wenn der Zugriff auf die Datei gewährt wird, gibt der Server die Datei-ID der angeforderten Datei zurück. Wenn die Datei nicht vorhanden ist oder der Benutzer nicht über unzureichende Anmeldeinformationen für den Zugriff auf die Datei verfügt, gibt der Server einen Fehlercode in diesem Paket zurück und verweigert den Zugriff auf die Datei.<br/>                                                                                                                                                                                                                                                  |
| **Paket 8: SMB \_ COM \_ READ \_ ANDX**<br/> **Richtung:** Client zu Server<br/> **Beschreibung:** Der Client fordert den Server auf, Daten aus der geöffneten Datei im Namen des Clients zu lesen und an den Client zurücksingen. Die Datei-ID, die vom Client beim Öffnen der Datei erhalten wurde, ist in diesem Paket enthalten, um zu ermitteln, aus welcher geöffneten Datei der Server Daten lesen soll.<br/>                                                                                                                                                                                                                   |
| **Paket 9: SMB \_ COM \_ READ \_ ANDX**<br/> **Richtung:** Server zu Client<br/> **Beschreibung:** Der Server gibt die angeforderten Dateidaten in diesem Paket zurück. Ein Fehler ist hier unwahrscheinlich, da der Zugriff auf den Server, die Freigabe und die Datei gewährt wurde. Dies kann jedoch in einigen Situationen der Fall sein, z. B. wenn der Zugriff auf eine Freigabe zwischen dem Zeitpunkt, zu dem die Datei geöffnet wird, und dem Zeitpunkt, zu dem sie gelesen wird, geändert wird.<br/>                                                                                                                                                                                                      |



 

> [!Note]  
> Wenn Sie ein CIFS implementieren, das keine Änderungsbenachrichtigungen unterstützt, kann Windows kein ausstehendes Handle für das Dateisystem behalten, und die SMB-Verbindung kann ohne vorherige Ankündigung entfernt werden.

 

 

 




