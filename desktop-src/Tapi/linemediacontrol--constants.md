---
description: Die linemediacontrol \_ -bitflagkonstanten beschreiben einen Satz generischer Vorgänge für Mediendaten Ströme.
ms.assetid: 1e8aeda8-2810-462a-bfba-0296d854d9aa
title: LINEMEDIACONTROL_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3241a3b5f4f8a0363f30ce7aefaded0c63fc4189
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362030"
---
# <a name="linemediacontrol_-constants"></a>Linemediacontrol- \_ Konstanten

Die **linemediacontrol \_** -bitflagkonstanten beschreiben einen Satz generischer Vorgänge für Mediendaten Ströme. Die Interpretationen werden durch den Mediendaten Strom bestimmt. Das liniengerät muss über die Medien Steuerungsfunktion verfügen, damit jeder Medien Steuerungs Vorgang effektiv ist.

<dl> <dt>

<span id="LINEMEDIACONTROL_NONE"></span><span id="linemediacontrol_none"></span>**linemediacontrol \_ None**
</dt> <dd> <dl> <dt>



Es muss keine Änderung am Medienstrom vorgenommen werden.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIACONTROL_PAUSE"></span><span id="linemediacontrol_pause"></span>**linemediacontrol \_ Anhalten**
</dt> <dd> <dl> <dt>



Halten Sie den Mediendaten Strom vorübergehend an.

Die Geschwindigkeit des Medien Stroms wird normal zurückgegeben.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIACONTROL_RATEDOWN"></span><span id="linemediacontrol_ratedown"></span>**linemediacontrol- \_ Raten nach unten**
</dt> <dd> <dl> <dt>



Die Geschwindigkeit des Mediendaten Stroms wird durch eine streamdefinierte Menge verringert.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIACONTROL_RATENORMAL"></span><span id="linemediacontrol_ratenormal"></span>**linemediacontrol \_ ratenormal**
</dt> <dd> <dl> <dt>


</dt> </dl> </dd> <dt>

<span id="LINEMEDIACONTROL_RATEUP"></span><span id="linemediacontrol_rateup"></span>**linemediacontrol- \_ rateup**
</dt> <dd> <dl> <dt>



Die Geschwindigkeit des Mediendaten Stroms wird durch eine streamdefinierte Menge gesteigert.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIACONTROL_RESET"></span><span id="linemediacontrol_reset"></span>**linemediacontrol \_ Zurücksetzen**
</dt> <dd> <dl> <dt>



Setzt den Mediendaten Strom zurück. Äquivalent zu einem Eingangs Ende. Alle Puffer werden freigegeben.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIACONTROL_RESUME"></span><span id="linemediacontrol_resume"></span>**linemediacontrol \_ fortsetzen**
</dt> <dd> <dl> <dt>



Fortsetzen eines angehaltenen Mediendaten Stroms


</dt> </dl> </dd> <dt>

<span id="LINEMEDIACONTROL_START"></span><span id="linemediacontrol_start"></span>**linemediacontrol \_ starten**
</dt> <dd> <dl> <dt>



Starten Sie den Mediendaten Strom.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIACONTROL_VOLUMEDOWN"></span><span id="linemediacontrol_volumedown"></span>**linemediacontrol- \_ volumedown**
</dt> <dd> <dl> <dt>



Die Amplitude des Mediendaten Stroms wird durch eine streamdefinierte Menge verringert.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIACONTROL_VOLUMENORMAL"></span><span id="linemediacontrol_volumenormal"></span>**linemediacontrol \_ volumenormal**
</dt> <dd> <dl> <dt>



Die Amplitude des Mediendaten Stroms wird normal zurückgegeben.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIACONTROL_VOLUMEUP"></span><span id="linemediacontrol_volumeup"></span>**linemediacontrol- \_ volumeup**
</dt> <dd> <dl> <dt>



Die Amplitude des Mediendaten Stroms wird durch eine streamdefinierte Menge erweitert.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die höherwertigen 16 Bits können für gerätespezifische Erweiterungen zugewiesen werden. Die nieder wertigen 16 Bits sind reserviert.

Mediensteuerung wird bereitgestellt, um die Leistung von Aktionen in Mediendaten strömen als Reaktion auf telefoniebezogene Ereignisse zu verbessern. Die Anwendung sollte normalerweise einen Mediendaten Strom über die medienspezifische API verwalten. Die hier bereitgestellte Medien Steuerungsfunktion ist nicht zum Ersetzen der APIs für Native Medien vorgesehen.

Medien Steuerungs Aktionen können mit der Erkennung von Ziffern, der Erkennung von Tönen, dem Übergang in einen aufrufzustand und der Erkennung eines Medientyps verknüpft werden. Überprüfen Sie die Gerätefunktionen einer Zeile, um zu bestimmen, ob die Mediensteuerung in der Zeile verfügbar ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2,0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




