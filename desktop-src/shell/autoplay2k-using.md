---
description: Wenn die Shell das Einfügen neuer Medien oder die Anlage eines Hot-Plug-Geräts erkennt, wird der Inhalt des Geräts oder der Medien bestimmt. Die automatische Wiedergabe führt abhängig von ihren aktuellen Einstellungen eine der folgenden Aufgaben aus.
title: Verwenden und Konfigurieren der automatischen Wiedergabe
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 096c7042-8cf0-4e4f-934f-274564218f4c
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 35de48ee77cde7c598088b3f3877083efc2151f5
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481486"
---
# <a name="using-and-configuring-autoplay"></a>Verwenden und Konfigurieren der automatischen Wiedergabe

Wenn die Shell das Einfügen neuer Medien oder die Anlage eines Hot-Plug-Geräts erkennt, wird der Inhalt des Geräts oder der Medien bestimmt. Die automatische Wiedergabe führt abhängig von ihren aktuellen Einstellungen eine der folgenden Aufgaben aus.

-   Gibt den Inhalt automatisch wieder.
-   Zeigt ein Dialogfeld an, in dem der Benutzer aufgefordert wird, einen Standardhandler für einen einzelnen Inhaltstyp zu wählen.
-   Zeigt im Fall von gemischtem Inhalt eine Liste der verfügbaren Handleranwendungen an, die gestartet werden können. Der ausgewählte Handler gibt dann automatisch den zugeordneten Inhaltstyp wieder.
-   Zeigt eine Standardordneransicht der Dateien an.
-   Führt nichts aus, wenn der  Benutzer zuvor keine Aktion für diesen Inhaltstyp sowie die angegebene **Option Immer die ausgewählte Aktion tun ausgewählt ausgewählt hat.**

Wenn der Inhalt die Kriterien für die automatische Wiedergabe nicht erfüllt, wird das Ereignis an Windows Image Acquisition (WIA) übergeben.

In den folgenden Themen wird die Einrichtung und Verwendung der automatischen Wiedergabe behandelt.

