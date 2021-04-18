---
description: Die \_ Bit-Flag-Konstanten von phonehuokswitchmode beschreiben die Mikrofon-und Redner Komponenten eines "huokswitch"-Geräts.
ms.assetid: 532bf089-d5ca-4a04-847d-69e48990ff5c
title: PHONEHOOKSWITCHMODE_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8028cb531d5b38185edf75ae58e4c3c855398f2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352178"
---
# <a name="phonehookswitchmode_-constants"></a>Phonehuokswitchmode- \_ Konstanten

Die Bit-Flag-Konstanten von **phonehuokswitchmode \_** beschreiben die Mikrofon-und Redner Komponenten eines "huokswitch"-Geräts.

<dl> <dt>

<span id="PHONEHOOKSWITCHMODE_MIC"></span><span id="phonehookswitchmode_mic"></span>**phonehuokswitchmode \_ MIC**
</dt> <dd> <dl> <dt>



Das Mikrofon des Geräts ist aktiv, der Redner ist stumm.


</dt> </dl> </dd> <dt>

<span id="PHONEHOOKSWITCHMODE_MICSPEAKER"></span><span id="phonehookswitchmode_micspeaker"></span>**phonehuokswitchmode \_ micspeaker**
</dt> <dd> <dl> <dt>



Das Mikrofon und der Referent des Geräts sind aktiv.


</dt> </dl> </dd> <dt>

<span id="PHONEHOOKSWITCHMODE_ONHOOK"></span><span id="phonehookswitchmode_onhook"></span>**phonehuokswitchmode- \_ OnHook**
</dt> <dd> <dl> <dt>



Das Mikrofon und der Referent des Geräts sind beide OnHook.


</dt> </dl> </dd> <dt>

<span id="PHONEHOOKSWITCHMODE_SPEAKER"></span><span id="phonehookswitchmode_speaker"></span>**phonehuokswitchmode- \_ Sprecher**
</dt> <dd> <dl> <dt>



Der Redner des Geräts ist aktiv, das Mikrofon ist stumm.


</dt> </dl> </dd> <dt>

<span id="PHONEHOOKSWITCHMODE_UNKNOWN"></span><span id="phonehookswitchmode_unknown"></span>**phonehuokswitchmode \_ unbekannt**
</dt> <dd> <dl> <dt>



Der Geräte Modus für den Gerätewechsel ist zurzeit unbekannt.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Bemerkungen

Keine Erweiterbarkeit. Alle 32 Bits sind reserviert.

Diese Konstanten werden verwendet, um eine individuelle Steuerungsebene für die Mikrofon-und Redner Komponenten eines Telefon Geräts bereitzustellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2,0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




