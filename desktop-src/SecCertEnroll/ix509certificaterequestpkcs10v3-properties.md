---
description: Die IX509CertificateRequestPkcs10V3-Schnittstelle macht die folgenden Eigenschaften verfügbar.
ms.assetid: 96FCB9C4-7DDB-4B6B-A776-5A33E07B0BD3
title: IX509CertificateRequestPkcs10V3-Eigenschaften
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d43fcc126c21ca5fee5e8d1c15dd2561439c7a35f0f6cef637177ff36160a22d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119976220"
---
# <a name="ix509certificaterequestpkcs10v3-properties"></a>IX509CertificateRequestPkcs10V3-Eigenschaften

Die [**IX509CertificateRequestPkcs10V3-Schnittstelle**](/windows/desktop/api/Certenroll/nn-certenroll-ix509certificaterequestpkcs10v3) macht die folgenden Eigenschaften verfügbar.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                                                            | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AttestationEncryptionCertificate(Eigenschaft)**](/windows/desktop/api/Certenroll/nf-certenroll-ix509certificaterequestpkcs10v3-get_attestationencryptioncertificate)<br/> | Das Zertifikat, das zum Verschlüsseln der EKPUB- und EKCERT-Werte vom Client verwendet wird. Diese Eigenschaft muss auf ein gültiges Zertifikat festgelegt werden, das mit einem vertrauenswürdigen Computerstamm verkettet ist.<br/>                                                                                                                                                                                |
| [**AttestPrivateKey(Eigenschaft)**](/windows/desktop/api/Certenroll/nf-certenroll-ix509certificaterequestpkcs10v3-get_attestprivatekey)<br/>                                 | TRUE, wenn der erstellte private Schlüssel bestätigt werden muss. andernfalls FALSE. True gibt an, dass die [**AttestationEncryptionCertificate-Eigenschaft**](/windows/desktop/api/Certenroll/nf-certenroll-ix509certificaterequestpkcs10v3-get_attestationencryptioncertificate) festgelegt wurde. <br/>                                                                                                        |
| [**ChallengePassword-Eigenschaft**](/windows/desktop/api/Certenroll/nf-certenroll-ix509certificaterequestpkcs10v3-get_challengepassword)<br/>                               | Das Kennwort, das beim Erstellen einer Anforderung mit einer Herausforderung verwendet werden soll. Legen Sie die [**ChallengePassword-Eigenschaft**](/windows/desktop/api/Certenroll/nf-certenroll-ix509certificaterequestpkcs10v3-get_challengepassword) nicht fest, um eine Anforderung ohne Aufforderung zu erstellen.<br/>                                                                                                                                      |
| [**EncryptionAlgorithm (Eigenschaft)**](/windows/desktop/api/Certenroll/nf-certenroll-ix509certificaterequestpkcs10v3-get_encryptionalgorithm)<br/>                           | Der Verschlüsselungsalgorithmus, der zum Verschlüsseln der EKPUB- und EKCERT-Werte vom Client verwendet wird.<br/>                                                                                                                                                                                                                                                               |
| [**EncryptionStrength-Eigenschaft**](/windows/desktop/api/Certenroll/nf-certenroll-ix509certificaterequestpkcs10v3-get_encryptionstrength)<br/>                             | Gibt die Bitlänge für [**encryptionAlgorithm an,**](/windows/desktop/api/Certenroll/nf-certenroll-ix509certificaterequestpkcs10v3-get_encryptionalgorithm) die für die Verschlüsselung verwendet werden soll. Wenn **EncryptionAlgorithm** nur eine Bitlänge unterstützt, müssen Sie keinen Wert für die [**EncryptionStrength-Eigenschaft**](/windows/desktop/api/Certenroll/nf-certenroll-ix509certificaterequestpkcs10v3-get_encryptionstrength) angeben.<br/> |
| [**NameValuePairs(Eigenschaft)**](/windows/desktop/api/Certenroll/nf-certenroll-ix509certificaterequestpkcs10v3-get_namevaluepairs)<br/>                                     | Eine Auflistung von Name-Wert-Paaren zusätzlicher Zertifikateigenschaftswerte.<br/>                                                                                                                                                                                                                                                                         |



 

 

 




