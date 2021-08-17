---
title: EAPHost Supplicant-Strukturen
description: Erfahren Sie mehr über die EAPHost Supplicant-API-Strukturen, z. B. EAP \_ CRED \_ REQ und EAP \_ METHOD PROPERTY \_ \_ ARRAY.
ms.assetid: 77595f36-140d-4d8e-af8e-63e9de0031c4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6703070eabbc571927569f28c39109bbe1eda2f1c70b621982dde3ab4ac3a61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117904617"
---
# <a name="eaphost-supplicant-structures"></a>EAPHost Supplicant-Strukturen

Die EAPHost Supplicant-API-Strukturen lauten wie folgt.



| Struktur                                                                        | BESCHREIBUNG                                                                                                          |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [**EAP \_ CRED \_ REQ**](eap-cred-req.md)                                           | Enthält sowohl die alten als auch die neuen EAP-Anmeldeinformationen für Änderungsvorgänge für Anmeldeinformationen.                                    |
| [**EAP \_ CRED \_ RESP**](eap-cred-resp.md)                                         | Enthält sowohl die alten als auch die neuen EAP-Anmeldeinformationen für Änderungsvorgänge für Anmeldeinformationen.                                    |
| [**EAP \_ CRED \_ EXPIRY \_ REQ**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_cred_expiry_req)                            | Enthält sowohl die alten als auch die neuen EAP-Anmeldeinformationen für Vorgänge zum Ablauf von Anmeldeinformationen.                                     |
| [**EAP \_ CRED \_ EXPIRY \_ RESP**](/previous-versions/windows/desktop/legacy/bb530539(v=vs.85))                      | Enthält sowohl die alten als auch die neuen EAP-Anmeldeinformationen für Vorgänge zum Ablauf von Anmeldeinformationen.                                    |
| [**REQ \_ DER EAP-CRED-ANMELDUNG \_ \_**](eap-cred-logon-req.md)                              | Enthält EAP-Anmeldeinformationen für die Netzwerkauthentifizierung.                                                                 |
| [**EAP \_ CRED \_ LOGON \_ RESP**](eap-cred-logon-resp.md)                            | Enthält EAP-Anmeldeinformationen für die Netzwerkauthentifizierung.                                                                 |
| [**INTERAKTIVE \_ \_ EAP-BENUTZEROBERFLÄCHENDATEN \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data)                    | Enthält Konfigurationsinformationen für interaktive Benutzeroberflächenkomponenten, die auf einem EAP-Supplicant ausgelöst werden.            |
| [**\_EAP-METHODENEIGENSCHAFT \_**](/windows/desktop/api/EapTypes/ns-eaptypes-eap_method_property)                             | Windows 7 oder höher: Stellt eine Methodeneigenschaft dar.                                                                    |
| [**\_EIGENSCHAFTENARRAY DER EAP-METHODE \_ \_**](/windows/desktop/api/EapTypes/ns-eaptypes-eap_method_property_array)                | Windows 7 oder höher: Enthält ein Array von Methodeneigenschaftsstrukturen.                                                 |
| [**\_ \_ EAP-METHODENEIGENSCHAFTSWERT \_**](/previous-versions/windows/desktop/api/EapTypes/ns-eaptypes-eap_method_property_value)                | Windows 7 oder höher: Enthält einen Methodeneigenschaftswert.                                                                |
| [**\_EAP-METHODENEIGENSCHAFTSWERT \_ \_ \_ BOOL**](/windows/desktop/api/EapTypes/ns-eaptypes-eap_method_property_value_bool)     | Windows 7 oder höher: Enthält einen BOOL-Datentyp-Methodeneigenschaftswert.                                                 |
| [**EAP \_ METHOD \_ PROPERTY \_ VALUE \_ DWORD**](/windows/desktop/api/EapTypes/ns-eaptypes-eap_method_property_value_dword)   | Windows 7 oder höher: Enthält einen Eigenschaftswert der DWORD-Datentypmethode.                                                |
| [**EAP \_ METHOD \_ PROPERTY \_ VALUE \_ STRING**](/windows/desktop/api/EapTypes/ns-eaptypes-eap_method_property_value_string) | Windows 7 oder höher: Enthält einen Zeichenfolgendatentyp-Methodeneigenschaftswert.                                               |
| [**\_EAPHOST-AUTHENTIFIZIERUNGSINFORMATIONEN \_**](/windows/desktop/api/eaphostpeertypes/ns-eaphostpeertypes-eaphost_auth_info)                                 | Beschreibt aktuelle Authentifizierungsinformationen in verschiedenen Phasen des EAP-Authentifizierungsprozesses.          |
| [**EapHostPeerMethodResult**](/windows/win32/api/eaphostpeertypes/ns-eaphostpeertypes-eaphostpeermethodresult)                       | Enthält die Von EAPHost während einer Authentifizierungssitzung generierten Ergebnisdaten, die dann an eine EAP-Methode übergeben werden. |
| [**EapHostPeerNapInfo**](/windows/win32/api/eaphostpeertypes/ns-eaphostpeertypes-eaphostpeermethodresult)                            | Windows 7 oder höher: Enthält die NAP-Informationen (Network Access Protection) zu einem EAP-Supplicant.                   |



 

 

 