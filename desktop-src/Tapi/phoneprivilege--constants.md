---
description: Die \_ Bit-Flag-Konstanten phoneprivilege beschreiben die verschiedenen Methoden, mit denen ein Telefongerät geöffnet werden kann.
ms.assetid: 1dc2fab9-b044-4ae3-8c16-fa450f9ef714
title: PHONEPRIVILEGE_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6d04c074e03d6f0b7f7a6c58e4268e0bd5057a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365857"
---
# <a name="phoneprivilege_-constants"></a>Phoneprivilege- \_ Konstanten

Die Bit-Flag-Konstanten **phoneprivilege \_** beschreiben die verschiedenen Methoden, mit denen ein Telefongerät geöffnet werden kann.

<dl> <dt>

<span id="PHONEPRIVILEGE_MONITOR"></span><span id="phoneprivilege_monitor"></span>**phoneprivilege- \_ Monitor**
</dt> <dd> <dl> <dt>



Eine Anwendung, die ein Telefongerät mit der Berechtigung überwachen öffnet, wird über Ereignisse und Zustandsänderungen informiert, die auf dem Telefon stattfinden. Die Anwendung kann keine Vorgänge auf dem Telefongerät aufrufen, die den Zustand ändern, sodass nur Status Vorgänge aufgerufen werden können. Mehrere Anwendungen können ein Telefongerät zu einem beliebigen Zeitpunkt überwachen.


</dt> </dl> </dd> <dt>

<span id="PHONEPRIVILEGE_OWNER"></span><span id="phoneprivilege_owner"></span>**phoneprivilege- \_ Besitzer**
</dt> <dd> <dl> <dt>



Eine Anwendung, die ein Telefongerät mit der Berechtigung "Besitzer" öffnet, kann den Status der Lampen, ruftys, Anzeige-, huokswitch-und Datenblöcke des Telefons ändern. Wenn Sie ein Telefongerät im Besitzer Modus öffnen, wird auch die Überwachung des Telefon Geräts ermöglicht. Es ist nur eine Anwendung berechtigt, zu einem beliebigen Zeitpunkt als Besitzer eines Telefon Geräts zu fungieren.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Bemerkungen

Keine Erweiterbarkeit. Alle 32 Bits sind reserviert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2,0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




