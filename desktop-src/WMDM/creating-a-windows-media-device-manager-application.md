---
title: Erstellen einer Windows Media Device Manager-Anwendung
description: Erstellen einer Windows Media Device Manager-Anwendung
ms.assetid: 6a200bd9-19dd-4130-acb4-e038b469c334
keywords:
- Windows Media Device Manager, Erstellen von Anwendungen
- Device Manager, Erstellen von Anwendungen
- Windows Media Device Manager, Programmier Handbuch
- Device Manager, Programmier Handbuch
- Programmier Handbuch, Desktop Anwendungen
- Programmier Handbuch, Windows Media Device Manager
- Programmier Handbuch, Plug-ins
- Programmier Handbuch, Erstellen von Anwendungen
- Windows Media Device Manager, Desktop Anwendungen
- Device Manager, Desktop Anwendungen
- Windows Media Device Manager, Plug-ins
- Device Manager, Plug-in
- Plug-ins, erstellen
- Plug-ins, Programmier Handbuch
- Desktop Anwendungen, erstellen
- Erstellen von Windows Media Device Manager-Anwendungen, Informationen zu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b50a2dfce057b993f84c0aca4c8f45796f67ba8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340205"
---
# <a name="creating-a-windows-media-device-manager-application"></a>Erstellen einer Windows Media Device Manager-Anwendung

In diesem Abschnitt wird beschrieben, wie Sie Windows Media Device Manager in der Anwendung verwenden. Der Begriff "Anwendung" bedeutet hier entweder eine ausführbare Datei, z. b. einen Media Player oder ein com-Plug-in, z. b. ein Messungs-Plug-in.

