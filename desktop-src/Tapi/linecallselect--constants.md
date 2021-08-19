---
description: Die \_ LINECALLSELECT-Bitflagkonst constants beschreiben, welche Aufrufe ausgewählt werden sollen.
ms.assetid: f19a41bc-403a-4d4b-ab85-240a73514ebb
title: LINECALLSELECT_ Konstanten (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: feaa76ea5b421b8090f9289431bfee65be61a6b47abd170569beff73a9846533
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003148"
---
# <a name="linecallselect_-constants"></a>\_LINECALLSELECT-Konstanten

Die **\_ LINECALLSELECT-Bitflagkonst** constants beschreiben, welche Aufrufe ausgewählt werden sollen.

<dl> <dt>

<span id="LINECALLSELECT_ADDRESS"></span><span id="linecallselect_address"></span>**\_LINECALLSELECT-ADRESSE**
</dt> <dd> <dl> <dt>



Wählt einen Aufruf für die angegebene Adresse aus.


</dt> </dl> </dd> <dt>

<span id="LINECALLSELECT_CALL"></span><span id="linecallselect_call"></span>**LINECALLSELECT-AUFRUF \_**
</dt> <dd> <dl> <dt>



Wählt verwandte Aufrufe des angegebenen Aufrufs aus. Beispielsweise die Parteien in einem Telefonkonferenz.


</dt> </dl> </dd> <dt>

<span id="LINECALLSELECT_CALLID"></span><span id="linecallselect_callid"></span>**LINECALLSELECT \_ CALLID**
</dt> <dd> <dl> <dt>



Wählt verwandte Aufrufe des angegebenen Aufrufbezeichners aus. Dieses Flag wird nur für Anwendungen verfügbar gemacht, die eine TAPI-Version von 3.0 oder höher aushandeln.


</dt> </dl> </dd> <dt>

<span id="LINECALLSELECT_DEVICEID"></span><span id="linecallselect_deviceid"></span>**LINECALLSELECT \_ DEVICEID**
</dt> <dd> <dl> <dt>



Wählt Aufrufe für die angegebene Geräte-ID aus. Dieses Flag wird nur für Anwendungen verfügbar gemacht, die eine TAPI-Version von 2.1 oder höher aushandeln. Anwendungen sollten die Verwendung der LINECALLSELECT \_ LINE-Konstante anstelle dieser verwenden.


</dt> </dl> </dd> <dt>

<span id="LINECALLSELECT_LINE"></span><span id="linecallselect_line"></span>**LINECALLSELECT \_ LINE**
</dt> <dd> <dl> <dt>



Wählt Aufrufe auf dem angegebenen Zeilengerät aus.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Hinweise

Keine Erweiterbarkeit. Alle 32 Bits sind reserviert.

Diese Konstante wird in [**lineGetNewCalls**](/windows/desktop/api/Tapi/nf-tapi-linegetnewcalls) und verwendet, um eine Auswahl (bereich) der angeforderten Aufrufe anzugeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2.0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




