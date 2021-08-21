---
title: IKE/AuthIP-Strukturen
description: IKE/AuthIP-Strukturen
ms.assetid: 3267EA3C-FD1F-4ED1-9794-92551222EFE1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5de46cd72ec382dd360e6311930e946da3bf4189855adeaa49915b15ce3a9865
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069090"
---
# <a name="ikeauthip-structures"></a>IKE/AuthIP-Strukturen

## <a name="in-this-section"></a>In diesem Abschnitt

-   [**\_IKEEXT-AUTHENTIFIZIERUNGSMETHODE0 \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_authentication_method0)
-   [**\_IKEEXT-AUTHENTIFIZIERUNGSMETHODE1 \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_authentication_method1)
-   [**\_IKEEXT-AUTHENTIFIZIERUNGSMETHODE2 \_**](/windows/win32/api/iketypes/ns-iketypes-ikeext_authentication_method2)
-   [**IKEEXT \_ CERT \_ EKUS0**](/windows/win32/api/iketypes/ns-iketypes-ikeext_cert_ekus0)
-   [**\_IKEEXT-ZERTIFIKATNAME0 \_**](/windows/win32/api/iketypes/ns-iketypes-ikeext_cert_name0)
-   [**IKEEXT \_ CERT \_ ROOT \_ CONFIG0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_cert_root_config0)
-   [**IKEEXT \_ CERTIFICATE \_ AUTHENTICATION0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_certificate_authentication0)
-   [**IKEEXT \_ CERTIFICATE \_ AUTHENTICATION1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_certificate_authentication1)
-   [**IKEEXT \_ CERTIFICATE \_ AUTHENTICATION2**](/windows/win32/api/iketypes/ns-iketypes-ikeext_certificate_authentication2)
-   [**IKEEXT \_ CERTIFICATE \_ CREDENTIAL0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_certificate_credential0)
-   [**IKEEXT \_ CERTIFICATE \_ CREDENTIAL1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_certificate_credential1)
-   [**IKEEXT \_ CERTIFICATE \_ CRITERIA0**](/windows/win32/api/iketypes/ns-iketypes-ikeext_certificate_criteria0)
-   [**IKEEXT \_ CIPHER \_ ALGORITHM0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_cipher_algorithm0)
-   [**IKEEXT \_ COMMON \_ STATISTICS0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_common_statistics0)
-   [**IKEEXT \_ COMMON \_ STATISTICS1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_common_statistics1)
-   [**IKEEXT \_ COOKIE \_ PAIR0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_cookie_pair0)
-   [**IKEEXT \_ CREDENTIAL0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credential0)
-   [**IKEEXT \_ CREDENTIAL1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credential1)
-   [**IKEEXT \_ CREDENTIAL2**](/windows/win32/api/iketypes/ns-iketypes-ikeext_credential2)
-   [**IKEEXT \_ CREDENTIALS0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credentials0)
-   [**IKEEXT \_ CREDENTIALS1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credentials1)
-   [**IKEEXT \_ CREDENTIALS2**](/windows/win32/api/iketypes/ns-iketypes-ikeext_credentials2)
-   [**IKEEXT \_ CREDENTIAL \_ PAIR0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credential_pair0)
-   [**IKEEXT \_ CREDENTIAL \_ PAIR1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credential_pair1)
-   [**IKEEXT \_ CREDENTIAL \_ PAIR2**](/windows/win32/api/iketypes/ns-iketypes-ikeext_credential_pair2)
-   [**IKEEXT \_ EAP \_ AUTHENTICATION0**](/windows/win32/api/iketypes/ns-iketypes-ikeext_eap_authentication0)
-   [**IKEEXT \_ EM \_ POLICY0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_em_policy0)
-   [**IKEEXT \_ EM \_ POLICY1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_em_policy1)
-   [**IKEEXT \_ EM \_ POLICY2**](/windows/win32/api/iketypes/ns-iketypes-ikeext_em_policy2)
-   [**IKEEXT \_ INTEGRITY \_ ALGORITHM0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_integrity_algorithm0)
-   [**IKEEXT \_ IP \_ VERSION \_ SPECIFIC \_ COMMON \_ STATISTICS0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_ip_version_specific_common_statistics0)
-   [**IKEEXT \_ IP \_ VERSION \_ SPECIFIC \_ COMMON \_ STATISTICS1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_ip_version_specific_common_statistics1)
-   [**IKEEXT \_ IP \_ VERSION \_ SPECIFIC \_ KEYMODULE \_ STATISTICS0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_ip_version_specific_keymodule_statistics0)
-   [**IKEEXT \_ IP \_ VERSION \_ SPECIFIC \_ KEYMODULE \_ STATISTICS1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_ip_version_specific_keymodule_statistics1)
-   [**IKEEXT \_ IPV6 \_ CGA \_ AUTHENTICATION0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_ipv6_cga_authentication0)
-   [**IKEEXT \_ KERBEROS \_ AUTHENTICATION0**](/windows/win32/api/iketypes/ns-iketypes-ikeext_kerberos_authentication0)
-   [**IKEEXT \_ KERBEROS \_ AUTHENTICATION1**](/windows/win32/api/iketypes/ns-iketypes-ikeext_kerberos_authentication1)
-   [**IKEEXT \_ KEYMODULE \_ STATISTICS0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_keymodule_statistics0)
-   [**IKEEXT \_ KEYMODULE \_ STATISTICS1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_keymodule_statistics1)
-   [**IKEEXT \_ NAME \_ CREDENTIAL0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_name_credential0)
-   [**IKEEXT \_ NTLM \_ V2 \_ AUTHENTICATION0**](/windows/win32/api/iketypes/ns-iketypes-ikeext_ntlm_v2_authentication0)
-   [**IKEEXT \_ POLICY0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_policy0)
-   [**IKEEXT \_ POLICY1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_policy1)
-   [**IKEEXT \_ POLICY2**](/windows/win32/api/iketypes/ns-iketypes-ikeext_policy2)
-   [**IKEEXT \_ PRESHARED \_ KEY \_ AUTHENTICATION0**](/windows/win32/api/iketypes/ns-iketypes-ikeext_preshared_key_authentication0)
-   [**IKEEXT \_ PRESHARED \_ KEY \_ AUTHENTICATION1**](/windows/win32/api/iketypes/ns-iketypes-ikeext_preshared_key_authentication1)
-   [**IKEEXT \_ PROPOSAL0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_proposal0)
-   [**RESERVIERTE \_ \_ IKEEXT-AUTHENTIFIZIERUNG0**](/windows/win32/api/iketypes/ns-iketypes-ikeext_reserved_authentication0)
-   [**IKEEXT \_ SA \_ DETAILS0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_sa_details0)
-   [**IKEEXT \_ SA \_ DETAILS1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_sa_details1)
-   [**IKEEXT \_ SA \_ DETAILS2**](/windows/win32/api/iketypes/ns-iketypes-ikeext_sa_details2)
-   [**IKEEXT \_ SA \_ ENUM \_ TEMPLATE0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_sa_enum_template0)
-   [**IKEEXT \_ STATISTICS0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_statistics0)
-   [**IKEEXT \_ STATISTICS1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_statistics1)
-   [**IKEEXT \_ TRAFFIC0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_traffic0)

 

 




