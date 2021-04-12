---
description: Befolgen Sie diese Richtlinien, wenn Sie eine Windows Installer benutzerdefinierte Aktion erstellen, um die Sicherheit einer Software Installation zu gewährleisten.
ms.assetid: f7081b0c-bfa2-47a1-840b-28881ad97071
title: Richtlinien zum Sichern von benutzerdefinierten Aktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 119c045833b165222756702244cf65bb2225a8f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216749"
---
# <a name="guidelines-for-securing-custom-actions"></a>Richtlinien zum Sichern von benutzerdefinierten Aktionen

Beachten Sie beim Erstellen eines Windows Installer Pakets mit benutzerdefinierten Aktionen die folgenden Richtlinien, um während der Installation eine sichere Umgebung zu gewährleisten:

-   Sichern Sie alle zusätzlichen Dateien, die von der benutzerdefinierten Aktion geschrieben wurden.
-   Überprüfen Sie die Puffer Längen und die Gültigkeit aller von der benutzerdefinierten Aktion gelesenen Daten. Dies schließt Eigenschaften ein, die möglicherweise Daten für Ihre benutzerdefinierte Aktion bereitstellen, insbesondere solche, die von einem Benutzer bereitgestellte öffentliche Eigenschaften verwenden.
-   Verlassen Sie sich nicht auf externe DLLs, die vom System auf allen Plattformen, auf denen das Installationspaket ausgeführt werden soll, nicht als vertrauenswürdig eingestuft werden.
-   Überlegen Sie sorgfältig, ob benutzerdefinierte Aktionen verwendet werden sollen, die [*erhöhte*](e-gly.md) Rechte oder Identitätswechsel verwenden. Benutzerdefinierte Aktionen, wie z. b. "URL nach der Installation öffnen", "die Software nach Abschluss der Installation starten" oder "die Installation nach Abschluss der Installation starten" erfordert normalerweise keine erhöhten Berechtigungen. Wenn Ihre benutzerdefinierte Aktion mit *erhöhten* Rechten ausgeführt werden muss, müssen Sie sicherstellen, dass der Code der benutzerdefinierten Aktion vor Pufferüberläufen und unbeabsichtigtem Laden von unsicherem Code schützt. Beachten Sie, dass das Installationsprogramm während der Ausführungsphase der Installation Informationen an einen Prozess mit *erhöhten* rechten übergibt und das Skript ausführt. Alle benutzerdefinierten Aktionen, die während der Ausführungsphase ausgeführt werden, werden möglicherweise mit *erhöhten* Rechten ausgeführt.
-   Sammeln Sie alle Informationen, die vom Benutzer während der UI-Sequenz bereitgestellt werden. Fordern Sie den Benutzer nicht auf, Informationen einzugeben, die nicht mit einer öffentlichen Eigenschaft festgelegt werden können.
-   Wenn die benutzerdefinierte Skript Aktion Eigenschaften erweitert, ergreifen Sie Vorsichtsmaßnahmen, dass die benutzerdefinierte Aktion vor der Möglichkeit der Skript Injektion geschützt ist. Das Skript kann als Klartext protokolliert werden.

Siehe auch [Sicherheit für benutzerdefinierte Aktionen](custom-action-security.md).

 

 