-   [Vorbereiten von Hardware und Software für die Verwendung mit autoplay](#preparing-hardware-and-software-for-use-with-autoplay)
-   [So sucht die automatische Wiedergabe nach Medien](#how-autoplay-searches-media)
-   [Definieren einzelner und gemischter Inhaltstypen](#defining-single-and-mixed-content-types)
-   [Beispielszenarien](#sample-scenarios)
    -   [Automatische Wiedergabe für Storage-Geräte mit Bildmedien](#autoplay-for-storage-devices-with-picture-media)
    -   [AutoPlay for Musik File Playback Devices and Storage Devices Containing Musik Media](#autoplay-for-music-file-playback-devices-and-storage-devices-containing-music-media)
    -   [Automatische Wiedergabe für die Videowiedergabe bei der ersten Präsentation](#autoplay-for-video-playback-on-first-presentation)
-   [Zuweisen von Standardhandleranwendungen](#assigning-default-handler-applications)
-   [Behandeln von Medien mit gemischten Inhaltstypen](#handling-media-containing-mixed-content-types)
-   [Benutzeroberflächen für die automatische Wiedergabe](#autoplay-user-interfaces)
    -   [Einzelner Inhaltstyp (Dialogfeld)](#single-content-type-dialog-box)
    -   [Dialogfeld "Gemischte Medien"](#mixed-media-dialog-box)
    -   [Eigenschaftenseite](#property-page)

## <a name="preparing-hardware-and-software-for-use-with-autoplay"></a>Vorbereiten von Hardware und Software für die Verwendung mit autoplay

In der Registrierung müssen mehrere Informationen angezeigt werden, damit die automatische Wiedergabe funktioniert. Diese Informationen interagieren miteinander und verweisen aufeinander, um die vollständige AutoPlay-Umgebung zu bilden. In diesem Dokument wird die Einrichtung jeder dieser Informationen als einzelne eigenständige Prozedur präsentiert.

Weitere Anweisungen finden Sie in den folgenden Themen.

-   [Zuweisen eines Gerätehandlers zu einem Gerät](how-to-assign-a-device-handler-to-a-device.md)
-   [Angeben eines Symbols, einer Bezeichnung oder eines Gerätehandlers für ein Gerät mithilfe einer Gerätegruppe](how-to-specify-an-icon--label--or-device-handler-for-a-device-using-a-device-group.md)
-   [Angeben eines Symbols, einer Bezeichnung oder eines Gerätehandlers für ein Gerät mithilfe einer Geräteklasse](how-to-specify-an-icon--label--or-device-handler-for-a-device-using-a-device-class.md)
-   [Verhindern der automatischen Wiedergabe für eine Komponente](how-to-prevent-autoplay-for-a-component.md)
-   [Registrieren eines Handlers für ein Geräteereignis](how-to-register-a-handler-for-a-device-event.md)
-   [Verwenden von AutoPlay-Ereignissen in ausgeführten Anwendungen](how-to-use-autoplay-events-in-running-applications.md)
-   [Registrieren eines Ereignishandlers](how-to-register-an-event-handler.md)

## <a name="how-autoplay-searches-media"></a>So sucht die automatische Wiedergabe nach Medien

AutoPlay sucht vier Verzeichnisebenen unterhalb des Stammverzeichnisses nach Medien, um bekannte Dateitypen zu finden. Er verwendet den Wert PerceivedType, der einer Dateierweiterung in der Registrierung zugeordnet ist, um die Dateikategorie zu bestimmen, unabhängig davon, ob es sich um ein Bild, eine Audiodatei oder eine Videodatei handelt. Mit diesen Informationen startet AutoPlay den entsprechenden Handler für das Gerät und den Dateityp. Weitere Informationen finden Sie unter [Wahrgenommene Typen und Anwendungsregistrierung.](fa-perceivedtypes.md)

## <a name="defining-single-and-mixed-content-types"></a>Definieren einzelner und gemischter Inhaltstypen

AutoPlay definiert drei Hauptinhaltskategorien.

-   Bilder
-   Musik
-   Video

Ein Medium enthält einen einzelnen Inhaltstyp, wenn alle Dateien auf dem Medium nur in eine dieser drei Kategorien fallen. Beachten Sie, dass dies nicht bedeutet, dass die Dateien denselben *Dateityp haben* müssen. .jpg, .gif und .bmp sind unterschiedliche Dateitypen, aber ein Inhaltstyp (Bilder).

Wenn unterstützte Inhaltstypen auf dem Medium vorhanden sind, aber kein einzelner Inhaltstyp 100 Prozent der Gesamtsumme berücksichtigen kann, wird das Medium als gemischter Inhaltstyp betrachtet und entsprechend behandelt. Weitere Informationen finden Sie unter [Behandeln von Medien mit gemischten Inhaltstypen.](#handling-media-containing-mixed-content-types)

## <a name="sample-scenarios"></a>Beispielszenarien

Die folgenden Szenarien bieten ein grundlegendes Verständnis dafür, was von autoplay zu erwarten ist.

### <a name="autoplay-for-storage-devices-with-picture-media"></a>Automatische Wiedergabe für Storage-Geräte mit Bildmedien

1.  Der Benutzer fügt ein USB-SanDisk CompactFlash-Readergerät an, für das bereits Medien eingefügt wurden, die den Inhaltstyp 100 % des Bilds in Form von .jpg enthalten.
2.  Die Benachrichtigung zeigt **Found New Hardware – SanDisk ImageMate an.**
3.  AutoPlay startet die entsprechende Imageanwendung.

Wenn der Benutzer dasselbe CompactFlash-Medium in den Reader einfügung, wenn der Reader bereits an das System angefügt ist, führt das Medieneinfügeereignis auch dazu, dass autoPlay die Anwendung der Bildschirmpräsentation startet. Der Benutzer hat die Möglichkeit, zur Seite Eigenschaften des SanDisk-Mediengeräts zu wechseln, um die Standardeinstellung in eine andere registrierte AutoPlay-Anwendung zu ändern, z. B. den Assistenten für Scanner und Kamera oder Picture It!.

### <a name="autoplay-for-music-file-playback-devices-and-storage-devices-containing-music-media"></a>AutoPlay for Musik File Playback Devices and Storage Devices Containing Musik Media

1.  Der Benutzer hängt einen USB Diamond Diamond MP3 Player an.
2.  In der Benachrichtigung **wird Found New Hardware – Diamond Diamond MP3 Player angezeigt.**
3.  AutoPlay gibt die Dateien mithilfe des registrierten Standardhandlers wieder, z. B. Windows Media Player.

Wenn der Benutzer medienverfügbare Medien mit .mp3-Dateien (z. B. CompactFlash, SmartMedia, Memory Stick oder CD-ROM) einträgt, die 100 Prozent des gesamten unterstützten Inhalts in ein Speichergerät einträgt, würde das Medieneinfügeereignis auch dazu führen, dass die Dateien mithilfe des Windows Media Player. Der Benutzer kann auf das Eigenschaftenblatt des Speichergeräts zugreifen und die Standardaktion in eine andere registrierte AutoPlay-Anwendung ändern, z. B. WinAmp oder Real Player.

### <a name="autoplay-for-video-playback-on-first-presentation"></a>Automatische Wiedergabe für die Videowiedergabe bei der ersten Präsentation

1.  Der Benutzer wird zum ersten Mal eine digitale Videokamera aus dem Jahr 1394 anschließen.
2.  Dem Benutzer wird ein einfaches Dialogfeld angezeigt, in dem sie gefragt werden, welche Anwendung ausgeführt werden soll. Sie können eine der registrierten AutoPlay-Anwendungen ausführen oder einen Ordner zum Anzeigen von Dateien öffnen. Der Benutzer kann festlegen, dass das ausgewählte Verhalten als Standardaktion für spätere Hot-Plug-Ereignisse der digitalen Videokamera gespeichert wird.

## <a name="assigning-default-handler-applications"></a>Zuweisen von Standardhandleranwendungen

Bei einer Neuinstallation von Windows autoplay mit einer Reihe registrierter Handleranwendungen gefunden. Anwendungen, die während einer Windows standardmäßig registriert werden, lauten wie folgt.




| Medientyp | Anwendungen | 
|------------|--------------|
| Bilder | <ul><li>Bildschirmpräsentation (Standard)</li><li>Assistent für Kamera und Scanner</li><li>Druck-Assistent</li><li>Ordner öffnen</li></ul> | 
| Musik | <ul><li>Windows Media Player (Standard)</li><li>Ordner öffnen</li></ul> | 
| Video | <ul><li>Windows Media Player (Standard)</li><li>Ordner öffnen</li></ul> | 




 

Bei nicht unterstützten Typen werden Benutzer bei der ersten Einführung in das System aufgefordert, die Standardeinstellung für die AutoPlay-Aktion zu zuweisen, die jedem Speichergerät zugeordnet ist. Zu diesem Zeitpunkt wird der Benutzer aufgefordert, eine Aktion aus einer bereitgestellten Liste registrierter Anwendungen zu wählen oder eine Ordneransicht mit dem Medieninhalt anzuzeigen. Der Benutzer hat auch die Möglichkeit, jedes Mal, wenn der Medientyp erkannt wird, dazu aufgefordert zu werden, anstatt eine bestimmte Anwendung als Standard zu speichern.

> [!Note]  
> Gerätehersteller haben die Möglichkeit, Standardanwendungen zu registrieren und zu zuweisen, die mit ihren jeweiligen Produkten verwendet werden sollen. In diesen Fällen wird das Dialogfeld, das dem Benutzer eine Auswahl bietet, nicht angezeigt.

 

Um von AutoPlay als Handleroption angeboten zu werden, müssen sich neu installierte Anwendungen selbst in der Registrierung registrieren. Weitere Informationen finden Sie unter Preparing Hardware and Software for Use with AutoPlay (Vorbereiten von Hardware und [Software für die Verwendung mit autoplay).](#preparing-hardware-and-software-for-use-with-autoplay)

Benutzer können den Standardmäßigen AutoPlay-Handler für jedes Speichergerät oder jeden Inhaltstyp jederzeit ändern. Auf die Eigenschaftenseite "AutoPlay" kann im Eigenschaftenblatt des Speichergeräts **in** der Arbeitsplatz.

Beispiele für Benutzeraufforderungen und Eigenschaftenseiten finden Sie unter [AutoPlay User Interfaces](#autoplay-user-interfaces).

## <a name="handling-media-containing-mixed-content-types"></a>Behandeln von Medien mit gemischten Inhaltstypen

Wenn autoplay mit einem gemischten Inhaltsmedium dargestellt wird, ist eine Benutzereingabe erforderlich, bevor Maßnahmen ergreifen werden können. In diesem Fall wird dem Benutzer ein Dialogfeld mit einer gefilterten Liste aller entsprechenden registrierten Anwendungen angezeigt, die für die auf den Medien vorhandenen Inhaltstypen verfügbar sind. Der Benutzer kann eine dieser Anwendungen auswählen, um diesen bestimmten Inhaltstyp automatisch wiederzugeben, während der Rest unverändert bleibt. Da die Zusammensetzung gemischter Inhaltsmedien mit den einzelnen Datenträgern variiert, gibt es keine Option, diese Auswahl als Standard zu speichern.

Beispiele für Benutzereingabeaufforderungen finden Sie unter Benutzeroberflächen für [die automatische Wiedergabe.](#autoplay-user-interfaces)

## <a name="autoplay-user-interfaces"></a>Benutzeroberflächen für die automatische Wiedergabe

Es gibt drei mögliche Benutzeroberflächen.

-   Ein Dialogfeld, in dem der Benutzer aufgefordert wird, eine Aktion für einen einzelnen Inhaltstyp einzugeben
-   Ein Dialogfeld, in dem der Benutzer aufgefordert wird, eine Aktion für gemischte Inhaltstypen einzugeben.
-   Eine Eigenschaftenseite

### <a name="single-content-type-dialog-box"></a>Einzelner Inhaltstyp (Dialogfeld)

Ein Dialogfeld ähnlich dem folgenden wird angezeigt, wenn dem System ein unterstütztes Medium angezeigt wird, dem noch keine Standardaktion für die automatische Wiedergabe zugewiesen ist.

![Screenshot des Dialogfelds "Einzelner Inhaltstyp"](images/pix.png)

Benutzer können eine der folgenden Schritte ausführen.

-   Wählen Sie eine Aktion aus der Liste der registrierten Anwendungen aus.
-   Listen Sie die Dateien auf dem Medium in einer normalen Ordneransicht auf.
-   Führen Sie keine Aktion aus.

Ein Benutzer kann eine Auswahl auch als Standardaktion für dieses Medium speichern, indem er auf das Feld **Ausgewählte Aktion immer durchführen** klickt. Sobald diese Auswahl getroffen wurde, wird das Dialogfeld nicht mehr angezeigt. Wenn dem Computer jedoch in Windows XP Service Pack 1 (SP1) eine neue Anwendung hinzugefügt wird, die einen bestimmten Medientyp verarbeiten kann, wird dem Benutzer das Dialogfeld erneut angezeigt, sodass er die neue Anwendung als Standardaktion für die automatische Wiedergabe auswählen kann. Anwendungen können sich auch selbst als Standardauswahl festlegen, wenn sie installiert werden.

Windows XP SP1 fügt auch ein Feature hinzu, das die Auswahl der AutoPlay-Aktion des Benutzers beibehält, wenn er nicht auf das Feld **Always do the selected action (Immer die ausgewählte Aktion durchführen)** klickt. Wenn ein Benutzer eine AutoPlay-Aktion für eine einzelne Instanz ausgibt, ist die gleiche Aktion die Standardauswahl, wenn dieses Dialogfeld das nächste Mal für diesen Medientyp angezeigt wird.

Damit eine Anwendung in die Liste der möglichen Aktionen aufgenommen werden kann, muss sie bei AutoPlay registriert werden. Weitere Informationen finden Sie unter [Preparing Hardware and Software for Use with AutoPlay](#preparing-hardware-and-software-for-use-with-autoplay).

### <a name="mixed-media-dialog-box"></a>Dialogfeld "Gemischte Medien"

Das folgende Dialogfeld wird angezeigt, wenn ein Medium, das eine Mischung aus unterstützten Dateitypen enthält, dem System angezeigt wird. Dies ist im Wesentlichen identisch mit dem dialogfeld "Medium für einzelnen Inhalt", jedoch mit zwei signifikanten Unterschieden. Zunächst bestehen die verfügbaren Aktionsoptionen aus einer gefilterten Liste von Anwendungen, die für alle inhaltstypen relevant sind, die auf dem Medium vorhanden sind. Zweitens gibt es keine Option zum Auswählen einer permanenten Standardaktion, da die Inhaltstypen und Prozentsätze gemischter Inhaltsmedien zu unvorhersehbar sind.

![Screenshot des Dialogfelds "Gemischte Medien"](images/mix.png)

Damit eine Anwendung in die Liste der möglichen Aktionen aufgenommen werden kann, muss sie bei AutoPlay registriert werden. Weitere Informationen finden Sie unter [Preparing Hardware and Software for Use with AutoPlay](#preparing-hardware-and-software-for-use-with-autoplay).

### <a name="property-page"></a>Eigenschaftenseite

Im Folgenden finden Sie eine Beispieleigenschaftenseite für die automatische Wiedergabe für ein DVD-/CD-ROM-Gerät.

![Screenshot der Eigenschaftenseite](images/apdlg.png)

Jeder Gerätetyp bietet eine geeignete Teilmenge von Inhaltstypen für die Konfiguration der automatischen Wiedergabe. Im Gegenzug bietet jeder Inhaltstyp, wenn er ausgewählt ist, eine entsprechende Liste von Aktionsoptionen im Listenfeld. Für jeden Inhaltstyp kann eine andere Aktion ausgewählt werden.

 

 



