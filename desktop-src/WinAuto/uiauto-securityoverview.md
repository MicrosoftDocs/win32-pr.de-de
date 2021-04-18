---
title: Sicherheitsüberlegungen für Hilfstechnologien
description: Hilfstechnologien sind Anwendungen, die auf dem Windows-Desktop ausgeführt werden und Benutzer der Benutzerfreundlichkeit bei der Interaktion mit dem Betriebssystem und anderen Anwendungen auf dem Computer unterstützen, einschließlich Anwendungen in der neuen Windows-Benutzeroberfläche.
ms.assetid: 0c3689e1-2124-4142-b0bd-233e95ee1285
f1_keywords:
- vs.debug.error.launch_elevation_requirements
keywords:
- UIAccess-Attribut
- UI-Automatisierung, UIAccess-Attribut
- Sicherheit, UIAccess-Attribut
- requestedExecutionLevel-Tag
- Benutzeroberflächenautomatisierungs-Tag (requestedExecutionLevel)
- Benutzeroberflächenautomatisierungs, Sicherheitsüberlegungen
- Benutzeroberflächenautomatisierungs, Manifest-Dateien
- Manifest-Dateien
- Benutzerkontensteuerung
- Sicherheit, Benutzerkontensteuerung
- Sicherheit, Manifest-Dateien
- Sicherheit, requestedExecutionLevel-Tag
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12f2f5cf006c0adaf9b170a4ed11abd9afd52012
ms.sourcegitcommit: 4e4f9e7c90d25af0774deec1d44bd49fa9b6daa9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2020
ms.locfileid: "106340292"
---
# <a name="security-considerations-for-assistive-technologies"></a>Sicherheitsüberlegungen für Hilfstechnologien

Hilfstechnologien sind Anwendungen, die auf dem Windows-Desktop ausgeführt werden und Barrierefreiheits Benutzer bei der Interaktion mit dem Betriebssystem und anderen Anwendungen auf dem Computer unterstützen, einschließlich der Anwendungen in der neuen Windows-Benutzeroberfläche. Hilfstechnologieanwendungen arbeiten durch Abrufen von Informationen vom Betriebssystem und anderen Anwendungen und anschließendes darstellen der Informationen auf eine Weise, auf die der Benutzer zugreifen kann. Eine hilfstechnologieanwendung kann das Betriebssystem und andere Anwendungen auch Programm gesteuert auf der Grundlage der Benutzereingaben steuern.

Die Art von Hilfstechnologieanwendungen erfordert, dass Sie prozessübergreifende Grenzen überschreiten und Zugriff auf Prozesse haben, die mit einer höheren Integritäts Ebene (IL) als sich selbst ausgeführt werden. (Eine hilfstechnologieanwendung wird mit mittlerer Il ausgeführt.) Wenn der Benutzer z. b. versucht, eine Aufgabe auszuführen, für die Administratorrechte erforderlich sind, wird in Windows ein Dialogfeld angezeigt, in dem der Benutzer zum Fortfahren aufgefordert wird. Dieses Dialogfeld wird mit einer höheren Integritäts Stufe ausgeführt, um es vor Prozess übergreifender Kommunikation zu schützen, damit Schadsoftware keine Benutzereingaben simulieren kann. Auf ähnliche Weise wird der Desktop Anmeldebildschirm mit einer höheren Integritäts Stufe ausgeführt, um zu verhindern, dass andere Prozesse darauf zugreifen.

Hilfstechnologieanwendungen benötigen in der Regel Zugriff auf die Benutzeroberflächen Elemente des geschützten Systems oder auf andere Prozesse, die möglicherweise auf einer höheren Berechtigungsstufe ausgeführt werden. Daher müssen Hilfstechnologieanwendungen vom System als vertrauenswürdig eingestuft werden und müssen mit besonderen Berechtigungen ausgeführt werden.

Um Zugriff auf höhere Il-Prozesse zu erhalten, muss eine hilfstechnologieanwendung das UIAccess-Flag im Manifest der Anwendung festlegen und von einem Benutzer mit Administratorrechten gestartet werden.

> [!NOTE]
> Zugriffsberechtigungen werden wie folgt eingeschränkt:
>
> - Eine Anwendung, die keinen UIAccess im Manifest hat, beginnt mit mittlerer Il und kann nicht auf die Benutzeroberfläche mit erhöhten Rechten ("Mittel +" Il-Prozess) zugreifen.
> - Eine Anwendung, die über UIAccess im Manifest verfügt und von einem Benutzer gestartet wird, der nicht der Gruppe "Administratoren" angehört, beginnt mit "Mittel +" und kann nicht auf die Benutzeroberfläche mit erhöhten Rechten zugreifen (es wird keine "hohe" Il ausgeführt, wie z. b. apps, die über einen **Rechtsklick > als Administrator ausgeführt** werden).
> - Eine Anwendung verfügt über Zugriff auf die Benutzeroberfläche und wird von einem Administrator gestartet, der als "High" Il startet und auf die Benutzeroberfläche mit erhöhten Rechten zugreifen kann, da Sie die gleiche Il hat
>
> UIAccess reicht nicht aus, damit ein Prozess über die Il-Grenze nach oben verschoben werden kann.

