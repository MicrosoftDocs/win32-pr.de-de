---
description: Listet die Enumerationen auf, die in Authentifizierungs-APIs verwendet werden.
ms.assetid: e27888e5-d01a-4fdd-8c7d-9849c0f90eb5
title: Authentifizierungsenumerationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc42553074b79726c9d1b70bfc6292f4acf44df225fa1f86c7f7a28289ec8ab7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101320"
---
# <a name="authentication-enumerations"></a>Authentifizierungsenumerationen

Authentifizierungsenumerationen werden gemäß der Verwendung wie folgt kategorisiert:

-   [Enumerationen der Anmeldeinformationsverwaltung](#credentials-management-enumerations)
-   [LSA-Enumerationen](#lsa-enumerations)
-   [Netzwerkanbieterenumerationen](#network-provider-enumerations)
-   [CredSSP-Enumerationen (Credential Security Support Provider)](#credential-security-support-provider-credssp-enumerations)
-   [Andere Enumerationen](#other-enumerations)

## <a name="credentials-management-enumerations"></a>Enumerationen der Anmeldeinformationsverwaltung

Die Anmeldeinformationsverwaltung verwendet die folgenden Enumerationen.



| Enumeration                                            | Beschreibung                                                                                                                                                                                               |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CRED \_ MARSHAL \_ TYPE**](/windows/desktop/api/WinCred/ne-wincred-cred_marshal_type)       | Enthält die Anmeldeinformationstypen, die von [**CredMarshalCredential**](/windows/desktop/api/WinCred/nf-wincred-credmarshalcredentiala) gemarshallt oder von [**CredUnmarshalCredential**](/windows/desktop/api/WinCred/nf-wincred-credunmarshalcredentiala)nicht gemarshallt werden können.<br/> |
| [**\_CRED-SCHUTZTYP \_**](/windows/desktop/api/WinCred/ne-wincred-cred_protection_type) | Gibt den Sicherheitskontext an, in dem Anmeldeinformationen bei Verwendung der [**CredProtect-Funktion**](/windows/desktop/api/WinCred/nf-wincred-credprotecta) verschlüsselt werden.<br/>                                                                  |



 

## <a name="lsa-enumerations"></a>LSA-Enumerationen

LSA verwendet die folgenden Enumerationen.



| Enumeration                                                                                   | Beschreibung                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**KERB \_ LOGON \_ SUBMIT \_ TYPE**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-kerb_logon_submit_type)                                   | Listet den Typ der angeforderten Anmeldung auf.<br/>                                                                                                                                                                                                                  |
| [**\_ \_ KERB-PROFILPUFFERTYP \_**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-kerb_profile_buffer_type)                               | Listet den Typ des zurückgegebenen Anmeldeprofils auf.<br/>                                                                                                                                                                                                                 |
| [**\_ \_ KERB-PROTOKOLLNACHRICHTENTYP \_**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-kerb_protocol_message_type)                           | Listet die Typen von Nachrichten auf, die durch Aufrufen von [**LsaCallAuthenticationPackage**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsacallauthenticationpackage)an das [*Kerberos-Authentifizierungspaket*](/windows/desktop/SecGloss/k-gly) gesendet werden können.<br/> |
| [**DATENSATZTYP DES \_ LSA-GESAMTSTRUKTUR-VERTRAUENSKONFLIKTS \_ \_ \_ \_**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-lsa_forest_trust_collision_record_type) | Definiert die Typen von Kollisionen, die zwischen LSA-Gesamtstruktur-Vertrauensstellungsdatensätzen auftreten können.<br/>                                                                                                                                                                           |
| [**DATENSATZTYP DER \_ LSA-GESAMTSTRUKTUR-VERTRAUENSSTELLUNG \_ \_ \_**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-lsa_forest_trust_record_type)                      | Definiert den Typ eines LSA-Gesamtstruktur-Vertrauensstellungsdatensatzes.<br/>                                                                                                                                                                                                           |
| [**\_ \_ LSA-TOKENINFORMATIONSTYP \_**](/windows/desktop/api/Ntsecpkg/ne-ntsecpkg-lsa_token_information_type)                           | Gibt die Informationsebenen an, die in ein Anmeldetoken aufgenommen werden können.<br/>                                                                                                                                                                                |
| [**MSV1 \_ 0 \_ LOGON \_ SUBMIT \_ TYPE**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-msv1_0_logon_submit_type)                              | Listet die Art der angeforderten Anmeldung auf.<br/>                                                                                                                                                                                                                  |
| [**MSV1 \_ \_ 0-PROFILPUFFERTYP \_ \_**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-msv1_0_profile_buffer_type)                          | Listet die Art des zurückgegebenen Anmeldeprofils auf.<br/>                                                                                                                                                                                                                 |
| [**MSV1 \_ \_ 0-PROTOKOLLNACHRICHTENTYP \_ \_**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-msv1_0_protocol_message_type)                      | Listet die Typen von Nachrichten auf, die durch Aufrufen von [**LsaCallAuthenticationPackage**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsacallauthenticationpackage)an das [MSV1 \_ 0-Authentifizierungspaket](msv1-0-authentication-package.md) gesendet werden können.<br/>                                                 |
| [**POLICY \_ DOMAIN \_ \_ INFORMATION-KLASSE**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_domain_information_class)                 | Definiert den Typ der Richtliniendomäneninformationen.<br/>                                                                                                                                                                                                            |
| [**\_ \_ SICHERHEITSANMELDUNGSTYP**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-security_logon_type)                                          | Gibt den Typ der Anmeldung an, die von einem Anmeldevorgang angefordert wird.<br/>                                                                                                                                                                                                 |



 

## <a name="network-provider-enumerations"></a>Netzwerkanbieterenumerationen

Der Netzwerkanbieter verwendet die folgenden Enumerationen.



| Enumeration                                                                       | Beschreibung                                                                                                                                                                                |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_SECPKG EXTENDED \_ \_ INFORMATION-KLASSE**](/windows/desktop/api/Ntsecpkg/ne-ntsecpkg-secpkg_extended_information_class) | Enumerationstyp, der den Typ der Informationen angibt, die für ein [*Sicherheitspaket*](/windows/desktop/SecGloss/s-gly)festgelegt oder abgerufen werden sollen.<br/> |
| [**\_SECPKG-NAMENSTYP \_**](/windows/desktop/api/Ntsecpkg/ne-ntsecpkg-secpkg_name_type)                                    | Enumerationswert, der den für ein Konto angegebenen Namenstyp angibt.<br/>                                                                                                     |



 

## <a name="credential-security-support-provider-credssp-enumerations"></a>CredSSP-Enumerationen (Credential Security Support Provider)

CredSSP verwendet die folgenden Enumerationen.



| Enumeration                                          | Beschreibung                                                                                                  |
|------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**CREDSPP \_ SUBMIT \_ TYPE**](/windows/win32/api/credssp/ne-credssp-credspp_submit_type) | Gibt den Typ der Anmeldeinformationen an, die von einer [**CREDSSP \_ CRED-Struktur**](/windows/desktop/api/Credssp/ns-credssp-credssp_cred) angegeben werden.<br/> |



 

## <a name="other-enumerations"></a>Andere Enumerationen

Hier sind die anderen Enumerationen, die von der Authentifizierung verwendet werden.



| Enumeration                                                   | Beschreibung                                                                                                                                                                                                                |
|---------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_IDENTITÄTSTYP**](/windows/win32/api/identitycommon/ne-identitycommon-identity_type)                       | Gibt den Typ der aufzuzählenden Identitäten an.<br/>                                                                                                                                                                  |
| [**PKU2U \_ LOGON SUBMIT TYPE (PKU2U-ANMELDETYP \_ ÜBERMITTELN) \_**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-pku2u_logon_submit_type) | Gibt den Typ der Anmeldemeldung an, die in einer [**PKU2U \_ CERTIFICATE \_ S4U \_ LOGON-Struktur**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-pku2u_certificate_s4u_logon) übergeben wird.<br/>                                                                                |
| [**SECPKG \_ ATTR \_ \_ LCT-STATUS**](/windows/desktop/api/Sspi/ne-sspi-secpkg_attr_lct_status)   | Gibt an, ob das Token aus dem letzten Aufruf der [**InitializeSecurityContext-Funktion**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) das letzte Token des Clients ist.<br/>                               |
| [**SECPKG \_ \_ CRED-KLASSE**](/windows/desktop/api/Sspi/ne-sspi-secpkg_cred_class)              | Gibt den Typ der in einem Clientkontext verwendeten Anmeldeinformationen an. Die [**SECPKG \_ CRED \_ CLASS-Enumeration**](/windows/desktop/api/Sspi/ne-sspi-secpkg_cred_class) wird in der [**SecPkgContext \_ CredInfo-Struktur**](/windows/desktop/api/Sspi/ns-sspi-secpkgcontext_credinfo) verwendet.<br/> |



 

 

