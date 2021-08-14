---
description: Die \_ LINEMEDIACONTROL-Bitflagkonstanten beschreiben einen Satz generischer Vorgänge für Medienstreams.
ms.assetid: 1e8aeda8-2810-462a-bfba-0296d854d9aa
title: LINEMEDIACONTROL_ Konstanten (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f54c7c83df769eef91afe7c310452c342a855f44391815bbc4429ac07bb6ec92
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119309970"
---
# <a name="linemediacontrol_-constants"></a>\_LINEMEDIACONTROL-Konstanten

Die **\_ LINEMEDIACONTROL-Bitflagkonstanten** beschreiben einen Satz generischer Vorgänge für Medienstreams. Die Interpretationen werden durch den Medienstream bestimmt. Das Liniengerät muss über die Mediensteuerungsfunktion verfügen, damit jeder Mediensteuerungsvorgang effektiv ist.

<dl> <dt>

<span id="LINEMEDIACONTROL_NONE"></span><span id="linemediacontrol_none"></span>**LINEMEDIACONTROL \_ NONE**
</dt> <dd> <dl> <dt>



Es ist keine Änderung am Medienstream erforderlich.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIACONTROL_PAUSE"></span><span id="linemediacontrol_pause"></span>**LINEMEDIACONTROL \_ PAUSE**
</dt> <dd> <dl> <dt>



Halten Sie den Medienstream vorübergehend an.

Die Geschwindigkeit des Medienstreams wird normal zurückgegeben.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIACONTROL_RATEDOWN"></span><span id="linemediacontrol_ratedown"></span>**LINEMEDIACONTROL \_ RATEDOWN**
</dt> <dd> <dl> <dt>



Die Geschwindigkeit des Medienstreams wird um eine durch den Stream definierte Menge verringert.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIACONTROL_RATENORMAL"></span><span id="linemediacontrol_ratenormal"></span>**LINEMEDIACONTROL \_ RATENORMAL**
</dt> <dd> <dl> <dt>


</dt> </dl> </dd> <dt>

<span id="LINEMEDIACONTROL_RATEUP"></span><span id="linemediacontrol_rateup"></span>**LINEMEDIACONTROL \_ RATEUP**
</dt> <dd> <dl> <dt>



Die Geschwindigkeit des Medienstreams wird um eine durch den Stream definierte Menge erhöht.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIACONTROL_RESET"></span><span id="linemediacontrol_reset"></span>**LINEMEDIACONTROL \_ RESET**
</dt> <dd> <dl> <dt>



Setzen Sie den Medienstream zurück. Entspricht einem Eingabeende. Alle Puffer werden freigegeben.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIACONTROL_RESUME"></span><span id="linemediacontrol_resume"></span>**LINEMEDIACONTROL \_ RESUME**
</dt> <dd> <dl> <dt>



Setzen Sie einen angehaltenen Medienstream fort.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIACONTROL_START"></span><span id="linemediacontrol_start"></span>**LINEMEDIACONTROL \_ START**
</dt> <dd> <dl> <dt>



Starten Sie den Medienstream.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIACONTROL_VOLUMEDOWN"></span><span id="linemediacontrol_volumedown"></span>**LINEMEDIACONTROL \_ VOLUMEDOWN**
</dt> <dd> <dl> <dt>



Die Amplitude des Medienstreams wird um eine vom Stream definierte Menge verringert.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIACONTROL_VOLUMENORMAL"></span><span id="linemediacontrol_volumenormal"></span>**LINEMEDIACONTROL \_ VOLUMENORMAL**
</dt> <dd> <dl> <dt>



Die Amplitude des Medienstreams wird normal zurückgegeben.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIACONTROL_VOLUMEUP"></span><span id="linemediacontrol_volumeup"></span>**LINEMEDIACONTROL \_ VOLUMEUP**
</dt> <dd> <dl> <dt>



Die Amplitude des Medienstreams wird um eine vom Stream definierte Menge erhöht.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Hinweise

Die 16 Bits mit hoher Ordnung können für gerätespezifische Erweiterungen zugewiesen werden. Die niedrigen 16 Bits sind reserviert.

Die Mediensteuerung wird bereitgestellt, um die Leistung von Aktionen in Medienstreams als Reaktion auf telefoniebezogene Ereignisse zu verbessern. Die Anwendung sollte normalerweise einen Medienstream über die medienspezifische API verwalten. Die hier bereitgestellte Mediensteuerungsfunktion dient nicht dazu, die nativen Medien-APIs zu ersetzen.

Mediensteuerungsaktionen können der Erkennung von Ziffern, der Erkennung von Tönen, dem Übergang in einen Aufrufzustand und der Erkennung eines Medientyps zugeordnet werden. Überprüfen Sie anhand der Gerätefunktionen einer Zeile, ob die Mediensteuerung in der Zeile verfügbar ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2.0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




