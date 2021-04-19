---
description: Die lineaddrfeature- \_ Konstanten Listen die Vorgänge auf, die für eine Adresse aufgerufen werden können.
ms.assetid: dedeee7b-578b-4b19-8b99-5cd23779d661
title: LINEADDRFEATURE_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 825902c2943806d1d495e14a0f0a5042f2949796
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366702"
---
# <a name="lineaddrfeature_-constants"></a>Lineaddrfeature- \_ Konstanten

Die **lineaddrfeature \_** -Konstanten Listen die Vorgänge auf, die für eine Adresse aufgerufen werden können.

<dl> <dt>

<span id="LINEADDRFEATURE_FORWARD"></span><span id="lineaddrfeature_forward"></span>**lineaddrfeature \_ Vorwärts**
</dt> <dd> <dl> <dt>



Die Adresse kann weitergeleitet werden.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_MAKECALL"></span><span id="lineaddrfeature_makecall"></span>**lineaddrfeature \_ MakeCall**
</dt> <dd> <dl> <dt>



Ein ausgehender Anruf kann für die Adresse platziert werden.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_PICKUP"></span><span id="lineaddrfeature_pickup"></span>**Abholung von lineaddrfeature \_**
</dt> <dd> <dl> <dt>



Ein-Rückruf kann an der Adresse abgerufen werden.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_PICKUPDIRECT"></span><span id="lineaddrfeature_pickupdirect"></span>**lineaddrfeature \_ pickupdirect**
</dt> <dd> <dl> <dt>



Die [**linepickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) -Funktion kann verwendet werden, um einen-Rückruf für eine bestimmte Adresse auszuwählen.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_PICKUPGROUP"></span><span id="lineaddrfeature_pickupgroup"></span>**"lineaddrfeature" \_ pickupgroup**
</dt> <dd> <dl> <dt>



Die [**linepickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) -Funktion kann verwendet werden, um einen-Rückruf in der Gruppe zu übernehmen.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_PICKUPHELD"></span><span id="lineaddrfeature_pickupheld"></span>**lineaddrfeature \_ pickat**
</dt> <dd> <dl> <dt>



Die [**linepickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) -Funktion (mit einer **null** -Zieladresse) kann verwendet werden, um einen für die Adresse gespeicherten-Befehl zu übernehmen. Dies wird normalerweise nur in einer überbrückten exklusiven Anordnung verwendet.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_PICKUPWAITING"></span><span id="lineaddrfeature_pickupwaiting"></span>**lineaddrfeature \_ pickupwaiting**
</dt> <dd> <dl> <dt>



Die [**linepickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) -Funktion (mit einer **null** -Zieladresse) kann verwendet werden, um einen wartenden callcallaufzurufen. Beachten Sie, dass dies nicht notwendigerweise darauf hinweist, dass ein warte Vorgang tatsächlich vorhanden ist, da es für ein Telefoniegerät oftmals nicht möglich ist, einen solchen Rückruf automatisch zu erkennen. Es zeigt jedoch an, dass die Hook-Flash-Funktion aufgerufen wird, um zu einem solchen Aufruf zu wechseln.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_SETMEDIACONTROL"></span><span id="lineaddrfeature_setmediacontrol"></span>**lineaddrfeature \_ setmediacontrol**
</dt> <dd> <dl> <dt>



Für diese Adresse kann ein mediensteuer Element festgelegt werden.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_SETTERMINAL"></span><span id="lineaddrfeature_setterminal"></span>**lineaddrfeature \_ setterminal**
</dt> <dd> <dl> <dt>



Die Terminal Modi für diese Adresse können festgelegt werden.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_SETUPCONF"></span><span id="lineaddrfeature_setupconf"></span>**lineaddrfeature \_ setupconf**
</dt> <dd> <dl> <dt>



An dieser Adresse kann ein Konferenzgespräch mit einem anfänglichen **null** -aufrufsbefehl eingerichtet werden.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_UNCOMPLETECALL"></span><span id="lineaddrfeature_uncompletecall"></span>**uncompletecallcenter für lineaddrfeature \_**
</dt> <dd> <dl> <dt>



Anforderungen zum Abrufen von Anforderungen können an dieser Adresse abgebrochen werden.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_UNPARK"></span><span id="lineaddrfeature_unpark"></span>**lineaddrfeature \_ unpark**
</dt> <dd> <dl> <dt>



Aufrufe können mithilfe dieser Adresse entparkt werden.

> [!Note]  
> Wenn keines der neuen geänderten "Pickup"-Bits im **dwaddressfeatures** -Member in [**lineaddressstatus**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) festgelegt ist, aber das Pickup-Bit "lineaddrfeature" \_ festgelegt ist, kann jeder der Pickup-Modi funktionieren. der Dienstanbieter hat einfach nicht angegeben, welche Werte verwendet werden.

 


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_FORWARDDND"></span><span id="lineaddrfeature_forwarddnd"></span>**\_weiterforwarddnd für lineaddrfeature**
</dt> <dd> <dl> <dt>



Die [**lineforward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) -Funktion (mit einer leeren Zieladresse) kann verwendet werden, um die Funktion "nicht stören" für die Adresse zu aktivieren. Lineaddrfeature \_ Forward wird ebenfalls festgelegt.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_FORWARDFWD"></span><span id="lineaddrfeature_forwardfwd"></span>**lineaddrfeature \_ forwardfwd**
</dt> <dd> <dl> <dt>



Die [**lineforward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) -Funktion kann verwendet werden, um Aufrufe an die Adresse an andere Zahlen weiterzuleiten. Lineaddrfeature \_ Forward wird ebenfalls festgelegt.

> [!Note]  
> Wenn keines der neuen geänderten "Forward"-Bits im **dwaddressfeatures** -Member in [**lineaddressstatus**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) festgelegt ist, aber das lineaddrfeature- \_ Forward-Bit festgelegt ist, kann jeder der vorwärts Modi funktionieren. der Dienstanbieter hat einfach nicht angegeben, welche Werte verwendet werden.

 


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Bemerkungen

Keine Erweiterbarkeit. Alle 32 Bits sind reserviert.

Diese Konstante wird sowohl in [**lineaddresscaps**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) (von [**linegetaddresscaps**](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps)zurückgegeben) als auch in [**lineaddressstatus**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) (zurückgegeben von [**linegetaddressstatus**](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus)) verwendet. **Lineaddresscaps** meldet die Verfügbarkeit der Adress Features durch den Dienstanbieter (hauptsächlich den Switch) für eine bestimmte Adresse. Eine Anwendung würde diese Entscheidung treffen, wenn Sie initialisiert wird. Die [**lineaddressstatus**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) -Struktur meldet für eine angegebene Adresse, welche Adress Features tatsächlich aufgerufen werden können, während sich die Adresse im aktuellen Zustand befindet. Diese Bestimmung wird von einer Anwendung nach Änderungen des Adress Zustands dynamisch durchgeführt, was in der Regel durch Aufrufe im Zusammenhang mit der Adresse verursacht wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2,0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Lineaddresscaps**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)
</dt> <dt>

[**Lineaddressstatus**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus)
</dt> <dt>

[**lineforward**](/windows/desktop/api/Tapi/nf-tapi-lineforward)
</dt> <dt>

[**linegetaddresscaps**](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps)
</dt> <dt>

[**linegetaddressstatus**](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus)
</dt> <dt>

[**linepickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup)
</dt> </dl>

 

 




