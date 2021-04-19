---
description: Bei einem Telefongerät handelt es sich um ein Gerät, das die Geräteklasse "Phone" unterstützt, die auch über "huokswitches", "Handsets", "Speakers"
ms.assetid: c2660d77-0265-49d4-bd04-1cddd674b760
title: Phone-Geräte Elemente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc5744967dc738a65d7632dc1a1f6126bfbc9887
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368770"
---
# <a name="phone-device-elements"></a>Phone-Geräte Elemente

Bei einem Telefongerät handelt es sich um ein Gerät, das die Geräteklasse "Phone" unterstützt und einige oder alle der folgenden Elemente enthält:

-   "", "", "" Für die Audioeingabe **und-Ausgabe**. Ein Telefongerät kann über mehrere Wandler verfügen, die in der Anwendung oder im manuellen Benutzer Steuerelement aktiviert und deaktiviert (abhook oder platziert) werden können.

    Telefonieart identifiziert drei Typen von für viele Telefon Sätze gemeinsamen Geräte, die sich auf dem Gerät befinden:

     **Handy**: die traditionelle Kombination aus Mund und Ohr, die manuell von einem Kraftakt entfernt und im Ohr des Benutzers gehalten werden muss.  
    **Speakerphone**: ermöglicht dem Benutzer das Durchführen von Anrufen durch Anrufe. Das Telefon Telefon kann intern oder extern auf dem Telefongerät vorliegen. Der Redner Teil eines Speakers ermöglicht mehrere Listener.  
    **Headset**: ermöglicht dem Benutzer das Durchführen von anrufen.  
    

    Ein Port Switch muss OFFHOOK sein, um zuzulassen, dass Audiodaten an den entsprechenden-Wandler gesendet und/oder empfangen werden.

-   Volumesteuerung/Steuerelement/stumm Schaltung: jedes Gerät mit dem Gerät ist die Kopplung eines Referenten und einer Mikrofon Komponente. Die API stellt die Volumensteuerung und das stumm Schaltung von Redner Komponenten sowie die Steuerung oder das stumm Schaltung von Mikrofon Komponenten bereit.
-   [](ring.md)Ruftart bedeutet, dass Benutzer in der Regel über eine Glocke warnen müssen. Ein Telefongerät kann möglicherweise in einer Vielzahl von Modi oder Mustern Klingeln.
-   [Display](display.md): ein Mechanismus zur visuellen Darstellung von Nachrichten für den Benutzer. Eine Telefonanzeige ist gekennzeichnet durch die Anzahl der Zeilen und Spalten.
-   [Telefon](phone-buttons.md)Schaltflächen: ein Array von Schaltflächen. Wenn der Benutzer auf eine Schaltfläche auf dem Telefon Satz drückt, meldet die API, dass die entsprechende Schaltfläche gedrückt wurde. Schaltflächen-Lamp-IDs identifizieren ein Schaltflächen-und Lamp-Paar. Natürlich ist es möglich, Schaltflächen-Lamp-Paare ohne Schaltfläche oder ohne Lamp zu haben. Schaltflächen-Lamp-IDs sind ganzzahlige Werte im Bereich von 0 bis zur maximalen Anzahl von Schaltflächen, die auf dem Telefongerät verfügbar sind, minus eins. Jede Schaltfläche gehört zu einer Schaltflächen Klasse. Zu den Klassen zählen Schaltflächen für die Anzeige Darstellung, Funktions Schaltflächen, Tastenkombinationen und lokale Schaltflächen.
-   - [Lampen](lamps.md): ein Array von-Lampen (z. b. LEDs), die einzeln von der API gesteuert werden. Die Beleuchtung kann in verschiedenen Modi beleuchtet werden, indem die Häufigkeit von ein-und ausgeschaltet wird. Mit dem Schaltflächen-Lamp-Bezeichner wird die Lamp identifiziert.
-   [Datenbereiche](data-areas.md): Speicherbereiche auf dem Telefongerät, in denen Anweisungs Code oder Daten heruntergeladen und/oder aus hochgeladen werden können. Die heruntergeladenen Informationen wirken sich auf das Verhalten (oder das Programm) auf das Telefongerät aus.

TAPI ermöglicht es einer Anwendung, Elemente des Telefon Geräts zu überwachen und zu steuern. Die nützlichsten Elemente für eine Anwendung sind die Geräte mit dem Gerät "". Der Telefon Satz kann als Audio-e/a-Gerät (auf dem Computer) mit der volumesteuerung, zum Erlangen von Kontrolle und stumm Schaltung (für Warnungen des Benutzers), zu Daten Bereichen (für die Programmierung des Telefons) und möglicherweise zu einer Anzeige dienen, obwohl die Anzeige des Computers besser ist. Der anwendungswriter wird von der direkten Steuerung oder Verwendung von Telefon-und Telefon Schaltflächen abgeraten, da LAMP-und Schaltflächen Funktionen zwischen den Telefon Sätzen stark variieren können, und Anwendungen können schnell auf bestimmte Telefon Sätze zugeschnitten werden.

Es gibt keine garantierte Kernreihe von Diensten, die von allen Telefongeräten unterstützt werden, da es für Linien Geräte (die grundlegenden Telefoniedienste) gilt. Bevor eine Anwendung ein Telefongerät verwenden kann, muss die Anwendung daher zunächst die genauen Funktionen des Telefon Geräts bestimmen. Telefoniefunktionen variieren je nach Konfiguration (Client im Vergleich zu Client/Server), der Telefon Hardware und der Dienstanbieter Software. Anwendungen sollten keine Annahmen darüber treffen, welche Telefoniefunktionen zur Verfügung stehen. Eine Anwendung bestimmt die Gerätefunktionen eines Phone-Geräts durch Aufrufen der [**phonegetdevcaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps) -Funktion. Die Gerätefunktionen eines Telefons geben an, welche dieser Elemente für jedes im System vorhandene Telefongerät vorhanden sind und welche Funktionen Sie haben. Diese Abstraktion ist zwar stark an die echten Telefon Sätze gerichtet, aber diese Abstraktion kann auch eine sinnvolle Implementierung (oder eine Teilmenge davon) für andere Geräte bereitstellen. Nehmen Sie als Beispiel ein separates Headset, das direkt mit dem Computer verbunden und steuerbar ist und als Telefongerät betrieben wird. Die Änderungen an "Anhebungs Switch" können durch die Erkennung von voiceenergy (OFFHOOK) oder eine Ruhe Periode (OnHook) ausgelöst werden. das Klingeln kann durch die Generierung eines akustischen Signals in das Headset emuliert werden. eine Anzeige kann über die Text-zu-Sprache-Konvertierung emuliert werden.

Ein Telefongerät muss nicht in der Hardware realisiert werden, sondern kann stattdessen in Software mit einer Maus-oder Tastatur gesteuerten grafischen Befehlsschnittstelle und dem Lautsprecher oder Audiosystem des Computers emuliert werden. Ein solches "Vorläufiges Telefon" kann eine Anwendung sein, die TAPI verwendet. Es kann auch ein Dienstanbieter sein, der als Telefongerät aufgeführt werden kann, das für andere Anwendungen über die API verfügbar ist, und als solcher wird eine Telefongeräte-ID zugewiesen.

Abhängig von der Umgebung und der Konfiguration können Telefon Sätze als gemeinsam genutzte Geräte zwischen der Anwendung und dem Switch verwendet werden. Eine geringfügige Bereitstellung erfolgt in der API, bei der der Switch die Kontrolle über ein Telefongerät der API vorübergehend aussetzen kann.

 

 



