---
title: Desktop Darstellung
description: Der neue Windows 7-Desktop bringt Ihre Anwendungen in den Leben.
ms.assetid: e706167a-435b-4c32-bb64-87113f368866
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3476f70c46aecceb365e17dba1803b876fd51e8d
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/06/2021
ms.locfileid: "104559890"
---
# <a name="the-desktop-experience"></a>Desktop Darstellung

Der neue Windows 7-Desktop bringt Ihre Anwendungen in den Leben. Anwendungen sind jetzt besser auffindbar, informativ und interaktiv. Moderne und intuitive Benutzeroberflächen können mit Windows 7 einfacher entwickelt werden. Zu den neuen Desktop-und Anwendungsumgebungen zählen die folgenden:

-   Die erweiterte Taskleiste führt interaktive Miniaturansichten ein und ermöglicht Animationen und Interaktionen für minimierte Anwendungen.
-   Mit dem Konzept der Ziele können Benutzer mit einem Klick auf die Dateien, Standorte oder Aufgaben springen, die Sie am häufigsten verwenden.
-   Neue Steuerelemente und APIs für das *Menüband*, basierend auf der Benutzeroberfläche des Office-Benutzeroberflächen, sind für das einfache Hinzufügen von Steuerelementen, Menüs und Galerien im *Menüband* für Ihre Anwendungen verfügbar.
-   Mithilfe eines Animations Frameworks können Sie benutzerdefinierte Animationen verbessern.

Dank der Verbesserungen an der Gadgets-Plattform können Anwendungen Begleit Mini Anwendungen während der Einrichtung oder der erstmaligen Durchführung installieren.

![Screenshot, der den Windows 7-Desktop anzeigt](images/windows7-6.jpg)

Der neue Windows 7-Desktop bringt Ihre Anwendungen in den Lebenszyklus

## <a name="jump-listsgetting-users-into-your-application-quickly"></a>Sprung Listen – schnelles hinzu bringen von Benutzern in Ihre Anwendung

Sprung Listen helfen Benutzern dabei, den gewünschten Einstieg zu beschleunigen. Sprung Listen sind Dateien, URLs, Tasks oder benutzerdefinierte Elemente, die in der Anwendung geöffnet werden. Mit dem Menü neue Sprung Listen im *Startmenü und in der Task* Leiste werden allgemeine Ziele und wichtige Aufgaben mit einem einzigen Klick zur Verfügung gestellt. Das Menü Sprung Listen wird automatisch basierend auf der Häufigkeit und der Verwendung von Elementen aufgefüllt. Entwickler können benutzerdefinierte Sprung Listen basierend auf Ihrer eigenen Semantik bereitstellen. Anwendungen können auch *Aufgaben* definieren, die in Ihren Menüs angezeigt werden sollen – dies sind Aktionen der Anwendung, auf die Benutzer direkt zugreifen möchten, z. b. das Verfassen einer e-Mail. (Weitere Informationen finden Sie unter [Task leisten Erweiterungen](../shell/taskbar-extensions.md) und [ICustomDestinationList-Schnittstelle](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icustomdestinationlist).)

![Sprung Listen](images/windows7-7.jpg)

Sprung Listen unterstützen Benutzer beim Einstieg in den gewünschten Weg.

## <a name="enhanced-taskbar"></a>Erweiterte Taskleiste

Mit der neuen Taskleiste in Windows 7 können Anwendungen Weitere Informationen auf intuitiver Weise für den Benutzer bereitstellen. Beispielsweise können Anwendungen Status anzeigen in Ihren Task leisten Schaltflächen anzeigen, sodass Benutzer den Fortschritt erkennen können, ohne dass das Fenster sichtbar bleiben muss. Dies ist nützlich, um zeitaufwändige Vorgänge wie das Kopieren von Dateien, Downloads, Installationen oder das Brennen von Medien zu überwachen. Symbol Überlagerungen können im unteren rechten Bereich der Task leisten Schaltfläche der Anwendung angezeigt werden und dienen zum Kommunizieren von Status oder Benachrichtigungen (z. b. neue e-Mail). Neue Miniatur Ansichts-APIs ermöglichen es einer Anwendung, untergeordnete Fenster und zugehörige Miniaturbilder für diese Fenster zu definieren. Die Miniaturansicht-Symbolleiste bietet einen Ort zum Steuern allgemeiner Aktionen, ohne dass eine Fenster Wiederherstellung erforderlich ist, wie z. b. wieder *Gabe/Ende* (Weitere Informationen finden Sie unter [Task leisten Erweiterungen](../shell/taskbar-extensions.md) und [Windows 7: Entwickler Ressourcen](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples).)

