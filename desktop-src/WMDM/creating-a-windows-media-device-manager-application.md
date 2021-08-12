---
title: Erstellen einer Windows Media Geräte-Manager-Anwendung
description: Erstellen einer Windows Media Geräte-Manager-Anwendung
ms.assetid: 6a200bd9-19dd-4130-acb4-e038b469c334
keywords:
- Windows Medien Geräte-Manager, Erstellen von Anwendungen
- Geräte-Manager,Erstellen von Anwendungen
- Windows Media Geräte-Manager, Programmierhandbuch
- Geräte-Manager, Programmierhandbuch
- Programmierhandbuch,Desktopanwendungen
- Programmierhandbuch,Windows Media Geräte-Manager
- Programmierhandbuch, Plug-Ins
- Programmierhandbuch,Erstellen von Anwendungen
- Windows Medien Geräte-Manager, Desktopanwendungen
- Geräte-Manager,Desktopanwendungen
- Windows Medien Geräte-Manager, Plug-Ins
- Geräte-Manager,Plug-Insp
- Plug-Ins, erstellen
- Plug-Ins, Programmierhandbuch
- Desktopanwendungen, Erstellen
- Erstellen von Windows Media Geräte-Manager-Anwendungen, Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ba468d4d9a04176847259087b8ba2626c2ffa3e0cac089f8433993320a7e125
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118585557"
---
# <a name="creating-a-windows-media-device-manager-application"></a>Erstellen einer Windows Media Geräte-Manager-Anwendung

In diesem Abschnitt wird beschrieben, wie Sie Windows Media Geräte-Manager in Ihrer Anwendung verwenden. Der Begriff "Anwendung" bedeutet hier entweder eine ausführbare Datei, z. B. ein Media Player, oder ein COM-Plug-In, z. B. ein Messungs-Plug-In.

Microsoft umfasst mehrere Dienstanbieter mit Windows XP und Windows Media Player 10, einschließlich eines MTP-Dienstanbieters, eines Windows CE-Dienstanbieters (für Geräte, auf denen Windows CE ausgeführt wird und die das PROTOKOLL CABI verwenden, z. B. der Pocket PC), und einem Dienstanbieter für Massenspeicherkategoriegeräte (MSC). Sie können auch einen eigenen Dienstanbieter erstellen, um die Kommunikation mit Ihrem eigenen Gerät sicherzustellen. Weitere Informationen finden Sie unter [Erstellen eines Dienstanbieters.](creating-a-service-provider.md)

Es gibt eine Reihe von Legacy-Dienstanbietern von Drittanbietern, die das Nicht-MTP-, Nicht-HACKI- oder Nicht-MSC-Gerät eines bestimmten Herstellers adressieren. Diese Dienstanbieter sind auf dem Treiberdatenträger enthalten, der mit diesen Geräten ausgeliefert wird.

Eine Anwendung, die Windows Media Geräte-Manager verwendet, muss die folgenden Schritte ausführen.

