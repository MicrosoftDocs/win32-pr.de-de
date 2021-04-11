---
title: Allgemeine MCI-Fehler
description: Allgemeine MCI-Fehler
ms.assetid: be9c4a2b-44bc-410c-be74-ba55bb4e785b
keywords:
- Mcierr-Rückgabewerte, allgemeine Fehler
- Multimedia-Referenz, MCI-Fehler
- Referenz für Multimedia-, MCI-Fehler
- Media Control Interface (MCI), allgemeine Fehler
- MCI (Medien Steuerungs Schnittstelle), allgemeine Fehler
- Referenz für MCI, allgemeine Fehler
- MCI-Referenz, allgemeine Fehler
- Media Control Interface (MCI), Fehler
- MCI (Medien Steuerungs Schnittstelle), Fehler
- Referenz für MCI, Fehler
- MCI-Referenz, Fehler
- mciSendCommand-Funktion
- mciSendString-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44538937be73c2ccfb1d30de1f1a1c729cc05095
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314787"
---
# <a name="general-mci-errors"></a>Allgemeine MCI-Fehler

Die folgenden Fehler Werte können entweder von der Funktion " [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) " oder der Funktion " [**mciSendString**](/previous-versions//dd757161(v=vs.85)) " zurückgegeben werden:



| Wert                            | Bedeutung                                                                                                                                                     |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| mcierr-ungültiges \_ \_ Zeit \_ Format        | Der angegebene Wert für das Zeitformat ist ungültig.                                                                                                         |
| mcierr \_ kann \_ den \_ Treiber nicht laden.     | Der angegebene Gerätetreiber wird nicht ordnungsgemäß geladen.                                                                                                         |
| mcierr \_ kann \_ nicht \_ alle verwenden         | Der Gerätename "All" ist für diesen Befehl nicht zulässig.                                                                                                      |
| mcierr- \_ kreatewindow             | Das Fenster konnte nicht erstellt oder verwendet werden.                                                                                                                             |
| mcierr- \_ Geräte \_ Länge           | Der Geräte-oder Treiber Name ist zu lang. Geben Sie einen Geräte-oder Treiber Namen an, der kleiner als 79 Zeichen ist.                                                     |
| mcierr- \_ Gerät \_ gesperrt           | Das Gerät wird jetzt geschlossen. Warten Sie einige Sekunden, und wiederholen Sie dann den Vorgang.                                                                                         |
| mcierr- \_ Gerät \_ nicht \_ installiert   | Das angegebene Gerät ist nicht auf dem System installiert. Verwenden Sie die Option Drivers in der Systemsteuerung, um das Gerät zu installieren.                                   |
| Das mcierr- \_ Gerät ist \_ nicht \_ bereit.       | Der Gerätetreiber ist nicht bereit.                                                                                                                             |
| mcierr- \_ Gerät \_ geöffnet             | Der Gerätename wird von dieser Anwendung bereits als Alias verwendet. Verwenden Sie einen eindeutigen Alias.                                                                        |
| Länge des mcierr- \_ Geräts ( \_ Ord) \_      | Der Geräte-oder Treiber Name ist zu lang. Geben Sie einen Geräte-oder Treiber Namen an, der kleiner als 79 Zeichen ist.                                                     |
| mcierr \_ - \_ Gerätetyp \_ erforderlich   | Das angegebene Gerät wurde im System nicht gefunden. Überprüfen Sie, ob das Gerät installiert ist und der Gerätename korrekt geschrieben ist.                            |
| mcierr- \_ Treiber                   | Der Gerätetreiber weist auf ein Problem hin. Wenden Sie sich an den Gerätehersteller, um einen neuen Treiber zu erhalten.                                                      |
| Interner mcierr- \_ Treiber \_         | Der Gerätetreiber weist auf ein Problem hin. Wenden Sie sich an den Gerätehersteller, um einen neuen Treiber zu erhalten.                                                      |
| mcierr- \_ doppelter \_ Alias         | Der angegebene Alias wird bereits in dieser Anwendung verwendet. Verwenden Sie einen eindeutigen Alias.                                                                                |
| die mcierr- \_ Erweiterung wurde \_ nicht \_ gefunden.    | Der angegebenen Erweiterung ist kein Gerätetyp zugeordnet. Geben Sie einen Gerätetyp an.                                                                       |
| mcierr- \_ zusätzliche \_ Zeichen        | Sie müssen eine Zeichenfolge in Anführungszeichen einschließen. Zeichen, die auf das schließende Anführungszeichen folgen, sind ungültig.                                              |
| die mcierr- \_ Datei wurde \_ nicht \_ gefunden.         | Die angeforderte Datei wurde nicht gefunden. Überprüfen Sie, ob Pfad und Dateiname korrekt sind.                                                                             |
| die mcierr- \_ Datei wurde \_ nicht \_ gespeichert.         | Die Datei wurde nicht gespeichert. Stellen Sie sicher, dass Ihr System über genügend Speicherplatz verfügt oder über eine intakte Netzwerkverbindung verfügt.                                                |
| mcierr- \_ Datei \_ Lesen               | Fehler beim Lesen aus der Datei. Stellen Sie sicher, dass die Datei auf Ihrem System vorhanden ist oder dass Ihr System über eine intakte Netzwerkverbindung verfügt.                             |
| mcierr- \_ Datei \_ Schreibvorgang              | Fehler beim Schreiben in die Datei. Stellen Sie sicher, dass Ihr System über genügend Speicherplatz verfügt oder über eine intakte Netzwerkverbindung verfügt.                                            |
| mcierr- \_ Dateiname \_ erforderlich       | Der Dateiname ist ungültig. Stellen Sie sicher, dass der Dateiname nicht länger als acht Zeichen ist, gefolgt von einem Zeitraum und einer Erweiterung.                                  |
| mcierr- \_ Flags sind \_ nicht \_ kompatibel.   | Die angegebenen Parameter können nicht gleichzeitig verwendet werden.                                                                                                           |
| mcierr \_ get \_ CD                  | Die angeforderte Datei oder das MCI-Gerät wurde nicht gefunden. Versuchen Sie, Verzeichnisse zu ändern oder das System neu zu starten.                                                         |
| mcierr- \_ Hardware                 | Das angegebene Gerät weist auf ein Problem hin. Prüfen Sie, ob das Gerät ordnungsgemäß funktioniert, oder wenden Sie sich an den Gerätehersteller.                                     |
| mcierr \_ \_ für \_ Automatisches \_ Öffnen unzulässig | MCI führt den angegebenen Befehl auf einem automatisch geöffneten Gerät nicht aus. Warten Sie, bis das Gerät geschlossen ist, und versuchen Sie dann, den Befehl auszuführen.             |
| mcierr \_ intern                 | Beim Initialisieren von MCI ist ein Problem aufgetreten. Versuchen Sie, das Windows-Betriebssystem neu zu starten.                                                                        |
| Ungültige mcierr- \_ \_ Geräte- \_ ID      | Ungültige Geräte-ID. Verwenden Sie die ID, die dem Gerät beim Öffnen des Geräts gegeben wurde.                                                                               |
| mcierr ( \_ ungültiger \_ Geräte \_ Name)    | Das angegebene Gerät ist weder geöffnet noch von MCI erkannt.                                                                                                     |
| Ungültige mcierr- \_ \_ Datei            | Die angegebene Datei kann auf dem angegebenen MCI-Gerät nicht wiedergegeben werden. Die Datei ist möglicherweise beschädigt oder weist ein falsches Dateiformat auf.                               |
| fehlender mcierr- \_ \_ Parameter       | Der angegebene Befehl erfordert einen Parameter, den Sie angeben müssen.                                                                                          |
| mcierr \_ Multiple                 | Auf mehreren Geräten sind Fehler aufgetreten. Geben Sie jeden Befehl und jedes Gerät separat an, um die Fehler zu identifizieren.                             |
| mcierr \_ muss \_ \_ share able verwenden     | Der Gerätetreiber wird bereits verwendet. Sie müssen den Parameter "sharable" mit jedem geöffneten Befehl angeben, um das Gerät gemeinsam zu verwenden.                                  |
| mcierr ist \_ kein \_ Element \_ zulässig.     | Das angegebene Gerät verwendet keinen Dateinamen.                                                                                                               |
| mcierr \_ keine \_ Ganzzahl              | Der Parameter für diesen MCI-Befehl muss ein ganzzahliger Wert sein.                                                                                                |
| mcierr \_ kein \_ Fenster               | Es ist kein Anzeige Fenster vorhanden.                                                                                                                                 |
| nicht anwendbare mcierr- \_ \_ Funktion  | Die angegebene MCI-Befehlssequenz kann nicht in der angegebenen Reihenfolge ausgeführt werden. Korrigieren der Befehlssequenz versuchen Sie es dann erneut.                                   |
| mcierr \_ - \_ Parameter \_ Block NULL   | Ein NULL-Parameter Block (Struktur) wurde an MCI übergeben.                                                                                                       |
| nicht genügend Arbeits \_ \_ Speicher für mcierr \_          | Ihr System verfügt nicht über genügend Arbeitsspeicher für diesen Task. Beenden Sie eine oder mehrere Anwendungen, um den verfügbaren Arbeitsspeicher zu vergrößern, und versuchen Sie dann erneut, die Aufgabe auszuführen. |
| mcierr \_ ouüber Frange               | Der angegebene Parameterwert liegt außerhalb des gültigen Bereichs für den angegebenen MCI-Befehl.                                                                                |
| mcierr \_ Set \_ CD                  | Der Zugriff auf die angegebene Datei bzw. das angegebene MCI-Gerät ist nicht möglich, da die Anwendung die Verzeichnisse                                                         |
| mcierr \_ Festlegen des \_ Laufwerks               | Der Zugriff auf die angegebene Datei bzw. das angegebene MCI-Gerät ist nicht möglich, da die Anwendung keine Laufwerke                                                              |
| unbenannte mcierr- \_ \_ Ressource        | Eine unbenannte Datei kann nicht gespeichert werden. Geben Sie einen Dateinamen an.                                                                                                       |
| Unbekannter mcierr- \_ \_ Befehl    | Der Treiber kann den angegebenen Befehl nicht erkennen.                                                                                                          |
| nicht unterstützte mcierr- \_ \_ Funktion    | Der angegebene Befehl wird vom MCI-Gerätetreiber, der vom System verwendet wird, nicht unterstützt.                                                                           |



 

 

 