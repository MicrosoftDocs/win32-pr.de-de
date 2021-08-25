---
title: Befehl "setvideo"
description: Der Befehl setvideo legt Werte fest, die der Videowiedergabe und -erfassung zugeordnet sind. Digital-Video- und VCR-Geräte erkennen diesen Befehl.
ms.assetid: a6851b9b-e09a-4251-bd1c-19b1e4b6f871
keywords:
- befehl setvideo Windows Multimedia
topic_type:
- apiref
api_name:
- setvideo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 674b8b35c21fa54f1c2ecfc8b9dff531266c319b827d675da46be04e6c7abe8e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119805380"
---
# <a name="setvideo-command"></a>Befehl "setvideo"

Der Befehl setvideo legt Werte fest, die der Videowiedergabe und -erfassung zugeordnet sind. Digital-Video- und VCR-Geräte erkennen diesen Befehl.

Um diesen Befehl zu senden, rufen Sie die [**mciSendString-Funktion**](/previous-versions//dd757161(v=vs.85)) mit dem *lpszCommand-Parameter* auf, der wie folgt festgelegt ist.

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

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Bezeichner eines MCI-Geräts. Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.

</dd> <dt>

<span id="lpszVideo"></span><span id="lpszvideo"></span><span id="LPSZVIDEO"></span>*lpszVideo*
</dt> <dd>

Flag für Videowiedergabe und -erfassung. In der folgenden Tabelle sind die Gerätetypen aufgeführt, die den **Befehl setvideo** und die von den einzelnen Typen verwendeten Flags erkennen.



| Wert        | Bedeutung                                                                                                                                                                                        | Bedeutung                                                                                                                                                                                                                                                                                                |
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| digitalvideo | Algorithm *algorithm* bitsperpel to count *brightness* to factor clocktimecolor to *factor* contrast to factor gamma to value halftoneinputkey color to r:g:b key index to index offonoutput (Algorithmusalgorithmus bitsperpel to count brightness to *factor* clocktimecolor to factor contrast to *factor* gamma to *value* halftoneinputkey color to *r:g:b* key index to *index* offonoutput | Über die Dauer palette color *color* over  *index* to *newrgb* palette handle to handle quality *descriptor* record frame rate to rate *record* onrecord offsharpness to *factor* source to *source* number *value* still algorithm *algorithm* still quality *descriptor* stream to *number* color to *factor* |
| Vcr          | offonmonitor zum *Eingeben des Nummernnummer-Datensatzes* offrecord track *track \_ number* off                                                                                                                | datensatz onrecord track *track \_ number* onsource to *type* number *number* track *\_ number* offtrack *track \_ number* on                                                                                                                                                                             |



 

In der folgenden Tabelle sind die Flags, die im **lpszVideo-Parameter** angegeben werden können, und ihre Bedeutungen aufgeführt.



| Wert                                          | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Algorithmusalgorithmus*                          | Gibt einen Videokomprimierungsalgorithmus zur Verwendung durch einen nachfolgenden Reserve- [oder](reserve.md) [Datensatzbefehl](record.md) an. Von einem Gerät unterstützte Algorithmen sind gerätespezifisch. MCI definiert die Konstanten "mpeg" und "h261" für den *Algorithmus*. Wenn der angegebene Algorithmus mit dem aktuellen Dateiformat in Konflikt steht, wird das Dateiformat in das Standardformat für den Algorithmus geändert.<br/>                                                                                                                                     |
| bitsperpel to *count*                          | Legt die Anzahl der Bits pro Pixel zum Speichern von Daten mit dem Aufzeichnungs- [oder](capture.md) [Datensatzbefehl](record.md) fest.                                                                                                                                                                                                                                                                                                                                                                                                              |
| Helligkeit zu *Faktor*                         | Legt die Helligkeitsstufe des Videos fest.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| clocktime                                      | Gibt an, dass die im Flag "over" angegebene Zeit in Millisekunden liegt. Die Zeit ist absolut und nicht im Schritt zur Wiedergabe des Arbeitsbereichs.                                                                                                                                                                                                                                                                                                                                                                                |
| Farbe zu *Faktor*                              | Legt den Farbsättigungsgrad fest.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| Kontrast zum *Faktor*                           | Legt die Videokontrastebene fest.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| gamma bis *value*                               | Gibt den Gammakorrektur-Exponenten multipliziert mit 1000 an. Um beispielsweise einen Exponenten von 2,2 anzugeben, verwenden Sie 2200 für *den Wert*. Der Gammawert 1,0 (1000) gibt an, dass keine Gammakorrektur angewendet wird. Die Gammakorrektur passt die Zuordnung zwischen der in der Präsentationsquelle codierten Intensität und der angezeigten Helligkeit an.                                                                                                                                                                                                 |
| Halbton                                       | Bewirkt, dass die Halbtonpalette anstelle der Standardpalette verwendet wird. Dieses Flag wird nur vom MCIAVI-Treiber für digitale Videos erkannt.                                                                                                                                                                                                                                                                                                                                                                                         |
| input                                          | Ändert das Flag "Helligkeit", "Farbe", "Kontrast", "Gamma", "Schärfe" oder "Tönung", sodass es das Eingabesignal beeinflusst und die aufgezeichneten Daten ändert. Wenn möglich, ist dies die Standardeinstellung bei der Überwachung der Eingabe.                                                                                                                                                                                                                                                                                                             |
| Schlüsselfarbe zu *r:g:b*                           | Legt die Schlüsselfarbe fest. Die *Variable r:g:b* ist ein RGB-Wert. Doppelpunkte (:) Trennen Sie die einzelnen Werte für Rot, Grün und Blau.                                                                                                                                                                                                                                                                                                                                                                                                       |
| Schlüsselindex zum *Indizieren*                           | Legt den Schlüsselindex fest. Die *Indexvariable* ist ein physischer Palettenindex.                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| monitor to *type* number *number*              | Steuert, welche Quelleingabe an die VCR-Ausgabe übergeben wird, ohne die Auswahl der Aufzeichnungsquelle zu ändern. Der Typ kann "output" oder eine der gültigen Eingabequellen sein. Wenn "number" nicht angegeben ist, wird die erste Eingabe dieses Typs ausgewählt.                                                                                                                                                                                                                                                                        |
| offon                                          | Aktiviert oder deaktiviert die Anzeige von Videos. Durch deaktivieren des Videos [](put.md) werden die Pixel im Zielrechteck (oder dessen Standard, der Clientbereich des aktuellen Fensters) auf eine Volltonfarbe festgelegt. Sie hat keine Auswirkungen auf den Framepuffer. Die Videoquelle – ob arbeitsbereichs- oder externe Eingabe – kann weiterhin neue Bilder im Framepuffer speichern. Sie werden erst angezeigt, wenn das Video aktiviert ist. Sie können den Befehl ["state"](window.md) des Fensters verwenden, um das Fenster auszublenden. Der Standardwert ist **setvideo** "on".<br/> |
| output                                         | Ändert das Flag "Helligkeit", "Farbe", "Kontrast", "Gamma", "Schärfe" oder "Tönung", sodass nur das angezeigte Signal und nicht das aufgezeichnete Signal verändert wird. Wenn möglich, ist dies die Standardeinstellung bei der Überwachung einer Datei.                                                                                                                                                                                                                                                                                                           |
| über *die Dauer*                                | Gibt an, wie lange eine Änderung, die eine Faktorvariable verwendet, *dauern* soll. Die Einheiten für *die Dauer* liegen im aktuellen Zeitformat vor. Änderungen erfolgen im Schritt mit der Wiedergabe des Arbeitsbereichs. Wenn die Wiedergabe angehalten wird, wird die Änderung ebenfalls angehalten, bis die Wiedergabe fortgesetzt wird. Wenn "over" nicht verwendet oder nicht unterstützt wird, erfolgt die Änderung sofort.                                                                                                                                                                    |
| palette color *color* over *index* to *newrgb* | Legt eine neue Palettenfarbe fest. Die zu ändernde Farbe und der Palettenindex werden durch die *Farb- und* *Indexparameter* angegeben. die neue Farbe wird durch *newrgb angegeben.* Dieses Flag wird nur vom MCIAVI-Treiber für digitale Videos erkannt.                                                                                                                                                                                                                                                                                               |
| Zu behandelnde *Palettenhand handle*                     | Gibt das Handle für eine Palette an, die das Gerät für das Rendering verwenden muss. Dieses Element wird nur von Geräten unterstützt, die Paletten verwenden. Wenn *handle* 0 (null) ist, wird die Standardpalette verwendet. Digitalvideogeräte sollten die mit diesem Befehl übergebene Palette nicht freischalten. Anwendungen sollten sie nach dem Schließen des Geräts wieder frei geben.<br/>                                                                                                                                                                                                 |
| *Qualitätsdeskriptor*                           | Gibt die Merkmale der Videokomprimierung an, die ausgeführt wird, wenn Videos in einer Datei aufgezeichnet werden. Alle Geräte unterstützen die drei Deskriptoren "low", "medium" und "high". Der Standardwert ist gerätespezifisch. Die Bedeutung dieser Namen hängt vom Algorithmus und vom Gerät ab. Geräte definieren möglicherweise zusätzliche Deskriptornamen. Der [Quality-Befehl](quality.md) kann verwendet werden, um zusätzliche Deskriptornamen zu definieren. Wenn das Flag "algorithm" nicht verwendet wird, gilt der *Deskriptor* für den aktuellen Algorithmus.<br/>   |
| Datensatzbildrate zu *Rate*                    | Legt die Aufzeichnung für Bewegungsvideos fest. Die *Aufzeichnungsrate* wird in Einheiten von Frames pro Sekunde multipliziert mit 1000 angegeben. Beispielsweise wird die NTSC-Framerate von 29,97 Frames pro Sekunde als 29970 dargestellt.                                                                                                                                                                                                                                                                                                                   |
| datensatz onrecord off                            | Aktiviert oder deaktiviert die Aufzeichnung von Videodaten. Die Standardeinstellung ist das Aufzeichnen von Videodaten.                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Record Track *Track \_ Number* off               | Clears the video-source selection so that no video will be recorded with the [next record](record.md) command. "Track" ermöglicht eine unabhängige Trackauswahl. Wenn "track" nicht angegeben ist, wird der Standardwert 1 angenommen. Möglicherweise ist es erforderlich, zuerst einen satz ["assemble](set.md) record off"-Befehl aus auszuführen, bevor die Videoaufzeichnung deaktiviert werden kann.                                                                                                                                                                     |
| Record Track *Track \_ Number* on                | Wählt die Videoquelle aus, die mit dem nächsten Datensatzbefehl **aufgezeichnet werden** soll. "Track" ermöglicht eine unabhängige Trackauswahl. Track 2 entspricht der PCM-Spur in Hi8. Wenn "track" nicht angegeben ist, wird der Standardwert 1 angenommen.                                                                                                                                                                                                                                                                                                      |
| Schärfe zum *Faktor*                          | Legt die Videoschärfestufe fest.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| *Source-to-Source-Zahlenwert*               | Legt die Quelle der Videoeingabe fest. Dies entspricht in der Regel externen Connectors. Die für die Quelle *definierten* Konstanten umfassen "rgb", "pal", "ntsc", "svideo" und "secam". Wenn mehr als eine Eingabe des angegebenen Typs  vorhanden ist, gibt der optionale Wert "number" die gewünschte Eingabe an. Beispielsweise gibt **setvideo** "source to ntsc number 2" die zweite NTSC-Eingabe an. Wenn die  Quelle "to" ausgelassen wird, wird die absolute Quelle gemäß der Definition durch den Befehl ["video](list.md) source" der Liste verwendet.<br/>            |
| source to *type* number *number*               | Wählt die Videoquelle aus, die auf dem Band aufgezeichnet werden soll. *Typ* muss "tuner", "line", "svideo", "aux", "generic", "mute" oder "rgb" sein.                                                                                                                                                                                                                                                                                                                                                                                              |
| *still-Algorithmusalgorithmus*                    | Gibt den vom Erfassungsbefehl verwendeten Algorithmus für die Bildkomprimierung [an.](capture.md) Jedes Gerät muss den Algorithmus *"None"* unterstützen, was bedeutet, dass keine Komprimierung durchgeführt wird. Dies ist die Standardoption. In diesem Fall speichern Digitalvideogeräte Stillbilder als RGB-geräteunabhängige Bitmaps. Geräte unterstützen möglicherweise auch eine gerätespezifische Liste zusätzlicher Algorithmen.                                                                                                                                                           |
| *Noch-Qualitätsdeskriptor*                     | Gibt die Merkmale der Stillbildkomprimierung an, die beim Erfassen eines Stillbilds ausgeführt wird. Alle Geräte unterstützen die Deskriptoren "niedrig", "mittel" und "hoch". Der Standardwert ist gerätespezifisch. Wenn das Flag "algorithm" nicht verwendet wird, gilt der *Deskriptor* für den aktuellen Algorithmus.<br/> Der [Quality-Befehl](quality.md) kann verwendet werden, um andere Deskriptornamen zu definieren.<br/>                                                                                                                            |
| stream to *number*                             | Gibt den Videostream an, der aus dem Arbeitsbereich wiedergibt. Wenn der Stream nicht angegeben ist und ein Standardstream nicht durch das Dateiformat definiert ist, wird der physisch erste überlappte Videostream abgespielt.                                                                                                                                                                                                                                                                                                                 |
| Tönung zu *Faktor*                               | Legt die Tönung des Bilds fest. In der Regel wird diese Anpassung nach der Tönungssteuerung vieler Farb-Tv-Sets modelliert. 250 bedeutet Grün, 750 bedeutet Rot und 0 (oder                                                                                                                                                                                                                                                                                                                                                             |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Kann "wait", "notify", "test" oder eine Kombination aus diesen sein. Weitere Informationen zu diesen Flags finden Sie unter [Die Warte-, Benachrichtigungs- und Testflags](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls ein Fehler.

## <a name="remarks"></a>Hinweise

Bei VCR-Geräten kann die Verwendung von setvideo mit einem Flag, das eine einzelne Spur ausschaltet ("Track *\_ track number* off"), dazu führen, dass Ihre Anwendung eine Statusmeldung erhält, die angibt, dass der Befehl nicht ausgeführt werden konnte. Einige VCRs können nur Kombinationen von Spuren deaktivieren, nicht einzelne Spuren. Beispiel: die erste Audiospur und eine Videospur einer Video cassette. Verwenden Sie in diesem Fall einfach [setaudio](setaudio.md) und setvideo, um die anderen Spuren, aus denen die Kombination aufbaut, weiter zu deaktivieren. Der Treiber deaktiviert die Spuren, wenn er den Befehl empfängt, um die letzte Spur in der Kombination zu deaktivieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mci](mci.md)
</dt> <dt>

[MCI-Befehlszeichenfolgen](mci-command-strings.md)
</dt> <dt>

[Erfassen](capture.md)
</dt> <dt>

[list](list.md)
</dt> <dt>

[put](put.md)
</dt> <dt>

[record](record.md)
</dt> <dt>

[Reserve](reserve.md)
</dt> <dt>

[set](set.md)
</dt> <dt>

[Setaudio](setaudio.md)
</dt> <dt>

[Fenster](window.md)
</dt> </dl>

 

