---
description: Die \_ LINESPECIALINFO-Bitflagkonstanten beschreiben spezielle Informationssignale, mit denen das Netzwerk verschiedene Berichts- und Netzwerküberwachungsvorgänge melden kann.
ms.assetid: b94f8a6f-b84d-4976-b4d4-10dee5a1a4d8
title: LINESPECIALINFO_ Konstanten (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1585146040db4392a271f5095420eee61f9873906443b58198676de806cb37f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002978"
---
# <a name="linespecialinfo_-constants"></a>\_LINESPECIALINFO-Konstanten

Die **\_ LINESPECIALINFO-Bitflagkonstanten** beschreiben spezielle Informationssignale, die das Netzwerk verwenden kann, um verschiedene Berichts- und Netzwerküberwachungsvorgänge zu melden. Dabei handelt es sich um spezielle codierte Tonsequenzen, die zu Beginn der aufgezeichneten Ankündigungen der Netzwerkempfehlung übertragen werden.

<dl> <dt>

<span id="LINESPECIALINFO_CUSTIRREG"></span><span id="linespecialinfo_custirreg"></span>**LINESPECIALINFO \_ CUSTIRREG**
</dt> <dd> <dl> <dt>



Dieser spezielle Informationston steht vor einer Nummernänderungsnummer, EINEM BER, einer Centrex-Nummeränderung und einer Nichtarbeitsstation, einem Nichtwahl- oder Einwählcode oder einer manuellen Abfangoperatornachricht (Kundensanfälligkeitskategorie). LINESPECIALINFO \_ CUSTIRREG wird auch gemeldet, wenn Abrechnungsinformationen abgelehnt werden und die gewählte Adresse beim Switch blockiert wird.


</dt> </dl> </dd> <dt>

<span id="LINESPECIALINFO_NOCIRCUIT"></span><span id="linespecialinfo_nocircuit"></span>**LINESPECIALINFO \_ NOCIRCUIT**
</dt> <dd> <dl> <dt>



Dieser spezielle Informationston steht vor einer No Circuit oder einer Notfallankündigung (Trunkblockierungskategorie).


</dt> </dl> </dd> <dt>

<span id="LINESPECIALINFO_REORDER"></span><span id="linespecialinfo_reorder"></span>**LINESPECIALINFO \_ REORDER**
</dt> <dd> <dl> <dt>



Dieser spezielle Informationston steht vor einer Ankündigung zur Neuanordnung (Kategorie "Gerätedezialität"). LINESPECIALINFO \_ REORDER wird auch gemeldet, wenn das Telefon zu lange ausgeschaltet wird.


</dt> </dl> </dd> <dt>

<span id="LINESPECIALINFO_UNAVAIL"></span><span id="linespecialinfo_unavail"></span>**LINESPECIALINFO \_ UNAVAIL**
</dt> <dd> <dl> <dt>



Details zum Ton der speziellen Informationen sind nicht verfügbar und werden nicht bekannt.


</dt> </dl> </dd> <dt>

<span id="LINESPECIALINFO_UNKNOWN"></span><span id="linespecialinfo_unknown"></span>**LINESPECIALINFO \_ UNKNOWN**
</dt> <dd> <dl> <dt>



Details zum Ton der speziellen Informationen sind derzeit unbekannt, können aber später bekannt werden.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Hinweise

Die 16 Bits mit hoher Ordnung können für gerätespezifische Erweiterungen zugewiesen werden. Die niedrigen 16 Bits sind reserviert.

Spezielle Informationstons werden für Beratungsmeldungen definiert und normalerweise nicht für Abrechnungs- oder Überwachungszwecken verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2.0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




