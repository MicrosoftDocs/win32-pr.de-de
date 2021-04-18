---
description: Die linefeature- \_ Konstanten Listen die Vorgänge auf, die mithilfe dieser API in einer Zeile aufgerufen werden können.
ms.assetid: 77fa313c-e720-4607-b691-51b5be76ceed
title: LINEFEATURE_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7eac930123a10f401a7a79de8ccf6c61452df05
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365828"
---
# <a name="linefeature_-constants"></a>Linefeature- \_ Konstanten

Die **linefeature- \_ Konstanten** Listen die Vorgänge auf, die mithilfe dieser API in einer Zeile aufgerufen werden können.

<dl> <dt>

<span id="LINEFEATURE_DEVSPECIFIC"></span><span id="linefeature_devspecific"></span>**linefeature \_ DevSpecific**
</dt> <dd> <dl> <dt>



Gerätespezifische Vorgänge können in der Zeile verwendet werden.


</dt> </dl> </dd> <dt>

<span id="LINEFEATURE_DEVSPECIFICFEAT"></span><span id="linefeature_devspecificfeat"></span>**linefeature \_ devspecificfeat**
</dt> <dd> <dl> <dt>



Gerätespezifische Features können in der Zeile verwendet werden.


</dt> </dl> </dd> <dt>

<span id="LINEFEATURE_FORWARD"></span><span id="linefeature_forward"></span>**linefeature \_ Vorwärts**
</dt> <dd> <dl> <dt>



Die Weiterleitung aller Adressen kann in der Zeile verwendet werden.


</dt> </dl> </dd> <dt>

<span id="LINEFEATURE_FORWARDDND"></span><span id="linefeature_forwarddnd"></span>**linefeature \_ forwarddnd**
</dt> <dd> <dl> <dt>



Die [**lineforward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) -Funktion (mit einer leeren Zieladresse) kann verwendet werden, um die Funktion "nicht stören" für alle Adressen in der Zeile zu aktivieren. Linefeature \_ Forward wird ebenfalls festgelegt. Dieses Flag ist nur für Anwendungen verfügbar, die eine TAPI-Version von 2,0 oder höher aushandeln.


</dt> </dl> </dd> <dt>

<span id="LINEFEATURE_FORWARDFWD"></span><span id="linefeature_forwardfwd"></span>**linefeature \_ forwardfwd**
</dt> <dd> <dl> <dt>



Die [**lineforward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) -Funktion kann verwendet werden, um Aufrufe an allen Adressen an der Zeile an andere Zahlen weiterzuleiten. Linefeature \_ Forward wird ebenfalls festgelegt. Dieses Flag ist nur für Anwendungen verfügbar, die eine TAPI-Version von 2,0 oder höher aushandeln.


</dt> </dl> </dd> <dt>

<span id="LINEFEATURE_MAKECALL"></span><span id="linefeature_makecall"></span>**linefeature \_ MakeCall**
</dt> <dd> <dl> <dt>



Ein ausgehender Anruf kann mithilfe einer nicht angegebenen Adresse in dieser Zeile platziert werden.


</dt> </dl> </dd> <dt>

<span id="LINEFEATURE_SETDEVSTATUS"></span><span id="linefeature_setdevstatus"></span>**linefeature \_ setdevstatus**
</dt> <dd> <dl> <dt>



Die [**linesetlinedevstatus**](/windows/desktop/api/Tapi/nf-tapi-linesetlinedevstatus) -Funktion kann auf dem liniengerät aufgerufen werden. Dieses Flag ist nur für Anwendungen verfügbar, die eine TAPI-Version von 2,0 oder höher aushandeln.


</dt> </dl> </dd> <dt>

<span id="LINEFEATURE_SETMEDIACONTROL"></span><span id="linefeature_setmediacontrol"></span>**linefeature \_ setmediacontrol**
</dt> <dd> <dl> <dt>



Ein mediensteuer Element kann in dieser Zeile festgelegt werden.


</dt> </dl> </dd> <dt>

<span id="LINEFEATURE_SETTERMINAL"></span><span id="linefeature_setterminal"></span>**linefeature \_ setterminal**
</dt> <dd> <dl> <dt>



Terminal Modi für diese Zeile können festgelegt werden.

> [!Note]  
> Wenn keines der neuen geänderten "Forward"-Bits im **dwlinefeatures** -Member in [**linedevstatus**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) festgelegt ist, aber das linefeature- \_ Forward-Bit festgelegt ist, kann jeder der vorwärts Modi funktionieren. der Dienstanbieter hat einfach nicht angegeben, welche Werte verwendet werden.

 


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Bemerkungen

Keine Erweiterbarkeit. Alle 32 Bits sind reserviert.

Die linefeature- \_ Konstanten werden in [**linedevstatus**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) verwendet (von [**linegetlinedevstatus**](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus)zurückgegeben). [**Linedevstatus**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) -Berichte für eine bestimmte Zeile, welche Zeilen Features tatsächlich aufgerufen werden können, während sich die Zeile im aktuellen Zustand befindet. Eine Anwendung würde diese Bestimmung nach Zeilen Statusänderungen dynamisch machen, was in der Regel durch Adressen-oder aufrufaktivitäten in der Zeile verursacht wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2,0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Linedevstatus**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus)
</dt> <dt>

[**lineforward**](/windows/desktop/api/Tapi/nf-tapi-lineforward)
</dt> <dt>

[**linegetlinedevstatus**](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus)
</dt> <dt>

[**linesetlinedevstatus**](/windows/desktop/api/Tapi/nf-tapi-linesetlinedevstatus)
</dt> </dl>

 

 




