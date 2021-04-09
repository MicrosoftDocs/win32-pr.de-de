---
title: List-Befehl
description: Der List-Befehl bestimmt die Anzahl und die Typen von Video-und Audioeingaben. Dieser Befehl wird von Digital-Video-und VCR-Geräten erkannt.
ms.assetid: b3fe3819-0b8a-4de5-9c79-03e1e089436f
keywords:
- Auflisten von Befehlen in Windows Multimedia
topic_type:
- apiref
api_name:
- list
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5d0a171c6768caf1b947a0d07cb46e5cccd28c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106214"
---
# <a name="list-command"></a>List-Befehl

Der List-Befehl bestimmt die Anzahl und die Typen von Video-und Audioeingaben. Dieser Befehl wird von Digital-Video-und VCR-Geräten erkannt.

Um diesen Befehl zu senden, wenden Sie die [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion mit dem festgelegten *lpszcommand* -Parameter wie folgt an.

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

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszde viceid*
</dt> <dd>

Der Bezeichner eines MCI-Geräts. Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.

</dd> <dt>

<span id="lpszList"></span><span id="lpszlist"></span><span id="LPSZLIST"></span>*lpszlist*
</dt> <dd>

Flag, mit dem die Anzahl und die Typen von Video-und Audioeingaben identifiziert werden. In der folgenden Tabelle werden die Gerätetypen aufgelistet, die den **Listen** Befehl und die von den einzelnen Typen verwendeten Flags erkennen.



| Wert        | Bedeutung                                                                           | Bedeutung                                                                                                                      |
|--------------|-----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| Digitalvideo | audioalgorithmusalgorithmusalgorithmus- *Algorithmus* audiostreamzählnummer *Index* | immer noch *Algorithmus Quality*-Algorithmus-Algorithmus, Video algorithmuvideo *Quality algorithmusalgorithmus Video* sourcevideo Stream |
| VCR          | Quellen Nummern *Index* für Audioquelle                                     | Videoquelle "Zielvideo Quell Nummern *Index* "                                                                                |



 

In der folgenden Tabelle werden die Flags aufgelistet, die im **lpszlist** -Parameter und deren Bedeutung angegeben werden können.



| Wert                               | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| audioalgorithmus                     | Gibt an, dass der Befehl audioalgorithmusnamen abrufen soll.                                                                                                                                                                                                                                                                                                                                                                                                                           |
| *Algorithmus für audioqualitäts Algorithmen* | Gibt an, dass der Befehl die dem angegebenen *Algorithmus* zugeordneten Qualitätsstufen abrufen soll. Wenn der *Algorithmus* "Current" ist, wird die Qualitätsstufe des aktuellen Algorithmus zurückgegeben.                                                                                                                                                                                                                                                                                                   |
| audioquellenanzahl                  | Gibt die Gesamtzahl der Audioeingaben zurück.                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| *Index* der audioquellnummer         | Gibt den Typ der Audioeingabe des Quell *Indexes* zurück.                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Audiodatenstrom                        | Gibt an, dass der Befehl die Namen der Audiostreams abrufen soll, die dem Arbeitsbereich zugeordnet sind. Diese Zeichen folgen (z. b. "Englisch" oder "Deutsch") werden in die Datei eingebettet und identifizieren den Stream.                                                                                                                                                                                                                                                                                    |
| count                               | Gibt die Anzahl der Optionen des angegebenen Typs zurück.                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Zahlen *Index*                      | Gibt eine Zeichenfolge zurück, die eine bestimmte Option (wie durch den *Index* identifiziert) des angegebenen Options Typs beschreibt. Der *Index* muss eine ganze Zahl zwischen 1 und dem Wert sein, der von "count" zurückgegeben wird.                                                                                                                                                                                                                                                                                                         |
| immer noch Algorithmus                     | Gibt an, dass der Befehl weiterhin Algorithmusnamen abrufen soll.                                                                                                                                                                                                                                                                                                                                                                                                                           |
| *Algorithmus* für Qualitäts Algorithmen | Gibt an, dass der Befehl Qualitätsstufen abrufen soll, die mit dem angegebenen noch *Algorithmus* verknüpft sind. Wenn der *Algorithmus* "Current" ist, wird die Qualitätsstufe des aktuellen Algorithmus zurückgegeben.                                                                                                                                                                                                                                                                                             |
| Video Algorithmus                     | Gibt an, dass der Befehl Video Algorithmusnamen abrufen soll.                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Algorithmus für Video *Qualitäts Algorithmen* | Gibt an, dass der Befehl die dem angegebenen Video *Algorithmus* zugeordneten Qualitätsstufen abrufen soll. Wenn der *Algorithmus* "Current" ist, wird die Qualitätsstufe des aktuellen Algorithmus zurückgegeben.                                                                                                                                                                                                                                                                                             |
| Videoquelle                        | Gibt an, dass der Befehl Informationen zu den Videoquellen zurückgeben soll. Bei Verwendung mit dem "count"-Flag wird die Anzahl der Videoquellen zurückgegeben. Bei Verwendung mit dem Flag "Number" wird der Typ einer Videoquelle zurückgegeben. MCI definiert die folgenden Konstanten für den Typ: "NTSC", "RGB", "PAL", "SECAM", "SVideo" und "Generic". Möglicherweise gibt es mehrere Quellen für jeden Typ, die zurückgegeben werden. Der "generische" Quelltyp wird verwendet, wenn mehr als ein Signal für diesen Connector zulässig ist. |
| Videoquellen Anzahl                  | Gibt die Gesamtanzahl der Videoeingaben zurück.                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| *Index* der Video Quellnummer         | Gibt den Typ der Videoeingabe des Quell *Indexes* zurück.                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Videostream                        | Gibt an, dass der Befehl die Namen der Videostreams abrufen soll, die dem Arbeitsbereich zugeordnet sind. Diese Zeichen folgen (z. b. "Funny End" oder "Sad End") werden in die Datei eingebettet und identifizieren den Stream.                                                                                                                                                                                                                                                                               |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszflags*
</dt> <dd>

Kann "wait", "notify" oder "Test" lauten. Weitere Informationen zu diesen Flags finden Sie [unter warte-, Benachrichtigungs-und testflags](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.

## <a name="remarks"></a>Bemerkungen

Für VCR-Geräte muss entweder "Videoquelle" oder "Audioquelle" mit den Flags "count" oder "Number" angegeben werden. Wenn "count" angegeben ist, wird die Gesamtzahl der Eingaben von Video oder Audiodatei zurückgegeben. Wenn "Number" angegeben wird, gibt der Treiber einen Typ zurück, der der Eingabe entspricht. Der Typ kann eines der folgenden sein: "Tuner", "Line", "SVideo", "AUX" oder "Generic". In der Regel sollten Sie zuerst den VCR nach "count" Abfragen und dann die Anzahl als Bereich für das Flag "Number" verwenden. Die "Quell Zahlen" beginnen mit "1".

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
</dt> </dl>

 

