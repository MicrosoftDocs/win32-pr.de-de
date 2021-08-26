---
description: Die folgenden Methoden werden von der IOCSPAdmin-Schnittstelle definiert. Die Methoden für den Eigenschaftenzugriff werden hier nicht angezeigt. Die Eigenschaften für IOCSPAdmin finden Sie unter Eigenschaften von IOCSPAdmin.
ms.assetid: cbe43e5d-cd1b-467c-a0fd-1ee7cc5adcf7
title: Methoden von IOCSPAdmin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a455ae5cfbb49d60cc0d0a03265d05c98efa2f2217746086b0acf0a4230709dc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992850"
---
# <a name="methods-of-iocspadmin"></a>Methoden von IOCSPAdmin

Die folgenden Methoden werden von der [**IOCSPAdmin-Schnittstelle**](/windows/desktop/api/certadm/nn-certadm-iocspadmin) definiert. Die Methoden für den Eigenschaftenzugriff werden hier nicht angezeigt. Die Eigenschaften für **IOCSPAdmin** finden Sie unter [Eigenschaften von IOCSPAdmin](properties-of-iocspadmin.md).



| Methode                                                              | BESCHREIBUNG                                                                                                                                                                                                                                                               |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetConfiguration**](/windows/desktop/api/Certadm/nf-certadm-iocspadmin-getconfiguration)      | Stellt eine Verbindung mit einem OCSP-Antwortserver (Online Certificate Status Protocol) her und initialisiert ein **OCSPAdmin-Objekt** mit den Konfigurationsinformationen vom Server.                                                                                                     |
| [**GetHashAlgorithms**](/windows/desktop/api/Certadm/nf-certadm-iocspadmin-gethashalgorithms)           | Ruft eine Liste von Hashalgorithmusnamen ab. Der Antwortserver verwendet einen der benannten Algorithmen, um OCSP-Antworten für eine bestimmte [*Zertifizierungsstellenkonfiguration*](../secgloss/c-gly.md) zu signieren. |
| [**GetMyRoles**](/windows/desktop/api/Certadm/nf-certadm-iocspadmin-getmyroles)                  | Ruft die Zugriffsmaske von Berechtigungsrollen für einen Benutzer auf einem bestimmten Antwortserver ab.                                                                                                                                                                                           |
| [**GetSecurity**](/windows/desktop/api/Certadm/nf-certadm-iocspadmin-getsecurity)                       | Ruft Sicherheitsbeschreibungsinformationen für einen Antwortserver ab.                                                                                                                                                                                                              |
| [**GetSigningCertificates**](/windows/desktop/api/Certadm/nf-certadm-iocspadmin-getsigningcertificates) | Ruft die Signaturzertifikate ab, die auf einem Antwortserver für ein bestimmtes Zertifizierungsstellenzertifikat verfügbar sind.                                                                                                                                                                        |
| [**Pingen**](/windows/desktop/api/Certadm/nf-certadm-iocspadmin-ping)                                     | Testet eine DCOM-Verbindung mit einem Antwortdienst.                                                                                                                                                                                                                         |
| [**SetConfiguration**](/windows/desktop/api/Certadm/nf-certadm-iocspadmin-setconfiguration)      | Aktualisiert einen Antwortdienst mit Konfigurationsänderungen.                                                                                                                                                                                                                   |
| [**SetSecurity**](/windows/desktop/api/Certadm/nf-certadm-iocspadmin-setsecurity)                       | Aktualisiert Sicherheitsbeschreibungsinformationen für einen OCSP-Antwortserver.                                                                                                                                                                                                     |



 

 

 
