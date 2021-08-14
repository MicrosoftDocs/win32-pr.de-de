---
description: Die \_ LINETONEMODE-Konstanten beschreiben verschiedene Auswahlen, die beim Generieren von Linienfarben verwendet werden.
ms.assetid: 7bfc7d4e-2ab3-44ec-a936-f2d7dcfce263
title: LINETONEMODE_ Konstanten (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 268d8a20d9cceaad732b3ef99cf8a8e7a3c4e7de4d841feff07f0b606cf4d314
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119404910"
---
# <a name="linetonemode_-constants"></a>\_LINETONEMODE-Konstanten

Die **\_ LINETONEMODE-Konstanten** beschreiben verschiedene Auswahlen, die beim Generieren von Linienfarben verwendet werden.

<dl> <dt>

<span id="LINETONEMODE_BEEP"></span><span id="linetonemode_beep"></span>**LINETONEMODE \_ BEEP**
</dt> <dd> <dl> <dt>



Der Ton ist ein Signalton, der z. B. verwendet wird, um den Anfang einer Aufzeichnung ankündigen. Die genaue Definition ist vom Dienstanbieter definiert.


</dt> </dl> </dd> <dt>

<span id="LINETONEMODE_BILLING"></span><span id="linetonemode_billing"></span>**\_LINETONEMODE-ABRECHNUNG**
</dt> <dd> <dl> <dt>



Der Ton ist ein Tonfall für Abrechnungsinformationen, z. B. ein Kreditkarten-Eingabeaufforderungston. Die genaue Definition ist vom Dienstanbieter definiert.


</dt> </dl> </dd> <dt>

<span id="LINETONEMODE_BUSY"></span><span id="linetonemode_busy"></span>**LINETONEMODE \_ AUSGELASTET**
</dt> <dd> <dl> <dt>



Der Ton ist ein starker Ton. Die genaue Definition ist vom Dienstanbieter definiert.


</dt> </dl> </dd> <dt>

<span id="LINETONEMODE_CUSTOM"></span><span id="linetonemode_custom"></span>**LINETONEMODE \_ CUSTOM**
</dt> <dd> <dl> <dt>



Der Ton ist ein benutzerdefinierter Ton, der durch seine Komponentenhäufigkeiten vom Typ [**LINEGENERATETONE definiert wird.**](/windows/desktop/api/Tapi/ns-tapi-linegeneratetone)


</dt> </dl> </dd> <dt>

<span id="LINETONEMODE_RINGBACK"></span><span id="linetonemode_ringback"></span>**LINETONEMODE \_ RINGBACK**
</dt> <dd> <dl> <dt>



Der Ton ist der Ringbackton. Die genaue Definition ist vom Dienstanbieter definiert.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Hinweise

Die hochwertigen 16 Bits können für gerätespezifische Erweiterungen zugewiesen werden. Die niedrigen 16 Bits sind reserviert.

Diese Konstanten werden verwendet, um Töne zu definieren, die inband über einen Aufruf der Remoteparty generiert werden sollen. Beachten Sie, dass die Tonerkennung von nicht benutzerdefinierten Tönen diese Konstanten nicht verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2.0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




