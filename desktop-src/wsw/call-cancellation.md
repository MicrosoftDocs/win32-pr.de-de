---
title: Anrufabbruch
description: Die Anrufabbruchbenachrichtigung bricht den Vorgang serverseitiger Dienstvorgänge und Dienstmodellrückrufe ab.
ms.assetid: dc371921-869f-4775-98d3-80a1006358ba
keywords:
- Aufrufabbruchwebdienste für Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dda4ec4227403bed5239b68cfa05d2064976517a7473fa7926c8de5f56227645
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119026698"
---
# <a name="call-cancellation"></a>Anrufabbruch

Die Anrufabbruchbenachrichtigung bricht den Vorgang [serverseitiger Dienstvorgänge und](server-side-service-operations.md) Dienstmodellrückrufe ab. Ein solcher Abbruch kann aus zwei Gründen auftreten:

-   Der Diensthost hat Vorgänge aufgrund eines Aufrufs der [**WsAbortServiceHost-Funktion**](/windows/desktop/api/WebServices/nf-webservices-wsabortservicehost) beendet.
-   Der zugrunde liegende Kanal hat einen Fehler ausgelöst.


Um eine Abbruchbenachrichtigung zu erhalten, muss der Dienstvorgang oder Dienstmodellrückruf einen [**WS \_ OPERATION CANCEL \_ \_ CALLBACK-Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_cancel_callback) registrieren, indem die [**WsRegisterOperationForCancel-Funktion**](/windows/desktop/api/WebServices/nf-webservices-wsregisteroperationforcancel) aufruft.

Optional kann der Dienstvorgang oder Dienstmodellrückruf im Rahmen der Registrierung für abbruchbenachrichtigungen auch anwendungsspezifische Zustandsdaten und den [**RÜCKRUF-Rückruf des \_ WS-VORGANGS FREE \_ \_ STATE \_**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_free_state_callback) registrieren.

Die Zustandsdaten werden dem [**Rückruf WS \_ OPERATION CANCEL \_ \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_cancel_callback) zur Verfügung gestellt. Bei Abschluss des Aufrufs wird der [**RÜCKRUF-Rückruf für den \_ WS-VORGANG FREE \_ \_ STATE \_**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_free_state_callback) aufgerufen, um der Anwendung die Möglichkeit zu geben, die Zustandsdaten frei zu geben.

Ein Codebeispiel finden Sie unter [BlockingServiceExample](blockingserviceexample.md).

Der Abbruchrückruf wird nur einmal für die Lebensdauer der [serverseitigen](server-side-service-operations.md) Dienstvorgänge oder Rückruffunktion aufgerufen.

Der Aufrufabbruch ist in für alle Diensthostrückrufe verfügbar, die [WS \_ OPERATION \_ CONTEXT](ws-operation-context.md) als Parameter verwenden.

Die folgenden API-Elemente beziehen sich auf den Aufrufabbruch.

| Rückruf                                                                         | BESCHREIBUNG                                                                                                                                |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [**RÜCKRUF ZUM \_ ABBRECHEN DES \_ WS-VORGANGS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_cancel_callback)          | Wird vom Dienstmodell aufgerufen, um einen Abbruch eines asynchronen Dienstvorgang als Ergebnis eines abgebrochenen Herunterfahrens des Diensthosts zu benachrichtigen. |
| [**RÜCKRUF FÜR \_ DEN FREIEN ZUSTAND DES \_ WS-VORGANGS \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_free_state_callback) | Wird vom Dienstmodell aufgerufen, damit eine Anwendung Zustandsdaten bereinigt, die beim Abbruchrückruf registriert wurden.                |



 



| Funktion                                                             | BESCHREIBUNG                                                                                       |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**WsRegisterOperationForCancel**](/windows/desktop/api/WebServices/nf-webservices-wsregisteroperationforcancel) | Ermöglicht es einem Dienstvorgang oder einem Dienstmodellrückruf, sich für eine Abbruchbenachrichtigung zu registrieren. |



 

 

 




