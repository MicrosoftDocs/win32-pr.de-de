---
description: Die IX509CertificateRequestPkcs10V3-Schnittstelle macht die folgenden Eigenschaften verfügbar.
ms.assetid: 96FCB9C4-7DDB-4B6B-A776-5A33E07B0BD3
title: IX509CertificateRequestPkcs10V3-Eigenschaften
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db4967b10e49ed015b22ffcab19726f5662937d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960754"
---
# <a name="ix509certificaterequestpkcs10v3-properties"></a>IX509CertificateRequestPkcs10V3-Eigenschaften

Die [**IX509CertificateRequestPkcs10V3**](/windows/desktop/api/Certenroll/nn-certenroll-ix509certificaterequestpkcs10v3) -Schnittstelle macht die folgenden Eigenschaften verfügbar.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                                                            | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Attestationverschlüsseltioncertificate (Eigenschaft)**](/windows/desktop/api/Certenroll/nf-certenroll-ix509certificaterequestpkcs10v3-get_attestationencryptioncertificate)<br/> | Das Zertifikat, das zum Verschlüsseln der ekpub-und ekcert-Werte vom Client verwendet wird. Diese Eigenschaft muss auf ein gültiges Zertifikat festgelegt werden, das mit einem vertrauenswürdigen Computer Stamm verkettet ist.<br/>                                                                                                                                                                                |
| [**Attestprivatekey (Eigenschaft)**](/windows/desktop/api/Certenroll/nf-certenroll-ix509certificaterequestpkcs10v3-get_attestprivatekey)<br/>                                 | True, wenn der erstellte private Schlüssel bestätigt werden muss. andernfalls false. Wenn der Wert true ist, wird erwartet, dass die [**attestationverschlüsseltioncertificate**](/windows/desktop/api/Certenroll/nf-certenroll-ix509certificaterequestpkcs10v3-get_attestationencryptioncertificate) -Eigenschaft festgelegt wurde. <br/>                                                                                                        |
| [**Herausforderer Password (Eigenschaft)**](/windows/desktop/api/Certenroll/nf-certenroll-ix509certificaterequestpkcs10v3-get_challengepassword)<br/>                               | Das Kennwort, das beim Erstellen einer Anforderung mit einer Herausforderung verwendet werden soll. Wenn Sie eine Anforderung ohne eine Herausforderung erstellen möchten, legen [**Sie die Eigenschaft**](/windows/desktop/api/Certenroll/nf-certenroll-ix509certificaterequestpkcs10v3-get_challengepassword) "-Eigenschaft" nicht fest.<br/>                                                                                                                                      |
| [**Verschlüsselungsalgorithmus (Eigenschaft)**](/windows/desktop/api/Certenroll/nf-certenroll-ix509certificaterequestpkcs10v3-get_encryptionalgorithm)<br/>                           | Der Verschlüsselungsalgorithmus, der zum Verschlüsseln der ekpub-und ekcert-Werte vom Client verwendet wird.<br/>                                                                                                                                                                                                                                                               |
| [**Verschlüsselungsstärke (Eigenschaft)**](/windows/desktop/api/Certenroll/nf-certenroll-ix509certificaterequestpkcs10v3-get_encryptionstrength)<br/>                             | Gibt die Bitlänge für den Verschlüsselungs [**Algorithmus**](/windows/desktop/api/Certenroll/nf-certenroll-ix509certificaterequestpkcs10v3-get_encryptionalgorithm) an, der für die Verschlüsselung verwendet werden soll. Wenn der **Verschlüsselungsalgorithmus** nur eine bidirektionale Länge unterstützt, müssen Sie keinen Wert für die Eigenschaft " [**Verschlüsselungsstärke**](/windows/desktop/api/Certenroll/nf-certenroll-ix509certificaterequestpkcs10v3-get_encryptionstrength) " angeben.<br/> |
| [**NameValuePairs (Eigenschaft)**](/windows/desktop/api/Certenroll/nf-certenroll-ix509certificaterequestpkcs10v3-get_namevaluepairs)<br/>                                     | Eine Auflistung von Name-Wert-Paaren mit zusätzlichen Zertifikat Eigenschafts Werten.<br/>                                                                                                                                                                                                                                                                         |



 

 

 




