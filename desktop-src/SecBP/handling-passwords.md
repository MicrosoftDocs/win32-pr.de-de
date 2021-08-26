---
description: Derzeit sind Benutzernamen und Kennwortanmeldeinformationen die gängigsten Anmeldeinformationen, die für die Authentifizierung verwendet werden.
ms.assetid: 1d810f71-9bf5-4c5c-a573-c35081f604cf
title: Behandeln von Kennwörtern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99aaf133d23390a6f4efce97940c5116fddf91b45776dfd6847b2712b15b74ef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120035470"
---
# <a name="handling-passwords"></a>Behandeln von Kennwörtern

Derzeit sind Benutzernamen und Kennwortanmeldeinformationen die gängigsten Anmeldeinformationen, die für die Authentifizierung verwendet werden. Auch wenn andere Arten von Anmeldeinformationen, z. B. Zertifikate und biometrische Daten, ihren Weg in die Welt der Systeme und Netzwerke finden, werden sie häufig durch Kennwörter gesichert. Und selbst wenn Zertifikate verwendet werden, müssen ihre Verschlüsselungsschlüssel geschützt werden. Daher werden Benutzernamen und Kennwörter auch in naher Zukunft weiterhin für Anmeldeinformationen verwendet.

Da Kennwörter und Verschlüsselungsschlüssel eine Weile liegen werden, ist es wichtig, dass Softwaresysteme sie sicher verwenden. Wenn ein Netzwerk- oder Computersystem sicher bleiben soll, müssen Kennwörter vor Eindringlingen geschützt werden. Dies mag zunächst trivial erscheinen. System nach System und Netzwerk, nachdem das Netzwerk kompromittiert wurde, da ein Angreifer die Kennwörter der Benutzer ermitteln konnte. Die Probleme reichen von Benutzern, die ihre Kennwörter für jemanden freigeben, bis hin zu Software, die von einem Angreifer durchdrungen werden kann.

Es ist unmöglich, geheime Informationen in Software vollständig sicher zu speichern. Da das Speichern von Kennwörtern und Verschlüsselungsschlüsseln in einem Softwaresystem nie vollständig sicher sein kann, wird empfohlen, sie nicht in einem Softwaresystem zu speichern.

Wenn Kennwörter jedoch in einem Softwaresystem gespeichert werden müssen , was in der Regel der Fall ist, gibt es Vorsichtsmaßnahmen, die ergriffen werden können. Die wichtigste Vorsichtsmaßnahme besteht darin, es einem Eindringling so schwer wie möglich zu machen, ein Kennwort zu ermitteln. Genau wie beim Sperren Ihrer Haustüren ist es fast unmöglich, dies zu verhindern, wenn jemand dazu bestimmt ist, einzubrechen. Aber hoffentlich haben Sie den Grad der Schwierigkeiten so stark erhöht, dass der eindrückliche Eindringling lieber eine einfachere Beute finden würde.

Es gibt viele Möglichkeiten, die Ermittlung von Kennwörtern durch einen Angreifer zu erschweren. Das Ausmaß der tatsächlichen Möglichkeiten ist jedoch in der Regel ein Kompromiss mit dem, mit dem die Benutzer des Netzwerks oder Systems leben möchten. Nehmen wir beispielsweise den Fall, in dem "einmaliges Anmelden" nicht verwendet wird und der Benutzer bei jedem Start einer Anwendung zur Eingabe eines Kennworts aufgefordert wird. In den meisten Fällen würde dies zu einer erheblichen Belastung für die Benutzer führen, und sie würden sich wahrscheinlich darüber beschweren. Nicht nur das, sondern das Fehlen eines einmaligen Anmeldens ist ineffizient und würde die Produktivität der Benutzer beeinträchtigen. Praktisch genommen wird also ein Kennwort in der Regel nur zum Zeitpunkt der Anmeldung von einem Benutzer erfasst.

Da Kennwörter in der Regel auf dem Softwaresystem gespeichert werden müssen, ist es wichtig sicherzustellen, dass Kennwörter so sicher wie möglich und die Benutzerfreundlichkeit beibehalten werden. Weitere Informationen finden Sie in den folgenden Themen:

-   [Bewertung der Kennwortbedrohung](password-threat-assessment.md)
-   [Techniken zur Bedrohungsminderung](threat-mitigation-techniques.md)

> [!Note]  
> Wenn Sie die Verwendung von Kennwörtern in Anwendungen abgeschlossen haben, löschen Sie die vertraulichen Informationen aus dem Arbeitsspeicher, indem Sie die [**SecureZeroMemory-Funktion**](/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) aufrufen.

 

 

 
