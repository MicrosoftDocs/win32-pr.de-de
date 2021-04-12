---
title: IKE/AuthIP-Strukturen
description: IKE/AuthIP-Strukturen
ms.assetid: 3267EA3C-FD1F-4ED1-9794-92551222EFE1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c1b5c8f69ec0ac667dee5fc541c84b8e9e66ceb
ms.sourcegitcommit: cb844c9ab17577ce171fd7b03add668645867bc7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/27/2020
ms.locfileid: "104389991"
---
# <a name="ikeauthip-structures"></a>IKE/AuthIP-Strukturen

## <a name="in-this-section"></a>In diesem Abschnitt

-   [**Ikeext- \_ Authentifizierung \_ METHOD0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_authentication_method0)
-   [**Ikeext- \_ Authentifizierung \_ Methode1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_authentication_method1)
-   [**Ikeext- \_ Authentifizierung \_ Methode2**](/windows/win32/api/iketypes/ns-iketypes-ikeext_authentication_method2)
-   [**Ikeext \_ CERT \_ EKUS0**](/windows/win32/api/iketypes/ns-iketypes-ikeext_cert_ekus0)
-   [**Ikeext \_ CERT \_ NAME0**](/windows/win32/api/iketypes/ns-iketypes-ikeext_cert_name0)
-   [**Ikeext \_ CERT \_ root \_ CONFIG0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_cert_root_config0)
-   [**Ikeext- \_ Zertifikat \_ AUTHENTICATION0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_certificate_authentication0)
-   [**Ikeext- \_ Zertifikat \_ AUTHENTICATION1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_certificate_authentication1)
-   [**Ikeext- \_ Zertifikat \_ fügen**](/windows/win32/api/iketypes/ns-iketypes-ikeext_certificate_authentication2)
-   [**Ikeext- \_ Zertifikat \_ CREDENTIAL0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_certificate_credential0)
-   [**Ikeext- \_ Zertifikat \_ CREDENTIAL1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_certificate_credential1)
-   [**Ikeext- \_ Zertifikat \_ CRITERIA0**](/windows/win32/api/iketypes/ns-iketypes-ikeext_certificate_criteria0)
-   [**Ikeext- \_ Chiffre \_ ALGORITHM0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_cipher_algorithm0)
-   [**Ikeext \_ Common \_ STATISTICS0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_common_statistics0)
-   [**Ikeext \_ Common \_ STATISTICS1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_common_statistics1)
-   [**Ikeext- \_ Cookie \_ PAIR0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_cookie_pair0)
-   [**Ikeext \_ CREDENTIAL0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credential0)
-   [**Ikeext \_ CREDENTIAL1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credential1)
-   [**Ikeext \_ CREDENTIAL2**](/windows/win32/api/iketypes/ns-iketypes-ikeext_credential2)
-   [**Ikeext \_ CREDENTIALS0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credentials0)
-   [**Ikeext \_ CREDENTIALS1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credentials1)
-   [**Ikeext \_ CREDENTIALS2**](/windows/win32/api/iketypes/ns-iketypes-ikeext_credentials2)
-   [**Ikeext \_ Credential \_ PAIR0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credential_pair0)
-   [**Ikeext \_ Credential \_ PAIR1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credential_pair1)
-   [**Ikeext \_ Credential \_ PAIR2**](/windows/win32/api/iketypes/ns-iketypes-ikeext_credential_pair2)
-   [**Ikeext \_ EAP \_ AUTHENTICATION0**](/windows/win32/api/iketypes/ns-iketypes-ikeext_eap_authentication0)
-   [**Ikeext \_ EM \_ POLICY0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_em_policy0)
-   [**Ikeext \_ EM \_ Richtlinie1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_em_policy1)
-   [**Ikeext \_ EM \_ POLICY2**](/windows/win32/api/iketypes/ns-iketypes-ikeext_em_policy2)
-   [**Ikeext- \_ Integrität \_ ALGORITHM0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_integrity_algorithm0)
-   [**Ikeext \_ IP- \_ Versions \_ spezifisch \_ Common \_ STATISTICS0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_ip_version_specific_common_statistics0)
-   [**Ikeext \_ IP- \_ Versions \_ spezifisch \_ Common \_ STATISTICS1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_ip_version_specific_common_statistics1)
-   [**Ikeext \_ IP- \_ Versions \_ spezifisches \_ keymodule \_ STATISTICS0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_ip_version_specific_keymodule_statistics0)
-   [**Ikeext \_ IP- \_ Versions \_ spezifisches \_ keymodule \_ STATISTICS1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_ip_version_specific_keymodule_statistics1)
-   [**Ikeext \_ IPv6- \_ CGA \_ AUTHENTICATION0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_ipv6_cga_authentication0)
-   [**Ikeext \_ Kerberos \_ AUTHENTICATION0**](/windows/win32/api/iketypes/ns-iketypes-ikeext_kerberos_authentication0)
-   [**Ikeext \_ Kerberos \_ AUTHENTICATION1**](/windows/win32/api/iketypes/ns-iketypes-ikeext_kerberos_authentication1)
-   [**Ikeext \_ keymodule \_ STATISTICS0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_keymodule_statistics0)
-   [**Ikeext \_ keymodule \_ STATISTICS1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_keymodule_statistics1)
-   [**Ikeext- \_ Name \_ CREDENTIAL0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_name_credential0)
-   [**Ikeext \_ NTLM \_ v2 \_ AUTHENTICATION0**](/windows/win32/api/iketypes/ns-iketypes-ikeext_ntlm_v2_authentication0)
-   [**Ikeext \_ POLICY0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_policy0)
-   [**Ikeext \_ Richtlinie1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_policy1)
-   [**Ikeext \_ POLICY2**](/windows/win32/api/iketypes/ns-iketypes-ikeext_policy2)
-   [**Ikeext, \_ vorinstaltzter \_ Schlüssel \_ AUTHENTICATION0**](/windows/win32/api/iketypes/ns-iketypes-ikeext_preshared_key_authentication0)
-   [**Ikeext, \_ vorinstaltzter \_ Schlüssel \_ AUTHENTICATION1**](/windows/win32/api/iketypes/ns-iketypes-ikeext_preshared_key_authentication1)
-   [**Ikeext \_ PROPOSAL0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_proposal0)
-   [**Ikeext \_ reserviert \_ AUTHENTICATION0**](/windows/win32/api/iketypes/ns-iketypes-ikeext_reserved_authentication0)
-   [**Ikeext \_ sa \_ DETAILS0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_sa_details0)
-   [**Ikeext \_ sa \_ DETAILS1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_sa_details1)
-   [**Ikeext \_ sa \_ DETAILS2**](/windows/win32/api/iketypes/ns-iketypes-ikeext_sa_details2)
-   [**Ikeext SA-Aufzählung \_ \_ \_ TEMPLATE0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_sa_enum_template0)
-   [**Ikeext \_ STATISTICS0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_statistics0)
-   [**Ikeext \_ STATISTICS1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_statistics1)
-   [**Ikeext \_ TRAFFIC0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_traffic0)

 

 




