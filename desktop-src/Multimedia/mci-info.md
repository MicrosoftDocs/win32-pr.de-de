---
title: MCI_INFO Befehl (MMSYSTEM. h)
description: Der MCI- \_ Info-Befehl ruft Zeichen folgen Informationen von einem Gerät ab.
ms.assetid: aed3fed3-87b9-4673-9171-4f57770d765c
keywords:
- MCI_INFO Befehl Windows-Multimedia
topic_type:
- apiref
api_name:
- MCI_INFO
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9f6ba5be1c2a4ce94b880a87a468c594bc5b676
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105710"
---
# <a name="mci_info-command"></a>MCI- \_ Info-Befehl

Der MCI- \_ Info-Befehl ruft Zeichen folgen Informationen von einem Gerät ab. Alle Geräte erkennen diesen Befehl. Informationen werden im **lpstraureturn** -Member der Struktur zurückgegeben, die von *lpInfo* identifiziert wird. Der **dwretsize** -Member gibt die Pufferlänge für die zurückgegebenen Daten an.

Um diesen Befehl zu senden, wenden Sie die [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion mit den folgenden Parametern an.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_INFO, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_INFO_PARMS) lpInfo
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

MCI \_ -Benachrichtigung, MCI \_ -Wartezeit oder, für Digital Video-und VCR-Geräte, MCI- \_ Test. Weitere Informationen zu diesen Flags finden Sie [unter Wait-, notify-und testflags](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpInfo"></span><span id="lpinfo"></span><span id="LPINFO"></span>*Puffer lpInfo*
</dt> <dd>

Zeiger auf eine [**MCI \_ - \_ Info**](mci-info-parms.md) -Parameter Struktur. (Geräte mit erweiterten Befehlssätzen können diese Struktur durch eine gerätespezifische Struktur ersetzen.)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.

## <a name="remarks"></a>Bemerkungen

Das folgende zusätzliche Standard-und Befehls spezifische Flag gilt für alle Geräte, die MCI-Informationen unterstützen \_ :

<dl> <dt>

<span id="MCI_INFO_PRODUCT"></span><span id="mci_info_product"></span>MCI- \_ Informations \_ Produkt
</dt> <dd>

Ruft eine Beschreibung der Hardware ab, die einem Gerät zugeordnet ist. Geräte sollten eine Beschreibung angeben, mit der sowohl der Treiber als auch die verwendete Hardware identifiziert werden.

</dd> </dl>

Die folgenden zusätzlichen Flags gelten für den **CDAudio** -Gerätetyp:

<dl> <dt>

<span id="MCI_INFO_MEDIA_IDENTITY"></span><span id="mci_info_media_identity"></span>MCI- \_ Info \_ Medien \_ Identität
</dt> <dd>

Erzeugt einen eindeutigen Bezeichner für die AudioCD, die derzeit in dem abgefragten Player geladen wird. Dieses Flag gibt eine Zeichenfolge mit 16 hexadezimalen Ziffern zurück.

</dd> <dt>

<span id="MCI_INFO_MEDIA_UPC"></span><span id="mci_info_media_upc"></span>MCI- \_ Info \_ Medien ( \_ UPC)
</dt> <dd>

Erzeugt den universellen Produkt Code (Universal Product Code, UPC), der auf einer AudioCD codiert ist. Der UPC ist eine Zeichenfolge mit Ziffern. Sie ist möglicherweise nicht für alle CDs verfügbar.

</dd> </dl>

Die folgenden zusätzlichen Flags gelten für den **Digitalvideo** -Gerätetyp:

<dl> <dt>

<span id="MCI_DGV_INFO_ITEM"></span><span id="mci_dgv_info_item"></span>MCI- \_ DGV- \_ Info \_ Element
</dt> <dd>

Eine-Konstante, die angibt, dass die gewünschten Informationen im **dwitem** -Member der durch *lpInfo* identifizierten-Struktur enthalten sind. Die folgenden Konstanten sind für Digital Video-Geräte definiert:

</dd> <dt>

<span id="MCI_DGV_INFO_AUDIO_ALG"></span><span id="mci_dgv_info_audio_alg"></span>MCI \_ DGV \_ Info \_ \_ audioalg
</dt> <dd>

Gibt den Namen für den aktuellen Audiokomprimierungs Algorithmus zurück.

</dd> <dt>

<span id="MCI_DGV_INFO_AUDIO_QUALITY"></span><span id="mci_dgv_info_audio_quality"></span>MCI \_ \_ -DGV \_ -Info- \_ Audioqualität
</dt> <dd>

Gibt den Namen für den aktuellen audioqualitätsdeskriptor zurück.

</dd> <dt>

<span id="MCI_DGV_INFO_STILL_ALG"></span><span id="mci_dgv_info_still_alg"></span>MCI- \_ DGV- \_ Informationen sind \_ immer noch \_ alg
</dt> <dd>

Gibt den Namen für den aktuellen immer noch Bild Komprimierungs Algorithmus zurück.

</dd> <dt>

<span id="MCI_DGV_INFO_STILL_QUALITY"></span><span id="mci_dgv_info_still_quality"></span>MCI- \_ DGV- \_ Informationen \_ weiterhin \_ Qualität
</dt> <dd>

Gibt den Namen für den aktuellen immer noch Bild Qualitäts Deskriptor zurück.

</dd> <dt>

<span id="MCI_DGV_INFO_USAGE"></span><span id="mci_dgv_info_usage"></span>MCI- \_ DGV- \_ Informations \_ Verwendung
</dt> <dd>

Gibt eine Zeichenfolge zurück, in der die Nutzungseinschränkungen beschrieben werden, die möglicherweise vom Besitzer der visuellen oder hörbaren Daten im Arbeitsbereich auferlegt werden.

</dd> <dt>

<span id="MCI_DGV_INFO_VIDEO_ALG"></span><span id="mci_dgv_info_video_alg"></span>MCI \_ DGV \_ Info \_ Video \_ alg
</dt> <dd>

Gibt den Namen für den aktuellen Video Komprimierungs Algorithmus zurück.

</dd> <dt>

<span id="MCI_DGV_INFO_VIDEO_QUALITY"></span><span id="mci_dgv_info_video_quality"></span>MCI- \_ DGV- \_ \_ Video \_ Qualität
</dt> <dd>

Gibt den Namen für den aktuellen Video Qualitäts Deskriptor zurück.

</dd> <dt>

<span id="MCI_INFO_VERSION"></span><span id="mci_info_version"></span>MCI- \_ Informations \_ Version
</dt> <dd>

Gibt die releaseebene des Gerätetreibers und der Hardware zurück. Gerätetreiber Entwickler müssen die Syntax der zurückgegebenen Zeichenfolge dokumentieren.

</dd> <dt>

<span id="MCI_DGV_INFO_TEXT"></span><span id="mci_dgv_info_text"></span>MCI- \_ DGV- \_ Info \_ Text
</dt> <dd>

Ruft die Beschriftung des Fensters ab.

</dd> <dt>

<span id="MCI_INFO_FILE"></span><span id="mci_info_file"></span>MCI \_ - \_ Infodatei
</dt> <dd>

Ruft den Pfad und den Dateinamen der letzten mit dem Befehl " [MCI \_ Öffnen](mci-open.md) " oder " [MCI \_ Laden](mci-load.md) " angegebenen Datei ab. Wenn keine Datei angegeben wurde, gibt das Gerät eine NULL-terminierte Zeichenfolge zurück. Dieses Flag wird nur von Geräten unterstützt, die " **true** " zurückgeben, um das MCI- \_ Flag "getdevcaps \_ verwendet Dateien" \_ des Befehls [MCI \_ getdevcaps](mci-getdevcaps.md) zu verwenden.

</dd> </dl>

Für Digital Video-Geräte verweist *lpInfo* auf eine [**MCI- \_ DGV \_ - \_ Informations**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_info_parmsa) Parameter Struktur.

Die folgenden zusätzlichen Flags gelten für den Typ des **Sequencer** -Geräts:

<dl> <dt>

<span id="MCI_INFO_COPYRIGHT"></span><span id="mci_info_copyright"></span>MCI- \_ Informationen \_ Copyright
</dt> <dd>

Ruft den Urheberrechts Hinweis der MIDI-Datei aus dem Copyright-Meta-Ereignis ab.

</dd> <dt>

<span id="MCI_INFO_FILE"></span><span id="mci_info_file"></span>MCI \_ - \_ Infodatei
</dt> <dd>

Ruft den Dateinamen der aktuellen Datei ab. Dieses Flag wird nur von Geräten unterstützt, die " **true** " zurückgeben, wenn Sie den [MCI \_ getdevcaps](mci-getdevcaps.md) -Befehl mit dem Flag "MCI \_ getdevcaps \_ verwendet Files" aufrufen \_ .

</dd> <dt>

<span id="MCI_INFO_NAME"></span><span id="mci_info_name"></span>MCI- \_ Informations \_ Name
</dt> <dd>

Ruft den Sequenznamen aus dem Meta-Ereignis für das Sequenz-/Track-Name ab.

</dd> </dl>

Das folgende zusätzliche Flag gilt für den **VCR** -Gerätetyp:

<dl> <dt>

<span id="MCI_VCR_INFO_VERSION"></span><span id="mci_vcr_info_version"></span>MCI \_ VCR- \_ Informations \_ Version
</dt> <dd>

Legt den **lpstraureturn** -Member der [**MCI- \_ Info- \_**](mci-info-parms.md) Parameter-Struktur auf die Versionsnummer fest. Legt außerdem den **dwretsize** -Member auf die Länge der Zeichenfolge fest, auf die verwiesen wird.

</dd> </dl>

Die folgenden zusätzlichen Flags gelten für den **Überlagerungs** Gerätetyp:

<dl> <dt>

<span id="MCI_INFO_FILE"></span><span id="mci_info_file"></span>MCI \_ - \_ Infodatei
</dt> <dd>

Ruft den Dateinamen der aktuellen Datei ab. Dieses Flag wird nur von Geräten unterstützt, die " **true** " zurückgeben, um das MCI- \_ Flag "getdevcaps \_ verwendet Dateien" \_ des Befehls [MCI \_ getdevcaps](mci-getdevcaps.md) zu verwenden.

</dd> <dt>

<span id="MCI_OVLY_INFO_TEXT"></span><span id="mci_ovly_info_text"></span>MCI- \_ OVLY- \_ Info \_ Text
</dt> <dd>

Ruft die Beschriftung des Fensters ab, das dem Video Überlagerungs Gerät zugeordnet ist.

</dd> </dl>

Die folgenden zusätzlichen Flags gelten für den **waveaudiogerätetyp** :

<dl> <dt>

<span id="MCI_INFO_FILE"></span><span id="mci_info_file"></span>MCI \_ - \_ Infodatei
</dt> <dd>

Ruft den Dateinamen der aktuellen Datei ab. Dieses Flag wird von Geräten unterstützt, die " **true** " zurückgeben, wenn Sie den [MCI \_ getdevcaps](mci-getdevcaps.md) -Befehl mit dem Flag "MCI \_ getdevcaps \_ verwendet Files" aufrufen \_ .

</dd> <dt>

<span id="MCI_WAVE_INPUT"></span><span id="mci_wave_input"></span>MCI- \_ Wave- \_ Eingabe
</dt> <dd>

Ruft den Produktnamen der aktuellen Eingabe ab.

</dd> <dt>

<span id="MCI_WAVE_OUTPUT"></span><span id="mci_wave_output"></span>MCI- \_ Wave- \_ Ausgabe
</dt> <dd>

Ruft den Produktnamen der aktuellen Ausgabe ab, und sein Wert ist gerätespezifisch.

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

 

