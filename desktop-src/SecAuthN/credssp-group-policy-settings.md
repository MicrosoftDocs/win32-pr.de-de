---
description: Damit das Credential Security Support Provider-Protokoll (CredSSP) Anmeldeinformationen delegieren kann, müssen Sie angeben, an welche Server delegiert werden kann.
ms.assetid: 15ed9a62-2eee-4f29-92c5-ccf2754cdf13
title: CredSSP-Gruppenrichtlinie Einstellungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8efaaab1b49efba89c9fa5788f60df372991f388c474d531eff8f59205af441
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008698"
---
# <a name="credssp-group-policy-settings"></a>CredSSP-Gruppenrichtlinie Einstellungen

Damit [das Credential Security Support Provider-Protokoll (CredSSP)](credential-security-support-provider.md) Anmeldeinformationen delegieren kann, müssen Sie angeben, an welche Server delegiert werden kann. Um diese Server anzugeben, ändern Sie die Einstellungen im MMC-Snap-In (Gruppenrichtlinie Editor) Microsoft Management Console (GPE). Die GPE-Einstellungen, die die Delegierung steuern, befinden sich unter **Computerkonfiguration \| Administrative Vorlagen \| \| Delegierung von Systemanmeldeinformationen.**

> [!Caution]  
> Dies ist keine eingeschränkte Delegierung. CredSSP übergibt die vollständigen Anmeldeinformationen des Benutzers ohne Einschränkung an den Server.

 

Gruppenrichtlinieneinstellungen steuern die Delegierung der folgenden Arten von Anmeldeinformationen.



| Anmeldeinformationstyp                                                                                                                                 | BESCHREIBUNG                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="Default_credentials"></span><span id="default_credentials"></span><span id="DEFAULT_CREDENTIALS"></span>Standardanmeldeinformationen<br/> | Die Anmeldeinformationen, die beim ersten Anmelden des Benutzers bei Windows abgerufen wurden.<br/>                   |
| <span id="Fresh_credentials"></span><span id="fresh_credentials"></span><span id="FRESH_CREDENTIALS"></span>Neue Anmeldeinformationen<br/>         | Die Anmeldeinformationen, zu denen der Benutzer beim Ausführen einer Anwendung aufgefordert wird.<br/>       |
| <span id="Saved_credentials"></span><span id="saved_credentials"></span><span id="SAVED_CREDENTIALS"></span>Gespeicherte Anmeldeinformationen<br/>         | Die Anmeldeinformationen, die mit [Anmeldeinformationsverwaltung](credential-manager.md)gespeichert werden.<br/> |



 

Um einen Server in die Kategorie aufzunehmen, die einer bestimmten Gruppenrichtlinieneinstellung zugeordnet ist, fügen Sie den [*Dienstprinzipalnamen (Service Principal Name,*](/windows/desktop/SecGloss/s-gly) SPN) dieses Servers der Liste der Server für diese Gruppenrichtlinieneinstellung hinzu. Der SPN kann ein einzelnes Platzhalterzeichen enthalten.

 

