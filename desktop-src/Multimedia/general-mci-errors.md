---
title: Allgemeine MCI-Fehler
description: Allgemeine MCI-Fehler
ms.assetid: be9c4a2b-44bc-410c-be74-ba55bb4e785b
keywords:
- MCIERR-Rückgabewerte, allgemeine Fehler
- Multimediareferenz, MCI-Fehler
- Referenz zu Multimediafehlern, MCI-Fehlern
- Media Control Interface (MCI), allgemeine Fehler
- MCI (Media Control Interface), allgemeine Fehler
- Referenz zu MCI,allgemeine Fehler
- MCI-Referenz, allgemeine Fehler
- Media Control Interface (MCI), Fehler
- MCI (Media Control Interface), Fehler
- Referenz für MCI, Fehler
- MCI-Referenz, Fehler
- mciSendCommand-Funktion
- mciSendString-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f6f402e532f1bcf22a9136764647c91b1f4d54479f932c509ec172c1d973f4a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118375157"
---
# <a name="general-mci-errors"></a>Allgemeine MCI-Fehler

Die folgenden Fehlerwerte können entweder von der [**mciSendCommand-**](/previous-versions//dd757160(v=vs.85)) oder [**mciSendString-Funktion**](/previous-versions//dd757161(v=vs.85)) zurückgegeben werden:



| Wert                            | Bedeutung                                                                                                                                                     |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MCIERR: \_ UNGÜLTIGES \_ \_ ZEITFORMAT        | Der angegebene Wert für das Zeitformat ist ungültig.                                                                                                         |
| MCIERR \_ KANN TREIBER NICHT \_ LADEN \_     | Der angegebene Gerätetreiber wird nicht ordnungsgemäß geladen.                                                                                                         |
| MCIERR \_ KANN NICHT \_ ALLE VERWENDEN \_         | Der Gerätename "all" ist für diesen Befehl nicht zulässig.                                                                                                      |
| MCIERR \_ CREATEWINDOW             | Das Fenster konnte nicht erstellt oder verwendet werden.                                                                                                                             |
| \_MCIERR-GERÄTELÄNGE \_           | Der Name des Geräts oder Treibers ist zu lang. Geben Sie einen Geräte- oder Treibernamen an, der kleiner als 79 Zeichen ist.                                                     |
| \_MCIERR-GERÄT \_ GESPERRT           | Das Gerät wird nun geschlossen. Warten Sie einige Sekunden, und versuchen Sie es erneut.                                                                                         |
| \_MCIERR-GERÄT \_ NICHT \_ INSTALLIERT   | Das angegebene Gerät ist nicht auf dem System installiert. Verwenden Sie die Option Treiber aus dem Systemsteuerung, um das Gerät zu installieren.                                   |
| \_MCIERR-GERÄT \_ NICHT \_ BEREIT       | Der Gerätetreiber ist nicht bereit.                                                                                                                             |
| MCIERR \_ DEVICE \_ OPEN             | Der Gerätename wird von dieser Anwendung bereits als Alias verwendet. Verwenden Sie einen eindeutigen Alias.                                                                        |
| MCIERR \_ DEVICE \_ ORD \_ LENGTH      | Der Name des Geräts oder Treibers ist zu lang. Geben Sie einen Geräte- oder Treibernamen an, der kleiner als 79 Zeichen ist.                                                     |
| \_MCIERR-GERÄTETYP \_ \_ ERFORDERLICH   | Das angegebene Gerät kann auf dem System nicht gefunden werden. Überprüfen Sie, ob das Gerät installiert ist und der Gerätename richtig geschrieben ist.                            |
| \_MCIERR-TREIBER                   | Der Gerätetreiber weist ein Problem auf. Informieren Sie sich beim Gerätehersteller über den Erhalt eines neuen Treibers.                                                      |
| \_MCIERR-TREIBER \_ INTERN         | Der Gerätetreiber weist ein Problem auf. Informieren Sie sich beim Gerätehersteller über den Erhalt eines neuen Treibers.                                                      |
| MCIERR \_ DUPLICATE \_ ALIAS         | Der angegebene Alias wird bereits in dieser Anwendung verwendet. Verwenden Sie einen eindeutigen Alias.                                                                                |
| \_MCIERR-ERWEITERUNG \_ NICHT \_ GEFUNDEN    | Der angegebenen Erweiterung ist kein Gerätetyp zugeordnet. Geben Sie einen Gerätetyp an.                                                                       |
| \_ZUSÄTZLICHE \_ MCIERR-ZEICHEN        | Sie müssen eine Zeichenfolge in Anführungszeichen einschließen. Zeichen, die auf das schließende Anführungszeichen folgen, sind ungültig.                                              |
| \_MCIERR-DATEI \_ NICHT \_ GEFUNDEN         | Die angeforderte Datei wurde nicht gefunden. Überprüfen Sie, ob der Pfad und der Dateiname korrekt sind.                                                                             |
| \_MCIERR-DATEI \_ NICHT \_ GESPEICHERT         | Die Datei wurde nicht gespeichert. Stellen Sie sicher, dass Ihr System über ausreichend Speicherplatz oder eine intakte Netzwerkverbindung verfügt.                                                |
| MCIERR \_ FILE \_ READ               | Fehler beim Lesen aus der Datei. Stellen Sie sicher, dass die Datei auf Ihrem System vorhanden ist oder dass ihr System über eine intakte Netzwerkverbindung verfügt.                             |
| MCIERR \_ FILE \_ WRITE              | Fehler beim Schreiben in die Datei. Stellen Sie sicher, dass Ihr System über ausreichend Speicherplatz oder eine intakte Netzwerkverbindung verfügt.                                            |
| MCIERR \_ FILENAME \_ ERFORDERLICH       | Der Dateiname ist ungültig. Stellen Sie sicher, dass der Dateiname nicht länger als acht Zeichen ist, gefolgt von einem Punkt und einer Erweiterung.                                  |
| \_MCIERR-FLAGS \_ SIND NICHT \_ KOMPATIBEL   | Die angegebenen Parameter können nicht zusammen verwendet werden.                                                                                                           |
| MCIERR \_ GET \_ CD                  | Das angeforderte Datei- ODER MCI-Gerät wurde nicht gefunden. Versuchen Sie, Verzeichnisse zu ändern oder Ihr System neu zu starten.                                                         |
| MCIERR \_ HARDWARE                 | Das angegebene Gerät weist ein Problem auf. Überprüfen Sie, ob das Gerät ordnungsgemäß funktioniert, oder wenden Sie sich an den Gerätehersteller.                                     |
| MCIERR \_ ILLEGAL \_ FOR \_ AUTO \_ OPEN | MCI führt den angegebenen Befehl nicht auf einem automatisch geöffneten Gerät aus. Warten Sie, bis das Gerät geschlossen ist, und versuchen Sie dann, den Befehl auszuführen.             |
| MCIERR \_ INTERNAL                 | Beim Initialisieren von MCI ist ein Problem aufgetreten. Versuchen Sie, das Windows Betriebssystem neu zu starten.                                                                        |
| \_UNGÜLTIGE \_ MCIERR-GERÄTE-ID \_      | Ungültige Geräte-ID. Verwenden Sie die ID, die dem Gerät beim Öffnen des Geräts angegeben wurde.                                                                               |
| UNGÜLTIGER \_ \_ MCIERR-GERÄTENAME \_    | Das angegebene Gerät ist nicht geöffnet und wird von MCI nicht erkannt.                                                                                                     |
| \_UNGÜLTIGE \_ MCIERR-DATEI            | Die angegebene Datei kann nicht auf dem angegebenen MCI-Gerät wiedergegeben werden. Die Datei ist möglicherweise beschädigt oder verwendet möglicherweise ein falsches Dateiformat.                               |
| MCIERR \_ MISSING \_ PARAMETER       | Der angegebene Befehl erfordert einen Parameter, den Sie angeben müssen.                                                                                          |
| MCIERR \_ MULTIPLE                 | Fehler sind auf mehr als einem Gerät aufgetreten. Geben Sie jeden Befehl und jedes Gerät separat an, um die Geräte zu identifizieren, die die Fehler verursachen.                             |
| MCIERR \_ MUSS \_ \_ FREIGABEFÄHIG VERWENDEN     | Der Gerätetreiber wird bereits verwendet. Sie müssen den Parameter "sharable" mit jedem geöffneten Befehl angeben, um das Gerät frei zu geben.                                  |
| MCIERR: \_ KEIN \_ ELEMENT \_ ZULÄSSIG     | Das angegebene Gerät verwendet keinen Dateinamen.                                                                                                               |
| MCIERR \_ NO \_ INTEGER              | Der Parameter für diesen MCI-Befehl muss ein ganzzahliger Wert sein.                                                                                                |
| MCIERR \_ KEIN \_ FENSTER               | Es gibt kein Anzeigefenster.                                                                                                                                 |
| NICHT APPLIZIERBARE \_ MCIERR-FUNKTION \_  | Die angegebene MCI-Befehlssequenz kann nicht in der angegebenen Reihenfolge ausgeführt werden. Korrigieren Sie die Befehlssequenz. Versuchen Sie es dann erneut.                                   |
| MCIERR \_ NULL \_ PARAMETER \_ BLOCK   | Ein NULL-Parameterblock (Struktur) wurde an MCI übergeben.                                                                                                       |
| MCIERR \_ NICHT \_ GENÜGEND \_ ARBEITSSPEICHER          | Ihr System verfügt nicht über genügend Arbeitsspeicher für diese Aufgabe. Beenden Sie eine oder mehrere Anwendungen, um den verfügbaren Arbeitsspeicher zu erhöhen, und versuchen Sie dann erneut, die Aufgabe auszuführen. |
| MCIERR \_ OUTOFRANGE               | Der angegebene Parameterwert liegt für den angegebenen MCI-Befehl nicht im Bereich.                                                                                |
| MCIERR \_ SET \_ CD                  | Auf die angegebene Datei oder das MCI-Gerät kann nicht zugegriffen werden, da die Anwendung die Verzeichnisse nicht ändern kann.                                                         |
| MCIERR \_ SET \_ DRIVE               | Auf die angegebene Datei oder das MCI-Gerät kann nicht zugegriffen werden, da die Anwendung die Laufwerke nicht ändern kann.                                                              |
| UNBENANNTE \_ MCIERR-RESSOURCE \_        | Sie können keine unbenannte Datei speichern. Geben Sie einen Dateinamen an.                                                                                                       |
| MCIERR \_ UNRECOGNIZED \_ COMMAND    | Der Treiber kann den angegebenen Befehl nicht erkennen.                                                                                                          |
| NICHT UNTERSTÜTZTE \_ MCIERR-FUNKTION \_    | Der MCI-Gerätetreiber, den das System verwendet, unterstützt den angegebenen Befehl nicht.                                                                           |



 

 

 