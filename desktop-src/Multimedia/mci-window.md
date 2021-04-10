---
title: MCI_WINDOW Befehl (MMSYSTEM. h)
description: Der MCI \_ -Fenster Befehl gibt das Fenster und die Fenster Eigenschaften für Grafikgeräte an. Dieser Befehl wird von Digital Video-und Video Überlagerungs Geräten erkannt.
ms.assetid: 8b6c4d9a-ee72-4c64-aebe-6c8153167496
keywords:
- MCI_WINDOW Befehl Windows-Multimedia
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
ms.openlocfilehash: 41b4d630dbc9dbc7403e93cd0bda3de2eef1e5cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956614"
---
# <a name="mci_window-command"></a>Befehl "MCI- \_ Fenster"

Der MCI \_ -Fenster Befehl gibt das Fenster und die Fenster Eigenschaften für Grafikgeräte an. Dieser Befehl wird von Digital Video-und Video Überlagerungs Geräten erkannt.

Um diesen Befehl zu senden, wenden Sie die [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion mit den folgenden Parametern an.


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

<span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*WDE viceid*
</dt> <dd>

Geräte Bezeichner des MCI-Geräts, das die Befehls Meldung empfangen soll.

</dd> <dt>

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*
</dt> <dd>

MCI- \_ Benachrichtigung, MCI- \_ Wartezeit oder, für Digital Video-Geräte, MCI- \_ Test. Weitere Informationen zu diesen Flags finden Sie [unter Wait-, notify-und testflags](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpWindow"></span><span id="lpwindow"></span><span id="LPWINDOW"></span>*lpwindow*
</dt> <dd>

Zeiger auf eine [**generische MCI-Struktur von \_ \_ Parametern**](mci-generic-parms.md) . (Geräte mit erweiterten Befehlssätzen können diese Struktur durch eine gerätespezifische Struktur ersetzen.)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.

## <a name="remarks"></a>Bemerkungen

Grafikgeräte sollten ein Standardfenster erstellen, wenn ein Gerät geöffnet wird, das jedoch erst angezeigt werden soll, wenn der Befehl " [MCI \_ Play](mci-play.md) " empfangen wird. Der MCI \_ -Fenster Befehl wird verwendet, um ein von der Anwendung erstelltes Fenster für das Gerät bereitzustellen und die Anzeigeeigenschaften eines Anwendungs definierten oder standardmäßigen Anzeige Fensters zu ändern. Wenn die Anwendung das Anzeige Fenster bereitstellt, sollte Sie darauf vorbereitet sein, ein ungültiges Rechteck im Fenster zu aktualisieren.

Die folgenden zusätzlichen Flags werden mit dem **Digitalvideo** -Gerätetyp verwendet:

<dl> <dt>

<span id="MCI_DGV_WINDOW_HWND"></span><span id="mci_dgv_window_hwnd"></span>MCI- \_ DGV- \_ Fenster ( \_ HWND)
</dt> <dd>

Das Handle des Fensters, das für die Verwendung als Ziel benötigt wird, ist im **HWND** -Member der durch *lpwindow* identifizierten Struktur enthalten.

</dd> <dt>

<span id="MCI_DGV_WINDOW_STATE"></span><span id="mci_dgv_window_state"></span>Status des MCI- \_ DGV- \_ Fensters \_
</dt> <dd>

Der **nCmdShow** -Member der Struktur, die von *lpwindow* identifiziert wird, enthält Parameter zum Festlegen des Fenster Zustands.

</dd> <dt>

<span id="MCI_DGV_WINDOW_TEXT"></span><span id="mci_dgv_window_text"></span>MCI- \_ DGV- \_ Fenster \_ Text
</dt> <dd>

Der **lpstrautext** -Member der durch *lpwindow* identifizierten Struktur enthält die Adresse eines Puffers, der die in der Fenstertitelleiste verwendete Beschriftung enthält.

</dd> </dl>

Für Digital Video-Geräte verweist der *lpwindow* -Parameter auf eine [**MCI- \_ DGV- \_ Fenster \_**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_window_parmsa) -Struktur.

Die folgenden zusätzlichen Flags werden mit dem **Überlagerungs** Gerätetyp verwendet:

<dl> <dt>

<span id="MCI_OVLY_WINDOW_DISABLE_STRETCH"></span><span id="mci_ovly_window_disable_stretch"></span>MCI- \_ OVLY- \_ Fenster zum Deaktivieren der \_ \_ Streckung
</dt> <dd>

Deaktiviert die Streckung des Bilds.

</dd> <dt>

<span id="MCI_OVLY_WINDOW_ENABLE_STRETCH"></span><span id="mci_ovly_window_enable_stretch"></span>MCI- \_ OVLY- \_ Fenster zum Aktivieren der \_ \_ Streckung
</dt> <dd>

Ermöglicht das Stretching des Bilds.

</dd> <dt>

<span id="MCI_OVLY_WINDOW_HWND"></span><span id="mci_ovly_window_hwnd"></span>MCI \_ OVLY \_ Window \_ HWND
</dt> <dd>

Das Handle des Fensters, das für das Ziel verwendet wird, ist in das **HWND** -Element der von *lpwindow* identifizierten Struktur eingeschlossen. Legen Sie dieses Flag auf MCI \_ OVLY \_ Window \_ default fest, um zum Standardfenster zurückzukehren.

</dd> <dt>

<span id="MCI_OVLY_WINDOW_STATE"></span><span id="mci_ovly_window_state"></span>Status des MCI- \_ OVLY- \_ Fensters \_
</dt> <dd>

Der **nCmdShow** -Member der *lpwindow* -Struktur enthält Parameter zum Festlegen des Fenster Zustands. Dieses Flag entspricht dem Aufrufen von [ShowWindow](/windows/win32/api/winuser/nf-winuser-showwindow) mit dem *State* -Parameter. Die Konstanten sind identisch mit den in Windows definierten Konstanten. H (z. b \_ . SW Hide, SW \_ minimieren oder SW \_ shownormal).

</dd> <dt>

<span id="MCI_OVLY_WINDOW_TEXT"></span><span id="mci_ovly_window_text"></span>Text des MCI- \_ OVLY- \_ Fensters \_
</dt> <dd>

Der **lpstrautext** -Member der durch *lpwindow* identifizierten Struktur enthält eine Adresse eines Puffers, der die für das Fenster verwendete Beschriftung enthält.

</dd> </dl>

Bei Video Überlagerungs Geräten zeigt der *lpwindow* -Parameter auf eine Struktur des [**MCI- \_ OVLY- \_ Fensters \_**](mci-ovly-window-parms.md) .

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

 