Microsoft umfasst mehrere Dienstanbieter mit Windows XP und Windows Media Player 10, darunter einen MTP-Dienstanbieter, einen Windows CE Dienstanbieter (für Geräte mit Windows CE und mithilfe des RAPI-Protokolls (z. b. Pocket PC) und einen Dienstanbieter für MSC-Geräte (Massenspeicher Kategorie). Sie können auch einen eigenen Dienstanbieter erstellen, um die Kommunikation mit Ihrem eigenen Gerät sicherzustellen. Weitere Informationen finden Sie unter [Erstellen eines Dienstanbieters](creating-a-service-provider.md).

Es gibt eine Reihe von Legacy Dienstanbietern von Drittanbietern, die die nicht-MTP-, nicht-RAPI-oder nicht-MSC-Geräte eines bestimmten Herstellers adressieren. Diese Dienstanbieter sind auf dem Treiber Datenträger enthalten, der mit diesen Geräten ausgeliefert wird.

Eine Anwendung, die Windows Media Device Manager verwendet, muss die folgenden Schritte ausführen.

1.  **Erkennen von Datenschutzproblemen, die mit der Entwicklung einer Anwendung verbunden sind.** In der [Datenschutzerklärung](privacy-statement.md) finden Sie Informationen zu einigen Datenschutzproblemen im Zusammenhang mit der Entwicklung einer Windows Media Device Manager Anwendung
2.  **Fügen Sie die erforderlichen Bibliotheks-und Header Dateien für die Anwendung ein.** Informationen zu den Dateien, die Sie in Ihr Projekt einschließen müssen, finden Sie unter [erforderliche Bibliothek-und Header Dateien für eine Anwendung](required-library-and-header-files-for-an-application.md) .
3.  **Authentifizieren Sie die Anwendung, und rufen Sie die Hauptschnittstelle von iwmdmdevice ab.** Die erste Aufgabe, die eine Anwendung für die Verwendung von Windows Media Device Manager ausführen muss, besteht darin, sich zu authentifizieren. Bei diesem Vorgang wird die Identität der Anwendung auf Windows Media-Device Manager mithilfe eines Dummy-Zertifikats für eingeschränkte Windows Media Device Manager-Funktionen überprüft, oder es wird ein offizielles Zertifikat für die vollständige Funktionalität verwendet. Weitere Informationen finden Sie unter [Authentifizieren der Anwendung](authenticating-the-application.md).
4.  **Listet die verbundenen Geräte auf.** Der erste Schritt bei der Kommunikation mit Geräten besteht darin herauszufinden, welche Geräte verbunden sind und für Windows Media Device Manager zugänglich sind. Weitere Informationen finden Sie unter Auflisten von [Geräten](enumerating-devices.md).
5.  **Überprüfen Sie den Status der DRM-Komponenten des Geräts.** Zum Verwenden von DRM-geschützten Dateien muss ein Gerät auf einer bestimmten Version von Windows Media DRM für tragbare Geräte erstellt werden, und die DRM-Komponenten müssen auf dem neuesten Stand sein. Bevor Sie mit der Verarbeitung von Dateien auf dem Gerät beginnen, sollten Sie überprüfen, ob das Gerät von DRM geschützte Dateien unterstützt und ob das Gerät aktualisiert werden muss. Weitere Informationen finden Sie unter [behandeln geschützter Inhalte in der Anwendung](handling-protected-content-in-the-application.md).
6.  **Erkunden Sie ein Gerät.** Nachdem Sie das gewünschte Gerät gefunden haben, können Sie den Inhalt dieses Geräts überprüfen. Weitere Informationen finden Sie unter unter [Suchen eines Geräts](exploring-a-device.md).
7.  **Lesen von Dateien vom Gerät und Schreiben von Dateien auf das Gerät.** Nachdem Sie das Layout des Geräts kennen, können Sie mit dem Übertragen von Dateien auf das und vom Gerät beginnen. Weitere Informationen finden Sie unter [Lesen von Dateien vom Gerät](reading-files-from-the-device.md) und [Schreiben von Dateien auf das Gerät](writing-files-to-the-device.md).
8.  **Erstellen von Wiedergabelisten auf dem Gerät.** Eine Datei, die Sie auf das Gerät schreiben können, ist eine abstrakte Datei, die eine Auflistung von Verweisen auf andere Dateien ist. Die Möglichkeit, abstrakte Dateien auf ein Gerät zu schreiben, hängt zwar vom Dienstanbieter und vom Gerät ab, aber im Allgemeinen haben nur MTP-Geräte diese Funktion. Weitere Informationen finden Sie unter [Erstellen einer Wiedergabeliste auf dem Gerät](creating-a-playlist-on-the-device.md).

Zusätzlich zu diesen Schritten gibt es mehrere weitere Funktionen, die Sie in Ihrer Anwendung aktivieren können:

-   **Benachrichtigungen.** Sie können Ihre Anwendung für den Empfang von Benachrichtigungen aktivieren, wenn Geräte eine Verbindung mit dem Computer herstellen oder diese trennen. Weitere Informationen finden Sie unter [Aktivieren von Benachrichtigungen](enabling-notifications.md).
-   **Protokollierung:** Windows Media Device Manager verwendet ein Protokollierungs Objekt, das einen Datensatz seiner Aktionen in einer lokalen Textdatei speichert. Sie können diesem Protokollmeldungen hinzufügen, um die Analyse von Fehlern oder der Leistung in Ihrer Anwendung zu erleichtern. Weitere Informationen finden Sie unter [Aktivieren der Protokollierung](enabling-logging.md).
-   **Verwendung der Messungs Inhalte.** Sie können Statistiken zur Inhalts Verwendung für Lizenzen abrufen, die dieses Recht erteilen. Diese Statistiken können dann an einen Webserver gesendet werden, um die Lizenzgebühren für Inhalts Besitzer zu berechnen. Weitere Informationen finden Sie unter [Messungs Inhalts Verwendung](metering-content-usage.md).

**Vorsicht beachten**

Möglicherweise muss Ihre Anwendung mit einer Vielzahl von Geräten arbeiten, einschließlich einiger, die Sie nicht entwickelt haben und deren Code Sie noch nie getestet haben. Diese Geräte reagieren möglicherweise nicht genau auf Abfragen und Befehle oder implementieren MTP oder andere Spezifikationen. Stellen Sie sicher, dass Sie eine robuste Fehlerüberprüfung und Fall Back Funktion einschließen, um die unerwartete zu behandeln. Programm defensiv.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Programmierhandbuch**](programming-guide.md)
</dt> </dl>

 

 




