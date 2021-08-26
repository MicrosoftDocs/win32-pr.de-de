---
title: IP_SPECIFIC_DATA-Struktur (Rtm.h)
description: Die \_ IP-SPEZIFISCHE DATENstruktur enthält IP-spezifische Daten.
ms.assetid: 68f2f4cc-141b-4f22-94ac-cc72e8dcca0a
keywords:
- IP_SPECIFIC_DATA struktur ras
- PIP_SPECIFIC_DATA Strukturzeiger RAS
topic_type:
- apiref
api_name:
- IP_SPECIFIC_DATA
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 906ae9f2accb3d380227f08ad6b65642b96ce6bfa928591bd11a69c478f531b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120036670"
---
# <a name="ip_specific_data-structure"></a>\_IP-SPEZIFISCHE \_ DATENstruktur

\[Diese API wurde von der Routing Table Manager Version [2-API](about-routing-table-manager-version-2.md) abgelöst und ist nicht mehr als Windows Server 2003 verfügbar. Anwendungen sollten die Routing Table Manager Version 2-API verwenden.\]

Die **\_ IP-SPEZIFISCHE DATENstruktur** enthält IP-spezifische Daten.

## <a name="syntax"></a>Syntax


```C++
typedef struct _IP_SPECIFIC_DATA {
  DWORD FSD_Type;
  DWORD FSD_Policy;
  DWORD FSD_NextHopAS;
  DWORD FSD_Priority;
  DWORD FSD_Metric;
  DWORD FSD_Metric1;
  DWORD FSD_Metric2;
  DWORD FSD_Metric3;
  DWORD FSD_Metric4;
  DWORD FSD_Metric5;
  DWORD FSD_Flags;
} IP_SPECIFIC_DATA, *PIP_SPECIFIC_DATA;
```



## <a name="members"></a>Member

<dl> <dt>

**\_FSD-Typ**
</dt> <dd>

Gibt den Routentyp an, wie in [RFC 1354](routing-protocols-request-for-comments.md)definiert. Die folgende Tabelle zeigt die möglichen Werte für dieses Element.



| Member                                                                                               | Bedeutung                                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | Der Routentyp ist nicht angegeben. Der Typ unterscheidet sich von den hier aufgeführten Typen.<br/>                                                                                                                                                                                         |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Die Route ist ungültig. Normalerweise wird dieser Wert verwendet, um eine Route ungültig zu machen. Da die Invalidierung jedoch vom Routingtabellen-Manager nicht unterstützt wird, wird die Route in Berechnungen mit der besten Route weiterhin berücksichtigt. Daher sollten Routingprotokolle diesen Wert nicht verwenden.<br/> |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | Die Route ist eine lokale Route, d. h., der nächste Hop ist das endgültige Ziel.<br/>                                                                                                                                                                                            |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | Die Route ist eine Remoteroute, d. h., der nächste Hop ist nicht das endgültige Ziel.<br/>                                                                                                                                                                                       |



 

</dd> <dt>

**\_FSD-Richtlinie**
</dt> <dd>

Gibt den Satz von Bedingungen an, die die Auswahl einer Route mit mehreren Pfaden verursachen würden. Dieser Member weist in der Regel das IP-TOS-Format auf. Weitere Informationen finden Sie unter [RFC 1354](routing-protocols-request-for-comments.md).

</dd> <dt>

**FSD \_ NextHopAS**
</dt> <dd>

Gibt die autonome Systemnummer des nächsten Hops an.

</dd> <dt>

**\_FSD-Priorität**
</dt> <dd>

Gibt einen Metrikwert an. Der Routingtabellen-Manager verwendet diesen Wert, um diesen Routeneintrag mit Routeneinträgen zu vergleichen, die von anderen Routingprotokollen abgerufen wurden. Der Wert dieses Members wird vom Routingtabellen-Manager festgelegt.

</dd> <dt>

**\_FSD-Metrik**
</dt> <dd>

Gibt einen Metrikwert an. Der Routingtabellen-Manager verwendet diesen Wert, um diesen Routeneintrag mit anderen Routeneinträgen zu vergleichen, die aus dem gleichen Routingprotokoll abgerufen wurden. Der Wert dieses Members wird durch das Routingprotokoll festgelegt.

</dd> <dt>

**FSD \_ Metric1**
</dt> <dd>

Gibt einen routingprotokollspezifischen Metrikwert an. Dieser Metrikwert ist in [RFC 1354](routing-protocols-request-for-comments.md)dokumentiert.

</dd> <dt>

**FSD \_ Metric2**
</dt> <dd>

Gibt einen routingprotokollspezifischen Metrikwert an. Dieser Metrikwert ist in [RFC 1354](routing-protocols-request-for-comments.md)dokumentiert.

</dd> <dt>

**\_FSD-Metrik3**
</dt> <dd>

Gibt einen routingprotokollspezifischen Metrikwert an. Dieser Metrikwert ist in [RFC 1354](routing-protocols-request-for-comments.md)dokumentiert.

</dd> <dt>

**\_FSD-Metrik4**
</dt> <dd>

Gibt einen routingprotokollspezifischen Metrikwert an. Dieser Metrikwert ist in [RFC 1354](routing-protocols-request-for-comments.md)dokumentiert.

</dd> <dt>

**\_FSD-Metrik5**
</dt> <dd>

Gibt einen routingprotokollspezifischen Metrikwert an. Dieser Metrikwert ist in [RFC 1354](routing-protocols-request-for-comments.md)dokumentiert.

</dd> <dt>

**\_FSD-Flags**
</dt> <dd>

Gibt an, ob die Route gültig ist. Das Routingprotokoll sollte diese Flags zuerst löschen und dann die Route entweder als gültig oder ungültig festlegen. Das Routingprotokoll sollte die Makros **ClearRouteFlags()**, **SetRouteValid()** und **ClearRouteValid()** verwenden, um diese Vorgänge auszuführen. Diese Makros werden in Rtm.h definiert.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Der Routingtabellen-Manager verwendet die **\_ FSD-Prioritäts-** und **\_ FSD-Metrikmember,** um die beste Route zu einem bestimmten Zielnetzwerk zu berechnen.

Die FSD Metric 1-5 members are for MIB II conformance **\_ (FSD-Metrik \[ \] 1-5-Member** für DIE MIB II-Konformität). MIB II-Agents zeigen nur diese Metrikwerte an. Der Metrikwert der **\_ FSD-Metrik** wird nicht angezeigt. Damit die **\_ FSD-Metrik** angezeigt wird, sollte das Routingprotokoll auch den Wert in einem der **\_ FSD-Metrik \[ 1-5 \]** Member speichern.

Der Routingtabellen-Manager verwendet beim Berechnen der besten Route zu einem Zielnetzwerk nicht die Metrikwerte in den **\_ \[ FSD-Metrik \] 1-5-Mitgliedern.** Daher sollte das Routingprotokoll sicherstellen, dass das **\_ FSD-Metrikmitglied** über einen geeigneten Metrikwert verfügt.

Ein Routingprotokoll kann die **\_ FSD-Flags** verwenden, um eine Route als ungültig zu kennzeichnen, wenn die Route nicht von anderen Routingprotokollen verwendet werden soll.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                   |
| Header<br/>                   | <dl> <dt>Rtm.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Referenz zu Routingtabellen-Manager, Version 1](routing-table-manager-version-1-reference.md)
</dt> <dt>

[Routingtabellen-Manager- Version 1-Strukturen](routing-table-manager-version-1-structures.md)
</dt> <dt>

[**\_RTM-IP-ROUTE \_**](rtm-ip-route.md)
</dt> </dl>

 

 





