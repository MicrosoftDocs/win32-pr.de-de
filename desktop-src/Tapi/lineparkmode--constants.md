---
description: Die \_ Bit-Flag-Konstanten von linepark Mode beschreiben verschiedene Arten von Park aufrufen.
ms.assetid: 4b182c16-9d58-4244-bc5a-05c393800948
title: LINEPARKMODE_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ef27aaf35f86b02834c93992e8f427c54ffb903
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361632"
---
# <a name="lineparkmode_-constants"></a>Lineparkmode- \_ Konstanten

Die Bit-Flag-Konstanten von **linepark Mode \_** beschreiben verschiedene Arten von Park aufrufen.

<dl> <dt>

<span id="LINEPARKMODE_DIRECTED"></span><span id="lineparkmode_directed"></span>**lineparkmode \_ gerichtet**
</dt> <dd> <dl> <dt>



Gibt den gerichteten callpark an. Die Adresse, in der der-Befehl geparkt werden soll, muss für den Schalter angegeben werden.


</dt> </dl> </dd> <dt>

<span id="LINEPARKMODE_NONDIRECTED"></span><span id="lineparkmode_nondirected"></span>**lineparkmode \_ nicht gesteuert**
</dt> <dd> <dl> <dt>



Gibt den nicht gesteuerten callpark an. Die Adresse, in der der-Befehl geparkt ist, wird durch den-Schalter ausgewählt und vom Switch zur Anwendung bereitgestellt.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Bemerkungen

Keine Erweiterbarkeit. Alle 32 Bits sind reserviert.

Die **lineparkmode- \_ Konstanten** werden verwendet, wenn ein-Befehl durchsucht wird. Sehen Sie sich die Gerätefunktionen einer Zeile an, um herauszufinden, welcher Park Modus verfügbar ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2,0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




