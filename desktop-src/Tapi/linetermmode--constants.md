---
description: Die \_ LINETERMMODE-Bitflagkonstanten beschreiben verschiedene Arten von Ereignissen in einer Telefonleitung, die an ein Terminalgerät weitergeleitet werden können.
ms.assetid: 60af1687-8958-4918-be21-a13780c60974
title: LINETERMMODE_ Konstanten (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 411c1dd633ff1bef49e08eb127f4145f81f3d6785d07f3566431fe7b5d7e8fee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119518810"
---
# <a name="linetermmode_-constants"></a>\_LINETERMMODE-Konstanten

Die **\_ LINETERMMODE-Bitflagkonstanten** beschreiben verschiedene Arten von Ereignissen in einer Telefonleitung, die an ein Terminalgerät weitergeleitet werden können.

<dl> <dt>

<span id="LINETERMMODE_BUTTONS"></span><span id="linetermmode_buttons"></span>**\_LINETERMMODE-SCHALTFLÄCHEN**
</dt> <dd> <dl> <dt>



Hierbei handelt es sich um Ereignisse mit Schaltflächendruck, die vom Terminal an die Zeile gesendet werden.


</dt> </dl> </dd> <dt>

<span id="LINETERMMODE_DISPLAY"></span><span id="linetermmode_display"></span>**\_LINETERMMODE-ANZEIGE**
</dt> <dd> <dl> <dt>



Hierbei handelt es sich um Anzeigeinformationen, die von der Zeile an das Terminal gesendet werden.


</dt> </dl> </dd> <dt>

<span id="LINETERMMODE_HOOKSWITCH"></span><span id="linetermmode_hookswitch"></span>**LINETERMMODE \_ HOOKSWITCH**
</dt> <dd> <dl> <dt>



Dies sind Hookswitch-Ereignisse, die vom Terminal an die Zeile gesendet werden.


</dt> </dl> </dd> <dt>

<span id="LINETERMMODE_LAMPS"></span><span id="linetermmode_lamps"></span>**\_LINETERMMODE-PAUSE**
</dt> <dd> <dl> <dt>



Dabei handelt es sich um Lampeereignisse, die von der Linie an das Terminal gesendet werden.


</dt> </dl> </dd> <dt>

<span id="LINETERMMODE_MEDIABIDIRECT"></span><span id="linetermmode_mediabidirect"></span>**LINETERMMODE \_ MEDIABIDIRECT**
</dt> <dd> <dl> <dt>



Dies ist der bidirektionale Medienstream, der einem Aufruf in der Zeile und im Terminal zugeordnet ist. Verwenden Sie diesen Wert, wenn das Routing beider unidirektionaler Kanäle des Mediendatenstroms eines Aufrufs nicht unabhängig gesteuert werden kann.


</dt> </dl> </dd> <dt>

<span id="LINETERMMODE_MEDIAFROMLINE"></span><span id="linetermmode_mediafromline"></span>**LINETERMMODE \_ MEDIAFROMLINE**
</dt> <dd> <dl> <dt>



Dies ist der unidirektionale Medienstream von der Zeile zum Terminal, das einem Aufruf der Zeile zugeordnet ist. Verwenden Sie diesen Wert, wenn das Routing beider unidirektionaler Kanäle des Mediendatenstroms eines Aufrufs unabhängig gesteuert werden kann.


</dt> </dl> </dd> <dt>

<span id="LINETERMMODE_MEDIATOLINE"></span><span id="linetermmode_mediatoline"></span>**LINETERMMODE \_ MEDIATOLINE**
</dt> <dd> <dl> <dt>



Dies ist der unidirektionale Medienstream vom Terminal zu der Zeile, die einem Aufruf in der Zeile zugeordnet ist. Verwenden Sie diesen Wert, wenn das Routing beider unidirektionaler Kanäle des Mediendatenstroms eines Aufrufs unabhängig gesteuert werden kann.


</dt> </dl> </dd> <dt>

<span id="LINETERMMODE_RINGER"></span><span id="linetermmode_ringer"></span>**LINETERMMODE \_ RINGER**
</dt> <dd> <dl> <dt>



Dies sind Ringersteuerelementinformationen, die vom Switch an das Terminal gesendet werden.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Hinweise

Keine Erweiterbarkeit. Alle 32 Bits sind reserviert.

Diese Konstanten beschreiben die Klassen von Steuerungs- und Informationsstreams, die direkt zwischen einem Liniengerät und einem Terminalgerät (z. B. einem Telefonsatz) weitergeleitet werden können.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2.0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




