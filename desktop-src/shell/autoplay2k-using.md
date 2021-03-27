---
description: Wenn die Shell das Einfügen neuer Medien oder die Anlage eines Hot-Plug-Geräts erkennt, wird der Inhalt des Geräts oder der Medien bestimmt. Die automatische Wiedergabe führt in Abhängigkeit von den aktuellen Einstellungen eine der folgenden Bedingungen aus.
title: Verwenden und Konfigurieren von AutoPlay
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 096c7042-8cf0-4e4f-934f-274564218f4c
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 04a4f6dd09e03f26b13649e860beb7f2621ce952
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750304"
---
# <a name="using-and-configuring-autoplay"></a>Verwenden und Konfigurieren von AutoPlay

Wenn die Shell das Einfügen neuer Medien oder die Anlage eines Hot-Plug-Geräts erkennt, wird der Inhalt des Geräts oder der Medien bestimmt. Die automatische Wiedergabe führt in Abhängigkeit von den aktuellen Einstellungen eine der folgenden Bedingungen aus.

-   Gibt den Inhalt automatisch wieder.
-   Zeigt ein Dialogfeld an, in dem der Benutzer zur Auswahl eines Standard Handlers für einen einzelnen Inhaltstyp aufgefordert wird.
-   Zeigt eine Liste der verfügbaren handleranwendungen an, die im Fall gemischter Inhalte angezeigt werden. Der ausgewählte Handler übernimmt dann automatisch den zugehörigen Inhaltstyp.
-   Zeigt eine Standardordner Ansicht der Dateien an.
-   Führt keine Aktion aus, wenn der Benutzer zuvor **keine Aktion** für diesen Inhaltstyp ausführen und **die Option immer die ausgewählte Aktion** ausführen ausgewählt hat.

Wenn der Inhalt die Kriterien für die automatische Wiedergabe nicht erfüllt, wird das Ereignis an die Windows-Abbild Beschaffung (WIA) weitergegeben.

In den folgenden Themen wird das Setup und die Verwendung von AutoPlay erläutert.

