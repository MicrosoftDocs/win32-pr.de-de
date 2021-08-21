---
description: Konfigurieren von Bibliotheksanwendungen
ms.assetid: db375e0f-74ca-44df-918a-b0e48742a594
title: Konfigurieren von Bibliotheksanwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b8ea0018d74070828384db25d76c73e7b5b3dba8a7dfc7d091c94e38aa0c3bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047498"
---
# <a name="configuring-library-applications"></a>Konfigurieren von Bibliotheksanwendungen

Da COM+-Bibliotheksanwendungen im Clientprozess ausgeführt werden, unterscheiden sich die konfigurierbaren Elemente für Bibliotheksanwendungen erheblich von denen für Serveranwendungen. Sie können keinen Aspekt der Anwendung konfigurieren, der durch den Hostingprozess bestimmt wird.

Auf Anwendungsebene sind mehrere Einstellungen für Bibliotheksanwendungen entweder eingeschränkt oder nicht verfügbar. Diese Einschränkungen werden in der folgenden Tabelle beschrieben:



| attribute                                       | Beschreibung                                                                                                                                                                                                                                   |
|-------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Sicherheitsstufe<br/>                       | Sie müssen Zugriffsüberprüfungen auf Komponentenebene auswählen. Die Bibliotheksanwendung kann keine Zugriffsüberprüfungen auf Prozessebene beeinflussen. Weitere Informationen finden Sie unter [Festlegen einer Sicherheitsstufe für Zugriffsüberprüfungen.](setting-a-security-level-for-access-checks.md)<br/>             |
| Aktivieren oder Deaktivieren der Authentifizierung<br/> | Sie können angeben, ob die Bibliotheksanwendung an der vom Hostprozess durchgeführten Authentifizierung teilnimmt. Weitere Informationen finden Sie unter [Aktivieren der Authentifizierung für eine Bibliotheksanwendung.](enabling-authentication-for-a-library-application.md)<br/> |
| Ebene des Identitätswechsels<br/>                  | Verfügbar. Die Einstellung des Hostprozesses wird verwendet. <br/>                                                                                                                                                                             |
| Sicherheitsidentität<br/>                    | Verfügbar. Die Anwendung wird unter der Identität des Hostprozesses ausgeführt.<br/>                                                                                                                                                          |
| Herunterfahren des Serverprozesses<br/>              | Verfügbar.<br/>                                                                                                                                                                                                                       |
| Aktivieren der 3-GB-Unterstützung<br/>                  | Verfügbar.<br/>                                                                                                                                                                                                                       |
| Starten im Debugger<br/>                   | Verfügbar.<br/>                                                                                                                                                                                                                       |
| Aktivieren von CRM<br/>                           | Verfügbar.<br/>                                                                                                                                                                                                                       |
| Queuing<br/>                              | Verfügbar.<br/>                                                                                                                                                                                                                       |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übersicht über COM+-Anwendungen](com--application-overview.md)
</dt> </dl>

 

 




