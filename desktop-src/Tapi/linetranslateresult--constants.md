---
description: Die linetranslateresult \_ -bitflagkonstanten beschreiben verschiedene Ergebnisse einer Adressübersetzung.
ms.assetid: 7b834c57-d862-4fe6-828c-9e8fa20f3ec7
title: LINETRANSLATERESULT_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aad10c3da2b4250ded5706e4aaa10b9b61f8739b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354829"
---
# <a name="linetranslateresult_-constants"></a>Linetranslateresult- \_ Konstanten

Die **linetranslateresult \_** -bitflagkonstanten beschreiben verschiedene Ergebnisse einer Adressübersetzung.

<dl> <dt>

<span id="LINETRANSLATERESULT_CANONICAL"></span><span id="linetranslateresult_canonical"></span>**linetranslateresult \_ Canonical**
</dt> <dd> <dl> <dt>



Gibt an, dass die Eingabe Zeichenfolge ein gültiges kanonisches Format hat.


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATERESULT_DIALBILLING"></span><span id="linetranslateresult_dialbilling"></span>**linetranslateresult \_ dialbilling**
</dt> <dd> <dl> <dt>



Gibt an, dass die zurückgegebene Adresse ein "$" enthält.


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATERESULT_DIALDIALTONE"></span><span id="linetranslateresult_dialdialtone"></span>**linetranslateresult \_ dialdialtone**
</dt> <dd> <dl> <dt>



Gibt an, dass die zurückgegebene Adresse ein "W" enthält.


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATERESULT_DIALPROMPT"></span><span id="linetranslateresult_dialprompt"></span>**linetranslateresult- \_ dialprompt**
</dt> <dd> <dl> <dt>



Gibt an, dass die zurückgegebene Adresse ein "?" enthält.


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATERESULT_DIALQUIET"></span><span id="linetranslateresult_dialquiet"></span>**linetranslateresult \_ dialquiet**
</dt> <dd> <dl> <dt>



Gibt an, dass die zurückgegebene Adresse ein @-Zeichen enthält.


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATERESULT_INTERNATIONAL"></span><span id="linetranslateresult_international"></span>**linetranslateresult \_ International**
</dt> <dd> <dl> <dt>



Gibt an, dass der-Befehl als internationaler-Rückruf behandelt wird (der in der Zieladresse angegebene Landes-oder Regions Code unterscheidet sich von dem für **currentlocation** angegebenen Länder-oder Regions Code).


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATERESULT_INTOLLLIST"></span><span id="linetranslateresult_intolllist"></span>**linetranslateresult \_ intolllist**
</dt> <dd> <dl> <dt>



Gibt an, dass der lokale Aufruf als lange Distanz gewählt wird, da für das Land oder die Region Maut Anrufe festgestellt werden und das Präfix in der **tollprefixlist** von **currentlocation** angezeigt wird.


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATERESULT_LOCAL"></span><span id="linetranslateresult_local"></span>**linetranslateresult \_ lokal**
</dt> <dd> <dl> <dt>



Gibt an, dass der-Befehl als lokaler-Befehl behandelt wird (Land-oder Regions Code und in der Zieladresse angegebener Bereichs Code entsprechen denen, die für **currentlocation** angegeben sind).


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATERESULT_LONGDISTANCE"></span><span id="linetranslateresult_longdistance"></span>**linetranslateresult \_ Longdistance**
</dt> <dd> <dl> <dt>



Gibt an, dass der-Befehl als langer Entfernungs Rückruf behandelt wird (der in der Zieladresse angegebene Landes-oder Regions Code ist identisch, aber der flächencode unterscheidet sich von dem, der für **currentlocation** angegeben ist).


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATERESULT_NOTINTOLLLIST"></span><span id="linetranslateresult_notintolllist"></span>**linetranslateresult \_ notintolllist**
</dt> <dd> <dl> <dt>



Gibt an, dass das Land oder die Region Maut Anrufe unterstützt, das Präfix aber nicht in der **tollprefixlist** angezeigt wird, sodass der Aufruf als lokaler Aufruf gewählt wird. Beachten Sie Folgendes: Wenn sowohl intollist als auch notintollist deaktiviert sind, unterstützt das aktuelle Land oder die Region keine Maut Präfixe, und Benutzeroberflächen Elemente im Zusammenhang mit Maut Präfixen sollten dem Benutzer nicht angezeigt werden. Wenn ein solches Bit aktiviert ist, unterstützt das Land oder die Region Maut Listen, und die zugehörigen Benutzeroberflächen Elemente sollten aktiviert werden.


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATERESULT_NOTRANSLATION"></span><span id="linetranslateresult_notranslation"></span>**linetranslateresult \_ notranslation**
</dt> <dd> <dl> <dt>



Gibt an, dass die Adressübersetzung nicht verfügbar ist. Dieses Element ist nur für Anwendungen verfügbar, die eine TAPI-Version von 3,0 oder höher aushandeln.


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATERESULT_VOICEDETECT"></span><span id="linetranslateresult_voicedetect"></span>**linetranslateresult \_ voicedetect**
</dt> <dd> <dl> <dt>



Gibt an, dass die zurückgegebene, als nicht zulässig angegebene Adresse ein ":" enthält. Dieses Element ist nur für Anwendungen verfügbar, die eine TAPI-Version von 2,0 oder höher aushandeln.

> [!Note]  
> Das Zeichen ":" (Doppelpunkt) wird der Liste der Zeichen hinzugefügt, die in eine ddable-Zeichenfolge eingebettet und an Zieladressen übermittelt werden können. Der Versuch, es von einer Anwendung an ein Line-Gerät zu übergeben, das eine API-Version vor 2,0 unterstützt, führt wahrscheinlich zu lineerr \_ invaladdress oder möglicherweise in dem Zeichen, das vollständig ignoriert wird. Die Bedeutung dieses Zeichens ist "anhalten, bis eine Spracheingabe Aufforderung erkannt wird. Es ist für die Verwendung bei der automatischen Wahl von Systemen vorgesehen, die Spracheingabe Aufforderungen wie z. b. lange Entfernungs Karten Prozessoren zur Verfügung stehen.

 


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Bemerkungen

Keine Erweiterbarkeit. Alle 32 Bits sind reserviert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2,0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




