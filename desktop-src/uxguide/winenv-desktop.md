---
title: Desktop
description: Der Desktop ist der Arbeitsbereich des Benutzers für Ihre Programme. Es ist keine Möglichkeit, das Bewusstsein für Ihr Programm oder seine Marke zu fördern. Nicht missbrauchen.
ms.assetid: 99cb218d-9b1f-4e43-94d2-4ea74b0e10d3
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 159be01b1058eac99c30b83534b7a9eafd9c4eb4
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "104050661"
---
# <a name="desktop"></a>Desktop

> [!NOTE]
> Dieses Entwurfs Handbuch wurde für Windows 7 erstellt und wurde für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt weiterhin im Prinzip, aber die Präsentation und die Beispiele entsprechen nicht unseren [aktuellen Entwurfs Anleitungen](/windows/uwp/design/).

Der Desktop ist der Arbeitsbereich des Benutzers für Ihre Programme. Es ist keine Möglichkeit, das Bewusstsein für Ihr Programm oder seine Marke zu fördern. Nicht missbrauchen!

Der Desktop ist der Arbeitsbereich auf dem Bildschirm, der von Microsoft Windows bereitgestellt wird, analog zu einem physischen Desktop. Sie besteht aus einem [Arbeitsbereich](glossary.md) und einer [Taskleiste](winenv-taskbar.md). Der Arbeitsbereich kann mehrere Monitore umfassen.

![Screenshot eines typischen Windows-Desktops ](images/winenv-desktop-image1.png)

Ein typischer Windows-Desktop.

Der aktive Monitor ist der Monitor, auf dem das aktive Programm ausgeführt wird. Der Standard Monitor ist der Standard Monitor mit dem Startmenü, der Taskleiste und dem Benachrichtigungsbereich.

## <a name="design-concepts"></a>Entwurfskonzepte

Der Windows-Desktop verfügt über die folgenden Programm Zugriffspunkte:

-   **Arbeitsbereich.** Der Bereich auf dem Bildschirm, in dem Benutzer ihre Arbeit ausführen und Programme, Dokumente und deren Verknüpfungen speichern können. Obwohl der Desktop technisch gesehen die Taskleiste enthält, bezieht er sich in den meisten Kontexten nur auf den Arbeitsbereich.
-   **Start Schaltfläche.** Der Zugriffspunkt für alle Programme und besonderen Windows-Speicherorte (Dokumente, Bilder, Musik, Spiele, Computer, Systemsteuerung) mit den Listen "zuletzt verwendet" für den schnellen Zugriff auf zuletzt verwendete Programme und Dokumente.
-   **Schnellstart: Aus Windows 7 entfernt.** Ein direkter Zugriffspunkt für Programme, die vom Benutzer ausgewählt wurden.
-   **Taskleiste.** Der Zugriffspunkt für das Ausführen von Programmen, die über Desktop Präsenz verfügen. Technisch gesehen erstreckt sich die Taskleiste auf den gesamten Balken von der Start Schaltfläche bis zum Benachrichtigungsbereich. in den meisten Kontexten bezieht sich die Taskleiste auf den Bereich dazwischen, der die Schaltflächen der Taskleiste enthält. Dieser Bereich wird manchmal auch als TaskBand bezeichnet.
-   **Deskbands. Nicht empfohlen.** Minimierte funktionale, lange laufende Programme, z. b. die sprach Leiste. Programme, die auf deskbands minimieren, zeigen bei minimaler Minimierung keine Task leisten Schaltflächen an
-   **Benachrichtigungsbereich.** Eine kurzfristige Quelle für Benachrichtigungen und Status sowie einen Zugriffspunkt für System-und programmbezogene Features, die nicht auf dem Desktop vorhanden sind.

![Screenshot der Schaltfläche "Start", Taskleiste, Miniaturansicht ](images/winenv-desktop-image2.png)

Zu den Windows-Desktop Zugriffs Punkten zählen die Start Schaltfläche, die Taskleiste und der Benachrichtigungsbereich. Beachten Sie die Miniaturansicht der Task leisten Schaltfläche.

