---
description: Listet die aktuell definierten ACE-Typen auf.
ms.assetid: 980b8242-2ba2-469f-b834-da7d3fb22e14
title: ACE (WinNT. h)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e4d06b3457e4df6aea38d3e35acf4f7aaa4e2f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347953"
---
# <a name="ace"></a>Spezialisierung

Ein **ACE** ist ein [*Zugriffs Steuerungs Eintrag*](/windows/desktop/SecGloss/a-gly) in einer [*Zugriffs Steuerungs Liste (Access Control List*](/windows/desktop/SecGloss/a-gly) , ACL).

In der folgenden Tabelle sind die aktuell definierten **ACE** -Typen aufgeführt.



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
<td>Räumen</td>
</tr>
<tr class="even">
<td><ul>
<li>Zugriff zulässig</li>
<li>Ermöglicht den Rückruf während der Zugriffs Überprüfung.</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-access_allowed_callback_ace"><strong>ACCESS_ALLOWED_CALLBACK_ACE</strong></a></td>
<td>Räumen</td>
</tr>
<tr class="odd">
<td><ul>
<li>Zugriff zulässig</li>
<li>Objekt spezifisch</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-access_allowed_object_ace"><strong>ACCESS_ALLOWED_OBJECT_ACE</strong></a></td>
<td>Räumen</td>
</tr>
<tr class="even">
<td><ul>
<li>Zugriff zulässig</li>
<li>Objekt spezifisch</li>
<li>Ermöglicht den Rückruf während der Zugriffs Überprüfung.</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-access_allowed_callback_object_ace"><strong>ACCESS_ALLOWED_CALLBACK_OBJECT_ACE</strong></a></td>
<td>Räumen</td>
</tr>
<tr class="odd">
<td><ul>
<li>Zugriff verweigert.</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-access_denied_ace"><strong>ACCESS_DENIED_ACE</strong></a></td>
<td>Räumen</td>
</tr>
<tr class="even">
<td><ul>
<li>Zugriff verweigert.</li>
<li>Ermöglicht den Rückruf während der Zugriffs Überprüfung.</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-access_denied_callback_ace"><strong>ACCESS_DENIED_CALLBACK_ACE</strong></a></td>
<td>Räumen</td>
</tr>
<tr class="odd">
<td><ul>
<li>Zugriff verweigert.</li>
<li>Objekt spezifisch</li>
<li>Ermöglicht den Rückruf während der Zugriffs Überprüfung.</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-access_denied_callback_object_ace"><strong>ACCESS_DENIED_CALLBACK_OBJECT_ACE</strong></a></td>
<td>Räumen</td>
</tr>
<tr class="even">
<td><ul>
<li>Zugriff verweigert.</li>
<li>Objekt spezifisch</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-access_denied_object_ace"><strong>ACCESS_DENIED_OBJECT_ACE</strong></a></td>
<td>Räumen</td>
</tr>
<tr class="odd">
<td><ul>
<li>System Alarm</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-system_alarm_ace"><strong>SYSTEM_ALARM_ACE</strong></a></td>
<td>System</td>
</tr>
<tr class="even">
<td><ul>
<li>System Alarm</li>
<li>Ermöglicht den Rückruf während der Zugriffs Überprüfung.</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-system_alarm_callback_ace"><strong>SYSTEM_ALARM_CALLBACK_ACE</strong></a></td>
<td>System</td>
</tr>
<tr class="odd">
<td><ul>
<li>System Alarm</li>
<li>Objekt spezifisch</li>
<li>Ermöglicht den Rückruf während der Zugriffs Überprüfung.</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-system_alarm_callback_object_ace"><strong>SYSTEM_ALARM_CALLBACK_OBJECT_ACE</strong></a></td>
<td>System</td>
</tr>
<tr class="even">
<td><ul>
<li>System Alarm</li>
<li>Objekt spezifisch</li>
</ul></td>
<td><a href="/windows/desktop/api/winnt/ns-winnt-system_alarm_object_ace"><strong>SYSTEM_ALARM_OBJECT_ACE</strong></a></td>
<td>System</td>
</tr>
<tr class="odd">
<td><ul>
<li>System Überwachung</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-system_audit_ace"><strong>SYSTEM_AUDIT_ACE</strong></a></td>
<td>System</td>
</tr>
<tr class="even">
<td><ul>
<li>System Überwachung</li>
<li>Ermöglicht den Rückruf während der Zugriffs Überprüfung.</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-system_audit_callback_ace"><strong>SYSTEM_AUDIT_CALLBACK_ACE</strong></a></td>
<td>System</td>
</tr>
<tr class="odd">
<td><ul>
<li>System Überwachung</li>
<li>Objekt spezifisch</li>
<li>Ermöglicht den Rückruf während der Zugriffs Überprüfung.</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-system_audit_callback_object_ace"><strong>SYSTEM_AUDIT_CALLBACK_OBJECT_ACE</strong></a></td>
<td>System</td>
</tr>
<tr class="even">
<td><ul>
<li>System Überwachung</li>
<li>Objekt spezifisch</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-system_alarm_object_ace"><strong>SYSTEM_AUDIT_OBJECT_ACE</strong></a></td>
<td>System</td>
</tr>
</tbody>
</table>



 

System Alarm und objektspezifische System Alarm-ACEs werden zurzeit nicht unterstützt.

> [!Note]  
> Jeder ACE beginnt mit einer [**ACE- \_ Header**](/windows/desktop/api/Winnt/ns-winnt-ace_header) Struktur. Das Format der Daten, die dem Header folgen, variiert je nach dem im Header angegebenen ACE-Typ.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                   |
| Header<br/>                   | <dl> <dt>WinNT. h (Include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Addace**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addace)
</dt> <dt>

[**Zugriffs zulässiger \_ \_ ACE**](/windows/desktop/api/Winnt/ns-winnt-access_allowed_ace)
</dt> <dt>

[**Zugriffs \_ Verweigerungs \_ ACE**](/windows/desktop/api/Winnt/ns-winnt-access_denied_ace)
</dt> <dt>

[**ACL**](/windows/desktop/api/Winnt/ns-winnt-acl)
</dt> <dt>

[**Systemalarm- \_ \_ ACE**](/windows/desktop/api/Winnt/ns-winnt-system_alarm_object_ace)
</dt> <dt>

[**Systemüberwachungs- \_ \_ ACE**](/windows/desktop/api/Winnt/ns-winnt-system_audit_ace)
</dt> </dl>

