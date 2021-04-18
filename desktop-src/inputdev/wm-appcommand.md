---
title: WM_APPCOMMAND Meldung (Winuser. h)
description: Benachrichtigt ein Fenster, dass der Benutzer ein Anwendungs Befehls Ereignis generiert hat, z. b. durch Klicken auf eine Anwendungs Befehlsschaltfläche mithilfe der Maus oder Eingabe eines Anwendungs Befehls Schlüssels auf der Tastatur.
ms.assetid: ffcdfc44-dbfa-42d4-8749-b33bf0e4de0c
keywords:
- Tastatur-und Maus Eingaben für WM_APPCOMMAND Nachricht
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
ms.openlocfilehash: d7f5e71f9a443e12ea56cb8ca23daea148da92aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391798"
---
# <a name="wm_appcommand-message"></a>WM- \_ appcommand-Meldung

Benachrichtigt ein Fenster, dass der Benutzer ein Anwendungs Befehls Ereignis generiert hat, z. b. durch Klicken auf eine Anwendungs Befehlsschaltfläche mithilfe der Maus oder Eingabe eines Anwendungs Befehls Schlüssels auf der Tastatur.


```C++
#define WM_APPCOMMAND                   0x0319
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein Handle für das Fenster, in dem der Benutzer auf die Schaltfläche geklickt oder die Taste gedrückt hat. Dies kann ein untergeordnetes Fenster des Fensters sein, in dem die Nachricht empfangen wird. Weitere Informationen zum Verarbeiten dieser Nachricht finden Sie im Abschnitt "Hinweise".

</dd> <dt>

*lParam* 
</dt> <dd>

Verwenden Sie den folgenden Code, um die im *LPARAM* -Parameter enthaltenen Informationen zu erhalten.


```
cmd  = GET_APPCOMMAND_LPARAM(lParam);

uDevice = GET_DEVICE_LPARAM(lParam);

