---
title: Info-Befehl
description: Der Befehl "Info" Ruft eine Hardware Beschreibung von einem Gerät ab. Dieser Befehl wird von allen MCI-Geräten erkannt.
ms.assetid: cdd6628b-bff8-4a0d-9dad-a63321f584ea
keywords:
- Info-Befehl Windows-Multimedia
topic_type:
- apiref
api_name:
- info
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6d401efca6a59d1ed3cbf433d7c33311678705d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392153"
---
# <a name="info-command"></a>Info-Befehl

Der Befehl "Info" Ruft eine Hardware Beschreibung von einem Gerät ab. Dieser Befehl wird von allen MCI-Geräten erkannt.

Um diesen Befehl zu senden, wenden Sie die [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion mit dem festgelegten *lpszcommand* -Parameter wie folgt an.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("info %s %s %s"), 
  lpszDeviceID, 
  lpszInfoType, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszde viceid*
</dt> <dd>

Der Bezeichner eines MCI-Geräts. Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.

</dd> <dt>

<span id="lpszInfoType"></span><span id="lpszinfotype"></span><span id="LPSZINFOTYPE"></span>*lpszinfotype*
</dt> <dd>

Flag, das den Typ der erforderlichen Informationen identifiziert. In der folgenden Tabelle werden die Gerätetypen aufgelistet, die den **Info** -Befehl und die von den einzelnen Typen verwendeten Flags erkennen.



| Wert        | Bedeutung                                                             | Bedeutung                                             |
|--------------|---------------------------------------------------------------------|-----------------------------------------------------|
| CDAudio      | Informationen identityinfo UPC                                               | product                                             |
| Digitalvideo | audioalgorithmaudioqualityfileproductimmer noch algorithmimmer Qualität | usageversionvideo algorithmvideo qualitywindow-Text |
| overlay      | file Product                                                         | Fenster Text                                         |
| sequencer    | copyrightfile                                                       | nameproduct                                         |
| VCR          | product                                                             | version                                             |
| Videodisk    | product                                                             |                                                     |
| waveaudiodatei    | FileInput                                                           | outputproduct                                       |



 

In der folgenden Tabelle werden die Flags aufgelistet, die im **lpszinfotype** -Parameter und deren Bedeutung angegeben werden können.



| Wert           | Bedeutung                                                                                                                                                                                            |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| audioalgorithmus | Gibt den Namen des aktuellen Audiokomprimierungs Algorithmus zurück.                                                                                                                                       |
| Audioqualität   | Gibt den Namen für den aktuellen audioqualitätsdeskriptor zurück. Dadurch wird möglicherweise "unknown" zurückgegeben, wenn die Anwendung Parameter auf bestimmte Werte festgelegt hat, die nicht definierten Qualitäten entsprechen.       |
| Copyright       | Ruft den Urheberrechts Hinweis der MIDI-Datei aus dem Copyright-Meta-Ereignis ab.                                                                                                                            |
| file            | Ruft den Namen der Datei ab, die vom Verbund Gerät verwendet wird. Wenn das Gerät ohne eine Datei geöffnet wird und der [Load](load.md) -Befehl nicht verwendet wurde, wird eine NULL-Zeichenfolge zurückgegeben.                  |
| Informations Identität   | Erzeugt einen eindeutigen Bezeichner für die AudioCD, die derzeit in dem abgefragten Player geladen wird.                                                                                                        |
| Info-UPC        | Erzeugt den universellen Produkt Code (Universal Product Code, UPC), der auf einer AudioCD codiert ist. Der UPC ist eine Zeichenfolge mit Ziffern. Sie ist möglicherweise nicht für alle CDs verfügbar.                                                    |
| input           | Ruft die Beschreibung des aktuellen Eingabe Geräts ab. Gibt "None" zurück, wenn ein Eingabegerät nicht festgelegt ist.                                                                                               |
| name            | Ruft den Sequenznamen aus dem Meta-Ereignis Sequence/Track Name ab.                                                                                                                               |
| output          | Ruft die Beschreibung des aktuellen Ausgabegeräts ab. Gibt "None" zurück, wenn kein Ausgabegerät festgelegt ist.                                                                                             |
| product         | Ruft eine Beschreibung des Geräts ab. Diese Informationen enthalten häufig den Produktnamen und das Modell. Die Länge der Zeichenfolge beträgt höchstens 31 Zeichen.                                               |
| immer noch Algorithmus | Gibt den Namen des aktuellen immer noch Bild Komprimierungs Algorithmus zurück.                                                                                                                                 |
| immer noch Qualität   | Gibt den Namen für den aktuellen immer noch Bild Qualitäts Deskriptor zurück. Dadurch wird möglicherweise "unknown" zurückgegeben, wenn die Anwendung Parameter auf bestimmte Werte festgelegt hat, die nicht definierten Qualitäten entsprechen. |
| Nutzung           | Gibt eine Zeichenfolge zurück, in der Nutzungseinschränkungen beschrieben werden, die möglicherweise vom Besitzer der visuellen oder Audiodaten im Arbeitsbereich auferlegt werden.                                                                    |
| version         | Gibt die releaseebene des Gerätetreibers und der Hardware zurück.                                                                                                                                       |
| Video Algorithmus | Gibt den Namen des aktuellen Video Komprimierungs Algorithmus zurück.                                                                                                                                       |
| Videoqualität   | Gibt den Namen für den aktuellen Video Qualitäts Deskriptor zurück. Dadurch wird möglicherweise "unknown" zurückgegeben, wenn die Anwendung Parameter auf bestimmte Werte festgelegt hat, die nicht definierten Qualitäten entsprechen.       |
| Fenster Text     | Ruft die Beschriftung des Fensters ab, das vom Gerät verwendet wird.                                                                                                                                            |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszflags*
</dt> <dd>

Kann "wait", "notify" oder beides sein. Für Digital Video-und VCR-Geräte kann auch "Test" angegeben werden. Weitere Informationen zu diesen Flags finden Sie [unter warte-, Benachrichtigungs-und testflags](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.

## <a name="examples"></a>Beispiele

Der folgende Befehl ruft eine Beschreibung der Hardware ab, die dem Gerät "mysound" zugeordnet ist.

``` syntax
info mysound product
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

[Laden](load.md)
</dt> </dl>

 

