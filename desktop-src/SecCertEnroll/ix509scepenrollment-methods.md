---
description: Die IX509SCEPEnrollment-Schnittstelle macht die folgenden Methoden verfügbar.
ms.assetid: B45B68D2-A14D-4D14-AF5F-1A1BB9921A0D
title: IX509SCEPEnrollment-Methoden
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a15fc7de6392c49bd38381771956685ba6c8427b3562e7c81c372c1bab61db49
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993540"
---
# <a name="ix509scepenrollment-methods"></a>IX509SCEPEnrollment-Methoden

Die [**IX509SCEPEnrollment-Schnittstelle**](/windows/desktop/api/Certenroll/nn-certenroll-ix509scepenrollment) macht die folgenden Methoden verfügbar.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                                              | Beschreibung                                                                                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateRequestMessage-Methode**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-createrequestmessage)<br/>                         | Erstellen Sie eine PKCS10-Anforderungsnachricht mit einem Aufforderungskennwort. Die Anforderungsnachricht befindet sich in einem umhumhierten PKCS7-Zertifikat, das mit dem SCEP-Serververschlüsselungszertifikat verschlüsselt und vom Serversignaturzertifikat signiert wird.<br/> |
| [**CreateRetriificCertificateMessage-Methode**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-createretrievecertificatemessage)<br/> | Rufen Sie ein zuvor ausgestelltes Zertifikat ab.<br/>                                                                                                                                                                   |
| [**CreateRetripendingPendingMessage-Methode**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-createretrievependingmessage)<br/>         | Erstellen Sie eine Nachricht für die Zertifikatsanforderung (manuelle Registrierung).<br/>                                                                                                                                               |
| [**DeleteRequest-Methode**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-deleterequest)<br/>                                       | Löschen Sie alle Zertifikate oder Schlüssel, die für die Anforderung erstellt wurden.<br/>                                                                                                                                                    |
| [**Initialize-Methode**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-initialize)<br/>                                             | Initialisieren Sie die -Instanz als Vorbereitung für eine neue Anforderung.<br/>                                                                                                                                                   |
| [**InitializeForPending-Methode**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-initializeforpending)<br/>                         | Initialisieren Sie die -Instanz, um die Generierung einer Nachricht zum Abrufen eines ausgestellten Zertifikats vorzubereiten, oder installieren Sie eine Antwort für eine vorherige Anforderung durch den Aussteller.<br/>                                              |
| [**ProcessResponseMessage-Methode**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-processresponsemessage)<br/>                     | Verarbeiten Sie eine Antwortnachricht, und geben Sie die Disposition der Nachricht zurück.<br/>                                                                                                                                       |



 

 

 




