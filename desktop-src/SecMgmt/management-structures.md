---
description: Listet die mit Sicherheitsverwaltungs-APIs verwendeten Strukturen auf.
ms.assetid: 8df25095-a215-464a-abac-39a6ea05f6a3
title: Sicherheits Verwaltungsstrukturen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2212332b65d89a8d2c1f5a24601a59cca041ff42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350046"
---
# <a name="security-management-structures"></a>Sicherheits Verwaltungsstrukturen

Dieser Abschnitt enthält Referenzseiten für die folgenden Gruppen von Strukturen:

-   [LSA-Richtlinien Verwaltungsstrukturen](#lsa-policy-management-structures)
-   [Anlagen Strukturen](#attachment-structures)
-   [Sicherere Strukturen](#safer-structures)

## <a name="lsa-policy-management-structures"></a>LSA-Richtlinien Verwaltungsstrukturen

Die folgenden Strukturen werden von den Richtlinien Verwaltungsfunktionen der [*lokalen Sicherheits Autorität*](/windows/desktop/SecGloss/l-gly) (LSA) verwendet.



| Struktur                                                                       | BESCHREIBUNG                                                                                                                                   |
|---------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**LSA \_ auth- \_ Informationen**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-lsa_auth_information)                          | Enthält Authentifizierungsinformationen für eine vertrauenswürdige Domäne.                                                                                     |
| [**LSA- \_ \_ enumerationsinformationen**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-lsa_enumeration_information)            | Enthält einen Zeiger auf eine [*Sicherheits*](/windows/desktop/SecGloss/s-gly) -ID (SID).    |
| [**LSA- \_ Objekt \_ Attribute**](/windows/desktop/api/LsaLookup/ns-lsalookup-lsa_object_attributes)                        | Gibt die Attribute einer Verbindung mit dem [**Richtlinien**](policy-object.md) Objekt an.                                                       |
| [**Liste der \_ referenzierten \_ Domänen \_**](/windows/win32/api/lsalookup/ns-lsalookup-lsa_referenced_domain_list)             | Enthält Informationen zu den Domänen, auf die in einem Suchvorgang verwiesen wird.                                                                      |
| [**LSA- \_ übersetzter \_ Name**](/windows/desktop/api/LsaLookup/ns-lsalookup-lsa_translated_name)                            | Enthält Informationen zu dem durch eine SID identifizierten Konto.                                                                                   |
| [**LSA-über \_ setzte \_ sid**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-lsa_translated_sid)                              | Enthält Informationen über die SID, die ein Konto identifiziert.                                                                                |
| [**LSA \_ übersetzt \_ SID2**](/windows/desktop/api/LsaLookup/ns-lsalookup-lsa_translated_sid2)                            | Enthält Informationen über die SID, die ein Konto identifiziert.                                                                                |
| [**LSA- \_ Vertrauensstellungs \_ Informationen**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_trust_information)                        | Identifiziert eine Domäne.                                                                                                                          |
| [**LSA- \_ Unicode- \_ Zeichenfolge**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string)                              | Enthält eine Zeichenfolge und deren Längen Informationen.                                                                                                 |
| [**Informationen zur Richtlinien \_ Konto \_ Domäne \_**](/windows/desktop/api/LsaLookup/ns-lsalookup-policy_account_domain_info)             | Wird verwendet, um den Namen und die SID der Konto Domäne des Systems festzulegen und abzufragen.                                                                        |
| [**Informationen zu Richtlinien Überwachungs \_ \_ Ereignissen \_**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-policy_audit_events_info)                 | Wird verwendet, um die Überwachungsregeln des Systems festzulegen und abzufragen.                                                                                            |
| [**\_Informationen zur DNS- \_ Domänen Domäne \_**](/windows/desktop/api/LsaLookup/ns-lsalookup-policy_dns_domain_info)                     | Wird verwendet, um Domain Name System (DNS)-Informationen zur primären Domäne festzulegen und abzufragen, die einem [**Richtlinien**](policy-object.md) Objekt zugeordnet sind. |
| [**Informationen zur Richtlinie \_ LSA- \_ Server \_ Rolle \_**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-policy_lsa_server_role_info)          | Wird verwendet, um die Rolle eines LSA-Servers festzulegen und abzufragen.                                                                                              |
| [**Informationen zu Richtlinien \_ Änderungen \_**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-policy_modification_info)                  | Wird verwendet, um Informationen über die Erstellungszeit und die letzte Änderung der LSA-Datenbank abzufragen.                                                  |
| [**richtlinienpd- \_ \_ Konto \_ Informationen**](policy-pd-account-info.md)                     | Veraltet. Arbeitsstationen verwenden den Namen der Arbeitsstation, gefolgt von einem $ als Kontonamen.                                                          |
| [**\_Informationen zur primären \_ Domäne \_ der Richtlinie**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-policy_primary_domain_info)             | Veraltet. Verwenden Sie stattdessen **policydnsdomaininformation** und die [**DNS- \_ \_ Domänen \_**](/windows/desktop/api/LsaLookup/ns-lsalookup-policy_dns_domain_info) Informationsstruktur der Richtlinie.           |
| [**Authentifizierungsinformationen zu vertrauenswürdigen \_ Domänen \_ \_**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-trusted_domain_auth_information)   | Dient zum Abrufen von Authentifizierungsinformationen für eine vertrauenswürdige Domäne.                                                                             |
| [**\_ \_ vollständige \_ Informationen zur vertrauenswürdigen Domäne**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-trusted_domain_full_information)   | Wird verwendet, um umfassende Informationen zu einer vertrauenswürdigen Domäne abzurufen.                                                                                 |
| [**Informationen zu vertrauenswürdigen \_ Domänen \_ \_**](/previous-versions/windows/desktop/legacy/ms722475(v=vs.85)) | Informationen zu einer vertrauenswürdigen Domäne. Diese Struktur ist mit [**LSA- \_ Vertrauensstellungs \_ Informationen**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_trust_information)identisch.                  |
| [**Informationen zu vertrauenswürdigen \_ Domänen \_ \_**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-trusted_domain_information_ex)       | Wird verwendet, um erweiterte Informationen zu einer vertrauenswürdigen Domäne abzurufen.                                                                                 |
| [**Informationen zum vertrauenswürdigen \_ Domänen \_ Namen \_**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-trusted_domain_name_info)                 | Wird verwendet, um den Namen einer vertrauenswürdigen Domäne abzufragen oder festzulegen.                                                                                            |
| [**Informationen zu vertrauenswürdigem \_ \_**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-trusted_password_info)                        | Wird verwendet, um das Kennwort für eine vertrauenswürdige Domäne abzufragen oder festzulegen.                                                                                       |
| [**Informationen zum vertrauenswürdigen \_ POSIX- \_ Offset \_**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-trusted_posix_offset_info)               | Wird verwendet, um den Wert abzufragen oder festzulegen, mit dem POSIX-Benutzer-und Gruppen Bezeichner generiert werden                                                             |



 

Die folgenden Strukturtypen sind veraltet oder sind für die zukünftige Verwendung reserviert:

-   **\_ \_ vollständige \_ Abfrage \_ Informationen zur Richtlinien Überwachung**
-   **\_ \_ vollständige \_ Set- \_ Informationen zur Richtlinien Prüfung**
-   **Informationen zum Richtlinien Überwachungs \_ \_ Protokoll \_**
-   **\_Standard \_ Kontingent \_ Informationen für Richtlinien**
-   **Informationen zur Richtlinien \_ Replikat \_ Quelle \_**
-   **Informationen über vertrauenswürdige \_ Controller \_**

## <a name="attachment-structures"></a>Anlagen Strukturen

Die folgenden Strukturen werden von den DLLs der Sicherheitskonfigurations-Anlage und deren unterstützenden Funktionen verwendet. Diese Strukturen werden in scesvc. h definiert.



| Struktur                                                        | BESCHREIBUNG                                                                                                                                     |
|------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [**scesvc- \_ Konfigurations \_ Informationen**](/windows/win32/api/scesvc/ns-scesvc-scesvc_configuration_info) | Enthält Konfigurationsinformationen für einen-Dienst.                                                                                               |
| [**scesvc- \_ Konfigurations \_ Zeile**](/windows/win32/api/scesvc/ns-scesvc-scesvc_configuration_line) | Enthält Informationen zu einer Zeile mit Konfigurationsdaten.                                                                                        |
| [**scesvc- \_ Analyse \_ Informationen**](/windows/win32/api/scesvc/ns-scesvc-scesvc_analysis_info)           | Enthält die Analyse Informationen.                                                                                                              |
| [**scesvc- \_ Analyse \_ Zeile**](/windows/win32/api/scesvc/ns-scesvc-scesvc_analysis_line)           | Enthält den Schlüssel, den Wert und die Wert Länge für eine bestimmte Zeile, die durch eine [**scesvc- \_ Analyse \_ Info**](/windows/win32/api/scesvc/ns-scesvc-scesvc_analysis_info) -Struktur angegeben wird. |
| [**scesvc- \_ Rückruf \_ Informationen**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info)           | Enthält einen nicht transparenten Daten Bank Handle und Rückruf Funktionszeiger zum Abfragen, festlegen und Freigeben von Informationen.                                          |



 

## <a name="safer-structures"></a>Sicherere Strukturen

Die folgenden Strukturen und Enumerationstypen werden in sichereren verwendet. Sie werden in winsafer. h definiert.



| Struktur                                                                | BESCHREIBUNG                                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**sicherere \_ Code \_ Eigenschaften**](/windows/desktop/api/WinSafer/ns-winsafer-safer_code_properties_v2)                 | Enthält Code Bild Informationen und Kriterien, die auf dem Codebild geprüft werden sollen. Ein Array dieser Strukturen wird an die Funktion " [**SaferIdentifyLevel**](/windows/desktop/api/WinSafer/nf-winsafer-saferidentifylevel) " übermittelt.                                                                  |
| [**sicherer \_ Identifikations \_ Header**](/windows/desktop/api/WinSafer/ns-winsafer-safer_identification_header)     | Header Struktur für [**sicherere \_ pathname- \_ Identifizierung**](/windows/desktop/api/WinSafer/ns-winsafer-safer_pathname_identification), [**sicherere \_ Hash \_ Identifizierung**](/windows/desktop/api/WinSafer/ns-winsafer-safer_hash_identification)und [**sicherere \_ urlzone- \_ Identifikations**](/windows/desktop/api/WinSafer/ns-winsafer-safer_urlzone_identification) Strukturen. |
| [**sichere \_ Pfadnamen \_ Identifizierung**](/windows/desktop/api/WinSafer/ns-winsafer-safer_pathname_identification) | Enthält den Pfadnamen eines zu überprüfenden Code Bilds.                                                                                                                                                                                                      |
| [**sicherere \_ Hash \_ Identifizierung**](/windows/desktop/api/WinSafer/ns-winsafer-safer_hash_identification)         | Identifiziert einen Hashwert des zu überprüfenden Code Bilds.                                                                                                                                                                                                      |
| [**sicherere \_ urlzone- \_ Identifikation**](/windows/desktop/api/WinSafer/ns-winsafer-safer_urlzone_identification)   | Gibt die URL-Ursprungszone des zu überprüfenden Code Bilds an.                                                                                                                                                                                      |



 

 

 
