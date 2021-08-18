---
description: Ein Telefongerät ist ein Gerät, das die Geräteklasse phone unterstützt und Hookswitches, Handsets, Lautsprecherphones und Headsets enthält.
ms.assetid: c2660d77-0265-49d4-bd04-1cddd674b760
title: Telefon Geräteelemente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71c882e7f9ebe279d0ee6622708f8b735b68f4c37a2f93dffe2a870271d556cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119774170"
---
# <a name="phone-device-elements"></a>Telefon Geräteelemente

Ein Telefongerät ist ein Gerät, das die Geräteklasse phone unterstützt und einige oder alle der folgenden Elemente enthält:

-   **Hookswitch/Transducer: Dies** ist ein Mittel für Audioeingabe und -ausgabe. Ein Telefongerät kann über mehrere Transducer verfügen, die unter der Anwendungs- oder manuellen Benutzersteuerung aktiviert und deaktiviert (offhook- oder onhook-geschaltet) werden können.

    Telefonie identifiziert drei Arten von Hookswitchgeräten, die vielen Telefonsätzen gemeinsam sind:

     **Handset:** Die herkömmliche Kombination aus 15 Und-Händen, die manuell aus einem Würfer entfernt und gegen das Gehör des Benutzers gehalten werden muss.  
    **Sprechertelefon:** Ermöglicht es dem Benutzer, Anrufe freihunter zu führen. Das Lautsprechertelefon kann intern oder extern für das Telefongerät sein. Der Sprecherteil eines Lautsprechers lässt mehrere Listener zu.  
    **Headset:** Ermöglicht es dem Benutzer, Anrufe ohne Freisprechen zu tätigen.  
    

    Ein Hookschalter muss ein Offhook sein, damit Audiodaten an den entsprechenden Transducer gesendet und/oder empfangen werden können.

-   Lautstärkesteuerung/Verstärkungssteuerung/Stummschaltung: Jedes Hookwitchgerät ist die Kopplung eines Lautsprechers mit einer Mikrofonkomponente. Die API ermöglicht die Lautstärkesteuerung und Stummschaltung von Sprecherkomponenten sowie die Steuerung oder Schaltung von Mikrofonkomponenten.
-   [Ringer:](ring.md)Ein Mittel zum Warnen von Benutzern, in der Regel über eine Glocke. Ein Telefongerät kann in einer Vielzahl von Modi oder Mustern ringen.
-   [Anzeigen:](display.md)Ein Mechanismus zum visuellen Präsentieren von Nachrichten für den Benutzer. Eine Telefonanzeige wird durch die Anzahl der Zeilen und Spalten gekennzeichnet.
-   [Telefon Schaltflächen:](phone-buttons.md)Ein Array von Schaltflächen. Wenn der Benutzer eine Schaltfläche auf dem Telefonset drückt, meldet die API, dass die entsprechende Schaltfläche gedrückt wurde. Bezeichner für Schaltflächen-Laternen identifizieren ein Schaltflächen- und ein Lampepaar. Natürlich ist es möglich, Taste-Laternen-Paare ohne Schaltfläche oder ohne Lampe zu verwenden. Bezeichner für Schaltflächenlanen sind ganzzahlige Werte, die zwischen 0 und der maximalen Anzahl der auf dem Telefongerät verfügbaren Schaltflächen-Glühfläche minus 1 liegen. Jede Schaltfläche gehört zu einer Schaltflächenklasse. Zu den Klassen gehören Schaltflächen zur Darstellung von Aufrufen, Funktionsschaltflächen, Tastaturschaltflächen und lokale Schaltflächen.
-   [Bild:](lamps.md)Ein Array von Steuerelementen (z. B. LEDs), die von der API einzeln kontrolliert werden können. Die Lichtung kann in verschiedenen Modi durch Variieren der Ein- und Aus-Häufigkeit beleuchtet werden. Der Bezeichner der Schaltflächen-Lampe identifiziert die Lampe.
-   [Datenbereiche:](data-areas.md)Arbeitsspeicherbereiche auf dem Telefongerät, in die Anweisungscode oder Daten heruntergeladen und/oder von dort hochgeladen werden können. Die heruntergeladenen Informationen wirken sich auf das Verhalten (oder anders ausgedrückt: Programm) des Telefongeräts aus.

TAPI ermöglicht einer Anwendung das Überwachen und Steuern von Elementen des Telefongeräts. Die nützlichsten Elemente für eine Anwendung sind hookswitch-Geräte. Der Telefonsatz kann als Audio-E/A-Gerät (für den Computer) mit Lautstärkesteuerung, Steuerung und Stummschaltung, einem Ringer (zum Warnen des Benutzers), Datenbereichen (zum Programmieren des Telefons) und möglicherweise als Anzeige fungieren, obwohl die Anzeige des Computers besser geeignet ist. Es wird davon abgeraten, den Anwendungswriter direkt zu steuern oder Telefonknöpfe oder Telefonschaltflächen zu verwenden, da die Lampe- und Schaltflächenfunktionen je nach Telefongruppen stark variieren können und Anwendungen schnell auf bestimmte Telefonsätze zugeschnitten werden können.

Es gibt keinen garantierten Kernsatz von Diensten, die von allen Telefongeräten unterstützt werden, wie es für Liniengeräte (die Basic-Telefoniedienste) gibt. Daher muss die Anwendung zunächst die genauen Funktionen des Telefongeräts bestimmen, bevor eine Anwendung ein Telefongerät verwenden kann. Die Telefoniefunktion variiert je nach Konfiguration (Client/Client/Server), Telefonhardware und Dienstanbietersoftware. Anwendungen sollten keine Annahmen darüber treffen, welche Telefoniefunktionen verfügbar sind. Eine Anwendung bestimmt die Gerätefunktionen eines Telefongeräts durch Aufrufen der [**phoneGetDevCaps-Funktion.**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps) Die Gerätefunktionen eines Telefons geben an, welches dieser Elemente für jedes im System enthaltene Telefongerät vorhanden ist und welche Funktionen es gibt. Obwohl diese Abstraktion stark auf echte Telefonsätze ausgerichtet ist, kann sie auch für andere Geräte eine sinnvolle Implementierung (oder eine Teilmenge davon) bereitstellen. Nehmen Wir als Beispiel ein separates Headset, das direkt vom Computer verbunden und steuerbar ist und als Telefongerät betrieben wird. Hookswitch-Änderungen können durch Erkennung der Sprachenergie (Offhook) oder einer Stille (Onhook) ausgelöst werden. Ringing kann durch die Generierung eines akustischen Signals in das Headset emuliert werden. Eine Anzeige kann durch Die Konvertierung von Text in Sprache emuliert werden.

Ein Telefongerät muss nicht in Hardware realisiert werden, sondern kann stattdessen mithilfe einer maus- oder tastaturgesteuerten grafischen Befehlsschnittstelle und des Lautsprechers oder Soundsystems des Computers in Software emuliert werden. Ein solches "soft phone" kann eine Anwendung sein, die TAPI verwendet. Es kann auch ein Dienstanbieter sein, der als Telefongerät aufgeführt werden kann, das für andere Anwendungen über die API verfügbar ist, und daher eine Geräte-ID des Telefons zugewiesen wird.

Je nach Umgebung und Konfiguration können Telefongruppen gemeinsam genutzte Geräte zwischen der Anwendung und dem Switch sein. Einige kleinere Bereitstellungen werden in der API vorgenommen, bei denen der Switch die Steuerung eines Telefongeräts durch die API vorübergehend aussetzen kann.

 

 



