---
title: Allgemeine EAPHost-API-Strukturen
description: Erfahren Sie mehr über allgemeine EAPHost-API-Strukturen. Sehen Sie sich eine Liste der Strukturen an, die von allen EAPHost-Technologien verwendet werden.
ms.assetid: f6f3b909-1e89-47f8-853c-c0f3f2414817
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4740658f798eadee2a658df1a7f9f8fd44b386c4ac39b52bcf49e75887d2d719
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118984330"
---
# <a name="common-eaphost-api-structures"></a>Allgemeine EAPHost-API-Strukturen

Die folgende Tabelle enthält Strukturen, die allen EAPHost-API-Technologien gemeinsam sind.



| Struktur                                                                | BESCHREIBUNG                                                                                                                                                                                                             |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_EAP-ATTRIBUT**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attribute)                                  | Enthält ein EAP-Attribut.                                                                                                                                                                                              |
| [**\_EAP-ATTRIBUTE**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attributes)                                | Enthält ein Array von EAP-Attributen.                                                                                                                                                                                    |
| [**EAP \_ CONFIG \_ INPUT \_ FIELD \_ ARRAY**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) | Enthält eine Reihe von [**EAP \_ CONFIG \_ INPUT FIELD \_ \_ DATA-Strukturen,**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_data) die zusammen die Benutzereingabefelddaten enthalten, die aus einem EAP-Konfigurationsdialogfeld für einmaliges Anmelden (Single-Sign-On, SSO) abgerufen wurden. |
| [**\_ \_ EAP-KONFIGURATIONSEINGABEFELDDATEN \_ \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_data)   | Enthält die Daten, die einem einzelnen Eingabefeld in einem Konfigurationsdialogfeld für einmaliges Anmelden (Single Sign-On, SSO) von EAP zugeordnet sind.                                                                                                              |
| [**\_EAP-FEHLER**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_error)                                          | Enthält Daten zu einem Fehler, der während eines EAPHost-Vorgangs aufgetreten ist.                                                                                                                                                 |
| [**\_ \_ EAP-METHODENINFORMATIONEN**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_info)                             | Enthält bestimmte Daten für eine EAP-Methode.                                                                                                                                                                               |
| [**\_EAP-METHODENINFORMATIONEN \_ \_ EX**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_info_ex)                      | Windows Vista mit Service Pack 1 (SP1) oder höher: Enthält bestimmte Daten für eine EAP-Methode.                                                                                                                             |
| [**\_ \_ \_ EAP-METHODENINFORMATIONSARRAY**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_info_array)                | Enthält Informationen zu EAP-Methoden, die auf dem Clientcomputer installiert sind.                                                                                                                                                   |
| [**\_ \_ EAP-METHODENINFORMATIONSARRAY \_ \_ EX**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_info_array_ex)         | Windows Vista mit SP1 oder höher: Enthält Informationen zu allen EAP-Methoden, die auf dem Clientcomputer installiert sind.                                                                                                    |
| [**\_EAP-METHODENTYP \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_type)                             | Enthält Typ-, Identifikations- und Erstellungsdaten für eine EAP-Methode.                                                                                                                                                       |
| [**\_EAP-TYP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_type)                                            | Enthält Typ- und Herstelleridentifikationsdaten für eine EAP-Methode.                                                                                                                                                         |
| [**EapPacket**](/windows/win32/api/eapmethodtypes/ns-eapmethodtypes-eappacket)                                           | Enthält ein Paket nicht transparenter Daten, die während einer EAP-Authentifizierungssitzung gesendet werden.                                                                                                                                             |



 

 

 




