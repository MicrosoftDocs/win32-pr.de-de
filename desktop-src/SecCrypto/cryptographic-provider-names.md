---
description: Wird mit den Funktionen CryptAcquireContext und cryptsetprovider verwendet.
ms.assetid: 97e9a708-83b5-48b3-9d16-f7b54367dc4e
title: Kryptografieanbienernamen (Wincrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58a5cbe497e56144a9948dab96be0c03dd5a99f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958842"
---
# <a name="cryptographic-provider-names"></a>Name des Kryptografieanbieters

Die folgenden CSP-Namen ( [*kryptografischen Service Provider*](../secgloss/c-gly.md) ) sind in Wincrypt. h definiert. Diese Konstanten werden mit den Funktionen [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) und [**cryptsetprovider**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetprovidera) verwendet.



| Konstante/Wert                                                                                                                                                                                                                                                                                          | BESCHREIBUNG                                                                                                                                                                                      |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MS_DEF_DH_SCHANNEL_PROV"></span><span id="ms_def_dh_schannel_prov"></span><dl> <dt>**MS \_ DEF \_ dh \_ SChannel \_ Prov**</dt> <dt>"Microsoft DH SChannel Cryptographic Provider"</dt> </dl>      | Der [Kryptografieanbieter Microsoft DSS und Diffie-Hellman/SChannel](microsoft-dss-and-diffie-hellman-schannel-cryptographic-provider.md).<br/>                                         |
| <span id="MS_DEF_DSS_DH_PROV"></span><span id="ms_def_dss_dh_prov"></span><dl> <dt>**MS \_ DEF \_ DSS \_ dh \_ Prov**</dt> <dt>"Microsoft Base DSS and Diffie-Hellman Cryptographic Provider"</dt> </dl>     | Der [Microsoft Base DSS und der Diffie-Hellman Kryptografieanbieter](microsoft-base-dss-and-diffie-hellman-cryptographic-provider.md).<br/>                                                 |
| <span id="MS_DEF_DSS_PROV"></span><span id="ms_def_dss_prov"></span><dl> <dt>**MS \_ DEF \_ DSS \_ Prov**</dt> <dt>"Microsoft Base DSS Cryptographic Provider"</dt> </dl>                                  | Der [Microsoft DSS-Kryptografieanbieter](microsoft-dss-cryptographic-provider.md).<br/>                                                                                                 |
| <span id="MS_DEF_PROV"></span><span id="ms_def_prov"></span><dl> <dt>**MS \_ DEF \_ Prov**</dt> <dt>"Microsoft Base Cryptographic Provider v 1.0"</dt> </dl>                                              | Der [Kryptografieanbieter von Microsoft](microsoft-base-cryptographic-provider.md).<br/>                                                                                               |
| <span id="MS_DEF_RSA_SCHANNEL_PROV"></span><span id="ms_def_rsa_schannel_prov"></span><dl> <dt>**MS \_ DEF \_ RSA \_ SChannel \_ Prov**</dt> <dt>"Microsoft RSA SChannel Cryptographic Provider"</dt> </dl>  | Der [Kryptografieanbieter Microsoft RSA/SChannel](microsoft-rsa-schannel-cryptographic-provider.md).<br/>                                                                               |
| <span id="MS_DEF_RSA_SIG_PROV"></span><span id="ms_def_rsa_sig_prov"></span><dl> <dt>**MS \_ DEF \_ RSA \_ sig \_ Prov**</dt> <dt>"Microsoft RSA Signature Cryptographic Provider"</dt> </dl>                | Der [Kryptografieanbieter für Microsoft RSA Signature](microsoft-rsa-signature-cryptographic-provider.md) wird nicht unterstützt.<br/>                                                            |
| <span id="MS_ENH_DSS_DH_PROV"></span><span id="ms_enh_dss_dh_prov"></span><dl> <dt>**MS \_ Enh \_ DSS \_ dh \_ Prov**</dt> <dt>"Microsoft Enhanced DSS and Diffie-Hellman Cryptographic Provider"</dt> </dl> | Der [Microsoft Enhanced DSS und der Diffie-Hellman Kryptografieanbieter](microsoft-enhanced-dss-and-diffie-hellman-cryptographic-provider.md).<br/>                                         |
| <span id="MS_ENH_RSA_AES_PROV"></span><span id="ms_enh_rsa_aes_prov"></span><dl> <dt>**MS \_ Enh \_ RSA \_ AES \_ Prov**</dt> <dt>"Microsoft Enhanced RSA and AES Cryptographic Provider"</dt> </dl>         | Der [Kryptografieanbieter von Microsoft AES](microsoft-aes-cryptographic-provider.md).<br/> * * Windows XP: * * "Microsoft Enhanced RSA and AES Cryptographic Provider (Prototype)"<br/> |
| <span id="MS_ENHANCED_PROV"></span><span id="ms_enhanced_prov"></span><dl> <dt>**MS \_ Enhanced \_ Prov**</dt> <dt>"Microsoft Enhanced Cryptographic Provider v 1.0"</dt> </dl>                           | Der [Microsoft Enhanced Cryptographic Provider](microsoft-enhanced-cryptographic-provider.md).<br/>                                                                                       |
| <span id="MS_SCARD_PROV"></span><span id="ms_scard_prov"></span><dl> <dt>**MS \_ Card \_ Prov**</dt> <dt>"Microsoft Base Smartcard-Kryptografieanbieter"</dt> </dl>                                         | Der [Kryptografiedienstanbieter der Microsoft-Basis Smartcard](/previous-versions/windows/desktop/secsmart/microsoft-base-smart-card-cryptographic-service-provider).<br/>                                                    |
| <span id="MS_STRONG_PROV"></span><span id="ms_strong_prov"></span><dl> <dt>**MS \_ Starker \_ Prov**</dt> <dt>"Microsoft Strong Cryptographic Provider"</dt> </dl>                                        | Der [Microsoft-starke Kryptografieanbieter](microsoft-strong-cryptographic-provider.md).<br/>                                                                                           |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>WinCrypt. h</dt> </dl> |



 

 
