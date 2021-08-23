---
title: MCI_REALIZE Befehl (Mmsystem.h)
description: Der MCI \_ REALIZE-Befehl bewirkt, dass ein Grafikgerät seine Palette in einen Gerätekontext (DC) umsetzt. Digitalvideogeräte erkennen diesen Befehl.
ms.assetid: cbc9e6ef-a372-4ddb-b7f3-ea99ac14ec95
keywords:
- MCI_REALIZE Befehl Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_REALIZE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e81204fe679d543438a0d0dcc7ec333462cb6a3d0c30212706969dc22a143df1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119689830"
---
# <a name="mci_realize-command"></a>MCI \_ REALIZE-Befehl

Der MCI \_ REALIZE-Befehl bewirkt, dass ein Grafikgerät seine Palette in einen Gerätekontext (DC) umsetzt. Digitalvideogeräte erkennen diesen Befehl.

Rufen Sie zum Senden dieses Befehls die [**mciSendCommand-Funktion**](/previous-versions//dd757160(v=vs.85)) mit den folgenden Parametern auf.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_REALIZE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpRealize
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

**MCI \_ NOTIFY,** **MCI \_ WAIT** oder bei Geräten mit digitalen Videos **MCI \_ TEST**. Informationen zu diesen Flags finden Sie unter [Die Warte-, Benachrichtigungs- und Testflags.](the-wait-notify-and-test-flags.md)

</dd> <dt>

<span id="lpRealize"></span><span id="lprealize"></span><span id="LPREALIZE"></span>*lpRealize*
</dt> <dd>

Zeiger auf eine [**GENERISCHE \_ MCI-PARMS-Struktur. \_**](mci-generic-parms.md) (Geräte mit erweiterten Befehlssätzen können diese Struktur durch eine gerätespezifische Struktur ersetzen.)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn der Fehler erfolgreich war, oder andernfalls ein Fehler.

## <a name="remarks"></a>Hinweise

Sie sollten diesen Befehl verwenden, wenn Ihre Anwendung die [**WM \_ QUERYNEWPALETTE-Nachricht**](/windows/desktop/gdi/wm-querynewpalette) empfängt.

Die folgenden zusätzlichen Flags werden mit dem Gerätetyp "digitalvideo" verwendet:

<dl> <dt>

<span id="MCI_DGV_REALIZE_BKGD"></span><span id="mci_dgv_realize_bkgd"></span>MCI \_ DGV \_ REALIZE \_ BKGD
</dt> <dd>

Erkennt die Palette als Hintergrundpalette.

</dd> <dt>

<span id="MCI_DGV_REALIZE_NORM"></span><span id="mci_dgv_realize_norm"></span>MCI \_ DGV \_ REALIZE \_ NORM
</dt> <dd>

Erkennt die Palette normal. Dies ist die Standardoption.

</dd> </dl>

Bei Digitalvideogeräten verweist der *lpRealize-Parameter* auf eine **MCI \_ REALIZE \_ PARMS-Struktur.** Weitere Informationen finden Sie in den Kommentaren in der [**\_ MCI GENERIC \_ PARMS-Struktur.**](mci-generic-parms.md)

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

 

