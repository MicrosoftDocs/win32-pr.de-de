---
description: Derzeit sind die Anmelde Informationen für Benutzername und Kennwort die häufigsten Anmelde Informationen, die für die Authentifizierung verwendet werden.
ms.assetid: 1d810f71-9bf5-4c5c-a573-c35081f604cf
title: Behandeln von Kenn Wörtern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3d3a5ab2bc034500159adb25dab02b47eb43bcd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353932"
---
# <a name="handling-passwords"></a>Behandeln von Kenn Wörtern

Derzeit sind die Anmelde Informationen für Benutzername und Kennwort die häufigsten Anmelde Informationen, die für die Authentifizierung verwendet werden. Obwohl andere Arten von Anmelde Informationen, wie z. b. Zertifikate und Biometrie, mit der Welt der Systeme und Netzwerke beginnen, werden Sie häufig durch Kenn Wörter gesichert. Und auch wenn Zertifikate verwendet werden, müssen ihre Verschlüsselungsschlüssel geschützt werden. Benutzernamen und Kenn Wörter werden also weiterhin in absehbarer Zeit für Anmelde Informationen verwendet.

Da Kenn Wörter und Verschlüsselungsschlüssel ungefähr eine Weile sein werden, ist es wichtig, dass Sie von Softwaresystemen auf sichere Weise verwendet werden. Wenn ein Netzwerk-oder Computersystem sicher bleibt, müssen die Kenn Wörter vor eindringenden Angreifern geschützt werden. Dies könnte zunächst trivial erscheinen. Das System nach dem System und Netzwerk nach dem Netzwerk ist jedoch gefährdet, da ein Angreifer die Kenn Wörter von Benutzern auslassen konnte. Die Probleme reichen von Benutzern, die ihre Kenn Wörter für Personen freigeben, bis hin zu Software, die von einem Angreifer eindringen kann.

Es ist nicht möglich, geheime Informationen vollständig sicher in Software zu speichern. Und da das Speichern von Kenn Wörtern und Verschlüsselungsschlüsseln in einem Softwaresystem nie vollständig sicher sein kann, wird empfohlen, dass Sie nicht in einem Softwaresystem gespeichert werden.

Wenn Kenn Wörter jedoch in einem Softwaresystem gespeichert werden müssen, was in der Regel der Fall ist, können Vorkehrungen getroffen werden. Die primäre Vorsichtsmaßnahme besteht darin, das Kennwort für einen Eindringling so schwierig wie möglich zu machen. Wenn ein Benutzer so festgelegt ist, dass er in die Haus Türen sperrt, ist es beinahe unmöglich, dies zu verhindern. Aber hoffentlich haben Sie den Grad der Schwierigkeit genug hervorgehoben, dass der wäre-wäre-Eindringling eher leichter zu finden.

Es gibt viele Möglichkeiten, die Arbeit eines Angreifers bei der Ermittlung von Kenn Wörtern zu erschweren. Allerdings ist es in der Regel ein Kompromiss, mit dem die Benutzer des Netzwerks oder Systems in der Praxis bereit sind. Nehmen Sie z. b. an, dass einmaliges Anmelden nicht verwendet wird und der Benutzer jedes Mal, wenn eine Anwendung gestartet wird, zur Eingabe eines Kennworts aufgefordert wird. In den meisten Fällen würde dies eine beträchtliche Belastung für die Benutzer verursachen, und Sie würden sich wahrscheinlich beschweren. Nicht nur, aber das einmalige Anmelden ist ineffizient und würde die Produktivität der Benutzer beeinträchtigen. In der Regel wird ein Kennwort in der Regel nicht von einem Benutzer erfasst, außer zum Zeitpunkt der Anmeldung.

Da Kenn Wörter in der Regel im Softwaresystem gespeichert werden müssen, ist es wichtig, sicherzustellen, dass Kenn Wörter so sicher wie möglich aufbewahrt werden und dass Benutzer die benutzerfreundliche Verwendung erhalten. Weitere Informationen finden Sie unter den folgenden Themen:

-   [Kenn Wort Bedrohungsbewertung](password-threat-assessment.md)
-   [Techniken zur Bedrohungsminderung](threat-mitigation-techniques.md)

> [!Note]  
> Wenn Sie die Verwendung von Kenn Wörtern in Anwendungen abgeschlossen haben, löschen Sie die vertraulichen Informationen aus dem Arbeitsspeicher, indem Sie die [**securezeromemory**](/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) -Funktion aufrufen.

 

 

 
