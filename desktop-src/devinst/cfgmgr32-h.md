---
title: 'Cfgmgr32.h '
description: Dieser Abschnitt enthält Referenzthemen für den Cfgmgr32.h-Header.
ms.assetid: 73b4b2ec-ce3d-47c1-9b0e-1052f390ae94
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cd09a0e905b85d2eae52bb267929d2e1e89e5c6c179a8d6ab4de00320e9f8f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118541424"
---
# <a name="cfgmgr32h"></a>Cfgmgr32.h 

Dieser Abschnitt enthält Referenzthemen für den Cfgmgr32.h-Header.

## <a name="in-this-section"></a>In diesem Abschnitt



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Thema</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-busnumber_des"><strong>BUSNUMBER_DES</strong></a><br/></td>
<td>Die BUSNUMBER_DES-Struktur wird verwendet, um entweder eine Ressourcenliste oder eine Ressourcenanforderungenliste anzugeben, die die Nutzung der Busnummer für eine Geräteinstanz beschreibt. Weitere Informationen zu Ressourcenlisten und Ressourcenanforderungen finden Sie unter <a href="/windows-hardware/drivers/kernel/hardware-resources">Hardwareressourcen</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-busnumber_range"><strong>BUSNUMBER_RANGE</strong></a><br/></td>
<td>Die BUSNUMBER_RANGE-Struktur gibt eine Ressourcenanforderungenliste an, die die Nutzung der Busnummer für eine Geräteinstanz beschreibt. Weitere Informationen zu Ressourcenanforderungen finden Sie unter <a href="/windows-hardware/drivers/kernel/hardware-resources">Hardwareressourcen.</a><br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-busnumber_resource"><strong>BUSNUMBER_RESOURCE</strong></a><br/></td>
<td>Die BUSNUMBER_RESOURCE-Struktur gibt entweder eine Ressourcenliste oder eine Ressourcenanforderungenliste an, die die Nutzung der Busnummer für eine Geräteinstanz beschreibt. Weitere Informationen zu Ressourcenlisten und Ressourcenanforderungen finden Sie unter <a href="/windows-hardware/drivers/kernel/hardware-resources">Hardwareressourcen</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_add_empty_log_conf"><strong>CM_Add_Empty_Log_Conf</strong></a><br/></td>
<td>Die <strong>CM_Add_Empty_Log_Conf</strong> erstellt eine leere logische Konfiguration <a href="/windows-hardware/drivers/kernel/hardware-resources">für</a>einen angegebenen Konfigurationstyp und eine angegebene Geräteinstanz auf dem lokalen Computer.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_add_empty_log_conf_ex"><strong>CM_Add_Empty_Log_Conf_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Ab Windows 8 und Windows Server 2012 ist diese Funktion veraltet. Verwenden Sie <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_add_empty_log_conf"><strong>CM_Add_Empty_Log_Conf.</strong></a>
</blockquote>
<br/> Die <strong>CM_Add_Empty_Log_Conf_Ex-Funktion</strong> erstellt <a href="/windows-hardware/drivers/kernel/hardware-resources"></a>eine leere logische Konfiguration für einen angegebenen Konfigurationstyp und eine angegebene Geräteinstanz auf dem lokalen computer oder einem Remotecomputer.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_add_idw"><strong>CM_Add_ID</strong></a><br/></td>
<td>Die <strong>CM_Add_ID-Funktion</strong> fügt eine angegebene Geräte-ID (sofern noch <a href="/windows-hardware/drivers/"></a> nicht vorhanden) an die Hardware-ID-Liste oder kompatible <a href="/windows-hardware/drivers/install/device-ids"></a> <a href="/windows-hardware/drivers/install/compatible-ids">ID-Liste einer Geräteinstanz</a> an. <a href="/windows-hardware/drivers/install/hardware-ids"></a><br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_add_id_exw"><strong>CM_Add_ID_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Ab Windows 8 und Windows Server 2012 ist diese Funktion veraltet. Verwenden Sie <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_add_idw"><strong>CM_Add_ID.</strong></a>
</blockquote>
<br/> Die <strong>CM_Add_ID_Ex-Funktion</strong> fügt eine <a href="/windows-hardware/drivers/install/device-ids">Geräte-ID</a> (sofern noch nicht vorhanden) an die <a href="/windows-hardware/drivers/install/hardware-ids">Hardware-ID-Liste</a> oder kompatible <a href="/windows-hardware/drivers/install/compatible-ids">ID-Liste</a> einer Geräteinstanz an, entweder auf dem lokalen Computer oder einem Remotecomputer.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_add_res_des"><strong>CM_Add_Res_Des</strong></a><br/></td>
<td>Die <strong>CM_Add_Res_Des-Funktion</strong> fügt einer <a href="/windows-hardware/drivers/">logischen</a> Konfiguration einen <a href="/windows-hardware/drivers/kernel/hardware-resources">Ressourcendeskriptor hinzu.</a><br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_add_res_des_ex"><strong>CM_Add_Res_Des_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Ab Windows 8 und Windows Server 2012 ist diese Funktion veraltet. Verwenden Sie <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_add_res_des"><strong>stattdessen CM_Add_Res_Des.</strong></a>
</blockquote>
<br/> Die <strong>CM_Add_Res_Des_Ex-Funktion</strong> fügt einer <a href="/windows-hardware/drivers/">logischen</a> Konfiguration einen <a href="/windows-hardware/drivers/kernel/hardware-resources">Ressourcendeskriptor hinzu.</a> Die logische Konfiguration kann entweder auf dem lokalen Computer oder auf einem Remotecomputer verwendet werden.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_connect_machinew"><strong>CM_Connect_Machine</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Ab Windows 8 und Windows Server 2012 Funktionalität für den Zugriff auf Remotecomputer entfernt. Sie können nicht auf Remotecomputer zugreifen, wenn Sie auf diesen Versionen von Windows.
</blockquote>
<br/> Die <strong>CM_Connect_Machine-Funktion</strong> erstellt eine Verbindung mit einem Remotecomputer.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_delete_class_key"><strong>CM_Delete_Class_Key</strong></a><br/></td>
<td>Die <strong>CM_Delete_Class_Key-Funktion</strong> entfernt die angegebene installierte <a href="/windows-hardware/drivers/">Geräteklasse</a> aus dem System.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_delete_device_interface_keyw"><strong>CM_Delete_Device_Interface_Key</strong></a><br/></td>
<td>Die <strong>CM_Delete_Device_Interface_Key-Funktion</strong> löscht den Registrierungsunterschlüssel, der von Anwendungen und Treibern zum Speichern schnittstellenspezifischer Informationen verwendet wird.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_delete_device_interface_key_exa"><strong>CM_Delete_Device_Interface_Key_ExA</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Ab Windows 8 und Windows Server 2012 ist diese Funktion veraltet. Verwenden Sie <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_delete_device_interface_keyw"><strong>stattdessen CM_Delete_Device_Interface_Key.</strong></a>
</blockquote>
<br/> Die <strong>CM_Delete_Device_Interface_Key_ExA-Funktion</strong> löscht den Registrierungsunterschlüssel, der von Anwendungen und Treibern zum Speichern schnittstellenspezifischer Informationen verwendet wird.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_delete_device_interface_key_exw"><strong>CM_Delete_Device_Interface_Key_ExW</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Ab Windows 8 und Windows Server 2012 ist diese Funktion veraltet. Verwenden Sie <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_delete_device_interface_keyw"><strong>stattdessen CM_Delete_Device_Interface_Key.</strong></a>
</blockquote>
<br/> Die <strong>CM_Delete_Device_Interface_Key_ExW-Funktion</strong> löscht den Registrierungsunterschlüssel, der von Anwendungen und Treibern zum Speichern schnittstellenspezifischer Informationen verwendet wird.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_delete_devnode_key"><strong>CM_Delete_DevNode_Key</strong></a><br/></td>
<td>Die <strong>CM_Delete_DevNode_Key-Funktion</strong> löscht die angegebenen registrierungsschlüssel, auf die benutzer zugegriffen werden kann, die einem Gerät zugeordnet sind.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_disable_devnode"><strong>CM_Disable_DevNode</strong></a><br/></td>
<td>Die <strong>CM_Disable_DevNode</strong> deaktiviert ein Gerät.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_disconnect_machine"><strong>CM_Disconnect_Machine</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Ab Windows 8 und Windows Server 2012 Funktionalität für den Zugriff auf Remotecomputer entfernt. Sie können nicht auf Remotecomputer zugreifen, wenn Sie auf diesen Versionen von Windows.
</blockquote>
<br/> Die <strong>CM_Disconnect_Machine-Funktion</strong> entfernt eine Verbindung mit einem Remotecomputer.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_enable_devnode"><strong>CM_Enable_DevNode</strong></a><br/></td>
<td>Die <strong>CM_Enable_DevNode-Funktion</strong> aktiviert ein Gerät.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_enumerate_classes"><strong>CM_Enumerate_Classes</strong></a><br/></td>
<td>Die <strong>CM_Enumerate_Classes-Funktion,</strong> wenn sie wiederholt aufgerufen wird, aufzählt die <a href="/windows-hardware/drivers/"></a> installierten Geräteklassen des lokalen Computers, indem die GUID der einzelnen Klassen übergeben wird.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_enumerate_classes_ex"><strong>CM_Enumerate_Classes_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Ab Windows 8 und Windows Server 2012 ist diese Funktion veraltet. Verwenden Sie <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_enumerate_classes"><strong>CM_Enumerate_Classes.</strong></a>
</blockquote>
<br/> Die <strong></strong> CM_Enumerate_Classes_Ex-Funktion, wenn sie wiederholt aufgerufen wird, aufzählt eine lokale oder die auf einem Remotecomputer installierten Geräteklassen, <a href="/windows-hardware/drivers/"></a>indem sie die GUID jeder Klasse anhing.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_enumerate_enumeratorsw"><strong>CM_Enumerate_Enumerators</strong></a><br/></td>
<td>Die <strong>CM_Enumerate_Enumerators-Funktion</strong> enumeriert die Geräteenumeratoren des lokalen Computers, indem der Name jedes Enumerators übergeben wird.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_enumerate_enumerators_exw"><strong>CM_Enumerate_Enumerators_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Ab Windows 8 und Windows Server 2012 ist diese Funktion veraltet. Verwenden Sie <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_enumerate_enumeratorsw"><strong>stattdessen CM_Enumerate_Enumerators.</strong></a>
</blockquote>
<br/> Die <strong>CM_Enumerate_Enumerators_Ex-Funktion</strong> aufzählt eine lokale oder die Geräteenumeratoren eines Remotecomputers, indem der Name jedes Enumerators übergeben wird.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_free_log_conf"><strong>CM_Free_Log_Conf</strong></a><br/></td>
<td>Die <strong>CM_Free_Log_Conf-Funktion</strong> entfernt eine <a href="/windows-hardware/drivers/kernel/hardware-resources">logische Konfiguration und</a> alle zugeordneten <a href="/windows-hardware/drivers/">Ressourcendeskriptoren</a> vom lokalen Computer.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_free_log_conf_ex"><strong>CM_Free_Log_Conf_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Ab Windows 8 und Windows Server 2012 ist diese Funktion veraltet. Verwenden Sie <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_free_log_conf"><strong>CM_Free_Log_Conf.</strong></a>
</blockquote>
<br/> Die <strong>CM_Free_Log_Conf_Ex-Funktion</strong> entfernt eine <a href="/windows-hardware/drivers/kernel/hardware-resources"></a> logische Konfiguration und alle zugeordneten <a href="/windows-hardware/drivers/">Ressourcendeskriptoren</a> von einem lokalen computer oder einem Remotecomputer.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_free_log_conf_handle"><strong>CM_Free_Log_Conf_Handle</strong></a><br/></td>
<td>Die <strong>CM_Free_Log_Conf_Handle-Funktion</strong> macht ein logisches Konfigurationshand handle ungültig und gibt die zugeordnete Speicherzuweisung frei.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_free_res_des"><strong>CM_Free_Res_Des</strong></a><br/></td>
<td>Die <strong>CM_Free_Res_Des-Funktion</strong> entfernt einen <a href="/windows-hardware/drivers/">Ressourcendeskriptor</a> aus einer <a href="/windows-hardware/drivers/kernel/hardware-resources">logischen Konfiguration auf</a> dem lokalen Computer.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_free_res_des_ex"><strong>CM_Free_Res_Des_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Ab Windows 8 und Windows Server 2012 ist diese Funktion veraltet. Verwenden Sie <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_free_res_des"><strong>CM_Free_Res_Des.</strong></a>
</blockquote>
<br/> Die <strong>CM_Free_Res_Des_Ex-Funktion</strong> entfernt einen Ressourcendeskriptor <a href="/windows-hardware/drivers/kernel/hardware-resources"></a> aus einer logischen Konfiguration auf einem lokalen oder einem Remotecomputer. <a href="/windows-hardware/drivers/"></a><br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_free_res_des_handle"><strong>CM_Free_Res_Des_Handle</strong></a><br/></td>
<td>Die <strong>CM_Free_Res_Des_Handle-Funktion</strong> macht ein Ressourcenbeschreibungshand handle ungültig und gibt die zugeordnete Speicherbelegung frei.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_free_resource_conflict_handle"><strong>CM_Free_Resource_Conflict_Handle</strong></a><br/></td>
<td>Die <strong>CM_Free_Resource_Conflict_Handle-Funktion</strong> macht ein Handle für eine Ressourcenkonfliktliste ungültig und gibt die zugeordnete Speicherzuordnung des Handles frei.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_child"><strong>CM_Get_Child</strong></a><br/></td>
<td>Die <strong>CM_Get_Child-Funktion</strong> wird verwendet, um ein Geräteinstanzhandles auf den ersten untergeordneten Knoten eines angegebenen Geräteknotens (<a href="/windows-hardware/drivers/">devnode</a>) in der Gerätestruktur des lokalen <a href="/windows-hardware/drivers/kernel/device-tree">Computers abzurufen.</a><br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_child_ex"><strong>CM_Get_Child_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Ab Windows 8 und Windows Server 2012 ist diese Funktion veraltet. Verwenden Sie <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_child"><strong>CM_Get_Child.</strong></a>
</blockquote>
<br/> Die <strong>CM_Get_Child_Ex-Funktion</strong> wird verwendet, um ein Geräteinstanzhandles auf den ersten untergeordneten Knoten eines angegebenen Geräteknotens (<a href="/windows-hardware/drivers/">devnode</a>) in einer lokalen oder der Gerätestruktur eines Remotecomputers <a href="/windows-hardware/drivers/kernel/device-tree">abzurufen.</a><br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_class_propertyw"><strong>CM_Get_Class_Property</strong></a><br/></td>
<td>Die <strong>CM_Get_Class_Property-Funktion</strong> ruft eine Geräteeigenschaft ab, die für eine Geräteschnittstellenklasse <a href="/windows-hardware/drivers/install/device-interface-classes">oder</a> eine <a href="/windows-hardware/drivers/install/device-setup-classes">Geräteeinrichtungsklasse festgelegt ist.</a><br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_class_property_exw"><strong>CM_Get_Class_Property_ExW</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Ab Windows 8 und Windows Server 2012 ist diese Funktion veraltet. Verwenden Sie stattdessen <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_class_propertyw"><strong>CM_Get_Class_Property.</strong></a>
</blockquote>
<br/> Die <strong>CM_Get_Class_Property_ExW-Funktion</strong> ruft eine Geräteeigenschaft ab, die für eine <a href="/windows-hardware/drivers/install/device-interface-classes">Geräteschnittstellenklasse</a> oder <a href="/windows-hardware/drivers/install/device-setup-classes">geräteeinrichtungsklasse</a>festgelegt ist.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_class_property_keys"><strong>CM_Get_Class_Property_Keys</strong></a><br/></td>
<td>Die <strong>CM_Get_Class_Property_Keys-Funktion</strong> ruft ein Array der Geräteeigenschaftsschlüssel ab, die die Geräteeigenschaften darstellen, die für eine <a href="/windows-hardware/drivers/install/device-interface-classes">Geräteschnittstellenklasse</a> oder <a href="/windows-hardware/drivers/install/device-setup-classes">Geräteeinrichtungsklasse</a>festgelegt sind.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_class_property_keys_ex"><strong>CM_Get_Class_Property_Keys_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Ab Windows 8 und Windows Server 2012 ist diese Funktion veraltet. Verwenden Sie stattdessen <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_class_property_keys"><strong>CM_Get_Class_Property_Keys.</strong></a>
</blockquote>
<br/> Die <strong>CM_Get_Class_Property_Keys_Ex-Funktion</strong> ruft ein Array der Geräteeigenschaftsschlüssel ab, die die Geräteeigenschaften darstellen, die für eine <a href="/windows-hardware/drivers/install/device-interface-classes">Geräteschnittstellenklasse</a> oder <a href="/windows-hardware/drivers/install/device-setup-classes">geräteeinrichtungsklasse</a>festgelegt sind.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_class_registry_propertyw"><strong>CM_Get_Class_Registry_Property</strong></a><br/></td>
<td>Die <strong>CM_Get_Class_Registry_Property-Funktion</strong> ruft die <a href="/windows-hardware/drivers/install/accessing-device-setup-class-properties">Geräteeinrichtungsklasseneigenschaft</a>ab.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_depth"><strong>CM_Get_Depth</strong></a><br/></td>
<td>Die <strong>CM_Get_Depth</strong> Funktion wird verwendet, um die Tiefe eines angegebenen Geräteknotens (<a href="/windows-hardware/drivers/">devnode</a>) innerhalb der <a href="/windows-hardware/drivers/kernel/device-tree">Gerätestruktur</a>des lokalen Computers abzurufen.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_depth_ex"><strong>CM_Get_Depth_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Ab Windows 8 und Windows Server 2012 ist diese Funktion veraltet. Verwenden Sie stattdessen <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_depth"><strong>CM_Get_Depth.</strong></a>
</blockquote>
<br/> Die <strong>CM_Get_Depth_Ex</strong> Funktion wird verwendet, um die Tiefe eines angegebenen Geräteknotens (<a href="/windows-hardware/drivers/">devnode</a>) innerhalb einer lokalen Gerätestruktur oder der <a href="/windows-hardware/drivers/kernel/device-tree">Gerätestruktur</a>eines Remotecomputers abzurufen.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_idw"><strong>CM_Get_Device_ID</strong></a><br/></td>
<td>Die <strong>CM_Get_Device_ID-Funktion</strong> ruft die <a href="/windows-hardware/drivers/install/device-instance-ids">Geräteinstanz-ID</a> für eine angegebene <a href="/windows-hardware/drivers/">Geräteinstanz</a> auf dem lokalen Computer ab.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_id_exw"><strong>CM_Get_Device_ID_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Ab Windows 8 und Windows Server 2012 ist diese Funktion veraltet. Verwenden Sie stattdessen <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_idw"><strong>CM_Get_Device_ID.</strong></a>
</blockquote>
<br/> Die <strong>CM_Get_Device_ID_Ex-Funktion</strong> ruft die <a href="/windows-hardware/drivers/install/device-instance-ids">Geräteinstanz-ID</a> für eine angegebene <a href="/windows-hardware/drivers/">Geräteinstanz</a> auf einem lokalen oder Remotecomputer ab.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_id_lista"><strong>CM_Get_Device_ID_List</strong></a><br/></td>
<td>Die <strong>CM_Get_Device_ID_List-Funktion</strong> ruft eine Liste der <a href="/windows-hardware/drivers/install/device-instance-ids">Geräteinstanz-IDs</a> für die <a href="/windows-hardware/drivers/">Geräteinstanzen</a>des lokalen Computers ab.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_id_list_exw"><strong>CM_Get_Device_ID_List_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Ab Windows 8 und Windows Server 2012 ist diese Funktion veraltet. Verwenden Sie stattdessen <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_id_lista"><strong>CM_Get_Device_ID_List.</strong></a>
</blockquote>
<br/> Die <strong>CM_Get_Device_ID_List_Ex-Funktion</strong> ruft eine Liste der <a href="/windows-hardware/drivers/install/device-instance-ids">Geräteinstanz-IDs</a> für die <a href="/windows-hardware/drivers/">Geräteinstanzen</a> auf einem lokalen oder Remotecomputer ab.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_id_list_sizea"><strong>CM_Get_Device_ID_List_Size</strong></a><br/></td>
<td>Die <strong>CM_Get_Device_ID_List_Size-Funktion</strong> ruft die Puffergröße ab, die zum Speichern einer Liste von <a href="/windows-hardware/drivers/install/device-instance-ids">Geräteinstanz-IDs</a> für die <a href="/windows-hardware/drivers/">Geräteinstanzen</a>des lokalen Computers erforderlich ist.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_id_list_size_exw"><strong>CM_Get_Device_ID_List_Size_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Ab Windows 8 und Windows Server 2012 ist diese Funktion veraltet. Verwenden Sie stattdessen <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_id_list_sizea"><strong>CM_Get_Device_ID_List_Size.</strong></a>
</blockquote>
<br/> Die <strong>CM_Get_Device_ID_List_Size_Ex</strong> Funktion ruft die Puffergröße ab, die zum Speichern einer Liste von <a href="/windows-hardware/drivers/install/device-instance-ids">Geräteinstanz-IDs</a> für die <a href="/windows-hardware/drivers/">Geräteinstanzen</a>eines lokalen oder Remotecomputers erforderlich ist.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_id_size"><strong>CM_Get_Device_ID_Size</strong></a><br/></td>
<td>Die <strong>CM_Get_Device_ID_Size-Funktion</strong> ruft die Puffergröße ab, die zum Speichern einer <a href="/windows-hardware/drivers/install/device-instance-ids">Geräteinstanz-ID</a> für eine <a href="/windows-hardware/drivers/">Geräteinstanz</a> auf dem lokalen Computer erforderlich ist.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_id_size_ex"><strong>CM_Get_Device_ID_Size_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Ab Windows 8 und Windows Server 2012 ist diese Funktion veraltet. Verwenden Sie stattdessen <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_id_size"><strong>CM_Get_Device_ID_Size.</strong></a>
</blockquote>
<br/> Die <strong>CM_Get_Device_ID_Size_Ex-Funktion</strong> ruft die Puffergröße ab, die zum Speichern einer <a href="/windows-hardware/drivers/install/device-instance-ids">Geräteinstanz-ID</a> für eine <a href="/windows-hardware/drivers/">Geräteinstanz</a> auf einem lokalen oder Remotecomputer erforderlich ist.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_interface_aliasw"><strong>CM_Get_Device_Interface_Alias</strong></a><br/></td>
<td>Die <strong>CM_Get_Device_Interface_Alias</strong> Funktion gibt den Alias der angegebenen Geräteschnittstelleninstanz zurück, wenn der Alias vorhanden ist.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_interface_lista"><strong>CM_Get_Device_Interface_List</strong></a><br/></td>
<td>Die <strong>CM_Get_Device_Interface_List-Funktion</strong> ruft eine Liste von Geräteschnittstelleninstanzen ab, die zu einer angegebenen <a href="/windows-hardware/drivers/install/device-interface-classes">Geräteschnittstellenklasse</a>gehören.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_interface_list_sizea"><strong>CM_Get_Device_Interface_List_Size</strong></a><br/></td>
<td>Die <strong>CM_Get_Device_Interface_List_Size</strong> Funktion ruft die Puffergröße ab, die an die <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_interface_lista"><strong>CM_Get_Device_Interface_List</strong></a> Funktion übergeben werden muss.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_interface_propertyw"><strong>CM_Get_Device_Interface_Property</strong></a><br/></td>
<td>Die <strong>CM_Get_Device_Interface_Property-Funktion</strong> ruft eine Geräteeigenschaft ab, die für eine Geräteschnittstelle festgelegt ist.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_interface_property_exw"><strong>CM_Get_Device_Interface_Property_ExW</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Ab Windows 8 und Windows Server 2012 ist diese Funktion veraltet. Verwenden Sie stattdessen <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_interface_propertyw"><strong>CM_Get_Device_Interface_Property.</strong></a>
</blockquote>
<br/> Die <strong>CM_Get_Device_Interface_Property_ExW-Funktion</strong> ruft eine Geräteeigenschaft ab, die für eine Geräteschnittstelle festgelegt ist.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_interface_property_keysw"><strong>CM_Get_Device_Interface_Property_Keys</strong></a><br/></td>
<td>Die <strong>CM_Get_Device_Interface_Property_Keys-Funktion</strong> ruft ein Array von Geräteeigenschaftsschlüsseln ab, die die Geräteeigenschaften darstellen, die für eine Geräteschnittstelle festgelegt sind.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_interface_property_keys_exw"><strong>CM_Get_Device_Interface_Property_Keys_ExW</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Ab Windows 8 und Windows Server 2012 ist diese Funktion veraltet. Verwenden Sie stattdessen <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_interface_property_keysw"><strong>CM_Get_Device_Interface_Property_Keys.</strong></a>
</blockquote>
<br/> Die <strong>CM_Get_Device_Interface_Property_Keys_ExW-Funktion</strong> ruft ein Array von Geräteeigenschaftsschlüsseln ab, die die Geräteeigenschaften darstellen, die für eine Geräteschnittstelle festgelegt sind.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_devnode_propertyw"><strong>CM_Get_DevNode_Property</strong></a><br/></td>
<td>Die <strong>CM_Get_DevNode_Property-Funktion</strong> ruft eine Geräteinstanzeigenschaft ab.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_devnode_property_exw"><strong>CM_Get_DevNode_Property_ExW</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Ab Windows 8 und Windows Server 2012 ist diese Funktion veraltet. Verwenden Sie stattdessen <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_devnode_propertyw"><strong>CM_Get_DevNode_Property.</strong></a>
</blockquote>
<br/> Die <strong>CM_Get_DevNode_Property_ExW-Funktion</strong> ruft eine Geräteinstanzeigenschaft ab.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_devnode_property_keys"><strong>CM_Get_DevNode_Property_Keys</strong></a><br/></td>
<td>Die <strong>CM_Get_DevNode_Property_Keys-Funktion</strong> ruft ein Array der Geräteeigenschaftsschlüssel ab, die die Geräteeigenschaften darstellen, die für eine Geräteinstanz festgelegt sind.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_devnode_property_keys_ex"><strong>CM_Get_DevNode_Property_Keys_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Ab Windows 8 und Windows Server 2012 ist diese Funktion veraltet. Verwenden Sie stattdessen <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_devnode_property_keys"><strong>CM_Get_DevNode_Property_Keys.</strong></a>
</blockquote>
<br/> Die <strong>CM_Get_DevNode_Property_Keys_Ex-Funktion</strong> ruft ein Array der Geräteeigenschaftsschlüssel ab, die die Geräteeigenschaften darstellen, die für eine Geräteinstanz festgelegt sind.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_devnode_registry_propertyw"><strong>CM_Get_DevNode_Registry_Property</strong></a><br/></td>
<td>Die <strong>CM_Get_DevNode_Registry_Property-Funktion</strong> ruft eine angegebene Geräteeigenschaft aus der Registrierung ab.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_devnode_status"><strong>CM_Get_DevNode_Status</strong></a><br/></td>
<td>Die <strong>CM_Get_DevNode_Status-Funktion</strong> ruft den Status einer Geräteinstanz von ihrem Geräteknoten (<a href="/windows-hardware/drivers/">devnode</a>) in der <a href="/windows-hardware/drivers/kernel/device-tree">Gerätestruktur</a>des lokalen Computers ab.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_devnode_status_ex"><strong>CM_Get_DevNode_Status_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Ab Windows 8 und Windows Server 2012 ist diese Funktion veraltet. Verwenden Sie stattdessen <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_devnode_status"><strong>CM_Get_DevNode_Status.</strong></a>
</blockquote>
<br/> Die <strong>CM_Get_DevNode_Status_Ex-Funktion</strong> ruft den Status einer Geräteinstanz von ihrem Geräteknoten (<a href="/windows-hardware/drivers/">devnode</a>) auf einem lokalen oder in der <a href="/windows-hardware/drivers/kernel/device-tree">Gerätestruktur</a>eines Remotecomputers ab.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_first_log_conf"><strong>CM_Get_First_Log_Conf</strong></a><br/></td>
<td>Die <strong>CM_Get_First_Log_Conf-Funktion</strong> ruft die erste <a href="/windows-hardware/drivers/kernel/hardware-resources">logische Konfiguration</a>eines angegebenen Konfigurationstyps ab, der einer angegebenen <a href="/windows-hardware/drivers/">Geräteinstanz</a> auf dem lokalen Computer zugeordnet ist.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_first_log_conf_ex"><strong>CM_Get_First_Log_Conf_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Ab Windows 8 und Windows Server 2012 ist diese Funktion veraltet. Verwenden Sie stattdessen <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_first_log_conf"><strong>CM_Get_First_Log_Conf.</strong></a>
</blockquote>
<br/> Die <strong>CM_Get_First_Log_Conf_Ex-Funktion</strong> ruft die erste <a href="/windows-hardware/drivers/kernel/hardware-resources">logische Konfiguration</a> ab, die einer angegebenen <a href="/windows-hardware/drivers/">Geräteinstanz</a> auf einem lokalen oder Remotecomputer zugeordnet ist.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_hw_prof_flagsa"><strong>CM_Get_HW_Prof_Flags</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Ab Windows 8 und Windows Server 2012 ist diese Funktion veraltet und sollte nicht mehr verwendet werden.
</blockquote>
<br/> Die <strong>CM_Get_HW_Prof_Flags-Funktion</strong> ruft die <a href="/windows-hardware/drivers/">Hardwareprofil-spezifischen</a>Konfigurationsflags für eine <a href="/windows-hardware/drivers/">Geräteinstanz</a> auf einem lokalen Computer ab.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_hw_prof_flags_exa"><strong>CM_Get_HW_Prof_Flags_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Diese Funktion ist veraltet und sollte nicht verwendet werden.
</blockquote>
<br/> Die <strong>CM_Get_HW_Prof_Flags_Ex-Funktion</strong> ruft die <a href="/windows-hardware/drivers/">Hardwareprofil-spezifischen</a>Konfigurationsflags für eine <a href="/windows-hardware/drivers/">Geräteinstanz</a> auf einem Remotecomputer oder einem lokalen Computer ab.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_log_conf_priority"><strong>CM_Get_Log_Conf_Priority</strong></a><br/></td>
<td>Die <strong>CM_Get_Log_Conf_Priority-Funktion</strong> ruft die Konfigurationspriorität einer angegebenen <a href="/windows-hardware/drivers/kernel/hardware-resources">logischen Konfiguration</a> auf dem lokalen Computer ab.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_log_conf_priority_ex"><strong>CM_Get_Log_Conf_Priority_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Ab Windows 8 und Windows Server 2012 ist diese Funktion veraltet. Verwenden Sie stattdessen <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_log_conf_priority"><strong>CM_Get_Log_Conf_Priority.</strong></a>
</blockquote>
<br/> Die <strong>CM_Get_Log_Conf_Priority_Ex-Funktion</strong> ruft die Konfigurationspriorität einer angegebenen <a href="/windows-hardware/drivers/kernel/hardware-resources">logischen Konfiguration</a> auf einem lokalen oder Remotecomputer ab.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_next_log_conf"><strong>CM_Get_Next_Log_Conf</strong></a><br/></td>
<td>Die <strong>CM_Get_Next_Log_Conf-Funktion</strong> ruft die nächste <a href="/windows-hardware/drivers/kernel/hardware-resources">logische Konfiguration</a> ab, die einer bestimmten <a href="/windows-hardware/drivers/">Geräteinstanz</a> auf dem lokalen Computer zugeordnet ist.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_next_log_conf_ex"><strong>CM_Get_Next_Log_Conf_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Ab Windows 8 und Windows Server 2012 ist diese Funktion veraltet. Verwenden Sie stattdessen <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_next_log_conf"><strong>CM_Get_Next_Log_Conf.</strong></a>
</blockquote>
<br/> Die <strong>CM_Get_Next_Log_Conf_Ex-Funktion</strong> ruft die nächste <a href="/windows-hardware/drivers/kernel/hardware-resources">logische Konfiguration</a> ab, die einer bestimmten <a href="/windows-hardware/drivers/">Geräteinstanz</a> auf einem lokalen oder Remotecomputer zugeordnet ist.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_next_res_des"><strong>CM_Get_Next_Res_Des</strong></a><br/></td>
<td>Die <strong>CM_Get_Next_Res_Des-Funktion</strong> ruft ein Handle für den nächsten <a href="/windows-hardware/drivers/">Ressourcendeskriptor</a>eines angegebenen Ressourcentyps für eine <a href="/windows-hardware/drivers/kernel/hardware-resources">logische Konfiguration</a> auf dem lokalen Computer ab.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_next_res_des_ex"><strong>CM_Get_Next_Res_Des_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Ab Windows 8 und Windows Server 2012 ist diese Funktion veraltet. Verwenden Sie stattdessen <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_next_res_des"><strong>CM_Get_Next_Res_Des.</strong></a>
</blockquote>
<br/> Die <strong>CM_Get_Next_Res_Des_Ex-Funktion</strong> ruft ein Handle für den nächsten <a href="/windows-hardware/drivers/">Ressourcendeskriptor</a>eines angegebenen Ressourcentyps für eine <a href="/windows-hardware/drivers/kernel/hardware-resources">logische Konfiguration</a> auf einem lokalen oder Remotecomputer ab.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_parent"><strong>CM_Get_Parent</strong></a><br/></td>
<td>Die <strong>CM_Get_Parent-Funktion</strong> ruft ein Geräteinstanzhandle für den übergeordneten Knoten eines angegebenen Geräteknotens (<a href="/windows-hardware/drivers/">devnode</a>) in der Gerätestruktur des lokalen Computers ab.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_parent_ex"><strong>CM_Get_Parent_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Ab Windows 8 und Windows Server 2012 ist diese Funktion veraltet. Verwenden Sie stattdessen <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_parent"><strong>CM_Get_Parent.</strong></a>
</blockquote>
<br/> Die <strong>CM_Get_Parent_Ex-Funktion</strong> ruft ein Geräteinstanzhandle für den übergeordneten Knoten eines angegebenen Geräteknotens (<a href="/windows-hardware/drivers/">devnode</a>) in einer lokalen gerätestruktur oder in der <a href="/windows-hardware/drivers/kernel/device-tree">Gerätestruktur</a>eines Remotecomputers ab.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_res_des_data"><strong>CM_Get_Res_Des_Data</strong></a><br/></td>
<td>Die <strong>CM_Get_Res_Des_Data-Funktion</strong> ruft die informationen ab, die in einem <a href="/windows-hardware/drivers/">Ressourcendeskriptor</a> auf dem lokalen Computer gespeichert sind.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_res_des_data_ex"><strong>CM_Get_Res_Des_Data_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Ab Windows 8 und Windows Server 2012 ist diese Funktion veraltet. Verwenden Sie stattdessen <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_res_des_data"><strong>CM_Get_Res_Des_Data.</strong></a>
</blockquote>
<br/> Die <strong>CM_Get_Res_Des_Data_Ex-Funktion</strong> ruft die Informationen ab, die in einem <a href="/windows-hardware/drivers/">Ressourcendeskriptor</a> auf einem lokalen oder Remotecomputer gespeichert sind.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_res_des_data_size"><strong>CM_Get_Res_Des_Data_Size</strong></a><br/></td>
<td>Die <strong>CM_Get_Res_Des_Data_Size-Funktion</strong> ruft die Puffergröße ab, die zum Speichern der Informationen in einem angegebenen <a href="/windows-hardware/drivers/">Ressourcendeskriptor</a> auf dem lokalen Computer erforderlich ist.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_res_des_data_size_ex"><strong>CM_Get_Res_Des_Data_Size_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Ab Windows 8 und Windows Server 2012 ist diese Funktion veraltet. Verwenden Sie stattdessen <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_res_des_data_size"><strong>CM_Get_Res_Des_Data_Size.</strong></a>
</blockquote>
<br/> Die <strong>CM_Get_Res_Des_Data_Size_Ex-Funktion</strong> ruft die Puffergröße ab, die erforderlich ist, um die Informationen in einem angegebenen <a href="/windows-hardware/drivers/">Ressourcendeskriptor</a> auf einem lokalen oder Remotecomputer zu speichern.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_resource_conflict_count"><strong>CM_Get_Resource_Conflict_Count</strong></a><br/></td>
<td>Die <strong>CM_Get_Resource_Conflict_Count-Funktion</strong> ruft die Anzahl der Konflikte ab, die in einer angegebenen Ressourcenkonfliktliste enthalten sind.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_resource_conflict_detailsw"><strong>CM_Get_Resource_Conflict_Details</strong></a><br/></td>
<td>Die <strong>CM_Get_Resource_Conflict_Details-Funktion</strong> ruft die Details zu einem der Ressourcenkonflikte in einer Konfliktliste ab.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_sibling"><strong>CM_Get_Sibling</strong></a><br/></td>
<td>Die <strong>CM_Get_Sibling-Funktion</strong> ruft ein Geräteinstanzhandle für den nächsten nebengeordneten Knoten eines angegebenen Geräteknotens (<a href="/windows-hardware/drivers/">devnode</a>) in der <a href="/windows-hardware/drivers/kernel/device-tree">Gerätestruktur</a>des lokalen Computers ab.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_sibling_ex"><strong>CM_Get_Sibling_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Ab Windows 8 und Windows Server 2012 ist diese Funktion veraltet. Verwenden Sie stattdessen <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_sibling"><strong>CM_Get_Sibling.</strong></a>
</blockquote>
<br/> Die <strong>CM_Get_Sibling_Ex-Funktion</strong> ruft ein Geräteinstanzhandle für den nächsten nebengeordneten Knoten eines angegebenen Geräteknotens in der <a href="/windows-hardware/drivers/kernel/device-tree">Gerätestruktur</a>eines lokalen oder Remotecomputers ab.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_version"><strong>CM_Get_Version</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Ab Windows 8 und Windows Server 2012 ist diese Funktion veraltet und sollte nicht mehr verwendet werden.
</blockquote>
<br/> The <strong>CM_Get_Version</strong> function returns version 4.0 of the Plug and Play (PnP) Configuration Manager <a href="/windows-hardware/drivers/">DLL</a> (<em>Cfgmgr32.dll</em>) for a local machine. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_version_ex"><strong>CM_Get_Version_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Ab Windows 8 und Windows Server 2012 ist diese Funktion veraltet und sollte nicht mehr verwendet werden.
</blockquote>
<br/> The <strong>CM_Get_Version_Ex</strong> function returns version 4.0 of the Plug and Play (PnP) Configuration Manager <a href="/windows-hardware/drivers/">DLL</a> (<em>Cfgmgr32.dll</em>) for a local or a remote machine. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_is_dock_station_present"><strong>CM_Is_Dock_Station_Present</strong></a><br/></td>
<td>Die <strong>CM_Is_Dock_Station_Present-Funktion</strong> identifiziert, ob eine <a href="/windows-hardware/drivers/">Andockstation</a> auf einem lokalen Computer vorhanden ist.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_is_dock_station_present_ex"><strong>CM_Is_Dock_Station_Present_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Ab Windows 8 und Windows Server 2012 ist diese Funktion veraltet. Verwenden Sie stattdessen <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_is_dock_station_present"><strong>CM_Is_Dock_Station_Present.</strong></a>
</blockquote>
<br/> Die <strong>CM_Is_Dock_Station_Present_Ex-Funktion</strong> gibt an, ob eine <a href="/windows-hardware/drivers/">Dockingstation</a> auf einem lokalen computer oder einem Remotecomputer vorhanden ist.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_is_version_available"><strong>CM_Is_Version_Available</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Ab Windows 8 und Windows Server 2012 ist diese Funktion veraltet und sollte nicht mehr verwendet werden.
</blockquote>
<br/> The <strong>CM_Is_Version_Available</strong> function indicates whether a specified version of the Plug and Play (PnP) Configuration Manager <a href="/windows-hardware/drivers/">DLL</a> (<em>Cfgmgr32.dll</em>) is supported by a local machine.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_is_version_available_ex"><strong>CM_Is_Version_Available_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Ab Windows 8 und Windows Server 2012 ist diese Funktion veraltet und sollte nicht mehr verwendet werden.
</blockquote>
<br/> The <strong>CM_Is_Version_Available_Ex</strong> function indicates whether a specified version of the Plug and Play (PNP) Configuration Manager <a href="/windows-hardware/drivers/">DLL</a> (<em>Cfgmgr32.dll</em>) is supported by a local or a remote machine.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_locate_devnodea"><strong>CM_Locate_DevNode</strong></a><br/></td>
<td>Die <strong>CM_Locate_DevNode-Funktion</strong> ruft ein Geräteinstanzhandle für den Geräteknoten ab, der einer angegebenen <a href="/windows-hardware/drivers/install/device-instance-ids">Geräteinstanz-ID</a> auf dem lokalen Computer zugeordnet ist.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_locate_devnode_exw"><strong>CM_Locate_DevNode_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Ab Windows 8 und Windows Server 2012 ist diese Funktion veraltet. Verwenden Sie stattdessen <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_locate_devnodea"><strong>CM_Locate_DevNode.</strong></a>
</blockquote>
<br/> Die <strong>CM_Locate_DevNode_Ex-Funktion</strong> ruft ein Geräteinstanzhandle für den Geräteknoten ab, der einer angegebenen <a href="/windows-hardware/drivers/install/device-instance-ids">Geräteinstanz-ID</a>zugeordnet ist, auf einem lokalen Computer oder einem Remotecomputer.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_mapcrtowin32err"><strong>CM_MapCrToWin32Err</strong></a><br/></td>
<td>Konvertiert einen angegebenen <strong>CONFIGRET-Code</strong> in den entsprechenden Systemfehlercode.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_modify_res_des"><strong>CM_Modify_Res_Des</strong></a><br/></td>
<td>Die <strong>CM_Modify_Res_Des-Funktion</strong> ändert einen angegebenen Ressourcendeskriptor auf dem lokalen Computer.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_modify_res_des_ex"><strong>CM_Modify_Res_Des_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Ab Windows 8 und Windows Server 2012 ist diese Funktion veraltet. Verwenden Sie stattdessen <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_modify_res_des"><strong>CM_Modify_Res_Des.</strong></a>
</blockquote>
<br/> Die <strong>CM_Modify_Res_Des_Ex-Funktion</strong> ändert einen angegebenen Ressourcendeskriptor auf einem lokalen oder Remotecomputer.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/ne-cfgmgr32-cm_notify_action"><strong>CM_NOTIFY_ACTION</strong></a><br/></td>
<td>Diese Enumeration identifiziert Plug & Play Geräteereignistypen.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/ns-cfgmgr32-cm_notify_event_data"><strong>CM_NOTIFY_EVENT_DATA</strong></a><br/></td>
<td>Dies ist eine Datenstruktur für Gerätebenachrichtigungsereignisse.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/ns-cfgmgr32-cm_notify_filter"><strong>CM_NOTIFY_FILTER</strong></a><br/></td>
<td>Struktur des Gerätebenachrichtigungsfilters<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_open_class_keyw"><strong>CM_Open_Class_Key</strong></a><br/></td>
<td>Die <strong>CM_Open_Class_Key-Funktion</strong> öffnet den Registrierungsschlüssel der Geräteeinrichtungsklasse, den Registrierungsschlüssel der Geräteschnittstellenklasse oder einen bestimmten Unterschlüssel einer Klasse.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_open_device_interface_keyw"><strong>CM_Open_Device_Interface_Key</strong></a><br/></td>
<td>Die <strong>CM_Open_Device_Interface_Key-Funktion</strong> öffnet den Registrierungsunterschlüssel, der von Anwendungen und Treibern zum Speichern von Informationen verwendet wird, die für eine Geräteschnittstelle spezifisch sind.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_open_device_interface_keya"><strong>CM_Open_Device_Interface_Key_ExA</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Ab Windows 8 und Windows Server 2012 ist diese Funktion veraltet. Verwenden Sie stattdessen <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_open_device_interface_keyw"><strong>CM_Open_Device_Interface_Key.</strong></a>
</blockquote>
<br/> Die <strong>CM_Open_Device_Interface_Key_ExA-Funktion</strong> öffnet den Registrierungsunterschlüssel, der von Anwendungen und Treibern zum Speichern von Informationen verwendet wird, die spezifisch für eine Geräteschnittstelle sind.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_open_device_interface_key_exw"><strong>CM_Open_Device_Interface_Key_ExW</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Ab Windows 8 und Windows Server 2012 ist diese Funktion veraltet. Verwenden Sie stattdessen <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_open_device_interface_keyw"><strong>CM_Open_Device_Interface_Key.</strong></a>
</blockquote>
<br/> Die <strong>CM_Open_Device_Interface_Key_ExW-Funktion</strong> öffnet den Registrierungsunterschlüssel, der von Anwendungen und Treibern zum Speichern von Informationen verwendet wird, die spezifisch für eine Geräteschnittstelle sind.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_open_devnode_key"><strong>CM_Open_DevNode_Key</strong></a><br/></td>
<td>Die <strong>CM_Open_DevNode_Key-Funktion</strong> öffnet einen Registrierungsschlüssel für gerätespezifische Konfigurationsinformationen.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_query_and_remove_subtreew"><strong>CM_Query_And_Remove_SubTree</strong></a><br/></td>
<td>Die <strong>CM_Query_And_Remove_SubTree-Funktion</strong> überprüft, ob eine Geräteinstanz und ihre untergeordneten Elemente entfernt werden können, und entfernt sie, wenn dies der Fall ist.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_query_and_remove_subtree_exw"><strong>CM_Query_And_Remove_SubTree_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Ab Windows 8 und Windows Server 2012 ist diese Funktion veraltet. Verwenden Sie stattdessen <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_query_and_remove_subtreew"><strong>CM_Query_And_Remove_SubTree.</strong></a>
</blockquote>
<br/> Die <strong>CM_Query_And_Remove_SubTree_Ex-Funktion</strong> überprüft, ob eine Geräteinstanz und ihre untergeordneten Elemente entfernt werden können. Wenn dies der Fall ist, werden sie entfernt.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_query_resource_conflict_list"><strong>CM_Query_Resource_Conflict_List</strong></a><br/></td>
<td>Die <strong>CM_Query_Resource_Conflict_List-Funktion</strong> identifiziert Geräteinstanzen mit Ressourcenanforderungen, die mit der Ressourcenbeschreibung einer angegebenen Geräteinstanz in Konflikt geraten.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_reenumerate_devnode"><strong>CM_Reenumerate_DevNode</strong></a><br/></td>
<td>Die <strong>CM_Reenumerate_DevNode-Funktion</strong> listet die von einem angegebenen Geräteknoten identifizierten Geräte und alle untergeordneten Elemente auf.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_reenumerate_devnode_ex"><strong>CM_Reenumerate_DevNode_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Ab Windows 8 und Windows Server 2012 ist diese Funktion veraltet. Verwenden Sie stattdessen <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_reenumerate_devnode"><strong>CM_Reenumerate_DevNode.</strong></a>
</blockquote>
<br/> Die <strong>CM_Reenumerate_DevNode_Ex-Funktion</strong> listet die Geräte auf, die von einem angegebenen Geräteknoten und allen untergeordneten Knoten identifiziert werden.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_register_notification"><strong>CM_Register_Notification</strong></a><br/></td>
<td>Verwenden Sie <a href="/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa"><strong>RegisterDeviceNotification</strong></a> anstelle <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_register_notification"><strong>von CM_Register_Notification,</strong></a> wenn Ihr Code auf Windows 7 oder frühere Versionen von Windows abzielt. Kernelmodusaufrufer sollten stattdessen <a href="/windows-hardware/drivers/ddi/content/wdm/nf-wdm-ioregisterplugplaynotification"><strong>IoRegisterPlugPlayNotification</strong></a> verwenden.<br/> Die <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_register_notification"><strong>CM_Register_Notification-Funktion</strong></a> registriert eine Anwendungsrückrufroutine, die aufgerufen wird, wenn ein PnP-Ereignis des angegebenen Typs auftritt.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_request_device_ejectw"><strong>CM_Request_Device_Eject</strong></a><br/></td>
<td>Die <strong>CM_Request_Device_Eject-Funktion</strong> bereitet eine lokale Geräteinstanz für die sichere Entfernung vor, wenn das Gerät wechselbar ist. Wenn das Gerät physisch ausgestreckt werden kann, ist dies der Gleiche.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_request_device_eject_exw"><strong>CM_Request_Device_Eject_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Ab Windows 8 und Windows Server 2012 ist diese Funktion veraltet. Verwenden Sie stattdessen <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_request_device_ejectw"><strong>CM_Request_Device_Eject.</strong></a>
</blockquote>
<br/> Die <strong>CM_Request_Device_Eject_Ex-Funktion</strong> bereitet eine lokale instanz oder eine Remotegeräteinstanz für die sichere Entfernung vor, wenn das Gerät entfernt werden kann. Wenn das Gerät physisch ausgestreckt werden kann, ist dies der Gleiche.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_request_eject_pc"><strong>CM_Request_Eject_PC</strong></a><br/></td>
<td>Die <strong>CM_Request_Eject_PC-Funktion</strong> fordert, dass ein portabler PC, der in eine lokale <a href="/windows-hardware/drivers/">Andockstation</a>eingefügt wird, ausgelassen wird.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_request_eject_pc_ex"><strong>CM_Request_Eject_PC_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Ab Windows 8 und Windows Server 2012 ist diese Funktion veraltet. Verwenden Sie stattdessen <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_request_eject_pc"><strong>CM_Request_Eject_PC.</strong></a>
</blockquote>
<br/> Die <strong>CM_Request_Eject_PC_Ex-Funktion</strong> fordert an, dass ein portabler PC, der in eine lokale oder eine <a href="/windows-hardware/drivers/">Remote-Dockingstation</a>eingefügt wird, ausgelassen wird.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_class_propertyw"><strong>CM_Set_Class_Property</strong></a><br/></td>
<td>Die <strong>CM_Set_Class_Property-Funktion</strong> legt eine Klasseneigenschaft für eine Geräteeinrichtungsklasse oder eine Geräteschnittstellenklasse fest.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_class_property_exw"><strong>CM_Set_Class_Property_ExW</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Ab Windows 8 und Windows Server 2012 ist diese Funktion veraltet. Verwenden Sie stattdessen <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_class_propertyw"><strong>CM_Set_Class_Property.</strong></a>
</blockquote>
<br/> Die <strong>CM_Set_Class_Property_ExW-Funktion</strong> legt eine Klasseneigenschaft für eine Geräteeinrichtungsklasse oder eine Geräteschnittstellenklasse fest.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_class_registry_propertyw"><strong>CM_Set_Class_Registry_Property</strong></a><br/></td>
<td>Die <strong>CM_Set_Class_Registry_Property-Funktion</strong> legt eine Eigenschaft einer <a href="/windows-hardware/drivers/install/device-setup-classes">Geräteeinrichtungsklasse</a>fest oder löscht sie.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_device_interface_propertyw"><strong>CM_Set_Device_Interface_Property</strong></a><br/></td>
<td>Die <strong>CM_Set_Device_Interface_Property-Funktion</strong> legt eine Geräteeigenschaft einer Geräteschnittstelle fest.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_device_interface_property_exw"><strong>CM_Set_Device_Interface_Property_ExW</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Ab Windows 8 und Windows Server 2012 ist diese Funktion veraltet. Verwenden Sie stattdessen <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_device_interface_propertyw"><strong>CM_Set_Device_Interface_Property.</strong></a>
</blockquote>
<br/> Die <strong>CM_Set_Device_Interface_Property_ExW-Funktion</strong> legt eine Geräteeigenschaft einer Geräteschnittstelle fest.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_devnode_problem"><strong>CM_Set_DevNode_Problem</strong></a><br/></td>
<td>Die <strong>CM_Set_DevNode_Problem-Funktion</strong> legt einen Problemcode für ein Gerät fest, das auf einem lokalen Computer installiert ist.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_devnode_problem_ex"><strong>CM_Set_DevNode_Problem_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Ab Windows 8 und Windows Server 2012 ist diese Funktion veraltet. Verwenden Sie stattdessen <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_devnode_problem"><strong>CM_Set_DevNode_Problem.</strong></a>
</blockquote>
<br/> Die <strong>CM_Set_DevNode_Problem_Ex-Funktion</strong> legt einen Problemcode für ein Gerät fest, das auf einem lokalen oder Remotecomputer installiert ist.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_devnode_propertyw"><strong>CM_Set_DevNode_Property</strong></a><br/></td>
<td>Die <strong>CM_Set_DevNode_Property-Funktion</strong> legt eine Geräteinstanzeigenschaft fest.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_devnode_property_exw"><strong>CM_Set_DevNode_Property_ExW</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Ab Windows 8 und Windows Server 2012 ist diese Funktion veraltet. Verwenden Sie stattdessen <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_devnode_propertyw"><strong>CM_Set_DevNode_Property.</strong></a>
</blockquote>
<br/> Die <strong>CM_Set_DevNode_Property_ExW-Funktion</strong> legt eine Geräteinstanzeigenschaft fest.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_devnode_registry_propertyw"><strong>CM_Set_DevNode_Registry_Property</strong></a><br/></td>
<td>Die <strong>CM_Set_DevNode_Registry_Property-Funktion</strong> legt eine angegebene Geräteeigenschaft in der Registrierung fest.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_setup_devnode"><strong>CM_Setup_DevNode</strong></a><br/></td>
<td>Die <strong>CM_Setup_DevNode-Funktion</strong> startet eine Geräteinstanz neu, die nicht ausgeführt wird, da ein Problem mit der Gerätekonfiguration vorliegt.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_uninstall_devnode"><strong>CM_Uninstall_DevNode</strong></a><br/></td>
<td>Die <strong>CM_Uninstall_DevNode</strong> Funktion entfernt den gesamten persistenten Zustand, der einer Geräteinstanz zugeordnet ist.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_unregister_notification"><strong>CM_Unregister_Notification</strong></a><br/></td>
<td>Verwenden Sie <a href="/windows/desktop/api/winuser/nf-winuser-unregisterdevicenotification"><strong>UnregisterDeviceNotification</strong></a> anstelle <strong>von CM_Unregister_Notification,</strong> wenn Ihr Code auf Windows 7 oder frühere Versionen von Windows abzielt.<br/> Die <strong>CM_Unregister_Notification</strong> Funktion schließt das angegebene HCMNOTIFICATION-Handle.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_waitnopendinginstallevents"><strong>CMP_WaitNoPendingInstallEvents</strong></a><br/></td>
<td>Die <strong>CMP_WaitNoPendingInstallEvents-Funktion</strong> wartet, bis keine ausstehenden Geräteinstallationsaktivitäten für den PnP-Manager vorhanden sind.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/cfgmgr32/ns-cfgmgr32-conflict_details_a"><strong>CONFLICT_DETAILS</strong></a><br/></td>
<td>Die CONFLICT_DETAILS-Struktur wird als Parameter für die <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_resource_conflict_detailsw"><strong>CM_Get_Resource_Conflict_Details-Funktion</strong></a> verwendet.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-cs_des"><strong>CS_DES</strong></a><br/></td>
<td>Die CS_DES-Struktur wird zum Angeben einer Ressourcenliste verwendet, die die geräteklassenspezifische Ressourcenverwendung für eine Geräteinstanz beschreibt. Weitere Informationen zu Ressourcenlisten finden Sie unter <a href="/windows-hardware/drivers/kernel/hardware-resources">Hardwareressourcen.</a><br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-cs_resource"><strong>CS_RESOURCE</strong></a><br/></td>
<td>Die CS_RESOURCE-Struktur wird zum Angeben einer Ressourcenliste verwendet, die die geräteklassenspezifische Ressourcenverwendung für eine Geräteinstanz beschreibt. Weitere Informationen zu Ressourcenlisten finden Sie unter <a href="/windows-hardware/drivers/kernel/hardware-resources">Hardwareressourcen.</a><br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-dma_des"><strong>DMA_DES</strong></a><br/></td>
<td>Die DMA_DES-Struktur wird verwendet, um entweder eine Ressourcenliste oder eine Ressourcenanforderungsliste anzugeben, die die Kanalnutzung des direkten Speicherzugriffs (Direct Memory Access, DMA) für eine Geräteinstanz beschreibt. Weitere Informationen zu Ressourcenlisten und Ressourcenanforderungen finden Sie unter <a href="/windows-hardware/drivers/kernel/hardware-resources">Hardwareressourcen.</a><br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-dma_range"><strong>DMA_RANGE</strong></a><br/></td>
<td>Die DMA_RANGE-Struktur gibt eine Ressourcenanforderungsliste an, in der die DMA-Kanalverwendung für eine Geräteinstanz beschrieben wird. Weitere Informationen zu Ressourcenanforderungen finden Sie unter <a href="/windows-hardware/drivers/kernel/hardware-resources">Hardwareressourcen.</a><br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-dma_resource"><strong>DMA_RESOURCE</strong></a><br/></td>
<td>Die DMA_RESOURCE-Struktur wird verwendet, um entweder eine Ressourcenliste oder eine Ressourcenanforderungsliste anzugeben, die die DMA-Kanalnutzung für eine Geräteinstanz beschreibt. Weitere Informationen zu Ressourcenlisten und Ressourcenanforderungen finden Sie unter <a href="/windows-hardware/drivers/kernel/hardware-resources">Hardwareressourcen.</a><br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-io_des"><strong>IO_DES</strong></a><br/></td>
<td>Die IO_DES-Struktur wird verwendet, um entweder eine Ressourcenliste oder eine Ressourcenanforderungsliste anzugeben, die die E/A-Portnutzung für eine Geräteinstanz beschreibt. Weitere Informationen zu Ressourcenlisten und Ressourcenanforderungen finden Sie unter <a href="/windows-hardware/drivers/kernel/hardware-resources">Hardwareressourcen.</a><br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-io_range"><strong>IO_RANGE</strong></a><br/></td>
<td>Die IO_RANGE-Struktur gibt eine Ressourcenanforderungsliste an, in der die E/A-Portnutzung für eine Geräteinstanz beschrieben wird. Weitere Informationen zu Ressourcenanforderungen finden Sie unter <a href="/windows-hardware/drivers/kernel/hardware-resources">Hardwareressourcen.</a><br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-io_resource"><strong>IO_RESOURCE</strong></a><br/></td>
<td>Die IO_RESOURCE Struktur wird verwendet, um entweder eine Ressourcenliste oder eine Ressourcenanforderungsliste anzugeben, die die E/A-Portnutzung für eine Geräteinstanz beschreibt. Weitere Informationen zu Ressourcenlisten und Ressourcenanforderungen finden Sie unter <a href="/windows-hardware/drivers/kernel/hardware-resources">Hardwareressourcen.</a><br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-irq_des_64"><strong>IRQ_DES</strong></a><br/></td>
<td>Die IRQ_DES-Struktur wird verwendet, um entweder eine Ressourcenliste oder eine Ressourcenanforderungsliste anzugeben, die die IRQ-Zeilennutzung für eine Geräteinstanz beschreibt. Weitere Informationen zu Ressourcenlisten und Ressourcenanforderungen finden Sie unter <a href="/windows-hardware/drivers/kernel/hardware-resources">Hardwareressourcen.</a><br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-irq_range"><strong>IRQ_RANGE</strong></a><br/></td>
<td>Die IRQ_RANGE-Struktur gibt eine Ressourcenanforderungsliste an, in der die IRQ-Zeilenverwendung für eine Geräteinstanz beschrieben wird. Weitere Informationen zu Ressourcenanforderungen finden Sie unter <a href="/windows-hardware/drivers/kernel/hardware-resources">Hardwareressourcen.</a><br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-irq_resource_64"><strong>IRQ_RESOURCE</strong></a><br/></td>
<td>Die IRQ_RESOURCE-Struktur wird verwendet, um entweder eine Ressourcenliste oder eine Ressourcenanforderungsliste anzugeben, die die IRQ-Zeilenverwendung für eine Geräteinstanz beschreibt. Weitere Informationen zu Ressourcenlisten und Ressourcenanforderungen finden Sie unter <a href="/windows-hardware/drivers/kernel/hardware-resources">Hardwareressourcen.</a><br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-mem_des"><strong>MEM_DES</strong></a><br/></td>
<td>Die MEM_DES-Struktur wird verwendet, um entweder eine Ressourcenliste oder eine Ressourcenanforderungsliste anzugeben, die die Speicherauslastung für eine Geräteinstanz beschreibt. Weitere Informationen zu Ressourcenlisten und Ressourcenanforderungen finden Sie unter <a href="/windows-hardware/drivers/kernel/hardware-resources">Hardwareressourcen.</a><br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-mem_range"><strong>MEM_RANGE</strong></a><br/></td>
<td>Die MEM_RANGE-Struktur gibt eine Ressourcenanforderungsliste an, in der die Speicherauslastung für eine Geräteinstanz beschrieben wird. Weitere Informationen zu Ressourcenanforderungen finden Sie unter <a href="/windows-hardware/drivers/kernel/hardware-resources">Hardwareressourcen.</a><br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-mem_resource"><strong>MEM_RESOURCE</strong></a><br/></td>
<td>Die MEM_RESOURCE-Struktur wird verwendet, um entweder eine Ressourcenliste oder eine Ressourcenanforderungsliste anzugeben, die die Speicherauslastung für eine Geräteinstanz beschreibt. Weitere Informationen zu Ressourcenlisten und Ressourcenanforderungen finden Sie unter <a href="/windows-hardware/drivers/kernel/hardware-resources">Hardwareressourcen.</a><br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-mfcard_des"><strong>MFCARD_DES</strong></a><br/></td>
<td>Die MFCARD_DES-Struktur wird verwendet, um entweder eine Ressourcenliste oder eine Ressourcenanforderungsliste anzugeben, die die Ressourcennutzung durch <em>eine</em> der Hardwarefunktionen beschreibt, die von einer Instanz eines Multifunktionsgeräts bereitgestellt werden. Weitere Informationen zu Ressourcenlisten und Ressourcenanforderungen finden Sie unter <a href="/windows-hardware/drivers/kernel/hardware-resources">Hardwareressourcen.</a><br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-mfcard_resource"><strong>MFCARD_RESOURCE</strong></a><br/></td>
<td>Die MFCARD_RESOURCE Struktur wird verwendet, um entweder eine Ressourcenliste oder eine Ressourcenanforderungsliste anzugeben, die die Ressourcennutzung durch <em>eine</em> der Hardwarefunktionen beschreibt, die von einer Instanz eines Multifunktionsgeräts bereitgestellt werden. Weitere Informationen zu Ressourcenlisten und Ressourcenanforderungen finden Sie unter <a href="/windows-hardware/drivers/kernel/hardware-resources">Hardwareressourcen.</a><br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-pccard_des"><strong>PCCARD_DES</strong></a><br/></td>
<td>Die PCCARD_DES-Struktur wird verwendet, um entweder eine Ressourcenliste oder eine Ressourcenanforderungsliste anzugeben, die die Ressourcennutzung durch eine PC-Karteninstanz beschreibt. Weitere Informationen zu Ressourcenlisten und Ressourcenanforderungen finden Sie unter <a href="/windows-hardware/drivers/kernel/hardware-resources">Hardwareressourcen.</a><br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-pccard_resource"><strong>PCCARD_RESOURCE</strong></a><br/></td>
<td>Die PCCARD_RESOURCE Struktur wird verwendet, um entweder eine Ressourcenliste oder eine Ressourcenanforderungsliste anzugeben, die die Ressourcennutzung durch eine PC-Karteninstanz beschreibt. Weitere Informationen zu Ressourcenlisten und Ressourcenanforderungen finden Sie unter <a href="/windows-hardware/drivers/kernel/hardware-resources">Hardwareressourcen.</a><br/></td>
</tr>
</tbody>
</table>



 

 

 

[Senden von Kommentaren zu diesem Thema an Microsoft](mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback%20%5Bdevinst\devinst%5D:%20Cfgmgr32.h%20%20RELEASE:%20%283/29/2018%29&body=%0A%0APRIVACY%20STATEMENT%0A%0AWe%20use%20your%20feedback%20to%20improve%20the%20documentation.%20We%20don't%20use%20your%20email%20address%20for%20any%20other%20purpose,%20and%20we'll%20remove%20your%20email%20address%20from%20our%20system%20after%20the%20issue%20that%20you're%20reporting%20is%20fixed.%20While%20we're%20working%20to%20fix%20this%20issue,%20we%20might%20send%20you%20an%20email%20message%20to%20ask%20for%20more%20info.%20Later,%20we%20might%20also%20send%20you%20an%20email%20message%20to%20let%20you%20know%20that%20we've%20addressed%20your%20feedback.%0A%0AFor%20more%20info%20about%20Microsoft's%20privacy%20policy,%20see%20http://privacy.microsoft.com/default.aspx. "Senden von Kommentaren zu diesem Thema an Microsoft")