---
description: Die \_ PHONESTATUSFLAGS-Bitflags-Konstanten beschreiben eine Vielzahl von Informationen zum Gerätestatus des Telefons.
ms.assetid: e94da591-49ab-4932-8621-0a62b8a55dd6
title: PHONESTATUSFLAGS_ Konstanten (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b42f8e13adfae54c56e44244d04b3961216edb87e29730fec6f689f315380a7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060648"
---
# <a name="phonestatusflags_-constants"></a>\_PHONESTATUSFLAGS-Konstanten

Die **\_ PHONESTATUSFLAGS-Bitflags-Konstanten** beschreiben eine Vielzahl von Informationen zum Gerätestatus des Telefons.

<dl> <dt>

<span id="PHONESTATUSFLAGS_CONNECTED"></span><span id="phonestatusflags_connected"></span>**PHONESTATUSFLAGS \_ VERBUNDEN**
</dt> <dd> <dl> <dt>



Gibt an, ob das Telefon derzeit mit TAPI verbunden ist. **TRUE,** wenn verbunden, **andernfalls FALSE.**


</dt> </dl> </dd> <dt>

<span id="PHONESTATUSFLAGS_SUSPENDED"></span><span id="phonestatusflags_suspended"></span>**PHONESTATUSFLAGS \_ ANGEHALTEN**
</dt> <dd> <dl> <dt>



Gibt an, ob die TapI-Manipulation des Telefongeräts angehalten wird. **TRUE,** wenn angehalten, **andernfalls FALSE.** Die Verwendung eines Telefongeräts durch eine Anwendung kann vorübergehend angehalten werden, wenn der Switch das Telefon auf eine Weise manipulieren möchte, die keine Störungen durch die Anwendung tolerieren kann.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Hinweise

Keine Erweiterbarkeit. Alle 32 Bits sind reserviert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2.0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




