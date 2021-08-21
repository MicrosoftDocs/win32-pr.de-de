---
description: Die \_ LINEDEVSTATUSFLAGS-Bitflagkonstanten beschreiben eine Auflistung von Gerätestatuselementen für boolesche Zeilen.
ms.assetid: 5fa754d3-07b2-4b75-91ef-1bf961d9fef4
title: LINEDEVSTATUSFLAGS_ Konstanten (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6649dc39c787be7c0b7f027637f12ff7f5d028add09b9f7d568149c6e9f76c97
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119682008"
---
# <a name="linedevstatusflags_-constants"></a>LINEDEVSTATUSFLAGS-Konstanten \_

Die **\_ LINEDEVSTATUSFLAGS-Bitflagkonstanten** beschreiben eine Auflistung von Gerätestatuselementen für boolesche Zeilen.

<dl> <dt>

<span id="LINEDEVSTATUSFLAGS_CONNECTED"></span><span id="linedevstatusflags_connected"></span>**LINEDEVSTATUSFLAGS \_ VERBUNDEN**
</dt> <dd> <dl> <dt>



Gibt an, ob die Zeile mit TAPI verbunden ist. True gibt an, dass die Linie verbunden ist und TAPI auf dem Liniengerät betrieben werden kann. **False** gibt an, dass die Verbindung getrennt wird und die Anwendung das Zeilengerät nicht über TAPI steuern kann.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATUSFLAGS_INSERVICE"></span><span id="linedevstatusflags_inservice"></span>**LINEDEVSTATUSFLAGS \_ INSERVICE**
</dt> <dd> <dl> <dt>



Gibt an, ob sich die Zeile im Dienst befindet. True gibt an, dass sich die Zeile im Dienst befindet. **false** gibt an, dass die Zeile nicht mehr in Betrieb ist.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATUSFLAGS_LOCKED"></span><span id="linedevstatusflags_locked"></span>**LINEDEVSTATUSFLAGS \_ GESPERRT**
</dt> <dd> <dl> <dt>



Gibt an, ob die Zeile gesperrt oder entsperrt ist. Dieses Bit wird am häufigsten mit Zeilengeräten verwendet, die Mobiltelefonen zugeordnet sind. Viele Mobiltelefone verfügen über einen Sicherheitsmechanismus, der die Eingabe eines Kennworts erfordert, damit das Telefon Anrufe tätigen kann. Dieses Bit kann verwendet werden, um Anwendungen anzugeben, dass das Telefon gesperrt ist und keine Anrufe tätigen kann, bis das Kennwort auf der Benutzeroberfläche des Telefons eingegeben wurde, sodass die Anwendung dem Benutzer eine entsprechende Warnung anzeigen kann.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATUSFLAGS_MSGWAIT"></span><span id="linedevstatusflags_msgwait"></span>**LINEDEVSTATUSFLAGS \_ MSGWAIT**
</dt> <dd> <dl> <dt>



Gibt an, ob in der Zeile eine Nachricht wartet. True gibt an, dass eine Nachricht wartet. **false** gibt an, dass keine Nachricht wartet.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Hinweise

Keine Erweiterbarkeit. Alle 32 Bits sind reserviert.

LINEDEVSTATUSFLAGS-Konstanten \_ werden innerhalb des **dwDevStatusFlags-Elements** der [**LINEDEVSTATUS-Datenstruktur**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2.0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




