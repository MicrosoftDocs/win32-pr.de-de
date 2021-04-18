---
title: Befehl "setvideo"
description: Der setvideo-Befehl legt Werte fest, die der Videowiedergabe und-Erfassung zugeordnet sind. Dieser Befehl wird von Digital-Video-und VCR-Geräten erkannt.
ms.assetid: a6851b9b-e09a-4251-bd1c-19b1e4b6f871
keywords:
- Befehl "setvideo" Windows Multimedia
topic_type:
- apiref
api_name:
- setvideo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fa4c3d1e3b90b9ab0c5bf5791dacd541c8a8bc0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392003"
---
# <a name="setvideo-command"></a>Befehl "setvideo"

Der setvideo-Befehl legt Werte fest, die der Videowiedergabe und-Erfassung zugeordnet sind. Dieser Befehl wird von Digital-Video-und VCR-Geräten erkannt.

Um diesen Befehl zu senden, wenden Sie die [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion mit dem festgelegten *lpszcommand* -Parameter wie folgt an.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("setvideo %s %s %s"), 
  lpszDeviceID, 
  lpszVideo, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszde viceid*
</dt> <dd>

Der Bezeichner eines MCI-Geräts. Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.

</dd> <dt>

<span id="lpszVideo"></span><span id="lpszvideo"></span><span id="LPSZVIDEO"></span>*lpszvideo*
</dt> <dd>

Flag für die Videowiedergabe und-Erfassung. In der folgenden Tabelle sind die Gerätetypen aufgeführt, die den Befehl **setvideo** und die von den einzelnen Typen verwendeten Flags erkennen.



| Wert        | Bedeutung                                                                                                                                                                                        | Bedeutung                                                                                                                                                                                                                                                                                                |
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Digitalvideo | *algorithmusalgorithmus* BitsPerPel *zum zählen* von Helligkeit zum *Faktor* clocktimecolor *, um den Kontrast zu* *Faktor Gamma zu* bewerten, um den *Wert* von "halftoneinputkey" in " *r:g: b* Key Index to *Index* offonoutput" zu verarbeiten | over *Duration* Palette Farb *Farbe* über *Index* zum *newrgb* -Palettenhandle, *um die* Framerate *des Qualitäts* *Deskriptors* zu *verarbeiten*, um die Daten Satz offschärfe zu bewerten *, um den* *Wert* *für* *die Quelle der Quellnummer* zu *bewerten*  |
| VCR          | offonmonitor zum *eingeben* der *Anzahl von Daten Satz Daten* Satz-Nachverfolgung *nachverfolgen \_*                                                                                                               | Aufzeichnen der onrecord-Track-Spur- *\_ Nummer* onsource in den *Typ* Nummer *Number* *Nachverfolgen der \_* Anzahl der *Nachverfolgung \_*                                                                                                                                                                             |



 

In der folgenden Tabelle werden die Flags aufgelistet, die im **lpszvideo** -Parameter und deren Bedeutung angegeben werden können.



| Wert                                          | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *algorithmusalgorithmus*                          | Gibt einen Video Komprimierungs Algorithmus an, der von einem nachfolgenden [Reserve](reserve.md) -oder [Daten Satz](record.md) Befehl verwendet wird. Von einem Gerät unterstützte Algorithmen sind gerätespezifisch. MCI definiert die Konstanten "MPEG" und "H261" für den *Algorithmus*. Wenn der angegebene Algorithmus mit dem aktuellen Dateiformat in Konflikt steht, wird das Dateiformat in das Standardformat für den Algorithmus geändert.<br/>                                                                                                                                     |
| zu *zählenden* BitsPerPel                          | Legt die Anzahl von Bits pro Pixel für das Speichern von Daten mit dem [Capture](capture.md) -oder [Daten Satz](record.md) Befehl fest.                                                                                                                                                                                                                                                                                                                                                                                                              |
| zu *Faktors* Helligkeit                         | Legt den Wert für die Bildhelligkeit fest.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| clocktime                                      | Gibt an, dass die im Over-Flag angegebene Zeit in Millisekunden angegeben wird. Die Zeit ist absolut und nicht im Schritt der Wiedergabe des Arbeitsbereichs.                                                                                                                                                                                                                                                                                                                                                                                |
| zu *fakfakfaktors*                              | Legt den Farb Sättigungsgrad fest.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| Kontrast zu *Faktor*                           | Legt die Video Kontrast Ebene fest.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Gamma bis *Wert*                               | Gibt den Gammakorrektur Exponent multipliziert mit 1000 an. Um z. b. einen Exponenten von 2,2 anzugeben, verwenden Sie 2200 als *Wert*. Ein Gammawert von 1,0 (1000) gibt an, dass keine Gammakorrektur angewendet wird. Gamma Korrektur passt die Zuordnung zwischen der in der Präsentations Quelle codierten Intensität und der angezeigten Helligkeit an.                                                                                                                                                                                                 |
| Halbton                                       | Bewirkt, dass die "Halbton"-Palette anstelle der Standardpalette verwendet wird. Dieses Flag wird nur vom MCIAVI Digital-Video-Treiber erkannt.                                                                                                                                                                                                                                                                                                                                                                                         |
| input                                          | Ändert das Flag "Helligkeit", "Color", "Contrast", "Gamma", "Schärding" oder "Tint" so, dass es sich auf das Eingabe Signal auswirkt und ändert, was aufgezeichnet wird. Wenn möglich, ist dies der Standardwert, wenn die Eingabe überwacht wird.                                                                                                                                                                                                                                                                                                             |
| Schlüsselfarbe für *r:g: b*                           | Legt die Schlüsselfarbe fest. Die Variable *r:g: b* ist ein RGB-Wert. Doppelpunkte (:) Trennen Sie die einzelnen Werte für Rot, grün und blau.                                                                                                                                                                                                                                                                                                                                                                                                       |
| zu *indizierenden* Schlüssel Index                           | Legt den Schlüssel Index fest. Die *Index* Variable ist ein physischer Palettenindex.                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Monitor für die *Typnummer*               | Steuert, welche Quell Eingaben an die VCR-Ausgabe übermittelt werden, ohne dass die Eingabeauswahl der aufzeichnungsquelle geändert wird. Type kann "Output" oder eine der gültigen Eingabe Quellen sein. Wenn "Number" nicht angegeben ist, wird die erste Eingabe dieses Typs ausgewählt.                                                                                                                                                                                                                                                                        |
| OFFON                                          | Aktiviert oder deaktiviert die Anzeige von Videos. Beim Deaktivieren von Videos werden die Pixel im ["Destination"-](put.md) Rechteck (oder der Standardwert, der Client Bereich des aktuellen Fensters) auf eine voll Tonfarbe festgelegt. Dies hat keine Auswirkung auf den Frame Puffer. Die Videoquelle, ob der Arbeitsbereich oder eine externe Eingabe, speichert möglicherweise weiterhin neue Images im Frame Puffer. Sie werden erst angezeigt, wenn das Video aktiviert ist. Sie [können das Fenster "State](window.md) "-Befehl verwenden, um das Fenster auszublenden. Der Standardwert ist **setvideo** "on".<br/> |
| output                                         | Ändert das Flag "Helligkeit", "Color", "Contrast", "Gamma", "Schärding" oder "Tint", sodass nur das angezeigte Signal geändert wird und nicht das, was aufgezeichnet wird. Wenn möglich, ist dies die Standardeinstellung beim Überwachen einer Datei.                                                                                                                                                                                                                                                                                                           |
| über *Dauer*                                | Gibt an, wie lange es dauert, eine Änderung vorzunehmen, bei der eine *Faktor* Variable verwendet wird. Die Einheiten für die *Dauer* liegen im aktuellen Zeitformat vor. Änderungen erfolgen im Schritt der Wiedergabe des Arbeitsbereichs. Wenn die Wiedergabe angehalten wird, wird die Änderung auch angehalten, bis die Wiedergabe fortgesetzt wird Wenn "Over" nicht verwendet oder nicht unterstützt wird, erfolgt die Änderung sofort.                                                                                                                                                                    |
| *palettenfarbfarbe* über *Index* zu *newrgb* | Legt eine neue Palettenfarbe fest. Der zu ändernde Farb-und Palettenindex wird durch die *Farb* -und *Index* Parameter angegeben. die neue Farbe wird von *newrgb* angegeben. Dieses Flag wird nur vom MCIAVI Digital-Video-Treiber erkannt.                                                                                                                                                                                                                                                                                               |
| zu *behandelnde* Palettenhandle                     | Gibt das Handle für eine Palette an, das vom Gerät zum Rendern verwendet werden muss. Dieses Element wird nur von Geräten unterstützt, die Paletten verwenden. Wenn *handle* gleich NULL ist, wird die Standardpalette verwendet. Digitale Videogeräte dürfen die mit diesem Befehl bestandene Palette nicht freigeben. Anwendungen sollten Sie nach dem Schließen des Geräts freigeben.<br/>                                                                                                                                                                                                 |
| Qualitäts *Deskriptor*                           | Gibt die Merkmale der Video Komprimierung an, die beim Aufzeichnen des Videos in einer Datei ausgeführt wird. Alle Geräte unterstützen die drei Deskriptoren: "niedrig", "Mittel" und "hoch". Der Standardwert ist gerätespezifisch. Die Bedeutung dieser Namen hängt von dem Algorithmus und dem Gerät ab. Geräte können zusätzliche Deskriptornamen definieren. Der [Quality](quality.md) -Befehl kann verwendet werden, um zusätzliche Deskriptornamen zu definieren. Wenn das Flag "Algorithmus" nicht verwendet wird, gilt der *Deskriptor* für den aktuellen Algorithmus.<br/>   |
| zu Rate der Daten *Satz* Rahmenrate                    | Legt die Aufzeichnung für Motion-Video fest. Die Aufzeichnungs *Rate* wird in den einzelnen Frames pro Sekunde multipliziert mit 1000 angegeben. Beispielsweise wird die NTSC-Frame Rate von 29,97 Frames pro Sekunde als 29970 dargestellt.                                                                                                                                                                                                                                                                                                                   |
| onrecord-Datensatz aus Datensatz                            | Aktiviert oder deaktiviert die Aufzeichnung von Videodaten. Das Aufzeichnen von Videodaten ist die Standardeinstellung.                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| *\_ Anzahl* der Daten Satz Nachverfolgung aus               | Löscht die Auswahl der Videoquelle, sodass kein Video mit dem nächsten [Datensatz](record.md) -Befehl aufgezeichnet wird. "Track" ermöglicht die unabhängige Nachverfolgung. Wenn "Track" nicht angegeben wird, wird der Standardwert 1 angenommen. Es kann erforderlich sein, zuerst einen [Set](set.md) -Befehl "assemblierungsdatensatz aus" auszugeben, bevor die Videoaufzeichnung ausgeschaltet werden kann.                                                                                                                                                                     |
| *\_ Anzahl* der Nachverfolgung Nachverfolgung auf                | Wählt die Videoquelle aus, die mit dem nächsten **Datensatz** -Befehl aufgezeichnet werden soll. "Track" ermöglicht die unabhängige Nachverfolgung. Track 2 entspricht dem PCM-Track in Hi8. Wenn "Track" nicht angegeben wird, wird der Standardwert 1 angenommen.                                                                                                                                                                                                                                                                                                      |
| zu *Faktor* Schärfe                          | Legt die Video Schärfe Ebene fest.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| *Wert* der Quelle zur *Quell* Nummer              | Legt die Quelle der Videoeingabe fest. Dies entspricht in der Regel externen Connectors. Zu den für die *Quelle* definierten Konstanten gehören "RGB", "PAL", "NTSC", "SVideo" und "SECAM". Wenn mehr als eine Eingabe vom angegebenen Typ vorhanden ist, gibt der optionale *Wert* "Number" die gewünschte Eingabe an. Beispielsweise gibt **setvideo** "Source to NTSC Number 2" die zweite NTSC-Eingabe an. Wenn die "to"- *Quelle* weggelassen wird, wird die absolute Quelle entsprechend der Definition durch den Befehl "Videoquelle [auflisten](list.md) " verwendet.<br/>            |
| Quelle für *Typnummer*                | Wählt die Videoquelle aus, die auf dem Band aufgezeichnet werden soll. Der *Typ* muss "Tuner", "Line", "SVideo", "AUX", "Generic", "stumm" oder "RGB" lauten.                                                                                                                                                                                                                                                                                                                                                                                              |
| *Algorithmus Algorithmus* noch immer                    | Gibt den immer noch Bild Komprimierungs Algorithmus an, der vom [Aufzeichnungs](capture.md) Befehl verwendet wird. Jedes Gerät muss den *Algorithmus* "None" unterstützen, was bedeutet, dass keine Komprimierung erforderlich ist. Dies ist die Standardoption. In diesem Fall speichern Digital Videogeräte weiterhin Bilder als RGB-geräteunabhängige Bitmaps. Geräte können auch eine gerätespezifische Liste zusätzlicher Algorithmen unterstützen.                                                                                                                                                           |
| immer noch Qualitäts *Deskriptor*                     | Gibt die Merkmale der noch Bildkomprimierung an, die beim Erfassen eines Images ausgeführt wird. Alle Geräte unterstützen die Deskriptoren "Low", "Medium" und "High". Der Standardwert ist gerätespezifisch. Wenn das Flag "Algorithmus" nicht verwendet wird, gilt der *Deskriptor* für den aktuellen Algorithmus.<br/> Der [Quality](quality.md) -Befehl kann verwendet werden, um andere Deskriptornamen zu definieren.<br/>                                                                                                                            |
| Stream zu *Zahl*                             | Gibt den Videostream an, der aus dem Arbeitsbereich wiedergegeben wird. Wenn der Stream nicht angegeben wird und kein Standarddaten Strom durch das Dateiformat definiert ist, wird der physisch erste überlappende Videostream wiedergegeben.                                                                                                                                                                                                                                                                                                                 |
| zu *fakfaktint*                               | Legt die Bild-tint fest. Diese Anpassung wird in der Regel nach dem Tönungs-Steuerelement von vielen Farb Fernseh Sätzen modelliert, wobei 250 Bedeutung grün, 750 Bedeutung rot und 0 (oder                                                                                                                                                                                                                                                                                                                                                             |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszflags*
</dt> <dd>

Kann "wait", "notify", "Test" oder eine Kombination daraus sein. Weitere Informationen zu diesen Flags finden Sie [unter warte-, Benachrichtigungs-und testflags](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.

## <a name="remarks"></a>Bemerkungen

Bei VCR-Geräten kann die Anwendung durch die Verwendung von setvideo mit einem Flag, das eine einzelne Spur deaktiviert ("Nachverfolgen der *Spur \_ Nummer* Off"), eine Statusmeldung erhalten, die darauf hinweist, dass der Befehl nicht ausgeführt werden konnte. Einige VCRs können nur die Kombinationen von Spuren und nicht einzelne Spuren deaktivieren. beispielsweise die erste Audiospur und eine Videospur einer Video-Kassette. Verwenden Sie in diesem Fall einfach [setaudiodatei](setaudio.md) und setvideo, um die anderen Titel zu deaktivieren, die die Kombination bilden. Der Treiber schaltet die Spuren aus, wenn er den Befehl empfängt, um den letzten Titel in der Kombination zu deaktivieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[MCI-Befehls Zeichenfolgen](mci-command-strings.md)
</dt> <dt>

[einver](capture.md)
</dt> <dt>

[list](list.md)
</dt> <dt>

[stellte](put.md)
</dt> <dt>

[record](record.md)
</dt> <dt>

[Reserve](reserve.md)
</dt> <dt>

[set](set.md)
</dt> <dt>

[setaudiodatei](setaudio.md)
</dt> <dt>

[ster](window.md)
</dt> </dl>

 

