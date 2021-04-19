---
description: Zum Delegieren von Anmelde Informationen für die Credential Security Support Provider Protocol (aufzurufende Anmelde Informationen) müssen Sie angeben, an welche Server delegiert werden kann.
ms.assetid: 15ed9a62-2eee-4f29-92c5-ccf2754cdf13
title: Einstellungen für den Gruppenrichtlinie ""
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a159b7a162df3eda692462a3d3972159e61797e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362302"
---
# <a name="credssp-group-policy-settings"></a>Einstellungen für den Gruppenrichtlinie ""

Zum Delegieren von Anmelde Informationen für die [Credential Security Support Provider Protocol (](credential-security-support-provider.md) aufzurufende Anmelde Informationen) müssen Sie angeben, an welche Server delegiert werden kann. Um diese Server anzugeben, ändern Sie die Einstellungen im MMC-Snap-in (Microsoft Management Console) des Gruppenrichtlinie-Editors (gpe). Die gpe-Einstellungen, die die Delegierung steuern, sind unter **Computer Konfiguration \| Administrative Vorlagen \| \| Delegierung von System Anmelde** Informationen

> [!Caution]  
> Dies ist keine eingeschränkte Delegierung. "Kredssp" übergibt die vollständigen Anmelde Informationen des Benutzers ohne Einschränkung an den Server.

 

Die Delegierung der folgenden Anmelde Informationstypen wird von Gruppenrichtlinien Einstellungen gesteuert.



| Typ der Anmelde Informationen                                                                                                                                 | BESCHREIBUNG                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="Default_credentials"></span><span id="default_credentials"></span><span id="DEFAULT_CREDENTIALS"></span>Standard Anmelde Informationen<br/> | Die Anmelde Informationen, die bei der ersten Anmeldung des Benutzers bei Windows abgerufen werden.<br/>                   |
| <span id="Fresh_credentials"></span><span id="fresh_credentials"></span><span id="FRESH_CREDENTIALS"></span>Neue Anmelde Informationen<br/>         | Die Anmelde Informationen, nach denen der Benutzer beim Ausführen einer Anwendung gefragt wird.<br/>       |
| <span id="Saved_credentials"></span><span id="saved_credentials"></span><span id="SAVED_CREDENTIALS"></span>Gespeicherte Anmelde Informationen<br/>         | Die Anmelde Informationen, die mit [Credential Manager](credential-manager.md)gespeichert werden.<br/> |



 

Fügen Sie den [*Dienst Prinzipal Namen*](/windows/desktop/SecGloss/s-gly) (SPN) dieses Servers der Liste der Server für diese Gruppenrichtlinien Einstellung hinzu, um einen Server in die Kategorie aufzunehmen, die einer bestimmten Gruppenrichtlinien Einstellung zugeordnet ist. Der SPN kann ein einzelnes Platzhalter Zeichen enthalten.

 

