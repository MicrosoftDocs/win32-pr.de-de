---
description: Die folgenden Methoden werden von der IOCSPAdmin-Schnittstelle definiert. Die Eigenschaften Zugriffsmethoden werden hier nicht angezeigt. Die Eigenschaften von IOCSPAdmin finden Sie unter Eigenschaften von IOCSPAdmin.
ms.assetid: cbe43e5d-cd1b-467c-a0fd-1ee7cc5adcf7
title: Methoden von IOCSPAdmin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9ecd14d2566c5e80e863ba06e38b2945492f59b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343848"
---
# <a name="methods-of-iocspadmin"></a>Methoden von IOCSPAdmin

Die folgenden Methoden werden von der [**IOCSPAdmin**](/windows/desktop/api/certadm/nn-certadm-iocspadmin) -Schnittstelle definiert. Die Eigenschaften Zugriffsmethoden werden hier nicht angezeigt. Die Eigenschaften von **IOCSPAdmin** finden Sie unter [Eigenschaften von IOCSPAdmin](properties-of-iocspadmin.md).



| Methode                                                              | BESCHREIBUNG                                                                                                                                                                                                                                                               |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetConfiguration**](/windows/desktop/api/Certadm/nf-certadm-iocspadmin-getconfiguration)      | Stellt eine Verbindung mit einem OCSP-responderserver (Online Certificate Status-Protokoll) her und initialisiert ein **ocspadmin** -Objekt mit den Konfigurationsinformationen vom Server.                                                                                                     |
| [**Gethashalgorithms**](/windows/desktop/api/Certadm/nf-certadm-iocspadmin-gethashalgorithms)           | Ruft eine Liste mit hashalgorithmusnamen ab. Der Beantworter-Server verwendet einen der benannten Algorithmen, um OCSP-Antworten für eine bestimmte [*Zertifizierungs*](../secgloss/c-gly.md) stellen Konfiguration (ca) zu signieren. |
| [**Getmyrollen**](/windows/desktop/api/Certadm/nf-certadm-iocspadmin-getmyroles)                  | Ruft die Zugriffs Maske von Berechtigungs Rollen für einen Benutzer auf einem bestimmten Antwort Server ab.                                                                                                                                                                                           |
| [**GetSecurity**](/windows/desktop/api/Certadm/nf-certadm-iocspadmin-getsecurity)                       | Ruft Sicherheits Deskriptorinformationen für einen Antwort Server ab.                                                                                                                                                                                                              |
| [**Getsigningzertifikate**](/windows/desktop/api/Certadm/nf-certadm-iocspadmin-getsigningcertificates) | Ruft die Signatur Zertifikate ab, die auf einem Beantworter-Server für ein bestimmtes Zertifizierungsstellen Zertifikat verfügbar sind.                                                                                                                                                                        |
| [**Ping**](/windows/desktop/api/Certadm/nf-certadm-iocspadmin-ping)                                     | Testet eine DCOM-Verbindung mit einem Beantworter-Dienst.                                                                                                                                                                                                                         |
| [**SetConfiguration**](/windows/desktop/api/Certadm/nf-certadm-iocspadmin-setconfiguration)      | Aktualisiert einen Beantworter-Dienst mit Konfigurationsänderungen.                                                                                                                                                                                                                   |
| [**SetSecurity**](/windows/desktop/api/Certadm/nf-certadm-iocspadmin-setsecurity)                       | Aktualisiert Sicherheits Deskriptorinformationen für einen OCSP-Beantworter-Server.                                                                                                                                                                                                     |



 

 

 
