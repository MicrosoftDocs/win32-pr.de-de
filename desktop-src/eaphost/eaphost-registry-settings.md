---
title: EAPHost Registry Einstellungen
description: Registrierungswerte in den folgenden Registrierungsschlüsseln steuern Aspekte der Funktionalität von EAPHost.
ms.assetid: 2b954911-7c2e-4c86-b031-24632235a669
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec08a7428dac4c68044b0491e084574c6ff3d006fcf06f59912754c5a9f93833
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119482980"
---
# <a name="eaphost-registry-settings"></a>EAPHost Registry Einstellungen

Registrierungswerte in den folgenden Registrierungsschlüsseln steuern Aspekte der Funktionalität von EAPHost.



| Unterschlüssel                                                                 | BESCHREIBUNG                                                                                                                                                              |
|------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [BypassNegotiation](bypassnegotiation.md)                             | Bestimmt, ob die Aushandlung von Funktionen zwischen ras-Server und Client erfolgt.<br/>                                                                              |
| [AssumePhase2Fragmentation](assumephase2fragmentation.md)             | Bestimmt, ob ras-Server und -Client von der Fragmentierung der Phase 2 ausgehen.<br/>                                                                                         |
| [OverrideEAPCertificateSelection](overrideeapcertificateselection.md) | Bestimmt, ob der Client das Standardmäßige Smartcard-Zertifikatauswahlverhalten überschreibt und dem Benutzer weitere Zertifikate zur Auswahl bereitstellt.<br/> |
| [PeapServerUseAllPurposeCert](peapserveruseallpurposecert.md)         | Bestimmt, ob allzweckbezogene Zertifikate für die PEAP-Authentifizierung verwendet werden.<br/>                                                                                      |
| [PeapServerAcceptAllPurposeCert](peapserveracceptallpurposecert.md)   | Bestimmt, ob Alle-Zweck-Zertifikate für die PEAP-Authentifizierung akzeptiert werden.<br/>                                                                                  |
| [TlsServerUseAllPurposeCert](tlsserveruseallpurposecert.md)           | Bestimmt, ob Alle-Zweck-Zertifikate für die EAP-TLS-Authentifizierung verwendet werden.<br/>                                                                                   |
| [TlsServerAcceptAllPurposeCert](tlsserveracceptallpurposecert.md)     | Bestimmt, ob Alle-Zweck-Zertifikate für die EAP-TLS-Authentifizierung akzeptiert werden.<br/>                                                                               |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[EAPHost-API-Referenz](eaphost-api-reference.md)
</dt> </dl>

 

 





