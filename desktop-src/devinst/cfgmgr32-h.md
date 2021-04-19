---
title: 'Cfgmgr32.h '
description: Dieser Abschnitt enthält Referenz Themen für den Header Cfgmgr32. h.
ms.assetid: 73b4b2ec-ce3d-47c1-9b0e-1052f390ae94
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08ccc2baf458fea5e20842c9bfa60028c2cb8e23
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/08/2020
ms.locfileid: "106339301"
---
# <a name="cfgmgr32h"></a>Cfgmgr32.h 

Dieser Abschnitt enthält Referenz Themen für den Header Cfgmgr32. h.

## <a name="in-this-section"></a>In diesem Abschnitt



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Thema</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-busnumber_des"><strong>BUSNUMBER_DES</strong></a><br/></td>
<td>Die BUSNUMBER_DES Struktur wird verwendet, um entweder eine Ressourcen Liste oder eine Ressourcen Anforderungsliste anzugeben, in der die Busnummern Verwendung für eine Geräte Instanz beschrieben wird. Weitere Informationen zu Ressourcen Listen und Ressourcen Anforderungslisten finden Sie unter <a href="/windows-hardware/drivers/kernel/hardware-resources">Hardware Ressourcen</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-busnumber_range"><strong>BUSNUMBER_RANGE</strong></a><br/></td>
<td>Die BUSNUMBER_RANGE Struktur gibt eine Ressourcen Anforderungsliste an, in der die busnummerverwendung für eine Geräte Instanz beschrieben wird. Weitere Informationen zu Ressourcen Anforderungslisten finden Sie unter <a href="/windows-hardware/drivers/kernel/hardware-resources">Hardware Ressourcen</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-busnumber_resource"><strong>BUSNUMBER_RESOURCE</strong></a><br/></td>
<td>Die BUSNUMBER_RESOURCE Struktur gibt entweder eine Ressourcen Liste oder eine Ressourcen Anforderungsliste an, in der die busnummerverwendung für eine Geräte Instanz beschrieben wird. Weitere Informationen zu Ressourcen Listen und Ressourcen Anforderungslisten finden Sie unter <a href="/windows-hardware/drivers/kernel/hardware-resources">Hardware Ressourcen</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_add_empty_log_conf"><strong>CM_Add_Empty_Log_Conf</strong></a><br/></td>
<td>Die <strong>CM_Add_Empty_Log_Conf</strong> -Funktion erstellt eine leere <a href="/windows-hardware/drivers/kernel/hardware-resources">logische Konfiguration</a>für einen angegebenen Konfigurationstyp und eine angegebene Geräte Instanz auf dem lokalen Computer.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_add_empty_log_conf_ex"><strong>CM_Add_Empty_Log_Conf_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Ab Windows 8 und Windows Server 2012 wurde diese Funktion als veraltet markiert. Verwenden Sie stattdessen <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_add_empty_log_conf"><strong>CM_Add_Empty_Log_Conf</strong></a> .
</blockquote>
<br/> Die <strong>CM_Add_Empty_Log_Conf_Ex</strong> -Funktion erstellt eine leere <a href="/windows-hardware/drivers/kernel/hardware-resources">logische Konfiguration</a>für einen angegebenen Konfigurationstyp und eine angegebene Geräte Instanz auf dem lokalen oder einem Remote Computer.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_add_idw"><strong>CM_Add_ID</strong></a><br/></td>
<td>Die <strong>CM_Add_ID</strong> -Funktion fügt eine angegebene <a href="/windows-hardware/drivers/install/device-ids">Geräte-ID</a> (sofern nicht bereits vorhanden) an <a href="/windows-hardware/drivers/">die Hardware-ID-Liste der Geräte Instanz</a> <a href="/windows-hardware/drivers/install/hardware-ids"></a> oder die <a href="/windows-hardware/drivers/install/compatible-ids">kompatible ID</a> -Liste an.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_add_id_exw"><strong>CM_Add_ID_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Ab Windows 8 und Windows Server 2012 wurde diese Funktion als veraltet markiert. Verwenden Sie stattdessen <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_add_idw"><strong>CM_Add_ID</strong></a> .
</blockquote>
<br/> Die <strong>CM_Add_ID_Ex</strong> -Funktion fügt eine <a href="/windows-hardware/drivers/install/device-ids">Geräte-ID</a> (sofern nicht bereits vorhanden) an die Hardware- <a href="/windows-hardware/drivers/install/hardware-ids">ID</a> -Liste oder die <a href="/windows-hardware/drivers/install/compatible-ids">kompatible ID</a> -Liste einer Geräte Instanz auf dem lokalen oder einem Remote Computer an.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_add_res_des"><strong>CM_Add_Res_Des</strong></a><br/></td>
<td>Die <strong>CM_Add_Res_Des</strong> -Funktion fügt einer <a href="/windows-hardware/drivers/kernel/hardware-resources">logischen Konfiguration</a>einen <a href="/windows-hardware/drivers/">Ressourcen Deskriptor</a> hinzu.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_add_res_des_ex"><strong>CM_Add_Res_Des_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Ab Windows 8 und Windows Server 2012 wurde diese Funktion als veraltet markiert. Verwenden Sie stattdessen <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_add_res_des"><strong>CM_Add_Res_Des</strong></a> .
</blockquote>
<br/> Die <strong>CM_Add_Res_Des_Ex</strong> -Funktion fügt einer <a href="/windows-hardware/drivers/kernel/hardware-resources">logischen Konfiguration</a>einen <a href="/windows-hardware/drivers/">Ressourcen Deskriptor</a> hinzu. Die logische Konfiguration kann sich entweder auf dem lokalen Computer oder auf einem Remote Computer befinden.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_connect_machinew"><strong>CM_Connect_Machine</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Ab Windows 8-und Windows Server 2012-Funktionen für den Zugriff auf Remote Computer wurde entfernt. Sie können nicht auf Remote Computer zugreifen, wenn Sie unter diesen Versionen von Windows ausführen.
</blockquote>
<br/> Die <strong>CM_Connect_Machine</strong> -Funktion erstellt eine Verbindung mit einem Remote Computer.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_delete_class_key"><strong>CM_Delete_Class_Key</strong></a><br/></td>
<td>Die <strong>CM_Delete_Class_Key</strong> -Funktion entfernt die angegebene installierte <a href="/windows-hardware/drivers/">Geräteklasse</a> aus dem System.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_delete_device_interface_keyw"><strong>CM_Delete_Device_Interface_Key</strong></a><br/></td>
<td>Die <strong>CM_Delete_Device_Interface_Key</strong> -Funktion löscht den Registrierungs Unterschlüssel, der von Anwendungen und Treibern zum Speichern Schnittstellen spezifischer Informationen verwendet wird.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_delete_device_interface_key_exa"><strong>CM_Delete_Device_Interface_Key_ExA</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Ab Windows 8 und Windows Server 2012 wurde diese Funktion als veraltet markiert. Verwenden Sie stattdessen <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_delete_device_interface_keyw"><strong>CM_Delete_Device_Interface_Key</strong></a> .
</blockquote>
<br/> Die <strong>CM_Delete_Device_Interface_Key_ExA</strong> -Funktion löscht den Registrierungs Unterschlüssel, der von Anwendungen und Treibern zum Speichern Schnittstellen spezifischer Informationen verwendet wird.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_delete_device_interface_key_exw"><strong>CM_Delete_Device_Interface_Key_ExW</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Ab Windows 8 und Windows Server 2012 wurde diese Funktion als veraltet markiert. Verwenden Sie stattdessen <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_delete_device_interface_keyw"><strong>CM_Delete_Device_Interface_Key</strong></a> .
</blockquote>
<br/> Die <strong>CM_Delete_Device_Interface_Key_ExW</strong> -Funktion löscht den Registrierungs Unterschlüssel, der von Anwendungen und Treibern zum Speichern Schnittstellen spezifischer Informationen verwendet wird.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_delete_devnode_key"><strong>CM_Delete_DevNode_Key</strong></a><br/></td>
<td>Die <strong>CM_Delete_DevNode_Key</strong> -Funktion löscht die angegebenen, vom Benutzer zugänglichen Registrierungsschlüssel, die einem Gerät zugeordnet sind.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_disable_devnode"><strong>CM_Disable_DevNode</strong></a><br/></td>
<td>Die <strong>CM_Disable_DevNode</strong> -Funktion deaktiviert ein Gerät.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_disconnect_machine"><strong>CM_Disconnect_Machine</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Ab Windows 8-und Windows Server 2012-Funktionen für den Zugriff auf Remote Computer wurde entfernt. Sie können nicht auf Remote Computer zugreifen, wenn Sie unter diesen Versionen von Windows ausführen.
</blockquote>
<br/> Die <strong>CM_Disconnect_Machine</strong> -Funktion entfernt eine Verbindung mit einem Remote Computer.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_enable_devnode"><strong>CM_Enable_DevNode</strong></a><br/></td>
<td>Die <strong>CM_Enable_DevNode</strong> -Funktion aktiviert ein Gerät.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_enumerate_classes"><strong>CM_Enumerate_Classes</strong></a><br/></td>
<td>Wenn die <strong>CM_Enumerate_Classes</strong> -Funktion wiederholt aufgerufen wird, listet Sie die installierten <a href="/windows-hardware/drivers/">Geräteklassen</a> des lokalen Computers auf, indem Sie die GUID der einzelnen Klassen bereitstellt.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_enumerate_classes_ex"><strong>CM_Enumerate_Classes_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Ab Windows 8 und Windows Server 2012 wurde diese Funktion als veraltet markiert. Verwenden Sie stattdessen <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_enumerate_classes"><strong>CM_Enumerate_Classes</strong></a> .
</blockquote>
<br/> Die <strong>CM_Enumerate_Classes_Ex</strong> Funktion zählt, wenn Sie wiederholt aufgerufen wird, eine lokale oder eine auf dem Remote Computer installierte <a href="/windows-hardware/drivers/">Geräteklasse</a>auf, indem Sie die GUID der einzelnen Klassen bereitstellt.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_enumerate_enumeratorsw"><strong>CM_Enumerate_Enumerators</strong></a><br/></td>
<td>Die <strong>CM_Enumerate_Enumerators</strong> -Funktion Listet die Geräte Enumeratoren des lokalen Computers durch Angabe des Namens jedes Enumeratoren auf.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_enumerate_enumerators_exw"><strong>CM_Enumerate_Enumerators_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Ab Windows 8 und Windows Server 2012 wurde diese Funktion als veraltet markiert. Verwenden Sie stattdessen <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_enumerate_enumeratorsw"><strong>CM_Enumerate_Enumerators</strong></a> .
</blockquote>
<br/> Die <strong>CM_Enumerate_Enumerators_Ex</strong> -Funktion Listet die Geräte Enumeratoren eines lokalen Computers oder eines Remote Computers auf, indem jeder Enumeratorname bereitgestellt wird.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_free_log_conf"><strong>CM_Free_Log_Conf</strong></a><br/></td>
<td>Die <strong>CM_Free_Log_Conf</strong> -Funktion entfernt eine <a href="/windows-hardware/drivers/kernel/hardware-resources">logische Konfiguration</a> und alle zugehörigen <a href="/windows-hardware/drivers/">Ressourcen Deskriptoren</a> aus dem lokalen Computer.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_free_log_conf_ex"><strong>CM_Free_Log_Conf_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Ab Windows 8 und Windows Server 2012 wurde diese Funktion als veraltet markiert. Verwenden Sie stattdessen <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_free_log_conf"><strong>CM_Free_Log_Conf</strong></a> .
</blockquote>
<br/> Die <strong>CM_Free_Log_Conf_Ex</strong> -Funktion entfernt eine <a href="/windows-hardware/drivers/kernel/hardware-resources">logische Konfiguration</a> und alle zugeordneten <a href="/windows-hardware/drivers/">Ressourcen Deskriptoren</a> entweder von einem lokalen oder einem Remote Computer.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_free_log_conf_handle"><strong>CM_Free_Log_Conf_Handle</strong></a><br/></td>
<td>Die <strong>CM_Free_Log_Conf_Handle</strong> -Funktion macht ein logisches Konfigurations Handle ungültig und gibt die zugeordnete Speicher Belegung frei.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_free_res_des"><strong>CM_Free_Res_Des</strong></a><br/></td>
<td>Die <strong>CM_Free_Res_Des</strong> -Funktion entfernt einen <a href="/windows-hardware/drivers/">Ressourcen Deskriptor</a> aus einer <a href="/windows-hardware/drivers/kernel/hardware-resources">logischen Konfiguration</a> auf dem lokalen Computer.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_free_res_des_ex"><strong>CM_Free_Res_Des_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Ab Windows 8 und Windows Server 2012 wurde diese Funktion als veraltet markiert. Verwenden Sie stattdessen <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_free_res_des"><strong>CM_Free_Res_Des</strong></a> .
</blockquote>
<br/> Die <strong>CM_Free_Res_Des_Ex</strong> -Funktion entfernt einen <a href="/windows-hardware/drivers/">Ressourcen Deskriptor</a> aus einer <a href="/windows-hardware/drivers/kernel/hardware-resources">logischen Konfiguration</a> auf einem lokalen oder einem Remote Computer.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_free_res_des_handle"><strong>CM_Free_Res_Des_Handle</strong></a><br/></td>
<td>Die <strong>CM_Free_Res_Des_Handle</strong> -Funktion macht ein Ressourcen Beschreibungs Handle ungültig und gibt die zugeordnete Speicher Belegung frei.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_free_resource_conflict_handle"><strong>CM_Free_Resource_Conflict_Handle</strong></a><br/></td>
<td>Die <strong>CM_Free_Resource_Conflict_Handle</strong> -Funktion macht ein Handle für eine Ressourcen Konflikt Liste ungültig und gibt die zugeordnete Speicher Belegung des Handles frei.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_child"><strong>CM_Get_Child</strong></a><br/></td>
<td>Die <strong>CM_Get_Child</strong> -Funktion wird verwendet, um ein geräteinstanzhandle für den ersten untergeordneten Knoten eines angegebenen Geräte Knotens (<a href="/windows-hardware/drivers/">devnode</a>) in der <a href="/windows-hardware/drivers/kernel/device-tree">Geräte</a>Struktur des lokalen Computers abzurufen.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_child_ex"><strong>CM_Get_Child_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Ab Windows 8 und Windows Server 2012 wurde diese Funktion als veraltet markiert. Verwenden Sie stattdessen <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_child"><strong>CM_Get_Child</strong></a> .
</blockquote>
<br/> Die <strong>CM_Get_Child_Ex</strong> -Funktion wird verwendet, um ein geräteinstanzhandle für den ersten untergeordneten Knoten eines angegebenen Geräte Knotens (<a href="/windows-hardware/drivers/">devnode</a>) in einer lokalen oder einer <a href="/windows-hardware/drivers/kernel/device-tree">Geräte</a>Struktur eines Remote Computers abzurufen.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_class_propertyw"><strong>CM_Get_Class_Property</strong></a><br/></td>
<td>Die <strong>CM_Get_Class_Property</strong> -Funktion Ruft eine Geräte Eigenschaft ab, die für eine <a href="/windows-hardware/drivers/install/device-interface-classes">Geräteschnittstellen Klasse</a> oder <a href="/windows-hardware/drivers/install/device-setup-classes">Geräte Setup Klasse</a>festgelegt ist.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_class_property_exw"><strong>CM_Get_Class_Property_ExW</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Ab Windows 8 und Windows Server 2012 wurde diese Funktion als veraltet markiert. Verwenden Sie stattdessen <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_class_propertyw"><strong>CM_Get_Class_Property</strong></a> .
</blockquote>
<br/> Die <strong>CM_Get_Class_Property_ExW</strong> -Funktion Ruft eine Geräte Eigenschaft ab, die für eine <a href="/windows-hardware/drivers/install/device-interface-classes">Geräteschnittstellen Klasse</a> oder <a href="/windows-hardware/drivers/install/device-setup-classes">Geräte Setup Klasse</a>festgelegt ist.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_class_property_keys"><strong>CM_Get_Class_Property_Keys</strong></a><br/></td>
<td>Die <strong>CM_Get_Class_Property_Keys</strong> -Funktion Ruft ein Array der Geräte Eigenschafts Schlüssel ab, die die Geräteeigenschaften darstellen, die für eine <a href="/windows-hardware/drivers/install/device-interface-classes">Geräteschnittstellen Klasse</a> oder <a href="/windows-hardware/drivers/install/device-setup-classes">Geräte Setup Klasse</a>festgelegt sind.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_class_property_keys_ex"><strong>CM_Get_Class_Property_Keys_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Ab Windows 8 und Windows Server 2012 wurde diese Funktion als veraltet markiert. Verwenden Sie stattdessen <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_class_property_keys"><strong>CM_Get_Class_Property_Keys</strong></a> .
</blockquote>
<br/> Die <strong>CM_Get_Class_Property_Keys_Ex</strong> -Funktion Ruft ein Array der Geräte Eigenschafts Schlüssel ab, die die Geräteeigenschaften darstellen, die für eine <a href="/windows-hardware/drivers/install/device-interface-classes">Geräteschnittstellen Klasse</a> oder <a href="/windows-hardware/drivers/install/device-setup-classes">Geräte Setup Klasse</a>festgelegt sind.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_class_registry_propertyw"><strong>CM_Get_Class_Registry_Property</strong></a><br/></td>
<td>Die <strong>CM_Get_Class_Registry_Property</strong> Funktion Ruft eine <a href="/windows-hardware/drivers/install/accessing-device-setup-class-properties">Eigenschaft der Geräte Setup Klasse</a>ab.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_depth"><strong>CM_Get_Depth</strong></a><br/></td>
<td>Die <strong>CM_Get_Depth</strong> -Funktion wird verwendet, um die Tiefe eines angegebenen Geräte Knotens (<a href="/windows-hardware/drivers/">devnode</a>) innerhalb der <a href="/windows-hardware/drivers/kernel/device-tree">Geräte</a>Struktur des lokalen Computers abzurufen.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_depth_ex"><strong>CM_Get_Depth_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Ab Windows 8 und Windows Server 2012 wurde diese Funktion als veraltet markiert. Verwenden Sie stattdessen <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_depth"><strong>CM_Get_Depth</strong></a> .
</blockquote>
<br/> Die <strong>CM_Get_Depth_Ex</strong> -Funktion wird verwendet, um die Tiefe eines angegebenen Geräte Knotens (<a href="/windows-hardware/drivers/">devnode</a>) innerhalb einer lokalen oder der <a href="/windows-hardware/drivers/kernel/device-tree">Geräte</a>Struktur eines Remote Computers abzurufen.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_idw"><strong>CM_Get_Device_ID</strong></a><br/></td>
<td>Die <strong>CM_Get_Device_ID</strong> -Funktion Ruft die <a href="/windows-hardware/drivers/install/device-instance-ids">Geräte Instanz-ID</a> für eine angegebene <a href="/windows-hardware/drivers/">Geräte Instanz</a> auf dem lokalen Computer ab.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_id_exw"><strong>CM_Get_Device_ID_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Ab Windows 8 und Windows Server 2012 wurde diese Funktion als veraltet markiert. Verwenden Sie stattdessen <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_idw"><strong>CM_Get_Device_ID</strong></a> .
</blockquote>
<br/> Die <strong>CM_Get_Device_ID_Ex</strong> -Funktion Ruft die <a href="/windows-hardware/drivers/install/device-instance-ids">Geräte Instanz-ID</a> für eine angegebene <a href="/windows-hardware/drivers/">Geräte Instanz</a> auf einem lokalen oder einem Remote Computer ab.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_id_lista"><strong>CM_Get_Device_ID_List</strong></a><br/></td>
<td>Die <strong>CM_Get_Device_ID_List</strong> -Funktion Ruft eine Liste von <a href="/windows-hardware/drivers/install/device-instance-ids">Geräte Instanz-IDs</a> für die <a href="/windows-hardware/drivers/">Geräte Instanzen</a>des lokalen Computers ab.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_id_list_exw"><strong>CM_Get_Device_ID_List_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Ab Windows 8 und Windows Server 2012 wurde diese Funktion als veraltet markiert. Verwenden Sie stattdessen <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_id_lista"><strong>CM_Get_Device_ID_List</strong></a> .
</blockquote>
<br/> Die <strong>CM_Get_Device_ID_List_Ex</strong> -Funktion Ruft eine Liste von <a href="/windows-hardware/drivers/install/device-instance-ids">Geräte Instanz-IDs</a> für die <a href="/windows-hardware/drivers/">Geräte Instanzen</a> auf einem lokalen oder einem Remote Computer ab.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_id_list_sizea"><strong>CM_Get_Device_ID_List_Size</strong></a><br/></td>
<td>Die <strong>CM_Get_Device_ID_List_Size</strong> -Funktion Ruft die Puffergröße ab, die erforderlich ist, um eine Liste der <a href="/windows-hardware/drivers/install/device-instance-ids">Geräte Instanz-IDs</a> für die <a href="/windows-hardware/drivers/">Geräte Instanzen</a>des lokalen Computers zu speichern.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_id_list_size_exw"><strong>CM_Get_Device_ID_List_Size_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Ab Windows 8 und Windows Server 2012 wurde diese Funktion als veraltet markiert. Verwenden Sie stattdessen <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_id_list_sizea"><strong>CM_Get_Device_ID_List_Size</strong></a> .
</blockquote>
<br/> Die <strong>CM_Get_Device_ID_List_Size_Ex</strong> Funktion Ruft die Puffergröße ab, die erforderlich ist, um eine Liste der <a href="/windows-hardware/drivers/install/device-instance-ids">Geräte Instanz-IDs</a> für die <a href="/windows-hardware/drivers/">Geräte Instanzen</a>eines lokalen Computers oder eines Remote Computers zu speichern.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_id_size"><strong>CM_Get_Device_ID_Size</strong></a><br/></td>
<td>Die <strong>CM_Get_Device_ID_Size</strong> -Funktion Ruft die Puffergröße ab, die zum Speichern einer <a href="/windows-hardware/drivers/install/device-instance-ids">Geräte Instanz-ID</a> für eine <a href="/windows-hardware/drivers/">Geräte Instanz</a> auf dem lokalen Computer erforderlich ist.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_id_size_ex"><strong>CM_Get_Device_ID_Size_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Ab Windows 8 und Windows Server 2012 wurde diese Funktion als veraltet markiert. Verwenden Sie stattdessen <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_id_size"><strong>CM_Get_Device_ID_Size</strong></a> .
</blockquote>
<br/> Die <strong>CM_Get_Device_ID_Size_Ex</strong> -Funktion Ruft die Puffergröße ab, die zum Speichern einer <a href="/windows-hardware/drivers/install/device-instance-ids">Geräte Instanz-ID</a> für eine <a href="/windows-hardware/drivers/">Geräte Instanz</a> auf einem lokalen oder einem Remote Computer erforderlich ist.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_interface_aliasw"><strong>CM_Get_Device_Interface_Alias</strong></a><br/></td>
<td>Die <strong>CM_Get_Device_Interface_Alias</strong> -Funktion gibt den Alias der angegebenen Geräteschnittstellen Instanz zurück, wenn der Alias vorhanden ist.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_interface_lista"><strong>CM_Get_Device_Interface_List</strong></a><br/></td>
<td>Die <strong>CM_Get_Device_Interface_List</strong> -Funktion Ruft eine Liste von Geräteschnittstellen Instanzen ab, die zu einer angegebenen <a href="/windows-hardware/drivers/install/device-interface-classes">Geräteschnittstellen Klasse</a>gehören.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_interface_list_sizea"><strong>CM_Get_Device_Interface_List_Size</strong></a><br/></td>
<td>Die <strong>CM_Get_Device_Interface_List_Size</strong> -Funktion Ruft die Puffergröße ab, die an die <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_interface_lista"><strong>CM_Get_Device_Interface_List</strong></a> -Funktion übermittelt werden muss.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_interface_propertyw"><strong>CM_Get_Device_Interface_Property</strong></a><br/></td>
<td>Die <strong>CM_Get_Device_Interface_Property</strong> -Funktion Ruft eine Geräte Eigenschaft ab, die für eine Geräteschnittstelle festgelegt ist.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_interface_property_exw"><strong>CM_Get_Device_Interface_Property_ExW</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Ab Windows 8 und Windows Server 2012 wurde diese Funktion als veraltet markiert. Verwenden Sie stattdessen <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_interface_propertyw"><strong>CM_Get_Device_Interface_Property</strong></a> .
</blockquote>
<br/> Die <strong>CM_Get_Device_Interface_Property_ExW</strong> -Funktion Ruft eine Geräte Eigenschaft ab, die für eine Geräteschnittstelle festgelegt ist.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_interface_property_keysw"><strong>CM_Get_Device_Interface_Property_Keys</strong></a><br/></td>
<td>Die <strong>CM_Get_Device_Interface_Property_Keys</strong> -Funktion Ruft ein Array von Geräte Eigenschafts Schlüsseln ab, die die Geräteeigenschaften darstellen, die für eine Geräteschnittstelle festgelegt sind.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_interface_property_keys_exw"><strong>CM_Get_Device_Interface_Property_Keys_ExW</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Ab Windows 8 und Windows Server 2012 wurde diese Funktion als veraltet markiert. Verwenden Sie stattdessen <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_interface_property_keysw"><strong>CM_Get_Device_Interface_Property_Keys</strong></a> .
</blockquote>
<br/> Die <strong>CM_Get_Device_Interface_Property_Keys_ExW</strong> -Funktion Ruft ein Array von Geräte Eigenschafts Schlüsseln ab, die die Geräteeigenschaften darstellen, die für eine Geräteschnittstelle festgelegt sind.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_devnode_propertyw"><strong>CM_Get_DevNode_Property</strong></a><br/></td>
<td>Die <strong>CM_Get_DevNode_Property</strong> -Funktion Ruft eine geräteinstanzeigenschaft ab.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_devnode_property_exw"><strong>CM_Get_DevNode_Property_ExW</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Ab Windows 8 und Windows Server 2012 wurde diese Funktion als veraltet markiert. Verwenden Sie stattdessen <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_devnode_propertyw"><strong>CM_Get_DevNode_Property</strong></a> .
</blockquote>
<br/> Die <strong>CM_Get_DevNode_Property_ExW</strong> -Funktion Ruft eine geräteinstanzeigenschaft ab.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_devnode_property_keys"><strong>CM_Get_DevNode_Property_Keys</strong></a><br/></td>
<td>Die <strong>CM_Get_DevNode_Property_Keys</strong> -Funktion Ruft ein Array der Geräte Eigenschafts Schlüssel ab, die die Geräteeigenschaften darstellen, die für eine Geräte Instanz festgelegt sind.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_devnode_property_keys_ex"><strong>CM_Get_DevNode_Property_Keys_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Ab Windows 8 und Windows Server 2012 wurde diese Funktion als veraltet markiert. Verwenden Sie stattdessen <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_devnode_property_keys"><strong>CM_Get_DevNode_Property_Keys</strong></a> .
</blockquote>
<br/> Die <strong>CM_Get_DevNode_Property_Keys_Ex</strong> -Funktion Ruft ein Array der Geräte Eigenschafts Schlüssel ab, die die Geräteeigenschaften darstellen, die für eine Geräte Instanz festgelegt sind.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_devnode_registry_propertyw"><strong>CM_Get_DevNode_Registry_Property</strong></a><br/></td>
<td>Die <strong>CM_Get_DevNode_Registry_Property</strong> -Funktion Ruft eine angegebene Geräte Eigenschaft aus der Registrierung ab.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_devnode_status"><strong>CM_Get_DevNode_Status</strong></a><br/></td>
<td>Die <strong>CM_Get_DevNode_Status</strong> Funktion Ruft den Status einer Geräte Instanz von Ihrem Geräteknoten (<a href="/windows-hardware/drivers/">devnode</a>) in der <a href="/windows-hardware/drivers/kernel/device-tree">Geräte</a>Struktur des lokalen Computers ab.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_devnode_status_ex"><strong>CM_Get_DevNode_Status_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Ab Windows 8 und Windows Server 2012 wurde diese Funktion als veraltet markiert. Verwenden Sie stattdessen <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_devnode_status"><strong>CM_Get_DevNode_Status</strong></a> .
</blockquote>
<br/> Die <strong>CM_Get_DevNode_Status_Ex</strong> Funktion Ruft den Status einer Geräte Instanz von seinem Geräteknoten (<a href="/windows-hardware/drivers/">devnode</a>) auf einem lokalen oder einem Remote Computer in der <a href="/windows-hardware/drivers/kernel/device-tree">Geräte</a>Struktur ab.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_first_log_conf"><strong>CM_Get_First_Log_Conf</strong></a><br/></td>
<td>Die <strong>CM_Get_First_Log_Conf</strong> Funktion Ruft die erste <a href="/windows-hardware/drivers/kernel/hardware-resources">logische Konfiguration</a>eines angegebenen Konfigurations Typs ab, die einer angegebenen <a href="/windows-hardware/drivers/">Geräte Instanz</a> auf dem lokalen Computer zugeordnet ist.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_first_log_conf_ex"><strong>CM_Get_First_Log_Conf_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Ab Windows 8 und Windows Server 2012 wurde diese Funktion als veraltet markiert. Verwenden Sie stattdessen <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_first_log_conf"><strong>CM_Get_First_Log_Conf</strong></a> .
</blockquote>
<br/> Die <strong>CM_Get_First_Log_Conf_Ex</strong> Funktion Ruft die erste <a href="/windows-hardware/drivers/kernel/hardware-resources">logische Konfiguration</a> ab, die einer angegebenen <a href="/windows-hardware/drivers/">Geräte Instanz</a> auf einem lokalen oder einem Remote Computer zugeordnet ist.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_hw_prof_flagsa"><strong>CM_Get_HW_Prof_Flags</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Ab Windows 8 und Windows Server 2012 ist diese Funktion veraltet und sollte nicht verwendet werden.
</blockquote>
<br/> Die <strong>CM_Get_HW_Prof_Flags</strong> -Funktion Ruft die <a href="/windows-hardware/drivers/">Hardwareprofil</a>spezifischen Konfigurationsflags für eine <a href="/windows-hardware/drivers/">Geräte Instanz</a> auf einem lokalen Computer ab.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_hw_prof_flags_exa"><strong>CM_Get_HW_Prof_Flags_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Diese Funktion ist veraltet und sollte nicht verwendet werden.
</blockquote>
<br/> Die <strong>CM_Get_HW_Prof_Flags_Ex</strong> -Funktion Ruft die <a href="/windows-hardware/drivers/">Hardwareprofil</a>spezifischen Konfigurationsflags für eine <a href="/windows-hardware/drivers/">Geräte Instanz</a> auf einem Remote Computer oder einem lokalen Computer ab.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_log_conf_priority"><strong>CM_Get_Log_Conf_Priority</strong></a><br/></td>
<td>Die <strong>CM_Get_Log_Conf_Priority</strong> Funktion Ruft die Konfigurations Priorität einer angegebenen <a href="/windows-hardware/drivers/kernel/hardware-resources">logischen Konfiguration</a> auf dem lokalen Computer ab.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_log_conf_priority_ex"><strong>CM_Get_Log_Conf_Priority_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Ab Windows 8 und Windows Server 2012 wurde diese Funktion als veraltet markiert. Verwenden Sie stattdessen <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_log_conf_priority"><strong>CM_Get_Log_Conf_Priority</strong></a> .
</blockquote>
<br/> Die <strong>CM_Get_Log_Conf_Priority_Ex</strong> Funktion Ruft die Konfigurations Priorität einer angegebenen <a href="/windows-hardware/drivers/kernel/hardware-resources">logischen Konfiguration</a> auf einem lokalen oder einem Remote Computer ab.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_next_log_conf"><strong>CM_Get_Next_Log_Conf</strong></a><br/></td>
<td>Die <strong>CM_Get_Next_Log_Conf</strong> Funktion Ruft die nächste <a href="/windows-hardware/drivers/kernel/hardware-resources">logische Konfiguration</a> ab, die einer bestimmten <a href="/windows-hardware/drivers/">Geräte Instanz</a> auf dem lokalen Computer zugeordnet ist.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_next_log_conf_ex"><strong>CM_Get_Next_Log_Conf_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Ab Windows 8 und Windows Server 2012 wurde diese Funktion als veraltet markiert. Verwenden Sie stattdessen <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_next_log_conf"><strong>CM_Get_Next_Log_Conf</strong></a> .
</blockquote>
<br/> Die <strong>CM_Get_Next_Log_Conf_Ex</strong> Funktion Ruft die nächste <a href="/windows-hardware/drivers/kernel/hardware-resources">logische Konfiguration</a> ab, die einer bestimmten <a href="/windows-hardware/drivers/">Geräte Instanz</a> auf einem lokalen oder einem Remote Computer zugeordnet ist.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_next_res_des"><strong>CM_Get_Next_Res_Des</strong></a><br/></td>
<td>Die <strong>CM_Get_Next_Res_Des</strong> -Funktion Ruft ein Handle für den nächsten <a href="/windows-hardware/drivers/">Ressourcen Deskriptor</a>eines angegebenen Ressourcentyps für eine <a href="/windows-hardware/drivers/kernel/hardware-resources">logische Konfiguration</a> auf dem lokalen Computer ab.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_next_res_des_ex"><strong>CM_Get_Next_Res_Des_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Ab Windows 8 und Windows Server 2012 wurde diese Funktion als veraltet markiert. Verwenden Sie stattdessen <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_next_res_des"><strong>CM_Get_Next_Res_Des</strong></a> .
</blockquote>
<br/> Die <strong>CM_Get_Next_Res_Des_Ex</strong> -Funktion Ruft ein Handle für den nächsten <a href="/windows-hardware/drivers/">Ressourcen Deskriptor</a>eines angegebenen Ressourcentyps für eine <a href="/windows-hardware/drivers/kernel/hardware-resources">logische Konfiguration</a> auf einem lokalen oder einem Remote Computer ab.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_parent"><strong>CM_Get_Parent</strong></a><br/></td>
<td>Die <strong>CM_Get_Parent</strong> Funktion Ruft ein geräteinstanzhandle für den übergeordneten Knoten eines angegebenen Geräte Knotens (<a href="/windows-hardware/drivers/">devnode</a>) in der Gerätestruktur des lokalen Computers ab.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_parent_ex"><strong>CM_Get_Parent_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Ab Windows 8 und Windows Server 2012 wurde diese Funktion als veraltet markiert. Verwenden Sie stattdessen <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_parent"><strong>CM_Get_Parent</strong></a> .
</blockquote>
<br/> Die <strong>CM_Get_Parent_Ex</strong> -Funktion Ruft ein geräteinstanzhandle für den übergeordneten Knoten eines angegebenen Geräte Knotens (<a href="/windows-hardware/drivers/">devnode</a>) in der <a href="/windows-hardware/drivers/kernel/device-tree">Geräte</a>Struktur eines lokalen Computers oder eines Remote Computers ab.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_res_des_data"><strong>CM_Get_Res_Des_Data</strong></a><br/></td>
<td>Die <strong>CM_Get_Res_Des_Data</strong> -Funktion Ruft die Informationen ab, die in einem <a href="/windows-hardware/drivers/">Ressourcen Deskriptor</a> auf dem lokalen Computer gespeichert sind.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_res_des_data_ex"><strong>CM_Get_Res_Des_Data_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Ab Windows 8 und Windows Server 2012 wurde diese Funktion als veraltet markiert. Verwenden Sie stattdessen <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_res_des_data"><strong>CM_Get_Res_Des_Data</strong></a> .
</blockquote>
<br/> Die <strong>CM_Get_Res_Des_Data_Ex</strong> -Funktion Ruft die Informationen ab, die in einem <a href="/windows-hardware/drivers/">Ressourcen Deskriptor</a> auf einem lokalen oder einem Remote Computer gespeichert sind.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_res_des_data_size"><strong>CM_Get_Res_Des_Data_Size</strong></a><br/></td>
<td>Die <strong>CM_Get_Res_Des_Data_Size</strong> Funktion Ruft die Puffergröße ab, die zum Speichern der Informationen in einem angegebenen <a href="/windows-hardware/drivers/">Ressourcen Deskriptor</a> auf dem lokalen Computer erforderlich ist.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_res_des_data_size_ex"><strong>CM_Get_Res_Des_Data_Size_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Ab Windows 8 und Windows Server 2012 wurde diese Funktion als veraltet markiert. Verwenden Sie stattdessen <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_res_des_data_size"><strong>CM_Get_Res_Des_Data_Size</strong></a> .
</blockquote>
<br/> Die <strong>CM_Get_Res_Des_Data_Size_Ex</strong> Funktion Ruft die Puffergröße ab, die zum Speichern der Informationen in einem angegebenen <a href="/windows-hardware/drivers/">Ressourcen Deskriptor</a> auf einem lokalen oder einem Remote Computer erforderlich ist.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_resource_conflict_count"><strong>CM_Get_Resource_Conflict_Count</strong></a><br/></td>
<td>Die <strong>CM_Get_Resource_Conflict_Count</strong> Funktion Ruft die Anzahl von Konflikten ab, die in einer angegebenen Ressourcen Konflikt Liste enthalten sind.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_resource_conflict_detailsw"><strong>CM_Get_Resource_Conflict_Details</strong></a><br/></td>
<td>Die <strong>CM_Get_Resource_Conflict_Details</strong> -Funktion Ruft die Details zu einem der Ressourcenkonflikte in einer Konflikt Liste ab.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_sibling"><strong>CM_Get_Sibling</strong></a><br/></td>
<td>Die <strong>CM_Get_Sibling</strong> -Funktion Ruft ein geräteinstanzhandle für den nächsten neben geordneten Knoten eines angegebenen Geräte Knotens (<a href="/windows-hardware/drivers/">devnode</a>) in der <a href="/windows-hardware/drivers/kernel/device-tree">Geräte</a>Struktur des lokalen Computers ab.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_sibling_ex"><strong>CM_Get_Sibling_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Ab Windows 8 und Windows Server 2012 wurde diese Funktion als veraltet markiert. Verwenden Sie stattdessen <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_sibling"><strong>CM_Get_Sibling</strong></a> .
</blockquote>
<br/> Die <strong>CM_Get_Sibling_Ex</strong> -Funktion Ruft ein geräteinstanzhandle für den nächsten neben geordneten Knoten eines angegebenen Geräte Knotens in einer lokalen oder einem Remote Computer- <a href="/windows-hardware/drivers/kernel/device-tree">Geräte</a>Struktur ab.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_version"><strong>CM_Get_Version</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Ab Windows 8 und Windows Server 2012 ist diese Funktion veraltet und sollte nicht verwendet werden.
</blockquote>
<br/> Die <strong>CM_Get_Version</strong> -Funktion gibt Version 4,0 des Plug & Play (PNP) Configuration Manager <a href="/windows-hardware/drivers/">dll</a> (<em>Cfgmgr32.dll</em>) für einen lokalen Computer zurück. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_version_ex"><strong>CM_Get_Version_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Ab Windows 8 und Windows Server 2012 ist diese Funktion veraltet und sollte nicht verwendet werden.
</blockquote>
<br/> Die <strong>CM_Get_Version_Ex</strong> -Funktion gibt Version 4,0 des Plug & Play (PNP) Configuration Manager <a href="/windows-hardware/drivers/">dll</a> (<em>Cfgmgr32.dll</em>) für einen lokalen oder einen Remote Computer zurück. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_is_dock_station_present"><strong>CM_Is_Dock_Station_Present</strong></a><br/></td>
<td>Die <strong>CM_Is_Dock_Station_Present</strong> -Funktion gibt an, ob eine <a href="/windows-hardware/drivers/">Docking Station</a> auf einem lokalen Computer vorhanden ist.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_is_dock_station_present_ex"><strong>CM_Is_Dock_Station_Present_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Ab Windows 8 und Windows Server 2012 wurde diese Funktion als veraltet markiert. Verwenden Sie stattdessen <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_is_dock_station_present"><strong>CM_Is_Dock_Station_Present</strong></a> .
</blockquote>
<br/> Die <strong>CM_Is_Dock_Station_Present_Ex</strong> -Funktion gibt an, ob eine <a href="/windows-hardware/drivers/">Docking Station</a> auf einem lokalen oder einem Remote Computer vorhanden ist.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_is_version_available"><strong>CM_Is_Version_Available</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Ab Windows 8 und Windows Server 2012 ist diese Funktion veraltet und sollte nicht verwendet werden.
</blockquote>
<br/> Die <strong>CM_Is_Version_Available</strong> -Funktion gibt an, ob eine angegebene Version des Plug & Play (PNP) Configuration Manager <a href="/windows-hardware/drivers/">dll</a> (<em>Cfgmgr32.dll</em>) von einem lokalen Computer unterstützt wird.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_is_version_available_ex"><strong>CM_Is_Version_Available_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Ab Windows 8 und Windows Server 2012 ist diese Funktion veraltet und sollte nicht verwendet werden.
</blockquote>
<br/> Die <strong>CM_Is_Version_Available_Ex</strong> -Funktion gibt an, ob eine angegebene Version des Plug & Play (PNP) Configuration Manager <a href="/windows-hardware/drivers/">dll</a> (<em>Cfgmgr32.dll</em>) von einem lokalen oder einem Remote Computer unterstützt wird.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_locate_devnodea"><strong>CM_Locate_DevNode</strong></a><br/></td>
<td>Die <strong>CM_Locate_DevNode</strong> -Funktion Ruft ein geräteinstanzhandle für den Geräteknoten ab, der einer angegebenen <a href="/windows-hardware/drivers/install/device-instance-ids">Geräte Instanz-ID</a> auf dem lokalen Computer zugeordnet ist.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_locate_devnode_exw"><strong>CM_Locate_DevNode_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Ab Windows 8 und Windows Server 2012 wurde diese Funktion als veraltet markiert. Verwenden Sie stattdessen <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_locate_devnodea"><strong>CM_Locate_DevNode</strong></a> .
</blockquote>
<br/> Die <strong>CM_Locate_DevNode_Ex</strong> -Funktion Ruft ein geräteinstanzhandle für den Geräteknoten ab, der einer angegebenen <a href="/windows-hardware/drivers/install/device-instance-ids">Geräte Instanz-ID</a>auf einem lokalen Computer oder einem Remote Computer zugeordnet ist.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_mapcrtowin32err"><strong>CM_MapCrToWin32Err</strong></a><br/></td>
<td>Konvertiert einen angegebenen <strong>configret</strong> -Code in den entsprechenden Systemfehler Code.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_modify_res_des"><strong>CM_Modify_Res_Des</strong></a><br/></td>
<td>Die <strong>CM_Modify_Res_Des</strong> -Funktion ändert einen angegebenen Ressourcen Deskriptor auf dem lokalen Computer.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_modify_res_des_ex"><strong>CM_Modify_Res_Des_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Ab Windows 8 und Windows Server 2012 wurde diese Funktion als veraltet markiert. Verwenden Sie stattdessen <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_modify_res_des"><strong>CM_Modify_Res_Des</strong></a> .
</blockquote>
<br/> Die <strong>CM_Modify_Res_Des_Ex</strong> -Funktion ändert einen angegebenen Ressourcen Deskriptor auf einem lokalen oder einem Remote Computer.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/ne-cfgmgr32-cm_notify_action"><strong>CM_NOTIFY_ACTION</strong></a><br/></td>
<td>Diese Enumeration identifiziert Plug & Play Geräte Ereignis Typen.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/ns-cfgmgr32-cm_notify_event_data"><strong>CM_NOTIFY_EVENT_DATA</strong></a><br/></td>
<td>Dabei handelt es sich um eine Datenstruktur für Geräte Benachrichtigungs Ereignisse.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/ns-cfgmgr32-cm_notify_filter"><strong>CM_NOTIFY_FILTER</strong></a><br/></td>
<td>Struktur der Geräte Benachrichtigungs Filter<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_open_class_keyw"><strong>CM_Open_Class_Key</strong></a><br/></td>
<td>Die <strong>CM_Open_Class_Key</strong> -Funktion öffnet den Registrierungsschlüssel für die Geräte Setup Klasse, den Registrierungsschlüssel der Geräteschnittstellen Klasse oder einen bestimmten Unterschlüssel einer Klasse.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_open_device_interface_keyw"><strong>CM_Open_Device_Interface_Key</strong></a><br/></td>
<td>Die <strong>CM_Open_Device_Interface_Key</strong> -Funktion öffnet den Registrierungs Unterschlüssel, der von Anwendungen und Treibern verwendet wird, um Informationen zu speichern, die für eine Geräteschnittstelle spezifisch sind.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_open_device_interface_keya"><strong>CM_Open_Device_Interface_Key_ExA</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Ab Windows 8 und Windows Server 2012 wurde diese Funktion als veraltet markiert. Verwenden Sie stattdessen <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_open_device_interface_keyw"><strong>CM_Open_Device_Interface_Key</strong></a> .
</blockquote>
<br/> Die <strong>CM_Open_Device_Interface_Key_ExA</strong> -Funktion öffnet den Registrierungs Unterschlüssel, der von Anwendungen und Treibern verwendet wird, um Informationen zu speichern, die für eine Geräteschnittstelle spezifisch sind.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_open_device_interface_key_exw"><strong>CM_Open_Device_Interface_Key_ExW</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Ab Windows 8 und Windows Server 2012 wurde diese Funktion als veraltet markiert. Verwenden Sie stattdessen <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_open_device_interface_keyw"><strong>CM_Open_Device_Interface_Key</strong></a> .
</blockquote>
<br/> Die <strong>CM_Open_Device_Interface_Key_ExW</strong> -Funktion öffnet den Registrierungs Unterschlüssel, der von Anwendungen und Treibern verwendet wird, um Informationen zu speichern, die für eine Geräteschnittstelle spezifisch sind.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_open_devnode_key"><strong>CM_Open_DevNode_Key</strong></a><br/></td>
<td>Die <strong>CM_Open_DevNode_Key</strong> -Funktion öffnet einen Registrierungsschlüssel für gerätespezifische Konfigurationsinformationen.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_query_and_remove_subtreew"><strong>CM_Query_And_Remove_SubTree</strong></a><br/></td>
<td>Die <strong>CM_Query_And_Remove_SubTree</strong> -Funktion überprüft, ob eine Geräte Instanz und deren untergeordnete Elemente entfernt werden können. wenn dies der Fall ist, werden Sie entfernt.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_query_and_remove_subtree_exw"><strong>CM_Query_And_Remove_SubTree_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Ab Windows 8 und Windows Server 2012 wurde diese Funktion als veraltet markiert. Verwenden Sie stattdessen <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_query_and_remove_subtreew"><strong>CM_Query_And_Remove_SubTree</strong></a> .
</blockquote>
<br/> Die <strong>CM_Query_And_Remove_SubTree_Ex</strong> -Funktion überprüft, ob eine Geräte Instanz und deren untergeordnete Elemente entfernt werden können. wenn dies der Fall ist, werden Sie entfernt.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_query_resource_conflict_list"><strong>CM_Query_Resource_Conflict_List</strong></a><br/></td>
<td>Die <strong>CM_Query_Resource_Conflict_List</strong> -Funktion identifiziert Geräte Instanzen mit Ressourcenanforderungen, die in Konflikt mit der Ressourcen Beschreibung einer angegebenen Geräte Instanz stehen.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_reenumerate_devnode"><strong>CM_Reenumerate_DevNode</strong></a><br/></td>
<td>Die <strong>CM_Reenumerate_DevNode</strong> -Funktion Listet die Geräte auf, die durch einen angegebenen Geräteknoten und alle untergeordneten Elemente identifiziert werden.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_reenumerate_devnode_ex"><strong>CM_Reenumerate_DevNode_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Ab Windows 8 und Windows Server 2012 wurde diese Funktion als veraltet markiert. Verwenden Sie stattdessen <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_reenumerate_devnode"><strong>CM_Reenumerate_DevNode</strong></a> .
</blockquote>
<br/> Die <strong>CM_Reenumerate_DevNode_Ex</strong> -Funktion Listet die Geräte auf, die durch einen angegebenen Geräteknoten und alle untergeordneten Elemente identifiziert werden.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_register_notification"><strong>CM_Register_Notification</strong></a><br/></td>
<td>Verwenden Sie <a href="/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa"><strong>registerdevicenotifianstelle</strong></a> von <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_register_notification"><strong>CM_Register_Notification</strong></a> , wenn Ihr Code auf Windows 7 oder frühere Versionen von Windows abzielt. Kernelmodusaufrufer sollten stattdessen <a href="/windows-hardware/drivers/ddi/content/wdm/nf-wdm-ioregisterplugplaynotification"><strong>IoRegisterPlugPlayNotification</strong></a> verwenden.<br/> Die <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_register_notification"><strong>CM_Register_Notification</strong></a> -Funktion registriert eine Anwendungs Rückruf Routine, die aufgerufen werden soll, wenn ein PNP-Ereignis des angegebenen Typs auftritt.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_request_device_ejectw"><strong>CM_Request_Device_Eject</strong></a><br/></td>
<td>Die <strong>CM_Request_Device_Eject</strong> -Funktion bereitet eine lokale Geräte Instanz vor dem sicheren Entfernen vor, wenn das Gerät entfernt werden kann. Wenn das Gerät physisch ausgestoßen werden kann, ist es.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_request_device_eject_exw"><strong>CM_Request_Device_Eject_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Ab Windows 8 und Windows Server 2012 wurde diese Funktion als veraltet markiert. Verwenden Sie stattdessen <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_request_device_ejectw"><strong>CM_Request_Device_Eject</strong></a> .
</blockquote>
<br/> Die <strong>CM_Request_Device_Eject_Ex</strong> -Funktion bereitet eine lokale oder eine Remote Geräte Instanz vor dem sicheren Entfernen vor, wenn das Gerät wechselseitig ist. Wenn das Gerät physisch ausgestoßen werden kann, ist es.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_request_eject_pc"><strong>CM_Request_Eject_PC</strong></a><br/></td>
<td>Die <strong>CM_Request_Eject_PC</strong> -Funktion fordert an, dass ein tragbarer PC, der in eine lokale <a href="/windows-hardware/drivers/">Docking Station</a>eingefügt wird, aussteht.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_request_eject_pc_ex"><strong>CM_Request_Eject_PC_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Ab Windows 8 und Windows Server 2012 wurde diese Funktion als veraltet markiert. Verwenden Sie stattdessen <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_request_eject_pc"><strong>CM_Request_Eject_PC</strong></a> .
</blockquote>
<br/> Die <strong>CM_Request_Eject_PC_Ex</strong> Funktion fordert an, dass ein tragbarer PC, der in eine lokale oder eine Remote <a href="/windows-hardware/drivers/">Docking Station</a>eingefügt wird, aussteht.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_class_propertyw"><strong>CM_Set_Class_Property</strong></a><br/></td>
<td>Die <strong>CM_Set_Class_Property</strong> -Funktion legt eine Klassen Eigenschaft für eine Geräte Setup Klasse oder eine Geräteschnittstellen Klasse fest.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_class_property_exw"><strong>CM_Set_Class_Property_ExW</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Ab Windows 8 und Windows Server 2012 wurde diese Funktion als veraltet markiert. Verwenden Sie stattdessen <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_class_propertyw"><strong>CM_Set_Class_Property</strong></a> .
</blockquote>
<br/> Die <strong>CM_Set_Class_Property_ExW</strong> -Funktion legt eine Klassen Eigenschaft für eine Geräte Setup Klasse oder eine Geräteschnittstellen Klasse fest.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_class_registry_propertyw"><strong>CM_Set_Class_Registry_Property</strong></a><br/></td>
<td>Mit der <strong>CM_Set_Class_Registry_Property</strong> -Funktion wird eine Eigenschaft einer <a href="/windows-hardware/drivers/install/device-setup-classes">Geräte Setup Klasse</a>festgelegt oder gelöscht.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_device_interface_propertyw"><strong>CM_Set_Device_Interface_Property</strong></a><br/></td>
<td>Die <strong>CM_Set_Device_Interface_Property</strong> -Funktion legt eine Geräte Eigenschaft einer Geräteschnittstelle fest.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_device_interface_property_exw"><strong>CM_Set_Device_Interface_Property_ExW</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Ab Windows 8 und Windows Server 2012 wurde diese Funktion als veraltet markiert. Verwenden Sie stattdessen <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_device_interface_propertyw"><strong>CM_Set_Device_Interface_Property</strong></a> .
</blockquote>
<br/> Die <strong>CM_Set_Device_Interface_Property_ExW</strong> -Funktion legt eine Geräte Eigenschaft einer Geräteschnittstelle fest.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_devnode_problem"><strong>CM_Set_DevNode_Problem</strong></a><br/></td>
<td>Mit der <strong>CM_Set_DevNode_Problem</strong> -Funktion wird ein Problem Code für ein Gerät festgelegt, das auf einem lokalen Computer installiert ist.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_devnode_problem_ex"><strong>CM_Set_DevNode_Problem_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Ab Windows 8 und Windows Server 2012 wurde diese Funktion als veraltet markiert. Verwenden Sie stattdessen <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_devnode_problem"><strong>CM_Set_DevNode_Problem</strong></a> .
</blockquote>
<br/> Mit der <strong>CM_Set_DevNode_Problem_Ex</strong> -Funktion wird ein Problem Code für ein Gerät festgelegt, das auf einem lokalen Computer oder einem Remote Computer installiert ist.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_devnode_propertyw"><strong>CM_Set_DevNode_Property</strong></a><br/></td>
<td>Die <strong>CM_Set_DevNode_Property</strong> -Funktion legt eine geräteinstanzeigenschaft fest.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_devnode_property_exw"><strong>CM_Set_DevNode_Property_ExW</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Ab Windows 8 und Windows Server 2012 wurde diese Funktion als veraltet markiert. Verwenden Sie stattdessen <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_devnode_propertyw"><strong>CM_Set_DevNode_Property</strong></a> .
</blockquote>
<br/> Die <strong>CM_Set_DevNode_Property_ExW</strong> -Funktion legt eine geräteinstanzeigenschaft fest.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_devnode_registry_propertyw"><strong>CM_Set_DevNode_Registry_Property</strong></a><br/></td>
<td>Mit der <strong>CM_Set_DevNode_Registry_Property</strong> -Funktion wird eine angegebene Geräte Eigenschaft in der Registrierung festgelegt.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_setup_devnode"><strong>CM_Setup_DevNode</strong></a><br/></td>
<td>Die <strong>CM_Setup_DevNode</strong> Funktion startet eine Geräte Instanz neu, die nicht ausgeführt wird, weil ein Problem mit der Gerätekonfiguration vorliegt.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_uninstall_devnode"><strong>CM_Uninstall_DevNode</strong></a><br/></td>
<td>Die <strong>CM_Uninstall_DevNode</strong> -Funktion entfernt den gesamten permanenten Zustand, der einer Geräte Instanz zugeordnet ist.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_unregister_notification"><strong>CM_Unregister_Notification</strong></a><br/></td>
<td>Verwenden Sie <a href="/windows/desktop/api/winuser/nf-winuser-unregisterdevicenotification"><strong>unregisterdevicenotifianstelle</strong></a> von <strong>CM_Unregister_Notification</strong> , wenn Ihr Code auf Windows 7 oder frühere Versionen von Windows abzielt.<br/> Die <strong>CM_Unregister_Notification</strong> -Funktion schließt das angegebene hcmnotification-handle.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_waitnopendinginstallevents"><strong>CMP_WaitNoPendingInstallEvents</strong></a><br/></td>
<td>Die <strong>CMP_WaitNoPendingInstallEvents</strong> Funktion wartet, bis keine ausstehenden Geräte Installationsaktivitäten vorhanden sind, die der PNP-Manager ausführen muss.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/cfgmgr32/ns-cfgmgr32-conflict_details_a"><strong>CONFLICT_DETAILS</strong></a><br/></td>
<td>Die CONFLICT_DETAILS-Struktur wird als Parameter für die <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_resource_conflict_detailsw"><strong>CM_Get_Resource_Conflict_Details</strong></a> -Funktion verwendet.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-cs_des"><strong>CS_DES</strong></a><br/></td>
<td>Die CS_DES Struktur wird verwendet, um eine Ressourcen Liste anzugeben, in der die Geräteklassen spezifische Ressourcenverwendung für eine Geräte Instanz beschrieben wird. Weitere Informationen zu Ressourcen Listen finden Sie unter <a href="/windows-hardware/drivers/kernel/hardware-resources">Hardware Ressourcen</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-cs_resource"><strong>CS_RESOURCE</strong></a><br/></td>
<td>Die CS_RESOURCE Struktur wird verwendet, um eine Ressourcen Liste anzugeben, in der die Geräteklassen spezifische Ressourcenverwendung für eine Geräte Instanz beschrieben wird. Weitere Informationen zu Ressourcen Listen finden Sie unter <a href="/windows-hardware/drivers/kernel/hardware-resources">Hardware Ressourcen</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-dma_des"><strong>DMA_DES</strong></a><br/></td>
<td>Die DMA_DES Struktur wird verwendet, um entweder eine Ressourcen Liste oder eine Ressourcen Anforderungsliste anzugeben, in der die DMA-Kanal Verwendung (Direct Memory Access) für eine Geräte Instanz beschrieben wird. Weitere Informationen zu Ressourcen Listen und Ressourcen Anforderungslisten finden Sie unter <a href="/windows-hardware/drivers/kernel/hardware-resources">Hardware Ressourcen</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-dma_range"><strong>DMA_RANGE</strong></a><br/></td>
<td>Die DMA_RANGE-Struktur gibt eine Ressourcen Anforderungsliste an, die die Verwendung von DMA-Kanälen für eine Geräte Instanz beschreibt. Weitere Informationen zu Ressourcen Anforderungslisten finden Sie unter <a href="/windows-hardware/drivers/kernel/hardware-resources">Hardware Ressourcen</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-dma_resource"><strong>DMA_RESOURCE</strong></a><br/></td>
<td>Die DMA_RESOURCE Struktur wird verwendet, um entweder eine Ressourcen Liste oder eine Ressourcen Anforderungsliste anzugeben, in der die DMA-Kanal Verwendung für eine Geräte Instanz beschrieben wird. Weitere Informationen zu Ressourcen Listen-und Ressourcen Anforderungslisten finden Sie unter <a href="/windows-hardware/drivers/kernel/hardware-resources">Hardware Ressourcen</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-io_des"><strong>IO_DES</strong></a><br/></td>
<td>Die IO_DES Struktur wird verwendet, um entweder eine Ressourcen Liste oder eine Ressourcen Anforderungsliste anzugeben, in der die e/a-Port Verwendung für eine Geräte Instanz beschrieben wird. Weitere Informationen zu Ressourcen Listen und Ressourcen Anforderungslisten finden Sie unter <a href="/windows-hardware/drivers/kernel/hardware-resources">Hardware Ressourcen</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-io_range"><strong>IO_RANGE</strong></a><br/></td>
<td>Die IO_RANGE Struktur gibt eine Ressourcen Anforderungsliste an, in der die e/a-Port Verwendung für eine Geräte Instanz beschrieben wird. Weitere Informationen zu Ressourcen Anforderungslisten finden Sie unter <a href="/windows-hardware/drivers/kernel/hardware-resources">Hardware Ressourcen</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-io_resource"><strong>IO_RESOURCE</strong></a><br/></td>
<td>Die IO_RESOURCE Struktur wird verwendet, um entweder eine Ressourcen Liste oder eine Ressourcen Anforderungsliste anzugeben, in der die e/a-Port Verwendung für eine Geräte Instanz beschrieben wird. Weitere Informationen zu Ressourcen Listen und Ressourcen Anforderungslisten finden Sie unter <a href="/windows-hardware/drivers/kernel/hardware-resources">Hardware Ressourcen</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-irq_des_64"><strong>IRQ_DES</strong></a><br/></td>
<td>Die IRQ_DES Struktur wird verwendet, um entweder eine Ressourcen Liste oder eine Ressourcen Anforderungsliste anzugeben, in der die Verwendung der Verwendung der Verwendung von in einer Geräte Instanz beschrieben wird. Weitere Informationen zu Ressourcen Listen und Ressourcen Anforderungslisten finden Sie unter <a href="/windows-hardware/drivers/kernel/hardware-resources">Hardware Ressourcen</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-irq_range"><strong>IRQ_RANGE</strong></a><br/></td>
<td>Die IRQ_RANGE-Struktur gibt eine Ressourcen Anforderungsliste an, die die Verwendung der Verwendung der Verwendung von in einer Geräte Instanz beschreibt. Weitere Informationen zu Ressourcen Anforderungslisten finden Sie unter <a href="/windows-hardware/drivers/kernel/hardware-resources">Hardware Ressourcen</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-irq_resource_64"><strong>IRQ_RESOURCE</strong></a><br/></td>
<td>Die IRQ_RESOURCE Struktur wird verwendet, um entweder eine Ressourcen Liste oder eine Ressourcen Anforderungsliste anzugeben, in der die Verwendung der Verwendung der Verwendung von in einer Geräte Instanz beschrieben wird. Weitere Informationen zu Ressourcen Listen und Ressourcen Anforderungslisten finden Sie unter <a href="/windows-hardware/drivers/kernel/hardware-resources">Hardware Ressourcen</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-mem_des"><strong>MEM_DES</strong></a><br/></td>
<td>Die MEM_DES Struktur wird verwendet, um entweder eine Ressourcen Liste oder eine Ressourcen Anforderungsliste anzugeben, in der die Speicherauslastung für eine Geräte Instanz beschrieben wird. Weitere Informationen zu Ressourcen Listen und Ressourcen Anforderungslisten finden Sie unter <a href="/windows-hardware/drivers/kernel/hardware-resources">Hardware Ressourcen</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-mem_range"><strong>MEM_RANGE</strong></a><br/></td>
<td>Die MEM_RANGE-Struktur gibt eine Ressourcen Anforderungsliste an, in der die Speicherauslastung für eine Geräte Instanz beschrieben wird. Weitere Informationen zu Ressourcen Anforderungslisten finden Sie unter <a href="/windows-hardware/drivers/kernel/hardware-resources">Hardware Ressourcen</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-mem_resource"><strong>MEM_RESOURCE</strong></a><br/></td>
<td>Die MEM_RESOURCE Struktur wird verwendet, um entweder eine Ressourcen Liste oder eine Ressourcen Anforderungsliste anzugeben, in der die Speicherauslastung für eine Geräte Instanz beschrieben wird. Weitere Informationen zu Ressourcen Listen und Ressourcen Anforderungslisten finden Sie unter <a href="/windows-hardware/drivers/kernel/hardware-resources">Hardware Ressourcen</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-mfcard_des"><strong>MFCARD_DES</strong></a><br/></td>
<td>Die MFCARD_DES Struktur wird verwendet, um entweder eine Ressourcen Liste oder eine Ressourcen Anforderungsliste anzugeben, die die Ressourcenverwendung durch <em>eine</em> der Hardwarefunktionen beschreibt, die von einer Instanz eines Multifunktionsgeräts bereitgestellt werden. Weitere Informationen zu Ressourcen Listen und Ressourcen Anforderungslisten finden Sie unter <a href="/windows-hardware/drivers/kernel/hardware-resources">Hardware Ressourcen</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-mfcard_resource"><strong>MFCARD_RESOURCE</strong></a><br/></td>
<td>Die MFCARD_RESOURCE Struktur wird verwendet, um entweder eine Ressourcen Liste oder eine Ressourcen Anforderungsliste anzugeben, die die Ressourcenverwendung durch <em>eine</em> der Hardwarefunktionen beschreibt, die von einer Instanz eines Multifunktionsgeräts bereitgestellt werden. Weitere Informationen zu Ressourcen Listen und Ressourcen Anforderungslisten finden Sie unter <a href="/windows-hardware/drivers/kernel/hardware-resources">Hardware Ressourcen</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-pccard_des"><strong>PCCARD_DES</strong></a><br/></td>
<td>Die PCCARD_DES Struktur wird verwendet, um entweder eine Ressourcen Liste oder eine Ressourcen Anforderungsliste anzugeben, in der die Ressourcenverwendung durch eine PC-Karten Instanz beschrieben wird. Weitere Informationen zu Ressourcen Listen und Ressourcen Anforderungslisten finden Sie unter <a href="/windows-hardware/drivers/kernel/hardware-resources">Hardware Ressourcen</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-pccard_resource"><strong>PCCARD_RESOURCE</strong></a><br/></td>
<td>Die PCCARD_RESOURCE Struktur wird verwendet, um entweder eine Ressourcen Liste oder eine Ressourcen Anforderungsliste anzugeben, in der die Ressourcenverwendung durch eine PC-Karten Instanz beschrieben wird. Weitere Informationen zu Ressourcen Listen und Ressourcen Anforderungslisten finden Sie unter <a href="/windows-hardware/drivers/kernel/hardware-resources">Hardware Ressourcen</a>.<br/></td>
</tr>
</tbody>
</table>



 

 

 

[Kommentare zu diesem Thema an Microsoft senden](mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback%20%5Bdevinst\devinst%5D:%20Cfgmgr32.h%20%20RELEASE:%20%283/29/2018%29&body=%0A%0APRIVACY%20STATEMENT%0A%0AWe%20use%20your%20feedback%20to%20improve%20the%20documentation.%20We%20don't%20use%20your%20email%20address%20for%20any%20other%20purpose,%20and%20we'll%20remove%20your%20email%20address%20from%20our%20system%20after%20the%20issue%20that%20you're%20reporting%20is%20fixed.%20While%20we're%20working%20to%20fix%20this%20issue,%20we%20might%20send%20you%20an%20email%20message%20to%20ask%20for%20more%20info.%20Later,%20we%20might%20also%20send%20you%20an%20email%20message%20to%20let%20you%20know%20that%20we've%20addressed%20your%20feedback.%0A%0AFor%20more%20info%20about%20Microsoft's%20privacy%20policy,%20see%20http://privacy.microsoft.com/default.aspx. "Kommentare zu diesem Thema an Microsoft senden")