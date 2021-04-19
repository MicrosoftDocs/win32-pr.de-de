---
description: Die linecallselect \_ -Bitflag-Konstanten beschreiben, welche Aufrufe ausgewählt werden sollen.
ms.assetid: f19a41bc-403a-4d4b-ab85-240a73514ebb
title: LINECALLSELECT_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8330b4c4e4e14ac399595d10d4a208a3c67f5b2a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370336"
---
# <a name="linecallselect_-constants"></a>Linecallselect- \_ Konstanten

Die **linecallselect \_** -Bitflag-Konstanten beschreiben, welche Aufrufe ausgewählt werden sollen.

<dl> <dt>

<span id="LINECALLSELECT_ADDRESS"></span><span id="linecallselect_address"></span>**linecallselect- \_ Adresse**
</dt> <dd> <dl> <dt>



Wählt den-Befehl für die angegebene Adresse aus.


</dt> </dl> </dd> <dt>

<span id="LINECALLSELECT_CALL"></span><span id="linecallselect_call"></span>**linecallselect \_ -Befehl**
</dt> <dd> <dl> <dt>



Wählt Verwandte Aufrufe des angegebenen Aufrufs aus. Beispielsweise werden die Parteien in einer Konferenz aufgerufen.


</dt> </dl> </dd> <dt>

<span id="LINECALLSELECT_CALLID"></span><span id="linecallselect_callid"></span>**linecallselect- \_ kallid**
</dt> <dd> <dl> <dt>



Wählt Verwandte Aufrufe der angegebenen Aufruf Kennung aus. Dieses Flag ist nur für Anwendungen verfügbar, die eine TAPI-Version von 3,0 oder höher aushandeln.


</dt> </dl> </dd> <dt>

<span id="LINECALLSELECT_DEVICEID"></span><span id="linecallselect_deviceid"></span>**linecallselect-Geräte-ID \_**
</dt> <dd> <dl> <dt>



Wählt Aufrufe für den angegebenen Geräte Bezeichner aus. Dieses Flag ist nur für Anwendungen verfügbar, die eine TAPI-Version von 2,1 oder höher aushandeln. Anwendungen sollten in Erwägung gezogen werden, die linecallselect- \_ Zeilen Konstante anstelle dieser zu verwenden.


</dt> </dl> </dd> <dt>

<span id="LINECALLSELECT_LINE"></span><span id="linecallselect_line"></span>**linecallselect- \_ Zeile**
</dt> <dd> <dl> <dt>



Wählt Aufrufe auf dem angegebenen Zeilen Gerät aus.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Bemerkungen

Keine Erweiterbarkeit. Alle 32 Bits sind reserviert.

Diese Konstante wird in [**linegetnewcalls**](/windows/desktop/api/Tapi/nf-tapi-linegetnewcalls) verwendet, um eine Auswahl (Bereich) der angeforderten Aufrufe anzugeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2,0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




