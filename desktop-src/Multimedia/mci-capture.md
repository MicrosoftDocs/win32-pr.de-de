---
title: MCI_CAPTURE Befehl (Mmsystem.h)
description: Der MCI \_ CAPTURE-Befehl erfasst den Inhalt des Framepuffers und speichert ihn in einer angegebenen Datei. Digitalvideogeräte erkennen diesen Befehl.
ms.assetid: bdebddc5-a0a0-449e-889e-37c7d6612c60
keywords:
- MCI_CAPTURE-Befehl Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_CAPTURE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cc6bc6e31fd66153a8ea867f56a4e2638ad1f3392a284a61818e521327e52d6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039450"
---
# <a name="mci_capture-command"></a>MCI \_ CAPTURE-Befehl

Der MCI \_ CAPTURE-Befehl erfasst den Inhalt des Framepuffers und speichert ihn in einer angegebenen Datei. Digitalvideogeräte erkennen diesen Befehl.

Um diesen Befehl zu senden, rufen Sie die [**mciSendCommand-Funktion**](/previous-versions//dd757160(v=vs.85)) mit den folgenden Parametern auf.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_CAPTURE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_CAPTURE_PARMS) lpCapture
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*
</dt> <dd>

Gerätebezeichner des MCI-Geräts, das die Befehlsnachricht empfangen soll.

</dd> <dt>

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*Dwflags*
</dt> <dd>

MCI \_ NOTIFY, MCI \_ WAIT oder MCI \_ TEST. Informationen zu diesen Flags finden Sie unter [Die Warte-, Benachrichtigungs- und Testflags](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpCapture"></span><span id="lpcapture"></span><span id="LPCAPTURE"></span>*lpCapture*
</dt> <dd>

Zeiger auf eine [**MCI \_ DGV \_ CAPTURE \_ PARMS-Struktur.**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_capture_parmsa)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls ein Fehler.

## <a name="remarks"></a>Hinweise

Die folgenden zusätzlichen Flags gelten für Digitalvideogeräte:

<dl> <dt>

<span id="MCI_DGV_CAPTURE_AS"></span><span id="mci_dgv_capture_as"></span>MCI \_ DGV \_ CAPTURE \_ AS
</dt> <dd>

Der **lpstrFileName-Member** der durch *lpCapture* identifizierten Struktur enthält eine Adresse eines Puffers, der den Zielpfad und den Dateinamen an gibt. (Dieses Flag ist erforderlich.)

</dd> <dt>

<span id="MCI_DGV_CAPTURE_AT"></span><span id="mci_dgv_capture_at"></span>MCI \_ DGV \_ CAPTURE \_ AT
</dt> <dd>

Der **rc-Member** der durch *lpCapture identifizierten* Struktur enthält ein gültiges Rechteck. Das Rechteck gibt den rechteckigen Bereich innerhalb des Framepuffers an, der zugeschnitten und auf dem Datenträger gespeichert wird. Wenn dieser Wert weggelassen wird, wird für den zugeschnittenen Bereich standardmäßig das Rechteck verwendet, das für einen vorherigen [MCI \_ PUT-Befehl](mci-put.md) angegeben wurde, der den Quellbereich für diese Instanz des Gerätetreibers angibt.

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

 