**Der Windows-Desktop ist eine begrenzte, freigegebene Ressource, die der Einstiegspunkt des Benutzers auf Windows ist. Belassen Sie die Benutzer in der Kontrolle.** Sie sollten die entsprechenden Bereiche wie vorgesehen verwenden – jede andere Verwendung sollte als Missbrauch angesehen werden. Zeigen Sie Sie nicht als Methoden an, um das Bewusstsein Ihres Programms oder seiner [Marke](exper-branding.md)zu fördern.

Für Windows 7 können OEMs (Original Equipment Manufacturers) und unabhängige Hardware Hersteller (IHVs) die Geräte Stufe verwenden, um eine angepasste Benutzeroberfläche für den Computer und die Geräte zu entwerfen, ohne dass die Desktops der Benutzer gruppiert werden. Insbesondere OEMs können Geräte Stufen-PCs verwenden, um benutzerdefinierte Programme, Dienst Angebote und Unterstützung bereitzustellen. Weitere Informationen finden Sie im [Microsoft Device-Entwicklungs-Kit](https://www.microsoft.com/whdc/device/DeviceExperience/Dev-Kit.mspx).

**Wenn Sie nur eine Aktion ausführen...**

-   Den Desktop nicht missbrauchen – behalten Sie die Kontrolle der Benutzer. Wenn Ihre Ziel Benutzer Ihr Programm wahrscheinlich häufig verwenden, stellen Sie während des Setups eine Option bereit, um eine Verknüpfung auf dem Desktop zu platzieren, deren Auswahl standardmäßig aufgehoben ist.

## <a name="guidelines"></a>Richtlinien

-   **Wenn Ihre Benutzer Ihr Programm sehr wahrscheinlich häufig verwenden, stellen Sie während des Setups eine Option bereit, um eine Programm Verknüpfung auf dem Desktop zu platzieren.** Die meisten Programme werden nicht häufig genug verwendet, um das anbieten dieser Option zu gewährleisten.
-   **Stellen Sie die Option standardmäßig nicht ausgewählt dar.** Es ist wichtig, dass die Benutzer die Option auswählen müssen, da sich die nicht gewünschten Symbole auf dem Desktop befinden, werden Sie von vielen Benutzern nur ungern entfernt. Dies kann zu unnötiger Desktop Übersichtlichkeit führen.
-   **Wenn Benutzer die Option auswählen, geben Sie nur eine einzelne Programm Verknüpfung an.** Wenn Ihr Produkt aus mehreren Programmen besteht, stellen Sie nur eine Verknüpfung mit dem Hauptprogramm bereit.
-   **Legen Sie nur Programm Verknüpfungen auf dem Desktop ab.** Legen Sie das eigentliche Programm oder andere Dateitypen nicht ab.

    **Richtig:**

    ![Screenshot des Verknüpfungs Symbols mit Pfeil Überlagerung ](images/winenv-desktop-image3.png)

    **Falsch:**

    ![Screenshot des Programm Symbols ](images/winenv-desktop-image4.png)

    Im falschen Beispiel wird das Programm, nicht eine Verknüpfung, auf den Desktop kopiert.

-   **Wählen Sie eine Bezeichnung aus, die ohne Abschneiden angezeigt werden kann.** Benutzer sollten keine Ellipsen sehen.

    **Richtig:**

    ![Screenshot des Verknüpfungs Symbols mit dem vollständigen Namen ](images/winenv-desktop-image3.png)

    **Falsch:**

    ![Screenshot des Verknüpfungs Symbols mit einem abgekürzten Namen ](images/winenv-desktop-image5.png)

    Im falschen Beispiel ist die Bezeichnung der Programm Verknüpfung so lang, dass Sie abgeschnitten wird.

## <a name="documentation"></a>Dokumentation

-   Wenn Sie auf den Desktop verweisen, verwenden Sie den Desktop ohne groß-und Kleinschreibung.
-   Wenn Sie auf Desktop Verknüpfungen verweisen, verwenden Sie die Verknüpfung ohne groß-und Kleinschreibung.

 

 