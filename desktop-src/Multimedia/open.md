---
title: open-Befehl (Corecrt \_ io.h)
description: Mit dem Befehl open wird ein Gerät initialisiert. Dieser Befehl wird von allen MCI-Geräten erkannt.
ms.assetid: 0bb97c8c-8222-4d4e-b20b-94e9f9095afe
keywords:
- Befehl "open" Windows Multimedia
topic_type:
- apiref
api_name:
- open
api_location:
- corecrt_io.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d2e585a44c19093fa0d20ab4870f579c67cd568c3a693523242b84910e6589d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118373269"
---
# <a name="open-command"></a>Befehl "open"

Mit dem Befehl open wird ein Gerät initialisiert. Dieser Befehl wird von allen MCI-Geräten erkannt.

Um diesen Befehl zu senden, rufen Sie die [**mciSendString-Funktion**](/previous-versions//dd757161(v=vs.85)) auf, wobei der *lpszCommand-Parameter* wie folgt festgelegt ist.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("open %s %s %s"), 
  lpszDevice, 
  lpszOpenFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lpszDevice"></span><span id="lpszdevice"></span><span id="LPSZDEVICE"></span>*lpszDevice*
</dt> <dd>

Bezeichner eines MCI-Geräts oder -Gerätetreibers. Dies kann entweder ein Gerätename (wie in der Registrierung oder in der SYSTEM.INI-Datei angegeben) oder der Dateiname des Gerätetreibers sein. Wenn Sie den Dateinamen des Gerätetreibers angeben, können Sie optional einschließen. DRV-Erweiterung, aber Sie sollten den Pfad zur Datei nicht einschließen.

</dd> <dt>

<span id="lpszOpenFlags"></span><span id="lpszopenflags"></span><span id="LPSZOPENFLAGS"></span>*lpszOpenFlags*
</dt> <dd>

Flag, das angibt, was initialisiert werden soll. In der folgenden Tabelle sind Gerätetypen aufgeführt, die den **geöffneten** Befehl und die von den einzelnen Typen verwendeten Flags erkennen.



| Wert        | Bedeutung                                                        | Bedeutung                                                                         |
|--------------|----------------------------------------------------------------|---------------------------------------------------------------------------------|
| cdaudio      | alias *device \_ alias* sharable                                  | *Typ des \_ Gerätetyps*                                                             |
| digitalvideo | alias *device \_ aliaselementname* nostatic parent *hwnd* sharable | stil child style overlapped style popup *style \_ style type* device type device *\_ type* |
| overlay      | alias *device \_ alias* parent *hwnd* sharable style child         | Stil überlappender Stil popup style *\_ type type* device type *(Stiltyp des Stiltyps \_ gerätetyp* überlappend)             |
| sequencer    | alias *device \_ alias* sharable                                 | *Typ des \_ Gerätetyps*                                                             |
| Vcr          | alias *device \_ alias* sharable                                  | *Typ des \_ Gerätetyps*                                                             |
| videodisk    | alias *device \_ alias* sharable                                  | *Typ des \_ Gerätetyps*                                                             |
| Waveaudio    | Puffergröße für *\_ Aliasgerätealiaspuffer* *\_*                     | *\_ Gerätetyp* "Sharable"                                                    |



 

Die folgende Tabelle enthält die Flags, die im **lpszOpenFlags-Parameter** angegeben werden können, und ihre Bedeutungen.



| Wert                 | Bedeutung                                                                                                                                                                                                                                                                                                                                                              |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *\_ Aliasgerätealias* | Gibt einen alternativen Namen für das angegebene Gerät an. Falls angegeben, muss sie in nachfolgenden Befehlen als *\_ Geräte-ID* verwendet werden.                                                                                                                                                                                                                                          |
| *Elementname*         | Gibt den Namen des Geräteelements (Datei) an, das beim Öffnen des Geräts geladen wird.                                                                                                                                                                                                                                                                                        |
| *\_ Pufferpuffergröße* | Legt die Größe des Puffers in Sekunden fest, der vom Waveform-Audio-Gerät verwendet wird. Die Standardgröße des Puffers wird festgelegt, wenn das Waveform-Audio-Gerät installiert oder konfiguriert wird. In der Regel ist die Puffergröße auf 4 Sekunden festgelegt. Beim MCIWAVE-Gerät beträgt die Mindestgröße 2 Sekunden und die maximale Größe 9 Sekunden.                                                |
| übergeordnetes *hwnd*         | Gibt das Fensterhandle des übergeordneten Fensters an.                                                                                                                                                                                                                                                                                                                    |
| Freigebbar              | Initialisiert das Gerät oder die Datei als trennbar. Nachfolgende Versuche, das Gerät oder die Datei zu öffnen, schlagen fehl, es sei denn, Sie geben "sharable" in den ursprünglichen und nachfolgenden **geöffneten** Befehlen an. MCI gibt einen ungültigen Gerätefehler zurück, wenn das Gerät bereits geöffnet und nicht zu trennen ist.<br/> Die MCISEQ-Sequencer- und MCIWAVE-Geräte unterstützen keine freigegebenen Dateien.<br/> |
| untergeordnetes Format           | Öffnet ein Fenster mit einem untergeordneten Fensterstil.                                                                                                                                                                                                                                                                                                                            |
| Format überlappend      | Öffnet ein Fenster mit einem überlappend formatierten Fenster.                                                                                                                                                                                                                                                                                                                      |
| Stil-Popup           | Öffnet ein Fenster mit einem Popupfensterstil.                                                                                                                                                                                                                                                                                                                           |
| *Stiltyp \_*   | Gibt einen Fensterstil an.                                                                                                                                                                                                                                                                                                                                            |
| *Typ des \_ Gerätetyps*   | Gibt den Gerätetyp einer Datei an.                                                                                                                                                                                                                                                                                                                                 |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Kann "wait", "notify" oder beides sein. Weitere Informationen zu diesen Flags finden Sie unter [Die Warte-, Benachrichtigungs- und Testflags.](the-wait-notify-and-test-flags.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn der Fehler erfolgreich war, oder andernfalls ein Fehler.

## <a name="remarks"></a>Hinweise

MCI reserviert "cdaudio" für den CD-Audiogerätetyp, "videodisc" für den Gerätetyp "videodisc", "sequencer" für den GERÄTEtyp "WAVE Sequencer", "AVIVideo" für den Gerätetyp "digital-video" und "waveaudio" für den Gerätetyp waveform-audio.

Als Alternative zum Flag "type" kann MCI das Gerät basierend auf der von der Datei verwendeten Erweiterung auswählen, wie in der Registrierung oder im \[ Abschnitt mci-Erweiterung \] der SYSTEM.INI-Datei aufgezeichnet.

MCI kann AVI-Dateien öffnen, indem ein Dateischnittstellenzeiger oder ein Streamschnittstellenzeiger verwendet wird. Um eine Datei mit einem der Schnittstellenzeigertypen zu öffnen, geben Sie ein at-Zeichen (@) gefolgt vom Schnittstellenzeiger anstelle der Datei oder des Gerätenamens für den *lpszDevice-Parameter* an. Weitere Informationen zu den Datei- und Streamschnittstellen finden Sie unter [AVIFile Functions and Macros](avifile-functions-and-macros.md).

Mit dem folgenden Befehl wird das Gerät "mysound" geöffnet.

``` syntax
open new type waveaudio alias mysound buffer 6
```

Mit dem Gerätenamen "new" bereitet der Waveform-Treiber eine neue Waveformressource vor. Der Befehl weist den Gerätealias "mysound" zu und gibt einen Puffer von 6 Sekunden an.

Sie können das Flag "type" entfernen, wenn Sie den Gerätenamen mit dem Dateinamen kombinieren. MCI erkennt diese Kombination, wenn Sie die folgende Syntax verwenden:

*\_ Gerätename* ! *\_Elementname*

Das Ausrufezeichen trennt den Gerätenamen vom Dateinamen. Das Ausrufezeichen darf nicht durch Leerzeichen getrennt werden.

Im folgenden Beispiel wird right geöffnet. WAV-Datei mit dem Gerät "waveaudio".

``` syntax
open waveaudio!right.wav
```

Der MCIWAVE-Treiber erfordert ein asynchrones Waveform-Audiogerät.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Corecrt \_ io.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Mci](mci.md)
</dt> <dt>

[MCI-Befehlszeichenfolgen](mci-command-strings.md)
</dt> </dl>

 

