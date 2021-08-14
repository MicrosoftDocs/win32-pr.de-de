---
description: Die \_ LINEADDRESSMODE-Bitflagkonstanten beschreiben verschiedene Methoden zum Identifizieren einer Adresse auf einem Zeilengerät.
ms.assetid: f0f132a0-2e8e-478f-909b-c100aa360daa
title: LINEADDRESSMODE_ Konstanten (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4863b79c4527395f6ecb2d28c4d9ef718ff5a7fd99681185ba892bac2b4639ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117761862"
---
# <a name="lineaddressmode_-constants"></a>LINEADDRESSMODE-Konstanten \_

Die **\_ LINEADDRESSMODE-Bitflagkonstanten** beschreiben verschiedene Methoden zum Identifizieren einer Adresse auf einem Zeilengerät.

<dl> <dt>

<span id="LINEADDRESSMODE_ADDRESSID"></span><span id="lineaddressmode_addressid"></span>**LINEADDRESSMODE \_ ADDRESSID**
</dt> <dd> <dl> <dt>



Die Adresse wird mit einer kleinen ganzen Zahl im Bereich von 0 bis *dwNumAddresses* minus 1 angegeben, wobei *dwNumAddresses* der Wert in den Gerätefunktionen der Zeile ist.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSMODE_DIALABLEADDR"></span><span id="lineaddressmode_dialableaddr"></span>**LINEADDRESSMODE \_ DIALABLEADDR**
</dt> <dd> <dl> <dt>



Die Adresse wird über ihre Telefonnummer angegeben.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Hinweise

Die 16 Bits mit hoher Ordnung können für gerätespezifische Erweiterungen zugewiesen werden. Die niedrigen 16 Bits sind reserviert.

Diese Konstante wird verwendet, um eine Adresse in einer Zeile auszuwählen, aus der ein Aufruf stammen soll. Das übliche Modell wählt die Adresse anhand seines Adressbezeichners aus. Adressbezeichner sind der Mechanismus, der zum Identifizieren von Adressen in TAPI verwendet wird. In einigen Umgebungen ist es jedoch häufig praktischer, bei einem Anruf die Ursprungsadresse eines Anrufs anhand der Telefonnummer und nicht anhand der Adress-ID zu identifizieren. Ein Beispiel hierfür ist die mögliche Modellierung einer großen Anzahl von Stationen (Drittanbieter) auf dem Switch mithilfe eines Zeilengeräts mit vielen Adressen. Die Linie stellt den Satz aller Stationen dar, und jede Station wird einer Adresse mit eigener primärer Telefonnummer und Adress-ID zugeordnet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2.0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




