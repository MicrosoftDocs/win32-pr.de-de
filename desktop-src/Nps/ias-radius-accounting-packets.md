---
title: Protokollierung mit dem Netzwerk Richtlinien Server
description: Protokollierung mit dem Netzwerk Richtlinien Server
ms.assetid: 903d89bd-c223-4f29-9eaf-1dc28d27a32a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5117ce15731ea656913b47525387a48a39aa414c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315837"
---
# <a name="logging-with-network-policy-server"></a>Protokollierung mit dem Netzwerk Richtlinien Server

> [!Note]  
> Der Internet Authentifizierungsdienst (IAS) wurde ab Windows Server 2008 in den Netzwerk Richtlinien Server (Network Policy Server, NPS) umbenannt. Der Inhalt dieses Themas gilt sowohl für IAS als auch für NPS. Im gesamten Text wird NPS verwendet, um auf alle Versionen des Dienstanbieter zu verweisen, einschließlich der Versionen, die ursprünglich als IAS bezeichnet wurden.

 

In der folgenden Tabelle werden nur die wichtigsten Aspekte der RADIUS-Buchhaltungs Pakete beschrieben. In der RADIUS-Buchhaltungs Anforderung für Kommentare ([RFC 2866](https://www.ietf.org/rfc/rfc2866.txt)) finden Sie ausführliche Informationen zu diesen Paketen.

RADIUS-Buchhaltungs Pakete können in die folgenden Kategorien unterteilt werden.



| Buchhaltungs Paket  | BESCHREIBUNG                                                                                                                                                                                                                |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Accounting-On      | Wird vom Netzwerk Zugriffs Server (NAS) gesendet, um anzugeben, dass er neu gestartet wurde.<br/> Enthält NAS-Identifier/IPAddress.<br/>                                                                                        |
| Accounting-Off     | Wird vom NAS gesendet, um anzugeben, dass es heruntergefahren wird.<br/> Enthält NAS-Identifier/IPAddress.<br/>                                                                                                            |
| Accounting-Start   | Wird vom NAS gesendet, nachdem der Benutzer authentifiziert und autorisiert wurde, um den Start einer Benutzersitzung anzugeben. <br/> Enthält UserID, NAS-Identifier/IPAddress sowie andere Informationen, die vom NAS empfangen werden.<br/> |
| Accounting-Stop    | Wird vom NAS gesendet, um das Ende einer Benutzersitzung anzugeben.<br/> Enthält UserID, NAS-Identifier/IPAddress sowie andere Informationen, die vom NAS empfangen werden.<br/>                                                      |
| Accounting-Interim | Kann in regelmäßigen Abständen vom NAS für jeden Benutzer gesendet werden, der beim NAS angemeldet ist. <br/> Diese Funktion wird im Allgemeinen in neueren Versionen von NAS unterstützt.<br/>                                                     |



 

Beim Erfassen von Buchhaltungsinformationen, die über RADIUS verfügbar gemacht werden, sind folgende Punkte zu beachten:

-   In seltenen Fällen können Pakete während der Übertragung verloren gehen und den RADIUS-Server möglicherweise nie erreichen.
-   Der RADIUS-Server wird nicht benachrichtigt, wenn das NAS abbricht.
-   ISDN unterstützt mehrere Sitzungen, und jede Sitzung generiert ein paar von Paketen, die eine Buchführung starten/beenden. Es gibt ein Buchhaltungs Attribut mit dem Namen "mehrfache Sitzungs Bezeichner", mit dem solche Pakete mit mehreren Sitzungen eindeutig identifiziert werden. Überprüfen Sie zusätzlich zur Sitzungs-ID den Bezeichner für mehrere Sitzungen, um die Anzahl der Sitzungen zu berechnen.

## <a name="requests-logged-by-nps"></a>Von NPS protokollierte Anforderungen

NPS protokolliert standardmäßig keine Daten. NPS kann mithilfe der NPS-Benutzeroberfläche (NPS. msc) konfiguriert werden, um die folgenden Anforderungen zu protokollieren.



| Protokolliertes Paket          | BESCHREIBUNG                                                                                                                                  |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Buchhaltungs Anforderung     | Alle in der vorherigen Tabelle beschriebenen Buchhaltungs Pakete.<br/>                                                                    |
| Authentifizierungsanforderung | Wird vom NAS im Auftrag des Benutzers gesendet, der eine Verbindung herstellt.<br/> Die Protokolleinträge enthalten nur eingehende Attribute.<br/>                    |
| Authentifizierungs Annahme  | Wird von NPS gesendet, um anzugeben, dass die Benutzer Verbindung akzeptiert werden soll.<br/> Die Protokolleinträge enthalten nur ausgehende Attribute.<br/> |
| Authentifizierung ablehnen  | Wird von NPS gesendet, um anzugeben, dass die Benutzer Verbindung abgelehnt werden soll.<br/> Die Protokolleinträge enthalten nur ausgehende Attribute.<br/> |



 

Daten, die von NPS protokolliert werden, können in eine Textdatei auf dem NPS-Server oder in eine zentrale SQL-Datenbank aufgenommen werden. Weitere Informationen zur NPS-SQL-Protokollierung finden Sie unter [SQL-Programmierbarkeit](sql-programmability.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Internet Authentifizierungsdienst und Netzwerk Richtlinien Server](internet-authentication-service-vs-network-policy-server.md)
</dt> <dt>

[RADIUS-Authentifizierung,-Autorisierung und-Kontoführung](/windows/desktop/Nps/ias-radius-authentication-and-accounting)
</dt> <dt>

[Arbeiten mit einem Zustands Server](/windows/desktop/Nps/ias-working-with-a-state-server)
</dt> </dl>

 

