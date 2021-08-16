---
title: Sicherheitsanmeldeinformationen
description: Sicherheitsanmeldeinformationen sind ein Beweis, den eine kommunizierende Partei besitzt, die zum Erstellen oder Abrufen eines Sicherheitstokens verwendet werden kann.
ms.assetid: 70e260ce-9e45-436f-b6d1-b650a5c9c0e9
keywords:
- Webdienste für Sicherheitsanmeldeinformationen für Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41f5703d9f58e7fee57f1ce8465e0413a7ca3c246590b816e84f7419e80f6efb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118192761"
---
# <a name="security-credentials"></a>Sicherheitsanmeldeinformationen

Sicherheitsanmeldeinformationen sind ein Beweis, den eine kommunizierende Partei besitzt, die zum Erstellen oder Abrufen eines Sicherheitstokens verwendet werden kann. Daher sind Anmeldeinformationen in der Regel länger als Sicherheitstoken, und ein Sicherheitstoken kann als Laufzeitmanifest der Sicherheitsanmeldeinformationen angesehen werden. Beispiele für Anmeldeinformationen sind ein Computerzertifikat (das zur Laufzeit in ein X.509-Sicherheitstoken konvertiert werden kann) oder ein Benutzername/Kennwort-Paar für eine Domäne (das zum Abrufen eines Kerberos-Sicherheitstokens verwendet werden kann).


Anmeldeinformationen werden als Teil der [Sicherheitsbindungen](security-bindings.md)angegeben.

Die folgenden API-Elemente werden mit Sicherheitsanmeldeinformationen verwendet.

| Rückruf                                                                  | BESCHREIBUNG                                              |
|---------------------------------------------------------------------------|----------------------------------------------------------|
| [**WS \_ GET \_ CERT \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_get_cert_callback)                   | Stellt ein Zertifikat für die Sicherheitslaufzeit bereit.          |
| [**WS \_ VALIDATE \_ PASSWORD \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_validate_password_callback) | Überprüft ein Benutzername-Kennwort-Paar auf empfängerseitiger Seite. |



 



| Enumeration                                                                                           | Beschreibung                                                   |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [**WS \_ CERT \_ CREDENTIAL \_ TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_cert_credential_type)                                         | Der Typ der Zertifikatanmeldeinformationen.                       |
| [**ANMELDEINFORMATIONSTYP DES \_ WS-BENUTZERNAMENS \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_username_credential_type)                                 | Der Typ der Anmeldeinformationen für Benutzername/Kennwort.                 |
| [**WS \_ WINDOWS \_ INTEGRATED \_ AUTH \_ CREDENTIAL \_ TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_windows_integrated_auth_credential_type) | Der Typ der Anmeldeinformationen für die integrierte Windows-Authentifizierung. |



 



| Struktur                                                                                                   | BESCHREIBUNG                                                                                                           |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [**\_ \_ WS-ZERTIFIKATANMELDEINFORMATIONEN**](/windows/desktop/api/WebServices/ns-webservices-ws_cert_credential)                                                          | Der abstrakte Basistyp für alle Zertifikatanmeldeinformationstypen.                                                          |
| [**BENUTZERDEFINIERTE \_ \_ WS-ZERTIFIKATANMELDEINFORMATIONEN \_**](/windows/desktop/api/WebServices/ns-webservices-ws_custom_cert_credential)                                           | Der Typ zum Angeben von Zertifikatanmeldeinformationen, die von einem Rückruf an die Anwendung bereitgestellt werden sollen.             |
| [**\_WS-STANDARDANMELDEINFORMATIONEN FÜR \_ \_ INTEGRIERTE \_ WINDOWS-AUTHENTIFIZIERUNG \_**](/windows/desktop/api/WebServices/ns-webservices-ws_default_windows_integrated_auth_credential) | Geben Sie ein, um auf Grundlage des aktuellen Threadtokens anmeldeinformationen für die integrierte Windows-Authentifizierung zur Verfügung zu stellen.                  |
| [**WS \_ OPAQUE \_ WINDOWS \_ INTEGRATED \_ AUTH \_ CREDENTIAL**](/windows/desktop/api/WebServices/ns-webservices-ws_opaque_windows_integrated_auth_credential)   | Geben Sie ein, um anmeldeinformationen für die integrierte Windows-Authentifizierung zur Verfügung zu stellen.                                                    |
| [**ANMELDEINFORMATIONEN \_ FÜR WS-ZEICHENFOLGENBENUTZERNAME \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_string_username_credential)                                   | Der Typ zum Bereitstellen eines Benutzername-Kennwort-Paars als Zeichenfolgen.                                                           |
| [**ANMELDEINFORMATIONEN FÜR \_ \_ INTEGRIERTE \_ WINDOWS-AUTHENTIFIZIERUNG \_ MIT WS-ZEICHENFOLGE \_**](/windows/desktop/api/WebServices/ns-webservices-ws_string_windows_integrated_auth_credential)   | Geben Sie ein, um eine Windows Anmeldeinformationen als Benutzername, Kennwort und Domänenzeichenfolgen anzugeben.                                        |
| [**ZERTIFIKATANMELDEINFORMATIONEN FÜR \_ WS-ANTRAGSTELLERNAME \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_subject_name_cert_credential)                              | Der Typ zum Angeben von Zertifikatanmeldeinformationen unter Verwendung des Antragstellernamens, des Speicherorts und des Speichernamens des Zertifikats. |
| [**WS \_ \_ THUMBPRINT-ZERTIFIKATANMELDEINFORMATIONEN \_**](/windows/desktop/api/WebServices/ns-webservices-ws_thumbprint_cert_credential)                                   | Der Typ zum Angeben von Zertifikatanmeldeinformationen unter Verwendung des Fingerabdrucks, des Speicherorts und des Speichernamens des Zertifikats.   |
| [**ANMELDEINFORMATIONEN \_ FÜR WS-BENUTZERNAME \_**](/windows/desktop/api/WebServices/ns-webservices-ws_username_credential)                                                  | Der abstrakte Basistyp für alle Anmeldeinformationen für Benutzername/Kennwort.                                                         |
| [**INTEGRIERTE \_ WS-AUTHENTIFIZIERUNGSANMELDEINFORMATIONEN FÜR WINDOWS \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_windows_integrated_auth_credential)                  | Der abstrakte Basistyp für alle Anmeldeinformationstypen, die mit Windows integrierte Authentifizierung verwendet werden.                          |



 

 

 




