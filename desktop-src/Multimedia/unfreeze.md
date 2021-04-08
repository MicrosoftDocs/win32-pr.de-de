---
title: Befehl zum Einfrieren aufheben
description: Mit dem Befehl zum Aufheben der Fixierung wird die Video Erfassung im Frame Puffer wieder aktiviert, nachdem Sie durch den Freeze-Befehl deaktiviert wurde. Dieser Befehl wird von digitalen Video-, VCR-und Video Überlagerungs Geräten erkannt.
ms.assetid: ca90c299-2003-44cb-a879-4bc767480965
keywords:
- Befehl zum Aufheben der Fixierung von Windows Multimedia
topic_type:
- apiref
api_name:
- unfreeze
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 155ba6b65fb08411d8404920c8f3337d1bddbcb1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743560"
---
# <a name="unfreeze-command"></a>Befehl zum Einfrieren aufheben

Mit dem Befehl zum Aufheben der Fixierung wird die Video Erfassung im Frame Puffer wieder aktiviert, nachdem Sie durch den [Freeze](freeze.md) -Befehl deaktiviert wurde. Dieser Befehl wird von digitalen Video-, VCR-und Video Überlagerungs Geräten erkannt.

Um diesen Befehl zu senden, wenden Sie die [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion mit dem festgelegten *lpszcommand* -Parameter wie folgt an.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("unfreeze %s %s %s"), 
  lpszDeviceID, 
  lpszUnfreeze, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszde viceid*
</dt> <dd>

Der Bezeichner eines MCI-Geräts. Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.

</dd> <dt>

<span id="lpszUnfreeze"></span><span id="lpszunfreeze"></span><span id="LPSZUNFREEZE"></span>*lpszunfreeze*
</dt> <dd>

Flag zum erneuten Aktivieren der Video Erfassung für den Frame Puffer. In der folgenden Tabelle sind die Gerätetypen aufgeführt **, die den Befehl zum** Aufheben der Fixierung und die von den einzelnen Typen verwendeten Flags erkennen.



| Wert        | Bedeutung        |
|--------------|----------------|
| Digitalvideo | at- *Rechteck* |
| overlay      | at- *Rechteck* |
| VCR          | Eingabe Ausgabe   |



 

In der folgenden Tabelle werden die Flags aufgelistet, die im **lpszunfreeze** -Parameter und deren Bedeutung angegeben werden können.



| Wert          | Bedeutung                                                                                                                                                                                                                                                                                    |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| at- *Rechteck* | Gibt die Region an, in der die Video Beschaffung erneut aktiviert wird. Das Rechteck ist relativ zum Video Puffer Ursprung und wird als *x1 y1 x2 Y2* angegeben. Die Koordinaten *x1 y1* geben die linke obere Ecke des Rechtecks an, und die Koordinaten *x2 Y2* geben die Breite und Höhe an. |
| input          | Heben Sie die Fixierung des Eingabe Bilds auf.                                                                                                                                                                                                                                                                  |
| output         | Entsperrung des Ausgabe Bilds. Wenn weder "Input" noch "Output" angegeben wird, wird "Output" angenommen.                                                                                                                                                                                                  |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszflags*
</dt> <dd>

Kann "wait", "notify" oder beides sein. Für Digital Video-und VCR-Geräte kann auch "Test" angegeben werden. Weitere Informationen zu diesen Flags finden Sie [unter warte-, Benachrichtigungs-und testflags](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.

## <a name="examples"></a>Beispiele

Der folgende Befehl entfriert einen Bereich des Video Puffers.

``` syntax
unfreeze vboard at 10 20 90 165
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

[ge](freeze.md)
</dt> </dl>

 

