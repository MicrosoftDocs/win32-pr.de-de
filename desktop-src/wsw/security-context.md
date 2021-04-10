---
title: Sicherheitskontext
description: Sicherheits Kontexte ermöglichen die Einrichtung eines Nachrichten Sicherheits Kontexts gemäß WS-SecureConversation.
ms.assetid: bea92650-21bd-41d4-9dba-043d6779d85f
keywords:
- 'Sicherheitskontext: Native Webdienste'
- Wwsapi
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cff86ea12ae7a4b8bd554e25cde534cba3b4dcb4
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104316790"
---
# <a name="security-context"></a>Sicherheitskontext

Sicherheits Kontexte ermöglichen die Einrichtung eines Nachrichten Sicherheits Kontexts gemäß WS-SecureConversation. Dieser Kontext kann dann verwendet werden, um Nachrichten als Alternative zur One-Shot-Sicherheit zu sichern, bei der die Anmelde Informationen für jede Anforderung übertragen werden. Der etablierte Sicherheitskontext ist eine effizientere Methode zum Sichern von Nachrichten, wenn mehrere Nachrichten ausgetauscht werden.


Sicherheits Kontexte erfordern das vorhanden sein von Bootstrap-Sicherheits Anmelde Informationen, die zum Sichern der im Kontext gesendeten Nachrichten verwendet werden. Zu diesem Zweck können die [**WS \_ Kerberos- \_ apreq- \_ Nachrichten \_ Sicherheits \_ Bindung**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding), die [**WS \_ XML \_ Token \_ Message- \_ Sicherheits \_ Bindung**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_token_message_security_binding)und [**WS \_ username \_ Message \_ Security \_**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding) Binding-Strukturen verwendet werden.

Sicherheits Kontexte sind ein Nachrichten Sicherheits Feature, das mithilfe von Nachrichten Sicherheits Bindungen konfiguriert wird.

## <a name="client"></a>Client

Auf der Clientseite ist der Sicherheitskontext an einen bestimmten Kanal gebunden. Sie wird mithilfe der [**WS- \_ Sicherheits \_ Kontext- \_ Nachrichten \_ Sicherheits \_ Bindung**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding)konfiguriert. Das Verhalten und die Lebensdauer des Kontexts werden vom Kanal bestimmt. Wenn die erste Nachricht auf dem Kanal gesendet wird, wird der Sicherheitskontext eingerichtet. Danach wird der Kontext proaktiv in einem konfigurierbaren Intervall erneuert. Wenn der Server einen Fehler zurückgibt, der angibt, dass der Kontext erneuert werden muss, wird der Kontext erneuert, wenn die nächste Nachricht gesendet wird. Wenn sich der Kanal im geöffneten Zustand befindet, wird der Kontext durch eine Abbruch Meldung abgebrochen, wenn der Kanal geschlossen wird.

## <a name="server"></a>Server

Auf dem-Server wird ein Sicherheitskontext auf die gleiche Weise wie auf dem Client konfiguriert. Es ist jedoch nicht an einen bestimmten Kanal gebunden. Stattdessen können alle Kanäle, die für den Listener erstellt werden, der über den [**WS \_ Security \_ context \_ Message- \_ \_ Bindungs**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) Satz verfügt, Nachrichten mit einem beliebigen Sicherheitskontext empfangen, der auf Kanälen dieses Listener eingerichtet wurde.

Wenn eine Nachricht in einem Kanal eingeht, der Sicherheits Kontexte unterstützt, kann der von dieser Nachricht verwendete Kontext durch Aufrufen der [**wsgetmessageproperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetmessageproperty) -Funktion mit dem [**WS- \_ Nachrichten Eigenschaften- \_ \_ Sicherheits \_ Kontext**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id)abgerufen werden. Der abgerufene Wert kann mit [**wsrevokesecuritycontext**](/windows/desktop/api/WebServices/nf-webservices-wsrevokesecuritycontext) und [**wsgetsecuritycontextproperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetsecuritycontextproperty)verwendet werden.

## <a name="metadata"></a>Metadaten

Die Sicherheitskontext-Einschränkungs Struktur des [**WS- \_ Sicherheits \_ Kontexts \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding_constraint) wird zum Extrahieren der Sicherheitskontext Richtlinie aus den Metadaten verwendet. Weitere Informationen finden Sie unter [Metadatenimport](metadata-import.md).

Die folgenden API-Elemente werden mit Sicherheits Kontexten verwendet.

| Enumeration                                                                    | Beschreibung                                         |
|--------------------------------------------------------------------------------|-----------------------------------------------------|
| [**WS- \_ Sicherheits \_ Kontext-Eigenschaften- \_ \_ ID**](/windows/desktop/api/WebServices/ne-webservices-ws_security_context_property_id) | Identifiziert eine Eigenschaft eines Sicherheitskontext Objekts. |



 



| Funktion                                                             | BESCHREIBUNG                                        |
|----------------------------------------------------------------------|----------------------------------------------------|
| [**Wsgetsecuritycontextproperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetsecuritycontextproperty) | Ruft eine Eigenschaft des angegebenen Sicherheits Kontexts ab. |
| [**Wsrevokesecuritycontext**](/windows/desktop/api/WebServices/nf-webservices-wsrevokesecuritycontext)           | Widerruft einen Sicherheitskontext.                        |



 



| Handle                                           | BESCHREIBUNG                                                 |
|--------------------------------------------------|-------------------------------------------------------------|
| [WS- \_ Sicherheits \_ Kontext](ws-security-context.md) | Ein nicht transparenter Typ, mit dem auf ein Sicherheitskontext Objekt verwiesen wird. |



 



| Struktur                                                               | BESCHREIBUNG                                                               |
|-------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [**WS- \_ Sicherheits \_ Kontext \_ Eigenschaft**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_property) | Definiert eine Eigenschaft eines [WS- \_ Sicherheits \_ Kontexts](ws-security-context.md). |



 

 

 




