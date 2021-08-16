---
description: Die LINEANSWERMODE-Bitflagkonstanten beschreiben, wie ein vorhandener aktiver Aufruf auf einem Liniengerät durch die Beantwortung eines anderen Angebotsaufrufs in derselben \_ Zeile beeinflusst wird.
ms.assetid: 35f63d92-970f-4fb8-aba9-179fc7de70f4
title: LINEANSWERMODE_ Konstanten (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abfb9d6491864f5be8788575d718e42cc5f5c7c337fd046c110bd5bd82eae110
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117761842"
---
# <a name="lineanswermode_-constants"></a>\_LINEANSWERMODE-Konstanten

Die **LINEANSWERMODE-Bitflagkonstanten \_** beschreiben, wie ein vorhandener aktiver  Aufruf auf einem Liniengerät durch die Beantwortung eines anderen Angebotsaufrufs in derselben Zeile beeinflusst wird.

<dl> <dt>

<span id="LINEANSWERMODE_DROP"></span><span id="lineanswermode_drop"></span>**LINEANSWERMODE \_ DROP**
</dt> <dd> <dl> <dt>



Der derzeit aktive Aufruf wird automatisch gelöscht.


</dt> </dl> </dd> <dt>

<span id="LINEANSWERMODE_HOLD"></span><span id="lineanswermode_hold"></span>**LINEANSWERMODE \_ HOLD**
</dt> <dd> <dl> <dt>



Der derzeit aktive Aufruf wird automatisch zurückhalten.


</dt> </dl> </dd> <dt>

<span id="LINEANSWERMODE_NONE"></span><span id="lineanswermode_none"></span>**LINEANSWERMODE \_ NONE**
</dt> <dd> <dl> <dt>



Das Beantworten eines weiteren Aufrufs in derselben Zeile hat keine Auswirkungen auf den vorhandenen aktiven Aufruf in der Zeile.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Hinweise

Keine Erweiterbarkeit. Alle 32 Bits sind reserviert.

Wenn ein Aufruf einkommt (angeboten wird), wenn ein anderer Aufruf bereits aktiv ist, wird der neue Aufruf durch Aufrufen von [**lineAnswer mit verbunden.**](/windows/desktop/api/Tapi/nf-tapi-lineanswer) Die Auswirkungen, die dies auf den vorhandenen aktiven Aufruf hat, hängen von den Gerätefunktionen der Zeile ab. Der erste Aufruf ist möglicherweise nicht betroffen, er wird möglicherweise automatisch gelöscht, oder er wird automatisch zurück gestellt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2.0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




