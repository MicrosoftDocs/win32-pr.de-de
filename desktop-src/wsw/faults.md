---
title: Fehler
description: Eine Fehlermeldung wird verwendet, um Fehlerinformationen zu einem Fehler an einem Remoteendpunkt zu übermitteln.
ms.assetid: d2bada50-2ddd-4f7f-9b25-7bbec77b431b
keywords:
- Faults Web Services for Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55cd9e28e9ec9ce2f3068643d44306f542eebabb9b0b0c8860b15e9e986b49b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117841770"
---
# <a name="faults"></a>Fehler

Eine Fehlermeldung wird verwendet, um Fehlerinformationen zu einem Fehler an einem Remoteendpunkt zu übermitteln. Eine Fehlermeldung ist wie jede andere Nachricht, mit der Ausnahme, dass das Format des Nachrichtentexts ein Standardformat hat. Fehler können sowohl von Infrastrukturprotokollen wie der WS-Adressierung als auch von Anwendungsprotokollen auf höherer Ebene verwendet werden.

-   [Übersicht](#overview)
-   [Generieren von Fehlern in einem Dienst](#generating-faults-in-a-service)
-   [Behandeln von Fehlern auf einem Client](#handling-faults-on-a-client)
-   [Verwenden von Fehlern mit Nachrichten](#using-faults-with-messages)

## <a name="overview"></a>Übersicht

Der Inhalt des Textkörpers einer Fehlermeldung wird in dieser API mithilfe der [**WS \_ FAULT-Struktur**](/windows/desktop/api/WebServices/ns-webservices-ws_fault) dargestellt. Obwohl ein Fehler über einen festen Satz von Feldern verfügt, die zum Bereitstellen von Informationen zum Fehler verwendet werden (z. B. der [**\_ WS-FEHLERCODE, \_**](/windows/desktop/api/WebServices/ns-webservices-ws_fault_code) der den Fehlertyp identifiziert, und der [**\_ \_ WS-FEHLERGRUND,**](/windows/desktop/api/WebServices/ns-webservices-ws_fault_reason) der Text enthält, der den Fehler beschreibt), enthält er auch ein Detailfeld, das verwendet werden kann, um beliebigen XML-Inhalt im Zusammenhang mit dem Fehler anzugeben.

## <a name="generating-faults-in-a-service"></a>Generieren von Fehlern in einem Dienst

Ein Dienst sendet in der Regel einen Fehler aufgrund eines Fehlers, der bei der Verarbeitung der Anforderung aufgetreten ist. Das von dieser API verwendete Modell ist, dass der Code im Dienst, der auf den Verarbeitungsfehler trifft, die erforderlichen Fehlerinformationen im [WS \_ ERROR-Objekt](ws-error.md) erfasst. Anschließend sendet code auf einer höheren Ebene in der Aufrufkette den Fehler mithilfe der auf der unteren Ebene erfassten Informationen. Mit diesem Schema kann der Code, der den Fehler sendet, von der Zuordnung von Fehlersituationen zu Fehlern isoliert werden, während gleichzeitig umfangreiche Fehlerinformationen gesendet werden können.

Die folgenden Eigenschaften können mit [**WsSetFaultErrorProperty**](/windows/desktop/api/WebServices/nf-webservices-wssetfaulterrorproperty) verwendet werden, um Fehlerinformationen für ein [WS \_ ERROR-Objekt zu](ws-error.md) erfassen:

-   [**WS \_ FAULT \_ ERROR \_ PROPERTY \_ ACTION**](/windows/desktop/api/WebServices/ne-webservices-ws_fault_error_property_id). Dies gibt die Aktion an, die für die Fehlermeldung verwendet werden soll. Wenn dies nicht angegeben wird, wird eine Standardaktion bereitgestellt.
-   [**WS \_ FAULT \_ ERROR \_ PROPERTY \_ FAULT**](/windows/desktop/api/WebServices/ne-webservices-ws_fault_error_property_id). Dieser enthält die [**WS \_ FAULT-Struktur,**](/windows/desktop/api/WebServices/ns-webservices-ws_fault) die im Text der Fehlermeldung gesendet wird.
-   [**WS \_ \_ \_ \_ FEHLERFEHLEREIGENSCHAFTSHEADER**](/windows/desktop/api/WebServices/ne-webservices-ws_fault_error_property_id). Einige Fehler umfassen Nachrichtenheader, die der Fehlermeldung hinzugefügt werden, um Verarbeitungsfehler im Zusammenhang mit Headern der Anforderungsnachricht zu übermitteln. Diese Eigenschaft kann verwendet werden, um einen [WS \_ XML \_ BUFFER](ws-xml-buffer.md) anzugeben, der einen Header enthält, der der Fehlermeldung hinzugefügt werden soll.

Alle Fehlerzeichenfolgen, die dem [WS \_ ERROR-Objekt](ws-error.md) hinzugefügt werden, werden als Text im gesendeten Fehler verwendet. Fehlerzeichenfolgen können dem Fehlerobjekt mithilfe von [**WsAddErrorString hinzugefügt werden.**](/windows/desktop/api/WebServices/nf-webservices-wsadderrorstring)

Mit [**der WsSetFaultErrorProperty-Funktion**](/windows/desktop/api/WebServices/nf-webservices-wssetfaulterrorproperty) können diese Eigenschaften des [WS \_ ERROR-Objekts festgelegt](ws-error.md) werden.

Verwenden Sie die [**WsSetFaultErrorDetail-Funktion,**](/windows/desktop/api/WebServices/nf-webservices-wssetfaulterrordetail) um die Details des im [WS \_ ERROR-Objekt](ws-error.md) gespeicherten Fehlers fest zu legen. Diese Funktion kann verwendet werden, um dem Fehler beliebigen XML-Inhalt zu zuordnen.

Der [Diensthost](service-host.md) sendet automatisch Fehler, indem er die oben genannten Informationen im [WS \_ ERROR-Objekt](ws-error.md) verwendet. Die [**WS \_ SERVICE PROPERTY \_ FAULT \_ \_ DISCLOSURE-Eigenschaft**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id) kann verwendet werden, um zu steuern, wie detailliert ein Fehler gesendet wird.

Wenn Sie auf der Kanalebene arbeiten, können Fehler für ein [WS \_ ERROR-Objekt](ws-error.md) mithilfe von [**WsSendFaultMessageForError gesendet werden.**](/windows/desktop/api/WebServices/nf-webservices-wssendfaultmessageforerror)

## <a name="handling-faults-on-a-client"></a>Behandeln von Fehlern auf einem Client

Wenn ein Client bei Verwendung [](service-proxy.md) eines Dienstproxys oder [**über WsRequestReply**](/windows/desktop/api/WebServices/nf-webservices-wsrequestreply) oder [**WsReceiveMessage**](/windows/desktop/api/WebServices/nf-webservices-wsreceivemessage)einen Fehler empfängt, wird der **Fehler WS E ENDPOINT \_ FAULT \_ \_ \_ RECEIVED** zurückgegeben. (Weitere Informationen finden Sie unter Windows [Webdienste-Rückgabewerte](windows-web-services-return-values.md).) Diese Funktionen füllen auch das für den Aufruf bereitgestellte [WS \_ ERROR-Objekt](ws-error.md) mit Informationen zum empfangenen Fehler auf.

Die folgenden Eigenschaften eines [WS \_ ERROR-Objekts](ws-error.md) können mit [**WsGetFaultErrorProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetfaulterrorproperty) abgefragt werden, um Informationen zu einem empfangenen Fehler zu erhalten:

-   [**WS \_ FAULT \_ ERROR \_ PROPERTY \_ ACTION**](/windows/desktop/api/WebServices/ne-webservices-ws_fault_error_property_id). Dies gibt den Aktionswert der Fehlermeldung an.
-   [**WS \_ FAULT \_ ERROR \_ PROPERTY \_ FAULT**](/windows/desktop/api/WebServices/ne-webservices-ws_fault_error_property_id). Dieser enthält die [**WS \_ FAULT-Struktur,**](/windows/desktop/api/WebServices/ns-webservices-ws_fault) die aus dem Text der Fehlermeldung deserialisiert wurde.

Ein Fehler kann beliebigen zusätzlichen XML-Inhalt in den Details des Fehlers enthalten. Darauf kann mithilfe der [**WsGetFaultErrorDetail-Funktion zugegriffen**](/windows/desktop/api/WebServices/nf-webservices-wsgetfaulterrordetail) werden.

## <a name="using-faults-with-messages"></a>Verwenden von Fehlern mit Nachrichten

Der folgende Abschnitt gilt für den direkten Umgang mit dem Inhalt des Textkörpers einer Fehlermeldung.

Der Inhalt des Textkörpers einer Fehlermeldung wird durch die [**WS \_ FAULT-Standardstruktur**](/windows/desktop/api/WebServices/ns-webservices-ws_fault) dargestellt, die eine integrierte Serialisierungsunterstützung bietet.

Beispielsweise kann der folgende Code verwendet werden, um einen Fehler in einen Nachrichtentext zu schreiben:

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

Um zu erfahren, ob eine empfangene Nachricht ein Fehler ist, kann [**die WS \_ MESSAGE PROPERTY \_ IS \_ \_ FAULT-Eigenschaft**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id) verwendet werden. Diese Eigenschaft wird basierend darauf festgelegt, ob das erste Element im Text ein Fault-Element während [**WsReadMessageStart**](/windows/desktop/api/WebServices/nf-webservices-wsreadmessagestart) oder [**WsReadEnvevesStart ist.**](/windows/desktop/api/WebServices/nf-webservices-wsreadenvelopestart)

Verwenden Sie die [**WsCreateFaultFromError-Funktion,**](/windows/desktop/api/WebServices/nf-webservices-wscreatefaultfromerror) um einen [**WS-FEHLER \_**](/windows/desktop/api/WebServices/ns-webservices-ws_fault) bei [einem \_ WS-FEHLER](ws-error.md)zu erstellen.

Die folgenden Enumerationen sind Teil von Fehlern:

-   [**\_WS-FEHLERVERÖFFENTLICHUNG \_**](/windows/desktop/api/WebServices/ne-webservices-ws_fault_disclosure)
-   [**\_ \_ WS-FEHLEREIGENSCHAFTS-ID \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_fault_error_property_id)

Die folgenden Funktionen sind Teil von Fehlern:

-   [**WsCreateFaultFromError**](/windows/desktop/api/WebServices/nf-webservices-wscreatefaultfromerror)
-   [**WsGetFaultErrorDetail**](/windows/desktop/api/WebServices/nf-webservices-wsgetfaulterrordetail)
-   [**WsGetFaultErrorProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetfaulterrorproperty)
-   [**WsSetFaultErrorDetail**](/windows/desktop/api/WebServices/nf-webservices-wssetfaulterrordetail)
-   [**WsSetFaultErrorProperty**](/windows/desktop/api/WebServices/nf-webservices-wssetfaulterrorproperty)

Die folgenden Strukturen sind Teil von Fehlern:

-   [**\_WS-FEHLER**](/windows/desktop/api/WebServices/ns-webservices-ws_fault)
-   [**\_WS-FEHLERCODE \_**](/windows/desktop/api/WebServices/ns-webservices-ws_fault_code)
-   [**\_ \_ WS-FEHLERDETAILBESCHREIBUNG \_**](/windows/desktop/api/WebServices/ns-webservices-ws_fault_detail_description)
-   [**\_WS-FEHLERGRUND \_**](/windows/desktop/api/WebServices/ns-webservices-ws_fault_reason)

 

 