1.  **Sie sollten sich über Datenschutzprobleme im Zusammenhang mit der Entwicklung einer Anwendung im Klaren sein.** Informationen zu einigen Datenschutzproblemen im Zusammenhang mit der Entwicklung einer Windows Media Geräte-Manager-Anwendung finden Sie unter [Datenschutzerklärung.](privacy-statement.md)
2.  **Schließen Sie die erforderlichen Bibliotheks- und Headerdateien für Ihre Anwendung ein.** Unter [Erforderliche Bibliotheks- und Headerdateien für eine Anwendung](required-library-and-header-files-for-an-application.md) erfahren Sie, welche Dateien Sie in Ihr Projekt einschließen müssen.
3.  **Authentifizieren Sie die Anwendung, und beziehen Sie die IWMDMDevice-Stammschnittstelle.** Die erste Aufgabe, die eine Anwendung für die Verwendung Windows Media Geräte-Manager durchführen muss, besteht darin, sich selbst zu authentifizieren. Bei diesem Prozess wird die Identität der Anwendung für Windows Media Geräte-Manager mithilfe eines Dummyzertifikats für eingeschränkte Windows Media Geräte-Manager-Funktionalität oder mit einem offiziellen Zertifikat für die vollständige Funktionalität überprüft. Weitere Informationen finden Sie unter [Authentifizieren der Anwendung.](authenticating-the-application.md)
4.  **Aufzählen der verbundenen Geräte.** Der erste Schritt bei der Kommunikation mit Geräten besteht darin, herauszufinden, welche Geräte mit Windows Media Geräte-Manager verbunden und zugänglich sind. Weitere Informationen finden Sie unter [Aufzählen von Geräten.](enumerating-devices.md)
5.  **Überprüfen Sie den Status der DRM-Komponenten des Geräts.** Um DRM-geschützte Dateien verwenden zu können, muss ein Gerät auf einer Version von Windows Medien-DRM für portable Geräte erstellt werden, und die DRM-Komponenten müssen auf dem neuesten Stand sein. Bevor Sie mit der Verarbeitung von Dateien auf dem Gerät beginnen, sollten Sie am besten prüfen, ob das Gerät DURCH DRM geschützte Dateien unterstützt und ob das Gerät aktualisiert werden muss. Weitere Informationen finden Sie unter [Behandeln von geschützten Inhalten in der Anwendung](handling-protected-content-in-the-application.md).
6.  **Erkunden eines Geräts** Nachdem Sie das gewünschte Gerät gefunden haben, können Sie den Inhalt dieses Geräts untersuchen. Weitere Informationen finden Sie unter [Untersuchen eines Geräts.](exploring-a-device.md)
7.  **Lesen von Dateien vom Gerät und Schreiben von Dateien auf das Gerät.** Nachdem Sie das Layout des Geräts kennen, können Sie mit dem Übertragen von Dateien auf das und vom Gerät beginnen. Weitere Informationen finden Sie unter [Lesen von Dateien vom Gerät](reading-files-from-the-device.md) und Schreiben von Dateien auf das [Gerät.](writing-files-to-the-device.md)
8.  **Erstellen Sie Wiedergabelisten auf dem Gerät.** Eine Art von Datei, die Sie auf das Gerät schreiben können, ist eine abstrakte Datei, bei der es sich um eine Sammlung von Verweisen auf andere Dateien handelt. Obwohl die Fähigkeit, abstrakte Dateien auf ein Gerät zu schreiben, vom Dienstanbieter und dem Gerät abhängt, verfügen in der Regel nur MTP-Geräte über diese Funktion. Weitere Informationen finden Sie unter [Erstellen einer Wiedergabeliste auf dem Gerät.](creating-a-playlist-on-the-device.md)

Zusätzlich zu diesen Schritten gibt es mehrere weitere Features, die Sie in Ihrer Anwendung aktivieren können:

-   **Benachrichtigungen.** Sie können es Ihrer Anwendung ermöglichen, Benachrichtigungen zu empfangen, wenn Geräte eine Verbindung mit dem Computer herstellen oder die Verbindung mit dem Computer trennen. Weitere Informationen finden Sie unter [Aktivieren von Benachrichtigungen.](enabling-notifications.md)
-   **Protokollierung:** Windows Media Geräte-Manager verwendet ein Protokollierungsobjekt, das einen Datensatz seiner Aktionen in einer lokalen Textdatei speichert. Sie können diesem Protokoll Meldungen hinzufügen, um Fehler oder die Leistung in Ihrer Anwendung zu analysieren. Weitere Informationen finden Sie unter [Aktivieren der Protokollierung.](enabling-logging.md)
-   **Nutzung von Messungsinhalten.** Sie können Inhaltsnutzungsstatistiken für Lizenzen abrufen, die dieses Recht gewähren. Diese Statistiken können dann an einen Webserver gesendet werden, um lizenzgebührende Zahlungen an Inhaltsbesitzer zu berechnen. Weitere Informationen finden Sie unter [Messung der Inhaltsverwendung.](metering-content-usage.md)

**Hinweis zur Vorsicht**

Ihre Anwendung muss möglicherweise mit einer Vielzahl von Geräten arbeiten, einschließlich einiger Geräte, die Sie nicht entwickelt haben und mit denen Sie Ihren Code noch nie getestet haben. Diese Geräte reagieren möglicherweise oder nicht genau auf Abfragen und Befehle oder implementieren MTP oder andere Spezifikationen. Stellen Sie sicher, dass Sie stabile Fehlerüberprüfungs- und Fallbackfunktionen für den Umgang mit unerwarteten Fehlern verwenden. Programm defensiv.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Programmierhandbuch**](programming-guide.md)
</dt> </dl>

 

 




