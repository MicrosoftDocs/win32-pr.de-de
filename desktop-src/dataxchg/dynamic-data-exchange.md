---
title: dynamische Daten Exchange
description: Dieser Abschnitt enthält Richtlinien zum Implementieren des dynamischen Datenaustauschs für Anwendungen, die die dynamische Daten Exchange Management Library (DDEML) nicht verwenden können.
ms.assetid: vs|winui|~\winui\windowsuserinterface\dataexchange\dynamicdataexchange.htm
keywords:
- dynamische Daten Exchange (DDE), Informationen
- DDE (dynamische Daten Exchange),about
- Datenaustausch,dynamische Daten Exchange (DDE)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4db58f1027f0dfaacf28c4b2ec8d4208747929b0d40ca55d7d377831777f78a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119678040"
---
# <a name="dynamic-data-exchange"></a>dynamische Daten Exchange

Dieser Abschnitt enthält Richtlinien zum Implementieren des dynamischen Datenaustauschs für Anwendungen, die die dynamische Daten Exchange Management Library (DDEML) nicht verwenden können. Weitere Informationen zur DDEML finden Sie unter dynamische Daten Exchange [Management Library](dynamic-data-exchange-management-library.md).

### <a name="overviews"></a>Übersichten



| Name                                                           | BESCHREIBUNG                                                        |
|----------------------------------------------------------------|--------------------------------------------------------------------|
| [Informationen dynamische Daten Exchange](about-dynamic-data-exchange.md) | Erläutert das Übertragen von Daten zwischen Anwendungen.<br/>       |
| [Verwenden dynamische Daten Exchange](using-dynamic-data-exchange.md) | Stellt Codebeispiele zum dynamischen Datenaustausch zur Verfügung.<br/> |
| [DDE-Referenz](dynamic-data-exchange-reference.md)           | Die API-Referenz.<br/>                                      |



 

### <a name="dde-functions"></a>DDE-Funktionen



| Name                                                             | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DdeSetQualityOfService**](/windows/desktop/api/Dde/nf-dde-ddesetqualityofservice)         | Gibt die Servicequalität (Quality of Service, QOS) an, die eine unformatiert dynamische Daten Exchange(DDE)-Anwendung für zukünftige DDE-Konversationen angibt, die sie initiiert. Das angegebene QOS gilt für alle Konversationen, die gestartet werden, während diese Einstellungen festgelegt sind. Die Dienstqualität einer DDE-Konversation dauert für die Dauer der Konversation. Aufrufe der [**DdeSetQualityOfService-Funktion**](/windows/desktop/api/Dde/nf-dde-ddesetqualityofservice) während einer Konversation wirken sich nicht auf das QOS dieser Konversation aus. <br/> |
| [**FreeDDElParam**](/windows/desktop/api/Dde/nf-dde-freeddelparam)                           | Gibt den durch den *lParam-Parameter* einer gesendeten DDE-Nachricht angegebenen Arbeitsspeicher frei. Eine Anwendung, die eine gesendete DDE-Nachricht empfängt, sollte diese Funktion aufrufen, nachdem sie die [**UnpackDDElParam-Funktion**](/windows/desktop/api/Dde/nf-dde-unpackddelparam) verwendet hat, um den *lParam-Wert zu* entpacken. <br/>                                                                                                                                                                                                     |
| [**ImpersonateDdeClientWindow**](/windows/desktop/api/Dde/nf-dde-impersonateddeclientwindow) | Ermöglicht einer DDE-Serveranwendung das Identitätswechseln des Sicherheitskontexts einer DDE-Clientanwendung. Dadurch werden sichere Serverdaten vor nicht autorisierten DDE-Clients geschützt. <br/>                                                                                                                                                                                                                                                                                                      |
| [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam)                           | Packt einen DDE *lParam-Wert* in eine interne Struktur, die zum Freigeben von DDE-Daten zwischen Prozessen verwendet wird.<br/>                                                                                                                                                                                                                                                                                                                                                                 |
| [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam)                         | Ermöglicht es einer Anwendung, einen gepackten DDE *lParam-Parameter* wiederzuverwenden, anstatt einen neuen gepackten *lParam-Parameter zu zuordnen.* Die Verwendung dieser Funktion reduziert Neuzuordnungen für Anwendungen, die gepackte DDE-Nachrichten übergeben. <br/>                                                                                                                                                                                                                                                          |
| [**UnpackDDElParam**](/windows/desktop/api/Dde/nf-dde-unpackddelparam)                       | Entpackt einen DDE *lParam-Wert,* der von einer gesendeten DDE-Nachricht empfangen wurde. <br/>                                                                                                                                                                                                                                                                                                                                                                                                  |



 

