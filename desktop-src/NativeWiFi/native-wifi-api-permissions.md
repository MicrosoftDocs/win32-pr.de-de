---
description: Native WIFI-API-Berechtigungen
ms.assetid: cfea9f7d-a069-497b-8138-b3949002fa5d
title: Native WIFI-API-Berechtigungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da56faac08b40ace46ef1e33c5d5644be87b45c6
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480726"
---
# <a name="native-wifi-api-permissions"></a>Native WIFI-API-Berechtigungen

Ein Native Wifi-API-Aufruf schlägt möglicherweise mit fehl, wenn ein Aufrufer nicht über ausreichende Berechtigungen zum Ausführen des angeforderten Vorgangs verfügt.

Berechtigungen werden in einer [DACL (Discretionary Access Control Lists)](../secauthz/access-control-lists.md) gespeichert, die einem [**WLAN \_ SECURABLE \_ OBJECT**](/windows/desktop/api/wlanapi/ne-wlanapi-wlan_securable_object)zugeordnet ist. Weitere Informationen zu DACLs und sicherungsfähigen Objekten finden Sie unter Steuern des Zugriffs auf ein Objekt durch [DACLs.](../secauthz/how-dacls-control-access-to-an-object.md)

Die folgende Tabelle zeigt die nativen Wifi-Funktionen, die sicherungsfähige Objekte verwenden, um zu bestimmen, ob der Aufrufer über ausreichende Berechtigungen zum Ausführen des angeforderten Vorgangs verfügt. Außerdem werden die sicherungsfähigen Objekte angezeigt, die von den einzelnen Funktionen verwendet werden.




| Funktion | Sicherungsfähiges Objekt | 
|----------|------------------|
| <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlangetfilterlist"><strong>WlanGetFilterList,</strong></a> <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetfilterlist"> <strong>WlanSetFilterList</strong></a><br /> | <ul><li>wlan_secure_deny_list</li><li>wlan_secure_permit_list</li></ul> | 
| <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanihvcontrol"><strong>WlanIhvControl</strong></a><br /> | <ul><li>wlan_secure_ihv_control</li></ul> | 
| <a href="/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryautoconfigparameter"><strong>WlanQueryAutoConfigParameter</strong></a>, <a href="/windows/desktop/api/Wlanapi/nf-wlanapi-wlansetautoconfigparameter"> <strong>WlanSetAutoConfigParameter</strong></a><br /> | <ul><li>wlan_secure_show_denied</li></ul> | 
| <a href="/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryinterface"><strong>WlanQueryInterface,</strong></a> <a href="/windows/desktop/api/Wlanapi/nf-wlanapi-wlansetinterface"> <strong>WlanSetInterface</strong></a><br /> | <ul><li>wlan_secure_ac_enabled</li><li>wlan_secure_bc_scan_enabled</li><li>wlan_secure_bss_type</li><li>wlan_secure_current_operation_mode</li><li>wlan_secure_interface_properties</li><li>wlan_secure_media_streaming_mode_enabled</li></ul> | 
| <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile"><strong>WlanSetProfile</strong></a><br /> | <ul><li>wlan_secure_add_new_all_user_profiles</li><li>wlan_secure_add_new_per_user_profiles</li></ul> | 
| <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofilelist"><strong>WlanSetProfileList,</strong></a> <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofileposition"> <strong>WlanSetProfilePosition</strong></a><br /> | <ul><li>wlan_secure_all_user_profiles_order</li></ul> | 




 

Bevor eine der oben genannten Funktionen ihren Vorgang abschließt, ruft die Funktion die im entsprechenden sicherungsfähigen Objekt gespeicherte DACL ab. Die Funktion überprüft dann die DACL, um festzustellen, ob der Aufrufer über ausreichende Berechtigungen verfügt. Die \* WlanGet- und \* WlanQuery-Funktionen erfordern, dass die DACL einen [Zugriffssteuerungseintrag (ACE)](../secauthz/access-control-entries.md) enthält, der das [Zugriffstoken](../secauthz/access-tokens.md) des aufrufenden Threads WLAN \_ READ ACCESS für die Funktion \_ gewährt. Die \* WlanSet-Funktionen erfordern einen ACE, der das Zugriffstoken des aufrufenden Threads WLAN \_ WRITE ACCESS \_ gewährt. Wenn der Aufrufer nicht über ausreichende Berechtigungen verfügt, schlägt der Funktionsaufruf mit dem Fehler ERROR \_ ACCESS \_ DENIED fehl.

Jedem sicherungsfähigen Objekt ist standardmäßig eine DACL zugeordnet. Die in der DACL gespeicherten Standardberechtigungen können mithilfe der [**WlanSetSecuritySettings-Funktion**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetsecuritysettings) geändert werden. Um die effektiven Benutzerrechte zu bestimmen, die zum Ausführen eines Vorgangs auf einem bestimmten System erforderlich sind, rufen Sie [**WlanGetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetsecuritysettings)auf.

Alle Benutzerprofile verfügen über zusätzliche Berechtigungen, die dem Profil selbst zugeordnet sind. Die Berechtigungen für ein Benutzerprofil werden eingerichtet, wenn das Profil mithilfe von [**WlanSetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile) oder [**WlanSaveTemporaryProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansavetemporaryprofile)erstellt oder geändert wird. Der *parameter strAllUserProfileSecurity* gibt die erforderlichen Berechtigungen zum Ändern eines Profils, Löschen eines Profils oder Herstellen einer Verbindung mit einem Netzwerk mithilfe eines Profils an. Zum Löschen oder Ändern eines Profils ist die WLAN \_ WRITE \_ ACCESS-Berechtigung erforderlich. Zum Herstellen einer Verbindung mit einem Netzwerk mithilfe eines Profils ist die EXECUTE \_ \_ ACCESS-WLAN-Berechtigung erforderlich.

**Windows XP mit SP3 und Wlan-LAN-API für Windows XP mit SP2: ** Die Funktionen [**WlanGetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetsecuritysettings) und [**WlanSetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetsecuritysettings) werden nicht unterstützt. Der *parameter strAllUserProfileSecurity* wird nicht verwendet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Steuern des Zugriffs auf ein Objekt durch DACLs](../secauthz/how-dacls-control-access-to-an-object.md)
</dt> <dt>

[**\_SICHERUNGSFÄHIGES \_ WLAN-OBJEKT**](/windows/desktop/api/wlanapi/ne-wlanapi-wlan_securable_object)
</dt> </dl>

 

 
