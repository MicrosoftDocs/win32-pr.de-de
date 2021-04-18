---
description: Die linedigitmode- \_ Konstanten beschreiben verschiedene Arten der Generierung von Inband-Ziffern.
ms.assetid: d603ea28-2b93-4548-bb16-78e93087f828
title: LINEDIGITMODE_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50bedd7f508368a84ab2fa70fac37c316dcc6c85
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352857"
---
# <a name="linedigitmode_-constants"></a>Linedigitmode- \_ Konstanten

Die **linedigitmode \_** -Konstanten beschreiben verschiedene Arten der Generierung von Inband-Ziffern.

<dl> <dt>

<span id="LINEDIGITMODE_DTMF"></span><span id="linedigitmode_dtmf"></span>**linedigitmode- \_ DTMF**
</dt> <dd> <dl> <dt>



Verwendet DTMF-Töne zum Signalisieren von Ziffern. Gültige Ziffern sind 0 bis 9, " \* ", " \# ", "a", "B", "C" und "d".


</dt> </dl> </dd> <dt>

<span id="LINEDIGITMODE_DTMFEND"></span><span id="linedigitmode_dtmfend"></span>**linedigitmode- \_ dtmfend**
</dt> <dd> <dl> <dt>



Verwendet DTMF-Töne, um Ziffern zu signalisieren und die unten Kanten zu erkennen. Gültige Ziffern sind 0 bis 9, " \* ", " \# ", "a", "B", "C" und "d".


</dt> </dl> </dd> <dt>

<span id="LINEDIGITMODE_PULSE"></span><span id="linedigitmode_pulse"></span>**linedigitmode- \_ Pulse**
</dt> <dd> <dl> <dt>



Verwendet zum Signalisieren von Ziffern Dreh Pulse Sequenzen. Gültige Ziffern sind 0 bis 9.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Bemerkungen

Keine Erweiterbarkeit. Alle 32 Bits sind reserviert.

Beim Erstellen oder erkennen von Ziffern kann ein Ziffern Modus angegeben werden. Beachten Sie, dass pulsziffern generiert werden, indem Sie die lokale Schleifen Verbindung erstellen und unterbrechen. Diese Pulse werden vom-Schalter übernommen. Das Remote Ende beobachtet dies nur als eine Reihe von Inband-audioklicks. Durch das Erkennen von Ziffern, die als Pulse gesendet werden, müssen diese Sequenzen von 1 bis 10 beschreibenden Klicks erkannt werden können.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2,0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