## <a name="gadgets-platform"></a>Gadgets-Plattform

Gadgets sind ein beliebtes Feature von Windows Vista Desktop, und in Windows 7 ist es für Anwendungen noch einfacher, Gadgets zu installieren. In Windows 7 kann eine Anwendung beim Einrichten der Anwendung oder beim ersten Ausführen Programm gesteuert ein Gadget zum Windows-Desktop hinzufügen. Dies bedeutet, dass die Standardfunktion einer Anwendung ein einfaches Kontrollkästchen enthalten kann, z. b. um eine Begleit Bare Mini Anwendung zu installieren, die auf dem Desktop verfügbar ist, sobald die Anwendung zur Verwendung bereit ist. (Weitere Informationen finden [Sie unter Einführung in die Gadget-Plattform](/previous-versions/windows/desktop/gadgetplatform/introduction-to-the-gadget-platform).)

![Windows-Gadgets](images/windows7-8.jpg)

In Windows 7 ist es für Anwendungen noch einfacher, Gadgets zu installieren.

## <a name="windows-ribbon"></a>Windows-Menüband



Das Windows-Menüband-Steuerelement unterstützt Entwickler dabei, die Benutzerfreundlichkeit zu verbessern, indem die am häufigsten verwendeten Features für Endbenutzer direkt auf die Das Menüband erleichtert Endbenutzern das Auffinden und Verwenden von Anwendungs Features, da weniger Funktionalität ausgeblendet wird, was zu einer höheren Produktivität führt. Das Menüband ist als Intent-basierte Alternative zum Befehls Präsentationsmodell von Menüs, Symbolleisten, Aufgabenbereichen und Dialogfeldern in Windows-Standardanwendungen konzipiert.

Die Menüband-Steuerelemente bestehen aus einer Reihe von Win32APIs, die die Menüleisten Funktion der obersten Ebene überschreiben und stattdessen eine Befehls Oberfläche im Menüband-Stil darstellen. Es ähnelt der Funktionalität und Darstellung der *Multifunktionsleiste* im 2007 Office-System. Die Benutzeroberfläche besteht aus mehreren untergeordneten Steuerelementen, die Folgendes umfassen:

-   Anwendungs Schaltfläche (oder-Perle)
-   Symbolleiste für den schnell Zugriff
-   Menü *Band* Steuerung von Kontext Registerkarten
-   Mini Symbolleisten
-   Stil Galerien

Vorlagen und Markup Erstellung stehen Entwicklern für eine schnelle Entwicklung und Integration von Multifunktionsleisten-Funktionen zur Verfügung. (Siehe [Windows-Menü Band Framework](../windowsribbon/-uiplat-windowsribbon-entry.md) und [Windows-Menü Band Framework: Entwickler Ressourcen](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsRibbon).)

![Menü Band Symbolleiste](images/windows7-9.jpg)

Das Menüband-Steuerelement unterstützt Entwickler dabei, die Benutzerfreundlichkeit zu verbessern, indem die am häufigsten verwendeten

## <a name="animation"></a>Animation

Smooth Animationen sind für viele grafische UI-Anwendungen von grundlegender Bedeutung, und Windows 7 führt ein System eigenes Animations Framework ein, um die Planung und die Ausführung von Animationen zu verwalten. Das Animations Framework stellt eine Bibliothek nützlicher mathematischer Funktionen zum Angeben des Verhaltens im Zeitverlauf bereit und ermöglicht Entwicklern außerdem das Bereitstellen Ihrer eigenen Verhaltens Funktionen. Das Framework unterstützt eine ausgereifte Auflösung von Konflikten, wenn mehrere Animationen versuchen, denselben Wert gleichzeitig zu bearbeiten. Eine Anwendung kann angeben, dass eine Animation abgeschlossen werden muss, bevor ein anderer gestartet werden kann, und die Beendigung innerhalb einer festgelegten Zeit erzwingen kann. Das neue Framework unterstützt Animationen auch bei der Bestimmung geeigneter Dauer. (Siehe [Windows Animation Manager](../uianimation/-main-portal.md).)

 

 