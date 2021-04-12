---
description: Die IX509EndorsementKey-Schnittstelle stellt die folgenden Methoden zur Verfügung.
ms.assetid: 536E5DE6-FF14-45C8-9227-68AF673E5FDC
title: IX509EndorsementKey-Methoden
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3c1eb6a96cd555d4b0a0fdcd2ad52ccf80ec4aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218332"
---
# <a name="ix509endorsementkey-methods"></a>IX509EndorsementKey-Methoden

Die [**IX509EndorsementKey**](/windows/desktop/api/Certenroll/nn-certenroll-ix509endorsementkey) -Schnittstelle stellt die folgenden Methoden zur Verfügung.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                        | BESCHREIBUNG                                                                                                                                                                                                                                                                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddCertificate-Methode**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-addcertificate)<br/>               | Fügen Sie dem Schlüsselspeicher Anbieter (KSP) ein Endorsement Key-Zertifikat hinzu, das Endorsement Keys unterstützt.<br/>                                                                                                                                                                                     |
| [**Close-Methode**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-close)<br/>                                 | Schließt den Endorsement Key. Sie können die [**Close**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-close) -Methode nur aufrufen, nachdem die [**Open**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open) -Methode erfolgreich aufgerufen wurde.<br/>                                                                                              |
| [**Exportpublickey-Methode**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-exportpublickey)<br/>             | Exportiert den öffentlichen Endorsement Key.<br/>                                                                                                                                                                                                                                                      |
| [**Getcertificatebyindex-Methode**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-getcertificatebyindex)<br/> | Ruft das Endorsement Certificate ab, das dem Endorsement Key des Schlüsselspeicher Anbieters für den angegebenen Index zugeordnet ist.<br/>                                                                                                                                                              |
| [**Getcertificatecount-Methode**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-getcertificatecount)<br/>     | Ruft die Anzahl der Endorsement-Zertifikate im Schlüsselspeicher Anbieter ab.<br/>                                                                                                                                                                                                              |
| [**Open-Methode**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open)<br/>                                   | Öffnet den Endorsement Key. Der Endorsement Key muss geöffnet sein, bevor Sie Informationen aus dem Endorsement Key abrufen, Zertifikate hinzufügen oder entfernen oder den Endorsement Key exportieren können.<br/>                                                                                                  |
| [**RemoveCertificate-Methode**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-removecertificate)<br/>         | Entfernt ein Endorsement Certificate, das mit dem Endorsement Key des Schlüsselspeicher Anbieters verknüpft ist. Sie können die [**RemoveCertificate**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-removecertificate) -Methode nur aufrufen, nachdem die [**Open**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open) -Methode erfolgreich aufgerufen wurde.<br/> |



 

 

 




