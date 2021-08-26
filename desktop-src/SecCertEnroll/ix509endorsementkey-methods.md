---
description: Die IX509EndorsementKey-Schnittstelle macht die folgenden Methoden verfügbar.
ms.assetid: 536E5DE6-FF14-45C8-9227-68AF673E5FDC
title: IX509EndorsementKey-Methoden
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83bc951830f308e2918558794c9790c9f57183ca250e17b7821ba2a152428576
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119881730"
---
# <a name="ix509endorsementkey-methods"></a>IX509EndorsementKey-Methoden

Die [**IX509EndorsementKey-Schnittstelle**](/windows/desktop/api/Certenroll/nn-certenroll-ix509endorsementkey) macht die folgenden Methoden verfügbar.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                        | BESCHREIBUNG                                                                                                                                                                                                                                                                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddCertificate-Methode**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-addcertificate)<br/>               | Fügen Sie dem Schlüsselspeicheranbieter (Key Storage Provider, KSP) ein Endorsement Key-Zertifikat hinzu, das Endorsement Keys unterstützt.<br/>                                                                                                                                                                                     |
| [**Close-Methode**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-close)<br/>                                 | Schließt den Endorsement Key. Sie können die [**Close-Methode nur aufrufen,**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-close) nachdem die [**Open-Methode**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open) erfolgreich aufgerufen wurde.<br/>                                                                                              |
| [**ExportPublicKey-Methode**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-exportpublickey)<br/>             | Exportiert den öffentlichen Endorsement Key.<br/>                                                                                                                                                                                                                                                      |
| [**GetCertificateByIndex-Methode**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-getcertificatebyindex)<br/> | Ruft das Endorsement Certificate ab, das dem Endorsement Key vom Schlüsselspeicheranbieter für den angegebenen Index zugeordnet ist.<br/>                                                                                                                                                              |
| [**GetCertificateCount-Methode**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-getcertificatecount)<br/>     | Ruft die Anzahl der Endorsement Certificates im Schlüsselspeicheranbieter ab.<br/>                                                                                                                                                                                                              |
| [**Open-Methode**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open)<br/>                                   | Öffnet den Endorsement Key. Der Endorsement Key muss offen sein, bevor Sie Informationen aus dem Endorsement Key abrufen, Zertifikate hinzufügen oder entfernen oder den Endorsement Key exportieren können.<br/>                                                                                                  |
| [**RemoveCertificate-Methode**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-removecertificate)<br/>         | Entfernt ein Endorsement Certificate, das sich auf den Endorsement Key bezieht, aus dem Schlüsselspeicheranbieter. Sie können die [**RemoveCertificate-Methode**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-removecertificate) nur aufrufen, nachdem die [**Open-Methode**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open) erfolgreich aufgerufen wurde.<br/> |



 

 

 




