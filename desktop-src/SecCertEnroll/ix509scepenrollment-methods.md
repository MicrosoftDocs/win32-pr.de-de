---
description: Die IX509SCEPEnrollment-Schnittstelle stellt die folgenden Methoden zur Verfügung.
ms.assetid: B45B68D2-A14D-4D14-AF5F-1A1BB9921A0D
title: IX509SCEPEnrollment-Methoden
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a33c3bdee14b865211b53649075dec6d4617a4c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363584"
---
# <a name="ix509scepenrollment-methods"></a>IX509SCEPEnrollment-Methoden

Die [**IX509SCEPEnrollment**](/windows/desktop/api/Certenroll/nn-certenroll-ix509scepenrollment) -Schnittstelle stellt die folgenden Methoden zur Verfügung.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                                              | BESCHREIBUNG                                                                                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Methode "samaterequestmessage"**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-createrequestmessage)<br/>                         | Erstellen Sie eine PKCS10-Anforderungs Nachricht mit einem Challenge-Kennwort. Die Anforderungs Nachricht befindet sich in einem eingeschlossenen PKCS7, das mit dem SCEP-Server Verschlüsselungs Zertifikat verschlüsselt und vom Server-Signaturzertifikat signiert wurde.<br/> |
| [**Methode "| aterezevecertificess"**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-createretrievecertificatemessage)<br/> | Rufen Sie ein zuvor ausgestelltes Zertifikat ab.<br/>                                                                                                                                                                   |
| [**Methode "kreaterezeveperedingmessage"**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-createretrievependingmessage)<br/>         | Erstellen Sie eine Nachricht für die Zertifikat Abruf Sperre (manuelle Registrierung).<br/>                                                                                                                                               |
| [**DeleteRequest-Methode**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-deleterequest)<br/>                                       | Löschen Sie alle Zertifikate und Schlüssel, die für die Anforderung erstellt wurden.<br/>                                                                                                                                                    |
| [**Initialize-Methode**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-initialize)<br/>                                             | Initialisieren Sie die-Instanz als Vorbereitung für eine neue Anforderung.<br/>                                                                                                                                                   |
| [**Initializeforpending-Methode**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-initializeforpending)<br/>                         | Initialisieren Sie die-Instanz, um eine Nachricht zu generieren, um entweder ein ausgestelltes Zertifikat abzurufen, oder eine Antwort für eine vorherige Anforderung vom Aussteller zu installieren.<br/>                                              |
| [**ProcessResponse Message-Methode**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-processresponsemessage)<br/>                     | Verarbeiten einer Antwortnachricht und Zurückgeben der Disposition der Nachricht.<br/>                                                                                                                                       |



 

 

 




