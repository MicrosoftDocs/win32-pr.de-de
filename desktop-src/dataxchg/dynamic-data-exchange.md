---
title: dynamischer Datenaustausch
description: Dieser Abschnitt enthält Richtlinien für die Implementierung des dynamischen Datenaustauschs für Anwendungen, die nicht die dynamischer Datenaustausch Management Library (Ddeml) verwenden können.
ms.assetid: vs|winui|~\winui\windowsuserinterface\dataexchange\dynamicdataexchange.htm
keywords:
- Dynamischer Datenaustausch (DDE), Informationen zu
- DDE (dynamischer Datenaustausch), Informationen zu
- Datenaustausch, dynamischer Datenaustausch (DDE)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91d5fa52078c2fa1d2e67a74d019535c801c4c96
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310207"
---
# <a name="dynamic-data-exchange"></a>dynamischer Datenaustausch

Dieser Abschnitt enthält Richtlinien für die Implementierung des dynamischen Datenaustauschs für Anwendungen, die nicht die dynamischer Datenaustausch Management Library (Ddeml) verwenden können. Weitere Informationen zur DDEML finden Sie unter [dynamischer Datenaustausch-Verwaltungs Bibliothek](dynamic-data-exchange-management-library.md).

### <a name="overviews"></a>Übersichten



| Name                                                           | BESCHREIBUNG                                                        |
|----------------------------------------------------------------|--------------------------------------------------------------------|
| [Informationen zu dynamischer Datenaustausch](about-dynamic-data-exchange.md) | Erläutert das Übertragen von Daten zwischen Anwendungen.<br/>       |
| [Verwenden von dynamischer Datenaustausch](using-dynamic-data-exchange.md) | Enthält Codebeispiele zum dynamischen Datenaustausch.<br/> |
| [DDE-Referenz](dynamic-data-exchange-reference.md)           | Die API-Referenz.<br/>                                      |



 

### <a name="dde-functions"></a>DDE-Funktionen



| Name                                                             | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Ddesetqualityofservice**](/windows/desktop/api/Dde/nf-dde-ddesetqualityofservice)         | Gibt die Quality of Service (QoS) an, die eine DDE-Anwendung (RAW dynamischer Datenaustausch) für künftige DDE-Konversationen, die Sie initiiert, wünscht Das angegebene QoS gilt für alle Unterhaltungen, die gestartet werden, während diese Einstellungen vorhanden sind. Die Quality of Service der DDE-Konversation dauert für die Dauer der Konversation. Aufrufe der [**ddesetqualityofservice**](/windows/desktop/api/Dde/nf-dde-ddesetqualityofservice) -Funktion während einer Konversation haben keine Auswirkung auf die QoS der Konversation. <br/> |
| [**Freeddelta param**](/windows/desktop/api/Dde/nf-dde-freeddelparam)                           | Gibt den durch den *LPARAM* -Parameter einer geposteten DDE-Nachricht angegebenen Arbeitsspeicher frei. Eine Anwendung, die eine bereitgestellte DDE-Nachricht empfängt, sollte diese Funktion nach dem Entpacken des *LPARAM* -Werts mit der [**unpackddelta param**](/windows/desktop/api/Dde/nf-dde-unpackddelparam) -Funktion verwenden. <br/>                                                                                                                                                                                                     |
| [**Identitätsnachweis für Identitätswechsel**](/windows/desktop/api/Dde/nf-dde-impersonateddeclientwindow) | Ermöglicht einer DDE-Serveranwendung, die Identität des Sicherheits Kontexts einer DDE-Client Anwendung anzunehmen. Dies schützt sichere Serverdaten vor nicht autorisierten DDE-Clients. <br/>                                                                                                                                                                                                                                                                                                      |
| [**Packddelta param**](/windows/desktop/api/Dde/nf-dde-packddelparam)                           | Packt einen DDE *LPARAM* -Wert in eine interne Struktur, die zum Freigeben von DDE-Daten zwischen Prozessen verwendet wird.<br/>                                                                                                                                                                                                                                                                                                                                                                 |
| [**Reuseddelta param**](/windows/desktop/api/Dde/nf-dde-reuseddelparam)                         | Ermöglicht es einer Anwendung, einen gepackten DDE- *LPARAM* -Parameter zu verwenden, anstatt einen neuen gepackten *LPARAM* zuzuordnen. Die Verwendung dieser Funktion reduziert die Neuzuordnung von Anwendungen, die gepackte DDE-Nachrichten übergeben. <br/>                                                                                                                                                                                                                                                          |
| [**Unpackddelta param**](/windows/desktop/api/Dde/nf-dde-unpackddelparam)                       | Entpackt einen DDE *LPARAM* -Wert, der von einer bereitstellten DDE-Nachricht empfangen wurde. <br/>                                                                                                                                                                                                                                                                                                                                                                                                  |



 

