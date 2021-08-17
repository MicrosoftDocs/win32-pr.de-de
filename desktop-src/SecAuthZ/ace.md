---
description: Listet die derzeit definierten ACE-Typen auf.
ms.assetid: 980b8242-2ba2-469f-b834-da7d3fb22e14
title: ACE (Winnt.h)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de555170bc8b7c1594b38adaa95d19b7e9ace54c8241fc971ea9f5383cf3e115
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117785219"
---
# <a name="ace"></a>Ass

Ein **ACE** ist ein [*Zugriffssteuerungseintrag*](/windows/desktop/SecGloss/a-gly) in einer [*Zugriffssteuerungsliste (Access Control List,*](/windows/desktop/SecGloss/a-gly) ACL).

In der folgenden Tabelle sind die derzeit definierten **ACE-Typen** aufgeführt.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>ACE-Typ</th>
<th>Struktur</th>
<th>ACL-Typ</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li>Zugriff zulässig</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-access_allowed_ace"><strong>ACCESS_ALLOWED_ACE</strong></a></td>
<td>Ermessensabhängiger</td>
</tr>
<tr class="even">
<td><ul>
<li>Zugriff zulässig</li>
<li>Ermöglicht den Rückruf während der Zugriffsüberprüfung.</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-access_allowed_callback_ace"><strong>ACCESS_ALLOWED_CALLBACK_ACE</strong></a></td>
<td>Ermessensabhängiger</td>
</tr>
<tr class="odd">
<td><ul>
<li>Zugriff zulässig</li>
<li>Objektspezifisch</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-access_allowed_object_ace"><strong>ACCESS_ALLOWED_OBJECT_ACE</strong></a></td>
<td>Ermessensabhängiger</td>
</tr>
<tr class="even">
<td><ul>
<li>Zugriff zulässig</li>
<li>Objektspezifisch</li>
<li>Ermöglicht den Rückruf während der Zugriffsüberprüfung.</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-access_allowed_callback_object_ace"><strong>ACCESS_ALLOWED_CALLBACK_OBJECT_ACE</strong></a></td>
<td>Ermessensabhängiger</td>
</tr>
<tr class="odd">
<td><ul>
<li>Zugriff verweigert.</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-access_denied_ace"><strong>ACCESS_DENIED_ACE</strong></a></td>
<td>Ermessensabhängiger</td>
</tr>
<tr class="even">
<td><ul>
<li>Zugriff verweigert.</li>
<li>Ermöglicht den Rückruf während der Zugriffsüberprüfung.</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-access_denied_callback_ace"><strong>ACCESS_DENIED_CALLBACK_ACE</strong></a></td>
<td>Ermessensabhängiger</td>
</tr>
<tr class="odd">
<td><ul>
<li>Zugriff verweigert.</li>
<li>Objektspezifisch</li>
<li>Ermöglicht den Rückruf während der Zugriffsüberprüfung.</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-access_denied_callback_object_ace"><strong>ACCESS_DENIED_CALLBACK_OBJECT_ACE</strong></a></td>
<td>Ermessensabhängiger</td>
</tr>
<tr class="even">
<td><ul>
<li>Zugriff verweigert.</li>
<li>Objektspezifisch</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-access_denied_object_ace"><strong>ACCESS_DENIED_OBJECT_ACE</strong></a></td>
<td>Ermessensabhängiger</td>
</tr>
<tr class="odd">
<td><ul>
<li>Systemalarm</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-system_alarm_ace"><strong>SYSTEM_ALARM_ACE</strong></a></td>
<td>System</td>
</tr>
<tr class="even">
<td><ul>
<li>Systemalarm</li>
<li>Ermöglicht den Rückruf während der Zugriffsüberprüfung.</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-system_alarm_callback_ace"><strong>SYSTEM_ALARM_CALLBACK_ACE</strong></a></td>
<td>System</td>
</tr>
<tr class="odd">
<td><ul>
<li>Systemalarm</li>
<li>Objektspezifisch</li>
<li>Ermöglicht den Rückruf während der Zugriffsüberprüfung.</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-system_alarm_callback_object_ace"><strong>SYSTEM_ALARM_CALLBACK_OBJECT_ACE</strong></a></td>
<td>System</td>
</tr>
<tr class="even">
<td><ul>
<li>Systemalarm</li>
<li>Objektspezifisch</li>
</ul></td>
<td><a href="/windows/desktop/api/winnt/ns-winnt-system_alarm_object_ace"><strong>SYSTEM_ALARM_OBJECT_ACE</strong></a></td>
<td>System</td>
</tr>
<tr class="odd">
<td><ul>
<li>Systemüberwachung</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-system_audit_ace"><strong>SYSTEM_AUDIT_ACE</strong></a></td>
<td>System</td>
</tr>
<tr class="even">
<td><ul>
<li>Systemüberwachung</li>
<li>Ermöglicht den Rückruf während der Zugriffsüberprüfung.</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-system_audit_callback_ace"><strong>SYSTEM_AUDIT_CALLBACK_ACE</strong></a></td>
<td>System</td>
</tr>
<tr class="odd">
<td><ul>
<li>Systemüberwachung</li>
<li>Objektspezifisch</li>
<li>Ermöglicht den Rückruf während der Zugriffsüberprüfung.</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-system_audit_callback_object_ace"><strong>SYSTEM_AUDIT_CALLBACK_OBJECT_ACE</strong></a></td>
<td>System</td>
</tr>
<tr class="even">
<td><ul>
<li>Systemüberwachung</li>
<li>Objektspezifisch</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-system_alarm_object_ace"><strong>SYSTEM_AUDIT_OBJECT_ACE</strong></a></td>
<td>System</td>
</tr>
</tbody>
</table>



 

Systemalarm- und objektspezifische Systemalarm-ACEs werden derzeit nicht unterstützt.

> [!Note]  
> Jeder ACE beginnt mit einer [**ACE \_ HEADER-Struktur.**](/windows/desktop/api/Winnt/ns-winnt-ace_header) Das Format der Daten, die auf den Header folgen, variiert je nach dem im Header angegebenen ACE-Typ.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                   |
| Header<br/>                   | <dl> <dt>Winnt.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**AddAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addace)
</dt> <dt>

[**ACCESS \_ ALLOWED \_ ACE**](/windows/desktop/api/Winnt/ns-winnt-access_allowed_ace)
</dt> <dt>

[**ACCESS \_ DENIED \_ ACE**](/windows/desktop/api/Winnt/ns-winnt-access_denied_ace)
</dt> <dt>

[**ACL**](/windows/desktop/api/Winnt/ns-winnt-acl)
</dt> <dt>

[**SYSTEM \_ ALARM \_ ACE**](/windows/desktop/api/Winnt/ns-winnt-system_alarm_object_ace)
</dt> <dt>

[**SYSTEM \_ AUDIT \_ ACE**](/windows/desktop/api/Winnt/ns-winnt-system_audit_ace)
</dt> </dl>

