---
description: Ein Satz von Zeichenfolgenschlüsseln, die mit der IBindCtx::RegisterObjectParam-Methode verwendet werden, um einen Bindungskontext anzugeben.
title: Bind Context String Keys (Shobjidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: d89a0ee1-9a4b-48a4-8965-0d92f09743a6
api_name:
- STR_AVOID_DRIVE_RESTRICTION_POLICY
- STR_BIND_DELEGATE_CREATE_OBJECT
- STR_BIND_FOLDER_ENUM_MODE
- STR_BIND_FOLDERS_READ_ONLY
- STR_BIND_FORCE_FOLDER_SHORTCUT_RESOLVE
- STR_DONT_PARSE_RELATIVE
- STR_DONT_RESOLVE_LINK
- STR_FILE_SYS_FIND_DATA
- STR_FILE_SYS_BIND_DATA_WIN7_FORMAT
- STR_GET_ASYNC_HANDLER
- STR_GPS_BESTEFFORT
- STR_GPS_DELAYCREATION
- STR_GPS_FASTPROPERTIESONLY
- STR_GPS_HANDLERPROPERTIESONLY
- STR_GPS_NO_OPLOCK
- STR_GPS_OPENSLOWITEM
- STR_IFILTER_FORCE_TEXT_FILTER_FALLBACK
- STR_IFILTER_LOAD_DEFINED_FILTER
- STR_INTERNAL_NAVIGATE
- STR_INTERNETFOLDER_PARSE_ONLY_URLMON_BINDABLE
- STR_ITEM_CACHE_CONTEXT
- STR_NO_VALIDATE_FILENAME_CHARS
- STR_PARSE_ALLOW_INTERNET_SHELL_FOLDERS
- STR_PARSE_AND_CREATE_ITEM
- STR_PARSE_DONT_REQUIRE_VALIDATED_URLS
- STR_PARSE_PARTIAL_IDLIST
- STR_PARSE_PREFER_FOLDER_BROWSING
- STR_PARSE_PREFER_WEB_BROWSING
- STR_PARSE_PROPERTYSTORE
- STR_PARSE_SHELL_PROTOCOL_TO_FILE_OBJECTS
- STR_PARSE_SHOW_NET_DIAGNOSTICS_UI
- STR_PARSE_SKIP_NET_CACHE
- STR_PARSE_TRANSLATE_ALIASES
- STR_PARSE_WITH_PROPERTIES
- STR_PROPERTYBAG_PARAM
- STR_SKIP_BINDING_CLSID
- STR_TRACK_CLSID
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 78743f18f9dc10b9c20b7e911224f1cd4e53e3f536f23686936a8f021605bf9a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118452047"
---
# <a name="bind-context-string-keys"></a>Binden von Kontextzeichenfolgenschlüsseln

Ein Satz von Zeichenfolgenschlüsseln, die mit der [**IBindCtx::RegisterObjectParam-Methode**](/windows/win32/api/objidl/nf-objidl-ibindctx-registerobjectparam) verwendet werden, um einen Bindungskontext anzugeben.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Konstante</th>
<th style="text-align: left;">Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="STR_AVOID_DRIVE_RESTRICTION_POLICY"></span><span id="str_avoid_drive_restriction_policy"></span><dl> <dt><strong>STR_AVOID_DRIVE_RESTRICTION_POLICY</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Eingeführt in Windows XP SP2</strong>. Geben Sie diesen Bindungskontext an, damit Clients der Datenquelle die Richtlinie für ausgeblendete Laufwerkbuchstaben außer Kraft setzen und den Zugriff auf die Ansichtsobjekte für Datenquellen auf den blockierten Laufwerken aktivieren können.<br/> Wird mit <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder::BindToObject oder</strong></a> <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler"><strong>IShellItem::BindToHandler verwendet.</strong></a><br/> Das System unterstützt vom Administrator gesteuerte Richtlinien, die angegebene Laufwerkbuchstaben ausblenden, um Benutzern den Zugriff auf diese Laufwerke über den Windows zu blockieren. Wenn diese Richtlinie aktiv ist, führt dies dazu, dass Ansichtsobjekte und andere Handler, die mit der <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-createviewobject"><strong>IShellFolder::CreateViewObject-Methode</strong></a> erstellt wurden, fehlschlagen, wenn sie auf Laufwerken aufgerufen werden, die durch die Richtlinie blockiert werden.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_BIND_DELEGATE_CREATE_OBJECT"></span><span id="str_bind_delegate_create_object"></span><dl> <dt><strong>STR_BIND_DELEGATE_CREATE_OBJECT</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Eingeführt in Windows Vista</strong>. Geben Sie diesen Bindungskontext an, damit die <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder::BindToObject-Methode</strong></a> das vom <em>pbc-Parameter</em> angegebene Objekt verwendet, um das Zielobjekt zu erstellen. In diesem Fall muss das objekt, das durch den <em>Parameter "parameters"</em> im <a href="/windows/desktop/api/objidl/nf-objidl-ibindctx-registerobjectparam"><strong>IBindCtx::RegisterObjectParam-Aufruf</strong></a> angegeben wird, die <a href="/windows/desktop/api/Propsys/nn-propsys-icreateobject"><strong>ICreateObject-Schnittstelle</strong></a> implementieren. <br/> Wird mit <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder::BindToObject oder</strong></a> <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler"><strong>IShellItem::BindToHandler verwendet.</strong></a><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_BIND_FOLDER_ENUM_MODE"></span><span id="str_bind_folder_enum_mode"></span><dl> <dt><strong>STR_BIND_FOLDER_ENUM_MODE</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Eingeführt in Windows 7</strong>. Wird an <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arseDisplayName</strong></a> mit <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-folder_enum_mode"><strong></strong></a> einem FOLDER_ENUM_MODE übergeben, um den Enumerationsmodus des analysierten Elements zu steuern. Der <strong>FOLDER_ENUM_MODE</strong> wird im Bindungskontext über ein Objekt übergeben, das <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iobjectwithfolderenummode"><strong>IObjectWithFolderEnumMode implementiert.</strong></a> <br/> Elemente mit unterschiedlichen Enumerationsmodi unterscheiden sich kanonisch (SHCIDS_CANONICALONLY), da sie unterschiedliche Sätze von Elementen aufzählen.<br/> Wenn ein Element den Enumerationsmodus nicht unterstützt (da es kein Ordner ist oder keinen Enumerationsmodus bietet), wird es im Standardenumerationsmodus erstellt.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_BIND_FOLDERS_READ_ONLY"></span><span id="str_bind_folders_read_only"></span><dl> <dt><strong>STR_BIND_FOLDERS_READ_ONLY</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Eingeführt in Windows 7</strong>. Übergeben an <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arseDisplayName</strong></a> zusammen <strong>mit STR_FILE_SYS_BIND_DATA.</strong> Dies erzwingt eine einfache Analyse und Desktop.ini dateien entlang des Pfads, aus dem eine lokalisierte Namenszeichenfolge zu erhalten ist. Dadurch wird die Suche nach Ordnern entlang des Pfads vermieden, was im Fall eines Ordners, der einen Server oder eine Freigabe darstellt, viel Zeit und Ressourcen dauern kann. Desktop.ini Dateien werden an einigen Speicherorten zwischengespeichert, sodass sie mindestens so effizient sind wie die Suche nach Ordnerattributen und die anschließende Suche nach dem Desktop.ini, wenn dieser Ordner ou int als schreibgeschützt festlegen soll.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_BIND_FORCE_FOLDER_SHORTCUT_RESOLVE"></span><span id="str_bind_force_folder_shortcut_resolve"></span><dl> <dt><strong>STR_BIND_FORCE_FOLDER_SHORTCUT_RESOLVE</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Eingeführt in Windows XP SP2</strong>. Geben Sie diesen Bindungskontext an, um eine Ordnerverknüpfung zu erzwingen, um den Link aufzulösen, der auf das Ziel verweist. <br/> Eine Ordnerverknüpfung ist ein Ordnerelement, das auf ein anderes Ordnerelement im gleichen Namespace verweist. Dabei wird ein Link (Verknüpfung) verwendet, um die IDList des Ziels zu speichern. Der Link wird aufgelöst, um das Ziel nachzuverfolgungen, falls es verschoben oder umbenannt wird. Beispielsweise können der Ordner Windows XP <strong>My Network Places</strong> und der Ordner Windows Vista <strong>Computer</strong> Ordnerverknüpfungen enthalten, die mit dem Assistenten zum Hinzufügen von <strong>Netzwerkspeicherorten erstellt</strong> wurden. Zur Verbesserung der Leistung löst die <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder::BindToObject-Methode</strong></a> standardmäßig keine Links zum Netzwerkordner auf.<br/> Wird mit <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder::BindToObject oder</strong></a> <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler"><strong>IShellItem::BindToHandler verwendet.</strong></a> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_DONT_PARSE_RELATIVE"></span><span id="str_dont_parse_relative"></span><dl> <dt><strong>STR_DONT_PARSE_RELATIVE</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Eingeführt in Windows XP</strong>. Geben Sie diesen Bindungskontext an, um zu verhindern, dass ein Aufruf der <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arseDisplayName-Methode</strong></a> im <strong>Desktopordner</strong> relative Pfade als relativ zum Desktop behandelt. in einem solchen Fall schlägt die Analyse fehl, wenn dieser Bindungskontext angegeben wird.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_DONT_RESOLVE_LINK"></span><span id="str_dont_resolve_link"></span><dl> <dt><strong>STR_DONT_RESOLVE_LINK</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Eingeführt in Windows Vista</strong>. Geben Sie diesen Bindungskontext an, um <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>ein IShellItem anweisen,</strong></a> das link-Ziel, das bei Verwendung der BHID_LinkTargetItem-GUID in <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler"><strong>IShellItem::BindToHandler</strong></a>erhalten <strong>wurde,</strong> nicht aufzulösen.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_FILE_SYS_FIND_DATA"></span><span id="str_file_sys_find_data"></span><dl> <dt><strong>STR_FILE_SYS_FIND_DATA</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Eingeführt in Windows XP</strong>. Geben Sie diesen Bindungskontext an, um Dateimetadaten für die <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arseDisplayName-Methode</strong></a> anzugeben, die verwendet wird, anstatt zu versuchen, die eigentlichen Dateimetadaten abzurufen. Das zugeordnete Objekt muss <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifilesystembinddata"><strong>IFileSystemBindData implementieren</strong></a> und kann optional auch <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifilesystembinddata2"><strong>IFileSystemBindData2 implementieren.</strong></a> Standardmäßig überprüft die <strong>IShellFolder::P arseDisplayName-Methode,</strong> ob die Datei vorhanden ist, und verwendet die tatsächlichen Metadaten der Datei, um die ID-Liste zu füllen.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_FILE_SYS_BIND_DATA_WIN7_FORMAT"></span><span id="str_file_sys_bind_data_win7_format"></span><dl> <dt><strong>STR_FILE_SYS_BIND_DATA_WIN7_FORMAT</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Eingeführt in Windows 8.1</strong>. Geben Sie diesen Bindungskontext <strong>an,</strong> um anzugeben, dass die im bindungskontext STR_FILE_SYS_FIND_DATA bereitgestellten Daten verwendet werden sollen, um eine ItemID-Liste im format Windows 7 zu erstellen.&quot;<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GET_ASYNC_HANDLER"></span><span id="str_get_async_handler"></span><dl> <dt><strong>STR_GET_ASYNC_HANDLER</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Eingeführt in Windows 7</strong>. Geben Sie diesen Bindungskontext an, wenn der Handler im selben Thread wie die Benutzeroberfläche abgerufen wird. Alle speicherintensiven Aktivitäten, z. B. solche mit Datenträger- oder Netzwerkzugriff, sollten vermieden werden.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GPS_BESTEFFORT"></span><span id="str_gps_besteffort"></span><dl> <dt><strong>STR_GPS_BESTEFFORT</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Eingeführt in Windows Vista</strong>. Geben Sie diesen Bindungskontext an, wenn Sie einen <a href="/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage"><strong>IPropertySetStorage- oder</strong></a> <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>IPropertyStore-Handler</strong></a> anfordern. Dieser Wert wird mit <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder::BindToObject verwendet.</strong></a> Weitere Informationen <a href="/windows/desktop/api/propsys/ne-propsys-getpropertystoreflags"><strong>finden GPS_BESTEFFORT</strong></a> -Flag.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GPS_DELAYCREATION"></span><span id="str_gps_delaycreation"></span><dl> <dt><strong>STR_GPS_DELAYCREATION</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Eingeführt in Windows Vista</strong>. Geben Sie diesen Bindungskontext an, wenn Sie einen <a href="/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage"><strong>IPropertySetStorage- oder</strong></a> <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>IPropertyStore-Handler</strong></a> anfordern. Dieser Wert wird mit <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder::BindToObject verwendet.</strong></a> Weitere Informationen <a href="/windows/desktop/api/propsys/ne-propsys-getpropertystoreflags"><strong>finden GPS_DELAYCREATION</strong></a> -Flag.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GPS_FASTPROPERTIESONLY"></span><span id="str_gps_fastpropertiesonly"></span><dl> <dt><strong>STR_GPS_FASTPROPERTIESONLY</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Eingeführt in Windows Vista</strong>. Geben Sie diesen Bindungskontext an, wenn Sie einen <a href="/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage"><strong>IPropertySetStorage- oder</strong></a> <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>IPropertyStore-Handler</strong></a> anfordern. Dieser Wert wird mit <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder::BindToObject verwendet.</strong></a> Weitere Informationen <a href="/windows/desktop/api/propsys/ne-propsys-getpropertystoreflags"><strong>finden GPS_FASTPROPERTIESONLY</strong></a> -Flag.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GPS_HANDLERPROPERTIESONLY"></span><span id="str_gps_handlerpropertiesonly"></span><dl> <dt><strong>STR_GPS_HANDLERPROPERTIESONLY</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Eingeführt in Windows Vista</strong>. Geben Sie diesen Bindungskontext an, wenn Sie einen <a href="/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage"><strong>IPropertySetStorage- oder</strong></a> <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>IPropertyStore-Handler</strong></a> anfordern. Dieser Wert wird mit <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder::BindToObject verwendet.</strong></a> Weitere Informationen <a href="/windows/desktop/api/propsys/ne-propsys-getpropertystoreflags"><strong>finden GPS_HANDLERPROPERTIESONLY</strong></a> -Flag.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GPS_NO_OPLOCK"></span><span id="str_gps_no_oplock"></span><dl> <dt><strong>STR_GPS_NO_OPLOCK</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Eingeführt in Windows 7</strong>. Geben Sie diesen Bindungskontext an, wenn Sie einen <a href="/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage"><strong>IPropertySetStorage- oder</strong></a> <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>IPropertyStore-Handler</strong></a> anfordern. Dieser Wert wird mit <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder::BindToObject verwendet.</strong></a> Weitere Informationen <a href="/windows/desktop/api/propsys/ne-propsys-getpropertystoreflags"><strong>finden sie GPS_NO_OPLOCK</strong></a> -Flag.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GPS_OPENSLOWITEM"></span><span id="str_gps_openslowitem"></span><dl> <dt><strong>STR_GPS_OPENSLOWITEM</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Eingeführt in Windows Vista</strong>. Geben Sie diesen Bindungskontext an, wenn Sie einen <a href="/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage"><strong>IPropertySetStorage- oder</strong></a> <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>IPropertyStore-Handler</strong></a> anfordern. Dieser Wert wird mit <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder::BindToObject verwendet.</strong></a> Weitere Informationen <a href="/windows/desktop/api/propsys/ne-propsys-getpropertystoreflags"><strong>finden GPS_OPENSLOWITEM</strong></a> -Flag.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_IFILTER_FORCE_TEXT_FILTER_FALLBACK"></span><span id="str_ifilter_force_text_filter_fallback"></span><dl> <dt><strong>STR_IFILTER_FORCE_TEXT_FILTER_FALLBACK</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Windows Nur Vista.</strong> Geben Sie diesen Bindungskontext an, um einen Aufruf der <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder::BindToObject-Methode</strong></a> zu verursachen, die die <a href="/windows/desktop/api/filter/nn-filter-ifilter"><strong>IFilter-Schnittstelle</strong></a> für ein Dateisystemobjekt an fordert, einen Textfilter zurückzuerlangen, wenn kein anderer Filter verfügbar ist. Dieser Wert ist ab 7 nicht Windows definiert.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_IFILTER_LOAD_DEFINED_FILTER"></span><span id="str_ifilter_load_defined_filter"></span><dl> <dt><strong>STR_IFILTER_LOAD_DEFINED_FILTER</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Windows Nur Vista.</strong> Geben Sie diesen Bindungskontext an, um einen Aufruf der <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder::BindToObject-Methode</strong></a> zu verursachen, die die <a href="/windows/desktop/api/filter/nn-filter-ifilter"><strong>IFilter-Schnittstelle</strong></a> für ein Dateisystemobjekt an fordert, keinen Fallbackfilter zurückzurücken, wenn kein registrierter Filter gefunden werden konnte.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_INTERNAL_NAVIGATE"></span><span id="str_internal_navigate"></span><dl> <dt><strong>STR_INTERNAL_NAVIGATE</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Eingeführt in Windows Vista</strong>. Geben Sie diesen Bindungskontext an, um das Laden des Verlaufs aus einem Stream für eine interne Navigation zu ermöglichen, wenn die <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768216(v=vs.85)"><strong>IPersistHistory::LoadHistory-Methode</strong></a> aufgerufen wird. Eine interne Navigation ist eine Navigation innerhalb derselben Ansicht.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_INTERNETFOLDER_PARSE_ONLY_URLMON_BINDABLE"></span><span id="str_internetfolder_parse_only_urlmon_bindable"></span><dl> <dt><strong>STR_INTERNETFOLDER_PARSE_ONLY_URLMON_BINDABLE</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Eingeführt in Windows 7</strong>. Geben Sie diesen Bindungskontext mit STR_PARSE_PREFER_FOLDER_BROWSING an, wenn der Client möchte, dass die Ordnerhandler von Internet Shell eine IDList für eine gültige URL generieren, wenn kein DAV-Typordner für diese URL erstellt werden kann. Die URL wird nicht als vorhanden überprüft. nur die Syntax wird überprüft und überprüft, ob sie über einen registrierten Protokollhandler verfügt.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_ITEM_CACHE_CONTEXT"></span><span id="str_item_cache_context"></span><dl> <dt><strong>STR_ITEM_CACHE_CONTEXT</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Eingeführt in Windows 7</strong>. Geben Sie diesen Bindungskontext an, um Implementierungen von <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arseDisplayName</strong></a> und <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder3-initializeex"><strong>IPersistFolder3::InitializeEx</strong></a> anweisen, speicherintensive Hilfsobjekte zwischenzuspeichern, die über Instanziierungen von Shellelementen hinweg vorhanden sein können, anstatt diese Objekte jedes Mal neu zu erstellen, wenn ein Shellelement erstellt wird. Das zugeordnete Objekt ist ein weiteres Bindungskontextobjekt, das anfänglich leer ist. Dies sollte zu einem separaten Bindungskontextobjekt führen, auf das über <a href="/windows/desktop/api/objidl/nf-objidl-ibindctx-getobjectparam"><strong>IBindCtx::GetObjectParam</strong></a> oder <a href="/windows/desktop/api/objidl/nf-objidl-ibindctx-registerobjectparam"><strong>IBindCtx::Register.ObjectParam zugegriffen wird.</strong></a> <br/> Ein Aufrufer muss dieses Verhalten durch Angabe dieses Bindungskontextparameters beim Aufrufen von <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateitemfromparsingname"><strong>SHCreateItemFromParsingName festlegen.</strong></a> Dadurch optimieren Sie das Verhalten der Bindung an mehrere Analysenamen nacheinander. Die Lebensdauer des Bindungskontextobjekts sollte mehrere Instanzen von Shellelementen und deren einzelne Bindungskontexte umfassen.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_NO_VALIDATE_FILENAME_CHARS"></span><span id="str_no_validate_filename_chars"></span><dl> <dt><strong>STR_NO_VALIDATE_FILENAME_CHARS</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Eingeführt in Windows Vista</strong>. Geben Sie diesen Bindungskontext an, damit ungültige Dateinamenzeichen in Dateinamen angezeigt werden können. Standardmäßig lehnt ein Aufruf der <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arseDisplayName-Methode</strong></a> Zeichen ab, die in Dateinamen ungültig sind. Dieser Bindungskontext ist nur in Verbindung mit dem Bindungskontext STR_FILE_SYS_FIND_DATA sinnvoll.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_PARSE_ALLOW_INTERNET_SHELL_FOLDERS"></span><span id="str_parse_allow_internet_shell_folders"></span><dl> <dt><strong>STR_PARSE_ALLOW_INTERNET_SHELL_FOLDERS</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Eingeführt in Windows Vista</strong>. Geben Sie diesen Bindungskontext an, um einen Aufruf der <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arseDisplayName-Methode</strong></a> im <strong>Ordner Desktop</strong> zum Analysieren von URLs zu aktivieren. Wenn dieser Bindungskontext angegeben wird, überschreibt er <strong><strong>STR_PARSE_PREFER_WEB_BROWSING</strong></strong>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_PARSE_AND_CREATE_ITEM"></span><span id="str_parse_and_create_item"></span><dl> <dt><strong>STR_PARSE_AND_CREATE_ITEM</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Eingeführt in Windows 7</strong>. Geben Sie diesen Bindungskontext an, um die Implementierung von <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arseDisplayName einer</strong></a> Datenquelle anweisen, das Verhalten von <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateitemfromparsingname"><strong>SHCreateItemFromParsingName zu optimieren.</strong></a> <br/> Normalerweise führt <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateitemfromparsingname"><strong>SHCreateItemFromParsingName zwei Bindungsvorgänge</strong></a> für den zu analysierenden Namen aus: eine bis und eine für <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arseDisplayName</strong></a> und eine zum Erstellen des Shellelements. Wenn der <strong>STR_PARSE_AND_CREATE_ITEM-Bindungskontext</strong> unterstützt wird, wird die zweite Bindung vermieden, indem das Shellelement während der <strong>IShellFolder::P arseDisplayName-Bindung</strong> erstellt und das Shellelement über <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iparseandcreateitem-setitem"><strong>IParseAndCreateItem::SetItem gespeichert wird.</strong></a> <strong>SHCreateItemFromParsingName</strong> verwendet dann das gespeicherte Shellelement, anstatt eines zu erstellen.<br/> Dieser Parameter gilt für das letzte Element des Namens, der analysiert wird. Im Namen derC:\Folder1\File.txt &quot; gelten die Daten beispielsweise für File.txt.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_PARSE_DONT_REQUIRE_VALIDATED_URLS"></span><span id="str_parse_dont_require_validated_urls"></span><dl> <dt><strong>STR_PARSE_DONT_REQUIRE_VALIDATED_URLS</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Windows Nur Vista.</strong> Geben Sie an, dass bei der Analyse einer URL für diesen Bindungskontext nicht erforderlich ist, dass die URL vorhanden ist, bevor eine IDList für sie generiert wird. Geben Sie diesen Bindungskontext <strong><strong>zusammen mit STR_PARSE_PREFER_FOLDER_BROWSING an,</strong></strong> wenn der Client möchte, dass die <strong>Ordnerhandler</strong> von Internet Shell eine IDList für die URL generieren, wenn kein DAV-Ordner für die gegebene URL erstellt werden kann.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_PARSE_PARTIAL_IDLIST"></span><span id="str_parse_partial_idlist"></span><dl> <dt><strong>STR_PARSE_PARTIAL_IDLIST</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Eingeführt in Windows Vista</strong>. Geben Sie diesen Bindungskontext an, um das ursprüngliche Element zu übergeben, das neu analysiert wird, wenn dieses Element als <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem-Objekt</strong></a> gespeichert wird, das auch die <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iparentanditem"><strong>IParentAndItem-Schnittstelle</strong></a> implementiert. Vor Windows 7 wurde dieser Wert nicht in einer Headerdatei definiert. Sie kann vom Aufrufer definiert oder als Zeichenfolgenwert von <strong>L &quot; &quot; ParseOriginalItem übergeben werden.</strong> Ab Windows 7 wird der Wert in Shlobj.h definiert. Beachten Sie, dass dies ein anderer Header als die anderen STR-Konstanten ist.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_PARSE_PREFER_FOLDER_BROWSING"></span><span id="str_parse_prefer_folder_browsing"></span><dl> <dt><strong>STR_PARSE_PREFER_FOLDER_BROWSING</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Eingeführt in Windows XP</strong>. Geben Sie diesen Bindungskontext an, um einen Aufruf der <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arseDisplayName-Methode</strong></a> im <strong>Ordner Desktop</strong> zu aktivieren, um URLs so zu analysieren, als ob es sich um Ordner wäre. Verwenden Sie diesen Bindungskontext, um eine Bindung an einen WebDAV-Server herzustellen.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_PARSE_PREFER_WEB_BROWSING"></span><span id="str_parse_prefer_web_browsing"></span><dl> <dt><strong>STR_PARSE_PREFER_WEB_BROWSING</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Eingeführt in Windows Vista</strong>. Geben Sie diesen Bindungskontext an, um einen Aufruf der <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arseDisplayName-Methode</strong></a> in den Analyse-URLs des Desktop-Ordnerformulars zu verhindern. <strong></strong> Dieser Bindungskontext kann <strong><strong></strong></strong>von der -STR_PARSE_ALLOW_INTERNET_SHELL_FOLDERS.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_PARSE_PROPERTYSTORE"></span><span id="str_parse_propertystore"></span><dl> <dt><strong>STR_PARSE_PROPERTYSTORE</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Eingeführt in Windows Vista</strong>. Geben Sie diesen Bindungskontext an, um den von der <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arseDisplayName-Methode</strong></a> verwendeten Standardeigenschaftsspeicher zu überschreiben, und verwenden Sie stattdessen den als bind-Parameter angegebenen Eigenschaftenspeicher. Gilt für Delegatordner.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_PARSE_SHELL_PROTOCOL_TO_FILE_OBJECTS"></span><span id="str_parse_shell_protocol_to_file_objects"></span><dl> <dt><strong>STR_PARSE_SHELL_PROTOCOL_TO_FILE_OBJECTS</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Eingeführt in Windows XP SP2</strong>. Geben Sie diesen Bindungskontext an, um einen Aufruf der <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arseDisplayName-Methode</strong></a> im <strong>Ordner Desktop</strong> zu aktivieren, um die Shell: Präfix notation für den Zugriff auf Dateien zu &quot; &quot; verwenden.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_PARSE_SHOW_NET_DIAGNOSTICS_UI"></span><span id="str_parse_show_net_diagnostics_ui"></span><dl> <dt><strong>STR_PARSE_SHOW_NET_DIAGNOSTICS_UI</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Eingeführt in Windows Vista</strong>. Geben Sie diesen Bindungskontext an, um einen Aufruf der <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arseDisplayName-Methode</strong></a> zu verursachen, um das Dialogfeld für die Netzwerkdiagnose anzuzeigen, wenn die Analyse eines Netzwerkpfads fehlschlägt.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_PARSE_SKIP_NET_CACHE"></span><span id="str_parse_skip_net_cache"></span><dl> <dt><strong>STR_PARSE_SKIP_NET_CACHE</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Eingeführt in Windows Vista</strong>. Geben Sie diesen Bindungskontext an, um einen Aufruf der <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arseDisplayName-Methode</strong></a> zu verursachen, um die Überprüfung des Caches der Netzwerkfreigaben zu überspringen und den Netzwerkserver direkt zu kontaktieren. Informationen zu Netzwerkfreigaben werden zur Verbesserung der Leistung zwischengespeichert, und <strong>IShellFolder::P arseDisplayName</strong> überprüft diesen Cache standardmäßig.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_PARSE_TRANSLATE_ALIASES"></span><span id="str_parse_translate_aliases"></span><dl> <dt><strong>STR_PARSE_TRANSLATE_ALIASES</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Eingeführt in Windows XP</strong>. Geben Sie diesen Bindungskontext an, um analysierte Eigenschaften an die <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arseDisplayName-Methode</strong></a> für einen Delegatnamespace zu übergeben. Der Namespace kann die übergebenen Eigenschaften verwenden, anstatt zu versuchen, den Namen selbst zu analysieren.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_PARSE_WITH_PROPERTIES"></span><span id="str_parse_with_properties"></span><dl> <dt><strong>STR_PARSE_WITH_PROPERTIES</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Windows Nur Vista.</strong> Ein Analysebindungskontext, der verwendet wird, um einen Satz von Eigenschaften und den Namen des Elements beim Aufrufen von <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arseDisplayName zu übergeben.</strong></a> Das Objekt im Bindungskontext implementiert <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>IPropertyStore</strong></a> und wird durch Aufrufen von <a href="/windows/desktop/api/objidl/nf-objidl-ibindctx-getobjectparam"><strong>IBindCtx::GetObjectParam abgerufen.</strong></a><br/> DBFolder ist eine Shell-Datenquelle, die Elemente in Suchergebnissen und abfragebasierten Sichten darstellt. DBFolder ruft diese Elemente ab, indem das Suchsystem Windows wird. Elemente in den Suchergebnissen werden über ein Protokollschema identifiziert, z. B. &quot; datei: &quot; oder &quot; mapi: &quot; . DBFolder stellt das Verhalten für diese Elemente durch Delegieren an Shell-Datenquellen zur Verfügung, die für diese Protokolle erstellt werden. Weitere Informationen finden Sie unter Entwickeln von <a href="/previous-versions/bb233544(v=msdn.10)">Protokollhandler-Add-Ins.</a><br/> Wenn DBFolder seinen Analysevorgang an die Shell-Datenquellen delegiert, die Windows Search-Protokolle unterstützen, bietet dieser Bindungskontext Zugriff auf Werte, die im Abfrageergebnis für dieses Element zurückgegeben wurden. Hierzu gehören folgende Elemente:<br/>
<ul>
<li><a href="/windows/desktop/properties/props-system-itemtype">System.ItemType</a> (PKEY_ItemType)</li>
<li><a href="/windows/desktop/properties/props-system-parsingpath">System.ParsingPath</a> (PKEY_ParsingPath)</li>
<li><a href="/windows/desktop/properties/props-system-itempathdisplay">System.ItemPathDisplay</a> (PKEY_ItemPathDisplay)</li>
<li><a href="/windows/desktop/properties/props-system-itemnamedisplay">System.ItemNameDisplay</a> (PKEY_ItemNameDisplay)</li>
</ul>
<br/> Dieser Bindungskontext kann auch verwendet werden, um ein DBFolder-Element zu analysieren, wenn ein Client über einen Satz von Eigenschaften verfügt, die das Element definieren. In diesem Fall sollte ein leerer Name an <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arseDisplayName übergeben werden.</strong></a><br/> Vor Windows 7 wurde dieser Wert nicht in einer Headerdatei definiert. Sie kann vom Aufrufer definiert oder als Zeichenfolgenwert übergeben werden: <code>L&quot;ParseWithProperties&quot;</code> . Ab Windows 7 wird der Wert in Shlobj.h definiert. Beachten Sie, dass dies ein anderer Header ist als der, an dem die anderen STR-Konstanten definiert sind.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_PROPERTYBAG_PARAM"></span><span id="str_propertybag_param"></span><dl> <dt><strong>STR_PROPERTYBAG_PARAM</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Eingeführt in Windows 8</strong>. Geben Sie diesen Bindungskontext an, um anzugeben, dass es sich bei dem Bindungskontextparameter um eine Eigenschaftentüte (<a href="/windows/win32/api/oaidl/nn-oaidl-ipropertybag"><strong>IPropertyBag</strong></a>) handelt, mit der VARIANT-Werte im Bindungskontext übergeben werden. Weitere Informationen finden Sie im Abschnitt "Hinweise".<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_SKIP_BINDING_CLSID"></span><span id="str_skip_binding_clsid"></span><dl> <dt><strong>STR_SKIP_BINDING_CLSID</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Eingeführt in Windows XP</strong>. Geben Sie diesen Bindungskontext an, damit Aufrufe der <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>Methoden IShellFolder::P arseDisplayName</strong></a> oder <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder::BindToObject</strong></a> beim Analyse- oder Bindungsing eine bestimmte Shellnamespaceerweiterung ignorieren. Die CLSID des zu ignorierenden Namespace wird von der <a href="/windows/desktop/api/objidl/nf-objidl-ipersist-getclassid"><strong>IPersist::GetClassID-Methode</strong></a> des bind-Parameters bereitgestellt. <br/>
<blockquote>
[!Note]<br />
Dieser In Windows 2000 SP3 eingeführte Wert wurde in Shlobj.h bis Windows XP definiert, als er in Shobjidl.h verschoben wurde.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_TRACK_CLSID"></span><span id="str_track_clsid"></span><dl> <dt><strong>STR_TRACK_CLSID</strong></dt> </dl></td>
<td style="text-align: left;">Wird nicht verwendet.<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Hinweise

Bindungskontexte werden verwendet, um optionale Parameter an Funktionen zu übergeben, die über einen IBindCtx-Parameter \* verfügen. Diese Parameter werden als COM-Objekte ausgedrückt und implementieren möglicherweise Schnittstellen, die zum Modellieren der Parameterdaten verwendet werden. Einige Bindungskontexte stellen einen booleschen Wert dar, wobei **TRUE** ein Objekt angibt, das nur [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) implementiert, und FALSE gibt an, dass kein Objekt vorhanden ist.

[**IShellFolder::P arseDisplayName,**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname) [**IShellFolder::BindToObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject) und [**IShellItem::BindToHandler**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler) verwenden einen Bindungskontext, und Sie können diese Parameter über diesen Bindungskontext übergeben.

Einige Bindungskontexte sind spezifisch für bestimmte Datenquellenimplementierungen oder Handlertypen.

Bindungskontextparameter werden für die Verwendung mit einer bestimmten Funktion oder Methode definiert.

Wenn Sie einen Eigenschaftenspeicher über [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder)anfordern, können Sie die Entsprechung von [**GPS \_ DEFAULT**](/windows/win32/api/propsys/ne-propsys-getpropertystoreflags) angeben, indem Sie einen [**NULL-IBindCtx-Parameter**](/windows/win32/api/objidl/nn-objidl-ibindctx) übergeben. Sie können auch die Entsprechung von GPS \_ READWRITE angeben, indem Sie den Modus STGM \_ READWRITE \| STGM \_ EXCLUSIVE im Bindungskontext übergeben.

Der vom STR **\_ PROPERTYBAG \_ PARAM-Bindungskontextobjekt** angegebene Eigenschaftenbehälter enthält zusätzliche Werte, auf die Sie mit den Methoden [**IPropertyBag::Read**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768197(v=vs.85)) und [**IPropertyBag::Write**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768198(v=vs.85)) zugreifen können.



| Eigenschaftenname                                 | type     | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-----------------------------------------------|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| FLAGS \_ FÜR STR-ENUMERATIONSELEMENTE \_ \_                       | VT \_ UI4  | **Eingeführt in Windows 8**. Gibt einen [**SHCONTF-Wert**](/windows/win32/api/shobjidl_core/ne-shobjidl_core-_shcontf) an, der an [**IShellFolder::EnumObjects**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-enumobjects) übergeben werden soll, wenn Sie [**IShellItem::BindToHandler**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler) mit **LDAPID \_ EnumItems** aufrufen.                                                                                                                                                                                                                         |
| STR \_ PARSE \_ EXPLICIT \_ ASSOCIATION \_ SUCCESSFUL | VT \_ BOOL | **Eingeführt in Windows 7.** Die [**IShellFolder::P arseDisplayName-Methode**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname) legt diese Eigenschaft fest, um dem Aufrufer mitzuteilen, dass die zurückgegebene IDList an die mit **STR PARSE WITH EXPLICIT \_ \_ \_ \_ PROGID** angegebene [ProgID](fa-progids.md) oder an die mit **STR PARSE WITH EXPLICIT \_ \_ \_ \_ ASSOCAPP** angegebene Anwendung gebunden wurde. Wenn **STR PARSE EXPLICIT ASSOCIATION \_ \_ \_ \_ SUCCESSFUL** nicht vorhanden ist, wurde die ProgID oder Anwendung nicht an die IDList gebunden. |
| STR \_ PARSE \_ WITH \_ EXPLICIT \_ ASSOCAPP          | VT \_ BSTR | **Eingeführt in Windows 7.** Geben Sie diese Eigenschaft an, damit ein Aufruf der [**IShellFolder::P arseDisplayName-Methode**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname) eine IDList zurückgibt, die an den Dateitypzuordnungshandler für die Anwendung gebunden ist.                                                                                                                                                                                                                                          |
| STR \_ PARSE \_ WITH \_ EXPLICIT \_ PROGID            | VT \_ BSTR | **Eingeführt in Windows 7.** Geben Sie diese Eigenschaft an, damit ein Aufruf der [**IShellFolder::P arseDisplayName-Methode**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname) eine IDList zurückgibt, die an den Dateizuordnungshandler der bereitgestellten [ProgID](fa-progids.md)gebunden ist.                                                                                                                                                                                                                          |



 

Im [Analysebeispiel mit Parametern](samples-parsingwithparameters.md) finden Sie ein Beispiel für die Verwendung von Bindungskontextwerten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Shobjidl.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Shobjidl.idl</dt> </dl> |



 

 
