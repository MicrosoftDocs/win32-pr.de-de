---
description: Wenn ein SSP/AP-Sicherheitspaket als Authentifizierungspaket funktioniert, wird es in den Prozessbereich der lokalen Sicherheitsstelle (LSA) geladen und als im LSA-Modus bezeichnet.
ms.assetid: ff4e61be-dbaa-4cfa-8c72-43e99fe1c3cb
title: LSA-Modus im Vergleich zum Benutzermodus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4aa965cd66f43548243c1e62329e6d9d337a2a0123344a8cb9f10915846a765f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118922079"
---
# <a name="lsa-mode-vs-user-mode"></a>LSA-Modus im Vergleich zum Benutzermodus

Wenn ein SSP/AP-Sicherheitspaket als Authentifizierungspaket [*funktioniert,*](../secgloss/a-gly.md)wird es in den Prozessbereich der lokalen Sicherheitsstelle (LSA) geladen und als im LSA-Modus bezeichnet. [](../secgloss/s-gly.md) [](../secgloss/l-gly.md) Anmeldeanwendungen greifen mithilfe der [LSA-Anmeldefunktionen auf die Authentifizierungspaketfunktionalität zu.](authentication-functions.md) Entwickler können LSA-Unterstützungsfunktionen verwenden, die nur für Sicherheitspakete im LSA-Modus verfügbar sind, um komplexere Authentifizierungspakete als bisher zu implementieren.

Wenn ein [*Sicherheitspaket*](../secgloss/s-gly.md) Sicherheitsdienste für eine Client-/Serveranwendung bietet, wird es in die Client- und Serverprozesse geladen und als Benutzermodus bezeichnet. Client-/Serveranwendungen greifen über die Microsoft [*Security Support Provider Interface*](../secgloss/s-gly.md) (SSPI) auf die Sicherheitssupportdienste des Sicherheitspakets zu.

Die LSA-Unterstützung für SSP/APs umfasst Funktionen, die die Instanzen des LSA-Modus und des Benutzermodus eines Sicherheitspakets für die Kommunikation verwenden können. Darüber hinaus kann die Benutzermodusinstanz eines Sicherheitspakets ausgewählte Informationsanforderungen an die Instanz des Pakets im LSA-Modus delegieren.

Weitere Informationen dazu, wie Sicherheitspakete für jeden Modus initialisiert werden, finden Sie unter Initialisierung im [LSA-Modus](lsa-mode-initialization.md) und [Initialisierung im Benutzermodus.](user-mode-initialization.md)

 

 
