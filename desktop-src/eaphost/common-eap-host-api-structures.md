---
title: Allgemeine EAPHost-API-Strukturen
description: Erfahren Sie mehr über gängige EAPHost-API-Strukturen. Hier finden Sie eine Liste der Strukturen, die von allen EAPHost-Technologien verwendet werden.
ms.assetid: f6f3b909-1e89-47f8-853c-c0f3f2414817
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b44a94aae1f18336dae8c11a1dc0217dc7c8d08
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730385"
---
# <a name="common-eaphost-api-structures"></a>Allgemeine EAPHost-API-Strukturen

In der folgenden Tabelle werden die Strukturen aufgelistet, die allen EAPHost-API-Technologien gemeinsam sind.



| Struktur                                                                | BESCHREIBUNG                                                                                                                                                                                                             |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EAP- \_ Attribut**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attribute)                                  | Enthält ein EAP-Attribut.                                                                                                                                                                                              |
| [**EAP- \_ Attribute**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attributes)                                | Enthält ein Array von EAP-Attributen.                                                                                                                                                                                    |
| [**\_ \_ Eingabe \_ Feld \_ Array der EAP-Konfiguration**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) | Enthält einen Satz von [**Datenstrukturen der EAP- \_ Konfigurations \_ Eingabe \_ Felder \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_data) , die zusammen die Benutzereingabe Feld Daten enthalten, die von einem EAP-Konfigurations Dialogfeld für einmaliges Anmelden (SSO) abgerufen werden. |
| [**\_ \_ Eingabe \_ Feld \_ Daten der EAP-Konfiguration**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_data)   | Enthält die Daten, die einem einzelnen Eingabefeld in einem EAP-Konfigurations Dialogfeld für einmaliges Anmelden (Single Sign-on, SSO) zugeordnet sind.                                                                                                              |
| [**EAP- \_ Fehler**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_error)                                          | Enthält Daten zu einem Fehler, der während eines EAPHost-Vorgangs aufgetreten ist.                                                                                                                                                 |
| [**EAP- \_ Methoden \_ Informationen**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_info)                             | Enthält spezifische Daten für eine EAP-Methode.                                                                                                                                                                               |
| [**Informationen zur EAP- \_ Methode \_ \_ Ex**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_info_ex)                      | Windows Vista mit Service Pack 1 (SP1) oder höher: enthält spezifische Daten für eine EAP-Methode.                                                                                                                             |
| [**\_ \_ Informations \_ Array der EAP-Methode**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_info_array)                | Enthält Informationen zu EAP-Methoden, die auf dem Client Computer installiert sind.                                                                                                                                                   |
| [**EAP- \_ Methoden \_ Info \_ array \_ Ex**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_info_array_ex)         | Windows Vista mit SP1 oder höher: enthält Informationen zu allen EAP-Methoden, die auf dem Client Computer installiert sind.                                                                                                    |
| [**Typ der EAP- \_ Methode \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_type)                             | Enthält Typen-, Identifikations-und Autoren Daten für eine EAP-Methode.                                                                                                                                                       |
| [**EAP- \_ Typ**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_type)                                            | Enthält die Typen-und Hersteller Identifizierungs Daten für eine EAP-Methode.                                                                                                                                                         |
| [**Eappacket**](/windows/win32/api/eapmethodtypes/ns-eapmethodtypes-eappacket)                                           | Enthält ein Paket mit nicht transparenten Daten, die während einer EAP-Authentifizierungs Sitzung gesendet werden.                                                                                                                                             |



 

 

 




