---
title: Sicherheitsanmeldeinformationen
description: Sicherheits Anmelde Informationen sind ein Beleg dafür, dass eine kommunizierende Partei über das verfügt, das verwendet werden kann, um ein Sicherheits Token zu erstellen oder abzurufen.
ms.assetid: 70e260ce-9e45-436f-b6d1-b650a5c9c0e9
keywords:
- Sicherheits Anmelde Informationen Webdienste für Windows
- Wwsapi
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0611e6e54fd83e09f811ffddcda4785cef162685
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "106342174"
---
# <a name="security-credentials"></a>Sicherheitsanmeldeinformationen

Sicherheits Anmelde Informationen sind ein Beleg dafür, dass eine kommunizierende Partei über das verfügt, das verwendet werden kann, um ein Sicherheits Token zu erstellen oder abzurufen. Daher sind Anmelde Informationen in der Regel länger als Sicherheits Token, und ein Sicherheits Token kann als Lauf Zeit Darstellung der Sicherheits Anmelde Informationen angezeigt werden. Beispiele für Anmelde Informationen sind ein Computer Zertifikat, das zur Laufzeit in ein X. 509-Sicherheits Token konvertiert werden kann, oder ein Benutzername/Kennwort-Paar für eine Domäne (das zum Abrufen eines Kerberos-Sicherheits Tokens verwendet werden kann).


Anmelde Informationen werden als Teil der [Sicherheits Bindungen](security-bindings.md)angegeben.

Die folgenden API-Elemente werden mit Sicherheits Anmelde Informationen verwendet.

| Rückruf                                                                  | BESCHREIBUNG                                              |
|---------------------------------------------------------------------------|----------------------------------------------------------|
| [**WS \_ get \_ CERT- \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_get_cert_callback)                   | Stellt ein Zertifikat für die Security Runtime bereit.          |
| [**WS \_ Validate \_ password \_ Callback**](/windows/desktop/api/WebServices/nc-webservices-ws_validate_password_callback) | Überprüft ein paar aus Benutzername und Kennwort auf Empfängerseite. |



 



| Enumeration                                                                                           | Beschreibung                                                   |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [**WS \_ CERT-Anmelde \_ \_ Informationstyp**](/windows/desktop/api/WebServices/ne-webservices-ws_cert_credential_type)                                         | Der Typ der Zertifikat Anmelde Informationen.                       |
| [**WS \_ username \_ Credential \_ Type**](/windows/desktop/api/WebServices/ne-webservices-ws_username_credential_type)                                 | Der Typ der Anmelde Informationen für Benutzername und Kennwort.                 |
| [**Anmelde \_ \_ \_ \_ \_ Informationstyp der integrierten WS Windows-Authentifizierung**](/windows/desktop/api/WebServices/ne-webservices-ws_windows_integrated_auth_credential_type) | Der Typ der Anmelde Informationen für die integrierte Windows-Authentifizierung. |



 



| Struktur                                                                                                   | BESCHREIBUNG                                                                                                           |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [**WS CERT-Anmelde Informationen \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_cert_credential)                                                          | Der abstrakte Basistyp für alle Typen von Zertifikat Anmelde Informationen.                                                          |
| [**WS \_ Custom \_ CERT \_ Credential**](/windows/desktop/api/WebServices/ns-webservices-ws_custom_cert_credential)                                           | Der Typ zum Angeben von Zertifikat Anmelde Informationen, die von einem Rückruf an die Anwendung bereitgestellt werden sollen.             |
| [**WS-Standard Anmelde Informationen für die \_ \_ \_ integrierte Windows \_ \_ -Authentifizierung**](/windows/desktop/api/WebServices/ns-webservices-ws_default_windows_integrated_auth_credential) | Geben Sie ein, um die Anmelde Informationen für die integrierte Windows-Authentifizierung basierend auf dem aktuellen Thread Token bereitzustellen.                  |
| [**WS-nicht transparente Anmelde Informationen für die \_ \_ \_ integrierte Windows \_ \_ -Authentifizierung**](/windows/desktop/api/WebServices/ns-webservices-ws_opaque_windows_integrated_auth_credential)   | Typ für die Bereitstellung von Anmelde Informationen für die integrierte Windows-Authentifizierung.                                                    |
| [**WS \_ String \_ username \_ Credential**](/windows/desktop/api/WebServices/ns-webservices-ws_string_username_credential)                                   | Der Typ, der ein Benutzername/Kennwort-Paar als Zeichen folgen bereitstellt.                                                           |
| [**WS \_ String \_ Windows \_ Integrated \_ auth \_ Credential**](/windows/desktop/api/WebServices/ns-webservices-ws_string_windows_integrated_auth_credential)   | Typ zum Bereitstellen von Windows-Anmelde Informationen als Benutzername, Kennwort und Domänen Zeichenfolgen.                                        |
| [**WS-Antragsteller \_ \_ Name \_ CERT \_ Credential**](/windows/desktop/api/WebServices/ns-webservices-ws_subject_name_cert_credential)                              | Der Typ zum Angeben von Zertifikat Anmelde Informationen mit dem Antragsteller Namen des Zertifikats, dem Speicherort und dem Speicher Namen. |
| [**WS \_ Thumbprint \_ CERT \_ Credential**](/windows/desktop/api/WebServices/ns-webservices-ws_thumbprint_cert_credential)                                   | Der Typ zum Angeben von Zertifikat Anmelde Informationen unter Verwendung des Fingerabdrucks des Zertifikats, des Speicher Orts und des Speicher namens.   |
| [**WS \_ username \_ Credential**](/windows/desktop/api/WebServices/ns-webservices-ws_username_credential)                                                  | Der abstrakte Basistyp für alle Anmelde Informationen für Benutzername und Kennwort.                                                         |
| [**Anmelde Informationen für die integrierte WS Windows-Authentifizierung \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_windows_integrated_auth_credential)                  | Der abstrakte Basistyp für alle Anmelde Informationstypen, die mit der integrierten Windows-Authentifizierung verwendet werden.                          |



 

 

 




