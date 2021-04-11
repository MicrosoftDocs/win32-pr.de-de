---
description: Im folgenden werden die WMI-Sicherheits Konstanten angezeigt, die für-Ereignisse verwendet werden. Sie werden verwendet, um Zugriffs Steuerungs Einträge (Access Control Entries, ACEs) in Sicherheits Beschreibungen festzulegen, die für Ereignisse oder senken verwendet werden.
ms.assetid: 18318262-d948-4329-8d48-23664798fc58
ms.tgt_platform: multiple
title: Ereignis Sicherheits Konstanten (wbemcli. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a3009b16e468a647ee96b9be365286caba2c12b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131156"
---
# <a name="event-security-constants"></a>Ereignis Sicherheits Konstanten

Im folgenden werden die WMI-Sicherheits Konstanten angezeigt, die für-Ereignisse verwendet werden. Sie werden verwendet, um Zugriffs Steuerungs Einträge (Access Control Entries, ACEs) in Sicherheits Beschreibungen festzulegen, die für Ereignisse oder senken verwendet werden.

<dl> <dt>

<span id="WBEM_RIGHT_PUBLISH"></span><span id="wbem_right_publish"></span>**WBEM \_ right \_ Publish**
</dt> <dd> <dl> <dt>

128 (0x80)
</dt> <dt>



Gibt an, dass das Konto Ereignisse in der Instanz von [**\_ \_ EventFilter**](--eventfilter.md) veröffentlichen kann, die den Ereignis Filter für einen permanenten Consumer definiert. Verfügbar in wbemcli. h.


</dt> </dl> </dd> <dt>

<span id="WBEM_RIGHT_SUBSCRIBE"></span><span id="wbem_right_subscribe"></span>**WBEM \_ right \_ Subscribe**
</dt> <dd> <dl> <dt>

64 (0x40)
</dt> <dt>



Gibt an, dass ein Consumer die an eine Senke übermittelten Ereignisse abonnieren kann. Wird in [**iwbemeventsink:: setsink Security**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setsinksecurity)verwendet. Verfügbar in wbemcli. h.


</dt> </dl> </dd> <dt>

<span id="WBEM_S_SUBJECT_TO_SDS"></span><span id="wbem_s_subject_to_sds"></span>**WBEM \_ S \_ unter \_ liegt \_ SDS**
</dt> <dd> <dl> <dt>

274435 (0x43003)
</dt> <dt>



Der Ereignis Anbieter zeigt an, dass WMI die **\_ sicherheitsbeschreibungenschaft** in jedem Ereignis überprüft (von [**\_ \_ Ereignis**](--event.md)geerbt) und nur Ereignisse an Consumer mit den entsprechenden Zugriffsberechtigungen sendet. Verfügbar in "wbemprov. h".


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                                                                                         |
| Header<br/>                   | <dl> <dt>Wbemcli. h; </dt> <dt>Wbemprov. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[WMI-Sicherheits Konstanten](wmi-security-constants.md)
</dt> <dt>

[Verwalten der WMI-Sicherheit](maintaining-wmi-security.md)
</dt> <dt>

[Sichern von WMI-Ereignissen](securing-wmi-events.md)
</dt> </dl>

 

 




