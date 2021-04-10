---
description: Wenn ein SSP/AP-Sicherheitspaket als Authentifizierungs Paket fungiert, wird es in den Prozessbereich der lokalen Sicherheits Autorität (Local Security Authority, LSA) geladen und befindet sich im LSA-Modus.
ms.assetid: ff4e61be-dbaa-4cfa-8c72-43e99fe1c3cb
title: LSA-Modus im Vergleich zum Benutzermodus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd8fadde30fe60c38a2b8ccb1f158d94ec7d5603
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050284"
---
# <a name="lsa-mode-vs-user-mode"></a>LSA-Modus im Vergleich zum Benutzermodus

Wenn ein SSP/AP- [*Sicherheitspaket*](../secgloss/s-gly.md) als [*Authentifizierungs Paket*](../secgloss/a-gly.md)fungiert, wird es in den Prozessbereich der [*lokalen Sicherheits Autorität (Local Security Authority*](../secgloss/l-gly.md) , LSA) geladen und befindet sich im LSA-Modus. Anmelde Anwendungen greifen mithilfe der [LSA-Anmelde Funktionen](authentication-functions.md)auf die Funktionen des Authentifizierungs Pakets zu. Entwickler können LSA-Unterstützungsfunktionen verwenden, die nur im LSA-Modus verfügbar sind, um komplexere Authentifizierungs Pakete zu implementieren, als zuvor unterstützt wurden.

Wenn ein [*Sicherheitspaket*](../secgloss/s-gly.md) Sicherheitsdienste für eine Client/Server-Anwendung bereitstellt, wird es in die Client-und Server Prozesse geladen und als Benutzermodus bezeichnet. Client-/Serveranwendungen greifen mithilfe der Microsoft [*Security Support Provider Interface*](../secgloss/s-gly.md) (SSPI) auf die Sicherheits Unterstützungsdienste des Sicherheitspakets zu.

LSA-Unterstützung für SSP/APS umfasst Funktionen, die der LSA-Modus und die benutzermodusinstanzen eines Sicherheitspakets für die Kommunikation verwenden können. Darüber hinaus kann die benutzermodusinstanz eines Sicherheitspakets ausgewählte Anforderungen nach Informationen an die Instanz des Pakets im LSA-Modus delegieren.

Ausführliche Informationen dazu, wie Sicherheitspakete für jeden Modus initialisiert werden, finden Sie unter [Initialisierung im LSA-Modus](lsa-mode-initialization.md) und [Initialisierung im Benutzermodus](user-mode-initialization.md).

 

 