### <a name="dde-messages"></a>DDE-Nachrichten



| Name                                         | BESCHREIBUNG                                                                                                                                                                                                                                                                                      |
|----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ DDE \_ initiieren**](wm-dde-initiate.md) | Initiiert eine Konversation mit einer Serveranwendung, die auf die angegebenen Anwendungs-und Themen Namen antwortet. Wenn diese Nachricht empfangen wird, wird Sie von allen Server Anwendungen mit Namen, die der angegebenen Anwendung entsprechen und die das angegebene Thema unterstützen, erwartet.<br/> |



 

### <a name="dde-notifications"></a>DDE-Benachrichtigungen



| Name                                           | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM-DDE-Bestätigung \_ \_**](wm-dde-ack.md)             | Nbenachrichtigt eine DDE-Anwendung über den Empfang und die Verarbeitung der folgenden Meldungen: [**WM \_ DDE \_ Poke**](wm-dde-poke.md), [**WM \_ DDE \_ Execute**](wm-dde-execute.md), [**WM \_ DDE \_ Data**](wm-dde-data.md), [**WM \_ DDE- \_ Empfehlung**](wm-dde-advise.md), [**WM \_ DDE \_ unempfehlung**](wm-dde-unadvise.md), [**WM \_ DDE \_ initiieren**](wm-dde-initiate.md)oder [**WM \_ DDE- \_ Anforderung**](wm-dde-request.md) (in einigen Fällen). <br/> |
| [**WM \_ DDE- \_ Empfehlung**](wm-dde-advise.md)       | Eine DDE-Client Anwendung sendet die Mitteilung " [**WM \_ DDE- \_ Empfehlung**](wm-dde-advise.md) " an eine DDE-Serveranwendung, um den Server aufzufordern, ein Update für ein Datenelement bereitzustellen, wenn das Element geändert wird. <br/>                                                                                                                                                                                                              |
| [**WM- \_ DDE- \_ Daten**](wm-dde-data.md)           | Eine DDE-Serveranwendung sendet eine [**WM- \_ DDE- \_ Daten**](wm-dde-data.md) Nachricht an eine DDE-Client Anwendung, um ein Datenelement an den Client zu übergeben oder den Client über die Verfügbarkeit eines Datenelements zu benachrichtigen. <br/>                                                                                                                                                                                                           |
| [**WM \_ DDE \_ Ausführen**](wm-dde-execute.md)     | Eine DDE-Client Anwendung sendet eine [**WM- \_ DDE- \_ Ausführungs**](wm-dde-execute.md) Nachricht an eine DDE-Serveranwendung, um eine Zeichenfolge an den Server zu senden, die als eine Reihe von Befehlen verarbeitet werden soll. Die Serveranwendung sendet eine [**WM- \_ DDE \_**](wm-dde-ack.md) -Bestätigungsnachricht als Antwort. <br/>                                                                                                                      |
| [**WM \_ DDE \_ Poke**](wm-dde-poke.md)           | Eine DDE-Client Anwendung sendet eine [**WM- \_ DDE- \_ Poke**](wm-dde-poke.md) -Nachricht an eine DDE-Serveranwendung. Ein Client verwendet diese Nachricht, um den Server aufzufordern, ein nicht angefordertes Datenelement zu akzeptieren. Der Server antwortet mit einer [**WM- \_ DDE \_**](wm-dde-ack.md) -Bestätigungsmeldung, die angibt, ob das Datenelement akzeptiert wurde. <br/>                                                                                   |
| [**WM- \_ DDE- \_ Anforderung**](wm-dde-request.md)     | Eine DDE-Client Anwendung sendet eine [**WM- \_ DDE- \_ Anforderungs**](wm-dde-request.md) Nachricht an eine DDE-Serveranwendung, um den Wert eines Datenelements anzufordern. <br/>                                                                                                                                                                                                                                                              |
| [**WM- \_ DDE \_ Beenden**](wm-dde-terminate.md) | Eine DDE-Anwendung (Client oder Server) sendet eine [**WM-DDE-Beendigungs \_ \_**](wm-dde-terminate.md) Nachricht, um eine Konversation zu beenden. <br/>                                                                                                                                                                                                                                                                                  |
| [**WM \_ DDE \_ nicht Empfehlung**](wm-dde-unadvise.md)   | Eine DDE-Client Anwendung sendet eine Fehlermeldung vom Typ " [**WM \_ DDE \_ unempfehlung**](wm-dde-unadvise.md) ", um eine DDE Server-Anwendung zu informieren, dass das angegebene Element oder ein bestimmtes Zwischenablage Format für das Element nicht mehr aktualisiert werden soll. Dadurch wird der Daten Link warm oder Hot für das angegebene Element beendet. <br/>                                                                                                                     |



 

