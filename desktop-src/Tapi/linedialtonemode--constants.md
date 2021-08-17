---
description: Die \_ LINEDIALTONEMODE-Bitflagkonst constants beschreiben verschiedene Arten von Tönen. Ein spezieller Wählton hat in der Regel eine besondere Bedeutung (wie bei wartenden Nachrichten).
ms.assetid: 0b040482-35cf-42e8-84bc-33002635b591
title: LINEDIALTONEMODE_ Konstanten (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6b51ac15da6c1cba2b1b4e5b51710f04ba54549d2e08f4e9b50a20c543c305d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119309960"
---
# <a name="linedialtonemode_-constants"></a>LINEDIALTONEMODE-Konstanten \_

Die **\_ LINEDIALTONEMODE-Bitflagkonst** constants beschreiben verschiedene Arten von Tönen. Ein spezieller Wählton hat in der Regel eine besondere Bedeutung (wie bei wartenden Nachrichten).

<dl> <dt>

<span id="LINEDIALTONEMODE_EXTERNAL"></span><span id="linedialtonemode_external"></span>**LINEDIALTONEMODE \_ EXTERNAL**
</dt> <dd> <dl> <dt>



Dies ist ein externer Wählton (öffentliches Netzwerk).


</dt> </dl> </dd> <dt>

<span id="LINEDIALTONEMODE_INTERNAL"></span><span id="linedialtonemode_internal"></span>**LINEDIALTONEMODE \_ INTERNAL**
</dt> <dd> <dl> <dt>



Dies ist ein interner Wählton, wie in einer PBX.


</dt> </dl> </dd> <dt>

<span id="LINEDIALTONEMODE_NORMAL"></span><span id="linedialtonemode_normal"></span>**LINEDIALTONEMODE \_ NORMAL**
</dt> <dd> <dl> <dt>



Dies ist ein normaler Wählton, bei dem es sich in der Regel um einen kontinuierlichen Ton handelt.


</dt> </dl> </dd> <dt>

<span id="LINEDIALTONEMODE_SPECIAL"></span><span id="linedialtonemode_special"></span>**LINEDIALTONEMODE \_ SPECIAL**
</dt> <dd> <dl> <dt>



Dies ist ein spezieller Wählton, der angibt, dass eine bestimmte Bedingung (die vom Switch oder Netzwerk bekannt ist) derzeit in Kraft ist. Spezielle Wählfarben verwenden in der Regel einen unterbrochenen Ton. Wie bei einem normalen Wählton gibt dies an, dass der Schalter bereit ist, die zu wählende Nummer zu empfangen.


</dt> </dl> </dd> <dt>

<span id="LINEDIALTONEMODE_UNAVAIL"></span><span id="linedialtonemode_unavail"></span>**LINEDIALTONEMODE \_ UNAVAIL**
</dt> <dd> <dl> <dt>



Der Wähltonmodus ist nicht verfügbar und wird nicht bekannt.


</dt> </dl> </dd> <dt>

<span id="LINEDIALTONEMODE_UNKNOWN"></span><span id="linedialtonemode_unknown"></span>**LINEDIALTONEMODE \_ UNKNOWN**
</dt> <dd> <dl> <dt>



Der Dial-Tonmodus ist derzeit nicht bekannt, kann aber später bekannt werden.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Hinweise

Die hochwertigen 16 Bits können für gerätespezifische Erweiterungen zugewiesen werden. Die niedrigen 16 Bits sind reserviert.

Die **LINEDIALTONEMODE-Konstanten \_** werden innerhalb der [**LINECALLSTATUS-Datenstruktur**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) für einen Aufruf im Dialtone-Zustand verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2.0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




