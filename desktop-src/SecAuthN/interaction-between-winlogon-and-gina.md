---
description: Winlogon und GINA müssen Initialisierungsinformationen kommunizieren, die Überwachung und Benachrichtigung der sicheren Aufmerksamkeitssequenz (Secure Attention Sequence, SAS) verarbeiten und Abmeldungs- und Herunterfahrensaktivitäten zulassen.
ms.assetid: ea45cd5f-9cb0-41bb-99bf-f84781ae9604
title: 'Interaktion zwischen Windows-Anmeldung und GINA '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 824c658e4f19b14de339b569a8c9d17992c1b60bb5d4d526de949ce76cd1554d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119482360"
---
# <a name="interaction-between-winlogon-and-gina"></a>Interaktion zwischen Windows-Anmeldung und GINA 

[*Winlogon*](../secgloss/w-gly.md) und [*GINA*](../secgloss/g-gly.md) müssen Initialisierungsinformationen kommunizieren, die Überwachung und Benachrichtigung der [*sicheren Aufmerksamkeitssequenz (Secure Attention Sequence,*](../secgloss/s-gly.md) SAS) verarbeiten und Abmeldungs- und Herunterfahrensaktivitäten zulassen. Der Status von Winlogon bestimmt, welche GINA-Funktion aufgerufen wird, um ein bestimmtes SAS-Ereignis zu verarbeiten. Die Kommunikation erfolgt in der hier gezeigten Reihenfolge.

> [!Note]  
> GINA-DLLs werden in Windows Vista ignoriert.

 



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
<td>Starten der Arbeitsstation</td>
<td><ol>
<li>Winlogon ruft die <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxnegotiate"><strong>WlxNegotiate-Funktion</strong></a> der GINA auf, um die GINA über die version von Winlogon zu benachrichtigen, die verwendet wird.</li>
<li>Winlogon ruft die <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxinitialize"><strong>WlxInitialize-Funktion</strong></a> der GINA auf, um der GINA die Adressen der Unterstützungsfunktionen, ein Handle für Winlogon und die <a href="/windows/desktop/SecGloss/c-gly"><em>Kontextinformationen</em></a> für die GINA zu geben (die in allen zukünftigen Aufrufen der GINA verwendet werden sollen).<br/> Winlogon befindet sich im Status "Abgemeldet".<br/></li>
</ol></td>
</tr>
<tr class="even">
<td>Es ist niemand angemeldet.</td>
<td>(Die GINA überwacht Geräte auf SAS-Ereignisse.)
<ol>
<li>Die GINA ruft die <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify-Funktion</strong></a> von Winlogon auf, wenn ein SAS-Ereignis empfangen wurde.</li>
<li>Winlogon ruft die <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedoutsas"><strong>WlxLoggedOutSAS-Funktion</strong></a> der GINA auf, sodass die GINA die Identifikations- und Authentifizierungsinformationen eines Benutzers verarbeiten kann.<br/> Wenn die Anmeldung erfolgreich ist, befindet sich Winlogon im Status "Angemeldet".<br/></li>
</ol></td>
</tr>
<tr class="odd">
<td>Der Benutzer ist angemeldet.</td>
<td>(Die GINA überwacht Geräte auf SAS-Ereignisse.)
<ol>
<li>Die GINA ruft die <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify-Funktion</strong></a> von Winlogon auf, wenn ein SAS-Ereignis empfangen wurde.</li>
<li>Winlogon ruft die <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedonsas"><strong>WlxLoggedOnSAS-Funktion</strong></a> der GINA auf, sodass die GINA dem Benutzer, der derzeit angemeldet ist, Optionen präsentieren kann.</li>
</ol></td>
</tr>
<tr class="even">
<td>Der Benutzer ist angemeldet und möchte den Computer sperren.</td>
<td>(Die GINA überwacht Geräte auf SAS-Ereignisse.)
<ol>
<li>Die GINA ruft die <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify-Funktion</strong></a> auf.</li>
<li>Winlogon ruft die <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedonsas"><strong>WlxLoggedOnSAS-Funktion</strong></a> der GINA auf.</li>
<li>Die GINA gibt WLX_SAS_ACTION_LOCK_WKSTA zurück.<br/> Winlogon befindet sich im Zustand "Arbeitsstation gesperrt".<br/></li>
</ol></td>
</tr>
<tr class="odd">
<td>Der Benutzer ist angemeldet, die Arbeitsstation ist gesperrt, und der Benutzer möchte den Computer entsperren.</td>
<td>(Die GINA überwacht Geräte auf SAS-Ereignisse.)
<ol>
<li>Die GINA ruft die <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify-Funktion</strong></a> auf.</li>
<li>Winlogon ruft die <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxwkstalockedsas"><strong>WlxWkstaLockedSAS-Funktion</strong></a> der GINA auf.</li>
<li>Die GINA gibt WLX_SAS_ACTION_UNLOCK_WKSTA zurück.</li>
</ol></td>
</tr>
<tr class="even">
<td>Der Benutzer ist angemeldet, und das Programm ruft die <a href="/windows/desktop/api/winuser/nf-winuser-exitwindowsex"><strong>ExitWindowsEx-Funktion</strong></a> auf.</td>
<td>Winlogon ruft die <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxlogoff"><strong>WlxLogoff-Funktion</strong></a> der GINA auf.</td>
</tr>
<tr class="odd">
<td>Der Benutzer ist angemeldet und möchte sich mit sas abmelden.</td>
<td>(Die GINA überwacht Geräte auf SAS-Ereignisse.)
<ol>
<li>Die GINA ruft die <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify-Funktion</strong></a> auf.</li>
<li>Winlogon ruft die <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedonsas"><strong>WlxLoggedOnSAS-Funktion</strong></a> der GINA auf.</li>
<li>Die GINA gibt WLX_SAS_ACTION_LOGOFF zurück.</li>
<li>Winlogon ruft die <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxlogoff"><strong>WlxLogoff-Funktion</strong></a> der GINA auf.</li>
</ol></td>
</tr>
<tr class="even">
<td>Der Benutzer ist angemeldet und möchte sich mit <a href="/windows/desktop/api/winuser/nf-winuser-exitwindowsex"> <strong>ExitWindowsEx abmelden</strong> und herunterfahren.</a></td>
<td><ol>
<li>Winlogon ruft die <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxlogoff"><strong>WlxLogoff-Funktion</strong></a> der GINA auf.</li>
<li>Winlogon ruft die <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxshutdown"><strong>WlxShutdown-Funktion</strong></a> der GINA auf.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Der Benutzer ist angemeldet und möchte sich mit sas abmelden und herunterfahren.</td>
<td>(Die GINA überwacht Geräte auf SAS-Ereignisse.)
<ol>
<li>Die GINA ruft die <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify-Funktion</strong></a> auf.</li>
<li>Winlogon ruft die <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedonsas"><strong>WlxLoggedOnSAS-Funktion</strong></a> der GINA auf.</li>
<li>Die GINA gibt WLX_SAS_ACTION_SHUTDOWN zurück.</li>
<li>Winlogon ruft die <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxlogoff"><strong>WlxLogoff-Funktion</strong></a> der GINA auf.</li>
<li>Winlogon ruft die <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxshutdown"><strong>WlxShutdown-Funktion</strong></a> der GINA auf.</li>
</ol></td>
</tr>
</tbody>
</table>



 

 

 
