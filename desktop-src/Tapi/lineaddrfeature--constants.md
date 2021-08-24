---
description: Die LINEADDRFEATURE-Konstanten listen die Vorgänge \_ auf, die für eine Adresse aufgerufen werden können.
ms.assetid: dedeee7b-578b-4b19-8b99-5cd23779d661
title: LINEADDRFEATURE_ Konstanten (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bb545bdf0195d9fd8ed35833150b9cfd1f6b10bfbd3d1ead7e8ebff65c93132
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119682219"
---
# <a name="lineaddrfeature_-constants"></a>LINEADDRFEATURE-Konstanten \_

Die **LINEADDRFEATURE-Konstanten \_** listen die Vorgänge auf, die für eine Adresse aufgerufen werden können.

<dl> <dt>

<span id="LINEADDRFEATURE_FORWARD"></span><span id="lineaddrfeature_forward"></span>**LINEADDRFEATURE \_ FORWARD**
</dt> <dd> <dl> <dt>



Die Adresse kann weitergeleitet werden.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_MAKECALL"></span><span id="lineaddrfeature_makecall"></span>**LINEADDRFEATURE \_ MAKECALL**
</dt> <dd> <dl> <dt>



Für die Adresse kann ein ausgehender Anruf platziert werden.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_PICKUP"></span><span id="lineaddrfeature_pickup"></span>**LINEADDRFEATURE \_ PICKUP**
</dt> <dd> <dl> <dt>



Ein Anruf kann unter der Adresse verwendet werden.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_PICKUPDIRECT"></span><span id="lineaddrfeature_pickupdirect"></span>**LINEADDRFEATURE \_ PICKUPDIRECT**
</dt> <dd> <dl> <dt>



Die [**linePickup-Funktion**](/windows/desktop/api/Tapi/nf-tapi-linepickup) kann verwendet werden, um einen Aufruf für eine bestimmte Adresse zu verwenden.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_PICKUPGROUP"></span><span id="lineaddrfeature_pickupgroup"></span>**LINEADDRFEATURE \_ PICKUPGROUP**
</dt> <dd> <dl> <dt>



Die [**linePickup-Funktion**](/windows/desktop/api/Tapi/nf-tapi-linepickup) kann verwendet werden, um einen Aufruf in der Gruppe zu verwenden.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_PICKUPHELD"></span><span id="lineaddrfeature_pickupheld"></span>**LINEADDRFEATURE \_ PICKUPER**
</dt> <dd> <dl> <dt>



Die [**linePickup-Funktion**](/windows/desktop/api/Tapi/nf-tapi-linepickup) (mit einer NULL-Zieladresse) kann verwendet werden, um einen Aufruf zu verwenden, der für die Adresse gehalten wird.  Dies wird normalerweise nur in einer exklusiven Bridged-Anordnung verwendet.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_PICKUPWAITING"></span><span id="lineaddrfeature_pickupwaiting"></span>**LINEADDRFEATURE \_ PICKUPWAITING**
</dt> <dd> <dl> <dt>



Die [**linePickup-Funktion**](/windows/desktop/api/Tapi/nf-tapi-linepickup) (mit einer **NULL-Zieladresse)** kann verwendet werden, um einen anrufwartenden Aufruf zu verwenden. Beachten Sie, dass dies nicht unbedingt darauf hinweist, dass tatsächlich ein wartender Anruf vorhanden ist, da es für ein Telefoniegerät oft nicht möglich ist, einen solchen Anruf automatisch zu erkennen. sie gibt jedoch an, dass die Hook-Flash-Funktion aufgerufen wird, um zu einem solchen Aufruf zu wechseln.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_SETMEDIACONTROL"></span><span id="lineaddrfeature_setmediacontrol"></span>**LINEADDRFEATURE \_ SETMEDIACONTROL**
</dt> <dd> <dl> <dt>



Die Mediensteuerung kann für diese Adresse festgelegt werden.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_SETTERMINAL"></span><span id="lineaddrfeature_setterminal"></span>**LINEADDRFEATURE \_ SETTERMINAL**
</dt> <dd> <dl> <dt>



Die Terminalmodi für diese Adresse können festgelegt werden.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_SETUPCONF"></span><span id="lineaddrfeature_setupconf"></span>**LINEADDRFEATURE \_ SETUPCONF**
</dt> <dd> <dl> <dt>



Ein Telefonkonferenz mit einem **ersten NULL-Aufruf** kann unter dieser Adresse eingerichtet werden.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_UNCOMPLETECALL"></span><span id="lineaddrfeature_uncompletecall"></span>**LINEADDRFEATURE \_ UNCOMPLETECALL**
</dt> <dd> <dl> <dt>



Aufruferledigungsanforderungen können unter dieser Adresse abgebrochen werden.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_UNPARK"></span><span id="lineaddrfeature_unpark"></span>**LINEADDRFEATURE \_ UNPARK**
</dt> <dd> <dl> <dt>



Aufrufe können mit dieser Adresse nicht geparkt werden.

> [!Note]  
> Wenn keines der neuen geänderten "PICKUP"-Bits im **dwAddressFeatures-Member** in [**LINEADDRESSSTATUS festgelegt**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) ist, aber das LINEADDRFEATURE PICKUP-Bit festgelegt ist, kann jeder der Abholmodi funktionieren. Der Dienstanbieter hat einfach nicht angegeben, welche modi es \_ gibt.

 


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_FORWARDDND"></span><span id="lineaddrfeature_forwarddnd"></span>**LINEADDRFEATURE \_ FORWARDDND**
</dt> <dd> <dl> <dt>



Die [**lineForward-Funktion**](/windows/desktop/api/Tapi/nf-tapi-lineforward) (mit einer leeren Zieladresse) kann verwendet werden, um die Funktion "Nicht stören" für die Adresse zu aktivieren. LINEADDRFEATURE \_ FORWARD wird ebenfalls festgelegt.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_FORWARDFWD"></span><span id="lineaddrfeature_forwardfwd"></span>**LINEADDRFEATURE \_ FORWARDFWD**
</dt> <dd> <dl> <dt>



Mit [**der lineForward-Funktion**](/windows/desktop/api/Tapi/nf-tapi-lineforward) können Aufrufe der Adresse an andere Zahlen weitergeleitet werden. LINEADDRFEATURE \_ FORWARD wird ebenfalls festgelegt.

> [!Note]  
> Wenn keines der neuen geänderten "FORWARD"-Bits im **dwAddressFeatures-Member** in [**LINEADDRESSSTATUS festgelegt**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) ist, aber das LINEADDRFEATURE FORWARD-Bit festgelegt ist, funktioniert möglicherweise einer der Vorwärtsmodi. Der Dienstanbieter hat einfach nicht angegeben, welche. \_

 


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Hinweise

Keine Erweiterbarkeit. Alle 32 Bits sind reserviert.

Diese Konstante wird sowohl in [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) (von [**lineGetAddressCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps)zurückgegeben) als auch in [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) (zurückgegeben von [**lineGetAddressStatus) verwendet.**](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus) **LINEADDRESSCAPS** meldet die Verfügbarkeit der Adressfeatures durch den Dienstanbieter (hauptsächlich den Switch) für eine bestimmte Adresse. Eine Anwendung würde diese Bestimmung treffen, wenn sie initialisiert wird. Die [**LINEADDRESSSTATUS-Struktur**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) meldet für eine bestimmte Adresse, welche Adressfeatures tatsächlich aufgerufen werden können, während sich die Adresse im aktuellen Zustand befindet. Eine Anwendung würde diese Bestimmung dynamisch nach Änderungen des Adresszustands vornehmen, die in der Regel durch aufrufbezogene Aktivitäten auf der Adresse verursacht werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2.0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)
</dt> <dt>

[**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus)
</dt> <dt>

[**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward)
</dt> <dt>

[**lineGetAddressCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps)
</dt> <dt>

[**lineGetAddressStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus)
</dt> <dt>

[**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup)
</dt> </dl>

 

 




