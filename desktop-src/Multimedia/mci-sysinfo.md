---
title: MCI_SYSINFO Befehl (MMSYSTEM. h)
description: Der MCI- \_ Befehl sysinfo Ruft Informationen zu MCI-Geräten ab.
ms.assetid: 605efd25-8849-42aa-99fd-b36b6fd2c7b7
keywords:
- MCI_SYSINFO Befehl Windows-Multimedia
topic_type:
- apiref
api_name:
- MCI_SYSINFO
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e722625449893771726a83738c3b0d7bc8bc523c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956577"
---
# <a name="mci_sysinfo-command"></a>MCI- \_ sysinfo-Befehl

Der MCI- \_ Befehl sysinfo Ruft Informationen zu MCI-Geräten ab. MCI unterstützt diesen Befehl direkt, anstatt ihn an das Gerät zu übergeben. Alle MCI-Anwendungen können diesen Befehl verwenden. Zeichen folgen Informationen werden im von der Anwendung bereitgestellten Puffer zurückgegeben, auf den der **lpstraureturn** -Member der Struktur verweist, die von *lpsysinfo* identifiziert wird. Numerische Informationen werden als **DWORD** -Wert zurückgegeben, der in den von der Anwendung bereitgestellten Puffer eingefügt wird. Der **dwretsize** -Member gibt die Länge des Puffers an.

Um diesen Befehl zu senden, wenden Sie die [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion mit den folgenden Parametern an.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SYSINFO, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_SYSINFO_PARMS) lpSysInfo
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*WDE viceid*
</dt> <dd>

Geräte Bezeichner des MCI-Geräts, das die Befehls Meldung empfangen soll.

</dd> <dt>

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*
</dt> <dd>

Eines oder mehrere der folgenden Standard-und Befehls spezifischen Flags:

</dd> <dt>

<span id="MCI_SYSINFO_INSTALLNAME"></span><span id="mci_sysinfo_installname"></span>MCI- \_ sysinfo- \_ installname
</dt> <dd>

Ruft den Namen (aufgelistet in der Registrierung oder der SYSTEM.INI Datei) ab, der zur Installation des Geräts verwendet wird.

</dd> <dt>

<span id="MCI_SYSINFO_NAME"></span><span id="mci_sysinfo_name"></span>MCI- \_ sysinfo- \_ Name
</dt> <dd>

Erhält einen Gerätenamen, der der Gerätenummer entspricht, die im **dwnumber** -Member der von **lpsysinfo** identifizierten Struktur angegeben ist. Wenn das MCI- \_ Flag zum \_ Öffnen von sysinfo festgelegt ist, gibt MCI die Namen offener Geräte zurück.

</dd> <dt>

<span id="MCI_SYSINFO_OPEN"></span><span id="mci_sysinfo_open"></span>MCI- \_ sysinfo \_ geöffnet
</dt> <dd>

Ruft die Menge oder den Namen offener Geräte ab.

</dd> <dt>

<span id="MCI_SYSINFO_QUANTITY"></span><span id="mci_sysinfo_quantity"></span>MCI- \_ sysinfo- \_ Menge
</dt> <dd>

Ruft die Anzahl der Geräte des angegebenen Typs ab, die in der Registrierung oder im \[ MCI- \] Abschnitt der SYSTEM.INI Datei aufgeführt sind. Wenn das \_ geöffnende MCI-sysinfo- \_ Flag festgelegt ist, wird die Anzahl der geöffneten Geräte zurückgegeben.

</dd> <dt>

<span id="lpSysInfo"></span><span id="lpsysinfo"></span><span id="LPSYSINFO"></span>*lpsysinfo*
</dt> <dd>

Zeiger auf eine [**MCI- \_ sysinfo \_**](mci-sysinfo-parms.md) -Elementstruktur.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.

## <a name="remarks"></a>Bemerkungen

Der **wdevicetype** -Member der durch *lpsysinfo* identifizierten Struktur wird verwendet, um den Gerätetyp der Abfrage anzugeben. Wenn der *WDE viceid* -Parameter auf MCI \_ all Device ID festgelegt ist, wird \_ \_ der Wert von **wdebug Type** überschrieben. Eine Liste der Gerätetypen finden Sie unter [MCI-Gerätetypen](mci-device-types.md).

Ganzzahlige Rückgabewerte sind im Puffer zurückgegebene **DWORD** -Werte, auf die durch den **lpstraureturn** -Member der durch *lpsysinfo* identifizierten Struktur verwiesen wird.

Zeichen folgen Rückgabewerte sind im Puffer zurückgegebene NULL-terminierte Zeichen folgen, auf die durch den **lpstrreturn** -Member der durch *lpsysinfo* identifizierten Struktur verwiesen wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>MMSYSTEM. h (Include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[MCI-Befehle](mci-commands.md)
</dt> </dl>

 

