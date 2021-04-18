---
description: Die \_ Bit-Flag-Konstanten von phonestatusflags beschreiben eine Vielzahl von Telefongeräte Statusinformationen.
ms.assetid: e94da591-49ab-4932-8621-0a62b8a55dd6
title: PHONESTATUSFLAGS_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 969c2553274037797bdf9abea3e8bdbc1cd8d018
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359287"
---
# <a name="phonestatusflags_-constants"></a>Phonestatus-Flags- \_ Konstanten

Die Bit-Flag-Konstanten von **phonestatusflags \_** beschreiben eine Vielzahl von Telefongeräte Statusinformationen.

<dl> <dt>

<span id="PHONESTATUSFLAGS_CONNECTED"></span><span id="phonestatusflags_connected"></span>**Verbindung mit phonestatus-Flags \_**
</dt> <dd> <dl> <dt>



Gibt an, ob das Telefon derzeit mit TAPI verbunden ist. **True** , wenn eine Verbindung hergestellt wurde, andernfalls **false** .


</dt> </dl> </dd> <dt>

<span id="PHONESTATUSFLAGS_SUSPENDED"></span><span id="phonestatusflags_suspended"></span>**phonestatus \_ -Flags angehalten**
</dt> <dd> <dl> <dt>



Gibt an, ob TAPI das Telefongerät bearbeitet hat. **True** , wenn angehalten, andernfalls **false** . Die Verwendung eines Telefon Geräts für eine Anwendung kann vorübergehend angehalten werden, wenn der Switch das Telefon auf eine Weise ändern möchte, die keine Störungen der Anwendung tolerieren kann.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Bemerkungen

Keine Erweiterbarkeit. Alle 32 Bits sind reserviert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2,0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




