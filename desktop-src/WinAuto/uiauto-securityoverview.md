---
title: Sicherheitsüberlegungen für Hilfstechnologien
description: Hilfstechnologien sind Anwendungen, die auf dem Windows Desktop ausgeführt werden und Barrierefreiheitsbenutzern helfen, mit dem Betriebssystem und anderen Anwendungen zu interagieren, die auf dem Computer ausgeführt werden, einschließlich Anwendungen in der neuen Windows Benutzeroberfläche.
ms.assetid: 0c3689e1-2124-4142-b0bd-233e95ee1285
f1_keywords:
- vs.debug.error.launch_elevation_requirements
keywords:
- uiAccess-Attribut
- Benutzeroberflächenautomatisierung,uiAccess-Attribut
- sicherheit,uiAccess-Attribut
- requestedExecutionLevel-Tag
- Benutzeroberflächenautomatisierung,requestedExecutionLevel-Tag
- Benutzeroberflächenautomatisierung,Sicherheitsüberlegungen
- Benutzeroberflächenautomatisierung,Manifestdateien
- Manifestdateien
- Benutzerkontensteuerung
- Sicherheit, Benutzerkontensteuerung
- Sicherheit, Manifestdateien
- security,requestedExecutionLevel-Tag
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f88ba97be98795be3725efaf76cf01297d7a00a2bb0112b0211581b3e0e4035f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118563963"
---
# <a name="security-considerations-for-assistive-technologies"></a>Sicherheitsüberlegungen für Hilfstechnologien

Hilfstechnologien sind Anwendungen, die auf dem Windows Desktop ausgeführt werden und Barrierefreiheitsbenutzern helfen, mit dem Betriebssystem und anderen Anwendungen zu interagieren, die auf dem Computer ausgeführt werden, einschließlich Anwendungen in der neuen Windows Ui. Hilfstechnologieanwendungen arbeiten, indem Sie Informationen aus dem Betriebssystem und anderen Anwendungen abrufen und die Informationen dann so darstellen, dass sie für den Benutzer zugänglich sind. Eine Hilfstechnologieanwendung kann das Betriebssystem und andere Anwendungen auch programmgesteuert basierend auf Eingaben des Benutzers "steuern".

Die Art von Hilfstechnologieanwendungen erfordert, dass sie Prozessgrenzen überschreiten und Zugriff auf Prozesse haben, die auf einer höheren Integritätsebene als sie selbst ausgeführt werden. (Eine Hilfstechnologieanwendung wird bei mittlerer IL ausgeführt.) Wenn der Benutzer beispielsweise versucht, eine Aufgabe auszuführen, die Administratorrechte erfordert, zeigt Windows ein Dialogfeld an, in dem der Benutzer zur Zustimmung aufgefordert wird, den Vorgang fortzusetzen. Dieses Dialogfeld wird auf einer höheren IL ausgeführt, um es vor prozessübergreifender Kommunikation zu schützen, sodass Schadsoftware keine Benutzereingaben simulieren kann. Auf ähnliche Weise wird der Desktopanmeldungsbildschirm auf einer höheren IL ausgeführt, um zu verhindern, dass andere Prozesse darauf zugreifen.

Hilfstechnologieanwendungen benötigen in der Regel Zugriff auf die Benutzeroberflächenelemente des geschützten Systems oder auf andere Prozesse, die möglicherweise auf einer höheren Berechtigungsebene ausgeführt werden. Daher müssen Hilfstechnologieanwendungen vom System als vertrauenswürdig eingestuft werden und mit speziellen Berechtigungen ausgeführt werden.

Um Zugriff auf höhere IL-Prozesse zu erhalten, muss eine Hilfstechnologieanwendung das UIAccess-Flag im Manifest der Anwendung festlegen und von einem Benutzer mit Administratorrechten gestartet werden.

> [!NOTE]
> Zugriffsberechtigungen sind wie folgt eingeschränkt:
>
> - Eine Anwendung, die nicht über UIAccess im Manifest verfügt, beginnt mit medium IL und kann nicht auf die Prozess-UI mit erhöhten Rechten ("Mittel+" IL) zugreifen.
> - Eine Anwendung, die UIAccess im Manifest enthält und von einem Benutzer gestartet wird, der sich nicht in der Gruppe "Administratoren" befindet, als IL "Mittel+" gestartet wird und nicht auf die benutzeroberfläche mit erhöhten Rechten zugreifen kann (nichts wird als "hohe" IL ausgeführt, z. B. Apps, die über einen **Rechtsklick -> Als Administrator ausführen** gestartet werden).
> - Eine Anwendung verfügt über Benutzeroberflächenzugriff und wird von einem Administratorbenutzer als "hohe" IL gestartet und kann auf die Benutzeroberfläche mit erhöhten Rechten zugreifen, da sie über die gleiche IL verfügt.
>
> UIAccess reicht nicht aus, um einen Prozess durch die IL-Grenze nach oben zu verschieben.

