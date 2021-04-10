---
description: Winlogon und Gina müssen Initialisierungs Informationen kommunizieren, die Überwachung und Benachrichtigung über die Sicherheitsüberwachung (Secure Monitoring Sequence, SAS) verarbeiten und die Aktivitäten zum Abmelden und Herunterfahren zulassen.
ms.assetid: ea45cd5f-9cb0-41bb-99bf-f84781ae9604
title: 'Interaktion zwischen Windows-Anmeldung und GINA '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 759d9171bca02e0a00fd35b77a4514d7438d43f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050387"
---
# <a name="interaction-between-winlogon-and-gina"></a>Interaktion zwischen Windows-Anmeldung und GINA 

[*Winlogon*](../secgloss/w-gly.md) und [*Gina*](../secgloss/g-gly.md) müssen Initialisierungs Informationen kommunizieren, die Überwachung und Benachrichtigung über die Sicherheitsüberwachung ( [*Secure Monitoring Sequence*](../secgloss/s-gly.md) , SAS) verarbeiten und die Aktivitäten zum Abmelden und Herunterfahren zulassen. Der Status von Winlogon bestimmt, welche Gina-Funktion aufgerufen wird, um ein bestimmtes SAS-Ereignis zu verarbeiten. Die Kommunikation erfolgt in der hier gezeigten Reihenfolge.

> [!Note]  
> Gina-DLLs werden in Windows Vista ignoriert.

 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Ereignis</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Arbeitsstation starten</td>
<td><ol>
<li>Winlogon Ruft die <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxnegotiate"><strong>wlxaushandlungs</strong></a> -Funktion von Gina auf, um die Gina über die verwendete Version von Winlogon zu benachrichtigen.</li>
<li>Winlogon Ruft die <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxinitialize"><strong>wlxinitialize</strong></a> -Funktion von Gina auf, um der Gina die Adressen der Unterstützungsfunktionen, ein Handle für die Winlogon-Funktion und zum Abrufen der <a href="/windows/desktop/SecGloss/c-gly"><em>Kontext</em></a> Informationen für die Gina (für die Verwendung in allen zukünftigen Aufrufen der Gina) zu geben.<br/> Winlogon befindet sich im Abmelde Zustand.<br/></li>
</ol></td>
</tr>
<tr class="even">
<td>Niemand ist angemeldet.</td>
<td>(Die Gina überwacht Geräte auf SAS-Ereignisse).
<ol>
<li>Die Gina Ruft die <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>wlxsasnotify</strong></a> -Funktion von Winlogon auf, wenn ein SAS-Ereignis empfangen wurde.</li>
<li>Winlogon Ruft die <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedoutsas"><strong>wlxloggedoutsas</strong></a> -Funktion von Gina auf und ermöglicht es der Gina, die Identifikations-und Authentifizierungsinformationen eines Benutzers zu verarbeiten.<br/> Wenn die Anmeldung erfolgreich ist, befindet sich die Winlogon im angemeldeten Zustand.<br/></li>
</ol></td>
</tr>
<tr class="odd">
<td>Der Benutzer ist angemeldet.</td>
<td>(Die Gina überwacht Geräte auf SAS-Ereignisse).
<ol>
<li>Die Gina Ruft die <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>wlxsasnotify</strong></a> -Funktion von Winlogon auf, wenn ein SAS-Ereignis empfangen wurde.</li>
<li>Winlogon Ruft die <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedonsas"><strong>wlxloggedonsas</strong></a> -Funktion von Gina auf, sodass die Gina Optionen für den aktuell angemeldeten Benutzer präsentieren kann.</li>
</ol></td>
</tr>
<tr class="even">
<td>Der Benutzer ist angemeldet und möchte den Computer sperren.</td>
<td>(Die Gina überwacht Geräte auf SAS-Ereignisse).
<ol>
<li>Die Gina Ruft die <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>wlxsasnotify</strong></a> -Funktion auf.</li>
<li>Winlogon Ruft die <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedonsas"><strong>wlxloggedonsas</strong></a> -Funktion von Gina auf.</li>
<li>Die Gina gibt WLX_SAS_ACTION_LOCK_WKSTA zurück.<br/> Winlogon befindet sich im Zustand der Arbeitsstation.<br/></li>
</ol></td>
</tr>
<tr class="odd">
<td>Der Benutzer ist angemeldet, die Arbeitsstation ist gesperrt, und der Benutzer möchte den Computer entsperren.</td>
<td>(Die Gina überwacht Geräte auf SAS-Ereignisse).
<ol>
<li>Die Gina Ruft die <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>wlxsasnotify</strong></a> -Funktion auf.</li>
<li>Winlogon Ruft die <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxwkstalockedsas"><strong>wlxwkstalockedsas</strong></a> -Funktion von Gina auf.</li>
<li>Die Gina gibt WLX_SAS_ACTION_UNLOCK_WKSTA zurück.</li>
</ol></td>
</tr>
<tr class="even">
<td>Der Benutzer ist angemeldet, und das Programm ruft die <a href="/windows/desktop/api/winuser/nf-winuser-exitwindowsex"><strong>ExitWindowsEx</strong></a> -Funktion auf.</td>
<td>Winlogon Ruft die <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxlogoff"><strong>wlxlogoff</strong></a> -Funktion von Gina auf.</td>
</tr>
<tr class="odd">
<td>Der Benutzer ist angemeldet und möchte sich mithilfe von SAS abmelden.</td>
<td>(Die Gina überwacht Geräte auf SAS-Ereignisse).
<ol>
<li>Die Gina Ruft die <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>wlxsasnotify</strong></a> -Funktion auf.</li>
<li>Winlogon Ruft die <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedonsas"><strong>wlxloggedonsas</strong></a> -Funktion von Gina auf.</li>
<li>Die Gina gibt WLX_SAS_ACTION_LOGOFF zurück.</li>
<li>Winlogon Ruft die <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxlogoff"><strong>wlxlogoff</strong></a> -Funktion von Gina auf.</li>
</ol></td>
</tr>
<tr class="even">
<td>Der Benutzer ist angemeldet und möchte sich abmelden und mithilfe von <a href="/windows/desktop/api/winuser/nf-winuser-exitwindowsex"> <strong>ExitWindowsEx</strong> Herunterfahren.</a></td>
<td><ol>
<li>Winlogon Ruft die <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxlogoff"><strong>wlxlogoff</strong></a> -Funktion von Gina auf.</li>
<li>Winlogon Ruft die <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxshutdown"><strong>wlxshutdown</strong></a> -Funktion von Gina auf.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Der Benutzer ist angemeldet und möchte sich abmelden und mithilfe von SAS Herunterfahren.</td>
<td>(Die Gina überwacht Geräte auf SAS-Ereignisse).
<ol>
<li>Die Gina Ruft die <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>wlxsasnotify</strong></a> -Funktion auf.</li>
<li>Winlogon Ruft die <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedonsas"><strong>wlxloggedonsas</strong></a> -Funktion von Gina auf.</li>
<li>Die Gina gibt WLX_SAS_ACTION_SHUTDOWN zurück.</li>
<li>Winlogon Ruft die <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxlogoff"><strong>wlxlogoff</strong></a> -Funktion von Gina auf.</li>
<li>Winlogon Ruft die <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxshutdown"><strong>wlxshutdown</strong></a> -Funktion von Gina auf.</li>
</ol></td>
</tr>
</tbody>
</table>



 

 

 