### <a name="dde-structures"></a>DDE-Strukturen



| Name                           | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DDE ACK**](/windows/desktop/api/Dde/ns-dde-ddeack)       | Enthält Statusflags, die eine DDE-Anwendung als Teil der [**WM \_ DDE \_ ACK**](wm-dde-ack.md) -Nachricht an Ihren Partner übergibt. Die Flags enthalten Details zur Antwort der Anwendung auf die Nachrichten [**WM- \_ DDE- \_ Daten**](wm-dde-data.md), [**WM \_ DDE \_ Poke**](wm-dde-poke.md), [**WM \_ DDE \_ Execute**](wm-dde-execute.md), [**WM DDE- \_ \_ Empfehlung**](wm-dde-advise.md), [**WM \_ DDE \_ unrequest**](wm-dde-unadvise.md)und [**WM \_ DDE \_ Request**](wm-dde-request.md). <br/> |
| [**DDE-Empfehlung**](/windows/desktop/api/Dde/ns-dde-ddeadvise) | Enthält Flags, die angeben, wie eine DDE-Serveranwendung während einer Benachrichtigungs Schleife Daten an eine Client Anwendung senden soll. Ein Client übergibt ein Handle an eine [**ddeberatungsstruktur**](/windows/desktop/api/Dde/ns-dde-ddeadvise) an einen Server als Teil einer [**WM- \_ DDE- \_ Empfehlung**](wm-dde-advise.md) -Nachricht. <br/>                                                                                                                                                                                               |
| [**DDE-Daten**](/windows/desktop/api/Dde/ns-dde-ddedata)     | Enthält die Daten und Informationen zu den Daten, die als Teil einer WM- [**\_ DDE- \_ Daten**](wm-dde-data.md) Nachricht gesendet werden. <br/>                                                                                                                                                                                                                                                                                                                                                       |
| [**DDE Poke**](/windows/desktop/api/Dde/ns-dde-ddepoke)     | Enthält die Daten und Informationen zu den Daten, die als Teil einer WM- [**\_ DDE- \_ Poke**](wm-dde-poke.md) -Nachricht gesendet werden. <br/>                                                                                                                                                                                                                                                                                                                                                       |
| [**Hszpair**](/windows/win32/api/ddeml/ns-ddeml-hszpair)     | Enthält einen DDE-Dienstnamen und einen Themen Namen. Eine DDE-Serveranwendung kann diese Struktur während einer [**xpair \_ wildconnect**](xtyp-wildconnect.md) -Transaktion verwenden, um die unterstützten Dienst Themen Paare aufzulisten. <br/>                                                                                                                                                                                                                                                   |



 

 

 





