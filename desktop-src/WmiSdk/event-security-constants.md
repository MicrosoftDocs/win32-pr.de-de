---
description: Das folgende Beispiel zeigt die WMI-Sicherheitskonstanten, die für Ereignisse verwendet werden. Sie werden verwendet, um Zugriffssteuerungseinträge (ACEs) in Sicherheitsbeschreibungen festzulegen, die für Ereignisse oder Senken verwendet werden.
ms.assetid: 18318262-d948-4329-8d48-23664798fc58
ms.tgt_platform: multiple
title: Ereignissicherheitskonstanten (Wbemcli.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8ae26364c7edf6daaf9b70dcf769675c0a39966286b3b8f725fefe0af73ff8b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119244290"
---
# <a name="event-security-constants"></a>Ereignissicherheitskonstanten

Das folgende Beispiel zeigt die WMI-Sicherheitskonstanten, die für Ereignisse verwendet werden. Sie werden verwendet, um Zugriffssteuerungseinträge (ACEs) in Sicherheitsbeschreibungen festzulegen, die für Ereignisse oder Senken verwendet werden.

<dl> <dt>

<span id="WBEM_RIGHT_PUBLISH"></span><span id="wbem_right_publish"></span>**WBEM \_ RIGHT \_ PUBLISH**
</dt> <dd> <dl> <dt>

128 (0x80)
</dt> <dt>



Gibt an, dass das Konto Ereignisse in der Instanz von [**\_ \_ EventFilter**](--eventfilter.md) veröffentlichen kann, die den Ereignisfilter für einen permanenten Consumer definiert. Verfügbar in wbemcli.h.


</dt> </dl> </dd> <dt>

<span id="WBEM_RIGHT_SUBSCRIBE"></span><span id="wbem_right_subscribe"></span>**WBEM \_ RIGHT \_ SUBSCRIBE**
</dt> <dd> <dl> <dt>

64 (0x40)
</dt> <dt>



Gibt an, dass ein Consumer die an eine Senke übermittelten Ereignisse abonnieren kann. Wird in [**IWbemEventSink::SetSinkSecurity**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setsinksecurity)verwendet. Verfügbar in wbemcli.h.


</dt> </dl> </dd> <dt>

<span id="WBEM_S_SUBJECT_TO_SDS"></span><span id="wbem_s_subject_to_sds"></span>**WBEM \_ S \_ UNTERLIEGT \_ \_ SDS**
</dt> <dd> <dl> <dt>

274435 (0x43003)
</dt> <dt>



Der Ereignisanbieter gibt an, dass WMI die **SECURITY \_ DESCRIPTOR-Eigenschaft** in jedem Ereignis überprüft (geerbt von [**\_ \_ Event)**](--event.md)und nur Ereignisse an Consumer mit den entsprechenden Zugriffsberechtigungen sendet. Verfügbar in wbemprov.h.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                                                                                         |
| Header<br/>                   | <dl> <dt>Wbemcli.h; </dt> <dt>Wbemprov.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[WMI-Sicherheitskonstanten](wmi-security-constants.md)
</dt> <dt>

[Verwalten der WMI-Sicherheit](maintaining-wmi-security.md)
</dt> <dt>

[Sichern von WMI-Ereignissen](securing-wmi-events.md)
</dt> </dl>

 

 




