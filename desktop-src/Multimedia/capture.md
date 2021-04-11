---
title: Aufzeichnungs Befehl
description: Mit dem Aufzeichnungs Befehl wird der Inhalt des Frame Puffers kopiert und in der angegebenen Datei gespeichert. Dieser Befehl wird von Digital-Video-Geräten erkannt.
ms.assetid: cdf177b9-874e-40d8-af3e-59070c55903d
keywords:
- Erfassungs Befehl Windows-Multimedia
topic_type:
- apiref
api_name:
- capture
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdf5edce248fc5402245e36e869cddc97ba3430a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105920"
---
# <a name="capture-command"></a>Aufzeichnungs Befehl

Mit dem Aufzeichnungs Befehl wird der Inhalt des Frame Puffers kopiert und in der angegebenen Datei gespeichert. Dieser Befehl wird von Digital-Video-Geräten erkannt.

Um diesen Befehl zu senden, wenden Sie die [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion mit dem festgelegten *lpszcommand* -Parameter wie folgt an.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("capture %s %s %s"), 
  lpszDeviceID, 
  lpszCapture, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszde viceid*
</dt> <dd>

Der Bezeichner eines MCI-Geräts. Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.

</dd> <dt>

<span id="lpszCapture"></span><span id="lpszcapture"></span><span id="LPSZCAPTURE"></span>*lpszcapture*
</dt> <dd>

Mindestens eines der folgenden Flags:



| Wert          | Bedeutung                                                                                                                                                                                                                                                   |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| als *Pfadname*  | Gibt den Zielpfad und den Dateinamen für das erfasste Abbild an. Dieses Flag ist erforderlich.                                                                                                                                                                |
| at- *Rechteck* | Gibt den rechteckigen Bereich innerhalb des Frame Puffers an, den das Gerät anlegt und auf dem Datenträger speichert. Wenn der Wert nicht angegeben wird, wird für den zugeschnittenen Bereich standardmäßig das Rechteck verwendet, das für den vorherigen Befehl "Quelle" für diese Geräte Instanz [festgelegt wurde](put.md) |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszflags*
</dt> <dd>

Kann "wait", "notify", "Test" oder eine Kombination daraus sein. Weitere Informationen zu diesen Flags finden Sie [unter warte-, Benachrichtigungs-und testflags](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.

## <a name="remarks"></a>Bemerkungen

Bei diesem Befehl tritt möglicherweise ein Fehler auf, wenn das Gerät gerade ein Bewegungsvideo wieder gibt oder ein anderer ressourcenintensiver Vorgang ausführt. Wenn der Frame Puffer in Echtzeit aktualisiert wird, wird die Aktualisierung vorübergehend angehalten, sodass ein Abbild erfasst wird. Wenn das Gerät die Aktualisierung anhält, kann es einen visuellen oder hörbaren Effekt geben. Wenn das Dateiformat, der Komprimierungs Algorithmus und die Qualitäts Ebenen nicht festgelegt wurden, werden die Standardwerte verwendet.

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

 

