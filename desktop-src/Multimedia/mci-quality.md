---
title: MCI_QUALITY Befehl (Mmsystem.h)
description: Der \_ MCI QUALITY-Befehl definiert eine benutzerdefinierte Qualitätsstufe für die Komprimierung von Audio-, Video- oder Standbilddaten. Digitalvideogeräte erkennen diesen Befehl.
ms.assetid: 91ad9704-0089-4b1f-b0f6-919ab5fd84e0
keywords:
- MCI_QUALITY Befehl Windows Multimedia
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
ms.openlocfilehash: 1237d9b70c9f06782342c404c19dd23cf6f0848f8c7b33523bce35990287fa27
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118138221"
---
# <a name="mci_quality-command"></a>MCI \_ QUALITY-Befehl

Der \_ MCI QUALITY-Befehl definiert eine benutzerdefinierte Qualitätsstufe für die Komprimierung von Audio-, Video- oder Standbilddaten. Digitalvideogeräte erkennen diesen Befehl.

Rufen Sie zum Senden dieses Befehls die [**mciSendCommand-Funktion**](/previous-versions//dd757160(v=vs.85)) mit den folgenden Parametern auf.


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

<span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*
</dt> <dd>

Gerätebezeichner des MCI-Geräts, das die Befehlsmeldung empfangen soll.

</dd> <dt>

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*Dwflags*
</dt> <dd>

MCI \_ NOTIFY, MCI \_ WAIT oder MCI \_ TEST. Informationen zu diesen Flags finden Sie unter [Die Warte-, Benachrichtigungs- und Testflags.](the-wait-notify-and-test-flags.md)

</dd> <dt>

<span id="lpQuality"></span><span id="lpquality"></span><span id="LPQUALITY"></span>*lpQuality*
</dt> <dd>

Zeiger auf eine [**MCI \_ DGV \_ QUALITY \_ PARMS-Struktur.**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_quality_parmsa)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn der Fehler erfolgreich war, oder andernfalls ein Fehler.

## <a name="remarks"></a>Hinweise

Der für diese Qualitätsstufe definierte Name kann beim Festlegen der Audio-, Video- oder noch-Qualität mit den Befehlen [MCI \_ SETAUDIO](mci-setaudio.md) und [MCI \_ SETVIDEO](mci-setvideo.md) verwendet werden.

Die folgenden zusätzlichen Flags gelten für Digitalvideogeräte:

<dl> <dt>

<span id="MCI_QUALITY_ALG"></span><span id="mci_quality_alg"></span>MCI \_ QUALITY \_ ALG
</dt> <dd>

Der **lpstrAlgorithm-Member** der von *lpQuality* identifizierten Struktur enthält eine Adresse eines Puffers, der den Namen des Algorithmus enthält. Dieser Algorithmus muss vom Gerätetreiber unterstützt werden und mit dem verwendeten Audio-, Still- oder Videodeskriptor kompatibel sein. Wenn dieses Flag ausgelassen wird, wird der aktuelle Algorithmus verwendet.

</dd> <dt>

<span id="MCI_QUALITY_DIALOG"></span><span id="mci_quality_dialog"></span>\_ \_ MCI-QUALITÄTSDIALOG
</dt> <dd>

Der Gerätetreiber sollte ein Dialogfeld zum Angeben des Qualitätsgrads anzeigen. Das Dialogfeld enthält algorithmusspezifische Felder, die intern vom Gerätetreiber verwendet werden, um eine Struktur zu erstellen, die eine bestimmte Qualitätsstufe beschreibt.

</dd> <dt>

<span id="MCI_QUALITY_HANDLE"></span><span id="mci_quality_handle"></span>MCI \_ QUALITY \_ HANDLE
</dt> <dd>

Der **dwHandle-Member** der von *lpQuality* identifizierten Struktur enthält ein Handle für eine -Struktur. Die -Struktur enthält algorithmisch spezifische Daten, die die spezifische Qualitätsstufe beschreiben. Das Format der Strukturen für die Algorithmen ist geräteabhängig.

</dd> <dt>

<span id="MCI_QUALITY_ITEM"></span><span id="mci_quality_item"></span>\_MCI-QUALITÄTSELEMENT \_
</dt> <dd>

Eine Konstante, die den Algorithmustyp angibt, ist im **dwItem-Member** der durch *lpQuality* identifizierten Struktur enthalten.

</dd> <dt>

<span id="MCI_QUALITY_NAME"></span><span id="mci_quality_name"></span>\_MCI-QUALITÄTSNAME \_
</dt> <dd>

Der **lpstrName-Member** der von *lpQuality* identifizierten Struktur enthält eine Adresse eines Puffers, der den Qualitätsdeskriptor enthält.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Mmsystem.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mci](mci.md)
</dt> <dt>

[MCI-Befehle](mci-commands.md)
</dt> </dl>

 

