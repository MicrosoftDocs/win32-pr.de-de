---
title: IP_SPECIFIC_DATA Struktur (RTM. h)
description: Die IP \_ -spezifische Datenstruktur enthält IP-spezifische Daten.
ms.assetid: 68f2f4cc-141b-4f22-94ac-cc72e8dcca0a
keywords:
- IP_SPECIFIC_DATA Struktur-RAS
- PIP_SPECIFIC_DATA-Struktur Zeiger RAS
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
ms.openlocfilehash: 2a3ed319f7cf42295bf918ed3ec67f5d59fe5d80
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104678"
---
# <a name="ip_specific_data-structure"></a>IP- \_ spezifische \_ Datenstruktur

\[Diese API wurde durch die API für [Routing Table Manager, Version 2](about-routing-table-manager-version-2.md) , ersetzt und ist nicht über Windows Server 2003 verfügbar. Anwendungen sollten die API für Routing Table Manager Version 2 verwenden.\]

Die **IP- \_ spezifische Daten** Struktur enthält IP-spezifische Daten.

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

**Typ " \_ Typ"**
</dt> <dd>

Gibt den Routentyp an, wie in [RFC 1354](routing-protocols-request-for-comments.md)definiert. In der folgenden Tabelle werden die möglichen Werte für diesen Member angezeigt.



| Member                                                                                               | Bedeutung                                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | Der Routentyp wurde nicht angegeben. Der-Typ unterscheidet sich von den hier aufgeführten.<br/>                                                                                                                                                                                         |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Die Route ist ungültig. Normalerweise wird dieser Wert verwendet, um eine Route für ungültig zu erklären. Da die Invalidierung vom Routing Tabellen-Manager jedoch nicht unterstützt wird, wird die Route weiterhin in den Best-Route-Berechnungen berücksichtigt. Daher sollten Routing Protokolle diesen Wert nicht verwenden.<br/> |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | Die Route ist eine lokale Route, d. h., der nächste Hop ist das endgültige Ziel.<br/>                                                                                                                                                                                            |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | Die Route ist eine Remote Route, d. h., der nächste Hop ist nicht das endgültige Ziel.<br/>                                                                                                                                                                                       |



 

</dd> <dt>

**F- \_ Richtlinie**
</dt> <dd>

Gibt den Satz von Bedingungen an, die die Auswahl einer multipfadroute bewirken würden. Dieser Member befindet sich in der Regel im IP-Adressformat. Weitere Informationen finden Sie unter [RFC 1354](routing-protocols-request-for-comments.md).

</dd> <dt>

**F// \_ nexthopas**
</dt> <dd>

Gibt die autonome System Nummer des nächsten Hops an.

</dd> <dt>

**F- \_ Priorität**
</dt> <dd>

Gibt einen Metrikwert an. Der Routing Tabellen-Manager verwendet diesen Wert, um diesen Routen Eintrag mit Routen Einträgen zu vergleichen, die aus anderen Routing Protokollen abgerufen wurden. Der Wert dieses Members wird vom Routing Tabellen-Manager festgelegt.

</dd> <dt>

**F- \_ Metrik**
</dt> <dd>

Gibt einen Metrikwert an. Der Routing Tabellen-Manager verwendet diesen Wert, um diesen Routen Eintrag mit anderen Routen Einträgen zu vergleichen, die aus demselben Routing Protokoll abgerufen werden. Der Wert dieses Members wird durch das Routing Protokoll festgelegt.

</dd> <dt>

**\_Metric1**
</dt> <dd>

Gibt einen Routing Protokoll spezifischen Metrikwert an. Dieser Metrikwert ist in [RFC 1354](routing-protocols-request-for-comments.md)dokumentiert.

</dd> <dt>

**\_Metric2**
</dt> <dd>

Gibt einen Routing Protokoll spezifischen Metrikwert an. Dieser Metrikwert ist in [RFC 1354](routing-protocols-request-for-comments.md)dokumentiert.

</dd> <dt>

**\_Metric3**
</dt> <dd>

Gibt einen Routing Protokoll spezifischen Metrikwert an. Dieser Metrikwert ist in [RFC 1354](routing-protocols-request-for-comments.md)dokumentiert.

</dd> <dt>

**\_Metric4**
</dt> <dd>

Gibt einen Routing Protokoll spezifischen Metrikwert an. Dieser Metrikwert ist in [RFC 1354](routing-protocols-request-for-comments.md)dokumentiert.

</dd> <dt>

**\_Metric5**
</dt> <dd>

Gibt einen Routing Protokoll spezifischen Metrikwert an. Dieser Metrikwert ist in [RFC 1354](routing-protocols-request-for-comments.md)dokumentiert.

</dd> <dt>

**F- \_ Flags**
</dt> <dd>

Gibt an, ob die Route gültig ist. Das Routing Protokoll sollte diese Flags zuerst löschen und dann die Route als gültig oder ungültig festlegen. Das Routing Protokoll sollte zum Durchführen dieser Vorgänge die Makros **clearrouteflags ()** **, "", "**", "", "", "", "", "", " **", "** " Diese Makros sind in RTM. h definiert.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der Routing Tabellen-Manager verwendet die **FSD- \_ Priorität** und die **FSD- \_ metrikelemente** , um die beste Route zu einem bestimmten Zielnetzwerk zu berechnen.

Die **FSD- \_ Metrik \[ 1-5 \]** -Elemente sind für die MIB II-Konformität vorgesehen. In MIB II-Agents werden nur diese Metrikwerte angezeigt. Der Wert der **SSD \_** -Metrik wird nicht angezeigt. Damit die **FSD- \_ Metrik** angezeigt wird, sollte das Routing Protokoll auch den Wert in einem der **FSD- \_ Metrik \[ 1-5 \]** -Elemente speichern.

Der Routing Tabellen-Manager verwendet die Metrikwerte in den **FSD- \_ Metrik \[ 1-5 \]** -Membern nicht, wenn die beste Route zu einem Zielnetzwerk berechnet wird. Daher sollte das Routing Protokoll sicherstellen, dass das **FSD- \_ metrikelement** über einen entsprechenden Metrikwert verfügt.

Ein Routing Protokoll könnte mithilfe der **FSD- \_ Flags** eine Route als ungültig markieren, wenn die Route nicht von anderen Routing Protokollen verwendet werden soll.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                   |
| Header<br/>                   | <dl> <dt>RTM. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Referenz für Routing Tabellen-Manager Version 1](routing-table-manager-version-1-reference.md)
</dt> <dt>

[Routing Tabellen-Manager, Version 1, Strukturen](routing-table-manager-version-1-structures.md)
</dt> <dt>

[**RTM \_ -IP- \_ Route**](rtm-ip-route.md)
</dt> </dl>

 

 





