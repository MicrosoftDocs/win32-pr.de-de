---
description: Die linecallorigin- \_ Konstanten beschreiben den Ursprung eines Aufrufes.
ms.assetid: b830a40e-62d9-4a6c-b43f-8318f30a7cd4
title: LINECALLORIGIN_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f00495d67dcff56ef7ee34cd85600a281e006ec3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351262"
---
# <a name="linecallorigin_-constants"></a>Linecallorigin- \_ Konstanten

Die **linecallorigin \_** -Konstanten beschreiben den Ursprung eines Aufrufes.

<dl> <dt>

<span id="LINECALLORIGIN_CONFERENCE"></span><span id="linecallorigin_conference"></span>**linecallorigin- \_ Konferenz**
</dt> <dd> <dl> <dt>



Das Telefon Handle ist ein Konferenzgespräch, d. h., es handelt sich um die Verbindung der Anwendung mit der Konferenzbrücke im Switch.


</dt> </dl> </dd> <dt>

<span id="LINECALLORIGIN_EXTERNAL"></span><span id="linecallorigin_external"></span>**linecallorigin \_ extern**
</dt> <dd> <dl> <dt>



Der-Befehl stammt als eingehender-Rückruf für eine externe Zeile.


</dt> </dl> </dd> <dt>

<span id="LINECALLORIGIN_INBOUND"></span><span id="linecallorigin_inbound"></span>**linecallorigin \_ eingehend**
</dt> <dd> <dl> <dt>



Der-Befehl stammt als eingehender-Rückruf, aber der Dienstanbieter kann nicht ermitteln, ob er von einer anderen Station desselben Switches oder von einer externen Zeile stammt. Dienstanbieter können diese Konstante nur verwenden, wenn TAPI-Version 1,4 oder höher ausgehandelt wurde. Andernfalls kann der Dienstanbieter den "linecallorigin"- \_ nicht Gebrauch ersetzen.


</dt> </dl> </dd> <dt>

<span id="LINECALLORIGIN_INTERNAL"></span><span id="linecallorigin_internal"></span>**linecallorigin ( \_ intern)**
</dt> <dd> <dl> <dt>



Der-Befehl stammt als eingehender aufrufungsort an einer Station, die sich intern in derselben Wechsel Umgebung befand.


</dt> </dl> </dd> <dt>

<span id="LINECALLORIGIN_OUTBOUND"></span><span id="linecallorigin_outbound"></span>**linecallorigin \_ ausgehend**
</dt> <dd> <dl> <dt>



Der-Befehl stammt von dieser Station als ausgehender-Befehl.


</dt> </dl> </dd> <dt>

<span id="LINECALLORIGIN_UNAVAIL"></span><span id="linecallorigin_unavail"></span>**linecallorigin ist \_ nicht erreichbar.**
</dt> <dd> <dl> <dt>



Der Ursprungs Ursprung ist nicht verfügbar und wird für diesen-Befehl nie bekannt werden.


</dt> </dl> </dd> <dt>

<span id="LINECALLORIGIN_UNKNOWN"></span><span id="linecallorigin_unknown"></span>**linecallorigin \_ unbekannt**
</dt> <dd> <dl> <dt>



Der Ursprungs Ursprung ist derzeit unbekannt, kann aber später bekannt werden.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Bemerkungen

Keine Erweiterbarkeit. Alle 32 Bits sind reserviert.

Der Ursprung eines Aufrufes wird im Member **dwOrigin** der [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) -Struktur des Aufrufes gespeichert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2,0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




