---
description: Die LINEADDRESSSHARING-Bitflagkonst constants beschreiben verschiedene Möglichkeiten, wie eine \_ Adresse zwischen Zeilen gemeinsam genutzt werden kann.
ms.assetid: f37ba549-c8dc-4a7c-bfe6-8e5f733d9750
title: LINEADDRESSSHARING_ Konstanten (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4fe92c92efd75a4f6e731944c487acff2ffd70e173dd04b03244ec9d55e8aba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003128"
---
# <a name="lineaddresssharing_-constants"></a>LINEADDRESSSHARING-Konstanten \_

Die **\_ LINEADDRESSSHARING-Bitflagkonst** constants beschreiben verschiedene Möglichkeiten, wie eine Adresse zwischen Zeilen gemeinsam genutzt werden kann.

<dl> <dt>

<span id="LINEADDRESSSHARING_PRIVATE"></span><span id="lineaddresssharing_private"></span>**LINEADDRESSSHARING \_ PRIVATE**
</dt> <dd> <dl> <dt>



Die Adresse ist für die Zeile des Benutzers privat. sie ist keinen anderen Station zugewiesen.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSHARING_BRIDGEDEXCL"></span><span id="lineaddresssharing_bridgedexcl"></span>**LINEADDRESSSHARING \_ BRIDGEDEXCL**
</dt> <dd> <dl> <dt>



Die Adresse wird an eine oder mehrere andere Stationen überbrückt. Die erste Zeile zum Aktivieren eines Anrufs in der Zeile hat exklusiven Zugriff auf die Adresse und Aufrufe, die möglicherweise in ihr vorhanden sind. Andere Zeilen können die Bridged-Adresse nicht verwenden, während sie verwendet wird.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSHARING_BRIDGEDNEW"></span><span id="lineaddresssharing_bridgednew"></span>**LINEADDRESSSHARING \_ BRIDGEDNEW**
</dt> <dd> <dl> <dt>



Die Adresse wird mit einer oder mehr anderen Stationen überbrückt. Die erste Zeile zum Aktivieren eines Aufrufs in der Zeile hat exklusiven Zugriff nur auf den entsprechenden Aufruf. Andere Anwendungen, die die Adresse verwenden, führen zu neuen und separaten Aufrufen.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSHARING_BRIDGEDSHARED"></span><span id="lineaddresssharing_bridgedshared"></span>**LINEADDRESSSHARING \_ BRIDGEDSHARED**
</dt> <dd> <dl> <dt>



Die Adresse wird mit mindestens einer anderen Linie überbrückt. Alle Überbrückungs parteien können aufrufe an der Adresse teilnehmen, die dann als Konferenz fungiert.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSHARING_MONITORED"></span><span id="lineaddresssharing_monitored"></span>**LINEADDRESSSHARING \_ ÜBERWACHT**
</dt> <dd> <dl> <dt>



Dies ist eine Adresse, deren Leerlauf-/Ausgelastetstatus für diese Zeile verfügbar gemacht wird.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Hinweise

Keine Erweiterbarkeit. Alle 32 Bits sind reserviert.

Die Art und Weise, wie eine Adresse zeilenübergreifend freigegeben wird, kann sich auf das Verhalten dieser Adresse auswirken. [**LINE \_ CALLSTATE-**](line-callstate.md) und [**LINE \_ ADDRESSSTATE-Nachrichten**](line-addressstate.md) werden als Reaktion auf Aktivitäten der Bridging-Stationen an die Anwendung gesendet. Über diese Nachrichten kann eine Anwendung den Status der Adresse nachverfolgen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2.0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**LINE \_ ADDRESSSTATE**](line-addressstate.md)
</dt> <dt>

[**LINE \_ CALLSTATE**](line-callstate.md)
</dt> </dl>

 

 




