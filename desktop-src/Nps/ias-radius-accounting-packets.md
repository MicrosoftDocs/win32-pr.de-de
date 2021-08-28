---
title: Protokollierung mit Netzwerkrichtlinienserver
description: Protokollierung mit Netzwerkrichtlinienserver
ms.assetid: 903d89bd-c223-4f29-9eaf-1dc28d27a32a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4c6446a6ece75a8da8e51ecab3ed4b6ebf256360e8d9032a676922b83b664d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119778070"
---
# <a name="logging-with-network-policy-server"></a>Protokollierung mit Netzwerkrichtlinienserver

> [!Note]  
> Der Internetauthentifizierungsdienst (INTERNET Authentication Service, IAS) wurde ab Windows Server 2008 in Netzwerkrichtlinienserver (Network Policy Server, NPS) umbenannt. Der Inhalt dieses Themas gilt sowohl für IAS als auch für NPS. Im gesamten Text wird NPS verwendet, um auf alle Versionen des Diensts zu verweisen, einschließlich der Versionen, die ursprünglich als IAS bezeichnet wurden.

 

In der folgenden Tabelle werden nur die wichtigsten Aspekte der RADIUS-Buchhaltungspakete beschrieben. Das Dokument RADIUS Accounting Request for Comments[(RFC 2866](https://www.ietf.org/rfc/rfc2866.txt)) enthält ausführliche Informationen zu diesen Paketen.

RADIUS-Buchhaltungspakete können in die folgenden Kategorien unterteilt werden.



| Buchhaltungspaket  | Beschreibung                                                                                                                                                                                                                |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Accounting-On      | Wird vom Netzwerkzugriffsserver (NAS) gesendet, um anzugeben, dass er neu gestartet wurde.<br/> Enthält nas-identifier/ipaddress.<br/>                                                                                        |
| Accounting-Off     | Wird vom NAS gesendet, um anzugeben, dass es heruntergefahren wird.<br/> Enthält nas-identifier/ipaddress.<br/>                                                                                                            |
| Accounting-Start   | Wird vom NAS gesendet, nachdem der Benutzer authentifiziert und autorisiert wurde, um den Start einer Benutzersitzung anzugeben. <br/> Enthält userid, nas-identifier/ipaddress sowie weitere vom NAS empfangene Informationen.<br/> |
| Accounting-Stop    | Wird vom NAS gesendet, um das Ende einer Benutzersitzung anzugeben.<br/> Enthält userid, nas-identifier/ipaddress sowie weitere vom NAS empfangene Informationen.<br/>                                                      |
| Accounting-Interim | Kann in regelmäßigen Abständen vom NAS für jeden Benutzer gesendet werden, der am NAS angemeldet ist. <br/> Dieses Feature wird in neueren Nas-Versionen allgemein unterstützt.<br/>                                                     |



 

Die folgenden Probleme müssen beim Sammeln von Buchhaltungsinformationen berücksichtigt werden, die über RADIUS zur Verfügung gestellt werden:

-   In seltenen Fällen können Pakete während der Übertragung verlorengehen und den RADIUS-Server möglicherweise nie erreichen.
-   Der RADIUS-Server wird nicht benachrichtigt, wenn der NAS abgebrochen wird.
-   ISDN unterstützt mehrere Sitzungen, und jede Sitzung generiert ein Paar aus Paketen mit Accounting-Start/Stop. Es gibt ein Buchhaltungsattribut namens Multisitzungsbezeichner, das solche Pakete mit mehreren Sitzungen eindeutig identifiziert. Suchen Sie zusätzlich zum Sitzungsbezeichner nach dem Multisitzungsbezeichner, um die Anzahl der Sitzungen zu berechnen.

## <a name="requests-logged-by-nps"></a>Von NPS protokollierte Anforderungen

NpS protokolliert standardmäßig keine Daten. NPS kann mithilfe der NPS-Benutzeroberfläche (nps.msc) konfiguriert werden, um die folgenden Anforderungen zu protokollieren.



| Protokolliertes Paket          | Beschreibung                                                                                                                                  |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Buchhaltungsanforderung     | Eines der in der vorherigen Tabelle beschriebenen Buchhaltungspakete.<br/>                                                                    |
| Authentifizierungsanforderung | Wird vom NAS im Auftrag des verbindenden Benutzers gesendet.<br/> Die Protokolleinträge enthalten nur eingehende Attribute.<br/>                    |
| Authentifizierung akzeptieren  | Wird von NPS gesendet, um anzugeben, dass die Benutzerverbindung akzeptiert werden soll.<br/> Die Protokolleinträge enthalten nur ausgehende Attribute.<br/> |
| Authentifizierung ablehnen  | Wird von NPS gesendet, um anzugeben, dass die Benutzerverbindung abgelehnt werden soll.<br/> Die Protokolleinträge enthalten nur ausgehende Attribute.<br/> |



 

Von NPS protokollierte Daten können in eine Textdatei auf dem NPS-Server oder in eine zentrale SQL Datenbank übertragen werden. Weitere Informationen zur NPS-SQL-Protokollierung finden Sie unter [SQL Programmierbarkeit.](sql-programmability.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Internetauthentifizierungsdienst und Netzwerkrichtlinienserver](internet-authentication-service-vs-network-policy-server.md)
</dt> <dt>

[RADIUS-Authentifizierung, -Autorisierung und -Buchhaltung](/windows/desktop/Nps/ias-radius-authentication-and-accounting)
</dt> <dt>

[Arbeiten mit einem Zustandsserver](/windows/desktop/Nps/ias-working-with-a-state-server)
</dt> </dl>

 

