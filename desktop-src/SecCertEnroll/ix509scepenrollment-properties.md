---
description: Die IX509SCEPEnrollment-Schnittstelle macht die folgenden Eigenschaften verfügbar.
ms.assetid: 53BE8DE9-87AC-41D1-B1B5-2FEC72F5FCEA
title: IX509SCEPEnrollment-Eigenschaften
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fd9b4cbf9df87f898e61ce0220243044b24607d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360672"
---
# <a name="ix509scepenrollment-properties"></a>IX509SCEPEnrollment-Eigenschaften

Die [**IX509SCEPEnrollment**](/windows/desktop/api/Certenroll/nn-certenroll-ix509scepenrollment) -Schnittstelle macht die folgenden Eigenschaften verfügbar.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                              | BESCHREIBUNG                                                                                                                                            |
|----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Zertifikat Eigenschaft**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-get_certificate)<br/>                         | Ruft das Zertifikat für die Anforderung ab.<br/>                                                                                                       |
| [**Certificatefriendlyname (Eigenschaft)**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-get_certificatefriendlyname)<br/> | Ruft den anzeigen Amen für das Zertifikat ab oder legt ihn fest.<br/>                                                                                         |
| [**Failinfo-Eigenschaft**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-get_failinfo)<br/>                               | Ruft Informationen ab, wenn die [**ProcessResponse Message**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-processresponsemessage) -Methode eine fehlerhafte Umgebung erkennt.<br/> |
| [**Oldcertificate (Eigenschaft)**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-get_oldcertificate)<br/>                   | Ruft ein altes Zertifikat ab, das von einer Anforderung ersetzt werden soll, oder legt dieses fest.<br/>                                                                      |
| [**Anforderungs Eigenschaft**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-get_request)<br/>                                 | Ruft die innere PKCS10-Anforderung ab.<br/>                                                                                                              |
| [**Serverfunktionalitäten (Eigenschaft)**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-put_servercapabilities)<br/>           | Legt die bevorzugten Hash-und Verschlüsselungsalgorithmen für die Anforderung fest.<br/>                                                                          |
| [**SignerCertificate (Eigenschaft)**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-get_signercertificate)<br/>             | Ruft das Signatur Geber Zertifikat für die Anforderung ab oder legt es fest.<br/>                                                                                        |
| [**Silent (Eigenschaft)**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-put_silent)<br/>                                   | Ruft ab oder legt fest, ob die Benutzeroberfläche während der Anforderung zugelassen wird.<br/>                                                                                        |
| [**Status (Eigenschaft)**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-get_status)<br/>                                   | Ruft den Status der Anforderung ab.<br/>                                                                                                             |
| [**Transaktionid (Eigenschaft)**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-get_transactionid)<br/>                     | Ruft die Transaktions-ID für die Anforderung ab oder legt Sie fest.<br/>                                                                                            |



 

 

 




