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
# <a name="native-wifi-api-permissions"></a><span data-ttu-id="df3b3-103">Native WiFi-API-Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="df3b3-103">Native Wifi API Permissions</span></span>

<span data-ttu-id="df3b3-104">Ein nativer WiFi-API-Aufruf schlägt möglicherweise fehl, wenn ein Aufrufer nicht über die erforderlichen Berechtigungen zum Ausführen des angeforderten Vorgangs verfügt.</span><span class="sxs-lookup"><span data-stu-id="df3b3-104">A Native Wifi API call may fail with when a caller does not have adequate permissions to perform the requested operation.</span></span>

<span data-ttu-id="df3b3-105">Berechtigungen werden in einer freigegebenen [Zugriffs Steuerungs Liste (DACL)](../secauthz/access-control-lists.md) gespeichert, die einem Sicherungs [**fähigen WLAN- \_ \_ Objekt**](/windows/desktop/api/wlanapi/ne-wlanapi-wlan_securable_object)zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="df3b3-105">Permissions are stored in a [discretionary access control lists (DACL)](../secauthz/access-control-lists.md) associated with a [**WLAN\_SECURABLE\_OBJECT**](/windows/desktop/api/wlanapi/ne-wlanapi-wlan_securable_object).</span></span> <span data-ttu-id="df3b3-106">Weitere Informationen zu DACLs und Sicherungs fähigen Objekten finden Sie unter [Steuern des Zugriffs auf ein Objekt durch DACLs](../secauthz/how-dacls-control-access-to-an-object.md).</span><span class="sxs-lookup"><span data-stu-id="df3b3-106">For more information about DACLs and securable objects, see [How DACLs Control Access to an Object](../secauthz/how-dacls-control-access-to-an-object.md).</span></span>

