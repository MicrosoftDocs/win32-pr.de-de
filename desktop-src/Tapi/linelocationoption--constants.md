---
description: Die LINELOCATIONOPTION-Konstanten definieren Werte, die im dwOptions-Member der LINELOCATIONENTRY-Struktur verwendet werden, die als Teil der LINETRANSLATECAPS-Struktur zurückgegeben wird, die von \_ lineGetTranslateCaps zurückgegeben wird.
ms.assetid: 3b185c16-2535-4a90-855b-29e52828ea4c
title: LINELOCATIONOPTION_ Konstanten (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c45de77a6d887b6fb0c5fa0e45e7005a621aa10ca44cc3218078eea74d00a2fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003048"
---
# <a name="linelocationoption_-constants"></a>\_LINELOCATIONOPTION-Konstanten

Die **\_ LINELOCATIONOPTION-Konstanten** definieren Werte, die im **dwOptions-Member** der [**LINELOCATIONENTRY-Struktur**](/windows/desktop/api/Tapi/ns-tapi-linelocationentry) verwendet werden, die als Teil der [**LINETRANSLATECAPS-Struktur**](/windows/desktop/api/Tapi/ns-tapi-linetranslatecaps) zurückgegeben wird, die von [**lineGetTranslateCaps**](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps)zurückgegeben wird.

<dl> <dt>

<span id="LINELOCATIONOPTION_PULSEDIAL"></span><span id="linelocationoption_pulsedial"></span>**LINELOCATIONOPTION \_ PULSEDIAL**
</dt> <dd> <dl> <dt>



Der Standardwählmodus an diesem Standort ist Pulse Dialing. Wenn dieses Bit festgelegt ist, fügt [**lineTranslateAddress**](/windows/desktop/api/Tapi/nf-tapi-linetranslateaddress) einen "P"-Wählmodifizierer am Anfang der Wählbaren Zeichenfolge ein, die bei Auswahl dieses Standorts zurückgegeben wird. Wenn dieses Bit nicht festgelegt ist, fügt **lineTranslateAddress** den Wählmodifizierer "T" am Anfang der Wählzeichenfolge ein.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Hinweise

Nicht erweiterbar. Alle 32 Bits sind reserviert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2.0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




