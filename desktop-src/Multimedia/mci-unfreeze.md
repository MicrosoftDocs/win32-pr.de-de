---
title: MCI_UNFREEZE Befehl (Mmsystem.h)
description: Der \_ MCI UNFREEZE-Befehl stellt die Bewegung in einem Bereich des Videopuffers wieder her, der mit dem MCI FREEZE-Befehl fixiert \_ wurde. Digitalvideo-, VCR- und Videoüberlagerungsgeräte erkennen diesen Befehl.
ms.assetid: 79ff1be5-6e30-4ef4-ab81-fc5643e3a72d
keywords:
- MCI_UNFREEZE Befehl Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_UNFREEZE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3011f3d2c05c304b37957c6f4cb78f2ada9389ab727a7af63a358fd4b5afdd3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119525570"
---
# <a name="mci_unfreeze-command"></a>MCI \_ UNFREEZE-Befehl

Der \_ MCI UNFREEZE-Befehl stellt die Bewegung in einem Bereich des Videopuffers wieder her, der mit dem [MCI \_ FREEZE-Befehl](mci-freeze.md) fixiert wurde. Digitalvideo-, VCR- und Videoüberlagerungsgeräte erkennen diesen Befehl.

Rufen Sie zum Senden dieses Befehls die [**mciSendCommand-Funktion**](/previous-versions//dd757160(v=vs.85)) mit den folgenden Parametern auf.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_UNFREEZE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpUnfreeze
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

MCI \_ NOTIFY, MCI \_ WAIT oder, für Digital Video- und VCR-Geräte, MCI \_ TEST. Informationen zu diesen Flags finden Sie unter [Die Warte-, Benachrichtigungs- und Testflags.](the-wait-notify-and-test-flags.md)

</dd> <dt>

<span id="lpUnfreeze"></span><span id="lpunfreeze"></span><span id="LPUNFREEZE"></span>*lpUnfreeze*
</dt> <dd>

Zeiger auf eine [**GENERISCHE \_ MCI-PARMS-Struktur. \_**](mci-generic-parms.md) (Geräte mit erweiterten Befehlssätzen können diese Struktur durch eine gerätespezifische Struktur ersetzen.)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn der Fehler erfolgreich war, oder andernfalls ein Fehler.

## <a name="remarks"></a>Hinweise

Das folgende zusätzliche Flag wird mit dem **Gerätetyp digitalvideo** verwendet:

MCI \_ DGV \_ RECT

Der **rc-Member** der von *lpUnfreeze* identifizierten Struktur enthält ein gültiges Anzeigerechteck. Das Rechteck gibt einen Bereich innerhalb des Rahmenpuffers an, dessen Pixel das Sperrmaskenbit deaktivieren sollen. Rechteckige Bereiche werden wie für den [MCI \_ PUT-Befehl](mci-put.md) beschrieben angegeben. Wenn dies nicht angegeben wird, wird das Rechteck standardmäßig auf den gesamten Framepuffer verwendet. Mithilfe einer Sequenz von Befehlen zum Einfrieren und Aufheben der Fixierung mit unterschiedlichen Rechtecke können beliebige Muster von Sperrmaskenbits beschrieben werden.

Bei Digitalvideogeräten verweist der *lpUnfreeze-Parameter* auf eine **MCI \_ DGV \_ UNFREEZE \_ PARMS-Struktur.** Weitere Informationen finden Sie in den Kommentaren zur [**MCI \_ DGV \_ RECT \_ PARMS-Struktur.**](/windows/win32/api/digitalv/ns-digitalv-mci_dgv_rect_parms)

Die folgenden zusätzlichen Flags werden mit dem **Vcr-Gerätetyp** verwendet:

<dl> <dt>

<span id="MCI_VCR_UNFREEZE_INPUT"></span><span id="mci_vcr_unfreeze_input"></span>MCI \_ VCR \_ UNFREEZE \_ INPUT
</dt> <dd>

Entbinden Sie die Eingabe.

</dd> <dt>

<span id="MCI_VCR_UNFREEZE_OUTPUT"></span><span id="mci_vcr_unfreeze_output"></span>MCI \_ VCR \_ UNFREEZE \_ OUTPUT
</dt> <dd>

Aufheben der Freigabe der Ausgabe.

</dd> </dl>

Das folgende zusätzliche Flag wird mit dem **Überlagerungsgerätetyp** verwendet:

<dl> <dt>

<span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>MCI \_ OVLY \_ RECT
</dt> <dd>

Der **rc-Member** der von *lpUnfreeze* identifizierten Struktur enthält ein gültiges Anzeigerechteck. Dies ist ein erforderlicher Parameter.

</dd> </dl>

Bei Videoüberlagerungsgeräten zeigt der *lpUnfreeze-Parameter* auf eine [**MCI \_ OVLY \_ RECT \_ PARMS-Struktur.**](mci-ovly-rect-parms.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Mmsystem.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Mci](mci.md)
</dt> <dt>

[MCI-Befehle](mci-commands.md)
</dt> </dl>

 

