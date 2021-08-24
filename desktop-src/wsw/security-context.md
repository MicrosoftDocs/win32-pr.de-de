---
title: Sicherheitskontext
description: Sicherheitskontexte ermöglichen die Einrichtung eines Nachrichtensicherheitskontexts gemäß WS-SecureConversation.
ms.assetid: bea92650-21bd-41d4-9dba-043d6779d85f
keywords:
- Sicherheitskontext nativer Webdienste
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06dc1754133f47cf06c5c12e7318a94525be3c821f3db52a7e7513349c3100be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083174"
---
# <a name="security-context"></a>Sicherheitskontext

Sicherheitskontexte ermöglichen die Einrichtung eines Nachrichtensicherheitskontexts gemäß WS-SecureConversation. Dieser Kontext kann dann verwendet werden, um Nachrichten als Alternative zur einmaligen Sicherheit zu schützen, bei der die Anmeldeinformationen für jede Anforderung übertragen werden. Der eingerichtete Sicherheitskontext ist eine effizientere Methode zum Sichern von Nachrichten, wenn mehrere Nachrichten ausgetauscht werden.


Sicherheitskontexte erfordern das Vorhandensein von Bootstrap-Sicherheitsanmeldeinformationen, die zum Sichern der im Kontext gesendeten Nachrichten verwendet werden. Die [**WS \_ \_ KERBEROS-APREQ-NACHRICHTENSICHERHEITSBINDUNG, \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding) [**die \_ WS-XML-TOKEN-NACHRICHTENSICHERHEITSBINDUNG \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_token_message_security_binding)und [**die WS \_ USERNAME MESSAGE \_ SECURITY \_ \_ BINDING-Strukturen**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding) können für diesen Zweck verwendet werden.

Sicherheitskontexte sind ein Nachrichtensicherheitsfeature und werden über Nachrichtensicherheitsbindungen konfiguriert.

## <a name="client"></a>Client

Auf der Clientseite ist der Sicherheitskontext an einen bestimmten Kanal gebunden. Sie wird mithilfe der [**\_ WS-SICHERHEITSKONTEXTMELDUNGSSICHERHEITSBINDUNG \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding)konfiguriert. Verhalten und Lebensdauer des Kontexts werden vom Kanal bestimmt. Wenn die erste Nachricht über den Kanal gesendet wird, wird der Sicherheitskontext eingerichtet. Danach wird der Kontext in einem konfigurierbaren Intervall proaktiv erneuert. Wenn der Server einen Fehler zurückgibt, der angibt, dass der Kontext erneuert werden muss, wird der Kontext erneuert, wenn die nächste Nachricht gesendet wird. Wenn sich der Kanal im geöffneten Zustand befindet, wird der Kontext durch eine Abbruchmeldung abgebrochen, wenn der Kanal geschlossen wird.

## <a name="server"></a>Server

Auf dem Server wird ein Sicherheitskontext auf die gleiche Weise wie auf dem Client konfiguriert. Sie ist jedoch nicht an einen bestimmten Kanal gebunden. Stattdessen können alle Kanäle, die für den Listener erstellt wurden, für den die [**WS \_ SECURITY CONTEXT MESSAGE SECURITY \_ \_ \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) festgelegt ist, Nachrichten mit einem der Sicherheitskontexte empfangen, die in Kanälen dieses Listeners eingerichtet wurden.

Wenn eine Nachricht in einem Kanal eingeht, der Sicherheitskontexte unterstützt, kann der von dieser Nachricht verwendete Kontext durch Aufrufen der [**WsGetMessageProperty-Funktion**](/windows/desktop/api/WebServices/nf-webservices-wsgetmessageproperty) mit dem [**WS \_ MESSAGE PROPERTY SECURITY \_ \_ \_ CONTEXT**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id)abgerufen werden. Der abgerufene Wert kann mit [**WsRevokeSecurityContext**](/windows/desktop/api/WebServices/nf-webservices-wsrevokesecuritycontext) und [**WsGetSecurityContextProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetsecuritycontextproperty)verwendet werden.

## <a name="metadata"></a>Metadaten

Die [**WS \_ SECURITY CONTEXT MESSAGE SECURITY BINDING \_ \_ \_ \_ \_ CONSTRAINT-Struktur**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding_constraint) wird verwendet, um die Sicherheitskontextrichtlinie aus Metadaten zu extrahieren. Weitere Informationen finden Sie unter [Metadatenimport.](metadata-import.md)

Die folgenden API-Elemente werden mit Sicherheitskontexten verwendet.

| Enumeration                                                                    | Beschreibung                                         |
|--------------------------------------------------------------------------------|-----------------------------------------------------|
| [**\_ \_ \_ WS-SICHERHEITSKONTEXTEIGENSCHAFTEN-ID \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_context_property_id) | Identifiziert eine Eigenschaft eines Sicherheitskontextobjekts. |



 



| Funktion                                                             | Beschreibung                                        |
|----------------------------------------------------------------------|----------------------------------------------------|
| [**WsGetSecurityContextProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetsecuritycontextproperty) | Ruft eine Eigenschaft des angegebenen Sicherheitskontexts ab. |
| [**WsRevokeSecurityContext**](/windows/desktop/api/WebServices/nf-webservices-wsrevokesecuritycontext)           | Widerruft einen Sicherheitskontext.                        |



 



| Handle                                           | Beschreibung                                                 |
|--------------------------------------------------|-------------------------------------------------------------|
| [\_WS-SICHERHEITSKONTEXT \_](ws-security-context.md) | Ein nicht transparenter Typ, der verwendet wird, um auf ein Sicherheitskontextobjekt zu verweisen. |



 



| Struktur                                                               | Beschreibung                                                               |
|-------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [**\_ \_ WS-SICHERHEITSKONTEXTEIGENSCHAFT \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_property) | Definiert eine Eigenschaft eines [ \_ WS-SICHERHEITSKONTEXTs. \_ ](ws-security-context.md) |



 

 

 




