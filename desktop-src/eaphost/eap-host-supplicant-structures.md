---
title: EAPHost-Supplicant-Strukturen
description: Erfahren Sie mehr über die EAPHost Supplicant-API-Strukturen, wie z \_ . b. EAP \_ -Eigenschaften Array "req" und EAP- \_ Methode \_ \_ .
ms.assetid: 77595f36-140d-4d8e-af8e-63e9de0031c4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e7121e123fd790a54a95dafb59c080f435ca917
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104391003"
---
# <a name="eaphost-supplicant-structures"></a>EAPHost-Supplicant-Strukturen

Die EAPHost Supplicant-API-Strukturen lauten wie folgt.



| Struktur                                                                        | BESCHREIBUNG                                                                                                          |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [**EAP- \_ Kred- \_ req**](eap-cred-req.md)                                           | Enthält sowohl die alten als auch die neuen EAP-Anmelde Informationen für einen Vorgang zum Ändern von Anmelde Informationen.                                    |
| [**EAP-Benutzer \_ -e/a \_**](eap-cred-resp.md)                                         | Enthält sowohl die alten als auch die neuen EAP-Anmelde Informationen für einen Vorgang zum Ändern von Anmelde Informationen.                                    |
| [**EAP- \_ \_ ablaufungsablauf- \_ req**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_cred_expiry_req)                            | Enthält sowohl die alten als auch die neuen EAP-Anmelde Informationen für den Ablauf von Anmelde Informationen.                                     |
| [**EAP- \_ \_ Ablaufs Ablauf (e) \_**](/previous-versions/windows/desktop/legacy/bb530539(v=vs.85))                      | Enthält sowohl die alten als auch die neuen EAP-Anmelde Informationen für die Ablauf Vorgänge der Anmelde Informationen.                                    |
| [**EAP- \_ \_ Anmelde- \_ req**](eap-cred-logon-req.md)                              | Enthält EAP-Anmelde Informationen für die Netzwerk Authentifizierung.                                                                 |
| [**EAP- \_ \_ Anmelde- \_ Anmeldedienst (e)**](eap-cred-logon-resp.md)                            | Enthält EAP-Anmelde Informationen für die Netzwerk Authentifizierung.                                                                 |
| [**interaktive EAP- \_ \_ Benutzeroberflächen \_ Daten**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data)                    | Enthält Konfigurationsinformationen für interaktive Benutzeroberflächen Komponenten, die auf einem EAP-Supplicant ausgelöst werden.            |
| [**EAP- \_ Methoden \_ Eigenschaft**](/windows/desktop/api/EapTypes/ns-eaptypes-eap_method_property)                             | Windows 7 oder höher: stellt eine Methoden Eigenschaft dar.                                                                    |
| [**\_ \_ Eigenschaften \_ Array der EAP-Methode**](/windows/desktop/api/EapTypes/ns-eaptypes-eap_method_property_array)                | Windows 7 oder höher: enthält ein Array von Methoden Eigenschaften Strukturen.                                                 |
| [**Eigenschafts Wert der EAP- \_ Methode \_ \_**](/previous-versions/windows/desktop/api/EapTypes/ns-eaptypes-eap_method_property_value)                | Windows 7 oder höher: enthält einen Eigenschaften Wert der-Methode.                                                                |
| [**Eigenschafts Wert der EAP- \_ Methode \_ \_ \_ bool**](/windows/desktop/api/EapTypes/ns-eaptypes-eap_method_property_value_bool)     | Windows 7 oder höher: enthält den Eigenschafts Wert einer booleschen Datentyp Methode.                                                 |
| [**EAP- \_ Methoden- \_ Eigenschafts \_ Wert \_ DWORD**](/windows/desktop/api/EapTypes/ns-eaptypes-eap_method_property_value_dword)   | Windows 7 oder höher: enthält den Eigenschafts Wert einer DWORD-Datentyp Methode.                                                |
| [**\_ \_ Eigenschaften \_ Wert- \_ Zeichenfolge der EAP-Methode**](/windows/desktop/api/EapTypes/ns-eaptypes-eap_method_property_value_string) | Windows 7 oder höher: enthält einen Eigenschafts Wert für eine Zeichen folgen-Datentyp Methode.                                               |
| [**EAPHost-Authentifizierungs \_ \_ Informationen**](/windows/desktop/api/eaphostpeertypes/ns-eaphostpeertypes-eaphost_auth_info)                                 | Beschreibt die aktuellen Authentifizierungsinformationen in verschiedenen Phasen des EAP-Authentifizierungsprozesses.          |
| [**Eaphostpeer-methodresult**](/windows/win32/api/eaphostpeertypes/ns-eaphostpeertypes-eaphostpeermethodresult)                       | Enthält die von EAPHost generierten Ergebnisdaten während einer Authentifizierungs Sitzung, die dann an eine EAP-Methode weitergegeben wird. |
| [**Eaphostpeer-Napinfo**](/windows/win32/api/eaphostpeertypes/ns-eaphostpeertypes-eaphostpeermethodresult)                            | Windows 7 oder höher: enthält Informationen zum Netzwerk Zugriffsschutz (Network Access Protection, NAP) für einen EAP-Supplicant.                   |



 

 

 