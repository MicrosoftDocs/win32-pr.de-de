---
title: Befehl "info"
description: Der Befehl info ruft eine Hardwarebeschreibung von einem Gerät ab. Dieser Befehl wird von allen MCI-Geräten erkannt.
ms.assetid: cdd6628b-bff8-4a0d-9dad-a63321f584ea
keywords:
- Infobefehl Windows Multimedia
topic_type:
- apiref
api_name:
- info
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f15675923f37a80ce694a400f18113f5178a54a3f75664008644919c6d9fc128
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119690470"
---
# <a name="info-command"></a>Befehl "info"

Der Befehl info ruft eine Hardwarebeschreibung von einem Gerät ab. Dieser Befehl wird von allen MCI-Geräten erkannt.

Um diesen Befehl zu senden, rufen Sie die [**mciSendString-Funktion**](/previous-versions//dd757161(v=vs.85)) mit dem *lpszCommand-Parameter* auf, der wie folgt festgelegt ist.

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

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Bezeichner eines MCI-Geräts. Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.

</dd> <dt>

<span id="lpszInfoType"></span><span id="lpszinfotype"></span><span id="LPSZINFOTYPE"></span>*lpszInfoType*
</dt> <dd>

Flag, das den Typ der erforderlichen Informationen identifiziert. In der folgenden Tabelle sind Gerätetypen aufgeführt, die den **Befehl info** und die von den einzelnen Typen verwendeten Flags erkennen.



| Wert        | Bedeutung                                                             | Bedeutung                                             |
|--------------|---------------------------------------------------------------------|-----------------------------------------------------|
| cdaudio      | info identityinfo upc                                               | product                                             |
| digitalvideo | audio algorithmaudio qualityfileproduct algorithm quality | usageversionvideo algorithmvideo qualitywindow text |
| overlay      | fileproduct                                                         | Fenstertext                                         |
| sequencer    | copyrightfile                                                       | nameproduct                                         |
| Vcr          | product                                                             | version                                             |
| videodisk    | product                                                             |                                                     |
| Waveaudio    | fileinput                                                           | outputproduct                                       |



 

In der folgenden Tabelle sind die Flags, die im **lpszInfoType-Parameter** angegeben werden können, und ihre Bedeutungen aufgeführt.



| Wert           | Bedeutung                                                                                                                                                                                            |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Audioalgorithmus | Gibt den Namen des aktuellen Audiokomprimierungsalgorithmus zurück.                                                                                                                                       |
| Audioqualität   | Gibt den Namen für den aktuellen Audioqualitätsdeskriptor zurück. Dies kann "unbekannt" zurückgeben, wenn die Anwendung Parameter auf bestimmte Werte festgelegt hat, die nicht den definierten Qualitäten entsprechen.       |
| Copyright       | Ruft den COPYRIGHT-Hinweis für die TEXTDATEI-Datei aus dem Copyrightmetaereignis ab.                                                                                                                            |
| file            | Ruft den Namen der Datei ab, die vom Verbundgerät verwendet wird. Wenn das Gerät ohne Datei geöffnet wird und der [Ladebefehl](load.md) nicht verwendet wurde, wird eine NULL-Zeichenfolge zurückgegeben.                  |
| Infoidentität   | Erzeugt einen eindeutigen Bezeichner für die Audio-CD, die derzeit in den abgefragten Player geladen wird.                                                                                                        |
| info upc        | Erzeugt den Universal Product Code (UPC), der auf einer Audio-CD codiert ist. Der UPC ist eine Zeichenfolge von Ziffern. Es ist möglicherweise nicht für alle CDs verfügbar.                                                    |
| input           | Ruft die Beschreibung des aktuellen Eingabegeräts ab. Gibt "none" zurück, wenn kein Eingabegerät festgelegt ist.                                                                                               |
| name            | Ruft den Sequenznamen aus dem Sequenz-/Nachverfolgungsnamen-Metaereignis ab.                                                                                                                               |
| output          | Ruft die Beschreibung des aktuellen Ausgabegeräts ab. Gibt "none" zurück, wenn kein Ausgabegerät festgelegt ist.                                                                                             |
| product         | Ruft eine Beschreibung des Geräts ab. Diese Informationen umfassen häufig den Produktnamen und das Modell. Die Zeichenfolgenlänge beträgt 31 Zeichen oder weniger.                                               |
| still-Algorithmus | Gibt den Namen des aktuellen Bildkomprimierungsalgorithmus zurück.                                                                                                                                 |
| noch qualität   | Gibt den Namen für den aktuellen Imagequalitätsdeskriptor zurück. Dies kann "unbekannt" zurückgeben, wenn die Anwendung Parameter auf bestimmte Werte festgelegt hat, die nicht den definierten Qualitäten entsprechen. |
| Nutzung           | Gibt eine Zeichenfolge zurück, die Nutzungseinschränkungen beschreibt, die möglicherweise vom Besitzer der Visuellen oder Audiodaten im Arbeitsbereich gelten.                                                                    |
| version         | Gibt die Releaseebene des Gerätetreibers und der Hardware zurück.                                                                                                                                       |
| Videoalgorithmus | Gibt den Namen des aktuellen Videokomprimierungsalgorithmus zurück.                                                                                                                                       |
| Videoqualität   | Gibt den Namen für den aktuellen Videoqualitätsdeskriptor zurück. Dies kann "unbekannt" zurückgeben, wenn die Anwendung Parameter auf bestimmte Werte festgelegt hat, die nicht den definierten Qualitäten entsprechen.       |
| Fenstertext     | Ruft die Beschriftung des Fensters ab, das vom Gerät verwendet wird.                                                                                                                                            |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Kann "wait", "notify" oder beides sein. Für digital-video- und VCR-Geräte kann auch "test" angegeben werden. Weitere Informationen zu diesen Flags finden Sie unter [Die Warte-, Benachrichtigungs- und Testflags](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls ein Fehler.

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

[Mci](mci.md)
</dt> <dt>

[MCI-Befehlszeichenfolgen](mci-command-strings.md)
</dt> <dt>

[Laden](load.md)
</dt> </dl>

 

