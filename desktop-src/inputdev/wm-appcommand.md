---
title: WM_APPCOMMAND Meldung (Winuser.h)
description: Benachrichtigt ein Fenster, dass der Benutzer ein Anwendungsbefehlsereignis generiert hat, z. B. indem er mit der Maus auf eine Anwendungsbefehlsschaltfläche klickt oder eine Anwendungsbefehlstaste auf der Tastatur eingibt.
ms.assetid: ffcdfc44-dbfa-42d4-8749-b33bf0e4de0c
keywords:
- WM_APPCOMMAND Meldung Tastatur- und Mauseingabe
topic_type:
- apiref
api_name:
- WM_APPCOMMAND
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 667b2974015edd8b8d3ac0505f4eb4d6c64d1da5b82737ec7d9bb89cc3e8776e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118248004"
---
# <a name="wm_appcommand-message"></a>WM \_ APPCOMMAND-Nachricht

Benachrichtigt ein Fenster, dass der Benutzer ein Anwendungsbefehlsereignis generiert hat, z. B. indem er mit der Maus auf eine Anwendungsbefehlsschaltfläche klickt oder eine Anwendungsbefehlstaste auf der Tastatur eingibt.


```C++
#define WM_APPCOMMAND                   0x0319
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein Handle für das Fenster, in dem der Benutzer auf die Schaltfläche geklickt oder die TASTE gedrückt hat. Dies kann ein untergeordnetes Fenster des Fensters sein, das die Nachricht empfängt. Weitere Informationen zum Verarbeiten dieser Nachricht finden Sie im Abschnitt "Hinweise".

</dd> <dt>

*lParam* 
</dt> <dd>

Verwenden Sie den folgenden Code, um die im *lParam-Parameter* enthaltenen Informationen abzurufen.


```
cmd  = GET_APPCOMMAND_LPARAM(lParam);

uDevice = GET_DEVICE_LPARAM(lParam);

