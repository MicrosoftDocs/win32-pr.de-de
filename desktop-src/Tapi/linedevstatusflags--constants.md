---
description: Die \_ Bit-Flag-Konstanten von linedevstatusflags beschreiben eine Auflistung boolescher Zeilen-Gerätestatus Elemente.
ms.assetid: 5fa754d3-07b2-4b75-91ef-1bf961d9fef4
title: LINEDEVSTATUSFLAGS_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70745b1a84119af2305cadabd0a39ab5954e5b7c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369563"
---
# <a name="linedevstatusflags_-constants"></a>Linedevstatus Flags- \_ Konstanten

Die Bit-Flag-Konstanten von **linedevstatusflags \_** beschreiben eine Auflistung boolescher Zeilen-Gerätestatus Elemente.

<dl> <dt>

<span id="LINEDEVSTATUSFLAGS_CONNECTED"></span><span id="linedevstatusflags_connected"></span>**verknüpfte linedevstatus \_ -Flags**
</dt> <dd> <dl> <dt>



Gibt an, ob die Linie mit TAPI verbunden ist. **True** gibt an, dass die Linie verbunden ist und TAPI auf dem liniengerät betrieben werden kann. Wenn der Wert **false** ist, wird die Zeile getrennt, und die Anwendung kann das liniengerät nicht über TAPI steuern.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATUSFLAGS_INSERVICE"></span><span id="linedevstatusflags_inservice"></span>**linedevstatus Flags- \_ INService**
</dt> <dd> <dl> <dt>



Gibt an, ob die Zeile im Dienst ist. **True** gibt an, dass sich die Zeile im Dienst befindet. Wenn der Wert **false** ist, ist die Zeile nicht mehr Dienst.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATUSFLAGS_LOCKED"></span><span id="linedevstatusflags_locked"></span>**linedevstatus-Flags \_ gesperrt**
</dt> <dd> <dl> <dt>



Gibt an, ob die Zeile gesperrt oder entsperrt ist. Dieses Bit wird am häufigsten bei Linien Geräten verwendet, die Mobiltelefonen zugeordnet sind. Viele Mobiltelefone verfügen über einen Sicherheitsmechanismus, der die Eingabe eines Kennworts erfordert, damit das Telefonanrufe platzieren kann. Dieses Bit kann verwendet werden, um Anwendungen mitzuteilen, dass das Telefon gesperrt ist, und kann keine Anrufe platzieren, bis das Kennwort auf der Benutzeroberfläche des Telefons eingegeben wird, damit die Anwendung dem Benutzer eine entsprechende Warnung präsentieren kann.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATUSFLAGS_MSGWAIT"></span><span id="linedevstatusflags_msgwait"></span>**linedevstatus Flags \_ msgwait**
</dt> <dd> <dl> <dt>



Gibt an, ob die Zeile eine Nachricht wartet. **True** gibt an, dass eine Nachricht wartet. **false** gibt an, dass keine Nachricht wartet.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Bemerkungen

Keine Erweiterbarkeit. Alle 32 Bits sind reserviert.

Linedevstatusflags- \_ Konstanten werden innerhalb des **dwdevstatusflags** -Members der [**linedevstatus**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) -Datenstruktur verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2,0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




