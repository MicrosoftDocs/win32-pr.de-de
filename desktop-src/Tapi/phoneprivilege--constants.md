---
description: Die \_ PHONEPRIVILEGE-Bitflagkonst constants beschreiben die verschiedenen Möglichkeiten, wie ein Telefongerät geöffnet werden kann.
ms.assetid: 1dc2fab9-b044-4ae3-8c16-fa450f9ef714
title: PHONEPRIVILEGE_ Konstanten (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae9b3f3848af8c9858522bd924ccb77d7bf1682f09b66c0cfdcb5527b93416dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117761292"
---
# <a name="phoneprivilege_-constants"></a>\_PHONEPRIVILEGE-Konstanten

Die **\_ PHONEPRIVILEGE-Bitflagkonst** constants beschreiben die verschiedenen Möglichkeiten, wie ein Telefongerät geöffnet werden kann.

<dl> <dt>

<span id="PHONEPRIVILEGE_MONITOR"></span><span id="phoneprivilege_monitor"></span>**PHONEPRIVILEGE \_ MONITOR**
</dt> <dd> <dl> <dt>



Eine Anwendung, die ein Telefongerät mit der Monitorberechtigung öffnet, wird über Ereignisse und Zustandsänderungen informiert, die auf dem Smartphone auftreten. Die Anwendung kann keine Vorgänge auf dem Telefongerät aufrufen, die ihren Zustand ändern würden, sodass nur Statusvorgänge aufgerufen werden können. Mehrere Anwendungen können ein Telefongerät jederzeit überwachen.


</dt> </dl> </dd> <dt>

<span id="PHONEPRIVILEGE_OWNER"></span><span id="phoneprivilege_owner"></span>**PHONEPRIVILEGE \_ OWNER**
</dt> <dd> <dl> <dt>



Eine Anwendung, die ein Telefongerät mit der Besitzerberechtigung öffnet, kann den Zustand der Sperre, des Ringers, der Anzeige, des Hookswitchs und der Datenblöcke des Telefons ändern. Das Öffnen eines Telefongeräts im Besitzermodus ermöglicht auch die Überwachung des Telefongeräts. Nur eine Anwendung darf zu einem bestimmten Zeitpunkt Besitzer eines Telefongeräts sein.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Hinweise

Keine Erweiterbarkeit. Alle 32 Bits sind reserviert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2.0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




