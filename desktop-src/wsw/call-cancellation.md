---
title: Abbruch Abbrechen
description: Die Aufruf Abbruch Benachrichtigung bricht den Betrieb der serverseitigen Dienst Vorgänge und Dienstmodell Rückrufe ab.
ms.assetid: dc371921-869f-4775-98d3-80a1006358ba
keywords:
- Aufrufe von Abbruch-Webdiensten für Windows
- Wwsapi
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5107f9ece421a3130f99c78b3b33788ee6c7e9f0
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "106337693"
---
# <a name="call-cancellation"></a>Abbruch Abbrechen

Die Aufruf Abbruch Benachrichtigung bricht den Betrieb der [serverseitigen Dienst Vorgänge](server-side-service-operations.md) und Dienstmodell Rückrufe ab. Ein solcher Abbruch kann aus zwei Gründen erfolgen:

-   Der Dienst Host hat Vorgänge aufgrund eines Aufrufes der [**wsabortservicehost**](/windows/desktop/api/WebServices/nf-webservices-wsabortservicehost) -Funktion beendet.
-   Der zugrunde liegende Kanal hat einen Fehler ausgelöst.


Um eine Abbruch Benachrichtigung zu erhalten, muss der Dienst Vorgang oder der Dienstmodell Rückruf einen [**WS- \_ Vorgangs \_ Abbruch- \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_cancel_callback) Rückruf registrieren, indem die [**wsregisteroperationforcancel**](/windows/desktop/api/WebServices/nf-webservices-wsregisteroperationforcancel) -Funktion aufgerufen wird.

Optional kann der Dienst Vorgang oder der Dienstmodell Rückruf im Rahmen der Registrierung für eine Abbruch Benachrichtigung auch anwendungsspezifische Zustandsdaten und den Rückruf Rückruf für den [**WS \_ - \_ Vorgangs \_ freien \_ Status**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_free_state_callback) registrieren.

Die Zustandsdaten werden für den WS- [**\_ Vorgang zum \_ Abbrechen des \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_cancel_callback) Rückrufs verfügbar gemacht. Bei der Beendigung des Aufrufs wird der Rückruf Rückruf Rückruf für den WS-Vorgang aufgerufen, um der Anwendung die Möglichkeit zu geben, die Zustandsdaten freizugeben. [**\_ \_ \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_free_state_callback)

Ein Codebeispiel finden Sie unter [blockingserviceexample](blockingserviceexample.md).

Der Abbruch Rückruf wird nur einmal für die Lebensdauer der [serverseitigen Dienst Vorgänge](server-side-service-operations.md) oder Rückruffunktion aufgerufen.

Der Aufruf Abbruch ist in für alle Dienst Host Rückrufe verfügbar, die den [WS- \_ Vorgangs \_ Kontext](ws-operation-context.md) als Parameter annehmen.

Die folgenden API-Elemente beziehen sich auf den Abbruch von anrufen.

| Rückruf                                                                         | BESCHREIBUNG                                                                                                                                |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [**WS- \_ Vorgang \_ Abbruch \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_cancel_callback)          | Wird vom Dienstmodell aufgerufen, um einen Abbruch eines asynchronen Dienst Vorgangs aufgrund eines abgebrochenen herunter Fahrens des Dienst Hosts zu benachrichtigen. |
| [**WS- \_ Vorgang, \_ freier \_ Zustands \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_free_state_callback) | Wird vom Dienstmodell aufgerufen, um einer Anwendung das Bereinigen von Zustandsdaten zu ermöglichen, die beim Abbruch Rückruf registriert wurden.                |



 



| Funktion                                                             | BESCHREIBUNG                                                                                       |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**Wsregisteroperationforcancel**](/windows/desktop/api/WebServices/nf-webservices-wsregisteroperationforcancel) | Ermöglicht, dass ein Dienst Vorgang oder ein Dienstmodell Rückruf für eine Abbruch Benachrichtigung registriert wird. |



 

 

 




