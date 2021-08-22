---
description: Um die Sicherheit einer Softwareinstallation zu gewährleisten, befolgen Sie diese Richtlinien, wenn Sie eine benutzerdefinierte Aktion Windows Installer erstellen.
ms.assetid: f7081b0c-bfa2-47a1-840b-28881ad97071
title: Richtlinien zum Schützen benutzerdefinierter Aktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00b5ea12bd8d38025587cb09fd7a17d3e87739acedf31d85f72ff4b1b76b0432
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119649290"
---
# <a name="guidelines-for-securing-custom-actions"></a>Richtlinien zum Schützen benutzerdefinierter Aktionen

Die Einhaltung der folgenden Richtlinien beim Erstellen eines Pakets Windows Installer mit benutzerdefinierten Aktionen trägt dazu bei, eine sichere Umgebung während der Installation zu gewährleisten:

-   Sichern Sie alle zusätzlichen Dateien, die von Ihrer benutzerdefinierten Aktion geschrieben wurden.
-   Überprüfen Sie die Pufferlänge und -gültigkeit aller Daten, die von Ihrer benutzerdefinierten Aktion gelesen werden. Dies schließt Eigenschaften ein, die Möglicherweise Daten für Ihre benutzerdefinierte Aktion liefern, insbesondere solche, die öffentliche Eigenschaften verwenden, die von einem Benutzer bereitgestellt werden.
-   Verlassen Sie sich nicht auf externe DLLs, die vom System nicht auf allen Plattformen als vertrauenswürdig eingestuft werden, auf denen Ihr Installationspaket ausgeführt werden soll.
-   Überlegen Sie sorgfältig, ob Sie benutzerdefinierte Aktionen verwenden, [*die*](e-gly.md) erhöhte Rechte oder Identitätswechsel verwenden. Benutzerdefinierte Aktionen wie "Öffnen einer URL nach Abschluss der Installation", "Software nach Abschluss der Installation starten" oder "ReadMe nach Abschluss der Installation starten" erfordern in der Regel keine erhöhten Berechtigungen, um zu funktionieren. Wenn Ihre benutzerdefinierte  Aktion mit erhöhten Rechten ausgeführt werden muss, stellen Sie sicher, dass der code der benutzerdefinierten Aktion vor Pufferüberläufen und unbeabsichtigten Ladevorgang von unsicheren Code schutzt. Beachten Sie, dass das Installationsprogramm während der Ausführungsphase  der Installation Informationen an einen Prozess mit erhöhten Rechten übergibt und das Skript ausgibt. Alle benutzerdefinierten Aktionen, die während der Ausführungsphase ausgeführt werden, können mit erhöhten *Rechten* ausgeführt werden.
-   Sammeln Sie alle Informationen, die vom Benutzer während der Benutzeroberflächensequenz bereitgestellt werden. Fragen Sie den Benutzer nicht nach Informationen, die nicht mithilfe einer öffentlichen Eigenschaft festgelegt werden können.
-   Wenn ihre benutzerdefinierte Skriptaktion Eigenschaften erweitert, treffen Sie Vorsichtsmaßnahmen, um die benutzerdefinierte Aktion vor der Möglichkeit der Skriptinjektion zu sichern. Das Skript kann als Klartext protokolliert werden.

Siehe auch [Benutzerdefinierte Aktionssicherheit](custom-action-security.md).

 

 



