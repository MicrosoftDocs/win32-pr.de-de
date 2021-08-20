---
title: Window-Befehl
description: Der Befehl window steuert das Anzeigefenster.
ms.assetid: 613dfedb-5ca8-45da-a4ba-ce465b933451
keywords:
- window-Befehl Windows Multimedia
topic_type:
- apiref
api_name:
- window
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c65fe13309d30a3aff94e6e78dc0ab1fbcfec26aa1634e8dae72130370cc8e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117800704"
---
# <a name="window-command"></a>Window-Befehl

Der Befehl window steuert das Anzeigefenster. Mit diesem Befehl können Sie die Anzeigemerkmale des Fensters ändern oder ein Zielfenster bereitstellen, das der Treiber statt des Standardanzeigefensters verwenden kann. Digital-Video- und Videoüberlagerungsgeräte erkennen diesen Befehl.

Um diesen Befehl zu senden, rufen Sie die [**mciSendString-Funktion**](/previous-versions//dd757161(v=vs.85)) mit dem *lpszCommand-Parameter* auf, der wie folgt festgelegt ist.

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

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Bezeichner eines MCI-Geräts. Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.

</dd> <dt>

<span id="lpszWindowFlags"></span><span id="lpszwindowflags"></span><span id="LPSZWINDOWFLAGS"></span>*lpszWindowFlags*
</dt> <dd>

Flag zum Steuern des Anzeigefensters. In der folgenden Tabelle sind Gerätetypen aufgeführt, die den Fensterbefehl und die von den einzelnen Typen verwendeten Flags erkennen.



| Wert        | Bedeutung                                                                                                                                        | Bedeutung                                                                                                                                   |
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| digitalvideo | handle *hwnd state* hidestate minimizestate restorestate showshow maximized                                                                    | show minimizedshow [**min**](min.md) noactiveshow nashow noactivateshow normaltext *caption*                                             |
| overlay      | fixedhandle defaulthandle *hwnd* state hidestate maximizedstate minimizestate minimizedstate no actionstate noactivatestate normal | status restorestate showshow maximizedshow minimizedshow [**min**](min.md) noactiveshow nashow noactivateshow normalstretchtext *caption* |



 

In der folgenden Tabelle sind die Flags, die im **lpszWindowFlags-Parameter** angegeben werden können, und ihre Bedeutungen aufgeführt.



| Wert                            | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| fixed                            | Deaktiviert das Strecken des Bilds.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| handle default                   | Gibt an, dass das Gerät das Anzeigefenster wieder auf das Standardfenster festlegen soll, das während des Öffnens [erstellt](open.md) wurde. Für Videoüberlagerungsgeräte gibt an, dass das Gerät ein eigenes Zielfenster erstellen und verwalten soll.                                                                                                                                                                                                                                                                                                                                                  |
| handle *hwnd*                    | Gibt das Handle des Zielfensters an, das anstelle des Standardfensters verwendet werden soll. Der *hwnd-Parameter* enthält die numerische ASCII-Entsprechung des Fensterhandpunkts, das von der [CreateWindow-Funktion zurückgegeben](/windows/win32/api/winuser/nf-winuser-createwindowa) wird. Zwei Geräteinstanzen können dasselbe Fensterhand handle verwenden, vorausgesetzt, dass jede Instanz die Video- und Bildpixel im Fenster aktualisiert, als wäre die andere Instanz nicht vorhanden. Wenn die Videoausgabe mit [setvideo](setvideo.md) "off" deaktiviert ist, wird das Zielrechteck durch einen Updatebefehl zu einer Volltonfarbe. [](update.md) |
| Maximiert anzeigen                   | Maximiert das Zielfenster.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| show [**min**](min.md) noactive | Zeigt das Zielfenster als Symbol an.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| minimiert anzeigen                   | Minimiert das Zielfenster.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| show na                          | Zeigt das Zielfenster im aktuellen Zustand an. Das fenster, das derzeit aktiv ist, bleibt aktiv.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| noactivate anzeigen                  | Zeigt das Zielfenster in seiner letzten Größe und Position an. Das fenster, das derzeit aktiv ist, bleibt aktiv.                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Normal anzeigen                      | Aktiviert das Zielfenster in seiner ursprünglichen Größe und Position und zeigt es an. (Dies ist identisch mit dem Flag "Zustandswiederherstellung".)                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Status ausblenden                       | Blendet das Zielfenster aus.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| Zustandserzustand                     | Zeigt das Zielfenster als Symbol an.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Zustand maximiert                  | Maximiert das Zielfenster.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Status minimieren                   | Minimiert das Zielfenster und aktiviert das Fenster der obersten Ebene in der Liste des Fenster-Managers.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Status minimiert                  | Minimiert das Zielfenster.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Status "Keine Aktion"                  | Zeigt das Zielfenster im aktuellen Zustand an. Das fenster, das derzeit aktiv ist, bleibt aktiv.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| state noactivate                 | Zeigt das Zielfenster in seiner letzten Größe und seinem aktuellen Zustand an. Das derzeit aktive Fenster bleibt aktiv.                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Normalzustand                     | Aktiviert das Zielfenster in seiner ursprünglichen Größe und Position und zeigt es an.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Zustandswiederherstellung                    | Aktiviert das Zielfenster in seiner ursprünglichen Größe und Position und zeigt es an.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| state show                       | Zeigt das Zielfenster an.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| strecken                          | Ermöglicht das Strecken des Bilds.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| *Textbeschriftung*                   | Gibt die Beschriftung für das Zielfenster an. Wenn dieser Text eingebettete Leerzeichen enthält, muss die gesamte Beschriftung in Anführungszeichen eingeschlossen werden. Die Standardbeschriftung für das Standardfenster ist leer.                                                                                                                                                                                                                                                                                                                                                                                        |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Kann "wait", "notify" oder beides sein. Für Digitalvideogeräte kann auch "test" angegeben werden. Weitere Informationen zu diesen Flags finden Sie unter [Die Warte-, Benachrichtigungs- und Testflags](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls ein Fehler.

## <a name="remarks"></a>Hinweise

Videoüberlagerungsgeräte erstellen in der Regel ein Fenster und zeigen es an, wenn es geöffnet wird. Wenn Ihre Anwendung ein Fenster für den Treiber bietet, ist Ihre Anwendung für die Verwaltung der an das Fenster gesendeten Nachrichten verantwortlich.

Da Sie den [](status.md) Statusbefehl verwenden können, um das Handle für das Anzeigefenster des Treibers abzurufen, können Sie auch die Standardmäßig-Fenster-Manager-Funktionen (z. B. [ShowWindow](/windows/win32/api/winuser/nf-winuser-showwindow)) verwenden, um das Fenster zu bearbeiten.

## <a name="examples"></a>Beispiele

Der folgende Befehl zeigt die Beschriftung für das Wiedergabefenster "Movie" an und legt sie fest.

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

[Mci](mci.md)
</dt> <dt>

[MCI-Befehlszeichenfolgen](mci-command-strings.md)
</dt> <dt>

[open](open.md)
</dt> <dt>

[Spielen](play.md)
</dt> <dt>

[setvideo](setvideo.md)
</dt> <dt>

[update](update.md)
</dt> </dl>

 

