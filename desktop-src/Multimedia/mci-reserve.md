---
title: MCI_RESERVE Befehl (MMSYSTEM. h)
description: Der Befehl MCI \_ Reserve ordnet dem Arbeitsbereich der Gerätetreiber Instanz zusammenhängenden Speicherplatz für die Verwendung bei der nachfolgenden Aufzeichnung zu. Dieser Befehl wird von Digital-Video-Geräten erkannt.
ms.assetid: 01f0a377-0179-4b05-a642-af152a7a12ae
keywords:
- MCI_RESERVE Befehl Windows-Multimedia
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
ms.openlocfilehash: b89eb457b63012aa9ee5624efef95945258d42c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956934"
---
# <a name="mci_reserve-command"></a>MCI- \_ Reserve Befehl

Der Befehl MCI \_ Reserve ordnet dem Arbeitsbereich der Gerätetreiber Instanz zusammenhängenden Speicherplatz für die Verwendung bei der nachfolgenden Aufzeichnung zu. Dieser Befehl wird von Digital-Video-Geräten erkannt.

Um diesen Befehl zu senden, wenden Sie die [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion mit den folgenden Parametern an.


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

<span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*WDE viceid*
</dt> <dd>

Geräte Bezeichner des MCI-Geräts, das die Befehls Meldung empfangen soll.

</dd> <dt>

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*
</dt> <dd>

MCI- \_ Benachrichtigung, MCI- \_ Wartezeit oder MCI- \_ Test. Weitere Informationen zu diesen Flags finden Sie [unter Wait-, notify-und testflags](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpReserve"></span><span id="lpreserve"></span><span id="LPRESERVE"></span>*lpreserve*
</dt> <dd>

Zeiger auf eine [**MCI- \_ DGV- \_ Reserve- \_ Parametern**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_reserve_parmsa) -Struktur.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.

## <a name="remarks"></a>Bemerkungen

Wenn der Arbeitsbereich nicht gespeicherte Daten enthält, gehen diese Daten verloren. Wenn der Speicherplatz vor dem Aufzeichnen nicht reserviert ist, führt der [MCI- \_ Daten Satz](mci-record.md) Befehl eine implizite Reserve mit gerätespezifischen Standardparametern aus. Bei manchen Implementierungen ist Reserve nicht erforderlich und kann vom Gerätetreiber ignoriert werden. Durch das explizite reservieren von Speicherplatz können Sie besser steuern, wann die Verzögerung für die Datenträger Zuordnung erfolgt, wie viel Speicherplatz belegt wird und wo der Speicherplatz zugeordnet ist. Die Menge und der Speicherort des bereits für diese Geräte Instanz reservierten Speicherplatzes können durch das erneute ausstellen der MCI-Reserve geändert werden \_ . Der zugeordnete und noch nicht verwendete Speicherplatz wird nicht aufgehoben, bis aufgezeichnete Daten gespeichert werden oder bis die Gerätetreiber Instanz geschlossen ist.

Wenn das Video mit dem MCI- \_ Flag off des Befehls [MCI \_ setvideo](mci-setvideo.md) ausgeschaltet ist, enthält der reservierte Speicherplatz kein Video. Wenn Audiodaten mit dem MCI- \_ Flag off des Befehls [MCI \_ setaudioausgeschaltet](mci-setaudio.md) werden, umfasst der reservierte Speicherplatz keine Audiodaten. Wenn sowohl Audiodaten als auch Videos ausgeschaltet sind oder die angeforderte Größe 0 (null) ist, ist kein Speicherplatz reserviert, und der vorhandene reservierte Speicherplatz wird aufgehoben.

Die folgenden zusätzlichen Flags gelten für Digital-Video-Geräte:

<dl> <dt>

<span id="MCI_DGV_RESERVE_IN"></span><span id="mci_dgv_reserve_in"></span>MCI- \_ DGV- \_ Reserve \_ in
</dt> <dd>

Der **lpstrinpath** -Member der durch *lpreserve* identifizierten Struktur enthält die Adresse eines Puffers, der den Speicherort einer temporären Datei enthält. Der Puffer enthält nur das Laufwerk und den Verzeichnispfad der Datei, die zum Speichern der aufgezeichneten Daten verwendet wird. der Dateiname wird vom Gerätetreiber angegeben. Diese temporäre Datei wird gelöscht, wenn die Geräte Instanz geschlossen wird, es sei denn, Sie wird explizit gespeichert. Wenn dieses Flag weggelassen wird, gibt der Gerätetreiber an, wo Speicherplatz zugeordnet ist.

</dd> <dt>

<span id="MCI_DGV_RESERVE_SIZE"></span><span id="mci_dgv_reserve_size"></span>MCI- \_ DGV- \_ Reserve \_ Größe
</dt> <dd>

Der **dwSize** -Member der durch *lpreserve* identifizierten Struktur gibt die ungefähre Menge an Speicherplatz an, die im Arbeitsbereich für die Aufzeichnung reserviert werden soll. Der Wert wird im aktuellen Zeitformat angegeben. Die Menge des Speicherplatzes wird aus der angeforderten Zeit geschätzt und aus dem Dateiformat und Video-und audioalgorithmus sowie Qualitätswerten. Wenn dieses Flag weggelassen wird, verwendet der Gerätetreiber möglicherweise einen Standardwert, den er definiert.

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

 

