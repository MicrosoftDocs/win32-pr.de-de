---
title: sysinfo-Befehl
description: Der sysinfo-Befehl ruft MCI-Systeminformationen ab. Der sysinfo-Befehl ist ein MCI-Systembefehl. Sie wird direkt von MCI interpretiert.
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
ms.openlocfilehash: 4751a5633462afe1ca8e8cd9abee1afeb16ac242
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342479"
---
# <a name="sysinfo-command"></a>sysinfo-Befehl

Der sysinfo-Befehl ruft MCI-Systeminformationen ab. Der sysinfo-Befehl ist ein MCI-Systembefehl. Sie wird direkt von MCI interpretiert.

Um diesen Befehl zu senden, wenden Sie die [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion mit dem festgelegten *lpszcommand* -Parameter wie folgt an.

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

*lpszde viceid* 
</dt> <dd>

Der Bezeichner eines MCI-Geräts oder-Gerätetyps. Wenn ein Gerätetyp angegeben wird, muss es sich um einen standardmäßigen MCI-Gerätetyp Namen handeln, wie im Referenzmaterial für [**den Funktions**](capability.md) Befehl aufgeführt. Sie können "All" angeben, wenn das in *lpszrequest* angegebene Flag diese Möglichkeit zulässt.

</dd> <dt>

*lpszrequest* 
</dt> <dd>

Eines der folgenden Flags.



| Wert                                                                                                                                                                | Bedeutung                                                                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="installname"></span><span id="INSTALLNAME"></span><dl> <dt>**installname**</dt> </dl>               | Gibt den Namen zurück, der in der Registrierung aufgeführt ist, oder die SYSTEM.INI Datei, die zum Installieren des geöffneten Geräts mit der angegebenen Gerätekennung verwendet wird.<br/>                                                                                                                                                                                                            |
| <span id="quantity"></span><span id="QUANTITY"></span><dl> <dt>**Mess**</dt> </dl>                        | Gibt die Anzahl der in der Registrierung aufgelisteten MCI-Geräte oder die SYSTEM.INI Datei des im *lpszdeviceid* -Parameter angegebenen Typs zurück. Bei dieser Gerätekennung muss es sich um einen standardmäßigen MCI-Gerätetyp Namen handeln. Alle Ziffern nach dem Gerätetyp werden ignoriert. Bei Angabe von "All" für *lpszde viceid* wird die Gesamtzahl der MCI-Geräte im System zurückgegeben.<br/> |
| <span id="quantity_open"></span><span id="QUANTITY_OPEN"></span><dl> <dt>**Menge geöffnet**</dt> </dl>         | Gibt die Anzahl der geöffneten MCI-Geräte des in " *lpszdeviceid*" angegebenen Typs zurück. Bei dieser Gerätekennung muss es sich um einen standardmäßigen MCI-Gerätetyp Namen handeln. Bei Angabe von "All" für *lpsztoviceid* wird die Gesamtzahl der geöffneten MCI-Geräte im System zurückgegeben.<br/>                                                                                                 |
| <span id="name_index"></span><span id="NAME_INDEX"></span><dl> <dt>* * Name * Index * * *</dt> </dl>                | Gibt den Namen eines MCI-Geräts zurück. Der Geräte Bezeichner muss ein standardmäßiger MCI-Gerätetyp Name sein. Der *Index* liegt zwischen 1 und der Anzahl der Geräte dieses Typs. Wenn "All" für *lpszde viceid* angegeben ist, liegt der *Index* zwischen 1 und der Gesamtzahl der Geräte im System.<br/>                                                                |
| <span id="name_index_open"></span><span id="NAME_INDEX_OPEN"></span><dl> <dt>**namens *Index* geöffnet**</dt> </dl> | Gibt den Namen eines geöffneten MCI-Geräts zurück. Der Geräte Bezeichner muss ein standardmäßiger MCI-Gerätetyp Name sein. Der *Index* liegt zwischen 1 und der Anzahl der geöffneten Geräte dieses Gerätetyps. Wenn "All" für *lpszde viceid* angegeben ist, liegt der *Index* zwischen 1 und der Gesamtzahl der geöffneten Geräte im System.<br/>                                          |



 

</dd> <dt>

*lpszflags* 
</dt> <dd>

Kann "wait", "notify" oder beides sein. Für Digital Video-und VCR-Geräte kann auch "Test" angegeben werden. Weitere Informationen zu diesen Flags finden Sie [unter warte-, Benachrichtigungs-und testflags](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="examples"></a>Beispiele

Mit dem folgenden Befehl wird die Anzahl der geöffneten Wellenform-Audiogeräte zurückgegeben.

``` syntax
sysinfo waveaudio quantity open
```

Der folgende Befehl gibt den Namen (Gerätealias) des ersten geöffneten Waveform-Audiogeräts zurück.

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

[MCI](mci.md)
</dt> <dt>

[MCI-Befehls Zeichenfolgen](mci-command-strings.md)
</dt> <dt>

[**Re**](capability.md)
</dt> </dl>

 

