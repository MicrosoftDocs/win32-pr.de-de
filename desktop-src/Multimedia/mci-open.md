---
title: MCI_OPEN Befehl (Mmsystem.h)
description: Der MCI \_ OPEN-Befehl initialisiert ein Gerät oder eine Datei. Dieser Befehl wird von allen Geräten erkannt.
ms.assetid: e2ee92b5-b10b-4408-950e-3002fe775b25
keywords:
- MCI_OPEN Befehl Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a84c95df35ecd602c207daa716b62d90f6bdc79b0ede7f937d3a38e6d6a9373b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119689980"
---
# <a name="mci_open-command"></a>MCI \_ OPEN-Befehl

Der MCI \_ OPEN-Befehl initialisiert ein Gerät oder eine Datei. Dieser Befehl wird von allen Geräten erkannt.

Rufen Sie zum Senden dieses Befehls die [**mciSendCommand-Funktion**](/previous-versions//dd757160(v=vs.85)) mit den folgenden Parametern auf.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_OPEN, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_OPEN_PARMS) lpOpen
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

MCI \_ NOTIFY oder MCI \_ WAIT. Informationen zu diesen Flags finden Sie unter [Die Warte-, Benachrichtigungs- und Testflags.](the-wait-notify-and-test-flags.md)

</dd> <dt>

<span id="lpOpen"></span><span id="lpopen"></span><span id="LPOPEN"></span>*lpOpen*
</dt> <dd>

Zeiger auf eine [**MCI \_ OPEN \_ PARMS-Struktur.**](mci-open-parms.md) (Geräte mit erweiterten Befehlssätzen können diese Struktur durch eine gerätespezifische Struktur ersetzen.)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn der Fehler erfolgreich war, oder andernfalls ein Fehler.

## <a name="remarks"></a>Hinweise

Das MCI \_ OPEN \_ TYPE-Flag muss immer dann verwendet werden, wenn ein Gerät in der [**mciSendCommand-Funktion**](/previous-versions//dd757160(v=vs.85)) angegeben wird. Wenn Sie ein Gerät öffnen, indem Sie eine Gerätetypkonstante angeben, müssen Sie zusätzlich zu MCI OPEN TYPE das \_ \_ \_ ID-Flag MCI \_ OPEN TYPE \_ angeben. Eine Liste der Gerätetypkonstanten finden Sie unter [MCI-Gerätetypen.](mci-device-types.md)

Wenn das MCI \_ OPEN \_ SHAREABLE-Flag beim ersten Öffnen eines Geräts oder einer Datei nicht angegeben wird, schlagen alle nachfolgenden MCI \_ OPEN-Befehle für das Gerät oder die Datei fehl. Wenn das Gerät oder die Datei bereits geöffnet ist und dieses Flag nicht angegeben ist, schlägt der Aufruf fehl, auch wenn der erste geöffnete Befehl MCI OPEN SHAREABLE angegeben \_ \_ hat. Für MCISEQ geöffnete Dateien. DRV und MCIWAVE. DRV-Geräte sind nicht verfügbar.

Die Groß-/Schreibung wird im Gerätenamen ignoriert, aber es dürfen keine führenden oder nachgestellten Leerzeichen vorhanden sein.

Um die automatische Typauswahl (über die Einträge in der Registrierung) zu verwenden, weisen Sie den Dateinamen und die Dateierweiterung dem **lpstrElementName-Member** der durch *lpOpen identifizierten* Struktur zu, legen Sie den **lpstrDeviceType-Member** auf **NULL** fest, und legen Sie das MCI \_ OPEN \_ ELEMENT-Flag fest.

Die folgenden zusätzlichen Flags gelten für alle Geräte, die MCI \_ OPEN unterstützen:

<dl> <dt>

<span id="MCI_OPEN_ALIAS"></span><span id="mci_open_alias"></span>MCI \_ OPEN \_ ALIAS
</dt> <dd>

Ein Alias ist im **lpstrAlias-Member** der durch *lpOpen identifizierten* Struktur enthalten.

</dd> <dt>

<span id="MCI_OPEN_SHAREABLE"></span><span id="mci_open_shareable"></span>MCI \_ OPEN \_ SHAREABLE
</dt> <dd>

Das Gerät oder die Datei sollte als trennbar geöffnet werden.

</dd> <dt>

<span id="MCI_OPEN_TYPE"></span><span id="mci_open_type"></span>MCI \_ OPEN \_ TYPE
</dt> <dd>

Ein Gerätetypname oder eine Konstante ist im **lpstrDeviceType-Member** der durch *lpOpen identifizierten* Struktur enthalten.

</dd> <dt>

<span id="MCI_OPEN_TYPE_ID"></span><span id="mci_open_type_id"></span>MCI \_ OPEN \_ TYPE \_ ID
</dt> <dd>

Das Wort mit niedriger Reihenfolge des **lpstrDeviceType-Members** der durch *lpOpen identifizierten* Struktur enthält einen Standard-MCI-Gerätetypbezeichner, und das Wort in hoher Ordnung enthält optional den Ordnungsindex für das Gerät. Verwenden Sie dieses Flag mit dem MCI \_ OPEN \_ TYPE-Flag.

</dd> </dl>

Die folgenden zusätzlichen Flags gelten für Verbundgeräte:

<dl> <dt>

<span id="MCI_OPEN_ELEMENT"></span><span id="mci_open_element"></span>MCI \_ \_ OPEN-ELEMENT
</dt> <dd>

Ein Dateiname ist im **lpstrElementName-Member** der durch *lpOpen identifizierten* Struktur enthalten.

</dd> <dt>

<span id="MCI_OPEN_ELEMENT_ID"></span><span id="mci_open_element_id"></span>MCI \_ OPEN \_ ELEMENT \_ ID
</dt> <dd>

Der **lpstrElementName-Member** der von *lpOpen identifizierten* Struktur wird als **DWORD-Wert** interpretiert und hat eine interne Bedeutung für das Gerät. Verwenden Sie dieses Flag mit dem MCI \_ OPEN \_ ELEMENT-Flag.

</dd> </dl>

Die folgenden zusätzlichen Flags werden mit dem **Gerätetyp digitalvideo** verwendet:

<dl> <dt>

<span id="MCI_DGV_OPEN_NOSTATIC"></span><span id="mci_dgv_open_nostatic"></span>MCI \_ DGV \_ OPEN \_ NOSTATIC
</dt> <dd>

Das Gerät sollte die Anzahl statischer Farben (Systemfarben) in der Palette reduzieren. Dies erhöht die Anzahl der Farben, die zum Rendern des Videostreams verfügbar sind. Dieses Flag gilt nur für Geräte, die eine Palette mit Windows gemeinsam nutzen.

</dd> <dt>

<span id="MCI_DGV_OPEN_PARENT"></span><span id="mci_dgv_open_parent"></span>MCI \_ DGV \_ OPEN \_ PARENT
</dt> <dd>

Das übergeordnete Fensterhandle wird im **hWndParent-Member** der durch *lpOpen identifizierten* Struktur angegeben.

</dd> <dt>

<span id="MCI_DGV_OPEN_WS"></span><span id="mci_dgv_open_ws"></span>MCI \_ DGV \_ OPEN \_ WS
</dt> <dd>

Ein Fensterstil wird im **dwStyle-Member** der durch *lpOpen identifizierten* Struktur angegeben.

</dd> <dt>

<span id="MCI_DGV_OPEN_16BIT"></span><span id="mci_dgv_open_16bit"></span>MCI \_ DGV \_ OPEN \_ 16 BIT
</dt> <dd>

Gibt eine Einstellung für die 16-Bit-MCI-Geräteunterstützung an.

</dd> <dt>

<span id="MCI_DGV_OPEN_32BIT"></span><span id="mci_dgv_open_32bit"></span>MCI \_ DGV \_ OPEN \_ 32 BIT
</dt> <dd>

Gibt eine Einstellung für die Unterstützung von 32-Bit-MCI-Geräten an.

</dd> </dl>

Bei Geräten mit digitalem Video zeigt der *lpOpen-Parameter* auf eine [**MCI \_ DGV \_ OPEN \_ PARMS-Struktur.**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_open_parmsa)

Die folgenden zusätzlichen Flags werden mit dem **Überlagerungsgerätetyp** verwendet:

<dl> <dt>

<span id="MCI_OVLY_OPEN_PARENT"></span><span id="mci_ovly_open_parent"></span>MCI \_ OVLY \_ OPEN \_ PARENT
</dt> <dd>

Das übergeordnete Fensterhandle wird im **hWndParent-Member** der durch *lpOpen identifizierten* Struktur angegeben.

</dd> <dt>

<span id="MCI_OVLY_OPEN_WS"></span><span id="mci_ovly_open_ws"></span>MCI \_ OVLY \_ OPEN \_ WS
</dt> <dd>

Ein Fensterstil wird im **dwStyle-Member** der durch *lpOpen identifizierten* Struktur angegeben. Der **dwStyle-Wert** gibt den Stil des Fensters an, das der Treiber erstellt und anzeigt, wenn die Anwendung keines bereitstellt. Der style-Parameter akzeptiert eine ganze Zahl, die den Fensterstil definiert. Diese Konstanten sind identisch mit den Standardfensterstilen (z. B. WS \_ CHILD, WS \_ OVERLAPPEDWINDOW oder WS \_ POPUP).

</dd> </dl>

Bei Videoüberlagerungsgeräten zeigt der *lpOpen-Parameter* auf eine [**MCI \_ OVLY \_ OPEN \_ PARMS-Struktur.**](mci-ovly-open-parms.md)

Das folgende zusätzliche Flag wird mit dem **Gerätetyp waveaudio** verwendet:

<dl> <dt>

<span id="MCI_WAVE_OPEN_BUFFER"></span><span id="mci_wave_open_buffer"></span>MCI \_ WAVE \_ OPEN \_ BUFFER
</dt> <dd>

Eine Pufferlänge wird im **dwBufferSeconds-Member** der -Struktur angegeben, die durch *lpOpen* identifiziert wird.

</dd> </dl>

Für Waveform-Audiogeräte zeigt der *lpOpen-Parameter* auf eine [**MCI \_ WAVE OPEN \_ \_ PARMS-Struktur.**](mci-wave-open-parms.md) Der MCIWAVE-Treiber erfordert ein asynchrones Waveform-Audiogerät.

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

 

