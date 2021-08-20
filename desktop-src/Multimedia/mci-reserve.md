---
title: MCI_RESERVE Befehl (Mmsystem.h)
description: Der MCI \_ RESERVE-Befehl ordnet dem Arbeitsbereich der Gerätetreiberinstanz zusammenhängenden Speicherplatz für die Verwendung mit nachfolgender Aufzeichnung zu. Digitalvideogeräte erkennen diesen Befehl.
ms.assetid: 01f0a377-0179-4b05-a642-af152a7a12ae
keywords:
- MCI_RESERVE Befehl Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_RESERVE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f21570d37fba9bc0c9595715715a9291aedd30650081edfa5d50f7264cf16c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117803461"
---
# <a name="mci_reserve-command"></a>MCI \_ RESERVE-Befehl

Der MCI \_ RESERVE-Befehl ordnet dem Arbeitsbereich der Gerätetreiberinstanz zusammenhängenden Speicherplatz für die Verwendung mit nachfolgender Aufzeichnung zu. Digitalvideogeräte erkennen diesen Befehl.

Rufen Sie zum Senden dieses Befehls die [**mciSendCommand-Funktion**](/previous-versions//dd757160(v=vs.85)) mit den folgenden Parametern auf.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_RESERVE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_RESERVE_PARMS) lpReserve
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

MCI \_ NOTIFY, MCI \_ WAIT oder MCI \_ TEST. Informationen zu diesen Flags finden Sie unter [Die Warte-, Benachrichtigungs- und Testflags.](the-wait-notify-and-test-flags.md)

</dd> <dt>

<span id="lpReserve"></span><span id="lpreserve"></span><span id="LPRESERVE"></span>*lpReserve*
</dt> <dd>

Zeiger auf eine [**MCI \_ DGV \_ RESERVE \_ PARMS-Struktur.**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_reserve_parmsa)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn der Fehler erfolgreich war, oder andernfalls ein Fehler.

## <a name="remarks"></a>Hinweise

Wenn der Arbeitsbereich nicht gespeicherte Daten enthält, geht er verloren. Wenn vor der Aufzeichnung kein Speicherplatz reserviert wird, führt der [MCI \_ RECORD-Befehl](mci-record.md) eine implizite Reserve mit gerätespezifischen Standardparametern aus. Bei einigen Implementierungen ist die Reservierung nicht erforderlich und wird möglicherweise vom Gerätetreiber ignoriert. Durch das explizite Reservieren von Speicherplatz können Sie besser steuern, wann die Verzögerung für die Datenträgerzuordnung auftritt, wie viel Speicherplatz belegt wird und wo der Speicherplatz zugeordnet wird. Die Menge und der Speicherort des bereits für diese Geräteinstanz reservierten Speicherplatzes können durch erneute Ausgabe von MCI RESERVE geändert \_ werden. Der zugeordnete und noch nicht belegte Speicherplatz wird erst freigegeben, wenn aufgezeichnete Daten gespeichert oder die Gerätetreiberinstanz geschlossen wurde.

Wenn video mit dem MCI \_ OFF-Flag des [MCI \_ SETVIDEO-Befehls](mci-setvideo.md) deaktiviert wird, enthält der reservierte Speicherplatz kein Video. Wenn audio mit dem MCI \_ OFF-Flag des [MCI \_ SETAUDIO-Befehls](mci-setaudio.md) deaktiviert wird, enthält der reservierte Speicherplatz keine Audiodaten. Wenn sowohl Audio als auch Video deaktiviert sind oder die angeforderte Größe 0 (null) ist, wird kein Speicherplatz reserviert, und die Zuordnung des vorhandenen reservierten Speicherplatzes wird freigegeben.

Die folgenden zusätzlichen Flags gelten für Digitalvideogeräte:

<dl> <dt>

<span id="MCI_DGV_RESERVE_IN"></span><span id="mci_dgv_reserve_in"></span>MCI \_ DGV \_ RESERVE \_ IN
</dt> <dd>

Der **lpstrPath-Member** der von *lpReserve* identifizierten Struktur enthält eine Adresse eines Puffers, der den Speicherort einer temporären Datei enthält. Der Puffer enthält nur das Laufwerk und den Verzeichnispfad der Datei, die zum Speichern aufgezeichneter Daten verwendet wird. Der Dateiname wird vom Gerätetreiber angegeben. Diese temporäre Datei wird gelöscht, wenn die Geräteinstanz geschlossen wird, es sei denn, sie wird explizit gespeichert. Wenn dieses Flag ausgelassen wird, gibt der Gerätetreiber an, wo Speicherplatz zugewiesen wird.

</dd> <dt>

<span id="MCI_DGV_RESERVE_SIZE"></span><span id="mci_dgv_reserve_size"></span>MCI \_ DGV \_ RESERVE \_ SIZE
</dt> <dd>

Der **dwSize-Member** der von *lpReserve* identifizierten Struktur gibt den ungefähren Speicherplatz an, der im Arbeitsbereich für die Aufzeichnung reserviert werden soll. Der Wert wird im aktuellen Zeitformat angegeben. Der Speicherplatz auf dem Datenträger wird ab dem angeforderten Zeitpunkt geschätzt, ab dem Dateiformat, Video- und Audioalgorithmus sowie Qualitätswerte wirksam sind. Wenn dieses Flag ausgelassen wird, verwendet der Gerätetreiber möglicherweise einen von ihm definierten Standardwert.

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

 

