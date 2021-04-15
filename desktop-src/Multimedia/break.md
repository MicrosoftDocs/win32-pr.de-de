---
title: Break-Befehl
description: Mit dem Break-Befehl wird ein Schlüssel angegeben, mit dem ein Befehl abgebrochen wird, der mithilfe von \ 0034; Wait \ 0034; aufgerufen wurde. ssen. Dieser Befehl ist ein MCI-Systembefehl. Sie wird direkt von MCI interpretiert.
ms.assetid: 959df85f-5020-4e37-952b-15ba5e6fb672
keywords:
- Umbruch Befehl Windows-Multimedia
topic_type:
- apiref
api_name:
- break
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f727fb6cf375e09a260ee68f62eac83816ff5d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478933"
---
# <a name="break-command"></a>Break-Befehl

Mit dem Break-Befehl wird ein Schlüssel angegeben, mit dem ein Befehl abgebrochen wird, der mit dem Flag "wait" aufgerufen wurde. Dieser Befehl ist ein MCI-Systembefehl. Sie wird direkt von MCI interpretiert.

Um diesen Befehl zu senden, wenden Sie die [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion mit dem festgelegten *lpszcommand* -Parameter wie folgt an.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("break %s %s %s"), 
  lpszDeviceID, 
  lpszVirtKey, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszde viceid*
</dt> <dd>

Der Bezeichner eines MCI-Geräts. Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.

</dd> <dt>

<span id="lpszVirtKey"></span><span id="lpszvirtkey"></span><span id="LPSZVIRTKEY"></span>*lpszvirtkey*
</dt> <dd>

Eines der folgenden Flags.



| Wert                 | Bedeutung                                                                         |
|-----------------------|---------------------------------------------------------------------------------|
| auf *virtuellem Schlüsselcode* | Gibt den Schlüssel an, der einen Befehl abbricht, der mit dem Flag "wait" gestartet wurde. |
| aus                   | Deaktiviert die aktuelle Break-Taste.                                                 |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszflags*
</dt> <dd>

Kann "wait", "notify" oder beides sein. Für Digital Video-und VCR-Geräte kann auch "Test" angegeben werden. Weitere Informationen zu diesen Flags finden Sie [unter warte-, Benachrichtigungs-und testflags](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.

## <a name="remarks"></a>Bemerkungen

Wenn die Break-Taste aktiviert ist und der Benutzer den Schlüssel drückt, der durch den im *lpszvirtkey* -Parameter angegebenen Code des virtuellen Schlüssels gekennzeichnet ist, gibt das Gerät die Steuerung an die Anwendung zurück. Wenn möglich, wird die Ausführung des Befehls fortgesetzt.

## <a name="examples"></a>Beispiele

Der folgende Befehl legt F2 als Break Key für das "mysound"-Gerät fest.

``` syntax
break mysound on 113
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
</dt> </dl>

 

