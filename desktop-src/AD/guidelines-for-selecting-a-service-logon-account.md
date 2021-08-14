---
title: Richtlinien für die Auswahl eines Dienstanmeldungskontos
description: Ein Win32-basierter Dienst kann im Sicherheitskontext eines lokalen Benutzerkontos, eines Domänenbenutzerkontos oder des LocalSystem-Kontos ausgeführt werden.
ms.assetid: aa2b93c7-335f-4e03-9198-fe2b396e296e
ms.tgt_platform: multiple
keywords:
- Richtlinien für die Auswahl eines Dienstanmeldungskontos AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a976927130a3585be2e6130dbb71b37fa0c69660b6ae953e28909fad3db570f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118188674"
---
# <a name="guidelines-for-selecting-a-service-logon-account"></a>Richtlinien für die Auswahl eines Dienstanmeldungskontos

Ein Win32-basierter Dienst kann im Sicherheitskontext eines lokalen Benutzerkontos, eines Domänenbenutzerkontos oder des LocalSystem-Kontos ausgeführt werden. Um zu entscheiden, welches Konto verwendet werden soll, sollte ein Administrator den Dienst mit dem mindesten Berechtigungssatz installieren, der zum Ausführen der Dienstvorgänge erforderlich ist. In einem typischen verzeichnisfähigen Dienst bedeutet dies, dass das Dienstinstallationsprogramm ein Domänenbenutzerkonto für den Dienst erstellen und diesem Konto die spezifischen Zugriffsrechte und Berechtigungen erteilen sollte, die der Dienst zur Laufzeit benötigt. Ein Dienst sollte nur unter dem LocalSystem-Konto ausgeführt werden, wenn der Dienst Administratorrechte erfordert oder als Teil des Betriebssystems auf dem lokalen Computer fungieren muss.

Beachten Sie, dass das Dienstinstallationsprogramm den Dienst standardmäßig für die Ausführung unter einem Domänenbenutzerkonto einrichten sollte. Um den Dienst unter dem LocalSystem-Konto auszuführen, sollte das Dienstinstallationsprogramm den Administrator um die Berechtigung dazu bitten.

Weitere Informationen zu Beschreibungen, Vor- und Nachteilen der einzelnen Kontotypen finden Sie unter:

-   [Lokale Benutzerkonten](local-user-accounts.md).
-   [Domänenbenutzerkonten](domain-user-accounts.md).
-   [Das LocalSystem-Konto](the-localsystem-account.md).

 

 




