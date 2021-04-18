---
description: Die linegenerateterm \_ -bitflagkonstanten beschreiben die Bedingungen, unter denen die Ziffern-oder Tongenerierung beendet wird.
ms.assetid: 5cdc43c0-2349-4ffc-9bf7-3b498b35db95
title: LINEGENERATETERM_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6804b09879471a77780a95ca4ed35b7aaa5b6e1a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371563"
---
# <a name="linegenerateterm_-constants"></a>Linegenerateterm- \_ Konstanten

Die **linegenerateterm \_** -bitflagkonstanten beschreiben die Bedingungen, unter denen die Ziffern-oder Tongenerierung beendet wird.

<dl> <dt>

<span id="LINEGENERATETERM_CANCEL"></span><span id="linegenerateterm_cancel"></span>**linegenerateterm \_ Abbrechen**
</dt> <dd> <dl> <dt>



Die Digit-oder Tone-Generierungs Anforderung wurde von dieser Anwendung, von einer anderen Anwendung oder von der Beendigung des Aufrufes abgebrochen. Dieser Wert kann auch zurückgegeben werden, wenn die Ziffern-oder Tongenerierung aufgrund eines internen Fehlers des Dienstanbieters nicht abgeschlossen werden kann.


</dt> </dl> </dd> <dt>

<span id="LINEGENERATETERM_DONE"></span><span id="linegenerateterm_done"></span>**linegenerateterm \_ abgeschlossen**
</dt> <dd> <dl> <dt>



Die angeforderte Anzahl von Ziffern oder angeforderten Tönen wurde für die angeforderte Dauer generiert.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Bemerkungen

Keine Erweiterbarkeit. Alle 32 Bits sind reserviert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2,0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