### <a name="dde-messages"></a>DDE-Nachrichten



| Name                                         | BESCHREIBUNG                                                                                                                                                                                                                                                                                      |
|----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ DDE \_ INITIATE**](wm-dde-initiate.md) | Initiiert eine Konversation mit einer Serveranwendung, die auf die angegebenen Anwendungs- und Themennamen antwortet. Nach dem Empfang dieser Meldung wird erwartet, dass alle Serveranwendungen mit Namen, die der angegebenen Anwendung übereinstimmen und das angegebene Thema unterstützen, dies bestätigen.<br/> |



 

### <a name="dde-notifications"></a>DDE-Benachrichtigungen



| Name                                           | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ DDE \_ ACK**](wm-dde-ack.md)             | Benachrichtigt eine DDE-Anwendung über den Empfang und die Verarbeitung der folgenden Nachrichten: [**WM \_ DDE \_ POKE,**](wm-dde-poke.md) [**WM \_ DDE \_ EXECUTE,**](wm-dde-execute.md) [**WM \_ DDE \_ DATA, WM**](wm-dde-data.md) [**\_ DDE \_ ADVISE,**](wm-dde-advise.md) [**WM \_ DDE \_ UNADVISE,**](wm-dde-unadvise.md) [**WM \_ DDE \_ INITIATE**](wm-dde-initiate.md)oder [**WM \_ DDE \_ REQUEST**](wm-dde-request.md) (in einigen Fällen). <br/> |
| [**WM \_ DDE \_ ADVISE**](wm-dde-advise.md)       | Eine DDE-Clientanwendung sendet die [**WM \_ DDE \_ ADVISE-Nachricht**](wm-dde-advise.md) an eine DDE-Serveranwendung, um den Server auf die Bereitstellung eines Updates für ein Datenelement zu bitten, wenn sich das Element ändert. <br/>                                                                                                                                                                                                              |
| [**WM \_ DDE \_ DATA**](wm-dde-data.md)           | Eine DDE-Serveranwendung sendet eine [**WM \_ DDE \_ DATA-Nachricht**](wm-dde-data.md) an eine DDE-Clientanwendung, um ein Datenelement an den Client zu übergeben oder den Client über die Verfügbarkeit eines Datenelements zu benachrichtigen. <br/>                                                                                                                                                                                                           |
| [**WM \_ DDE \_ EXECUTE**](wm-dde-execute.md)     | Eine DDE-Clientanwendung sendet eine [**WM \_ DDE \_ EXECUTE-Nachricht**](wm-dde-execute.md) an eine DDE-Serveranwendung, um eine Zeichenfolge an den Server zu senden, die als Eine Reihe von Befehlen verarbeitet werden soll. Es wird erwartet, dass die Serveranwendung als Antwort eine [**WM \_ DDE \_ ACK-Nachricht**](wm-dde-ack.md) sendet. <br/>                                                                                                                      |
| [**WM \_ DDE \_ POKE**](wm-dde-poke.md)           | Eine DDE-Clientanwendung sendet eine [**WM \_ DDE \_ POKE-Nachricht**](wm-dde-poke.md) an eine DDE-Serveranwendung. Ein Client verwendet diese Meldung, um den Server anfordert, ein nicht angefordertes Datenelement zu akzeptieren. Es wird erwartet, dass der Server mit einer [**WM \_ DDE \_ ACK-Meldung**](wm-dde-ack.md) antwortet, die angibt, ob er das Datenelement akzeptiert hat. <br/>                                                                                   |
| [**WM \_ \_ DDE-ANFORDERUNG**](wm-dde-request.md)     | Eine DDE-Clientanwendung sendet eine [**WM \_ DDE \_ REQUEST-Nachricht**](wm-dde-request.md) an eine DDE-Serveranwendung, um den Wert eines Datenelements an fordern zu können. <br/>                                                                                                                                                                                                                                                              |
| [**WM \_ DDE \_ TERMINATE**](wm-dde-terminate.md) | Eine DDE-Anwendung (Client oder Server) sendet eine [**WM \_ DDE \_ TERMINATE-Nachricht,**](wm-dde-terminate.md) um eine Konversation zu beenden. <br/>                                                                                                                                                                                                                                                                                  |
| [**WM \_ DDE \_ UNADVISE**](wm-dde-unadvise.md)   | Eine DDE-Clientanwendung sendet eine [**WM \_ DDE \_ UNADVISE-Meldung,**](wm-dde-unadvise.md) um eine DDE-Serveranwendung darüber zu informieren, dass das angegebene Element oder ein bestimmtes Zwischenablageformat für das Element nicht mehr aktualisiert werden soll. Dadurch wird der Warm- oder Hot-Datenlink für das angegebene Element beendet. <br/>                                                                                                                     |



 

