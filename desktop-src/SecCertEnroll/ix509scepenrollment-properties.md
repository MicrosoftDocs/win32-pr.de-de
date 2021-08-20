---
description: Die IX509SCEPEnrollment-Schnittstelle macht die folgenden Eigenschaften verfügbar.
ms.assetid: 53BE8DE9-87AC-41D1-B1B5-2FEC72F5FCEA
title: IX509SCEPEnrollment-Eigenschaften
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf98252a1600ba8f5feceeeffe239730cf53ddee2096b85192083756bc7e5cc0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117774855"
---
# <a name="ix509scepenrollment-properties"></a>IX509SCEPEnrollment-Eigenschaften

Die [**IX509SCEPEnrollment-Schnittstelle**](/windows/desktop/api/Certenroll/nn-certenroll-ix509scepenrollment) macht die folgenden Eigenschaften verfügbar.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                              | Beschreibung                                                                                                                                            |
|----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Certificate-Eigenschaft**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-get_certificate)<br/>                         | Ruft das Zertifikat für die Anforderung ab.<br/>                                                                                                       |
| [**CertificateFriendlyName (Eigenschaft)**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-get_certificatefriendlyname)<br/> | Ruft den Benutzerfreundlichen Namen für das Zertifikat ab oder legt den Namen fest.<br/>                                                                                         |
| [**FailInfo-Eigenschaft**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-get_failinfo)<br/>                               | Ruft Informationen ab, wenn [**die ProcessResponseMessage-Methode**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-processresponsemessage) eine fehlerhafte Umgebung erkennt.<br/> |
| [**OldCertificate-Eigenschaft**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-get_oldcertificate)<br/>                   | Ruft ein altes Zertifikat ab, das durch eine Anforderung ersetzt werden soll, oder legt dieses fest.<br/>                                                                      |
| [**Anforderungseigenschaft**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-get_request)<br/>                                 | Ruft die innere PKCS10-Anforderung ab.<br/>                                                                                                              |
| [**ServerCapabilities-Eigenschaft**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-put_servercapabilities)<br/>           | Legt die bevorzugten Hash- und Verschlüsselungsalgorithmen für die Anforderung fest.<br/>                                                                          |
| [**SignerCertificate(Eigenschaft)**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-get_signercertificate)<br/>             | Ruft das Signatorzertifikat für die Anforderung ab oder legt es fest.<br/>                                                                                        |
| [**Silent-Eigenschaft**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-put_silent)<br/>                                   | Ruft ab oder legt fest, ob die Benutzeroberfläche während der Anforderung zulässig ist.<br/>                                                                                        |
| [**Status-Eigenschaft**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-get_status)<br/>                                   | Ruft den Status der Anforderung ab.<br/>                                                                                                             |
| [**TransactionId-Eigenschaft**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-get_transactionid)<br/>                     | Ruft die Transaktions-ID für die Anforderung ab oder legt sie fest.<br/>                                                                                            |



 

 

 




