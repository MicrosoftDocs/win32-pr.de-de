---
description: Native WiFi-API-Berechtigungen
ms.assetid: cfea9f7d-a069-497b-8138-b3949002fa5d
title: Native WiFi-API-Berechtigungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afafec7619e0920a17e3769a430c8c79aeff3828
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215900"
---
# <a name="native-wifi-api-permissions"></a>Native WiFi-API-Berechtigungen

Ein nativer WiFi-API-Aufruf schlägt möglicherweise fehl, wenn ein Aufrufer nicht über die erforderlichen Berechtigungen zum Ausführen des angeforderten Vorgangs verfügt.

Berechtigungen werden in einer freigegebenen [Zugriffs Steuerungs Liste (DACL)](../secauthz/access-control-lists.md) gespeichert, die einem Sicherungs [**fähigen WLAN- \_ \_ Objekt**](/windows/desktop/api/wlanapi/ne-wlanapi-wlan_securable_object)zugeordnet ist. Weitere Informationen zu DACLs und Sicherungs fähigen Objekten finden Sie unter [Steuern des Zugriffs auf ein Objekt durch DACLs](../secauthz/how-dacls-control-access-to-an-object.md).

Die folgende Tabelle zeigt die systemeigenen WiFi-Funktionen, die Sicherungs fähige Objekte verwenden, um zu bestimmen, ob der Aufrufer über ausreichende Berechtigungen zum Ausführen des angeforderten Vorgangs verfügt. Außerdem werden die Sicherungs fähigen Objekte angezeigt, die von den einzelnen Funktionen verwendet werden.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Funktion</th>
<th>Sicherungs fähiges Objekt</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlangetfilterlist"><strong>Wlangetfilterlist</strong></a>, <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetfilterlist"> <strong>wlansetfilterlist</strong></a><br/></td>
<td><ul>
<li>wlan_secure_deny_list</li>
<li>wlan_secure_permit_list</li>
</ul></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanihvcontrol"><strong>Wlanihvcontrol</strong></a><br/></td>
<td><ul>
<li>wlan_secure_ihv_control</li>
</ul></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryautoconfigparameter"><strong>Wlanqueryautoconfigparameter</strong></a>, <a href="/windows/desktop/api/Wlanapi/nf-wlanapi-wlansetautoconfigparameter"> <strong>wlanabtaureconfigparameter</strong></a><br/></td>
<td><ul>
<li>wlan_secure_show_denied</li>
</ul></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryinterface"><strong>Wlanqueryinterface</strong></a>, <a href="/windows/desktop/api/Wlanapi/nf-wlanapi-wlansetinterface"> <strong>wlansetinterface</strong></a><br/></td>
<td><ul>
<li>wlan_secure_ac_enabled</li>
<li>wlan_secure_bc_scan_enabled</li>
<li>wlan_secure_bss_type</li>
<li>wlan_secure_current_operation_mode</li>
<li>wlan_secure_interface_properties</li>
<li>wlan_secure_media_streaming_mode_enabled</li>
</ul></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile"><strong>WLanSetProfile</strong></a><br/></td>
<td><ul>
<li>wlan_secure_add_new_all_user_profiles</li>
<li>wlan_secure_add_new_per_user_profiles</li>
</ul></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofilelist"><strong>Wlansetprofilelist</strong></a>, <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofileposition"> <strong>wlansetprofileposition</strong></a><br/></td>
<td><ul>
<li>wlan_secure_all_user_profiles_order</li>
</ul></td>
</tr>
</tbody>
</table>



 

Bevor einer der oben genannten Funktionen den Vorgang abschließt, ruft die Funktion die DACL ab, die im entsprechenden Sicherungs fähigen Objekt gespeichert ist. Die-Funktion überprüft dann die DACL, um festzustellen, ob der Aufrufer über ausreichende Berechtigungen verfügt. Die wlanget \* -und wlanquery- \* Funktionen erfordern, dass die DACL einen [Zugriffs Steuerungs Eintrag (ACE)](../secauthz/access-control-entries.md) enthält [](../secauthz/access-tokens.md) , der dem aufrufenden Thread WLAN \_ Lese \_ Zugriff auf die Funktion gewährt. Die wlanset- \* Funktionen erfordern einen ACE, der das Zugriffs Token für den Schreibzugriff des aufrufenden Threads gewährt \_ \_ . Wenn der Aufrufer nicht über ausreichende Berechtigungen verfügt, schlägt der Funktionsaufruf mit der Fehlermeldung " \_ Zugriff verweigert" fehl \_ .

Jedem Sicherungs fähigen Objekt ist standardmäßig eine DACL zugeordnet. Die in der DACL gespeicherten Standard Berechtigungen können mithilfe der [**wlansetsecuritysettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetsecuritysettings) -Funktion geändert werden. Zum Ermitteln der effektiven Benutzerrechte, die erforderlich sind, um einen Vorgang auf einem bestimmten System auszuführen, nennen Sie [**wlangetsecuritysettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetsecuritysettings).

Alle Benutzerprofile verfügen über zusätzliche Berechtigungen, die dem Profil selbst zugeordnet sind. Die Berechtigungen für ein Profil für alle Benutzer werden festgelegt, wenn das Profil mithilfe von [**WLanSetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile) oder [**wlansavetemporaryprofile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansavetemporaryprofile)erstellt oder geändert wird. Der Parameter " *straualluserprofilesecurity* " gibt die erforderlichen Berechtigungen zum Ändern eines Profils, zum Löschen eines Profils oder zum Herstellen einer Verbindung mit einem Netzwerk mithilfe eines Profils an. Das Löschen oder Ändern eines Profils erfordert die WLAN- \_ Schreib \_ Zugriffsberechtigung. Zum Herstellen einer Verbindung mit einem Netzwerk mithilfe eines Profils ist die WLAN- \_ Berechtigung zum Ausführen von \_ Zugriffs

* * Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2: * * die [**wlangetsecuritysettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetsecuritysettings) -und [**wlansetsecuritysettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetsecuritysettings) -Funktionen werden nicht unterstützt. Der *Parameter* "" "" "" "" "" "" "" ".

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Steuern des Zugriffs auf ein Objekt durch DACLs](../secauthz/how-dacls-control-access-to-an-object.md)
</dt> <dt>

[**Sicherungs \_ fähiges WLAN- \_ Objekt**](/windows/desktop/api/wlanapi/ne-wlanapi-wlan_securable_object)
</dt> </dl>

 

 
