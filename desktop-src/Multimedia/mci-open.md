---
title: MCI_OPEN Befehl (MMSYSTEM. h)
description: Der Befehl MCI \_ Open Initialisiert ein Gerät oder eine Datei. Alle Geräte erkennen diesen Befehl.
ms.assetid: e2ee92b5-b10b-4408-950e-3002fe775b25
keywords:
- MCI_OPEN Befehl Windows-Multimedia
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
ms.openlocfilehash: 14d8b33e70a2e061b54260aeffc6e69432c469f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858630"
---
# <a name="mci_open-command"></a>MCI- \_ Befehl "Öffnen"

Der Befehl MCI \_ Open Initialisiert ein Gerät oder eine Datei. Alle Geräte erkennen diesen Befehl.

Um diesen Befehl zu senden, wenden Sie die [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion mit den folgenden Parametern an.


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

<span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*WDE viceid*
</dt> <dd>

Geräte Bezeichner des MCI-Geräts, das die Befehls Meldung empfangen soll.

</dd> <dt>

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*
</dt> <dd>

MCI- \_ Benachrichtigung oder MCI- \_ Wartezeit. Weitere Informationen zu diesen Flags finden Sie [unter Wait-, notify-und testflags](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpOpen"></span><span id="lpopen"></span><span id="LPOPEN"></span>*lpopen*
</dt> <dd>

Zeiger auf eine [**MCI- \_ Open- \_ Parser**](mci-open-parms.md) -Struktur. (Geräte mit erweiterten Befehlssätzen können diese Struktur durch eine gerätespezifische Struktur ersetzen.)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.

## <a name="remarks"></a>Bemerkungen

Das MCI \_ - \_ Flag für Open Type muss immer verwendet werden, wenn ein Gerät in der [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion angegeben wird. Wenn Sie ein Gerät öffnen, indem Sie eine gerätertyp Konstante angeben, müssen Sie \_ \_ \_ zusätzlich zum geöffneten MCI-Typ das MCI-Flag für das Open Type-ID-Flag angeben \_ \_ . Eine Liste der Gerätetyp Konstanten finden Sie unter [MCI-Gerätetypen](mci-device-types.md).

Wenn das MCI \_ - \_ Flag zum Öffnen von freistellbar beim ersten Öffnen eines Geräts oder einer Datei nicht angegeben wird, schlagen alle nachfolgenden MCI- \_ Befehle zum Öffnen des Geräts oder der Datei fehl. Wenn das Gerät oder die Datei bereits geöffnet ist und dieses Flag nicht angegeben ist, schlägt der Aufruf fehl, auch wenn der erste geöffnete Befehl, den MCI angegeben hat, \_ \_ share able geöffnet hat. Dateien, die für mciseq geöffnet wurden. DRV und MCIWave. DRV-Geräte sind nicht Sharable.

Der Fall wird im Gerätenamen ignoriert, es dürfen jedoch keine führenden oder nachfolgenden Leerzeichen vorhanden sein.

Wenn Sie die automatische Typauswahl (über die Einträge in der Registrierung) verwenden möchten, weisen Sie dem **lpstrelementname** -Member der von *lpopen* identifizierten Struktur den Dateinamen und die Dateierweiterung zu, legen Sie den **lpstrdevicetype** -Member auf **null** fest, und legen Sie das Flag für das MCI- \_ Open-Element fest \_ .

Die folgenden zusätzlichen Flags gelten für alle Geräte, die MCI geöffnet unterstützen \_ :

<dl> <dt>

<span id="MCI_OPEN_ALIAS"></span><span id="mci_open_alias"></span>MCI- \_ Open- \_ Alias
</dt> <dd>

Ein Alias ist im **lpstralias** -Member der durch *lpopen* identifizierten Struktur enthalten.

</dd> <dt>

<span id="MCI_OPEN_SHAREABLE"></span><span id="mci_open_shareable"></span>MCI \_ Open \_ share able
</dt> <dd>

Das Gerät oder die Datei muss als Sharable geöffnet werden.

</dd> <dt>

<span id="MCI_OPEN_TYPE"></span><span id="mci_open_type"></span>MCI- \_ Open- \_ Typ
</dt> <dd>

Ein Gerätetyp Name oder eine Konstante ist im **lpstrdevicetype** -Member der durch *lpopen* identifizierten Struktur enthalten.

</dd> <dt>

<span id="MCI_OPEN_TYPE_ID"></span><span id="mci_open_type_id"></span>MCI- \_ öffnende \_ Typ- \_ ID
</dt> <dd>

Das nieder wertige Wort des **lpstrdevicetype** -Members der von *lpopen* identifizierten Struktur enthält einen Standard-MCI-Gerätetyp Bezeichner, und das höchst wertige Wort enthält optional den Ordinalindex für das Gerät. Verwenden Sie dieses Flag mit dem MCI- \_ \_ Flag Open Type.

</dd> </dl>

Die folgenden zusätzlichen Flags gelten für Verbund Geräte:

<dl> <dt>

<span id="MCI_OPEN_ELEMENT"></span><span id="mci_open_element"></span>geöffnetes MCI- \_ \_ Element
</dt> <dd>

Ein Dateiname ist im **lpstrelementname** -Member der durch *lpopen* identifizierten Struktur enthalten.

</dd> <dt>

<span id="MCI_OPEN_ELEMENT_ID"></span><span id="mci_open_element_id"></span>MCI- \_ Open- \_ Element- \_ ID
</dt> <dd>

Der **lpstrelementname** -Member der Struktur, die von *lpopen* identifiziert wird, wird als **DWORD** -Wert interpretiert und hat eine interne Bedeutung für das Gerät. Verwenden Sie dieses Flag mit dem MCI- \_ Flag "Open \_ Element".

</dd> </dl>

Die folgenden zusätzlichen Flags werden mit dem **Digitalvideo** -Gerätetyp verwendet:

<dl> <dt>

<span id="MCI_DGV_OPEN_NOSTATIC"></span><span id="mci_dgv_open_nostatic"></span>MCI \_ DGV \_ Open \_ nostatic
</dt> <dd>

Das Gerät sollte die Anzahl der statischen (System) Farben in der Palette reduzieren. Dadurch erhöht sich die Anzahl der zum Rendern des Videodaten Stroms verfügbaren Farben. Dieses Flag gilt nur für Geräte, die eine Palette mit Windows gemeinsam verwenden.

</dd> <dt>

<span id="MCI_DGV_OPEN_PARENT"></span><span id="mci_dgv_open_parent"></span>übergeordnetes MCI- \_ DGV-Element \_ Öffnen \_
</dt> <dd>

Das übergeordnete Fenster Handle wird im **hwndParent** -Member der durch *lpopen* identifizierten Struktur angegeben.

</dd> <dt>

<span id="MCI_DGV_OPEN_WS"></span><span id="mci_dgv_open_ws"></span>MCI \_ DGV \_ Open \_ WS
</dt> <dd>

Im **dwstyle** -Member der-Struktur, die von *lpopen* identifiziert wird, wird ein Fenster Stil angegeben.

</dd> <dt>

<span id="MCI_DGV_OPEN_16BIT"></span><span id="mci_dgv_open_16bit"></span>MCI \_ DGV, \_ geöffnet, \_ 16 Bit
</dt> <dd>

Gibt eine Einstellung für die Unterstützung von 16-Bit-MCI-Geräten an.

</dd> <dt>

<span id="MCI_DGV_OPEN_32BIT"></span><span id="mci_dgv_open_32bit"></span>MCI \_ DGV, \_ geöffnet, \_ 32-Bit
</dt> <dd>

Gibt eine Einstellung für die 32-Bit-MCI-Geräte Unterstützung an.

</dd> </dl>

Für Digital Video-Geräte verweist der *lpopen* -Parameter auf eine [**MCI-DGV-Struktur mit \_ \_ geöffneten \_ para**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_open_parmsa) Metern.

Die folgenden zusätzlichen Flags werden mit dem **Überlagerungs** Gerätetyp verwendet:

<dl> <dt>

<span id="MCI_OVLY_OPEN_PARENT"></span><span id="mci_ovly_open_parent"></span>MCI \_ OVLY \_ über \_ geordnetes Element öffnen
</dt> <dd>

Das übergeordnete Fenster Handle wird im **hwndParent** -Member der durch *lpopen* identifizierten Struktur angegeben.

</dd> <dt>

<span id="MCI_OVLY_OPEN_WS"></span><span id="mci_ovly_open_ws"></span>MCI \_ OVLY- \_ Open- \_ WS
</dt> <dd>

Im **dwstyle** -Member der-Struktur, die von *lpopen* identifiziert wird, wird ein Fenster Stil angegeben. Der **dwstyle** -Wert gibt den Stil des Fensters an, den der Treiber erstellt und anzeigt, wenn die Anwendung keinen bereitstellt. Der style-Parameter nimmt eine ganze Zahl an, die den Fenster Stil definiert. Diese Konstanten sind identisch mit den Standardfenster Stilen (z. b. WS \_ Child, WS \_ overlappedwindow oder WS \_ Popup).

</dd> </dl>

Bei Video Überlagerungs Geräten zeigt der *lpopen* -Parameter auf eine [**MCI \_ OVLY- \_ Open \_**](mci-ovly-open-parms.md) -Parameterstruktur.

Das folgende zusätzliche Flag wird mit dem **waveaudiogerätetyp** verwendet:

<dl> <dt>

<span id="MCI_WAVE_OPEN_BUFFER"></span><span id="mci_wave_open_buffer"></span>MCI- \_ Wellen \_ Öffnungs \_ Puffer
</dt> <dd>

Im **dwbufferseconds** -Member der Struktur, die von *lpopen* identifiziert wird, wird eine Pufferlänge angegeben.

</dd> </dl>

Bei Waveform-Audiogeräten zeigt der *lpopen* -Parameter auf eine [**MCI \_ Wave \_ Open \_**](mci-wave-open-parms.md) -Parameter Struktur. Der MCIWave-Treiber erfordert ein asynchrones Waveform-Audiogerät.

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

 

