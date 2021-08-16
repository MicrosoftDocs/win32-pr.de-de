---
title: Befehl "break"
description: Der Break-Befehl gibt einen Schlüssel zum Abbrechen eines Befehls an, der mit \0034;wait \ 0034 aufgerufen wurde. Flag. Dieser Befehl ist ein MCI-Systembefehl. sie wird direkt von MCI interpretiert.
ms.assetid: 959df85f-5020-4e37-952b-15ba5e6fb672
keywords:
- Befehl "break" Windows Multimedia
topic_type:
- apiref
api_name:
- break
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f99c8609b1364d374d91965816fde2d9c48b750d7bf0b3f6fb2957ed205a85a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118375472"
---
# <a name="break-command"></a>Befehl "break"

Der Break-Befehl gibt einen Schlüssel zum Abbrechen eines Befehls an, der mit dem Flag "wait" aufgerufen wurde. Dieser Befehl ist ein MCI-Systembefehl. sie wird direkt von MCI interpretiert.

Um diesen Befehl zu senden, rufen Sie die [**mciSendString-Funktion**](/previous-versions//dd757161(v=vs.85)) mit dem *lpszCommand-Parameter* auf, der wie folgt festgelegt ist.

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

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Bezeichner eines MCI-Geräts. Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.

</dd> <dt>

<span id="lpszVirtKey"></span><span id="lpszvirtkey"></span><span id="LPSZVIRTKEY"></span>*lpszVirtKey*
</dt> <dd>

Eines der folgenden Flags.



| Wert                 | Bedeutung                                                                         |
|-----------------------|---------------------------------------------------------------------------------|
| für *code des virtuellen Schlüssels* | Gibt den Schlüssel an, der einen Befehl abbricht, der mit dem Flag "wait" gestartet wurde. |
| aus                   | Deaktiviert die aktuelle Haltetaste.                                                 |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Kann "wait", "notify" oder beides sein. Für digital-video- und VCR-Geräte kann auch "test" angegeben werden. Weitere Informationen zu diesen Flags finden Sie unter [Die Warte-, Benachrichtigungs- und Testflags](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls ein Fehler.

## <a name="remarks"></a>Hinweise

Wenn die Haltetaste aktiviert ist und der Benutzer den Schlüssel drückt, der durch den im *lpszVirtKey-Parameter* angegebenen virtuellen Schlüsselcode identifiziert wird, gibt das Gerät die Steuerung an die Anwendung zurück. Wenn möglich, setzt der Befehl die Ausführung fort.

## <a name="examples"></a>Beispiele

Der folgende Befehl legt F2 als Halteschlüssel für das Gerät "mysound" fest.

``` syntax
break mysound on 113
```

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>       |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Mci](mci.md)
</dt> <dt>

[MCI-Befehlszeichenfolgen](mci-command-strings.md)
</dt> </dl>

 

