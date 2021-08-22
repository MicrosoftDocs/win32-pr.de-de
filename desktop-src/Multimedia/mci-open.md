---
title: MCI_OPEN Befehl (Mmsystem.h)
description: Der MCI \_ OPEN-Befehl initialisiert ein Gerät oder eine Datei. Dieser Befehl wird von allen Geräten erkannt.
ms.assetid: e2ee92b5-b10b-4408-950e-3002fe775b25
keywords:
- MCI_OPEN-Befehl Windows Multimedia
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

Um diesen Befehl zu senden, rufen Sie die [**mciSendCommand-Funktion**](/previous-versions//dd757160(v=vs.85)) mit den folgenden Parametern auf.


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

Gerätebezeichner des MCI-Geräts, das die Befehlsnachricht empfangen soll.

</dd> <dt>

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*Dwflags*
</dt> <dd>

MCI \_ NOTIFY oder MCI \_ WAIT. Informationen zu diesen Flags finden Sie unter [Die Warte-, Benachrichtigungs- und Testflags](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpOpen"></span><span id="lpopen"></span><span id="LPOPEN"></span>*lpOpen*
</dt> <dd>

Zeiger auf eine [**MCI \_ OPEN \_ PARMS-Struktur.**](mci-open-parms.md) (Geräte mit erweiterten Befehlssätzen ersetzen diese Struktur möglicherweise durch eine gerätespezifische Struktur.)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls ein Fehler.

## <a name="remarks"></a>Hinweise

Das MCI OPEN TYPE-Flag muss immer dann verwendet werden, wenn ein Gerät \_ \_ in der [**mciSendCommand-Funktion angegeben**](/previous-versions//dd757160(v=vs.85)) wird. Wenn Sie ein Gerät öffnen, indem Sie eine Konstante vom Typ device angeben, müssen Sie zusätzlich zu MCI OPEN TYPE das MCI \_ OPEN \_ TYPE ID-Flag \_ \_ \_ angeben. Eine Liste der Gerätetypkonst konstanten finden Sie unter [MCI-Gerätetypen.](mci-device-types.md)

Wenn das MCI OPEN SHAREABLE-Flag beim ersten Öffnen eines Geräts oder einer Datei nicht angegeben wird, können alle nachfolgenden MCI OPEN-Befehle für das Gerät oder die \_ \_ Datei nicht ausgeführt \_ werden. Wenn das Gerät oder die Datei bereits geöffnet ist und dieses Flag nicht angegeben ist, kann der Aufruf auch dann nicht ausgeführt werden, wenn im ersten geöffneten Befehl MCI \_ OPEN \_ SHAREABLE angegeben wurde. Für MCISEQ geöffnete Dateien. DRV und MCIWAVE. DRV-Geräte sind nicht verfügbar.

Case wird im Gerätenamen ignoriert, es dürfen jedoch keine führenden oder nachstellenden Leerzeichen angezeigt werden.

Um die automatische Typauswahl (über die Einträge in der Registrierung) zu verwenden, weisen Sie den Dateinamen und die Dateierweiterung dem **lpstrElementName-Element** der durch *lpOpen* identifizierten Struktur zu, legen Sie den **lpstrDeviceType-Member** auf **NULL** fest, und legen Sie das MCI \_ OPEN \_ ELEMENT-Flag fest.

Die folgenden zusätzlichen Flags gelten für alle Geräte, die MCI \_ OPEN unterstützen:

<dl> <dt>

<span id="MCI_OPEN_ALIAS"></span><span id="mci_open_alias"></span>MCI \_ OPEN \_ ALIAS
</dt> <dd>

Ein Alias ist im **lpstrAlias-Member der** -Struktur enthalten, die durch *lpOpen identifiziert wird.*

</dd> <dt>

<span id="MCI_OPEN_SHAREABLE"></span><span id="mci_open_shareable"></span>MCI \_ OPEN \_ SHAREABLE
</dt> <dd>

Das Gerät oder die Datei sollte als sharable geöffnet werden.

</dd> <dt>

<span id="MCI_OPEN_TYPE"></span><span id="mci_open_type"></span>MCI \_ OPEN \_ TYPE
</dt> <dd>

Ein Gerätetypname oder eine Konstante ist im **lpstrDeviceType-Member** der struktur enthalten, die durch *lpOpen identifiziert wird.*

</dd> <dt>

<span id="MCI_OPEN_TYPE_ID"></span><span id="mci_open_type_id"></span>MCI \_ OPEN \_ TYPE \_ ID
</dt> <dd>

Das niedrige Wort des **lpstrDeviceType-Members** der durch *lpOpen* identifizierten Struktur enthält einen MCI-Standardgerätetypbezeichner, und das obere Wort enthält optional den Ordinalindex für das Gerät. Verwenden Sie dieses Flag mit dem MCI \_ OPEN \_ TYPE-Flag.

</dd> </dl>

Die folgenden zusätzlichen Flags gelten für Verbundgeräte:

<dl> <dt>

<span id="MCI_OPEN_ELEMENT"></span><span id="mci_open_element"></span>MCI \_ \_ OPEN-ELEMENT
</dt> <dd>

Ein Dateiname ist im **lpstrElementName-Element der** -Struktur enthalten, die durch *lpOpen identifiziert wird.*

</dd> <dt>

<span id="MCI_OPEN_ELEMENT_ID"></span><span id="mci_open_element_id"></span>MCI \_ OPEN \_ ELEMENT \_ ID
</dt> <dd>

Der **lpstrElementName-Member** der durch *lpOpen identifizierten* Struktur wird als **DWORD-Wert** interpretiert und hat eine interne Bedeutung für das Gerät. Verwenden Sie dieses Flag mit dem MCI \_ OPEN \_ ELEMENT-Flag.

</dd> </dl>

Die folgenden zusätzlichen Flags werden mit dem **Gerätetyp digitalvideo** verwendet:

<dl> <dt>

<span id="MCI_DGV_OPEN_NOSTATIC"></span><span id="mci_dgv_open_nostatic"></span>MCI \_ DGV \_ OPEN \_ NOSTATIC
</dt> <dd>

Das Gerät sollte die Anzahl der statischen (System-)Farben in der Palette reduzieren. Dadurch wird die Anzahl der Farben erhöht, die zum Rendern des Videostreams verfügbar sind. Dieses Flag gilt nur für Geräte, die eine Palette mit Windows.

</dd> <dt>

<span id="MCI_DGV_OPEN_PARENT"></span><span id="mci_dgv_open_parent"></span>MCI \_ DGV \_ OPEN \_ PARENT
</dt> <dd>

Das handle des übergeordneten Fensters wird im **hWndParent-Element** der -Struktur angegeben, die durch *lpOpen identifiziert wird.*

</dd> <dt>

<span id="MCI_DGV_OPEN_WS"></span><span id="mci_dgv_open_ws"></span>MCI \_ DGV \_ OPEN \_ WS
</dt> <dd>

Ein Fensterstil wird im **dwStyle-Member** der -Struktur angegeben, die durch *lpOpen identifiziert wird.*

</dd> <dt>

<span id="MCI_DGV_OPEN_16BIT"></span><span id="mci_dgv_open_16bit"></span>MCI \_ DGV \_ OPEN \_ 16BIT
</dt> <dd>

Gibt eine Einstellung für die Unterstützung von 16-Bit-MCI-Geräten an.

</dd> <dt>

<span id="MCI_DGV_OPEN_32BIT"></span><span id="mci_dgv_open_32bit"></span>MCI \_ DGV \_ OPEN \_ 32BIT
</dt> <dd>

Gibt eine Einstellung für die Unterstützung von 32-Bit-MCI-Geräten an.

</dd> </dl>

Bei Digitalvideogeräten verweist *der lpOpen-Parameter* auf eine [**MCI \_ DGV OPEN \_ \_ PARMS-Struktur.**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_open_parmsa)

Die folgenden zusätzlichen Flags werden mit dem **Überlagerungsgerätetyp** verwendet:

<dl> <dt>

<span id="MCI_OVLY_OPEN_PARENT"></span><span id="mci_ovly_open_parent"></span>MCI \_ OVLY \_ OPEN \_ PARENT
</dt> <dd>

Das handle des übergeordneten Fensters wird im **hWndParent-Element** der -Struktur angegeben, die durch *lpOpen identifiziert wird.*

</dd> <dt>

<span id="MCI_OVLY_OPEN_WS"></span><span id="mci_ovly_open_ws"></span>MCI \_ OVLY \_ OPEN \_ WS
</dt> <dd>

Ein Fensterstil wird im **dwStyle-Member** der -Struktur angegeben, die durch *lpOpen identifiziert wird.* Der **dwStyle-Wert** gibt den Stil des Fensters an, das der Treiber erstellt und angibt, wenn die Anwendung keines angibt. Der style-Parameter akzeptiert eine ganze Zahl, die den Fensterstil definiert. Diese Konstanten sind identisch mit den Standardfensterstilen (z. B. WS \_ CHILD, WS \_ OVERLAPPEDWINDOW oder WS \_ POPUP).

</dd> </dl>

Bei Videoüberlagerungsgeräten verweist *der lpOpen-Parameter* auf eine [**MCI \_ OVLY \_ OPEN \_ PARMS-Struktur.**](mci-ovly-open-parms.md)

Das folgende zusätzliche Flag wird mit dem **Waveaudio-Gerätetyp** verwendet:

<dl> <dt>

<span id="MCI_WAVE_OPEN_BUFFER"></span><span id="mci_wave_open_buffer"></span>MCI \_ WAVE \_ OPEN \_ BUFFER
</dt> <dd>

Eine Pufferlänge wird im **dwBufferSeconds-Member** der -Struktur angegeben, die durch *lpOpen identifiziert wird.*

</dd> </dl>

Bei Waveform-Audiogeräten verweist *der lpOpen-Parameter* auf eine [**MCI \_ WAVE OPEN \_ \_ PARMS-Struktur.**](mci-wave-open-parms.md) Der MCIWAVE-Treiber erfordert ein asynchrones Waveform-Audio-Gerät.

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

 