-   [Vorbereiten von Hardware und Software für die Verwendung mit Autoplay](#preparing-hardware-and-software-for-use-with-autoplay)
-   [Suchen von Medien durch AutoPlay](#how-autoplay-searches-media)
-   [Definieren von einzelnen und gemischten Inhaltstypen](#defining-single-and-mixed-content-types)
-   [Beispielszenarien](#sample-scenarios)
    -   [AutoPlay für Speichergeräte mit Bildmedien](#autoplay-for-storage-devices-with-picture-media)
    -   [Automatische Wiedergabe von Musikdateien und Speichergeräten mit Musik Medien](#autoplay-for-music-file-playback-devices-and-storage-devices-containing-music-media)
    -   [AutoPlay für die Video Wiedergabe bei der ersten Präsentation](#autoplay-for-video-playback-on-first-presentation)
-   [Zuweisen von standardhandleranwendungen](#assigning-default-handler-applications)
-   [Verarbeiten von Medien mit gemischten Inhaltstypen](#handling-media-containing-mixed-content-types)
-   [Wiedergabe von Benutzeroberflächen](#autoplay-user-interfaces)
    -   [Dialog Feld "einzelner Inhaltstyp"](#single-content-type-dialog-box)
    -   [Dialog Feld ' Gemischte Medien '](#mixed-media-dialog-box)
    -   [Eigenschaftenseite](#property-page)

## <a name="preparing-hardware-and-software-for-use-with-autoplay"></a>Vorbereiten von Hardware und Software für die Verwendung mit Autoplay

Mehrere Informationen müssen in der Registrierung angezeigt werden, damit die automatische Wiedergabe funktioniert. Diese Informationen interagieren und verweisen aufeinander, um die vollständige AutoPlay-Umgebung zu bilden. In diesem Dokument wird das Einrichten der einzelnen Informationen als einzelner eigenständiger Vorgang dargestellt.

Weitere Anweisungen finden Sie in den folgenden Themen.

-   [Zuweisen eines Geräte Handlers zu einem Gerät](how-to-assign-a-device-handler-to-a-device.md)
-   [Angeben eines Symbols, einer Bezeichnung oder eines Geräte Handlers für ein Gerät mithilfe einer Gerätegruppe](how-to-specify-an-icon--label--or-device-handler-for-a-device-using-a-device-group.md)
-   [Angeben eines Symbols, einer Bezeichnung oder eines Geräte Handlers für ein Gerät mithilfe einer Geräteklasse](how-to-specify-an-icon--label--or-device-handler-for-a-device-using-a-device-class.md)
-   [Verhindern von AutoPlay für eine Komponente](how-to-prevent-autoplay-for-a-component.md)
-   [Registrieren eines Handlers für ein Geräte Ereignis](how-to-register-a-handler-for-a-device-event.md)
-   [Verwenden von AutoPlay-Ereignissen in laufenden Anwendungen](how-to-use-autoplay-events-in-running-applications.md)
-   [Registrieren eines Ereignis Handlers](how-to-register-an-event-handler.md)

## <a name="how-autoplay-searches-media"></a>Suchen von Medien durch AutoPlay

Bei der automatischen Suche werden Medien mit vier Verzeichnis Ebenen unter dem Stammverzeichnis gesucht, um bekannte Dateitypen zu suchen. Er verwendet den Wert "wahrnehmvedtype", der einer Dateinamenerweiterung in der Registrierung zugeordnet ist, um die Datei Kategorie zu bestimmen, ob es sich um ein Bild, eine Audiodatei oder eine Videodatei handelt. Mit diesen Informationen wird durch die automatische Wiedergabe der entsprechende Handler für das Gerät und den Dateityp gestartet. Weitere Informationen finden Sie unter [wahrgenommene Typen und Anwendungs Registrierung](fa-perceivedtypes.md).

## <a name="defining-single-and-mixed-content-types"></a>Definieren von einzelnen und gemischten Inhaltstypen

Die Autoplay definiert drei Hauptinhalts Kategorien.

-   Bilder
-   Musik
-   Video

Ein Medium wird als einzelner Inhaltstyp betrachtet, wenn alle Dateien auf dem Medium nur in eine dieser drei Kategorien fallen. Beachten Sie, dass dies nicht bedeutet, dass die Dateien denselben *Dateityp* aufweisen müssen. jpg, GIF und BMP sind unterschiedliche Dateitypen, aber ein Inhaltstyp (Bilder).

Wenn unterstützte Inhaltstypen auf dem Medium vorhanden sind, aber kein einzelner Inhaltstyp 100 Prozent der Gesamtsumme berücksichtigen kann, wird das Medium als gemischter Inhaltstyp angesehen und entsprechend behandelt. Weitere Informationen finden Sie unter [Verarbeiten von Medien, die gemischte Inhaltstypen enthalten](#handling-media-containing-mixed-content-types).

## <a name="sample-scenarios"></a>Beispielszenarien

In den folgenden Szenarien wird erläutert, was von der automatischen Wiedergabe zu erwarten ist.

### <a name="autoplay-for-storage-devices-with-picture-media"></a>AutoPlay für Speichergeräte mit Bildmedien

1.  Der Benutzer fügt ein USB-Gerät mit einem USB-Lese Gerät an, auf das bereits ein Medium eingefügt wurde, das 100% Bild Inhaltstyp in Form von JPG-Dateien enthält.
2.  Benachrichtigung zeigt **neue Hardware-SanDisk ImageMate gefunden**.
3.  Die automatische Abbild Anwendung wird von der automatischen Wiedergabe gestartet

Analog dazu bewirkt das Medien Einfügungs Ereignis auch dann, dass das Media INSERT-Ereignis zum Starten der Bild Folie Show-Anwendung eine automatische Wiedergabe der Bild Folie anzeigt, wenn der Benutzer das gleiche "CompactFlash"-Medium in den Reader einfügt. Der Benutzer hat die Möglichkeit, auf der Seite "Eigenschaften" des SanDisk Media-Geräts den Standardwert in eine andere registrierte AutoPlay-Anwendung zu ändern, wie z. b. den Scanner für Scanner und Kameras.

### <a name="autoplay-for-music-file-playback-devices-and-storage-devices-containing-music-media"></a>Automatische Wiedergabe von Musikdateien und Speichergeräten mit Musik Medien

1.  Der Benutzer fügt einen USB-Diamant-MP3-Player an.
2.  In der Benachrichtigung **finden Sie neue Hardware-Diamant Rio MP3 Player**.
3.  AutoPlay gibt die Dateien mithilfe Ihres registrierten Standard Handlers wieder – beispielsweise Windows Media Player.

Wenn der Benutzer beispielsweise ein Medium mit. MP3-Dateien (z. b. "CompactFlash", "SmartMedia", "Memory Stick" oder CD-ROM) einfügt, das 100 Prozent der gesamten unterstützten Inhalte in ein Speichergerät einfügt, würde das Media INSERT-Ereignis auch zur Wiedergabe der Dateien mit dem Windows-Media Player führen. Der Benutzer kann auf das Eigenschaften Blatt des Speichergeräts zugreifen und die Standardaktion in eine andere registrierte AutoPlay-Anwendung wie z. b. "Winamp" oder "Real Player" ändern.

### <a name="autoplay-for-video-playback-on-first-presentation"></a>AutoPlay für die Video Wiedergabe bei der ersten Präsentation

1.  Der Benutzer ist zum ersten Mal eine digitale 1394-Videokamera angeschlossen.
2.  Dem Benutzer wird ein einfaches Dialogfeld angezeigt, in dem Sie gefragt werden, welche Anwendung ausgeführt werden soll. Die Auswahl besteht darin, eine der registrierten AutoPlay-Anwendungen auszuführen oder einen Ordner zum Anzeigen von Dateien zu öffnen. Der Benutzer kann das ausgewählte Verhalten so festlegen, dass es als Standardaktion für spätere Hot-Plug-Ereignisse der digitalen Videokamera gespeichert wird.

## <a name="assigning-default-handler-applications"></a>Zuweisen von standardhandleranwendungen

Eine Neuinstallation von Windows findet eine automatische Wiedergabe mit einem Satz registrierter handleranwendungen. Anwendungen, die während einer Windows-Installation standardmäßig registriert sind, lauten wie folgt.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Medientyp</th>
<th>Anwendungen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Bilder</td>
<td><ul>
<li>Folien Anzeige (Standard)</li>
<li>Kamera-und Scanner-Assistent</li>
<li>Druck-Assistent</li>
<li>Ordner öffnen</li>
</ul></td>
</tr>
<tr class="even">
<td>Musik</td>
<td><ul>
<li>Windows-Media Player (Standard)</li>
<li>Ordner öffnen</li>
</ul></td>
</tr>
<tr class="odd">
<td>Video</td>
<td><ul>
<li>Windows-Media Player (Standard)</li>
<li>Ordner öffnen</li>
</ul></td>
</tr>
</tbody>
</table>



 

Bei nicht unterstützten Typen werden Benutzer aufgefordert, die Standardeinstellung für die Autoplay-Aktion zuzuweisen, die den einzelnen Speichergeräten bei der ersten Einführung in das System zugeordnet ist. Zu diesem Zeitpunkt wird der Benutzer aufgefordert, eine Aktion aus einer bereitgestellten Liste registrierter Anwendungen auszuwählen oder eine Ordneransicht anzuzeigen, in der der Medieninhalt aufgelistet ist. Der Benutzer hat auch die Möglichkeit, jedes Mal, wenn der Medientyp erkannt wird, aufgefordert zu werden, anstatt eine bestimmte Anwendung als Standard zu speichern.

> [!Note]  
> Gerätehersteller können Standardanwendungen registrieren und zuweisen, die für ihre jeweiligen Produkte verwendet werden sollen. In diesen Fällen wird das Dialogfeld, das dem Benutzer eine Auswahl bietet, nicht angezeigt.

 

Um von der automatischen Wiedergabe als handleroption angeboten zu werden, müssen sich neu installierte Anwendungen selbst in der Registrierung registrieren. Weitere Informationen finden Sie unter [Vorbereiten von Hardware und Software für die Verwendung mit Autoplay](#preparing-hardware-and-software-for-use-with-autoplay).

Benutzer können den standardmäßigen AutoPlay-Handler für beliebige Speichergeräte oder Inhaltstyp jederzeit ändern. Der Zugriff auf die Eigenschaften Seite "AutoPlay" kann im Eigenschaften Blatt des Speichergeräts in **Arbeitsplatz** geändert werden.

Beispiele für Benutzer Aufforderungen und Eigenschaften Seiten finden Sie unter [AutoPlay User Interfaces](#autoplay-user-interfaces).

## <a name="handling-media-containing-mixed-content-types"></a>Verarbeiten von Medien mit gemischten Inhaltstypen

Wenn die automatische Wiedergabe mit einem gemischten Inhalts Medium erfolgt, ist eine Benutzereingabe erforderlich, bevor Sie Maßnahmen ergreifen kann. In diesem Fall wird dem Benutzer ein Dialogfeld angezeigt, das eine gefilterte Liste aller entsprechenden registrierten Anwendungen enthält, die für die auf dem Medium vorhandenen Inhaltstypen verfügbar sind. Der Benutzer kann eine dieser Anwendungen auswählen, um diesen bestimmten Inhaltstyp zu wiedergeben, während der Rest unverändert bleibt. Wenn die Komposition gemischter Inhalts Medien mit den einzelnen einzelnen CDs variiert, ist es nicht möglich, diese Auswahl als Standard zu speichern.

Beispiele für Benutzer Aufforderungen finden Sie unter [AutoPlay User Interfaces](#autoplay-user-interfaces).

## <a name="autoplay-user-interfaces"></a>Wiedergabe von Benutzeroberflächen

Es gibt drei mögliche Benutzeroberflächen.

-   Ein Dialogfeld, in dem der Benutzer aufgefordert wird, eine Aktion für einen einzelnen Inhaltstyp einzugeben.
-   Ein Dialogfeld, in dem der Benutzer aufgefordert wird, eine Aktion für gemischte Inhaltstypen einzugeben
-   Eine Eigenschaften Seite

### <a name="single-content-type-dialog-box"></a>Dialog Feld "einzelner Inhaltstyp"

Ein Dialogfeld ähnlich dem folgenden wird angezeigt, wenn ein unterstütztes Medium, dem noch keine Standardaktion für die automatische Wiedergabe zugewiesen wurde, dem System angezeigt wird.

![Screenshot des Dialog Felds "einzelner Inhaltstyp"](images/pix.png)

Benutzer können eine der folgenden Aktionen ausführen:

-   Wählen Sie in der Liste der registrierten Anwendungen eine Aktion aus.
-   Listet die Dateien auf dem Medium in einer normalen Ordneransicht auf.
-   Führen Sie keine Aktion aus.

Ein Benutzer kann auch eine Auswahl als Standardaktion für dieses Medium speichern, indem Sie auf das Feld **ausgewählte Aktion immer** ausführen klicken. Nachdem diese Auswahl getroffen wurde, wird das Dialogfeld nicht mehr angezeigt. Wenn jedoch in Windows XP Service Pack 1 (SP1) eine neue Anwendung, die einen bestimmten Medientyp verarbeiten kann, dem Computer hinzugefügt wird, wird das Dialogfeld dem Benutzer erneut angezeigt, sodass die neue Anwendung als Standardaktion für die automatische Wiedergabe ausgewählt werden kann. Anwendungen können sich auch selbst als Standardauswahl festlegen, wenn Sie installiert werden.

Windows XP SP1 fügt auch eine Funktion hinzu, die die Auswahl der Aktion für die automatische Wiedergabe durch den Benutzer beibehält, wenn Sie nicht auf das Feld **ausgewählte Aktion immer** ausführen klicken. Wenn ein Benutzer eine Autoplay-Aktion für eine einzelne Instanz auswählt, wird bei der nächsten Anzeige des Dialog Felds für den Medientyp dieselbe Aktion als Standardauswahl angezeigt.

Damit eine Anwendung in die Liste der möglichen Aktionen eingeschlossen werden kann, muss Sie bei der automatischen Wiedergabe registriert werden. Weitere Informationen finden Sie unter [Vorbereiten von Hardware und Software für die Verwendung mit Autoplay](#preparing-hardware-and-software-for-use-with-autoplay).

### <a name="mixed-media-dialog-box"></a>Dialog Feld ' Gemischte Medien '

Das folgende Dialogfeld wird angezeigt, wenn ein Medium, das eine Mischung aus unterstützten Dateitypen enthält, dem System angezeigt wird. Dies ist im Wesentlichen das gleiche wie das einzelne Inhalts Medium (Dialogfeld), jedoch mit zwei signifikanten Unterschieden. Zuerst bestehen die verfügbaren Aktions Optionen aus einer gefilterten Liste von Anwendungen, die für alle auf dem Medium vorhandenen Inhaltstypen relevant sind. Zweitens gibt es keine Option zum Auswählen einer permanenten Standardaktion, da die Inhaltstypen und Prozentsätze gemischter Inhalts Medien zu unvorhersehbar sind.

![Screenshot des Dialog Felds "Gemischte Medien"](images/mix.png)

Damit eine Anwendung in die Liste der möglichen Aktionen eingeschlossen werden kann, muss Sie bei der automatischen Wiedergabe registriert werden. Weitere Informationen finden Sie unter [Vorbereiten von Hardware und Software für die Verwendung mit Autoplay](#preparing-hardware-and-software-for-use-with-autoplay).

### <a name="property-page"></a>Eigenschaftenseite

Im folgenden finden Sie ein Beispiel für eine Autoplay-Eigenschaften Seite für ein DVD/CD-ROM-Gerät.

![Screenshot der Eigenschaften Seite](images/apdlg.png)

Jeder Gerätetyp bietet eine geeignete Teilmenge der Inhaltstypen für die automatische Konfiguration. Jeder Inhaltstyp, wenn er ausgewählt wird, bietet wiederum eine passende Liste von Aktions Optionen im Listenfeld. Für jeden Inhaltstyp kann eine andere Aktion ausgewählt werden.

 

 



