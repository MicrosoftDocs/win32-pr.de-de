---
description: Die linelocationoption- \_ Konstanten definieren Werte, die im dwOptions-Member der linelocationentry-Struktur verwendet werden, die als Teil der linetranslatecaps-Struktur zurückgegeben wird, die von linegettranslatecaps zurückgegeben wurde.
ms.assetid: 3b185c16-2535-4a90-855b-29e52828ea4c
title: LINELOCATIONOPTION_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f60398953d2f809e29a78323e3b1dedfcac7a1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372653"
---
# <a name="linelocationoption_-constants"></a>Linelocationoption- \_ Konstanten

Die **linelocationoption \_** -Konstanten definieren Werte, die im **dwOptions** -Member der [**linelocationentry**](/windows/desktop/api/Tapi/ns-tapi-linelocationentry) -Struktur verwendet werden, die als Teil der [**linetranslatecaps**](/windows/desktop/api/Tapi/ns-tapi-linetranslatecaps) -Struktur zurückgegeben wird, die von [**linegettranslatecaps**](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps)zurückgegeben wurde.

<dl> <dt>

<span id="LINELOCATIONOPTION_PULSEDIAL"></span><span id="linelocationoption_pulsedial"></span>**linelocationoption \_ Pull Dial**
</dt> <dd> <dl> <dt>



Der standardmäßige Wähl Modus an diesem Speicherort ist Pulse Wähl. Wenn dieses Bit festgelegt ist, fügt [**linetranslateaddress**](/windows/desktop/api/Tapi/nf-tapi-linetranslateaddress) einen "P"-Wähl Modifizierer an den Anfang der als DFÜ-Zeichenfolge zurückgegebenen Zeichenfolge ein, wenn dieser Speicherort ausgewählt wird. Wenn dieses Bit nicht festgelegt ist, fügt **linetranslateaddress** einen "T"-wählmodifizierer am Anfang der DFÜ-Zeichenfolge ein.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Bemerkungen

Nicht erweiterbar. Alle 32 Bits sind reserviert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2,0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