dwKeys = GET_KEYSTATE_LPARAM(lParam);
```



Der Anwendungsbefehl ist *cmd*. Dies kann einer der folgenden Werte sein.



| Wert                                                                                                                                                                                                                                                                                                                  | Bedeutung                                                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="APPCOMMAND_BASS_BOOST"></span><span id="appcommand_bass_boost"></span><dl> <dt>**APPCOMMAND \_ BOOST \_**</dt> <dt>20</dt> </dl>                                                                         | Schalten Sie den Verstärkungston ein und aus.<br/>                                                                                                                                                                                                                                               |
| <span id="APPCOMMAND_BASS_DOWN"></span><span id="appcommand_bass_down"></span><dl> <dt>**APPCOMMAND \_ DROPDOWN \_**</dt> <dt>19</dt> </dl>                                                                            | Verringern Sie den 16-Prozent-80-Prozent<br/>                                                                                                                                                                                                                                                              |
| <span id="APPCOMMAND_BASS_UP"></span><span id="appcommand_bass_up"></span><dl> <dt>**APPCOMMAND \_ POPUP \_ 21**</dt> <dt></dt> </dl>                                                                                  | Erhöhen Sie den Vergrößerungston.<br/>                                                                                                                                                                                                                                                              |
| <span id="APPCOMMAND_BROWSER_BACKWARD"></span><span id="appcommand_browser_backward"></span><dl> <dt>**APPCOMMAND \_ BROWSER \_ RÜCKWÄRTS**</dt> <dt>1</dt> </dl>                                                        | Navigieren Sie rückwärts.<br/>                                                                                                                                                                                                                                                              |
| <span id="APPCOMMAND_BROWSER_FAVORITES"></span><span id="appcommand_browser_favorites"></span><dl> <dt>**APPCOMMAND \_ \_BROWSERFAVORITEN**</dt> <dt>6</dt> </dl>                                                     | Öffnen Sie Favoriten.<br/>                                                                                                                                                                                                                                                                 |
| <span id="APPCOMMAND_BROWSER_FORWARD"></span><span id="appcommand_browser_forward"></span><dl> <dt>**APPCOMMAND \_ BROWSER \_ FORWARD**</dt> <dt>2</dt> </dl>                                                           | Navigieren Sie vorwärts.<br/>                                                                                                                                                                                                                                                               |
| <span id="APPCOMMAND_BROWSER_HOME"></span><span id="appcommand_browser_home"></span><dl> <dt>**APPCOMMAND \_ BROWSER \_ HOME**</dt> <dt>7</dt> </dl>                                                                    | Navigieren Sie zur Startseite.<br/>                                                                                                                                                                                                                                                                  |
| <span id="APPCOMMAND_BROWSER_REFRESH"></span><span id="appcommand_browser_refresh"></span><dl> <dt>**APPCOMMAND \_ \_BROWSERAKTUALISIERUNG**</dt> <dt>3</dt> </dl>                                                           | Seite "Aktualisieren".<br/>                                                                                                                                                                                                                                                                   |
| <span id="APPCOMMAND_BROWSER_SEARCH"></span><span id="appcommand_browser_search"></span><dl> <dt>**APPCOMMAND \_ \_BROWSERSUCHE**</dt> <dt>5</dt> </dl>                                                              | Öffnen Sie die Suche.<br/>                                                                                                                                                                                                                                                                    |
| <span id="APPCOMMAND_BROWSER_STOP"></span><span id="appcommand_browser_stop"></span><dl> <dt>**APPCOMMAND \_ \_BROWSERSTOPP**</dt> <dt>4</dt> </dl>                                                                    | Beenden Sie den Download.<br/>                                                                                                                                                                                                                                                                  |
| <span id="APPCOMMAND_CLOSE"></span><span id="appcommand_close"></span><dl> <dt>**APPCOMMAND \_ CLOSE**</dt> <dt>31</dt> </dl>                                                                                         | Schließen Sie das Fenster (nicht die Anwendung).<br/>                                                                                                                                                                                                                                         |
| <span id="APPCOMMAND_COPY"></span><span id="appcommand_copy"></span><dl> <dt>**APPCOMMAND \_ COPY**</dt> <dt>36</dt> </dl>                                                                                            | Kopieren Sie die Auswahl.<br/>                                                                                                                                                                                                                                                             |
| <span id="APPCOMMAND_CORRECTION_LIST"></span><span id="appcommand_correction_list"></span><dl> <dt>**APPCOMMAND \_ \_KORREKTURLISTE**</dt> <dt>45</dt> </dl>                                                          | Ruft die Korrekturliste auf, wenn ein Wort während der Spracheingabe falsch identifiziert wird. <br/>                                                                                                                                                                                       |
| <span id="APPCOMMAND_CUT"></span><span id="appcommand_cut"></span><dl> <dt>**APPCOMMAND \_ CUT**</dt> <dt>37</dt> </dl>                                                                                               | Schneiden Sie die Auswahl aus.<br/>                                                                                                                                                                                                                                                              |
| <span id="APPCOMMAND_DICTATE_OR_COMMAND_CONTROL_TOGGLE"></span><span id="appcommand_dictate_or_command_control_toggle"></span><dl> <dt>**APPCOMMAND \_ DIKTIEREN \_ ODER \_ \_ BEFEHLSSTEUERUNG \_ UMSCHALTEN**</dt> <dt>43</dt> </dl> | Schaltet zwischen zwei Modi der Spracheingabe um: Diktat und Befehls-/Steuerungsmodus (Das Erteilen von Befehlen an eine Anwendung oder das Zugreifen auf Menüs). <br/>                                                                                                                                               |
| <span id="APPCOMMAND_FIND"></span><span id="appcommand_find"></span><dl> <dt>**APPCOMMAND \_ FIND**</dt> <dt>28</dt> </dl>                                                                                            | Öffnen Sie das Dialogfeld **Suchen.**<br/>                                                                                                                                                                                                                                                       |
| <span id="APPCOMMAND_FORWARD_MAIL"></span><span id="appcommand_forward_mail"></span><dl> <dt>**APPCOMMAND \_ WEITERLEITEN \_ VON E-MAIL**</dt> <dt>40</dt> </dl>                                                                   | Weiterleiten einer E-Mail-Nachricht.<br/>                                                                                                                                                                                                                                                         |
| <span id="APPCOMMAND_HELP"></span><span id="appcommand_help"></span><dl> <dt>**APPCOMMAND \_ HILFE**</dt> <dt>27</dt> </dl>                                                                                            | Öffnen Sie das Dialogfeld **Hilfe.**<br/>                                                                                                                                                                                                                                                       |
| <span id="APPCOMMAND_LAUNCH_APP1"></span><span id="appcommand_launch_app1"></span><dl> <dt>**APPCOMMAND \_ STARTEN \_ VON APP1**</dt> <dt>17</dt> </dl>                                                                      | Starten Sie App1.<br/>                                                                                                                                                                                                                                                                     |
| <span id="APPCOMMAND_LAUNCH_APP2"></span><span id="appcommand_launch_app2"></span><dl> <dt>**APPCOMMAND \_ STARTEN VON \_ APP2**</dt> <dt>18</dt> </dl>                                                                      | Starten Sie App2.<br/>                                                                                                                                                                                                                                                                     |
| <span id="APPCOMMAND_LAUNCH_MAIL"></span><span id="appcommand_launch_mail"></span><dl> <dt>**APPCOMMAND \_ STARTEN VON \_ MAIL**</dt> <dt>15</dt> </dl>                                                                      | Öffnen Sie die E-Mail.<br/>                                                                                                                                                                                                                                                                      |
| <span id="APPCOMMAND_LAUNCH_MEDIA_SELECT"></span><span id="appcommand_launch_media_select"></span><dl> <dt>**APPCOMMAND \_ LAUNCH \_ MEDIA \_ SELECT**</dt> <dt>16</dt> </dl>                                             | Wechseln Sie zum Medienauswahlmodus.<br/>                                                                                                                                                                                                                                                        |
| <span id="APPCOMMAND_MEDIA_CHANNEL_DOWN"></span><span id="appcommand_media_channel_down"></span><dl> <dt>**APPCOMMAND \_ MEDIA \_ CHANNEL \_ DOWN**</dt> <dt>52</dt> </dl>                                                | Dekrementierung des Kanalwerts, z. B. für einen TV- oder Radio-Tuner. <br/>                                                                                                                                                                                                             |
| <span id="APPCOMMAND_MEDIA_CHANNEL_UP"></span><span id="appcommand_media_channel_up"></span><dl> <dt>**APPCOMMAND \_ MEDIA \_ CHANNEL \_ UP**</dt> <dt>51</dt> </dl>                                                      | Erhöhen Sie den Kanalwert, z. B. für einen TV- oder Radio-Tuner. <br/>                                                                                                                                                                                                             |
| <span id="APPCOMMAND_MEDIA_FAST_FORWARD"></span><span id="appcommand_media_fast_forward"></span><dl> <dt>**APPCOMMAND \_ MEDIA \_ FAST \_ FORWARD**</dt> <dt>49</dt> </dl>                                                | Erhöhen Sie die Geschwindigkeit der Streamwiedergabe. Dies kann auf unterschiedliche Weise implementiert werden, z. B. mit einer festen Geschwindigkeit oder durch eine Reihe steigender Geschwindigkeiten. <br/>                                                                                                               |
| <span id="APPCOMMAND_MEDIA_NEXTTRACK"></span><span id="appcommand_media_nexttrack"></span><dl> <dt>**APPCOMMAND \_ MEDIA \_ NEXTTRACK**</dt> <dt>11</dt> </dl>                                                          | Wechseln Sie zur nächsten Spur.<br/>                                                                                                                                                                                                                                                               |
| <span id="APPCOMMAND_MEDIA_PAUSE"></span><span id="appcommand_media_pause"></span><dl> <dt>**APPCOMMAND \_ MEDIA \_ PAUSE**</dt> <dt>47</dt> </dl>                                                                      | Anhalten. Wenn sie bereits angehalten wurde, können Sie keine weiteren Maßnahmen ergreifen. Dies ist ein direkter PAUSE-Befehl ohne Status. Wenn diskrete Wiedergabe- und Pausenschaltflächen vorhanden sind, sollten Anwendungen aktionen für diesen Befehl sowie **APPCOMMAND \_ MEDIA PLAY PAUSE \_ \_ ausführen.** <br/>                               |
| <span id="APPCOMMAND_MEDIA_PLAY"></span><span id="appcommand_media_play"></span><dl> <dt>**APPCOMMAND \_ MEDIA \_ PLAY**</dt> <dt>46</dt> </dl>                                                                         | Beginnen Sie mit der Wiedergabe an der aktuellen Position. Wenn sie bereits angehalten wurde, wird sie fortgesetzt. Dies ist ein direkter PLAY-Befehl ohne Status. Wenn **diskrete** Wiedergabe- und Pausenschaltflächen vorhanden sind, sollten Anwendungen aktionen für diesen Befehl sowie **APPCOMMAND \_ MEDIA PLAY PAUSE \_ \_ ausführen.** <br/> |
| <span id="APPCOMMAND_MEDIA_PLAY_PAUSE"></span><span id="appcommand_media_play_pause"></span><dl> <dt>**APPCOMMAND \_ MEDIA \_ PLAY \_ PAUSE**</dt> <dt>14</dt> </dl>                                                      | Wiedergabe wiedergeben oder anhalten. Wenn **diskrete** Wiedergabe- und Pausenschaltflächen vorhanden sind, sollten Anwendungen aktionen für diesen Befehl sowie **APPCOMMAND \_ MEDIA \_ PLAY** und **APPCOMMAND \_ MEDIA PAUSE \_ ausführen.** <br/>                                                                          |
| <span id="APPCOMMAND_MEDIA_PREVIOUSTRACK"></span><span id="appcommand_media_previoustrack"></span><dl> <dt>**APPCOMMAND \_ MEDIA \_ PREVIOUSTRACK**</dt> <dt>12</dt> </dl>                                              | Wechseln Sie zur vorherigen Spur.<br/>                                                                                                                                                                                                                                                           |
| <span id="APPCOMMAND_MEDIA_RECORD"></span><span id="appcommand_media_record"></span><dl> <dt>**APPCOMMAND \_ MEDIA \_ RECORD**</dt> <dt>48</dt> </dl>                                                                   | Beginnen Sie mit der Aufzeichnung des aktuellen Streams.<br/>                                                                                                                                                                                                                                             |
| <span id="APPCOMMAND_MEDIA_REWIND"></span><span id="appcommand_media_rewind"></span><dl> <dt>**APPCOMMAND \_ MEDIA \_ REWIND**</dt> <dt>50</dt> </dl>                                                                   | Wechseln Sie in einem Stream mit einer höheren Geschwindigkeit rückwärts. Dies kann auf unterschiedliche Weise implementiert werden, z. B. mit einer festen Geschwindigkeit oder durch eine Reihe steigender Geschwindigkeiten. <br/>                                                                                                   |
| <span id="APPCOMMAND_MEDIA_STOP"></span><span id="appcommand_media_stop"></span><dl> <dt>**APPCOMMAND \_ \_MEDIENSTOPP**</dt> <dt>13</dt> </dl>                                                                         | Beenden Sie die Wiedergabe.<br/>                                                                                                                                                                                                                                                                  |
| <span id="APPCOMMAND_MIC_ON_OFF_TOGGLE"></span><span id="appcommand_mic_on_off_toggle"></span><dl> <dt>**APPCOMMAND \_ MIC \_ ON \_ OFF \_ TOGGLE**</dt> <dt>44</dt> </dl>                                                  | Schalten Sie das Mikrofon um.<br/>                                                                                                                                                                                                                                                          |
| <span id="APPCOMMAND_MICROPHONE_VOLUME_DOWN"></span><span id="appcommand_microphone_volume_down"></span><dl> <dt>**APPCOMMAND \_ MIKROFONVOLUMEN \_ \_ NACH UNTEN**</dt> <dt>25</dt> </dl>                                    | Verringern Sie die Mikrofonlautstärke.<br/>                                                                                                                                                                                                                                                     |
| <span id="APPCOMMAND_MICROPHONE_VOLUME_MUTE"></span><span id="appcommand_microphone_volume_mute"></span><dl> <dt>**APPCOMMAND \_ \_ \_ MIKROFONLAUTSTÄRKE**</dt> <dt>24</dt> </dl>                                    | Stummschalten des Mikrofons.<br/>                                                                                                                                                                                                                                                            |
| <span id="APPCOMMAND_MICROPHONE_VOLUME_UP"></span><span id="appcommand_microphone_volume_up"></span><dl> <dt>**APPCOMMAND \_ \_ \_ MIKROFONLAUTSTÄRKE BIS**</dt> <dt>26</dt> </dl>                                          | Erhöhen Sie die Mikrofonlautstärke.<br/>                                                                                                                                                                                                                                                     |
| <span id="APPCOMMAND_NEW"></span><span id="appcommand_new"></span><dl> <dt>**APPCOMMAND \_ NEU**</dt> <dt>29</dt> </dl>                                                                                               | Erstellen Sie ein neues Fenster.<br/>                                                                                                                                                                                                                                                            |
| <span id="APPCOMMAND_OPEN"></span><span id="appcommand_open"></span><dl> <dt>**APPCOMMAND \_ OPEN**</dt> <dt>30</dt> </dl>                                                                                            | Öffnen Sie ein Fenster.<br/>                                                                                                                                                                                                                                                                  |
| <span id="APPCOMMAND_PASTE"></span><span id="appcommand_paste"></span><dl> <dt>**APPCOMMAND \_ PASTE**</dt> <dt>38</dt> </dl>                                                                                         | Einfügen<br/>                                                                                                                                                                                                                                                                           |
| <span id="APPCOMMAND_PRINT"></span><span id="appcommand_print"></span><dl> <dt>**APPCOMMAND \_ PRINT**</dt> <dt>33</dt> </dl>                                                                                         | Drucken des aktuellen Dokuments.<br/>                                                                                                                                                                                                                                                         |
| <span id="APPCOMMAND_REDO"></span><span id="appcommand_redo"></span><dl> <dt>**APPCOMMAND \_ REDO**</dt> <dt>35</dt> </dl>                                                                                            | Letzte Aktion wiederholen.<br/>                                                                                                                                                                                                                                                               |
| <span id="APPCOMMAND_REPLY_TO_MAIL"></span><span id="appcommand_reply_to_mail"></span><dl> <dt>**APPCOMMAND \_ ANTWORT \_ AN \_ MAIL**</dt> <dt>39</dt> </dl>                                                               | Antwort auf eine E-Mail.<br/>                                                                                                                                                                                                                                                        |
| <span id="APPCOMMAND_SAVE"></span><span id="appcommand_save"></span><dl> <dt>**APPCOMMAND \_ SAVE**</dt> <dt>32</dt> </dl>                                                                                            | Speichern Sie das aktuelle Dokument.<br/>                                                                                                                                                                                                                                                          |
| <span id="APPCOMMAND_SEND_MAIL"></span><span id="appcommand_send_mail"></span><dl> <dt>**APPCOMMAND \_ MAIL \_ 41**</dt> <dt>SENDEN</dt> </dl>                                                                            | Senden einer E-Mail.<br/>                                                                                                                                                                                                                                                            |
| <span id="APPCOMMAND_SPELL_CHECK"></span><span id="appcommand_spell_check"></span><dl> <dt>**APPCOMMAND \_ \_RECHTSCHREIBPRÜFUNG**</dt> <dt>42</dt> </dl>                                                                      | Initiieren Sie eine Rechtschreibprüfung.<br/>                                                                                                                                                                                                                                                         |
| <span id="APPCOMMAND_TREBLE_DOWN"></span><span id="appcommand_treble_down"></span><dl> <dt>**APPCOMMAND \_ TREBLE \_ DOWN**</dt> <dt>22</dt> </dl>                                                                      | Verringern Sie den Treble.<br/>                                                                                                                                                                                                                                                            |
| <span id="APPCOMMAND_TREBLE_UP"></span><span id="appcommand_treble_up"></span><dl> <dt>**APPCOMMAND \_ TREBLE \_ UP**</dt> <dt>23</dt> </dl>                                                                            | Erhöhen Sie die Verdreibung.<br/>                                                                                                                                                                                                                                                            |
| <span id="APPCOMMAND_UNDO"></span><span id="appcommand_undo"></span><dl> <dt>**APPCOMMAND \_ RÜCKGÄNGIG**</dt> <dt>34</dt> </dl>                                                                                            | Letzte Aktion rückgängig machen.<br/>                                                                                                                                                                                                                                                               |
| <span id="APPCOMMAND_VOLUME_DOWN"></span><span id="appcommand_volume_down"></span><dl> <dt>**APPCOMMAND \_ VOLUME \_ DOWN**</dt> <dt>9</dt> </dl>                                                                       | Senken Sie das Volume.<br/>                                                                                                                                                                                                                                                               |
| <span id="APPCOMMAND_VOLUME_MUTE"></span><span id="appcommand_volume_mute"></span><dl> <dt>**APPCOMMAND \_ VOLUME \_ MUTE**</dt> <dt>8</dt> </dl>                                                                       | Stummschalten des Volumes.<br/>                                                                                                                                                                                                                                                                |
| <span id="APPCOMMAND_VOLUME_UP"></span><span id="appcommand_volume_up"></span><dl> <dt>**APPCOMMAND \_ VOLUME \_ BIS**</dt> <dt>10</dt> </dl>                                                                            | Heben Sie das Volume auf.<br/>                                                                                                                                                                                                                                                               |



 

Die *Komponente uDevice* gibt das Eingabegerät an, das das Eingabeereignis generiert hat, und kann einer der folgenden Werte sein.



| Wert                                                                                                                                                                                                                                 | Bedeutung                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span id="FAPPCOMMAND_KEY"></span><span id="fappcommand_key"></span><dl> <dt>**FAPPCOMMAND \_ KEY**</dt> <dt>0</dt> </dl>            | Der Benutzer hat eine Taste gedrückt.<br/>                                                                           |
| <span id="FAPPCOMMAND_MOUSE"></span><span id="fappcommand_mouse"></span><dl> <dt>**FAPPCOMMAND \_ MAUS-0x8000**</dt> <dt></dt> </dl> | Der Benutzer hat auf eine Maustaste geklickt.<br/>                                                                  |
| <span id="FAPPCOMMAND_OEM"></span><span id="fappcommand_oem"></span><dl> <dt>**FAPPCOMMAND \_ OEM-0x1000**</dt> <dt></dt> </dl>       | Eine nicht identifizierte Hardwarequelle hat das Ereignis generiert. Dabei kann es sich um ein Maus- oder Tastaturereignis geben.<br/> |



 

Die *dwKeys-Komponente* gibt an, ob verschiedene virtuelle Schlüssel nicht mehr verwendet werden können, und kann mindestens einer der folgenden Werte sein.



| Wert                                                                                                                                                                                                               | Bedeutung                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="MK_CONTROL"></span><span id="mk_control"></span><dl> <dt>**MK \_ CONTROL**</dt> <dt>0x0008</dt> </dl>    | Die STRG-TASTE ist gedrückt.<br/>            |
| <span id="MK_LBUTTON"></span><span id="mk_lbutton"></span><dl> <dt>**MK \_ LBUTTON-0x0001**</dt> <dt></dt> </dl>    | Die linke Maustaste ist nach unten.<br/>   |
| <span id="MK_MBUTTON"></span><span id="mk_mbutton"></span><dl> <dt>**MK \_ MBUTTON-0x0010**</dt> <dt></dt> </dl>    | Die mittlere Maustaste ist nach unten.<br/> |
| <span id="MK_RBUTTON"></span><span id="mk_rbutton"></span><dl> <dt>**MK \_ RBUTTON-0x0002**</dt> <dt></dt> </dl>    | Die rechte Maustaste ist nach unten.<br/>  |
| <span id="MK_SHIFT"></span><span id="mk_shift"></span><dl> <dt>**MK \_ UMSCHALT 0X0004**</dt> <dt></dt> </dl>          | Die UMSCHALTTASTE ist heruntergefahren.<br/>           |
| <span id="MK_XBUTTON1"></span><span id="mk_xbutton1"></span><dl> <dt>**MK \_ XBUTTON1-0x0020**</dt> <dt></dt> </dl> | Die erste X-Schaltfläche ist nicht mehr zu sehen.<br/>      |
| <span id="MK_XBUTTON2"></span><span id="mk_xbutton2"></span><dl> <dt>**MK \_ XBUTTON2-0x0040**</dt> <dt></dt> </dl> | Die zweite X-Schaltfläche ist nicht mehr zu sehen.<br/>     |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn eine Anwendung diese Nachricht verarbeitet, sollte sie **TRUE zurückgeben.** Weitere Informationen zur Verarbeitung des Rückgabewerts finden Sie im Abschnitt Hinweise.

## <a name="remarks"></a>Hinweise

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) generiert die **WM \_ APPCOMMAND-Nachricht,** wenn die [**WM \_ XBUTTONUP-**](wm-xbuttonup.md) oder [**WM \_ NCXBUTTONUP-Nachricht**](wm-ncxbuttonup.md) verarbeitet wird oder wenn der Benutzer einen Anwendungsbefehlsschlüssel eintipft.

Wenn ein untergeordnetes Fenster diese Nachricht nicht verarbeiten und stattdessen [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)aufruft, sendet **DefWindowProc** die Nachricht an das übergeordnete Fenster. Wenn ein Fenster der obersten Ebene diese Nachricht nicht verarbeiten und stattdessen **DefWindowProc** aufruft, ruft **DefWindowProc** einen Shellhook mit dem Hookcode **HSHELL \_ APPCOMMAND auf.**

Um die Koordinaten des Cursors zu erhalten, wenn die Nachricht durch einen Mausklick generiert wurde, kann die Anwendung [**GetMessagePos aufrufen.**](/windows/desktop/api/winuser/nf-winuser-getmessagepos) Eine Anwendung kann testen, ob die Nachricht mit der Maus generiert wurde, indem überprüft wird, ob *lParam* **FAPPCOMMAND \_ MOUSE enthält.**

Im Gegensatz zu anderen Windows-Nachrichten sollte eine Anwendung **true** aus dieser Meldung zurückgeben, wenn sie sie verarbeitet. Auf diese Weise kann software, die diese Nachricht auf Windows-Systemen vor Windows 2000 simuliert, bestimmen, ob die Fensterprozedur die Nachricht verarbeitet oder [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) aufgerufen hat, um sie zu verarbeiten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**GET \_ APPCOMMAND \_ LPARAM**](/windows/win32/api/winuser/nf-winuser-get_appcommand_lparam)
</dt> <dt>

[**GET \_ DEVICE \_ LPARAM**](/windows/win32/api/winuser/nf-winuser-get_device_lparam)
</dt> <dt>

[**GET \_ KEYSTATE \_ LPARAM**](/windows/win32/api/winuser/nf-winuser-get_keystate_lparam)
</dt> <dt>

[**ShellProc**](/previous-versions/windows/desktop/legacy/ms644991(v=vs.85))
</dt> <dt>

[**WM \_ XBUTTONUP**](wm-xbuttonup.md)
</dt> <dt>

[**WM \_ NCXBUTTONUP**](wm-ncxbuttonup.md)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Mauseingabe](mouse-input.md)
</dt> </dl>

 

