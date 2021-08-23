---
description: Die \_ LINETRANSLATERESULT-Bitflagkonst constants beschreiben verschiedene Ergebnisse einer Adressübersetzung.
ms.assetid: 7b834c57-d862-4fe6-828c-9e8fa20f3ec7
title: LINETRANSLATERESULT_ Konstanten (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ba28c04bc52d3857d76bffefed5fe07803954e72f4a5e7e05ffa22d4ee6c646
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119518780"
---
# <a name="linetranslateresult_-constants"></a>\_LINETRANSLATERESULT-Konstanten

Die **\_ LINETRANSLATERESULT-Bitflags-Konstanten** beschreiben verschiedene Ergebnisse einer Adressübersetzung.

<dl> <dt>

<span id="LINETRANSLATERESULT_CANONICAL"></span><span id="linetranslateresult_canonical"></span>**LINETRANSLATERESULT \_ KANONISCH**
</dt> <dd> <dl> <dt>



Gibt an, dass die Eingabezeichenfolge ein gültiges kanonisches Format hatte.


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATERESULT_DIALBILLING"></span><span id="linetranslateresult_dialbilling"></span>**LINETRANSLATERESULT \_ DIALBILLING**
</dt> <dd> <dl> <dt>



Gibt an, dass die zurückgegebene Adresse ein "$" enthält.


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATERESULT_DIALDIALTONE"></span><span id="linetranslateresult_dialdialtone"></span>**LINETRANSLATERESULT \_ DIALDIALTONE**
</dt> <dd> <dl> <dt>



Gibt an, dass die zurückgegebene Adresse ein "W" enthält.


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATERESULT_DIALPROMPT"></span><span id="linetranslateresult_dialprompt"></span>**LINETRANSLATERESULT \_ DIALPROMPT**
</dt> <dd> <dl> <dt>



Gibt an, dass die zurückgegebene Adresse ein "?" enthält.


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATERESULT_DIALQUIET"></span><span id="linetranslateresult_dialquiet"></span>**LINETRANSLATERESULT \_ DIALQUIET**
</dt> <dd> <dl> <dt>



Gibt an, dass die zurückgegebene Adresse ein @-Zeichen enthält.


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATERESULT_INTERNATIONAL"></span><span id="linetranslateresult_international"></span>**LINETRANSLATERESULT \_ INTERNATIONAL**
</dt> <dd> <dl> <dt>



Gibt an, dass der Aufruf als internationaler Aufruf behandelt wird (der in der Zieladresse angegebene Länder- oder Regioncode ist anders als der für CurrentLocation angegebene Länder- oder **Regioncode).**


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATERESULT_INTOLLLIST"></span><span id="linetranslateresult_intolllist"></span>**LINETRANSLATERESULT \_ INTOLLLIST**
</dt> <dd> <dl> <dt>



Gibt an, dass der lokale Anruf als Fernverbindung gewählt wird, da für das Land oder die Region ein Mautaufruf gilt und das Präfix in **der TollPrefixList** von **CurrentLocation angezeigt wird.**


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATERESULT_LOCAL"></span><span id="linetranslateresult_local"></span>**LINETRANSLATERESULT \_ LOCAL**
</dt> <dd> <dl> <dt>



Gibt an, dass der Aufruf als lokaler Aufruf behandelt wird (die in der Zieladresse angegebene Landes- oder Gebietscode und Die Ortsvorwahl sind identisch mit denen, die für **CurrentLocation angegeben sind).**


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATERESULT_LONGDISTANCE"></span><span id="linetranslateresult_longdistance"></span>**LINETRANSLATERESULT \_ LONGDISTANCE**
</dt> <dd> <dl> <dt>



Gibt an, dass der Aufruf als Fernaufruf behandelt wird (der in der Zieladresse angegebene Länder- oder Regioncode ist identisch, aber die Ortsvorwahl ist anders als die für **CurrentLocation angegebene).**


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATERESULT_NOTINTOLLLIST"></span><span id="linetranslateresult_notintolllist"></span>**LINETRANSLATERESULT \_ NOTINTOLLLIST**
</dt> <dd> <dl> <dt>



Gibt an, dass das Land oder die Region Mautanrufe unterstützt, aber das Präfix nicht in **tollPrefixList** angezeigt wird, sodass der Anruf als lokaler Anruf gewählt wird. Wenn INTOLLIST und NOTINTOLLIST deaktiviert sind, unterstützt das aktuelle Land oder die aktuelle Region keine Mautpräfixe, und Benutzeroberflächenelemente im Zusammenhang mit Mautpräfixen sollten dem Benutzer nicht angezeigt werden. Wenn ein solches Bit aktiviert ist, unterstützt das Land oder die Region Mautlisten, und die zugehörigen Benutzeroberflächenelemente sollten aktiviert werden.


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATERESULT_NOTRANSLATION"></span><span id="linetranslateresult_notranslation"></span>**LINETRANSLATERESULT \_ NOTRANSLATION**
</dt> <dd> <dl> <dt>



Gibt an, dass die Adressübersetzung nicht verfügbar ist. Dieses Element wird nur für Anwendungen verfügbar gemacht, die eine TAPI-Version von 3.0 oder höher aushandeln.


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATERESULT_VOICEDETECT"></span><span id="linetranslateresult_voicedetect"></span>**LINETRANSLATERESULT \_ VOICEDETECT**
</dt> <dd> <dl> <dt>



Gibt an, dass die zurückgegebene wählbare Adresse ein ":" enthält. Dieses Element wird nur für Anwendungen verfügbar gemacht, die eine TAPI-Version von 2.0 oder höher aushandeln.

> [!Note]  
> Das Zeichen ":" (Doppelpunkt) wird der Liste der Zeichen hinzugefügt, die in eine Wählbare Zeichenfolge eingebettet und an Zieladressen übergeben werden können. Der Versuch, sie von einer Anwendung an ein Liniengerät zu übergeben, das eine API-Version vor 2.0 unterstützt, führt höchstwahrscheinlich dazu, dass LINEERR INVALADDRESS oder möglicherweise das Zeichen vollständig ignoriert \_ wird. Die Bedeutung dieses Zeichens ist "Pause until a voice prompt is detected, then continue dialing"; Sie ist für die Verwendung bei der automatischen Einwahl in Systeme vorgesehen, die Sprachanrufe geben, z. B. Bei Kartenprozessoren mit langen Entfernungen.

 


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Hinweise

Keine Erweiterbarkeit. Alle 32 Bits sind reserviert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2.0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




