---
description: Die \_ Bitflag-Konstanten von linecallpartyid beschreiben die Art der Informationen, die über die an einem-Befehl beteiligten Parteien verfügbar sind.
ms.assetid: e2a89f25-15f0-4f3c-9ac8-1e6b72c0d8db
title: LINECALLPARTYID_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5dd8cca75fe6e91b97fac63dca6c0fdda554394
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370826"
---
# <a name="linecallpartyid_-constants"></a>Linecallpartyid- \_ Konstanten

Die Bitflag-Konstanten von **linecallpartyid \_** beschreiben die Art der Informationen, die über die an einem-Befehl beteiligten Parteien verfügbar sind.

<dl> <dt>

<span id="LINECALLPARTYID_ADDRESS"></span><span id="linecallpartyid_address"></span>**linecallpartyid- \_ Adresse**
</dt> <dd> <dl> <dt>



Informationen zu Partei Bezeichnern bestehen aus der Adresse der Partei im kanonischen Adressformat oder im Format der ausführbaren Adresse.


</dt> </dl> </dd> <dt>

<span id="LINECALLPARTYID_BLOCKED"></span><span id="linecallpartyid_blocked"></span>**die linecallpartyid ist \_ blockiert.**
</dt> <dd> <dl> <dt>



Die Informationen zur Partei Kennung sind nicht verfügbar, da Sie von der Remote Partei blockiert wurden.


</dt> </dl> </dd> <dt>

<span id="LINECALLPARTYID_NAME"></span><span id="linecallpartyid_name"></span>**Name der linecallpartyid \_**
</dt> <dd> <dl> <dt>



Die Informationen zur Partei Kennung bestehen aus dem Namen der Partei (z. b. aus einem Verzeichnis, das im Switch aufbewahrt wird).


</dt> </dl> </dd> <dt>

<span id="LINECALLPARTYID_OUTOFAREA"></span><span id="linecallpartyid_outofarea"></span>**linecallpartyid- \_ outof-Bereich**
</dt> <dd> <dl> <dt>



Aufrufer-ID-Informationen für den Aufruf sind nicht verfügbar, da Sie nicht auf die gesamte Weise vom Netzwerk weitergegeben werden.


</dt> </dl> </dd> <dt>

<span id="LINECALLPARTYID_PARTIAL"></span><span id="linecallpartyid_partial"></span>**linecallpartyid \_ partiell**
</dt> <dd> <dl> <dt>



Die Informationen zu Partei Bezeichnern sind gültig, sind jedoch nur auf partielle Informationen beschränkt.


</dt> </dl> </dd> <dt>

<span id="LINECALLPARTYID_UNAVAIL"></span><span id="linecallpartyid_unavail"></span>**linecallpartyid ist \_ nicht erreichbar.**
</dt> <dd> <dl> <dt>



Die Informationen zur Partei Kennung sind nicht verfügbar und werden später nicht mehr verfügbar sein. Informationen sind aus unbekannten Gründen möglicherweise nicht verfügbar. Beispielsweise wurden die Informationen nicht vom Netzwerk übermittelt, Sie wurden vom Dienstanbieter ignoriert usw.


</dt> </dl> </dd> <dt>

<span id="LINECALLPARTYID_UNKNOWN"></span><span id="linecallpartyid_unknown"></span>**linecallpartyid \_ unbekannt**
</dt> <dd> <dl> <dt>



Informationen zu Partei Bezeichnern sind zurzeit unbekannt, werden aber später möglicherweise bekannt sein.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Bemerkungen

Keine Erweiterbarkeit. Alle 32 Bits sind reserviert.

Für jede der möglichen Parteien, die an einem-Befehl beteiligt sind, beschreiben die **linecallpartyid \_** -Konstanten, wie die Partei-Bezeichnerinformationen formatiert sind. Diese Informationen werden in der [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) -Datenstruktur bereitgestellt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2,0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