Neben dem Zugriff auf höhere IL-Prozesse kann eine Hilfstechnologieanwendung mit diesen Berechtigungen jederzeit als oberste Anwendung in der Z-Reihenfolge ausgeführt werden. Dies bedeutet, dass eine Hilfstechnologieanwendung immer sichtbar und verfügbar sein kann, wenn der Benutzer sie benötigt.

> [!Important]
> Keines der zuvor aufgeführten Szenarien bietet Zugriff auf die Benutzeroberfläche, die unter der System-IL ausgeführt wird. Dies ist nur möglich, wenn der Prozess im Desktop der Benutzerkontensteuerung (User Account Control, UAC) unter SYSTEM (und System-IL) gestartet wird. In diesem Fall hat das Festlegen von UIAccess keine Auswirkungen.

## <a name="uiaccess-requirements-for-assistive-technology-applications"></a>UIAccess-Anforderungen für Hilfstechnologieanwendungen

Eine Hilfstechnologieanwendung ist eine Windows Windows Desktopanwendung, die mit anderen Prozessen interagiert, die auf dem Desktop und in der neuen Windows Ui ausgeführt werden, um Informationen aus dem System und den Anwendungen abzurufen. Die Hilfstechnologieanwendung kann dann die Informationen für Barrierefreiheitsbenutzer bereitstellen.

Eine Hilfstechnologieanwendung erhält Zugriff auf andere Prozesse, indem sie das UIAccess-Flag im Anwendungsmanifest festlegt. Um das UIAccess-Flag zu verwenden, muss eine Hilfstechnologieanwendung die folgenden Anforderungen erfüllen.

-   Es ist erforderlich, Informationen einer anderen Anwendung anzuzeigen, mit ihnen zu interagieren oder diese widerzuspiegeln, um Informationen für ein Barrierefreiheitsszenario bereitzustellen, und/oder
-   Führen Sie als oberstes Fenster aus, um diese Informationen abzurufen oder anzuzeigen.

Um UIAccess verwenden zu können, muss eine Hilfstechnologieanwendung:

-   Sie müssen mit einem Zertifikat signiert werden, um mit Anwendungen zu interagieren, die auf einer höheren Berechtigungsebene ausgeführt werden.
-   Sie müssen vom System als vertrauenswürdig eingestuft werden. Die Anwendung muss an einem sicheren Speicherort installiert werden, der eine Eingabeaufforderung zur Benutzerkontensteuerung (User Account Control, UAC) für den Zugriff erfordert. Beispielsweise der Ordner Programme.
-   Erstellen Sie mit einer Manifestdatei, die das uiAccess-Flag enthält.

UIAccess sollte nicht verwendet werden:

-   Durch Anwendungen, die keine Hilfstechnologien sind.
-   Durch Hilfstechnologieanwendungen, die Informationen oder eine Benutzeroberfläche anzeigen, die für das Barrierefreiheitsszenario, auf das sie abzielen, nicht relevant sind.
-   Von Anwendungen, die nur über anderen Anwendungen in der neuen Windows Ui angezeigt werden sollen.
    > [!Note]  
    > Für Anwendungen, die für die neue Windows Ui entwickelt wurden, ist UIAccess nicht verfügbar.

     

## <a name="setting-uiaccess-in-the-application-manifest-file"></a>Festlegen von UIAccess in der Anwendungsmanifestdatei

Um Zugriff auf die benutzeroberfläche des geschützten Systems zu erhalten, müssen Anwendungen mit einer Manifestdatei erstellt werden, die ein spezielles Attribut in der Manifestdatei enthält. Dieses **uiAccess-Attribut** ist im **requestedExecutionLevel-Tag** enthalten, wie im folgenden Codebeispiel gezeigt.


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



Der Wert  des Ebenenattributs in diesem Code ist nur ein Beispiel.

**UIAccess** ist standardmäßig "false". Wenn das Attribut ausgelassen wird oder kein Manifest vorhanden ist, kann die Anwendung keinen Zugriff auf die geschützte Benutzeroberfläche erhalten.

Weitere Informationen zur sicherheit Windows, zum Signieren von Anwendungen und zum Erstellen von Manifesten finden Sie unter [The Windows Vista and Windows Server 2008 Developer Story: Windows Vista Application Development Requirements for User Account Control (UAC)](/previous-versions/aa905330(v=msdn.10)) auf MSDN.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Grundlagen der Benutzeroberflächenautomatisierung](entry-uiautocore-overview.md)
</dt> </dl>

 

 