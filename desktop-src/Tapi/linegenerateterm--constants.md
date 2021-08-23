---
description: Die \_ LINEGENERATETERM-Bitflags-Konstanten beschreiben die Bedingungen, unter denen die Ziffern- oder Tongenerierung beendet wird.
ms.assetid: 5cdc43c0-2349-4ffc-9bf7-3b498b35db95
title: LINEGENERATETERM_ Konstanten (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c34d119f503c677e5c251bb494c5ea991dbd0fccf0bfbdb3affecf4c4ff1914
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119518970"
---
# <a name="linegenerateterm_-constants"></a>LINEGENERATETERM-Konstanten \_

Die **\_ LINEGENERATETERM-Bitflagkonstitionen** beschreiben die Bedingungen, unter denen die Ziffern- oder Tongenerierung beendet wird.

<dl> <dt>

<span id="LINEGENERATETERM_CANCEL"></span><span id="linegenerateterm_cancel"></span>**LINEGENERATETERM \_ CANCEL**
</dt> <dd> <dl> <dt>



Die Anforderung zur Ziffern- oder Tongenerierung wurde von dieser Anwendung, von einer anderen Anwendung oder aufgrund des Beendeten des Aufrufs abgebrochen. Dieser Wert kann auch zurückgegeben werden, wenn die Ziffern- oder Tongenerierung aufgrund eines internen Fehlers des Dienstanbieters nicht abgeschlossen werden kann.


</dt> </dl> </dd> <dt>

<span id="LINEGENERATETERM_DONE"></span><span id="linegenerateterm_done"></span>**LINEGENERATETERM \_ DONE**
</dt> <dd> <dl> <dt>



Die angeforderte Anzahl von Ziffern oder angeforderten Tönen wurde für die angeforderte Dauer generiert.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Hinweise

Keine Erweiterbarkeit. Alle 32 Bits sind reserviert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2.0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




