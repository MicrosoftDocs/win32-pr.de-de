---
title: Sicherheitsbindungseinstellungen
description: Sicherheitsbindungs Einstellungen steuern die Art und Weise, wie ein Sicherheits Token abgerufen oder verwendet wird.
ms.assetid: 4bc03cb4-1ac2-4ad1-a45d-eae8f50f5355
keywords:
- Sicherheitsbindungs Einstellungen Webdienste für Windows
- Wwsapi
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c5a3d27627c3360560a38ef9cb85e3fb5ece434
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "103734825"
---
# <a name="security-binding-settings"></a>Sicherheitsbindungseinstellungen

Sicherheitsbindungs Einstellungen steuern die Art und Weise, wie ein Sicherheits Token abgerufen oder verwendet wird. Sie werden als Auflistung von Eigenschaften-Wert-Paaren mit den Eigenschafts Schlüsseln dargestellt, die von der Enumeration [**WS \_ Security \_ Binding- \_ Eigenschaft**](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding_property)definiert werden. Jede Eigenschaft in der Auflistung weist einen angemessenen Standardwert auf. Daher ist es möglich, eine Sicherheits Beschreibung zu definieren und zu verwenden, ohne die Einstellungen der Sicherheitsbindung anzugeben.


Informationen zu den channelweiten Sicherheitseinstellungen mit Eigenschaften, deren Schlüssel durch die [**WS-Sicherheitseigenschaften \_ - \_ \_ ID**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id) -Enumeration definiert werden, finden Sie unter [Security Channel Settings](security-channel-settings.md).

Die folgenden API-Elemente werden mit den Einstellungen für die Sicherheitsbindung verwendet.

| Enumeration                                                                          | Beschreibung                                                                                                                                                       |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WS- \_ CERT- \_ Fehler**](/windows/win32/api/webservices/ne-webservices-ws_value_type)                                         | Definiert Fehler im Zusammenhang mit der Zertifikats Überprüfung.                                                                                                               |
| [**WS-HTTP-Header-Authentifizierungs \_ \_ \_ \_ Schema**](https://technet.microsoft.com/windows/dd401907(v=vs.60))                 | Definiert die Optionen zum Durchführen der Client Authentifizierung mithilfe von http-Authentifizierungs Headern.                                                                       |
| [**WS-HTTP-Header-Authentifizierungs \_ \_ \_ \_ Ziel**](/windows/desktop/api/WebServices/ne-webservices-ws_http_header_auth_target)                 | Definiert das Ziel für die Sicherheitsbindung der HTTP-Header Authentifizierung.                                                                                           |
| [**WS- \_ Anforderungs \_ Sicherheits Token- \_ \_ Aktion**](/windows/desktop/api/WebServices/ne-webservices-ws_request_security_token_action)     | Definiert, welche Aktionen beim Aushandeln von Sicherheits Token mithilfe von WS-Trust verwendet werden sollen.                                                                              |
| [**Name der WS- \_ Sicherheits \_ Algorithmus- \_ Suite \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_algorithm_suite_name)     | Eine Reihe von Sicherheits Algorithmen, die für Aufgaben wie Signierung und Encryting verwendet werden.                                                                                      |
| [**WS \_ - \_ sicherheitsbindungs- \_ Eigenschaften- \_ ID**](/windows/desktop/api/WebServices/ne-webservices-ws_security_binding_property_id)       | Gibt die Eigenschaften an, die zum Angeben der sicherheitsbindungs Einstellungen verwendet werden.                                                                                              |
| [**WS \_ - \_ sicherheitsschlüsselentropie- \_ \_ Modus**](/windows/desktop/api/WebServices/ne-webservices-ws_security_key_entropy_mode)             | Definiert, wie Zufälligkeit bei der Aushandlung von Sicherheits Token, die mit der Sicherheit von Nachrichten und im gemischten Modus ausgeführt wird, zum ausgestellten Schlüssel beigetragen werden soll.                     |
| [**WS \_ - \_ Sicherheits \_ Schlüsseltyp**](/windows/desktop/api/WebServices/ne-webservices-ws_security_key_type)                              | Der Schlüsseltyp eines Sicherheits Tokens.                                                                                                                                 |
| [**WS- \_ Sicherheits \_ Token- \_ Verweis \_ Modus**](/windows/desktop/api/WebServices/ne-webservices-ws_security_token_reference_mode)     | der Mechanismus, der verwendet wird, um auf ein Sicherheits Token von Signaturen, verschlüsselten Elementen und abgeleiteten Token im Kontext von Nachrichten-und gemischten Sicherheits Bindungen zu verweisen. |
| [**WS- \_ Trust- \_ Version**](/windows/desktop/api/WebServices/ne-webservices-ws_trust_version)                                       | Definiert die WS-Trust Spezifikations Version, die mit Nachrichten Sicherheit und Sicherheit im gemischten Modus verwendet werden soll.                                                              |
| [**WS \_ Windows \_ Integrated \_ auth- \_ Paket**](/windows/desktop/api/WebServices/ne-webservices-ws_windows_integrated_auth_package) | Definiert das für die integrierte Windows-Authentifizierung zu verwendende SSP-Paket.                                                                                |



 



| Struktur                                                               | BESCHREIBUNG                                    |
|-------------------------------------------------------------------------|------------------------------------------------|
| [**WS- \_ Sicherheits \_ Bindungs \_ Eigenschaft**](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding_property) | Gibt eine spezifische Einstellung für die Sicherheitsbindung an. |



 

 

 




