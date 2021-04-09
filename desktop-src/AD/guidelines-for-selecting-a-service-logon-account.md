---
title: Richtlinien für das Auswählen eines Dienst Anmelde Kontos
description: Ein Win32-basierter Dienst kann im Sicherheitskontext eines lokalen Benutzerkontos, eines Domänen Benutzerkontos oder des Kontos "LocalSystem" ausgeführt werden.
ms.assetid: aa2b93c7-335f-4e03-9198-fe2b396e296e
ms.tgt_platform: multiple
keywords:
- Richtlinien für das Auswählen eines Dienst Anmelde Konto-AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5bb8f5b4fe6a57863c09c9563454fc3ec09e75c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036358"
---
# <a name="guidelines-for-selecting-a-service-logon-account"></a>Richtlinien für das Auswählen eines Dienst Anmelde Kontos

Ein Win32-basierter Dienst kann im Sicherheitskontext eines lokalen Benutzerkontos, eines Domänen Benutzerkontos oder des Kontos "LocalSystem" ausgeführt werden. Um zu entscheiden, welches Konto verwendet werden soll, sollte ein Administrator den Dienst mit dem minimalen Satz an Berechtigungen installieren, der zum Durchführen der Dienst Vorgänge erforderlich ist. In einem typischen, Verzeichnis aktivierten Dienst bedeutet dies, dass das Dienst Installationsprogramm ein Domänen Benutzerkonto für den Dienst erstellen und diesem Konto die für den Dienst zur Laufzeit erforderlichen Zugriffsrechte und Berechtigungen erteilen soll. Ein Dienst sollte nur unter dem Konto "LocalSystem" ausgeführt werden, wenn der Dienst Administratorrechte erfordert oder als Teil des Betriebssystems auf dem lokalen Computer fungieren muss.

Beachten Sie, dass der Dienst Installer standardmäßig den Dienst so einrichten muss, dass er unter einem Domänen Benutzerkonto ausgeführt wird. Um den Dienst unter dem Konto "LocalSystem" auszuführen, sollte das Dienst Installationsprogramm den Administrator über die entsprechende Berechtigung Abfragen.

Weitere Informationen zu Beschreibungen, Vorteilen und Nachteilen der einzelnen Kontotypen finden Sie unter:

-   [Lokale Benutzerkonten](local-user-accounts.md).
-   [Domänen Benutzerkonten](domain-user-accounts.md).
-   [Das LocalSystem-Konto](the-localsystem-account.md).

 

 




