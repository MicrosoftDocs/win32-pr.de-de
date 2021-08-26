---
title: MCI_INFO Befehl (Mmsystem.h)
description: Der \_ MCI INFO-Befehl ruft Zeichenfolgeninformationen von einem Gerät ab.
ms.assetid: aed3fed3-87b9-4673-9171-4f57770d765c
keywords:
- MCI_INFO Befehl Windows Multimedia
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
ms.openlocfilehash: 18d53acbdfeb0c13b4b9e201d1bea23008dfbaa83221007152181fe685d09957
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039199"
---
# <a name="mci_info-command"></a>MCI \_ INFO-Befehl

Der \_ MCI INFO-Befehl ruft Zeichenfolgeninformationen von einem Gerät ab. Dieser Befehl wird von allen Geräten erkannt. Informationen werden im **lpstrReturn-Member** der durch *lpInfo* identifizierten Struktur zurückgegeben. Der **dwRetSize-Member** gibt die Pufferlänge für die zurückgegebenen Daten an.

Rufen Sie zum Senden dieses Befehls die [**mciSendCommand-Funktion**](/previous-versions//dd757160(v=vs.85)) mit den folgenden Parametern auf.


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

<span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*
</dt> <dd>

Gerätebezeichner des MCI-Geräts, das die Befehlsmeldung empfangen soll.

</dd> <dt>

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*Dwflags*
</dt> <dd>

MCI \_ NOTIFY, MCI \_ WAIT oder, für Digital Video- und VCR-Geräte, MCI \_ TEST. Informationen zu diesen Flags finden Sie unter [Die Warte-, Benachrichtigungs- und Testflags.](the-wait-notify-and-test-flags.md)

</dd> <dt>

<span id="lpInfo"></span><span id="lpinfo"></span><span id="LPINFO"></span>*lpInfo*
</dt> <dd>

Zeiger auf eine [**MCI \_ INFO \_ PARMS-Struktur.**](mci-info-parms.md) (Geräte mit erweiterten Befehlssätzen können diese Struktur durch eine gerätespezifische Struktur ersetzen.)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn der Fehler erfolgreich war, oder andernfalls ein Fehler.

## <a name="remarks"></a>Hinweise

Das folgende zusätzliche Standard- und Befehlsflag gilt für alle Geräte, die MCI \_ INFO unterstützen:

<dl> <dt>

<span id="MCI_INFO_PRODUCT"></span><span id="mci_info_product"></span>MCI \_ INFO \_ PRODUCT
</dt> <dd>

Ruft eine Beschreibung der Hardware ab, die einem Gerät zugeordnet ist. Geräte sollten eine Beschreibung bereitstellen, die sowohl den Treiber als auch die verwendete Hardware identifiziert.

</dd> </dl>

Die folgenden zusätzlichen Flags gelten für den **Cdaudio-Gerätetyp:**

<dl> <dt>

<span id="MCI_INFO_MEDIA_IDENTITY"></span><span id="mci_info_media_identity"></span>MCI \_ INFO \_ MEDIA \_ IDENTITY
</dt> <dd>

Erzeugt einen eindeutigen Bezeichner für die Audio-CD, die derzeit in den abgefragten Player geladen ist. Dieses Flag gibt eine Zeichenfolge mit 16 Hexadezimalziffern zurück.

</dd> <dt>

<span id="MCI_INFO_MEDIA_UPC"></span><span id="mci_info_media_upc"></span>MCI \_ INFO \_ MEDIA \_ UPC
</dt> <dd>

Erzeugt den Universal Product Code (UPC), der auf einer Audio-CD codiert ist. Der UPC ist eine Zeichenfolge von Ziffern. Sie ist möglicherweise nicht für alle CDs verfügbar.

</dd> </dl>

Die folgenden zusätzlichen Flags gelten für den **Gerätetyp digitalvideo:**

<dl> <dt>

<span id="MCI_DGV_INFO_ITEM"></span><span id="mci_dgv_info_item"></span>MCI \_ DGV \_ INFO \_ ITEM
</dt> <dd>

Eine Konstante, die die gewünschten Informationen angibt, ist im **dwItem-Member** der durch *lpInfo* identifizierten Struktur enthalten. Die folgenden Konstanten werden für Digitalvideogeräte definiert:

</dd> <dt>

<span id="MCI_DGV_INFO_AUDIO_ALG"></span><span id="mci_dgv_info_audio_alg"></span>MCI \_ DGV \_ INFO \_ AUDIO \_ ALG
</dt> <dd>

Gibt den Namen für den aktuellen Audiokomprimierungsalgorithmus zurück.

</dd> <dt>

<span id="MCI_DGV_INFO_AUDIO_QUALITY"></span><span id="mci_dgv_info_audio_quality"></span>MCI \_ DGV \_ INFO \_ AUDIO \_ QUALITY
</dt> <dd>

Gibt den Namen für den aktuellen Audioqualitätsdeskriptor zurück.

</dd> <dt>

<span id="MCI_DGV_INFO_STILL_ALG"></span><span id="mci_dgv_info_still_alg"></span>MCI \_ DGV \_ INFO \_ STILL \_ ALG
</dt> <dd>

Gibt den Namen für den aktuellen Algorithmus für die Komprimierung von Standbildern zurück.

</dd> <dt>

<span id="MCI_DGV_INFO_STILL_QUALITY"></span><span id="mci_dgv_info_still_quality"></span>MCI \_ DGV \_ INFO \_ STILL \_ QUALITY
</dt> <dd>

Gibt den Namen für den aktuellen Imagequalitätsdeskriptor zurück.

</dd> <dt>

<span id="MCI_DGV_INFO_USAGE"></span><span id="mci_dgv_info_usage"></span>VERWENDUNG \_ VON MCI-DGV-INFORMATIONEN \_ \_
</dt> <dd>

Gibt eine Zeichenfolge zurück, die Nutzungseinschränkungen beschreibt, die vom Besitzer der visuellen oder akustischen Daten im Arbeitsbereich erzwungen werden können.

</dd> <dt>

<span id="MCI_DGV_INFO_VIDEO_ALG"></span><span id="mci_dgv_info_video_alg"></span>MCI \_ DGV \_ INFO \_ VIDEO \_ ALG
</dt> <dd>

Gibt den Namen für den aktuellen Videokomprimierungsalgorithmus zurück.

</dd> <dt>

<span id="MCI_DGV_INFO_VIDEO_QUALITY"></span><span id="mci_dgv_info_video_quality"></span>MCI \_ DGV \_ INFO \_ VIDEO \_ QUALITY
</dt> <dd>

Gibt den Namen für den aktuellen Videoqualitätsdeskriptor zurück.

</dd> <dt>

<span id="MCI_INFO_VERSION"></span><span id="mci_info_version"></span>MCI \_ INFO \_ VERSION
</dt> <dd>

Gibt die Releaseebene des Gerätetreibers und der Hardware zurück. Gerätetreiberentwickler müssen die Syntax der zurückgegebenen Zeichenfolge dokumentieren.

</dd> <dt>

<span id="MCI_DGV_INFO_TEXT"></span><span id="mci_dgv_info_text"></span>MCI \_ DGV \_ INFO \_ TEXT
</dt> <dd>

Ruft die Fensterbeschriftung ab.

</dd> <dt>

<span id="MCI_INFO_FILE"></span><span id="mci_info_file"></span>\_MCI-INFODATEI \_
</dt> <dd>

Ruft den Pfad und den Dateinamen der letzten Datei ab, die mit dem [MCI \_ OPEN-](mci-open.md) oder [MCI \_ LOAD-Befehl](mci-load.md) angegeben wurde. Wenn keine Datei angegeben wurde, gibt das Gerät eine auf NULL endende Zeichenfolge zurück. Dieses Flag wird nur von Geräten unterstützt, die **TRUE** an das MCI \_ GETDEVCAPS \_ USES \_ FILES-Flag des [MCI \_ GETDEVCAPS-Befehls](mci-getdevcaps.md) zurückgeben.

</dd> </dl>

Für Digitalvideogeräte verweist *lpInfo* auf eine [**MCI \_ DGV \_ INFO \_ PARMS-Struktur.**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_info_parmsa)

Die folgenden zusätzlichen Flags gelten für den **Sequencergerätetyp:**

<dl> <dt>

<span id="MCI_INFO_COPYRIGHT"></span><span id="mci_info_copyright"></span>MCI \_ INFO \_ COPYRIGHT
</dt> <dd>

Ruft den COPYRIGHT-Hinweis für die DATEI COPYRIGHT aus dem Copyrightmetaereignis ab.

</dd> <dt>

<span id="MCI_INFO_FILE"></span><span id="mci_info_file"></span>\_MCI-INFODATEI \_
</dt> <dd>

Ruft den Dateinamen der aktuellen Datei ab. Dieses Flag wird nur von Geräten unterstützt, die **TRUE** zurückgeben, wenn Sie den [MCI \_ GETDEVCAPS-Befehl](mci-getdevcaps.md) mit dem \_ MCI GETDEVCAPS \_ USES \_ FILES-Flag aufrufen.

</dd> <dt>

<span id="MCI_INFO_NAME"></span><span id="mci_info_name"></span>\_MCI-INFONAME \_
</dt> <dd>

Ruft den Sequenznamen aus dem Sequenz-/Nachverfolgungsnamen-Metaereignis ab.

</dd> </dl>

Das folgende zusätzliche Flag  gilt für den Vcr-Gerätetyp:

<dl> <dt>

<span id="MCI_VCR_INFO_VERSION"></span><span id="mci_vcr_info_version"></span>MCI \_ VCR \_ INFO \_ VERSION
</dt> <dd>

Legt **den lpstrReturn-Member** der [**MCI INFO \_ \_ PARMS-Struktur**](mci-info-parms.md) so fest, dass er auf die Versionsnummer verweist. Legt außerdem das **dwRetSize-Element** auf die Länge der Zeichenfolge fest, auf die verwiesen wird.

</dd> </dl>

Die folgenden zusätzlichen Flags gelten für den **Überlagerungsgerätetyp:**

<dl> <dt>

<span id="MCI_INFO_FILE"></span><span id="mci_info_file"></span>\_MCI-INFODATEI \_
</dt> <dd>

Ruft den Dateinamen der aktuellen Datei ab. Dieses Flag wird nur von Geräten unterstützt, die **TRUE** an das MCI \_ GETDEVCAPS \_ USES \_ FILES-Flag des [MCI \_ GETDEVCAPS-Befehls](mci-getdevcaps.md) zurückgeben.

</dd> <dt>

<span id="MCI_OVLY_INFO_TEXT"></span><span id="mci_ovly_info_text"></span>MCI \_ OVLY \_ INFO \_ TEXT
</dt> <dd>

Ruft die Beschriftung des Fensters ab, das dem Videoüberlagerungsgerät zugeordnet ist.

</dd> </dl>

Die folgenden zusätzlichen Flags gelten für den **Waveaudio-Gerätetyp:**

<dl> <dt>

<span id="MCI_INFO_FILE"></span><span id="mci_info_file"></span>\_MCI-INFODATEI \_
</dt> <dd>

Ruft den Dateinamen der aktuellen Datei ab. Dieses Flag wird von Geräten unterstützt, die **TRUE** zurückgeben, wenn Sie den [MCI \_ GETDEVCAPS-Befehl](mci-getdevcaps.md) mit dem \_ MCI GETDEVCAPS \_ USES \_ FILES-Flag aufrufen.

</dd> <dt>

<span id="MCI_WAVE_INPUT"></span><span id="mci_wave_input"></span>MCI \_ WAVE \_ INPUT
</dt> <dd>

Ruft den Produktnamen der aktuellen Eingabe ab.

</dd> <dt>

<span id="MCI_WAVE_OUTPUT"></span><span id="mci_wave_output"></span>MCI \_ \_ WAVE-AUSGABE
</dt> <dd>

Ruft den Produktnamen der aktuellen Ausgabe ab, und sein Wert ist gerätespezifisch.

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

 

