---
title: Befehl "Where"
description: Der WHERE-Befehl ruft das Rechteck ab, das den Quell-oder Zielbereich angibt. Dieses Rechteck wurde mit dem Put-Befehl angegeben. Dieser Befehl wird von Digital Video-und Video Überlagerungs Geräten erkannt.
ms.assetid: 85c68ded-bd3e-4a48-9af7-58478615a7f0
keywords:
- Where-Befehl Windows Multimedia
topic_type:
- apiref
api_name:
- where
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22c499eae8f0209c1ef93efb9677ae438dcf0e86
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957026"
---
# <a name="where-command"></a>Befehl "Where"

Der WHERE-Befehl ruft das Rechteck ab, das den Quell-oder Zielbereich angibt. Dieses Rechteck wurde mit dem [Put](put.md) -Befehl angegeben. Dieser Befehl wird von Digital Video-und Video Überlagerungs Geräten erkannt.

Um diesen Befehl zu senden, wenden Sie die [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion mit dem festgelegten *lpszcommand* -Parameter wie folgt an.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("where %s %s %s"), 
  lpszDeviceID, 
  lpszRequestRect, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszde viceid*
</dt> <dd>

Der Bezeichner eines MCI-Geräts. Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.

</dd> <dt>

<span id="lpszRequestRect"></span><span id="lpszrequestrect"></span><span id="LPSZREQUESTRECT"></span>*lpszrequestrect*
</dt> <dd>

Flag, das das Rechteck identifiziert, dessen Dimensionen abgerufen werden. In der folgenden Tabelle werden die Gerätetypen aufgelistet, die den **Where** -Befehl und die von den einzelnen Typen verwendeten Flags erkennen.



| Wert        | Bedeutung                                                       | Bedeutung                                  |
|--------------|---------------------------------------------------------------|------------------------------------------|
| Digitalvideo | destinationdestination [**Max**](max.md)frameframe maxsource | Quelle maxvideovideo maxwindowwindow Max |
| overlay      | destinationframe                                              | sourcevideo                              |



 

In der folgenden Tabelle werden die Flags aufgelistet, die im **lpszrequestrect** -Parameter und deren Bedeutung angegeben werden können.



| Wert                          | Bedeutung                                                                                                                                                                                                                                                                                              |
|--------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| destination                    | Ruft den Ziel Offset und-Block ab. Bei Video Überlagerungs Geräten definiert das Ziel Rechteck den Bereich des Client Bereichs Anzeige Fenster, in dem die Bilddaten aus dem Frame Puffer angezeigt werden.                                                                                             |
| [ **Max** . Ziel](max.md) | Ruft die aktuelle Größe des Client Rechtecks ab.                                                                                                                                                                                                                                                  |
| frame                          | Ruft den Offset und den Umfang des Frame Puffer Rechtecks ab. Das Rahmen Puffer Rechteck definiert den Bereich des Frame Puffers, der eingehende Videodaten empfängt. Bilder aus dem Rechteck "Video" werden in diesen Bereich skaliert.                                                                     |
| [ **Max** . Frame](max.md)       | Gibt die maximale Größe des Frame Puffers zurück.                                                                                                                                                                                                                                                        |
| source                         | Ruft den Quell Offset und den Wertebereich ab. Bei Video Überlagerungs Geräten definiert das Quell Rechteck den Bereich des Frame Puffers, der im Zielfenster angezeigt wird. Das Gerät verwendet dieses Rechteck zum Zuschneiden des Bilds, bevor es gestreckt wird, um das Ziel Rechteck auf der Anzeige anzupassen. |
| [ **Maximale** Quelldatei](max.md)      | Ruft die maximale Größe des Frame Puffers ab.                                                                                                                                                                                                                                                      |
| video                          | Ruft den Offset und den Umfang des Video Rechtecks ab. Das Video Rechteck definiert den Bereich der eingehenden Videodaten, die an den Frame Puffer übertragen werden.                                                                                                                                   |
| [ **Maximales** Video](max.md)       | Gibt die maximale Größe der Eingabe zurück.                                                                                                                                                                                                                                                               |
| Fenster                         | Ruft die aktuelle Größe und Position des Anzeige Fensterrahmens ab.                                                                                                                                                                                                                                 |
| [ **Max** . Fenster](max.md)      | Ruft die Größe der gesamten Anzeige ab.                                                                                                                                                                                                                                                            |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszflags*
</dt> <dd>

Kann "wait", "notify" oder beides sein. Für Digital Video-Geräte kann auch "Test" angegeben werden. Weitere Informationen zu diesen Flags finden Sie [unter warte-, Benachrichtigungs-und testflags](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt ein Rechteck im *lpszreturnstring* -Parameter der [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion zurück. Das Rechteck beschreibt den Bereich, der im *lpszrequestrect* -Parameter dieses Befehls angegeben ist. Das Rechteck wird als *x1 y1 x2 Y2* angegeben. Die Koordinaten *x1 y1* geben die linke obere Ecke des Rechtecks an, und die Koordinaten *x2 Y2* geben die Breite und Höhe an.

## <a name="examples"></a>Beispiele

Der folgende Befehl gibt das Anzeige Rechteck des "Movie"-Geräts zurück.

``` syntax
where movie destination
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

[stellte](put.md)
</dt> </dl>

 

