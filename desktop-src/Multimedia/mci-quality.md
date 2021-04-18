---
title: MCI_QUALITY Befehl (MMSYSTEM. h)
description: Mit dem MCI \_ -Qualitäts Befehl wird eine benutzerdefinierte Qualität für die Datenkomprimierung von Audiodaten, Videodaten oder Bild Daten definiert. Dieser Befehl wird von Digital-Video-Geräten erkannt.
ms.assetid: 91ad9704-0089-4b1f-b0f6-919ab5fd84e0
keywords:
- MCI_QUALITY Befehl Windows-Multimedia
topic_type:
- apiref
api_name:
- MCI_QUALITY
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 996703c1a5b7d3adec1a001af58ebc8d916301a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391510"
---
# <a name="mci_quality-command"></a>MCI- \_ Qualitäts Befehl

Mit dem MCI \_ -Qualitäts Befehl wird eine benutzerdefinierte Qualität für die Datenkomprimierung von Audiodaten, Videodaten oder Bild Daten definiert. Dieser Befehl wird von Digital-Video-Geräten erkannt.

Um diesen Befehl zu senden, wenden Sie die [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion mit den folgenden Parametern an.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_QUALITY, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_QUALITY_PARMS) lpQuality
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

MCI- \_ Benachrichtigung, MCI- \_ Wartezeit oder MCI- \_ Test. Weitere Informationen zu diesen Flags finden Sie [unter Wait-, notify-und testflags](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpQuality"></span><span id="lpquality"></span><span id="LPQUALITY"></span>*lpquality*
</dt> <dd>

Zeiger auf eine [**MCI \_ DGV \_ Quality \_**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_quality_parmsa) -Struktur.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.

## <a name="remarks"></a>Bemerkungen

Der Name, der für diese Qualitätsstufe definiert ist, kann beim Festlegen der Audiodatei, des Videos oder der Qualität mit den Befehls [MCI \_ setaudiound](mci-setaudio.md) [MCI \_ setvideo](mci-setvideo.md) verwendet werden.

Die folgenden zusätzlichen Flags gelten für Digital-Video-Geräte:

<dl> <dt>

<span id="MCI_QUALITY_ALG"></span><span id="mci_quality_alg"></span>MCI \_ Quality \_ alg
</dt> <dd>

Der **lpstrinalgorithmus** -Member der Struktur, die von *lpquality* identifiziert wird, enthält eine Adresse eines Puffers, der den Namen des Algorithmus enthält. Dieser Algorithmus muss vom Gerätetreiber unterstützt werden und muss mit dem verwendeten audiodeskriptor (noch) und dem verwendeten Video Deskriptor kompatibel sein. Wenn dieses Flag weggelassen wird, wird der aktuelle Algorithmus verwendet.

</dd> <dt>

<span id="MCI_QUALITY_DIALOG"></span><span id="mci_quality_dialog"></span>MCI- \_ Qualitäts \_ Dialogfeld
</dt> <dd>

Der Gerätetreiber sollte ein Dialogfeld zum Angeben der Qualitäts Ebene anzeigen. Das Dialogfeld enthält algorithmusspezifische Felder, die intern vom Gerätetreiber verwendet werden, um eine Struktur zu erstellen, die eine bestimmte Qualitätsstufe beschreibt.

</dd> <dt>

<span id="MCI_QUALITY_HANDLE"></span><span id="mci_quality_handle"></span>MCI- \_ Qualitäts \_ handle
</dt> <dd>

Der **dwhandle** -Member der-Struktur, die von *lpquality* identifiziert wird, enthält ein Handle für eine-Struktur. Die Struktur enthält algorithmische spezifische Daten, die die jeweilige Qualitätsstufe beschreiben. Das Format der Strukturen für die Algorithmen ist Geräte abhängig.

</dd> <dt>

<span id="MCI_QUALITY_ITEM"></span><span id="mci_quality_item"></span>MCI- \_ Qualitäts \_ Element
</dt> <dd>

Eine-Konstante, die angibt, dass der Algorithmustyp im **dwitem** -Member der durch *lpquality* identifizierten-Struktur enthalten ist.

</dd> <dt>

<span id="MCI_QUALITY_NAME"></span><span id="mci_quality_name"></span>Name der MCI- \_ Qualität \_
</dt> <dd>

Der **lpstrinname** -Member der Struktur, die von *lpquality* identifiziert wird, enthält eine Adresse eines Puffers, der den Qualitäts Deskriptor enthält.

</dd> </dl>

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

 

