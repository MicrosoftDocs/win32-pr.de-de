---
description: Enthält Informationen zur Programmierschnittstelle für den Wireless Zero Configuration-Dienst auf Windows XP und Windows Server 2003.
ms.assetid: cd9e8fc0-0a65-4654-95aa-201751183521
title: Drahtlose Nullkonfigurationsreferenz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 358ff3727edc34d4a5de0f4195895cf02b4596722aecd5849f4e35b9991dbe88
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684430"
---
# <a name="wireless-zero-configuration-reference"></a>Drahtlose Nullkonfigurationsreferenz

\[Die Wireless Zero Configuration-Programmierschnittstelle wird ab Windows Vista und Windows Server 2008 nicht mehr unterstützt. Verwenden Sie stattdessen die [Native Wifi-API](native-wifi-reference.md), die ähnliche Funktionen bereitstellt. Weitere Informationen finden Sie unter [Informationen zur Native Wifi-API.](about-the-native-wifi-api.md)\]

Dieser Abschnitt enthält Informationen zur Programmierschnittstelle für den Wireless Zero Configuration-Dienst auf Windows XP und Windows Server 2003. Die Themen umfassen Folgendes:

-   [Drahtlose Nullkonfigurationsfunktionen](wireless-zero-configuration-functions.md)
-   [Drahtlose Nullkonfigurationsstrukturen](wireless-zero-configuration-structures.md)

Wireless Zero Configuration ist ein Windows-Dienst auf Windows XP und Windows Server 2003, der zum Konfigurieren und Verwalten von Drahtlosnetzwerkverbindungen auf einem Drahtlosadapter verwendet wird. Der Dienstname für Wireless Zero Configuration lautet WZCSVC. Auf Windows XP lautet der Anzeigename für den WZCSVC-Dienst Wireless Zero Configuration. Auf Windows Server 2003 lautet der Anzeigename für den WZCSVC-Dienst Funkkonfiguration.

Der Wireless Zero Configuration-Dienst wird normalerweise zur Startzeit gestartet. Die Programmierschnittstelle für den Wireless Zero Configuration-Dienst kann nur verwendet werden, wenn der Wireless Zero Configuration-Dienst gestartet wurde. Wenn der Wireless Zero Configuration-Dienst nicht gestartet wird, geben die Wireless Zero Configuration-Funktionen einen Fehler zurück.

Um den Wireless Zero Configuration-Dienst so zu aktivieren, dass er automatisch gestartet wird, wechseln Sie zur Schaltfläche **Start.** Wählen Sie die **Option Einstellungen** und dann **Systemsteuerung** aus. Wenn Sie die ansicht Windows XP verwenden, wählen Sie die Kategorie **Leistung und Wartung und** dann **Verwaltung** aus. Wenn Sie die klassische Ansicht verwenden, wählen Sie **Verwaltung aus.** Klicken Sie im linken Bereich auf das Symbol **Dienste.** Klicken Sie im rechten Bereich auf das Symbol Drahtlose Nullkonfiguration, und ändern Sie die Dropbox **für den Starttyp** in **Automatisch.** Mit dieser Einstellung wird festgelegt, dass der Dienst zur Startzeit automatisch gestartet wird. Klicken Sie dann auf die Schaltfläche **Start,** um den Wireless Zero Wireless Zero Configuration-Dienst zu starten, und klicken Sie auf die Schaltfläche **OK.**

Die Drahtlose Zero-Konfiguration kann auch über eine Eingabeaufforderung gestartet und beendet werden. Führen Sie den folgenden Befehl aus, um die Drahtlose Nullkonfiguration zu starten:

**net start wzcsvc**

Führen Sie den folgenden Befehl aus, um die Drahtlose Nullkonfiguration zu beenden:

**net stop wzcsvc**

 

 



