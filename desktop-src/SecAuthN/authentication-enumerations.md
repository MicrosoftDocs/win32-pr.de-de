---
description: Listet die in den Authentifizierungs-APIs verwendeten Enumerationen auf.
ms.assetid: e27888e5-d01a-4fdd-8c7d-9849c0f90eb5
title: Authentifizierungs Enumerationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5640151967867f610aa8b18c81940c684d23c18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750936"
---
# <a name="authentication-enumerations"></a>Authentifizierungs Enumerationen

Authentifizierungs Enumerationen werden gemäß der Verwendung wie folgt kategorisiert:

-   [Enumerationen zur Verwaltung von Anmelde Informationen](#credentials-management-enumerations)
-   [LSA-Enumerationen](#lsa-enumerations)
-   [Netzwerkanbieter-Enumerationen](#network-provider-enumerations)
-   [Aufzählung der Credential Security Support Provider (kredssp)](#credential-security-support-provider-credssp-enumerations)
-   [Weitere Enumerationen](#other-enumerations)

## <a name="credentials-management-enumerations"></a>Enumerationen zur Verwaltung von Anmelde Informationen

Die Verwaltung von Anmelde Informationen verwendet die folgenden Enumerationen.



| Enumeration                                            | Beschreibung                                                                                                                                                                                               |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Typ der \_ Typ-Mars Hall \_**](/windows/desktop/api/WinCred/ne-wincred-cred_marshal_type)       | Enthält die Typen von Anmelde Informationen, die von " [**kredmarshalcredential**](/windows/desktop/api/WinCred/nf-wincred-credmarshalcredentiala) " gemarshallt oder von " [**kredunmarshalcredential**](/windows/desktop/api/WinCred/nf-wincred-credunmarshalcredentiala)" nicht gemarshallt werden können.<br/> |
| [**Typ des \_ Typs "Schutz" \_**](/windows/desktop/api/WinCred/ne-wincred-cred_protection_type) | Gibt den Sicherheitskontext an, in dem Anmelde Informationen verschlüsselt werden, [**Wenn die Funktion**](/windows/desktop/api/WinCred/nf-wincred-credprotecta) "Funktion" verwendet wird.<br/>                                                                  |



 

## <a name="lsa-enumerations"></a>LSA-Enumerationen

LSA verwendet die folgenden Enumerationen.



| Enumeration                                                                                   | Beschreibung                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**KERB \_ - \_ Anmeldetyp für Anmeldung \_**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-kerb_logon_submit_type)                                   | Listet den Typ der angeforderten Anmeldung auf.<br/>                                                                                                                                                                                                                  |
| [**\_ \_ Puffertyp des KERB Profils \_**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-kerb_profile_buffer_type)                               | Listet den Typ des zurückgegebenen Anmelde Profils auf.<br/>                                                                                                                                                                                                                 |
| [**KERB \_ - \_ Protokoll \_ Nachrichtentyp**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-kerb_protocol_message_type)                           | Listet die Nachrichten Typen auf, die durch Aufrufen von [**lsacallauthenticationpackage**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsacallauthenticationpackage)an das [*Kerberos*](/windows/desktop/SecGloss/k-gly) -Authentifizierungs Paket gesendet werden können.<br/> |
| [**LSA-Gesamtstruktur- \_ \_ Vertrauensstellungs Konflikt \_ \_ Daten Satz \_**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-lsa_forest_trust_collision_record_type) | Definiert die Arten von Kollisionen, die zwischen LSA-Gesamtstruktur-Vertrauensstellungs Datensätzen auftreten können.<br/>                                                                                                                                                                           |
| [**LSA-Gesamtstruktur- \_ \_ Vertrauens \_ Datensatz- \_ Typ**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-lsa_forest_trust_record_type)                      | Definiert den Typ eines LSA-Gesamtstruktur-Vertrauensstellungs Datensatzes.<br/>                                                                                                                                                                                                           |
| [**LSA \_ - \_ \_ tokeninformationstyp**](/windows/desktop/api/Ntsecpkg/ne-ntsecpkg-lsa_token_information_type)                           | Gibt die Ebenen der Informationen an, die in einem Anmelde Token enthalten sein können.<br/>                                                                                                                                                                                |
| [**MSV1 \_ 0 \_ Anmeldetyp für Anmeldung \_ \_**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-msv1_0_logon_submit_type)                              | Listet die Art der angeforderten Anmeldung auf.<br/>                                                                                                                                                                                                                  |
| [**MSV1 \_ 0 \_ Profil \_ \_ Puffertyp**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-msv1_0_profile_buffer_type)                          | Listet die Art des zurückgegebenen Anmelde Profils auf.<br/>                                                                                                                                                                                                                 |
| [**MSV1 \_ 0 \_ Protokoll \_ \_ Nachrichtentyp**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-msv1_0_protocol_message_type)                      | Listet die Nachrichten Typen auf, die durch Aufrufen von [**lsacallauthenticationpackage**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsacallauthenticationpackage)an das [ \_ Authentifizierungs Paket MSV1 0](msv1-0-authentication-package.md) gesendet werden können.<br/>                                                 |
| [**Richtlinien \_ Domänen \_ Informations \_ Klasse**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_domain_information_class)                 | Definiert den Typ der Richtlinien Domänen Informationen.<br/>                                                                                                                                                                                                            |
| [**Sicherheits \_ \_ Anmeldetyp**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-security_logon_type)                                          | Gibt den Typ der Anmeldung an, die von einem Anmeldeprozess angefordert wurde.<br/>                                                                                                                                                                                                 |



 

## <a name="network-provider-enumerations"></a>Netzwerkanbieter-Enumerationen

Der Netzwerkanbieter verwendet die folgenden Enumerationen.



| Enumeration                                                                       | Beschreibung                                                                                                                                                                                |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**secpkg- \_ Erweiterte \_ Informations \_ Klasse**](/windows/desktop/api/Ntsecpkg/ne-ntsecpkg-secpkg_extended_information_class) | Enumerationstyp, der den Typ der Informationen angibt, die für ein [*Sicherheitspaket*](/windows/desktop/SecGloss/s-gly)festgelegt oder erhalten werden.<br/> |
| [**Typ des secpkg- \_ namens \_**](/windows/desktop/api/Ntsecpkg/ne-ntsecpkg-secpkg_name_type)                                    | -Enumerationswert, der den für ein Konto angegebenen Namen angibt.<br/>                                                                                                     |



 

## <a name="credential-security-support-provider-credssp-enumerations"></a>Aufzählung der Credential Security Support Provider (kredssp)

"Kredssp" verwendet die folgenden Enumerationen.



| Enumeration                                          | Beschreibung                                                                                                  |
|------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**\_ \_ ermittelungstyp von "tydspp**](/windows/win32/api/credssp/ne-credssp-credspp_submit_type) | Gibt den Typ der Anmelde Informationen an, die von einer [**kredssp \_ -**](/windows/desktop/api/Credssp/ns-credssp-credssp_cred) Erstellungs Struktur angegeben werden.<br/> |



 

## <a name="other-enumerations"></a>Weitere Enumerationen

Dies sind die anderen Enumerationen, die von der-Authentifizierung verwendet werden.



| Enumeration                                                   | Beschreibung                                                                                                                                                                                                                |
|---------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_Identitätstyp**](/windows/win32/api/identitycommon/ne-identitycommon-identity_type)                       | Gibt den Typ der aufzuzählenden Identitäten an.<br/>                                                                                                                                                                  |
| [**PKU2U \_ Anmeldetyp für Anmeldung \_ \_**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-pku2u_logon_submit_type) | Gibt den Typ der Anmelde Nachricht an, die in einer [**PKU2U \_ Certificate \_ S4U \_ Logon**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-pku2u_certificate_s4u_logon) -Struktur übermittelt wurde.<br/>                                                                                |
| [**Status der secpkg- \_ attr- \_ LCT \_**](/windows/desktop/api/Sspi/ne-sspi-secpkg_attr_lct_status)   | Gibt an, ob das Token des letzten Aufrufes der [**InitializeSecurityContext**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) -Funktion das letzte Token des Clients ist.<br/>                               |
| [**secpkg- \_ Klasse "- \_ Klasse"**](/windows/desktop/api/Sspi/ne-sspi-secpkg_cred_class)              | Gibt den Typ der Anmelde Informationen an, die in einem Client Kontext verwendet werden. Die Enumeration der [**secpkg- \_ \_ Klasse**](/windows/desktop/api/Sspi/ne-sspi-secpkg_cred_class) "Enumeration" wird in der " [**secpkgcontext"-Struktur " \_ alidinfo**](/windows/desktop/api/Sspi/ns-sspi-secpkgcontext_credinfo) " verwendet.<br/> |



 

 

