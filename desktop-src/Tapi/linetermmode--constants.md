---
description: Die \_ Bit-Flag-Konstanten von linetermmode beschreiben verschiedene Arten von Ereignissen in einer Telefonleitung, die an ein Terminal Gerät weitergeleitet werden können.
ms.assetid: 60af1687-8958-4918-be21-a13780c60974
title: LINETERMMODE_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e689e2e4e432d6cf804e64babd462e749e7e9e2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373716"
---
# <a name="linetermmode_-constants"></a>Linetermmode- \_ Konstanten

Die Bit-Flag-Konstanten von **linetermmode \_** beschreiben verschiedene Arten von Ereignissen in einer Telefonleitung, die an ein Terminal Gerät weitergeleitet werden können.

<dl> <dt>

<span id="LINETERMMODE_BUTTONS"></span><span id="linetermmode_buttons"></span>**linetermmode- \_ Schaltflächen**
</dt> <dd> <dl> <dt>



Dabei handelt es sich um Schaltflächen, die vom Terminal an die Zeile gesendet werden.


</dt> </dl> </dd> <dt>

<span id="LINETERMMODE_DISPLAY"></span><span id="linetermmode_display"></span>**linetermmode- \_ Anzeige**
</dt> <dd> <dl> <dt>



Dies sind Anzeigeinformationen, die von der Zeile an das Terminal gesendet werden.


</dt> </dl> </dd> <dt>

<span id="LINETERMMODE_HOOKSWITCH"></span><span id="linetermmode_hookswitch"></span>**linetermmode ( \_ huokswitch)**
</dt> <dd> <dl> <dt>



Dabei handelt es sich um vom Terminal an die Zeile gesendete Ereignisse vom-Terminal.


</dt> </dl> </dd> <dt>

<span id="LINETERMMODE_LAMPS"></span><span id="linetermmode_lamps"></span>**linetermmode- \_ Lampen**
</dt> <dd> <dl> <dt>



Dies sind Lamp-Ereignisse, die von der Zeile an das Terminal gesendet werden.


</dt> </dl> </dd> <dt>

<span id="LINETERMMODE_MEDIABIDIRECT"></span><span id="linetermmode_mediabidirect"></span>**linetermmode \_ mediabidirect**
</dt> <dd> <dl> <dt>



Dies ist der bidirektionale Mediendaten Strom, der einem-Befehl in der-Zeile und dem Terminal zugeordnet ist. Verwenden Sie diesen Wert, wenn das Routing beider unidirektionaler Kanäle des Medien Stroms eines Aufrufes nicht unabhängig voneinander gesteuert werden kann.


</dt> </dl> </dd> <dt>

<span id="LINETERMMODE_MEDIAFROMLINE"></span><span id="linetermmode_mediafromline"></span>**linetermmode- \_ mediafromline**
</dt> <dd> <dl> <dt>



Dies ist der unidirektionale Mediendaten Strom von der Zeile bis zum Terminal, das einem-Befehl in der Zeile zugeordnet ist. Verwenden Sie diesen Wert, wenn das Routing beider unidirektionaler Kanäle des Medien Stroms eines Aufrufens unabhängig voneinander gesteuert werden kann.


</dt> </dl> </dd> <dt>

<span id="LINETERMMODE_MEDIATOLINE"></span><span id="linetermmode_mediatoline"></span>**linetermmode- \_ mediatoline**
</dt> <dd> <dl> <dt>



Dies ist der unidirektionale Mediendaten Strom vom Terminal zu der Zeile, die einem-Befehl in der Zeile zugeordnet ist. Verwenden Sie diesen Wert, wenn das Routing beider unidirektionaler Kanäle des Medien Stroms eines Aufrufens unabhängig voneinander gesteuert werden kann.


</dt> </dl> </dd> <dt>

<span id="LINETERMMODE_RINGER"></span><span id="linetermmode_ringer"></span>**linetermmode- \_ Ringer**
</dt> <dd> <dl> <dt>



Dies sind die ruftsteuerinformationen, die vom Switch zum Terminal gesendet werden.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Bemerkungen

Keine Erweiterbarkeit. Alle 32 Bits sind reserviert.

Diese Konstanten beschreiben die Klassen von Steuerungs-und Informationsdaten strömen, die direkt zwischen einem Linien Gerät und einem Terminal Gerät (z. b. einem Telefon Satz) weitergeleitet werden können.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2,0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




