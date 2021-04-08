---
title: Open-Befehl (corecrt \_ IO. h)
description: Der Open-Befehl initialisiert ein Gerät. Dieser Befehl wird von allen MCI-Geräten erkannt.
ms.assetid: 0bb97c8c-8222-4d4e-b20b-94e9f9095afe
keywords:
- Open-Befehl Windows Multimedia
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
ms.openlocfilehash: ac8d31f1806a9c12f764c679548564aa053c3041
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741432"
---
# <a name="open-command"></a>Befehl Öffnen

Der Open-Befehl initialisiert ein Gerät. Dieser Befehl wird von allen MCI-Geräten erkannt.

Um diesen Befehl zu senden, wenden Sie die [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion mit dem festgelegten *lpszcommand* -Parameter wie folgt an.

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

<span id="lpszDevice"></span><span id="lpszdevice"></span><span id="LPSZDEVICE"></span>*lpszdevice*
</dt> <dd>

Der Bezeichner eines MCI-Geräts oder Gerätetreibers. Dabei kann es sich entweder um einen Gerätenamen (wie in der Registrierung oder in der SYSTEM.INI-Datei angegeben) oder um den Dateinamen des Gerätetreibers handeln. Wenn Sie den Dateinamen des Gerätetreibers angeben, können Sie optional den einschließen. DRV-Erweiterung, Sie sollten jedoch nicht den Pfad zur Datei einschließen.

</dd> <dt>

<span id="lpszOpenFlags"></span><span id="lpszopenflags"></span><span id="LPSZOPENFLAGS"></span>*lpszopenflags*
</dt> <dd>

Flag, das angibt, was initialisiert werden soll. In der folgenden Tabelle werden die Gerätetypen aufgelistet, die den **geöffneten** Befehl und die von den einzelnen Typen verwendeten Flags erkennen.



| Wert        | Bedeutung                                                        | Bedeutung                                                                         |
|--------------|----------------------------------------------------------------|---------------------------------------------------------------------------------|
| CDAudio      | Alias *- \_ geräteralias* freigegeben                                  | Typ des *Geräte \_ Typs*                                                             |
| Digitalvideo | Alias *Gerät \_ aliaselementname* nostatic übergeordnetes *HWND* freigegeben | Stil für Stil des untergeordneten Stils im Stil *von \_ Popup Stil Typen Typ* *\_ Gerätetyp* |
| overlay      | Alias *- \_ Gerätealias* übergeordnetes *HWND*-Element mit shardstil         | Stil des Stil Überlapp enden Stils *Stil \_ Typs* Typ *\_ Gerätetyp*             |
| sequencer    | Alias *- \_ geräteralias* freigegeben                                 | Typ des *Geräte \_ Typs*                                                             |
| VCR          | Alias *- \_ geräteralias* freigegeben                                  | Typ des *Geräte \_ Typs*                                                             |
| Videodisk    | Alias *- \_ geräteralias* freigegeben                                  | Typ des *Geräte \_ Typs*                                                             |
| waveaudiodatei    | Alias Puffer *\_ Größe* des Alias *Geräts \_*                     | *\_ Gerätetyp* "freigegeben Type"                                                    |



 

In der folgenden Tabelle werden die Flags aufgelistet, die im **lpszopenflags** -Parameter und deren Bedeutung angegeben werden können.



| Wert                 | Bedeutung                                                                                                                                                                                                                                                                                                                                                              |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Alias *- \_ Gerätealias* | Gibt einen alternativen Namen für das angegebene Gerät an. Wenn dieser Wert angegeben ist, muss er in nachfolgenden Befehlen als *Geräte- \_ ID* verwendet werden.                                                                                                                                                                                                                                          |
| *Elementname*         | Gibt den Namen des Geräte Elements (Datei) an, das beim Öffnen des Geräts geladen wird.                                                                                                                                                                                                                                                                                        |
| Puffer *Puffer \_ Größe* | Legt die Größe des Puffers, der vom Waveform-Audiogerät verwendet wird, in Sekunden fest. Die Standardgröße des Puffers wird festgelegt, wenn das Waveform-Audiogerät installiert oder konfiguriert wird. In der Regel ist die Puffergröße auf 4 Sekunden festgelegt. Mit dem MCIWave-Gerät beträgt die Mindestgröße 2 Sekunden, und die maximale Größe beträgt 9 Sekunden.                                                |
| übergeordnetes *HWND*         | Gibt das Fenster Handle des übergeordneten Fensters an.                                                                                                                                                                                                                                                                                                                    |
| freigegeben              | Initialisiert das Gerät oder die Datei als Sharable. Bei nachfolgenden versuchen, das Gerät oder die Datei zu öffnen, tritt ein Fehler auf, es sei denn, Sie geben "sharable" in den ursprünglichen **und nachfolgenden** MCI gibt einen ungültigen Gerätefehler zurück, wenn das Gerät bereits geöffnet ist und nicht freigegeben werden kann.<br/> Die mciseq Sequencer-und MCIWave-Geräte unterstützen keine freigegebenen Dateien.<br/> |
| untergeordnetes Stil           | Öffnet ein Fenster mit einem untergeordneten Fenster Stil.                                                                                                                                                                                                                                                                                                                            |
| überschlender Stil      | Öffnet ein Fenster mit einem überlappenden Fenster Stil.                                                                                                                                                                                                                                                                                                                      |
| Stil-Popup           | Öffnet ein Fenster mit einem Popup Fenster Stil.                                                                                                                                                                                                                                                                                                                           |
| Stil *\_ Stiltyp*   | Gibt einen Fenster Stil an.                                                                                                                                                                                                                                                                                                                                            |
| Typ des *Geräte \_ Typs*   | Gibt den Gerätetyp einer Datei an.                                                                                                                                                                                                                                                                                                                                 |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszflags*
</dt> <dd>

Kann "wait", "notify" oder beides sein. Weitere Informationen zu diesen Flags finden Sie [unter warte-, Benachrichtigungs-und testflags](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.

## <a name="remarks"></a>Bemerkungen

MCI reserviert "CDAudio" für den CD-audiogerätetyp "Videodisk" für den Videodisk-Gerätetyp "Sequencer" für den Typ des MIDI Sequencer-Geräts, "AVIVideo" für den Gerätetyp Digital-Video und "waveaudiodatei" für den Typ "Waveform-Audiogerät".

Als Alternative zum Flag "Type" kann MCI das Gerät basierend auf der von der Datei verwendeten Erweiterung auswählen, wie in der Registrierung oder im \[ MCI-Erweiterungs \] Abschnitt der SYSTEM.INI Datei aufgezeichnet.

MCI kann AVI-Dateien mithilfe eines Datei Schnittstellen Zeigers oder eines Stream-Schnittstellen Zeigers öffnen. Wenn Sie eine Datei mit einer der beiden Schnittstellen Zeiger Typen öffnen möchten, geben Sie ein @-Zeichen gefolgt vom Schnittstellen Zeiger anstelle des Datei-oder Geräte namens für den *lpszdevice* -Parameter an. Weitere Informationen über die Datei-und streamschnittstellen finden Sie unter " [avifile-Funktionen und-Makros](avifile-functions-and-macros.md)".

Mit dem folgenden Befehl wird das Gerät "mysound" geöffnet.

``` syntax
open new type waveaudio alias mysound buffer 6
```

Mit dem Gerätenamen "New" bereitet der Wellenform-Treiber eine neue Wellenform-Ressource vor. Der Befehl weist den Gerätealias "mysound" zu und gibt einen 6-Sekunden-Puffer an.

Sie können das Flag "Type" entfernen, wenn Sie den Gerätenamen mit dem Dateinamen kombinieren. MCI erkennt diese Kombination, wenn Sie die folgende Syntax verwenden:

*Geräte \_ Name* ! *Element \_ Name*

Das Ausrufezeichen trennt den Gerätenamen vom Dateinamen. Das Ausrufezeichen sollte nicht durch Leerzeichen getrennt werden.

Im folgenden Beispiel wird das Recht geöffnet. WAV-Datei, die das Gerät "WaveAudio" verwendet.

``` syntax
open waveaudio!right.wav
```

Der MCIWave-Treiber erfordert ein asynchrones Waveform-Audiogerät.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Corecrt \_ IO. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[MCI-Befehls Zeichenfolgen](mci-command-strings.md)
</dt> </dl>

 