<span data-ttu-id="df3b3-107">Die folgende Tabelle zeigt die systemeigenen WiFi-Funktionen, die Sicherungs fähige Objekte verwenden, um zu bestimmen, ob der Aufrufer über ausreichende Berechtigungen zum Ausführen des angeforderten Vorgangs verfügt.</span><span class="sxs-lookup"><span data-stu-id="df3b3-107">The following table shows the Native Wifi functions that use securable objects to determine if the caller has sufficient permissions to perform the requested operation.</span></span> <span data-ttu-id="df3b3-108">Außerdem werden die Sicherungs fähigen Objekte angezeigt, die von den einzelnen Funktionen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="df3b3-108">It also shows the securable objects used by each function.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="df3b3-109">Funktion</span><span class="sxs-lookup"><span data-stu-id="df3b3-109">Function</span></span></th>
<th><span data-ttu-id="df3b3-110">Sicherungs fähiges Objekt</span><span class="sxs-lookup"><span data-stu-id="df3b3-110">Securable object</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="df3b3-111"><a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlangetfilterlist"><strong>Wlangetfilterlist</strong></a>, <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetfilterlist"> <strong>wlansetfilterlist</strong></a></span><span class="sxs-lookup"><span data-stu-id="df3b3-111"><a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlangetfilterlist"><strong>WlanGetFilterList</strong></a>, <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetfilterlist"><strong>WlanSetFilterList</strong></a></span></span><br/></td>
<td><ul>
<li><span data-ttu-id="df3b3-112">wlan_secure_deny_list</span><span class="sxs-lookup"><span data-stu-id="df3b3-112">wlan_secure_deny_list</span></span></li>
<li><span data-ttu-id="df3b3-113">wlan_secure_permit_list</span><span class="sxs-lookup"><span data-stu-id="df3b3-113">wlan_secure_permit_list</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="df3b3-114"><a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanihvcontrol"><strong>Wlanihvcontrol</strong></a></span><span class="sxs-lookup"><span data-stu-id="df3b3-114"><a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanihvcontrol"><strong>WlanIhvControl</strong></a></span></span><br/></td>
<td><ul>
<li><span data-ttu-id="df3b3-115">wlan_secure_ihv_control</span><span class="sxs-lookup"><span data-stu-id="df3b3-115">wlan_secure_ihv_control</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="df3b3-116"><a href="/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryautoconfigparameter"><strong>Wlanqueryautoconfigparameter</strong></a>, <a href="/windows/desktop/api/Wlanapi/nf-wlanapi-wlansetautoconfigparameter"> <strong>wlanabtaureconfigparameter</strong></a></span><span class="sxs-lookup"><span data-stu-id="df3b3-116"><a href="/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryautoconfigparameter"><strong>WlanQueryAutoConfigParameter</strong></a>, <a href="/windows/desktop/api/Wlanapi/nf-wlanapi-wlansetautoconfigparameter"><strong>WlanSetAutoConfigParameter</strong></a></span></span><br/></td>
<td><ul>
<li><span data-ttu-id="df3b3-117">wlan_secure_show_denied</span><span class="sxs-lookup"><span data-stu-id="df3b3-117">wlan_secure_show_denied</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="df3b3-118"><a href="/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryinterface"><strong>Wlanqueryinterface</strong></a>, <a href="/windows/desktop/api/Wlanapi/nf-wlanapi-wlansetinterface"> <strong>wlansetinterface</strong></a></span><span class="sxs-lookup"><span data-stu-id="df3b3-118"><a href="/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryinterface"><strong>WlanQueryInterface</strong></a>, <a href="/windows/desktop/api/Wlanapi/nf-wlanapi-wlansetinterface"><strong>WlanSetInterface</strong></a></span></span><br/></td>
<td><ul>
<li><span data-ttu-id="df3b3-119">wlan_secure_ac_enabled</span><span class="sxs-lookup"><span data-stu-id="df3b3-119">wlan_secure_ac_enabled</span></span></li>
<li><span data-ttu-id="df3b3-120">wlan_secure_bc_scan_enabled</span><span class="sxs-lookup"><span data-stu-id="df3b3-120">wlan_secure_bc_scan_enabled</span></span></li>
<li><span data-ttu-id="df3b3-121">wlan_secure_bss_type</span><span class="sxs-lookup"><span data-stu-id="df3b3-121">wlan_secure_bss_type</span></span></li>
<li><span data-ttu-id="df3b3-122">wlan_secure_current_operation_mode</span><span class="sxs-lookup"><span data-stu-id="df3b3-122">wlan_secure_current_operation_mode</span></span></li>
<li><span data-ttu-id="df3b3-123">wlan_secure_interface_properties</span><span class="sxs-lookup"><span data-stu-id="df3b3-123">wlan_secure_interface_properties</span></span></li>
<li><span data-ttu-id="df3b3-124">wlan_secure_media_streaming_mode_enabled</span><span class="sxs-lookup"><span data-stu-id="df3b3-124">wlan_secure_media_streaming_mode_enabled</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="df3b3-125"><a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile"><strong>WLanSetProfile</strong></a></span><span class="sxs-lookup"><span data-stu-id="df3b3-125"><a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile"><strong>WlanSetProfile</strong></a></span></span><br/></td>
<td><ul>
<li><span data-ttu-id="df3b3-126">wlan_secure_add_new_all_user_profiles</span><span class="sxs-lookup"><span data-stu-id="df3b3-126">wlan_secure_add_new_all_user_profiles</span></span></li>
<li><span data-ttu-id="df3b3-127">wlan_secure_add_new_per_user_profiles</span><span class="sxs-lookup"><span data-stu-id="df3b3-127">wlan_secure_add_new_per_user_profiles</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="df3b3-128"><a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofilelist"><strong>Wlansetprofilelist</strong></a>, <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofileposition"> <strong>wlansetprofileposition</strong></a></span><span class="sxs-lookup"><span data-stu-id="df3b3-128"><a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofilelist"><strong>WlanSetProfileList</strong></a>, <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofileposition"><strong>WlanSetProfilePosition</strong></a></span></span><br/></td>
<td><ul>
<li><span data-ttu-id="df3b3-129">wlan_secure_all_user_profiles_order</span><span class="sxs-lookup"><span data-stu-id="df3b3-129">wlan_secure_all_user_profiles_order</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="df3b3-130">Bevor einer der oben genannten Funktionen den Vorgang abschließt, ruft die Funktion die DACL ab, die im entsprechenden Sicherungs fähigen Objekt gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="df3b3-130">Before one of the above-named functions completes its operation, the function retrieves the DACL stored in the appropriate securable object.</span></span> <span data-ttu-id="df3b3-131">Die-Funktion überprüft dann die DACL, um festzustellen, ob der Aufrufer über ausreichende Berechtigungen verfügt.</span><span class="sxs-lookup"><span data-stu-id="df3b3-131">The function then checks the DACL to see if the caller has sufficient permissions.</span></span> <span data-ttu-id="df3b3-132">Die wlanget \* -und wlanquery- \* Funktionen erfordern, dass die DACL einen [Zugriffs Steuerungs Eintrag (ACE)](../secauthz/access-control-entries.md) enthält [](../secauthz/access-tokens.md) , der dem aufrufenden Thread WLAN \_ Lese \_ Zugriff auf die Funktion gewährt.</span><span class="sxs-lookup"><span data-stu-id="df3b3-132">The WlanGet\* and WlanQuery\* functions require that the DACL contains an [access control entry (ACE)](../secauthz/access-control-entries.md) that grants the [access token](../secauthz/access-tokens.md) of the calling thread WLAN\_READ\_ACCESS to the function.</span></span> <span data-ttu-id="df3b3-133">Die wlanset- \* Funktionen erfordern einen ACE, der das Zugriffs Token für den Schreibzugriff des aufrufenden Threads gewährt \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="df3b3-133">The WlanSet\* functions require an ACE that grants the access token of the calling thread WLAN\_WRITE\_ACCESS.</span></span> <span data-ttu-id="df3b3-134">Wenn der Aufrufer nicht über ausreichende Berechtigungen verfügt, schlägt der Funktionsaufruf mit der Fehlermeldung " \_ Zugriff verweigert" fehl \_ .</span><span class="sxs-lookup"><span data-stu-id="df3b3-134">If the caller does not have sufficient permissions, the function call fails with the error ERROR\_ACCESS\_DENIED.</span></span>

