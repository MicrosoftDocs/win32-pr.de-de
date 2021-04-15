---
title: Fenster Befehl
description: Der Fenster Befehl steuert das Anzeige Fenster.
ms.assetid: 613dfedb-5ca8-45da-a4ba-ce465b933451
keywords:
- Fenster Befehl Windows Multimedia
topic_type:
- apiref
api_name:
- window
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21dde3304fa1445b0eaac68950cdfb91f48e5986
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476581"
---
# <a name="window-command"></a>Fenster Befehl

Der Fenster Befehl steuert das Anzeige Fenster. Sie können diesen Befehl verwenden, um die Anzeigeeigenschaften des Fensters zu ändern oder ein Zielfenster für den Treiber bereitzustellen, das anstelle des Standard Anzeige Fensters verwendet werden soll. Dieser Befehl wird von Digital Video-und Video Überlagerungs Geräten erkannt.

Um diesen Befehl zu senden, wenden Sie die [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion mit dem festgelegten *lpszcommand* -Parameter wie folgt an.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("window %s %s %s"), 
  lpszDeviceID, 
  lpszWindowFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszde viceid*
</dt> <dd>

Der Bezeichner eines MCI-Geräts. Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.

</dd> <dt>

<span id="lpszWindowFlags"></span><span id="lpszwindowflags"></span><span id="LPSZWINDOWFLAGS"></span>*lpszwindowflags*
</dt> <dd>

Flag zum Steuern des Anzeige Fensters. In der folgenden Tabelle werden die Gerätetypen aufgelistet, die den Fenster Befehl und die von den einzelnen Typen verwendeten Flags erkennen.



| Wert        | Bedeutung                                                                                                                                        | Bedeutung                                                                                                                                   |
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| Digitalvideo | Handle für *HWND* State hidestate minimizestate restorestate das zeigt maximiert                                                                    | Anzeigen von minimizedshow [**Min**](min.md) noactiveshow nashow noactivateshow Normaltext *Caption*                                             |
| overlay      | fixedhandle defaulthandle *HWND* State hidestate iconicstate maximizedstate minimizestate minimizedstate No aktionstate noactivatestate normal | State restorestate das zeigt maximizedshow minimizedshow [**Min**](min.md) noactiveshow nashow noactivatesas normalstretchtext *Caption* |



 

In der folgenden Tabelle werden die Flags aufgelistet, die im **lpszwindowflags** -Parameter und deren Bedeutung angegeben werden können.



| Wert                            | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| fixed                            | Deaktiviert die Streckung des Bilds.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Standard verarbeiten                   | Gibt an, dass das Gerät das Anzeige Fenster auf das Standardfenster zurücksetzen soll, das während des [öffnenden](open.md) Vorgangs erstellt wurde. Gibt bei Video Überlagerungs Geräten an, dass das Gerät sein eigenes Zielfenster erstellen und verwalten soll.                                                                                                                                                                                                                                                                                                                                                  |
| *HWND* behandeln                    | Gibt das Handle des Zielfensters an, das anstelle des Standard Fensters verwendet werden soll. Der *HWND* -Parameter enthält die numerische ASCII-Entsprechung des Fenster Handles, das von der Funktion "up [Window](/windows/win32/api/winuser/nf-winuser-createwindowa) " zurückgegeben wird. Zwei Geräte Instanzen können dasselbe Fenster Handle verwenden, vorausgesetzt, dass jede Instanz die Video-und Bild Pixel im Fenster aktualisiert, als wäre die andere Instanz nicht vorhanden. Wenn die Videoausgabe mit [setvideo](setvideo.md) "Off" deaktiviert ist, wird das Ziel Rechteck durch einen [Update](update.md) -Befehl zu einer voll Tonfarbe. |
| maximiert anzeigen                   | Maximiert das Zielfenster.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [**minimale**](min.md) noaktive anzeigen | Zeigt das Zielfenster als Symbol an.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Minimierte anzeigen                   | Minimiert das Zielfenster.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Na anzeigen                          | Zeigt das Zielfenster im aktuellen Zustand an. das aktuell aktive Fenster bleibt aktiv.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| noaktivierungs anzeigen                  | Zeigt das Zielfenster in seiner aktuellen Größe und Position an. das aktuell aktive Fenster bleibt aktiv.                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| normal anzeigen                      | Aktiviert und zeigt das Zielfenster in der ursprünglichen Größe und Position an. (Dies ist das gleiche wie das Flag "State Restore".)                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Status ausblenden                       | Blendet das Zielfenster aus.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| Status "berühmt"                     | Zeigt das Zielfenster als Symbol an.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Status maximiert                  | Maximiert das Zielfenster.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Status Minimierung                   | Minimiert das Zielfenster und aktiviert das Fenster der obersten Ebene in der Liste der Fenster-Manager.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Status minimiert                  | Minimiert das Zielfenster.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| State No action                  | Zeigt das Zielfenster im aktuellen Zustand an. Das aktuell aktive Fenster bleibt aktiv.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Status noaktivierungs                 | Zeigt das Zielfenster in der aktuellen Größe und dem aktuellen Status an. Das derzeit aktive Fenster bleibt aktiv.                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Zustand normal                     | Aktiviert und zeigt das Zielfenster in der ursprünglichen Größe und Position an.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Zustands Wiederherstellung                    | Aktiviert und zeigt das Zielfenster in der ursprünglichen Größe und Position an.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Statusanzeige                       | Zeigt das Zielfenster an.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| strecken                          | Ermöglicht das Stretching des Bilds.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Text *Beschriftung*                   | Gibt die Beschriftung für das Zielfenster an. Wenn dieser Text eingebettete Leerzeichen enthält, muss die gesamte Beschriftung in Anführungszeichen eingeschlossen werden. Die Standard Beschriftung für das Standardfenster ist leer.                                                                                                                                                                                                                                                                                                                                                                                        |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszflags*
</dt> <dd>

Kann "wait", "notify" oder beides sein. Für Digital Video-Geräte kann auch "Test" angegeben werden. Weitere Informationen zu diesen Flags finden Sie [unter warte-, Benachrichtigungs-und testflags](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.

## <a name="remarks"></a>Bemerkungen

Video Überlagerungs Geräte erstellen und zeigen beim Öffnen normalerweise ein Fenster an. Wenn Ihre Anwendung ein Fenster für den Treiber bereitstellt, ist Ihre Anwendung für die Verwaltung der an das Fenster gesendeten Nachrichten verantwortlich.

Da Sie mit dem Befehl " [Status](status.md) " das Handle zum Anzeige Fenster des Treibers abrufen können, können Sie auch die Standardfenster-Manager-Funktionen (z. b. [ShowWindow](/windows/win32/api/winuser/nf-winuser-showwindow)) verwenden, um das Fenster zu bearbeiten.

## <a name="examples"></a>Beispiele

Der folgende Befehl zeigt die Beschriftung für das Wiedergabe Fenster "Movie" an und legt diese fest.

``` syntax
window movie text "Welcome to the Movies" state show
```

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

[open](open.md)
</dt> <dt>

[Theater](play.md)
</dt> <dt>

[setvideo](setvideo.md)
</dt> <dt>

[update](update.md)
</dt> </dl>

 

