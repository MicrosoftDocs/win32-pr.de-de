---
description: Die lineaddresssharing \_ -Bitflag-Konstanten beschreiben verschiedene Methoden, mit denen eine Adresse zwischen Zeilen gemeinsam genutzt werden kann.
ms.assetid: f37ba549-c8dc-4a7c-bfe6-8e5f733d9750
title: LINEADDRESSSHARING_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 785c7e924ffc958d3fe14b739bb2eb28dec322a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359387"
---
# <a name="lineaddresssharing_-constants"></a>Lineaddresssharing- \_ Konstanten

Die **lineaddresssharing \_** -Bitflag-Konstanten beschreiben verschiedene Methoden, mit denen eine Adresse zwischen Zeilen gemeinsam genutzt werden kann.

<dl> <dt>

<span id="LINEADDRESSSHARING_PRIVATE"></span><span id="lineaddresssharing_private"></span>**lineaddresssharing \_ Privat**
</dt> <dd> <dl> <dt>



Die Adresse ist für die Zeile des Benutzers privat. Sie ist keiner anderen Station zugewiesen.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSHARING_BRIDGEDEXCL"></span><span id="lineaddresssharing_bridgedexcl"></span>**lineaddresssharing \_ bridgedexcl**
</dt> <dd> <dl> <dt>



Die Adresse wird an eine oder mehrere andere Stationen überbrückt. Die erste Zeile zum Aktivieren eines Aufrufs in der Zeile hat exklusiven Zugriff auf die Adresse und die Aufrufe, die möglicherweise vorhanden sind. Andere Zeilen sind nicht in der Lage, die überbrückt Adresse zu verwenden, während Sie verwendet wird.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSHARING_BRIDGEDNEW"></span><span id="lineaddresssharing_bridgednew"></span>**lineaddresssharing \_ bridgednew**
</dt> <dd> <dl> <dt>



Die Adresse wird mit einer oder mehreren anderen Stationen überbrückt. Die erste Zeile zum Aktivieren eines Aufrufes in der Zeile hat exklusiven Zugriff auf den entsprechenden-Befehl. Andere Anwendungen, die die Adresse verwenden, führen zu neuen und separaten aufrufungen.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSHARING_BRIDGEDSHARED"></span><span id="lineaddresssharing_bridgedshared"></span>**lineaddresssharing \_ bridgedshared**
</dt> <dd> <dl> <dt>



Die Adresse wird durch eine oder mehrere andere Zeilen überbrückt. Alle überbrückten Parteien können Aufrufe für die Adresse freigeben, die dann als Konferenz fungiert.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSHARING_MONITORED"></span><span id="lineaddresssharing_monitored"></span>**überwachte lineaddresssharing \_**
</dt> <dd> <dl> <dt>



Dabei handelt es sich um eine Adresse, deren Status im Leerlauf/ausgelastet für diese Zeile verfügbar gemacht wird.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Bemerkungen

Keine Erweiterbarkeit. Alle 32 Bits sind reserviert.

Die Art und Weise, in der eine Adresse Zeilen übergreifend freigegeben wird, kann sich auf das Verhalten dieser Adresse auswirken. [**Zeile \_ CallState**](line-callstate.md) -und [**line \_ addressstate**](line-addressstate.md) -Meldungen werden als Reaktion auf Aktivitäten durch die Bridging-Stationen an die Anwendung gesendet. In diesen Nachrichten kann eine Anwendung den Status der Adresse nachverfolgen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2,0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Zeile \_ addressstate**](line-addressstate.md)
</dt> <dt>

[**\_liniencallstate**](line-callstate.md)
</dt> </dl>

 

 