dwKeys = GET_KEYSTATE_LPARAM(lParam);
```



Der Anwendungs Befehl ist " *cmd*", bei dem es sich um einen der folgenden Werte handeln kann.



| Wert                                                                                                                                                                                                                                                                                                                  | Bedeutung                                                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="APPCOMMAND_BASS_BOOST"></span><span id="appcommand_bass_boost"></span><dl> <dt>**Appcommand \_ Bass \_ Verstärkung**</dt> <dt>20</dt> </dl>                                                                         | Schalten Sie die Bass Verstärkung ein/aus.<br/>                                                                                                                                                                                                                                               |
| <span id="APPCOMMAND_BASS_DOWN"></span><span id="appcommand_bass_down"></span><dl> <dt>**Appcommand \_ Bass \_ nach unten**</dt> <dt>19</dt> </dl>                                                                            | Verringern Sie den Bass.<br/>                                                                                                                                                                                                                                                              |
| <span id="APPCOMMAND_BASS_UP"></span><span id="appcommand_bass_up"></span><dl> <dt>**Appcommand \_ Bass nach \_ oben**</dt> <dt>21</dt> </dl>                                                                                  | Vergrößern Sie den Bass.<br/>                                                                                                                                                                                                                                                              |
| <span id="APPCOMMAND_BROWSER_BACKWARD"></span><span id="appcommand_browser_backward"></span><dl> <dt>**Appcommand \_ Browser \_ rückwärts**</dt> <dt>1</dt> </dl>                                                        | Rückwärts navigieren.<br/>                                                                                                                                                                                                                                                              |
| <span id="APPCOMMAND_BROWSER_FAVORITES"></span><span id="appcommand_browser_favorites"></span><dl> <dt>**Appcommand \_ Browser \_ Favoriten**</dt> <dt>6</dt> </dl>                                                     | Öffnen Sie Favoriten.<br/>                                                                                                                                                                                                                                                                 |
| <span id="APPCOMMAND_BROWSER_FORWARD"></span><span id="appcommand_browser_forward"></span><dl> <dt>**Appcommand \_ Browser- \_ Vorwärts**</dt> <dt>2</dt> </dl>                                                           | Vorwärts navigieren.<br/>                                                                                                                                                                                                                                                               |
| <span id="APPCOMMAND_BROWSER_HOME"></span><span id="appcommand_browser_home"></span><dl> <dt>**Appcommand \_ Browser \_ Home**</dt> <dt>7</dt> </dl>                                                                    | Navigieren Sie zu Home.<br/>                                                                                                                                                                                                                                                                  |
| <span id="APPCOMMAND_BROWSER_REFRESH"></span><span id="appcommand_browser_refresh"></span><dl> <dt>**Appcommand \_ Browser \_ Aktualisierung**</dt> <dt>3</dt> </dl>                                                           | Aktualisieren Sie die Seite.<br/>                                                                                                                                                                                                                                                                   |
| <span id="APPCOMMAND_BROWSER_SEARCH"></span><span id="appcommand_browser_search"></span><dl> <dt>**Appcommand \_ Browser \_ Suche**</dt> <dt>5</dt> </dl>                                                              | Öffnen Sie die Suche.<br/>                                                                                                                                                                                                                                                                    |
| <span id="APPCOMMAND_BROWSER_STOP"></span><span id="appcommand_browser_stop"></span><dl> <dt>**Appcommand \_ Browser \_ Ende**</dt> <dt>4</dt> </dl>                                                                    | Beendet den Download.<br/>                                                                                                                                                                                                                                                                  |
| <span id="APPCOMMAND_CLOSE"></span><span id="appcommand_close"></span><dl> <dt>**Appcommand \_ Schließen**</dt> Sie <dt>31</dt> </dl>                                                                                         | Schließen Sie das Fenster (nicht die Anwendung).<br/>                                                                                                                                                                                                                                         |
| <span id="APPCOMMAND_COPY"></span><span id="appcommand_copy"></span><dl> <dt>**Appcommand \_ Kopieren**</dt> von <dt>36</dt> </dl>                                                                                            | Kopieren Sie die Auswahl.<br/>                                                                                                                                                                                                                                                             |
| <span id="APPCOMMAND_CORRECTION_LIST"></span><span id="appcommand_correction_list"></span><dl> <dt>**Appcommand \_ Korrektur \_ Liste**</dt> <dt>45</dt> </dl>                                                          | Ruft die Korrektur Liste auf, wenn ein Wort während der Spracheingabe falsch identifiziert wird. <br/>                                                                                                                                                                                       |
| <span id="APPCOMMAND_CUT"></span><span id="appcommand_cut"></span><dl> <dt>**Appcommand \_ 37 Ausschneiden**</dt> <dt></dt> </dl>                                                                                               | Auswahl ausschneiden.<br/>                                                                                                                                                                                                                                                              |
| <span id="APPCOMMAND_DICTATE_OR_COMMAND_CONTROL_TOGGLE"></span><span id="appcommand_dictate_or_command_control_toggle"></span><dl> <dt>**Appcommand \_ Ein- \_ oder \_ Befehls Steuerelement \_ \_ Umschalten**</dt> <dt>43</dt> </dl> | Schaltet zwischen zwei Modi der Spracheingabe um: Diktat und Befehls-/Steuerungsart (Befehle für eine Anwendung oder für den Zugriff auf Menüs). <br/>                                                                                                                                               |
| <span id="APPCOMMAND_FIND"></span><span id="appcommand_find"></span><dl> <dt>**Appcommand \_**</dt> <dt>28</dt> suchen </dl>                                                                                            | Öffnen Sie das Dialogfeld **Suchen** .<br/>                                                                                                                                                                                                                                                       |
| <span id="APPCOMMAND_FORWARD_MAIL"></span><span id="appcommand_forward_mail"></span><dl> <dt>**Appcommand \_ Weiterleiten von \_ e-Mail**</dt> <dt>40</dt> </dl>                                                                   | Weiterleiten einer e-Mail-Nachricht<br/>                                                                                                                                                                                                                                                         |
| <span id="APPCOMMAND_HELP"></span><span id="appcommand_help"></span><dl> <dt>**Appcommand \_ Hilfe**</dt> <dt>27</dt> </dl>                                                                                            | Öffnen Sie das **Hilfe** Dialogfeld.<br/>                                                                                                                                                                                                                                                       |
| <span id="APPCOMMAND_LAUNCH_APP1"></span><span id="appcommand_launch_app1"></span><dl> <dt>**Appcommand \_ Start \_ App1**</dt> <dt>17</dt> </dl>                                                                      | Starten Sie App1.<br/>                                                                                                                                                                                                                                                                     |
| <span id="APPCOMMAND_LAUNCH_APP2"></span><span id="appcommand_launch_app2"></span><dl> <dt>**Appcommand \_ Start \_ APP2**</dt> <dt>18</dt> </dl>                                                                      | Starten Sie App2.<br/>                                                                                                                                                                                                                                                                     |
| <span id="APPCOMMAND_LAUNCH_MAIL"></span><span id="appcommand_launch_mail"></span><dl> <dt>**Appcommand \_ \_E-Mail starten**</dt> <dt>15</dt> </dl>                                                                      | Öffnen Sie e-Mail.<br/>                                                                                                                                                                                                                                                                      |
| <span id="APPCOMMAND_LAUNCH_MEDIA_SELECT"></span><span id="appcommand_launch_media_select"></span><dl> <dt>**Appcommand \_ Start \_ Medien \_ Wählen Sie**</dt> <dt>16</dt> aus. </dl>                                             | Wechseln Sie zum Modus "Medienauswahl".<br/>                                                                                                                                                                                                                                                        |
| <span id="APPCOMMAND_MEDIA_CHANNEL_DOWN"></span><span id="appcommand_media_channel_down"></span><dl> <dt>**Appcommand \_ Medien \_ Kanal \_ nach unten**</dt> <dt>52</dt> </dl>                                                | Verringern Sie den channelwert, z. b. für einen Fernseh-oder Radio-Tuner. <br/>                                                                                                                                                                                                             |
| <span id="APPCOMMAND_MEDIA_CHANNEL_UP"></span><span id="appcommand_media_channel_up"></span><dl> <dt>**Appcommand \_ Medien \_ Kanal \_ aufwärts**</dt> <dt>51</dt> </dl>                                                      | Erhöhen Sie den channelwert, z. b. für einen Fernseh-oder Radio-Tuner. <br/>                                                                                                                                                                                                             |
| <span id="APPCOMMAND_MEDIA_FAST_FORWARD"></span><span id="appcommand_media_fast_forward"></span><dl> <dt>**Appcommand \_ Medien \_ schnell \_ Vorwärts**</dt> <dt>49</dt> </dl>                                                | Erhöhen Sie die Geschwindigkeit der streamwiedergabe. Dies kann auf unterschiedlichste Weise implementiert werden, z. b. mit einer Fixed-Geschwindigkeit oder durch eine Reihe von zunehmenden Geschwindigkeiten. <br/>                                                                                                               |
| <span id="APPCOMMAND_MEDIA_NEXTTRACK"></span><span id="appcommand_media_nexttrack"></span><dl> <dt>**Appcommand \_ Medien \_ NextTrack**</dt> <dt>11</dt> </dl>                                                          | Gehe zu nächster Spur.<br/>                                                                                                                                                                                                                                                               |
| <span id="APPCOMMAND_MEDIA_PAUSE"></span><span id="appcommand_media_pause"></span><dl> <dt>**Appcommand \_ Medien \_ Pause**</dt> <dt>47</dt> </dl>                                                                      | Anhalten. Wenn Sie bereits angehalten ist, müssen Sie keine weiteren Maßnahmen ergreifen. Dies ist ein direkter Pause-Befehl, der keinen Status aufweist. Wenn diskrete Wiedergabe-und Pausen Schaltflächen vorhanden sind, sollten Anwendungen mit diesem Befehl und der **appcommand- \_ Medien \_ Wiedergabe \_ Pause** Aktionen ausführen. <br/>                               |
| <span id="APPCOMMAND_MEDIA_PLAY"></span><span id="appcommand_media_play"></span><dl> <dt>**Appcommand \_ Medien \_ Wiedergabe**</dt> <dt>46</dt> </dl>                                                                         | Mit der Wiedergabe an der aktuellen Position beginnen. Wenn Sie bereits angehalten wurde, wird Sie fortgesetzt. Dies ist ein direkter Wiedergabe Befehl, der keinen Status aufweist. Wenn diskrete **Wiedergabe** -und **Pausen** Schaltflächen vorhanden sind, sollten Anwendungen mit diesem Befehl und der **appcommand- \_ Medien \_ Wiedergabe \_ Pause** Aktionen ausführen.<br/> |
| <span id="APPCOMMAND_MEDIA_PLAY_PAUSE"></span><span id="appcommand_media_play_pause"></span><dl> <dt>**Appcommand \_ Medien \_ Wiedergabe \_ Pause**</dt> <dt>14</dt> </dl>                                                      | Wiedergabe oder Pause Wiedergabe. Wenn diskrete **Wiedergabe** -und **Pausen** Schaltflächen vorhanden sind, sollten Anwendungen mit diesem Befehl sowie **appcommand- \_ Medien \_ Wiedergabe** und **appcommand- \_ Medien \_** anhalten Aktionen ausführen.<br/>                                                                          |
| <span id="APPCOMMAND_MEDIA_PREVIOUSTRACK"></span><span id="appcommand_media_previoustrack"></span><dl> <dt>**Appcommand \_ Medien \_ PreviousTrack**</dt> <dt>12</dt> </dl>                                              | Gehe zum vorherigen Track.<br/>                                                                                                                                                                                                                                                           |
| <span id="APPCOMMAND_MEDIA_RECORD"></span><span id="appcommand_media_record"></span><dl> <dt>**Appcommand \_ Medien \_ Daten Satz**</dt> <dt>48</dt> </dl>                                                                   | Startet die Aufzeichnung des aktuellen Streams.<br/>                                                                                                                                                                                                                                             |
| <span id="APPCOMMAND_MEDIA_REWIND"></span><span id="appcommand_media_rewind"></span><dl> <dt>**Appcommand \_ Medien \_ Rewind**</dt> <dt>50</dt> </dl>                                                                   | Gehen Sie mit einer höheren Geschwindigkeit in einem Stream rückwärts. Dies kann auf unterschiedlichste Weise implementiert werden, z. b. mit einer Fixed-Geschwindigkeit oder durch eine Reihe von zunehmenden Geschwindigkeiten. <br/>                                                                                                   |
| <span id="APPCOMMAND_MEDIA_STOP"></span><span id="appcommand_media_stop"></span><dl> <dt>**Appcommand \_ Medien \_ Ende**</dt> <dt>13</dt> </dl>                                                                         | Wiedergabe wird beendet.<br/>                                                                                                                                                                                                                                                                  |
| <span id="APPCOMMAND_MIC_ON_OFF_TOGGLE"></span><span id="appcommand_mic_on_off_toggle"></span><dl> <dt>**Appcommand \_ MIC \_ on \_ Off \_**</dt> , Umschalten <dt>44</dt> </dl>                                                  | Schalten Sie das Mikrofon ein/aus.<br/>                                                                                                                                                                                                                                                          |
| <span id="APPCOMMAND_MICROPHONE_VOLUME_DOWN"></span><span id="appcommand_microphone_volume_down"></span><dl> <dt>**Appcommand \_ Mikrofon- \_ Volume \_ nach unten**</dt> <dt>25</dt> </dl>                                    | Verringern Sie das Mikrofon Volume.<br/>                                                                                                                                                                                                                                                     |
| <span id="APPCOMMAND_MICROPHONE_VOLUME_MUTE"></span><span id="appcommand_microphone_volume_mute"></span><dl> <dt>**Appcommand \_ Mikrofon \_ Volume \_ stumm schalten**</dt> <dt>24</dt> </dl>                                    | Stumm schalten des Mikrofons.<br/>                                                                                                                                                                                                                                                            |
| <span id="APPCOMMAND_MICROPHONE_VOLUME_UP"></span><span id="appcommand_microphone_volume_up"></span><dl> <dt>**Appcommand \_ Mikrofon \_ laut \_ Stärke**</dt> <dt>26</dt> </dl>                                          | Vergrößern Sie das Mikrofon Volume.<br/>                                                                                                                                                                                                                                                     |
| <span id="APPCOMMAND_NEW"></span><span id="appcommand_new"></span><dl> <dt>**Appcommand \_ Neu**</dt> <dt>29</dt> </dl>                                                                                               | Erstellen Sie ein neues Fenster.<br/>                                                                                                                                                                                                                                                            |
| <span id="APPCOMMAND_OPEN"></span><span id="appcommand_open"></span><dl> <dt>**Appcommand \_**</dt> <dt>30</dt> öffnen </dl>                                                                                            | Öffnen Sie ein Fenster.<br/>                                                                                                                                                                                                                                                                  |
| <span id="APPCOMMAND_PASTE"></span><span id="appcommand_paste"></span><dl> <dt>**Appcommand \_**</dt> <dt>38</dt> einfügen </dl>                                                                                         | Einfügen<br/>                                                                                                                                                                                                                                                                           |
| <span id="APPCOMMAND_PRINT"></span><span id="appcommand_print"></span><dl> <dt>**Appcommand \_ Drucken**</dt> <dt>33</dt> </dl>                                                                                         | Aktuelles Dokument drucken.<br/>                                                                                                                                                                                                                                                         |
| <span id="APPCOMMAND_REDO"></span><span id="appcommand_redo"></span><dl> <dt>**Appcommand \_ Wiederholen**</dt> <dt>35</dt> </dl>                                                                                            | Letzte Aktion wiederholen.<br/>                                                                                                                                                                                                                                                               |
| <span id="APPCOMMAND_REPLY_TO_MAIL"></span><span id="appcommand_reply_to_mail"></span><dl> <dt>**Appcommand \_ Antworten \_ auf \_ e-Mail**</dt> <dt>39</dt> </dl>                                                               | Antworten auf eine e-Mail-Nachricht.<br/>                                                                                                                                                                                                                                                        |
| <span id="APPCOMMAND_SAVE"></span><span id="appcommand_save"></span><dl> <dt>**Appcommand \_**</dt> <dt>32</dt> speichern </dl>                                                                                            | Speichern Sie das aktuelle Dokument.<br/>                                                                                                                                                                                                                                                          |
| <span id="APPCOMMAND_SEND_MAIL"></span><span id="appcommand_send_mail"></span><dl> <dt>**Appcommand \_ \_E-Mail senden**</dt> <dt>41</dt> </dl>                                                                            | Sendet eine e-Mail-Nachricht.<br/>                                                                                                                                                                                                                                                            |
| <span id="APPCOMMAND_SPELL_CHECK"></span><span id="appcommand_spell_check"></span><dl> <dt>**Appcommand \_ Rechtschreib \_ Prüfung**</dt> <dt>42</dt> </dl>                                                                      | Initiieren Sie eine Rechtschreibprüfung.<br/>                                                                                                                                                                                                                                                         |
| <span id="APPCOMMAND_TREBLE_DOWN"></span><span id="appcommand_treble_down"></span><dl> <dt>**Appcommand \_ \_Nach unten**</dt> <dt>22</dt> </dl>                                                                      | Verringern Sie den Treble.<br/>                                                                                                                                                                                                                                                            |
| <span id="APPCOMMAND_TREBLE_UP"></span><span id="appcommand_treble_up"></span><dl> <dt>**Appcommand \_ In \_ Höhe**</dt> von <dt>23</dt> </dl>                                                                            | Vergrößern Sie den Treble.<br/>                                                                                                                                                                                                                                                            |
| <span id="APPCOMMAND_UNDO"></span><span id="appcommand_undo"></span><dl> <dt>**Appcommand \_ Rückgängig**</dt> <dt>34</dt> </dl>                                                                                            | Letzte Aktion rückgängig machen.<br/>                                                                                                                                                                                                                                                               |
| <span id="APPCOMMAND_VOLUME_DOWN"></span><span id="appcommand_volume_down"></span><dl> <dt>**Appcommand \_ Laut \_ Stärke**</dt> <dt>9</dt> </dl>                                                                       | Verringern Sie das Volume.<br/>                                                                                                                                                                                                                                                               |
| <span id="APPCOMMAND_VOLUME_MUTE"></span><span id="appcommand_volume_mute"></span><dl> <dt>**Appcommand \_ Volume \_ stumm schalten**</dt> <dt>8</dt> </dl>                                                                       | Das Volume wird stumm geschaltet.<br/>                                                                                                                                                                                                                                                                |
| <span id="APPCOMMAND_VOLUME_UP"></span><span id="appcommand_volume_up"></span><dl> <dt>**Appcommand \_ Laut \_ Stärke**</dt> <dt>10</dt> </dl>                                                                            | Erhöhen Sie das Volume.<br/>                                                                                                                                                                                                                                                               |



 

Die *udevice* -Komponente gibt das Eingabegerät an, das das Eingabe Ereignis generiert hat, und kann einen der folgenden Werte aufweisen.



| Wert                                                                                                                                                                                                                                 | Bedeutung                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span id="FAPPCOMMAND_KEY"></span><span id="fappcommand_key"></span><dl> <dt>**Fappcommand \_ Schlüssel**</dt> <dt>0</dt> </dl>            | Der Benutzer hat eine Taste gedrückt.<br/>                                                                           |
| <span id="FAPPCOMMAND_MOUSE"></span><span id="fappcommand_mouse"></span><dl> <dt>**Fappcommand \_ Maus**</dt> <dt>0X8000</dt> </dl> | Benutzer hat auf eine Maustaste geklickt.<br/>                                                                  |
| <span id="FAPPCOMMAND_OEM"></span><span id="fappcommand_oem"></span><dl> <dt>**Fappcommand \_ OEM**</dt> <dt>0x1000</dt> </dl>       | Das Ereignis wurde von einer nicht identifizierten Hardware Quelle generiert. Dabei kann es sich um eine Maus oder ein Tastaturereignis handeln.<br/> |



 

Die Komponente *dwkeys* gibt an, ob verschiedene virtuelle Schlüssel herunter sind, und kann einen oder mehrere der folgenden Werte aufweisen.



| Wert                                                                                                                                                                                                               | Bedeutung                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="MK_CONTROL"></span><span id="mk_control"></span><dl> <dt>**MK \_ Steuer**</dt> Element <dt>0x0008</dt> </dl>    | Die STRG-Taste ist nicht gedrückt.<br/>            |
| <span id="MK_LBUTTON"></span><span id="mk_lbutton"></span><dl> <dt>**MK \_ Lbutton**</dt> <dt>0x0001</dt> </dl>    | Die linke Maustaste ist nicht mehr vorhanden.<br/>   |
| <span id="MK_MBUTTON"></span><span id="mk_mbutton"></span><dl> <dt>**MK \_ MButton**</dt> <dt>0x0010</dt> </dl>    | Die mittlere Maustaste ist nicht mehr angezeigt.<br/> |
| <span id="MK_RBUTTON"></span><span id="mk_rbutton"></span><dl> <dt>**MK \_ Rbutton**</dt> <dt>0x0002</dt> </dl>    | Die Rechte Maustaste ist nicht mehr angezeigt.<br/>  |
| <span id="MK_SHIFT"></span><span id="mk_shift"></span><dl> <dt>**MK \_ UMSCHALT**</dt> <dt>0x0004</dt> </dl>          | Die UMSCHALTTASTE ist nicht mehr festgelegt.<br/>           |
| <span id="MK_XBUTTON1"></span><span id="mk_xbutton1"></span><dl> <dt>**MK \_ XButton1**</dt> <dt>0x0020</dt> </dl> | Die erste X-Schaltfläche ist nicht angezeigt.<br/>      |
| <span id="MK_XBUTTON2"></span><span id="mk_xbutton2"></span><dl> <dt>**MK \_ XButton2**</dt> <dt>0x0040</dt> </dl> | Die zweite X-Schaltfläche ist nicht mehr festgelegt.<br/>     |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie " **true**" zurückgeben. Weitere Informationen zum Verarbeiten des Rückgabewerts finden Sie im Abschnitt "Hinweise".

## <a name="remarks"></a>Bemerkungen

[**Defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) generiert die **WM- \_ appcommand** -Nachricht, wenn Sie die [**WM- \_ xbuttonup**](wm-xbuttonup.md) -oder [**WM- \_ ncxbuttonup**](wm-ncxbuttonup.md) -Nachricht verarbeitet oder wenn der Benutzer einen Anwendungs Befehls Schlüssel eingibt.

Wenn ein untergeordnetes Fenster diese Nachricht nicht verarbeitet und stattdessen [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)aufruft, sendet **defwindowproc** die Nachricht an das übergeordnete Fenster. Wenn ein Fenster der obersten Ebene diese Nachricht nicht verarbeitet und stattdessen **defwindowproc** aufruft, ruft **defwindowproc** einen ShellHook mit dem **hshell- \_ appcommand-Befehl** auf.

Die Anwendung kann [**GetMessagePos**](/windows/desktop/api/winuser/nf-winuser-getmessagepos)aufrufen, um die Koordinaten des Cursors zu erhalten, wenn die Meldung durch einen Mausklick generiert wurde. Eine Anwendung kann testen, ob die Nachricht mit der Maus generiert wurde, indem Sie überprüft, ob *LPARAM* die **fappcommand- \_ Maus** enthält.

Anders als bei anderen Windows-Meldungen sollte eine Anwendung aus dieser Nachricht **true** zurückgeben, wenn Sie sie verarbeitet. Auf diese Weise kann Software, die diese Meldung auf Windows-Systemen vor Windows 2000 simuliert, ermitteln, ob die Fenster Prozedur die Nachricht verarbeitet hat oder [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) aufgerufen hat, um Sie zu verarbeiten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**\_appcommand- \_ LPARAM erhalten**](/windows/win32/api/winuser/nf-winuser-get_appcommand_lparam)
</dt> <dt>

[**\_Geräte- \_ LPARAM**](/windows/win32/api/winuser/nf-winuser-get_device_lparam)
</dt> <dt>

[**\_KeyState \_ LPARAM erhalten**](/windows/win32/api/winuser/nf-winuser-get_keystate_lparam)
</dt> <dt>

[**Shellproc**](/previous-versions/windows/desktop/legacy/ms644991(v=vs.85))
</dt> <dt>

[**WM- \_ xbuttonup**](wm-xbuttonup.md)
</dt> <dt>

[**WM- \_ ncxbuttonup**](wm-ncxbuttonup.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Mauseingabe](mouse-input.md)
</dt> </dl>

 

