---
title: Fehler
description: Eine Fehlermeldung wird verwendet, um Fehlerinformationen über einen Fehler an einem Remote Endpunkt zu übermitteln.
ms.assetid: d2bada50-2ddd-4f7f-9b25-7bbec77b431b
keywords:
- Fehler-Webdienste für Windows
- Wwsapi
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b2ecad1b63335b7f2bfc81c099b4f920d9de21c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341432"
---
# <a name="faults"></a>Fehler

Eine Fehlermeldung wird verwendet, um Fehlerinformationen über einen Fehler an einem Remote Endpunkt zu übermitteln. Eine Fehlermeldung ist wie jede andere Nachricht, mit dem Unterschied, dass das Format des Nachrichten Texts ein Standardformat aufweist. Fehler können sowohl von Infrastruktur Protokollen, wie z. b. WS-Adressierung, als auch von Anwendungs Protokollen höherer Ebene verwendet werden.

-   [Übersicht](#overview)
-   [Erzeugen von Fehlern in einem Dienst](#generating-faults-in-a-service)
-   [Behandeln von Fehlern auf einem Client](#handling-faults-on-a-client)
-   [Verwenden von Fehlern mit Nachrichten](#using-faults-with-messages)

## <a name="overview"></a>Übersicht

Der Inhalt des Texts einer Fehlermeldung wird in dieser API mithilfe der [**WS- \_ Fehler**](/windows/desktop/api/WebServices/ns-webservices-ws_fault) Struktur dargestellt. Obwohl ein Fehler einen festgelegten Satz von Feldern hat, die zum Bereitstellen von Informationen über den Fehler verwendet werden (z. b. der [**WS- \_ Fehler \_ Code**](/windows/desktop/api/WebServices/ns-webservices-ws_fault_code) , der den Fehlertyp identifiziert, und die [**WS- \_ Fehler \_ Ursache**](/windows/desktop/api/WebServices/ns-webservices-ws_fault_reason) , die Text beschreibt, der den Fehler beschreibt), enthält er auch ein Detailfeld, mit dem Sie beliebige XML-Inhalte angeben können, die den Fehler beschreiben

## <a name="generating-faults-in-a-service"></a>Erzeugen von Fehlern in einem Dienst

Ein Dienst sendet in der Regel einen Fehler aufgrund eines Fehlers, der bei der Verarbeitung der Anforderung aufgetreten ist. Das von dieser API verwendete Modell ist, dass der Code im Dienst, der auf den Verarbeitungsfehler stößt, die erforderlichen Fehlerinformationen im [WS- \_ Fehler](ws-error.md) Objekt erfasst, und dann der Code auf einer höheren Ebene in der Aufrufkette den Fehler mithilfe der Informationen, die auf der unteren Ebene aufgezeichnet werden. Mit diesem Schema kann der Code, der den Fehler sendet, von der Art und Weise isoliert werden, wie Fehlersituationen Fehlern zugeordnet werden, und es wird weiterhin das Senden von Rich-Fault-Informationen ermöglicht.

Die folgenden Eigenschaften können mit [**wssetfaulterrorproperty**](/windows/desktop/api/WebServices/nf-webservices-wssetfaulterrorproperty) verwendet werden, um Fehlerinformationen für ein [WS- \_ Fehler](ws-error.md) Objekt zu erfassen:

-   [**WS \_ Fehler \_ \_ fehlereigenschafts \_ Aktion**](/windows/desktop/api/WebServices/ne-webservices-ws_fault_error_property_id). Gibt die Aktion an, die für die Fehlermeldung verwendet werden soll. Wenn dies nicht angegeben ist, wird eine Standardaktion bereitgestellt.
-   [**WS \_ Fehler der Fehler \_ \_ Eigenschaft \_**](/windows/desktop/api/WebServices/ne-webservices-ws_fault_error_property_id). Diese enthält die [**WS- \_ Fehler**](/windows/desktop/api/WebServices/ns-webservices-ws_fault) Struktur, die im Text der Fehlermeldung gesendet wird.
-   [**WS \_ Fehler \_ \_ fehlereigenschafts \_ Header**](/windows/desktop/api/WebServices/ne-webservices-ws_fault_error_property_id). Einige Fehler schließen Nachrichten Header ein, die der Fehlermeldung hinzugefügt werden, um Verarbeitungsfehler im Zusammenhang mit Headern der Anforderungs Nachricht zu übermitteln. Diese Eigenschaft kann verwendet werden, um einen [WS- \_ XML- \_ Puffer](ws-xml-buffer.md) anzugeben, der einen Header enthält, der der Fehlermeldung hinzugefügt werden soll.

Alle Fehler Zeichenfolgen, die dem [WS- \_ Fehler](ws-error.md) Objekt hinzugefügt werden, werden als Text in dem gesendeten Fehler verwendet. Fehler Zeichenfolgen können dem Error-Objekt mithilfe von [**wsadderrorstring**](/windows/desktop/api/WebServices/nf-webservices-wsadderrorstring)hinzugefügt werden.

Die [**wssetfaulterrorproperty**](/windows/desktop/api/WebServices/nf-webservices-wssetfaulterrorproperty) -Funktion kann verwendet werden, um diese Eigenschaften des [WS- \_ Fehler](ws-error.md) Objekts festzulegen.

Um die Details des im [WS- \_ Fehler](ws-error.md) Objekt gespeicherten Fehlers festzulegen, verwenden Sie die [**wssetfaulterrordetail**](/windows/desktop/api/WebServices/nf-webservices-wssetfaulterrordetail) -Funktion. Diese Funktion kann verwendet werden, um dem Fehler beliebige XML-Inhalte zuzuordnen.

Der [Dienst Host](service-host.md) sendet Fehler automatisch mithilfe der obigen Informationen im [WS- \_ Fehler](ws-error.md) Objekt. Mit der Eigenschaft [**\_ \_ \_ Fehler \_ Veröffentlichung der WS-Dienst Eigenschaft**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id) können Sie steuern, wie ausführlich ein Fehler gesendet wird.

Bei der Arbeit auf der Kanal Ebene können mithilfe von [**wssendfaultmessageforerror**](/windows/desktop/api/WebServices/nf-webservices-wssendfaultmessageforerror)Fehler für ein [WS- \_ Fehler](ws-error.md) Objekt gesendet werden.

## <a name="handling-faults-on-a-client"></a>Behandeln von Fehlern auf einem Client

Wenn ein Client bei der Verwendung eines [Dienst Proxys](service-proxy.md) oder über [**wsrequestreply**](/windows/desktop/api/WebServices/nf-webservices-wsrequestreply) oder [**wsreceivemess**](/windows/desktop/api/WebServices/nf-webservices-wsreceivemessage)einen Fehler empfängt, wird der Fehler " **WS \_ E- \_ Endpunkt \_ Fehler \_ empfangen** " zurückgegeben. (Weitere Informationen finden Sie unter [Rückgabewerte für Windows-Webdienste](windows-web-services-return-values.md).) Diese Funktionen füllen auch das dem-Befehl bereitgestellte [WS- \_ Fehler](ws-error.md) Objekt mit Informationen zum empfangenen Fehler auf.

Die folgenden Eigenschaften eines [WS- \_ Fehler](ws-error.md) Objekts können mithilfe von [**wsgetfaulterrorproperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetfaulterrorproperty) abgefragt werden, um Informationen über einen empfangenen Fehler zu erhalten:

-   [**WS \_ Fehler \_ \_ fehlereigenschafts \_ Aktion**](/windows/desktop/api/WebServices/ne-webservices-ws_fault_error_property_id). Gibt den Aktionswert der Fehlermeldung an.
-   [**WS \_ Fehler der Fehler \_ \_ Eigenschaft \_**](/windows/desktop/api/WebServices/ne-webservices-ws_fault_error_property_id). Diese enthält die [**WS- \_ Fehler**](/windows/desktop/api/WebServices/ns-webservices-ws_fault) Struktur, die aus dem Text der Fehlermeldung deserialisiert wurde.

Ein Fehler kann beliebigen zusätzlichen XML-Inhalt im Detail des Fehlers enthalten. Auf diesen kann mithilfe der [**wsgetfaulterrordetail**](/windows/desktop/api/WebServices/nf-webservices-wsgetfaulterrordetail) -Funktion zugegriffen werden.

## <a name="using-faults-with-messages"></a>Verwenden von Fehlern mit Nachrichten

Der folgende Abschnitt gilt für den direkten Umgang mit dem Inhalt des Texts einer Fehlermeldung.

Der Inhalt des Texts einer Fehlermeldung wird durch die standardmäßige WS- [**\_ Fehler**](/windows/desktop/api/WebServices/ns-webservices-ws_fault) Struktur dargestellt, die über integrierte Unterstützung für die Serialisierung verfügt.

Beispielsweise kann der folgende Code verwendet werden, um einen Fehler in den Nachrichtentext zu schreiben:

``` syntax
HRESULT hr;
WS_ELEMENT_DESCRIPTION faultDescription = { NULL, WS_FAULT_TYPE, NULL, NULL };
WS_FAULT fault = { ... };
hr = WsWriteBody(message, &faultDescription, WS_WRITE_REQUIRED_VALUE, &fault, sizeof(fault), error);
```

Der folgende Code kann verwendet werden, um einen Fehler aus einem Nachrichtentext zu lesen:

``` syntax
HRESULT hr;
WS_ELEMENT_DESCRIPTION faultDescription = { NULL, WS_FAULT_TYPE, NULL, NULL };
WS_FAULT fault;
hr = WsReadBody(message, &faultDescription, WS_READ_REQUIRED_VALUE, &fault, sizeof(fault), error);
```

Um zu ermitteln, ob es sich bei einer empfangenen Nachricht um einen Fehler handelt, kann die [**WS- \_ Nachrichten Eigenschaft " \_ \_ \_ Fault**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id) " auf "Fault" (Fehler) " Diese Eigenschaft wird festgelegt, je nachdem, ob das erste Element im Text ein Fault-Element während [**wsread messagestart**](/windows/desktop/api/WebServices/nf-webservices-wsreadmessagestart) oder [**wsleserenvelopestart**](/windows/desktop/api/WebServices/nf-webservices-wsreadenvelopestart)ist.

Verwenden Sie zum Erstellen eines [**WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_fault) -Fehlers mithilfe eines [WS- \_ Fehlers](ws-error.md)die [**wscreatefaultfromerror**](/windows/desktop/api/WebServices/nf-webservices-wscreatefaultfromerror) -Funktion.

Die folgenden Enumerationen sind Teil von Fehlern:

-   [**WS- \_ Fehler \_ Offenlegung**](/windows/desktop/api/WebServices/ne-webservices-ws_fault_disclosure)
-   [**Eigenschaften-ID für WS-Fehler \_ \_ Fehler \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_fault_error_property_id)

Die folgenden Funktionen sind Bestandteil von Fehlern:

-   [**Wscreatefaultfromerror**](/windows/desktop/api/WebServices/nf-webservices-wscreatefaultfromerror)
-   [**Wsgetfaulterrordetail**](/windows/desktop/api/WebServices/nf-webservices-wsgetfaulterrordetail)
-   [**Wsgetfaulterrorproperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetfaulterrorproperty)
-   [**Wssetfaulterrordetail**](/windows/desktop/api/WebServices/nf-webservices-wssetfaulterrordetail)
-   [**Wssetfaulterrorproperty**](/windows/desktop/api/WebServices/nf-webservices-wssetfaulterrorproperty)

Die folgenden Strukturen sind Teil von Fehlern:

-   [**WS- \_ Fehler**](/windows/desktop/api/WebServices/ns-webservices-ws_fault)
-   [**WS- \_ Fehler \_ Code**](/windows/desktop/api/WebServices/ns-webservices-ws_fault_code)
-   [**Beschreibung der WS- \_ Fehler \_ Details \_**](/windows/desktop/api/WebServices/ns-webservices-ws_fault_detail_description)
-   [**WS- \_ Fehler \_ Ursache**](/windows/desktop/api/WebServices/ns-webservices-ws_fault_reason)

 

 