Zusätzlich zum Zugriff auf höhere Il-Prozesse kann eine hilfstechnologieanwendung mit diesen Berechtigungen jederzeit in der z-Reihenfolge als oberste Anwendung ausgeführt werden. Dies bedeutet, dass eine hilfstechnologieanwendung sichtbar und verfügbar sein kann, wenn der Benutzer Sie benötigt.

> [!Important]
> Keines der zuvor aufgeführten Szenarien bietet Zugriff auf die Benutzeroberfläche, die unter der System-Il ausgeführt wird. Dies ist nur möglich, wenn der Prozess im Desktop der Benutzerkontensteuerung (User Account Control, UAC) unter System (und System IL) gestartet wird. In diesem Fall hat das Festlegen von UIAccess keine Auswirkung.

## <a name="uiaccess-requirements-for-assistive-technology-applications"></a>UIAccess-Anforderungen für Hilfstechnologieanwendungen

Eine hilfstechnologieanwendung ist eine Windows-Desktop Anwendung, die mit anderen Prozessen interagiert, die auf dem Desktop und in der neuen Windows-Benutzeroberfläche ausgeführt werden, um Informationen aus dem System und den Anwendungen zu erhalten. Die hilfstechnologieanwendung kann die Informationen dann für Barrierefreiheits Benutzer bereitstellen.

Eine hilfstechnologieanwendung erhält Zugriff auf andere Prozesse, indem das UIAccess-Flag im Anwendungs Manifest festgelegt wird. Um das UIAccess-Flag zu verwenden, muss eine hilfstechnologieanwendung die folgenden Anforderungen erfüllen.

-   Erfordert, dass Informationen für ein Barrierefreiheits Szenario angezeigt, mit einer anderen Anwendung interagiert oder wieder angezeigt werden, um Informationen für ein Barrierefreiheits Szenario bereitzustellen.
-   Erfordert die Ausführung als oberstes Fenster, um diese Informationen zu erhalten oder anzuzeigen.

Um UIAccess zu verwenden, muss eine hilfstechnologieanwendung folgende Aktionen ausführen:

-   Sie müssen mit einem Zertifikat signiert werden, um mit Anwendungen zu interagieren, die auf einer höheren Berechtigungsstufe ausgeführt werden
-   Wird vom System als vertrauenswürdig eingestuft. Die Anwendung muss an einem sicheren Speicherort installiert sein, der eine Eingabeaufforderung für die Benutzerkontensteuerung (User Account Control, UAC) erfordert. Beispielsweise der Ordner "Programme".
-   Sie sollten mit einer Manifest-Datei erstellt werden, die das UIAccess-Flag enthält.

UIAccess sollte nicht verwendet werden:

-   Anwendungen, bei denen es sich nicht um Hilfstechnologien handelt.
-   Von Hilfstechnologieanwendungen, in denen Informationen oder Benutzeroberflächen angezeigt werden, die für das für die Barrierefreiheit relevante Szenario nicht relevant sind.
-   Von Anwendungen, die nur über anderen Anwendungen in der neuen Windows-Benutzeroberfläche angezeigt werden sollen.
    > [!Note]  
    > Anwendungen, die für die neue Windows-Benutzeroberfläche entwickelt wurden, verfügen nicht über UIAccess als verfügbare Option.

     

## <a name="setting-uiaccess-in-the-application-manifest-file"></a>Festlegen von UIAccess in der Anwendungs Manifest-Datei

Für den Zugriff auf die Benutzeroberfläche des geschützten Systems müssen Anwendungen mit einer Manifestressource erstellt werden, die ein spezielles Attribut in der Manifest-Datei enthält. Dieses **UIAccess** -Attribut ist im **requestedExecutionLevel** -Tag enthalten, wie im folgenden Codebeispiel gezeigt.


```XML
<trustInfo xmlns="urn:schemas-microsoft-com:asm.v3"> 
    <security> 
        <requestedPrivileges> 
        <requestedExecutionLevel 
            level="highestAvailable" 
            uiAccess="true" /> 
        </requestedPrivileges> 
    </security> 
</trustInfo> 
```



Der Wert des **Levels** -Attributs in diesem Code ist nur ein Beispiel.

**UIAccess** ist standardmäßig "false". Wenn das Attribut ausgelassen wird oder kein Manifest vorhanden ist, kann die Anwendung keinen Zugriff auf die geschützte Benutzeroberfläche erhalten.

Weitere Informationen zur Windows-Sicherheit, zum Signieren von Anwendungen und zum Erstellen von Manifesten finden Sie [unter Windows Vista und Windows Server 2008 Developer Story: Anforderungen für die Windows Vista-Anwendungsentwicklung für die Benutzerkontensteuerung (User Account Control, UAC)](/previous-versions/aa905330(v=msdn.10)) auf MSDN.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Grundlagen der Benutzeroberflächenautomatisierung](entry-uiautocore-overview.md)
</dt> </dl>

 

 