<span data-ttu-id="df3b3-135">Jedem Sicherungs fähigen Objekt ist standardmäßig eine DACL zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="df3b3-135">Each securable object has a DACL associated with it by default.</span></span> <span data-ttu-id="df3b3-136">Die in der DACL gespeicherten Standard Berechtigungen können mithilfe der [**wlansetsecuritysettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetsecuritysettings) -Funktion geändert werden.</span><span class="sxs-lookup"><span data-stu-id="df3b3-136">The default permissions stored in the DACL can be changed using the [**WlanSetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetsecuritysettings) function.</span></span> <span data-ttu-id="df3b3-137">Zum Ermitteln der effektiven Benutzerrechte, die erforderlich sind, um einen Vorgang auf einem bestimmten System auszuführen, nennen Sie [**wlangetsecuritysettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetsecuritysettings).</span><span class="sxs-lookup"><span data-stu-id="df3b3-137">To determine the effective user rights required to perform an operation on a particular system, call [**WlanGetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetsecuritysettings).</span></span>

<span data-ttu-id="df3b3-138">Alle Benutzerprofile verfügen über zusätzliche Berechtigungen, die dem Profil selbst zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="df3b3-138">All-user profiles have additional permissions associated with the profile itself.</span></span> <span data-ttu-id="df3b3-139">Die Berechtigungen für ein Profil für alle Benutzer werden festgelegt, wenn das Profil mithilfe von [**WLanSetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile) oder [**wlansavetemporaryprofile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansavetemporaryprofile)erstellt oder geändert wird.</span><span class="sxs-lookup"><span data-stu-id="df3b3-139">The permissions on an all-user profile are established when the profile is created or modified using [**WlanSetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile) or [**WlanSaveTemporaryProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansavetemporaryprofile).</span></span> <span data-ttu-id="df3b3-140">Der Parameter " *straualluserprofilesecurity* " gibt die erforderlichen Berechtigungen zum Ändern eines Profils, zum Löschen eines Profils oder zum Herstellen einer Verbindung mit einem Netzwerk mithilfe eines Profils an.</span><span class="sxs-lookup"><span data-stu-id="df3b3-140">The *strAllUserProfileSecurity* parameter specifies the required permissions for modifying a profile, deleting a profile, or connecting to a network using a profile.</span></span> <span data-ttu-id="df3b3-141">Das Löschen oder Ändern eines Profils erfordert die WLAN- \_ Schreib \_ Zugriffsberechtigung.</span><span class="sxs-lookup"><span data-stu-id="df3b3-141">Deleting or modifying a profile requires WLAN\_WRITE\_ACCESS permission.</span></span> <span data-ttu-id="df3b3-142">Zum Herstellen einer Verbindung mit einem Netzwerk mithilfe eines Profils ist die WLAN- \_ Berechtigung zum Ausführen von \_ Zugriffs</span><span class="sxs-lookup"><span data-stu-id="df3b3-142">Connecting to a network using a profile requires WLAN\_EXECUTE\_ACCESS permission.</span></span>

<span data-ttu-id="df3b3-143">\* \* Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2: \* \* die [**wlangetsecuritysettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetsecuritysettings) -und [**wlansetsecuritysettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetsecuritysettings) -Funktionen werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="df3b3-143">\*\*Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:  \*\* The [**WlanGetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetsecuritysettings) and [**WlanSetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetsecuritysettings) functions are not supported.</span></span> <span data-ttu-id="df3b3-144">Der *Parameter* "" "" "" "" "" "" "" ".</span><span class="sxs-lookup"><span data-stu-id="df3b3-144">The *strAllUserProfileSecurity* parameter is not used.</span></span>

## <a name="related-topics"></a><span data-ttu-id="df3b3-145">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="df3b3-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="df3b3-146">Steuern des Zugriffs auf ein Objekt durch DACLs</span><span class="sxs-lookup"><span data-stu-id="df3b3-146">How DACLs Control Access to an Object</span></span>](../secauthz/how-dacls-control-access-to-an-object.md)
</dt> <dt>

[<span data-ttu-id="df3b3-147">**Sicherungs \_ fähiges WLAN- \_ Objekt**</span><span class="sxs-lookup"><span data-stu-id="df3b3-147">**WLAN\_SECURABLE\_OBJECT**</span></span>](/windows/desktop/api/wlanapi/ne-wlanapi-wlan_securable_object)
</dt> </dl>

 

 
