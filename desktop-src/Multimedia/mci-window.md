---
title: MCI_WINDOW Befehl (Mmsystem.h)
description: Der \_ MCI WINDOW-Befehl gibt das Fenster und die Fenstermerkmale für Grafikgeräte an. Digital-Video- und Videoüberlagerungsgeräte erkennen diesen Befehl.
ms.assetid: 8b6c4d9a-ee72-4c64-aebe-6c8153167496
keywords:
- MCI_WINDOW Befehl Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_WINDOW
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3270dce8b2127cce783c7c3b8bf21102590cd3e82d74a3e990a3117c59772381
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119783690"
---
# <a name="mci_window-command"></a>MCI \_ WINDOW-Befehl

Der \_ MCI WINDOW-Befehl gibt das Fenster und die Fenstermerkmale für Grafikgeräte an. Digital-Video- und Videoüberlagerungsgeräte erkennen diesen Befehl.

Rufen Sie zum Senden dieses Befehls die [**mciSendCommand-Funktion**](/previous-versions//dd757160(v=vs.85)) mit den folgenden Parametern auf.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_WINDOW, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpWindow
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

MCI \_ NOTIFY, MCI \_ WAIT oder, für Digital Video-Geräte, MCI \_ TEST. Informationen zu diesen Flags finden Sie unter [Die Warte-, Benachrichtigungs- und Testflags.](the-wait-notify-and-test-flags.md)

</dd> <dt>

<span id="lpWindow"></span><span id="lpwindow"></span><span id="LPWINDOW"></span>*lpWindow*
</dt> <dd>

Zeiger auf eine [**GENERISCHE \_ MCI-PARMS-Struktur. \_**](mci-generic-parms.md) (Geräte mit erweiterten Befehlssätzen können diese Struktur durch eine gerätespezifische Struktur ersetzen.)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn der Fehler erfolgreich war, oder andernfalls ein Fehler.

## <a name="remarks"></a>Hinweise

Grafikgeräte sollten beim Öffnen eines Geräts ein Standardfenster erstellen, es jedoch erst anzeigen, wenn sie den [MCI \_ PLAY-Befehl](mci-play.md) erhalten. Der \_ MCI WINDOW-Befehl wird verwendet, um dem Gerät ein von der Anwendung erstelltes Fenster zur Verfügung zu stellen und die Anzeigemerkmale eines anwendungsdefiniert oder standardmäßigen Anzeigefensters zu ändern. Wenn die Anwendung das Anzeigefenster zur Verfügung stellt, sollte sie darauf vorbereitet sein, ein ungültiges Rechteck im Fenster zu aktualisieren.

Die folgenden zusätzlichen Flags werden mit dem **Gerätetyp digitalvideo** verwendet:

<dl> <dt>

<span id="MCI_DGV_WINDOW_HWND"></span><span id="mci_dgv_window_hwnd"></span>MCI \_ DGV \_ WINDOW \_ HWND
</dt> <dd>

Das Handle des Fensters, das für die Verwendung als Ziel benötigt wird, ist im **hWnd-Member** der von *lpWindow* identifizierten Struktur enthalten.

</dd> <dt>

<span id="MCI_DGV_WINDOW_STATE"></span><span id="mci_dgv_window_state"></span>MCI \_ DGV \_ WINDOW \_ STATE
</dt> <dd>

Der **nCmdShow-Member** der von *lpWindow* identifizierten Struktur enthält Parameter zum Festlegen des Fensterzustands.

</dd> <dt>

<span id="MCI_DGV_WINDOW_TEXT"></span><span id="mci_dgv_window_text"></span>MCI \_ DGV \_ WINDOW \_ TEXT
</dt> <dd>

Der **lpstrText-Member** der von *lpWindow* identifizierten Struktur enthält eine Adresse eines Puffers, der die beschriftung enthält, die in der Titelleiste des Fensters verwendet wird.

</dd> </dl>

Bei Digitalvideogeräten verweist der *lpWindow-Parameter* auf eine [**MCI \_ DGV \_ WINDOW \_ PARMS-Struktur.**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_window_parmsa)

Die folgenden zusätzlichen Flags werden mit dem **Überlagerungsgerätetyp** verwendet:

<dl> <dt>

<span id="MCI_OVLY_WINDOW_DISABLE_STRETCH"></span><span id="mci_ovly_window_disable_stretch"></span>MCI \_ OVLY \_ WINDOW \_ DISABLE \_ STRETCH
</dt> <dd>

Deaktiviert das Stretching des Bilds.

</dd> <dt>

<span id="MCI_OVLY_WINDOW_ENABLE_STRETCH"></span><span id="mci_ovly_window_enable_stretch"></span>MCI \_ OVLY \_ WINDOW \_ ENABLE \_ STRETCH
</dt> <dd>

Aktiviert stretching des Bilds.

</dd> <dt>

<span id="MCI_OVLY_WINDOW_HWND"></span><span id="mci_ovly_window_hwnd"></span>MCI \_ OVLY \_ WINDOW \_ HWND
</dt> <dd>

Das Handle des für das Ziel verwendeten Fensters ist im **hWnd-Member** der von *lpWindow* identifizierten Struktur enthalten. Legen Sie dieses Flag auf MCI \_ OVLY \_ WINDOW \_ DEFAULT fest, um zum Standardfenster zurückzukehren.

</dd> <dt>

<span id="MCI_OVLY_WINDOW_STATE"></span><span id="mci_ovly_window_state"></span>\_ \_ MCI-OVLY-FENSTERSTATUS \_
</dt> <dd>

Der **nCmdShow-Member** der *lpWindow-Struktur* enthält Parameter zum Festlegen des Fensterzustands. Dieses Flag entspricht dem Aufrufen von [ShowWindow](/windows/win32/api/winuser/nf-winuser-showwindow) mit dem *State-Parameter.* Die Konstanten sind mit denen identisch, die in WINDOWS definiert sind. H (z. B. SW \_ HIDE, SW \_ MINIMIZE oder SW \_ SHOWNORMAL).

</dd> <dt>

<span id="MCI_OVLY_WINDOW_TEXT"></span><span id="mci_ovly_window_text"></span>MCI \_ \_ OVLY-FENSTERTEXT \_
</dt> <dd>

Der **lpstrText-Member** der von *lpWindow* identifizierten Struktur enthält eine Adresse eines Puffers, der die für das Fenster verwendete Beschriftung enthält.

</dd> </dl>

Bei Videoüberlagerungsgeräten zeigt der *lpWindow-Parameter* auf eine [**\_ MCI-OVLY \_ WINDOW \_ PARMS-Struktur.**](mci-ovly-window-parms.md)

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

 

