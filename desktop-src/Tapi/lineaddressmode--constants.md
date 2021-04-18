---
description: Die \_ Bit-Flag-Konstanten von lineaddressmode beschreiben verschiedene Möglichkeiten, eine Adresse auf einem liniengerät zu identifizieren.
ms.assetid: f0f132a0-2e8e-478f-909b-c100aa360daa
title: LINEADDRESSMODE_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e5e926772c82a36865c7f3b95c1ca1321db5682
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372072"
---
# <a name="lineaddressmode_-constants"></a>Lineaddressmode- \_ Konstanten

Die Bit-Flag-Konstanten von **lineaddressmode \_** beschreiben verschiedene Möglichkeiten, eine Adresse auf einem liniengerät zu identifizieren.

<dl> <dt>

<span id="LINEADDRESSMODE_ADDRESSID"></span><span id="lineaddressmode_addressid"></span>**lineaddressmode \_ -adressssid**
</dt> <dd> <dl> <dt>



Die Adresse wird mit einer kleinen Ganzzahl im Bereich 0 bis *dwnumadkleider* minus 1 angegeben, wobei *dwnumadkleidungs* der Wert in den Gerätefunktionen der Linie ist.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSMODE_DIALABLEADDR"></span><span id="lineaddressmode_dialableaddr"></span>**lineaddressmode- \_ dialableaddr**
</dt> <dd> <dl> <dt>



Die Adresse wird durch die Telefonnummer angegeben.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die höherwertigen 16 Bits können für gerätespezifische Erweiterungen zugewiesen werden. Die nieder wertigen 16 Bits sind reserviert.

Diese Konstante wird verwendet, um eine Adresse in einer Zeile auszuwählen, von der ein-Befehl stammt. Das übliche Modell wählt die Adresse mithilfe des Adress Bezeichners aus. Adress Bezeichner sind der Mechanismus, mit dem die Adressen in TAPI identifiziert werden. In einigen Umgebungen ist es jedoch oft praktischer, die Ursprungsadresse eines Aufrufs anhand der Telefonnummer anstelle des Adress Bezeichners zu identifizieren. Ein Beispiel hierfür ist die Möglichkeit, eine große Anzahl von Stationen (Drittanbieter) auf dem Switch mithilfe eines einzelnen Zeilen Geräts mit vielen Adressen zu modellieren. Die Linie stellt den Satz aller Stationen dar, und jede Station wird einer Adresse mit ihrer eigenen primären Telefonnummer und Adress Kennung zugeordnet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2,0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