### <a name="dde-structures"></a>DDE-Strukturen



| Name                           | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DDEACK**](/windows/desktop/api/Dde/ns-dde-ddeack)       | Enthält Statusflags, die eine DDE-Anwendung als Teil der [**WM \_ DDE \_ ACK-Nachricht**](wm-dde-ack.md) an ihren Partner übergibt. Die Flags enthalten Details zur Antwort der Anwendung auf die Nachrichten [**WM \_ DDE \_ DATA**](wm-dde-data.md), [**WM \_ DDE \_ POKE**](wm-dde-poke.md), [**WM \_ DDE \_ EXECUTE**](wm-dde-execute.md), [**WM \_ DDE \_ ADVISE**](wm-dde-advise.md), [**WM \_ DDE \_ UNADVISE**](wm-dde-unadvise.md)und [**WM \_ DDE \_ REQUEST**](wm-dde-request.md). <br/> |
| [**DDEADVISE**](/windows/desktop/api/Dde/ns-dde-ddeadvise) | Enthält Flags, die angeben, wie eine DDE-Serveranwendung Daten während einer Advise-Schleife an eine Clientanwendung senden soll. Ein Client übergibt als Teil einer WM DDE ADVISE-Nachricht ein Handle an eine [**DDEADVISE-Struktur**](/windows/desktop/api/Dde/ns-dde-ddeadvise) [**\_ an \_ einen**](wm-dde-advise.md) Server. <br/>                                                                                                                                                                                               |
| [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata)     | Enthält die Daten und Informationen zu den Daten, die als Teil einer [**WM \_ DDE \_ DATA-Nachricht gesendet**](wm-dde-data.md) werden. <br/>                                                                                                                                                                                                                                                                                                                                                       |
| [**DDEPOKE**](/windows/desktop/api/Dde/ns-dde-ddepoke)     | Enthält die Daten und Informationen zu den Daten, die als Teil einer [**WM \_ DDE \_ POKE-Nachricht gesendet**](wm-dde-poke.md) werden. <br/>                                                                                                                                                                                                                                                                                                                                                       |
| [**HSZPAIR**](/windows/win32/api/ddeml/ns-ddeml-hszpair)     | Enthält einen DDE-Dienstnamen und einen Themennamen. Eine DDE-Serveranwendung kann diese Struktur während einer [**XTYP \_ WILDCONNECT-Transaktion**](xtyp-wildconnect.md) verwenden, um die unterstützten Dienst-Themen-Paare zu aufzählen. <br/>                                                                                                                                                                                                                                                   |



 

 

 





