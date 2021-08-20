---
title: Befehl „list“
description: Der Befehl list bestimmt die Anzahl und Typen von Video- und Audioeingaben. DigitalVideo- und VCR-Geräte erkennen diesen Befehl.
ms.assetid: b3fe3819-0b8a-4de5-9c79-03e1e089436f
keywords:
- Befehl "list" Windows Multimedia
topic_type:
- apiref
api_name:
- list
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8881c85d146ce869e41d234a72190901135d233f8e45d580d5f568c4ccc48da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118139473"
---
# <a name="list-command"></a>Befehl „list“

Der Befehl list bestimmt die Anzahl und Typen von Video- und Audioeingaben. DigitalVideo- und VCR-Geräte erkennen diesen Befehl.

Um diesen Befehl zu senden, rufen Sie die [**mciSendString-Funktion**](/previous-versions//dd757161(v=vs.85)) auf, wobei der *lpszCommand-Parameter* wie folgt festgelegt ist.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("list %s %s %s"), 
  lpszDeviceID, 
  lpszList, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Bezeichner eines MCI-Geräts. Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.

</dd> <dt>

<span id="lpszList"></span><span id="lpszlist"></span><span id="LPSZLIST"></span>*lpszList*
</dt> <dd>

Flag, das die Anzahl und Typen von Video- und Audioeingaben identifiziert. In der folgenden Tabelle sind die Gerätetypen aufgeführt, die den **List-Befehl** und die von den einzelnen Typen verwendeten Flags erkennen.



| Wert        | Bedeutung                                                                           | Bedeutung                                                                                                                      |
|--------------|-----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| digitalvideo | audio algorithmaudio quality algorithm *algorithm* audio streamcountnumber *index* | still algorithm algorithm algorithm *algorithm* video algorithmvideo quality *algorithm algorithm* video sourcevideo stream |
| Vcr          | AudioquellanzahlAudio-Quellnummernindex                                      | Anzahl der VideoquellenVideoquellzahlenindex                                                                                 |



 

Die folgende Tabelle enthält die Flags, die im **lpszList-Parameter** angegeben werden können, und ihre Bedeutungen.



| Wert                               | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Audioalgorithmus                     | Gibt an, dass der Befehl Audioalgorithmusnamen abrufen soll.                                                                                                                                                                                                                                                                                                                                                                                                                           |
| *Algorithmus für* die Audioqualität | Gibt an, dass der Befehl Qualitätsstufen abrufen soll, die dem angegebenen *Algorithmus* zugeordnet sind. Wenn *der Algorithmus* "current" ist, wird die Qualitätsstufe des aktuellen Algorithmus zurückgegeben.                                                                                                                                                                                                                                                                                                   |
| Anzahl der Audioquellen                  | Gibt die Gesamtzahl der Audioeingaben zurück.                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| *Index* der Audioquellnummer         | Gibt den Typ der Audioeingabe des *Quellindexes* zurück.                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Audiostream                        | Gibt an, dass der Befehl die Namen der Audiostreams abrufen soll, die dem Arbeitsbereich zugeordnet sind. Diese Zeichenfolgen (z. B. "Englisch" oder "Deutsch") werden in die Datei eingebettet und identifizieren den Datenstrom.                                                                                                                                                                                                                                                                                    |
| count                               | Gibt die Anzahl der Optionen des angegebenen Typs zurück.                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| *Zahlenindex*                      | Gibt eine Zeichenfolge zurück, die eine bestimmte Option (wie durch *den Index* identifiziert) des angegebenen Optionstyps beschreibt. *Der Index* muss eine ganze Zahl zwischen 1 und dem von "count" zurückgegebenen Wert sein.                                                                                                                                                                                                                                                                                                         |
| still-Algorithmus                     | Gibt an, dass der Befehl stille Algorithmusnamen abrufen soll.                                                                                                                                                                                                                                                                                                                                                                                                                           |
| *Algorithmusalgorithmus* für stille Qualität | Gibt an, dass der Befehl Qualitätsstufen abrufen soll, die dem angegebenen *still-Algorithmus* zugeordnet sind. Wenn *der Algorithmus* "current" ist, wird die Qualitätsstufe des aktuellen Algorithmus zurückgegeben.                                                                                                                                                                                                                                                                                             |
| Videoalgorithmus                     | Gibt an, dass der Befehl Videoalgorithmusnamen abrufen soll.                                                                                                                                                                                                                                                                                                                                                                                                                           |
| *Algorithmus für* die Videoqualität | Gibt an, dass der Befehl Qualitätsstufen abrufen soll, die dem angegebenen *Videoalgorithmus* zugeordnet sind. Wenn *der Algorithmus* "current" ist, wird die Qualitätsstufe des aktuellen Algorithmus zurückgegeben.                                                                                                                                                                                                                                                                                             |
| Videoquelle                        | Gibt an, dass der Befehl Informationen zu den Videoquellen zurückgeben soll. Bei Verwendung mit dem Flag "count" wird die Anzahl der Videoquellen zurückgegeben. Bei Verwendung mit dem Flag "number" wird der Typ einer Videoquelle zurückgegeben. MCI definiert die folgenden Konstanten für den Typ: "ntsc", "rgb", "pal", "secam", "svideo" und "generic". Es kann mehrere Quellen für jeden zurückgegebenen Typ geben. Der "generische" Quelltyp wird verwendet, wenn mehr als ein Signal für diesen Connector zulässig ist. |
| Anzahl der Videoquellen                  | Gibt die Gesamtzahl der Videoeingaben zurück.                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| *Index* der Videoquellnummer         | Gibt den Typ der Videoeingabe des *Quellindexes* zurück.                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Videostream                        | Gibt an, dass der Befehl die Namen der Videostreams abrufen soll, die dem Arbeitsbereich zugeordnet sind. Diese Zeichenfolgen (z. B. "Endendung" oder "leideres Ende") werden in die Datei eingebettet und identifizieren den Datenstrom.                                                                                                                                                                                                                                                                               |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Kann "wait", "notify" oder "test" sein. Weitere Informationen zu diesen Flags finden Sie unter [Die Warte-, Benachrichtigungs- und Testflags.](the-wait-notify-and-test-flags.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn der Fehler erfolgreich war, oder andernfalls ein Fehler.

## <a name="remarks"></a>Hinweise

Bei VCR-Geräten muss entweder "Videoquelle" oder "Audioquelle" mit den Flags "count" oder "number" angegeben werden. Wenn "count" angegeben ist, wird die Gesamtzahl der Eingaben von Video oder Audio zurückgegeben. Wenn "number" angegeben ist, gibt der Treiber einen Typ zurück, der der Eingabe entspricht. Der Typ kann eine der folgenden Typen sein: "tuner", "line", "svideo", "aux" oder "generic". In der Regel sollten Sie zuerst den VCR nach "count" abfragen und dann die Anzahl als Bereich für das Flag "number" verwenden. Die Quellnummern beginnen bei 1.

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
</dt> </dl>

 

