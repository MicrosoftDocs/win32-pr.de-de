---
title: sysinfo-Befehl
description: Der sysinfo-Befehl ruft MCI-Systeminformationen ab. Der sysinfo-Befehl ist ein MCI-Systembefehl. sie wird direkt von MCI interpretiert.
ms.assetid: 494e8976-aac3-4d9f-b14b-3d3fd1917b45
keywords:
- sysinfo-Befehl Windows Multimedia
topic_type:
- apiref
api_name:
- sysinfo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a0af11370fd3968a2f5a6cf296ea04507f18d517665071674cfa8a4573e1a4f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119688330"
---
# <a name="sysinfo-command"></a>sysinfo-Befehl

Der sysinfo-Befehl ruft MCI-Systeminformationen ab. Der sysinfo-Befehl ist ein MCI-Systembefehl. sie wird direkt von MCI interpretiert.

Um diesen Befehl zu senden, rufen Sie die [**mciSendString-Funktion**](/previous-versions//dd757161(v=vs.85)) auf, wobei der *lpszCommand-Parameter* wie folgt festgelegt ist.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("sysinfo %s %s %s"), 
  lpszDeviceID, 
  lpszRequest, 
  lpszFlags
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*lpszDeviceID* 
</dt> <dd>

Bezeichner eines MCI-Geräts oder -Gerätetyps. Wenn ein Gerätetyp angegeben wird, muss es sich um einen MCI-Standardgerätetypnamen handelt, wie im Referenzmaterial für den [**Funktionsbefehl**](capability.md) aufgeführt. Sie können "all" angeben, wenn das in *lpszRequest* angegebene Flag diese Möglichkeit zulässt.

</dd> <dt>

*lpszRequest* 
</dt> <dd>

Eines der folgenden Flags.



| Wert                                                                                                                                                                | Bedeutung                                                                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="installname"></span><span id="INSTALLNAME"></span><dl> <dt>**installname**</dt> </dl>               | Gibt den Namen zurück, der in der Registrierung oder in der SYSTEM.INI Datei aufgeführt ist, die zum Installieren des geöffneten Geräts mit dem angegebenen Gerätebezeichner verwendet wird.<br/>                                                                                                                                                                                                            |
| <span id="quantity"></span><span id="QUANTITY"></span><dl> <dt>**Menge**</dt> </dl>                        | Gibt die Anzahl der MCI-Geräte zurück, die in der Registrierung oder in der SYSTEM.INI Datei des im *lpszDeviceID-Parameter angegebenen* Typs aufgeführt sind. Dieser Gerätebezeichner muss ein MCI-Standardgerätetypname sein. Alle Ziffern nach dem Gerätetyp werden ignoriert. Wenn Sie "all" für *lpszDeviceID* angeben, wird die Gesamtzahl der MCI-Geräte im System zurückgegeben.<br/> |
| <span id="quantity_open"></span><span id="QUANTITY_OPEN"></span><dl> <dt>**Menge geöffnet**</dt> </dl>         | Gibt die Anzahl der offenen MCI-Geräte des in *lpszDeviceID angegebenen* Typs zurück. Dieser Gerätebezeichner muss ein MCI-Standardgerätetypname sein. Wenn Sie "all" für *lpszDeviceID* angeben, wird die Gesamtzahl der offenen MCI-Geräte im System zurückgegeben.<br/>                                                                                                 |
| <span id="name_index"></span><span id="NAME_INDEX"></span><dl> <dt>**Name *Index**</dt> </dl>                | Gibt den Namen eines MCI-Geräts zurück. Der Gerätebezeichner muss ein MCI-Standardgerätetypname sein. Der *Index* reicht von 1 bis zur Anzahl der Geräte dieses Typs. Wenn "all" für *lpszDeviceID* angegeben wird, reicht der *Index* von 1 bis zur Gesamtzahl der Geräte im System.<br/>                                                                |
| <span id="name_index_open"></span><span id="NAME_INDEX_OPEN"></span><dl> <dt>**Name *Index* geöffnet**</dt> </dl> | Gibt den Namen eines geöffneten MCI-Geräts zurück. Der Gerätebezeichner muss ein MCI-Standardgerätetypname sein. Der *Index* reicht von 1 bis zur Anzahl der geöffneten Geräte dieses Gerätetyps. Wenn "all" für *lpszDeviceID* angegeben wird, reicht der *Index* von 1 bis zur Gesamtzahl der geöffneten Geräte im System.<br/>                                          |



 

</dd> <dt>

*lpszFlags* 
</dt> <dd>

Kann "wait", "notify" oder beides sein. Für DigitalVideo- und VCR-Geräte kann auch "Test" angegeben werden. Weitere Informationen zu diesen Flags finden Sie unter [Die Warte-, Benachrichtigungs- und Testflags.](the-wait-notify-and-test-flags.md)

</dd> </dl>

## <a name="examples"></a>Beispiele

Der folgende Befehl gibt die Anzahl der offenen Waveform-Audiogeräte zurück.

``` syntax
sysinfo waveaudio quantity open
```

Der folgende Befehl gibt den Namen (Gerätealias) des ersten geöffneten Waveform-Audio-Geräts zurück.

``` syntax
sysinfo waveaudio name 1 open
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

[**Fähigkeit**](capability.md)
</dt> </dl>

 

