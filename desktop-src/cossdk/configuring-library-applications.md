---
description: Konfigurieren von Bibliotheksanwendungen
ms.assetid: db375e0f-74ca-44df-918a-b0e48742a594
title: Konfigurieren von Bibliotheksanwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e51e00626d42044797881ccb86553ddfda38a089
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041383"
---
# <a name="configuring-library-applications"></a>Konfigurieren von Bibliotheksanwendungen

Da com+-Bibliotheksanwendungen im Client Prozess ausgeführt werden, unterscheiden sich die konfigurierbaren Elemente für Bibliotheksanwendungen erheblich von der für Server Anwendungen. Es ist nicht möglich, einen Aspekt der Anwendung zu konfigurieren, der vom Hostingprozess bestimmt wird.

Auf Anwendungsebene sind mehrere Einstellungen für Bibliotheksanwendungen entweder eingeschränkt oder nicht verfügbar. Diese Einschränkungen werden in der folgenden Tabelle beschrieben:



| Attribut                                       | BESCHREIBUNG                                                                                                                                                                                                                                   |
|-------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Sicherheitsstufe<br/>                       | Sie müssen Zugriffs Überprüfungen auf Komponentenebene auswählen. Die Bibliotheks Anwendung kann keine Zugriffs Überprüfungen auf Prozessebene beeinflussen. Weitere Informationen finden Sie unter [Festlegen einer Sicherheitsstufe für Zugriffs Überprüfungen](setting-a-security-level-for-access-checks.md).<br/>             |
| Aktivieren oder Deaktivieren der Authentifizierung<br/> | Sie können angeben, ob die Bibliotheks Anwendung an der vom Host Prozess ausgeführten Authentifizierung beteiligt sein soll. Siehe [Aktivieren der Authentifizierung für eine Bibliotheks Anwendung](enabling-authentication-for-a-library-application.md).<br/> |
| Ebene des Identitätswechsels<br/>                  | Vorübergehend. Die Einstellung des Host Prozesses wird verwendet. <br/>                                                                                                                                                                             |
| Sicherheitsidentität<br/>                    | Vorübergehend. Die Anwendung wird mit der Identität des Host Prozesses ausgeführt.<br/>                                                                                                                                                          |
| Server Prozess wird heruntergefahren<br/>              | Vorübergehend.<br/>                                                                                                                                                                                                                       |
| Unterstützung für 3 GB aktivieren<br/>                  | Vorübergehend.<br/>                                                                                                                                                                                                                       |
| Im Debugger starten<br/>                   | Vorübergehend.<br/>                                                                                                                                                                                                                       |
| Aktivieren von CRM<br/>                           | Vorübergehend.<br/>                                                                                                                                                                                                                       |
| Queuing<br/>                              | Vorübergehend.<br/>                                                                                                                                                                                                                       |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übersicht über die COM+-Anwendung](com--application-overview.md)
</dt> </dl>

 

 




