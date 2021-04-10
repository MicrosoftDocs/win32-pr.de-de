---
description: Enthält Informationen zur Programmierschnittstelle für den Konfigurations Dienst für drahtlos Dienste unter Windows XP und Windows Server 2003.
ms.assetid: cd9e8fc0-0a65-4654-95aa-201751183521
title: Verweis auf drahtlos Konfigurations Referenz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ebe202e16aa38fef617f382559f124772d50a58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215896"
---
# <a name="wireless-zero-configuration-reference"></a>Verweis auf drahtlos Konfigurations Referenz

\[Die Programmierschnittstelle für die drahtlose Null-Konfiguration wird ab Windows Vista und Windows Server 2008 nicht mehr unterstützt. Verwenden Sie stattdessen die [native WiFi-API](native-wifi-reference.md), die eine ähnliche Funktionalität bietet. Weitere Informationen finden Sie unter Informationen zur [nativen WiFi-API](about-the-native-wifi-api.md).\]

Dieser Abschnitt enthält Informationen zur Programmierschnittstelle für den Konfigurations Dienst für drahtlos Dienste unter Windows XP und Windows Server 2003. Die Themen umfassen Folgendes:

-   [Konfigurationsfunktionen für drahtlose NULL](wireless-zero-configuration-functions.md)
-   [Konfigurations Strukturen mit drahtlos NULL](wireless-zero-configuration-structures.md)

Die Konfiguration für drahtlose NULL ist ein Windows-Dienst unter Windows XP und Windows Server 2003, der zum Konfigurieren und Verwalten von drahtlos Netzwerkverbindungen auf einem drahtlosen Adapter verwendet wird. Der Dienst Name für die drahtlose Null-Konfiguration ist wzcsvc. Unter Windows XP lautet der Anzeige Name für den wzcsvc-Dienst drahtlos-Null-Konfiguration. Unter Windows Server 2003 lautet der Anzeige Name für den wzcsvc-Dienst "drahtlose Konfiguration".

Der Konfigurations Dienst für drahtlose NULL wird normalerweise zum Startzeitpunkt gestartet. Die Programmierschnittstelle für den Konfigurations Dienst für drahtlose NULL kann nur verwendet werden, wenn der Konfigurations Dienst für drahtlose NULL-Werte gestartet wurde. Wenn der Konfigurations Dienst drahtlos, 0 (null) nicht gestartet wird, wird ein Fehler zurückgegeben.

Um den Konfigurations Dienst für drahtlose NULL zu aktivieren, sodass er automatisch gestartet wird, klicken Sie auf die Schaltfläche **Start** . Wählen Sie die Option **Einstellungen** aus, und klicken Sie dann auf **Systemsteuerung**. Wenn Sie die Windows XP-Ansicht verwenden, wählen Sie die Kategorie **Leistung und Wartung** aus, und klicken Sie dann auf **Verwaltung**. Wenn Sie die klassische Ansicht verwenden, klicken Sie auf **Verwaltung**. Klicken Sie im linken Bereich auf das Symbol " **Dienste** ". Klicken Sie im rechten Bereich auf das Symbol drahtlos Konfiguration, und ändern Sie den **Starttyp** Dropbox in **automatisch**. Diese Einstellung legt fest, dass der Dienst beim Start automatisch gestartet wird. Klicken Sie dann auf die Schaltfläche **Start** , um den Konfigurations Dienst drahtlos 0 (null) zu starten, und klicken Sie auf **OK** .

Die Konfiguration für drahtlose NULL kann auch an einer Eingabeaufforderung gestartet und beendet werden. Führen Sie den folgenden Befehl aus, um die Konfiguration für drahtlose NULL zu starten:

**NET Start-wzcsvc**

Führen Sie den folgenden Befehl aus, um die Konfiguration für drahtlose NULL zu verhindern:

**NET stoppt wzcsvc**

 

 



